### Nasqueron FreeBSD ports

This repository contains internal FreeBSD ports to deploy
specific Nasqueron software we don't intend to upstream to
the official FreeBSD ports tree.

The idea is to provide a port for each application used:

 - if this is a global one, the ports should go to the FreeBSD ports tree
 - if this is a local one, commit the port here

#### How to add a new port

Follow the [FreeBSD porters handbook](https://www.freebsd.org/doc/en/books/porters-handbook/)
or require assistance on Freenode #nasqueron-ops.

Send your commit for review to DevCentral (our Phabricator instance).
The procedure is explained in our [How to contribute code](https://agora.nasqueron.org/How_to_contribute_code) guide.
