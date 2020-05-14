# Changelog
All notable changes to this project will be documented in this file.

## [1.3.4.29]
- Changed groupId of this artifact

## [1.3.4.28]
- Removed final from Config class so it can be inherited in other connectors

## [1.3.4.27]
- Added connector's configuration property 'extensionAttToGet', where you can add attributes. These attributes will be retruned from connector. (each attribute on different line)

## [1.3.4.26]
- pwdLastSet attribute was fixed, when this attribute is provisioned with creation of users

## [1.3.4.25]
- ldapGroups are now returned - Merge strategy is now working
- sAMAccountName is returning - objectGUID can be used as uid
- if you are changing connector version, check system's schema sAMAccountName attribute, it should be - able to read, create, edit and returned by default
- connector's configuration was modified:
 - checkbox 'Permit password change only' was removed
 - checkbox 'Return default attributes' was added - returns all default attributes, if turned off only ldapGroups sAMAccountName and special connector's attributes (like \_\_NAME\_\_)
 - checkbox 'Return DN of primary group' was added - returns distinguished name of primary group with other memberOf/ldapGroups values
