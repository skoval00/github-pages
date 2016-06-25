Title: Update alternatives in Ubuntu
Date: 2015-12-23 4:38

It is possible for several programs  fulfilling  the  same  or  similar functions  to  be  installed  on a single system at the same time.  For example, many systems have several  text  editors  installed  at  once.  This gives choice to the users of a system, allowing each to use a different editor, if desired, but makes it difficult for a program to make a  good  choice for an editor to invoke if the user has not specified a particular preference.

*updates-alternatives(1)*

The easiest way to update alternative is to execute
`update-alternatives --config [alternative generic name]`

List all master alternative  names
`update-alternatives --get-selections`

Display all targets of the link group
`update-alternatives --list [alternative generic name]`

Directory /etc/alternatives contains symlinks to existing alternatives.
