---
author: Michele
comments: true
date: 2015-11-10 17:58:28+00:00
layout: post
slug: python-bottle-gevent-name-protocol_sslv3-is-not-defined
title: python, bottle, gevent, name 'PROTOCOL_SSLv3' is not defined
wordpress_id: 749
---

Avevo un piccolo progetto python che usava [bottle](http://bottlepy.org/docs/dev/index.html) e [gevent](http://www.gevent.org/), oggi l'ho ripreso in mano, ho provato ad eseguirlo e ho ottenuto l'errore:

```
name 'PROTOCOL_SSLv3' is not defined
```

MA IO NON USO SSL DA NESSUNA PARTE!
Colpa dell'aggiornamento a debian Jessie?
Dopo una ricerca su google ho trovato 2 comandi magici da dare:

```
pip uninstall gevent
apt-get install python-gevent
```

ok, funziona di nuovo, fiuuuu
