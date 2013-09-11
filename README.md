SNORQL-CM
=========

About
-----

SNORQL is an AJAXy front-end for exploring an RDF SPARQL endpoint, and SNORQL-CM is its modified version for syntax highlighting of a SPARQL query.
SNORQL-CM utilizes CodeMirror ( http://codemirror.net/ ) which is a versatile text editor implemented in JavaScript for web browsers.

Installation
------------

1. Clone from github.
  ```
  $ git clone https://github.com/dbcls/SNORQL-CM.git
  ```

1. Copy snorql-cm directory to your webserver's directory.
  ```
  $ cp -rp SNORQL-CM/snorql-cm /path/to/your/webserver/directory/
  ```

Configuration
-------------

1. Add reverse proxy configurations to your Apache conf file.
  ```
  ProxyRequests Off
  <Proxy *>
    Order deny,allow
    Allow from all 
  </Proxy>
  ProxyPass /sparql http://your.sparql/endpoint
  ProxyPassReverse /sparql http://your.sparql/endpoint
  ```

1. Change endpoint path at sparql.js to change this.\_endpoint.
  ```
  this._endpoint = 'http://webserver/sparql';
  ```

Copyrights
----------

SNORQL was originally created by Richard Cyganaik ( http://richard.cyganiak.de/ ) for the D2R server project ( http://www4.wiwiss.fu-berlin.de/bizer/d2r-server/ ), and Database Center for Life Science ( http://dbcls.rois.ac.jp/ ) modified the following files.  

 * ./snorql-cm/index.html
 * ./snorql-cm/snorql.js
 * ./snorql-cm/style.css 

Licenses
--------

SNORQL-CM is licensed under MIT style license (see ./LICENSE).  
SNORQL is licensed under the Apache 2.0 License ( see ./Apache-2.0-LICENSE ).  
