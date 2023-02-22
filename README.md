# [RavenDB](https://ravendb.net/)

RavenDB is an open-source fully ACID document-oriented database written in C#, developed by Hibernating Rhinos Ltd. 
First release of RavenDB was in may 2010.
With a RavenDB database you can set up a NoSQL data architecture or add a NoSQL layer to your current relational database.
RavenDB stores data as JSON documents and can be deployed in distributed clusters.

## Supported Platforms
* Windows
* Linux
* Docker
* MacOS
* Raspberry Pi

## Instalation
You can download ravendb from [official site](https://ravendb.net/download) for any supported platform

Docker
```
docker pull ravendb/ravendb
```

Linux (highly recommend updating your Linux OS prior to launching the RavenDB server)
```
wget -O ravendb.tar.bz2 https://hibernatingrhinos.com/downloads/RavenDB%20for%20Linux%20x64/latest
tar xvjf ravendb.tar.bz2
```

## Setup
You can setup RavenDB manualy or use setup wizard.
I will use wizard for unsecure setup.

Firstly we need to unpack RavenDB archive in some folder.

Secondly we need to open run file "run.ps1"
In your browser will open setup wizard.

Choose "New Cluster" field.

Choose "Unsecure" mode.

Nextly you can set the settings you need, 
in my case this will be default ports with ip "127.0.0.1"

When configuration completed click "Restart server"
You will be on RavenDB GUI main page.

## Usage
RavenDB use own SQL-like query language named RQL (Raven Query Language)
In RavenDB all documents grouped by collections

#### CREATE
```

```
#### SELECT
```
from '@all_docs'
```
or if we want to see all users
```
from 'users'
```
#### UPDATE
("Patch" field)
```
from Users as u
where Name = '123'
update 
{
   u.age = '20';
}

```
#### DELETE
```
from "@all_docs"
update 
{
   del('user123');
}
```




## Links
https://github.com/ravendb/book/blob/v4.0/Ch09/Ch09.md



