vm-server
=========

Helper scripts for running/maintaining a Virtual Box VM server.

Install
-------

Clone this repo.
Read-only:

        $ git clone git://github.com/jmcaffee/vm-server.git

or Read-Write:

        $ git clone git@github.com:jmcaffee/vm-server.git

Change into the directory.

        $ cd vm-server

Run `bin/install.run` as `sudo` or `root` to create helpful links in `/usr/local/bin`.

        $ sudo ./bin/install.run

Profit!

Summary
-------

These scripts/commands help moderate/maintain a VirtualBox Headless server
running on Ubuntu/Debian.

Within the root directory of this project a number of directories are
created:

+ machines - where the VMs are located
+ isos     - keep your OS image files here
+ vmdks    - got VMDKs? Keep them here
+ bin      - all of the commands, and the un/install scripts

License
-------
   Copyright 2013 Jeff McAffee

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.

