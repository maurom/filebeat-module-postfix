filebeat-module-postfix
=======================

This is a simple [Filebeat](https://www.elastic.co/products/beats/filebeat)
module that parses logs created by [Postfix](http://www.postfix.org/).


Compatibility
-------------

This Postfix module was tested with logs from version 3.1 on Debian 9 Stretch.


Installation
------------

These instructions assume you have a working Filebeat installation.

1. Install module files:

   1. Move these files to your filebeat/module directory:
   
        mv module/postfix /usr/share/filebeat/module/

   2. Create a module descriptor in your modules.d directory:
   
        cp modules.d/postfix.yml.disabled /etc/filebeat/modules.d/

2. Test whether or not the module was picked up by Filebeat:
 
        filebeat modules list | grep postfix
    
3. Enable the module:
 
        filebeat modules enable postfix
    
4. Restart Filebeat (if necessary).

        systemctl restart filebeat
 
 
Copyright & License
-------------------

Copyright © 2019 Mauro A. Meloni

```
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
