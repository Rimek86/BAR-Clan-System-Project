# Requirement Specification

This document collects all requirements according to this project. Sources are the BAR- and GBAR-Discord Communities and my own ideas.

## Overall requirements

- [ ] RQ-01: The BAR-Lobby shall include an area for a Clan-System.

## Clan list

- [ ] RQ-10: The Clan-System shall include a list of all available clans.
  - [ ] RQ-10.1: The clan list shall provive a search-functionality.
  - [ ] RQ-10.2: The clan list shall provide a button to open the clan profil.
  - [ ] RQ-10.3: The clan list shall show clan id, tag, name and member-count for each clan.
  - [ ] RQ-10.4: For performed reasons that clan system shall provide request to read a limited count of clans in one communication-cycle for one page. (Pagination)

## Clan profil

- [ ] RQ-20: The Clan-System shall include a detailed clan profil.
  - [ ] RQ-20.1: The detailed clan profil shall include a name.
  - [ ] RQ-20.2: The detailed clan profil shall include a clan-tag.
    - [ ] RQ-20.2.1: The clan-tag shall support 3 up to 6 characters. (All characters are allowed.)
  - [ ] RQ-20.3: The detailed clan profil shall include a description.
    - [ ] RQ-20.3.1: The clan description shall provid a implementation which allows to create hyperlinks to external sides.
    - [ ] RQ-20.3.2: The clan desciption shall provide simple formatting like bold, italic, underline, linebreak.
  - [ ] RQ-20.4: The detailed clan profil shall include a logo.
    - [ ] RQ-20.4.1: In a first step there shall be a pool of default-logos in differenz colors which can be selected by the clan administrator.
    - [ ] RQ-20.4.2: In a first step the logo-feature must not support a upload-feature.
- [ ] RQ-20.5: The detailed clan profil shall provide a member list.
  - [ ] RQ-20.5.1: The member list shall show the user names.
  - [ ] RQ-20.5.2: The member list shall show the user online state with the same icons/colors as in the "friend list" (grey/green/zzz).
  - [ ] RQ-20.5.3: The member list shall show the user role.
    - [ ] RQ-20.5.3.1: The roles shall be represented by icons with a "title-text".

## Clan management

- [ ] RQ-30: The Clan-System shall support different clan roles.
  - [ ] RQ-30.1: The clan-system shall support a clan role member.
    - [ ] RQ-30.1.1: The clan-member shall be able to leave the clan.
  - [ ] RQ-30.2: The clan-system shall support a clan role leader.
    - [ ] RQ-30.2.1: The Clan-leader role shall automatically assigned to the creater of the clan.
    - [ ] RQ-30.2.2: The Clan-leader shall be able to invite user.
    - [ ] RQ-30.2.3: The Clan-leader shall be able to kick member.
    - [ ] RQ-30.2.4: The Clan-leader shall be able to decline join-requests.
    - [ ] RQ-30.2.5: The Clan-leader shall be allowed to delete the clan.
  - [ ] RQ-30.3: The clan-system shall support a clan role co-leader.
    - [ ] RQ-30.3.1: The co-leader should have the same permissions as the clan leader, except for deleting the clan.
- [ ] RQ-31: The Clan-System shall support a trial feature which allows the leaders and co-leaders to mark a member as trial
  - [ ] RQ-31.1: The Clan-System shall provide an optional feature to set a timespan for a trial-phase which automatically ends after.
- [ ] RQ-32: The Clan-System shall log the entry-date of each member.

## Overall topics

- [ ] RQ-40: The clan-tag shall be visible in front of each member-name.
  - [ ] RQ-40.1: The clan-tag shall be seperated from the member-name by two blank spaces.
  - [ ] RQ-40.2: The clan-tag shall be indepentant to the user-name. (If the user-name changes it has no impact.)
- [ ] RQ-41: A user shall only be allowed to join one clan. (Multiple clan-membership must not be allowed.)
- [ ] RQ-42: The clan-system shall provide multiple invites for users (MaybI think it has to be handeled by user-profil not directly be clan-system!)
- [ ] RQ-43:

## Clan messaging system (TBD / Rough ideas for future!)

- [ ] RQ-50: Each clan provides a messaging system which can be used by clan-leaders and co-leaders.
  - [ ] RQ-50.1: The messaging system shall provide application handling.
  - [ ] RQ-50.2: The messaging system shall provide "clan-war-requests".

## Discord connection (TBD / Rough ideas for future!)

- [ ] RQ-60: TBD
