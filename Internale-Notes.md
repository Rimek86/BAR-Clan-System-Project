# Internal notes

This document collects important notes / quotes for development from the discord community.

"And for testing, you have automated tests for that. You can also fire up a shell and do things there + check with a db viewer on the side."

"You can start with only create&get&list&delete clan, at the domain layer (no protocol). That can be done first, without touching the protocol. Then you can expand with invite&leave, again, only at the domain layer. Then you can add the concept of member roles. And finally, you can then add these to the protocol handler."

"The clan system is going to be rather similar to the friend system. Because all state is stored in the database, there is no transient information, so you don't need to handle anything from [the session](https://github.com/beyond-all-reason/teiserver/blob/master/lib/teiserver/player/session.ex).
Instead, you can add the logic to the [tachyon handler](https://github.com/beyond-all-reason/teiserver/blob/master/lib/teiserver/player/tachyon_handler.ex), following what's been done for friends.

The main clan logic should all live under lib/teiserver/clan.ex, anything called from the handler should live there. This module can defdelegate to clan_lib (or other) or implement things internally.

The tachyon handler should merely parse the incoming data, delegate the logic to the domain layer (clan.ex), and then serialize the response in the appropriate format. The incoming data is already checked against the [vendored schemas](https://github.com/beyond-all-reason/teiserver/tree/master/priv/tachyon/schema), but you need additional parsing because internally the userId is an integer, but it's a string at the protocol level. This has already been done in that file though, so you can just reuse something.

The stuff under clan.ex or the internals like clan_lib should be tested under test/teiserver/, these do not require spinning up actual ws connection. It should mostly be "setup test data, invoke function, check data in db and return values match expectations".
Then you can test the actual tachyon logic under test/teiserver_web/clan.exs.

As for more general documentation, the relevant ones should be ecto for database access, and regular elixir for the rest. There shouldn't be much OTP concepts involved for clans." => **"That's why I like webstorm for teiserver dev, it has a built-in db viewer"**
