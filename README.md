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
running on Ubuntu/Debian. The commands are mainly wrappers around
VBoxManage and VBoxHeadless.

Ultimately, they're so I don't have to look up the details when I come back
to set up a new VM a month or two down the road.

Within the root directory of this project a number of directories are
created:

+ machines - where the VMs are located
+ isos     - keep your OS image files here
+ vmdks    - got VMDKs? Keep them here
+ bin      - all of the commands, and the un/install scripts

Commands
--------

#### listvms

List VMs that VBox knows about, running or not.

#### runningvms

List VMs that are currently running.

#### vmstatus

Display a VM configuration

    Usage: vmstatus  VM_NAME

#### startvm

Start a stopped VM

    Usage: startvm  VM_NAME  [OPTION]
    
      Surround VM name in quotes if it contains spaces.
    
      OPTIONS
      -v, --vrde      Force VRDE on (Remote Desktop)
      -n, --no-vrde   Force VRDE off
                By default, VRDE setting in config will be used.

#### stopvm

Stop a running VM

    Usage: stopvm  VM_NAME  [STOP_TYPE]
    
      Surround VM name in quotes if it contains spaces.
    
      STOP_TYPE
          savestate  [Default]
          poweroff
          reset

#### deletevm

Delete a registered VM

    Usage:"
        deletevm VMNAME"

#### clonevm

Clone a stopped VM

    Usage: clonevm  SRC_VM_NAME  NEW_VM_NAME  [--newmac | -n]
    
      Surround VM names in quotes if they contain spaces.
    
      -n, --newmac    Generate a new MAC for the network card. Default: no

#### movevm

Move a VM to another location (directory)

    Usage: clonevm  SRC_VM_NAME  DEST_DIR_ROOT
    
      Surround VM name in quotes if it contains spaces.
      DEST_DIR_ROOT should NOT include the VM's dir name.
      Ex:
          If you want a vm named 'test' to end up in the '/machines/test' dir,
          then you should use '/machines' as the dest dir.
    
     WARNING!
     Moving VMs that contain snapshots IS NOT SUPPORTED!
     You should merge your snapshots before moving the VM.
    





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

