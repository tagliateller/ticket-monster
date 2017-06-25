# What is this?

This is the TicketMonster distribution, a showcase application for [JBoss Developer Framework](http://jboss.org/jdf).

## What can you find here?

The content of the underlying directories is as follows:

* `demo` - the sources of TicketMonster application - you can build and run it! Follow the [instructions](demo/README.md). Or you can see it at work [here](http://ticketmonster-jdf.rhcloud.com).
* `cordova` - the sources of the TicketMonster Hybrid Mobile (Cordova) application. Follow the [instructions](cordova/README.md) to build and run it.

# OpenShift

oc new-app -f ticketmonster-inmemory.json
oc start-build bc/ticket-monster

oc new-app -f ticketmonster-mysql.json

TODO: noch fkt. der automatische Build nicht (bei mysql)

Zugriff auf MySQL-DB:

oc rsh [pod-name]

> mysql -u root

Beispiele für Templates https://github.com/jboss-openshift/application-templates/blob/master/eap/eap64-mysql-persistent-s2i.json

Aktuell geht die Übergabe der Maven-Args so noch nicht. WIr probieren eine Manipulation der pom.xml.
