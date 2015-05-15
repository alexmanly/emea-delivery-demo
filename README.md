# EMEA Demo Infrastructure

Before you start, ensure you are connected to the Chef VPN!!!

## Setup workstation

1. [Install Git](http://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
2. [Install ChefDK](https://downloads.chef.io/chef-dk/)

## Installing the Delivery CLI

To interact with Delivery we suggest you use our CLI on your
workstation. Currently we support Mac, Ubuntu 14.04, RHEL 6.5, EL 6.5.

##### Mac
1. Download the
   [package](https://s3.amazonaws.com/delivery-packages/cli/deliverycli-20150415170013-1.pkg).
2. Click the package and install

##### Ubuntu

1. ```curl https://packagecloud.io/install/repositories/chef/current/script.deb | sudo bash```
2. ```sudo apt-get install delivery-cli```

##### RHEL/EL (This install is the least tested...)

1. ```curl -o delivery-cli.rpm https://s3.amazonaws.com/delivery-packages/cli/delivery-cli-20150408004719-1.x86_64.rpm```
2. ```sudo yum install delivery-cli.rpm```

## Delivery Server Cluster Settings

* [Delivery Server Web Login](https://10.194.9.71)
  * Enterprise: [emea_enterprise](https://10.194.9.71/e/emea_enterprise/)
    * Organisation: [dbaas](https://10.194.9.71/e/emea_enterprise/#/organizations/dbaas)
      * Project - [httpdbaas](https://10.194.9.71/e/emea_enterprise/#/organizations/dbaas/projects/httpdbaas)
        * [Acceptance](http://10.194.13.23)
        * [Union](http://10.194.15.114)
        * [Rehearsal](http://10.194.9.160) 
        * [Delivered](http://10.194.8.220)
      * Project - [sitedbaas](https://10.194.9.71/e/emea_enterprise/#/organizations/dbaas/projects/sitedbaas)
        * [Acceptance](http://10.194.8.123) 
        * [Union](http://10.194.15.106)
        * [Rehearsal](http://10.194.11.252)
        * [Delivered](http://10.194.8.147)  
  * Build Node: build-node-emea_dc-1 - 10.194.13.100
  * Users - Make sure you log in and enter your SSH public key into your own user profile.  [Instructions to generate an ssh key](https://help.github.com/articles/generating-ssh-keys/)
    * amanly - Alex Manly
    * apop - Alex Pop
    * dromologue - Justin Arbuckle
    * jfitzpatrick - John Fiztpatrick
    * kjohnson - Kimball Johnson
    * mdepue - Matt Depue
    * mducy - Michael Ducy
    * sc0ttruss - Scott Russell
    * yvo - Yvo van Doorn

## Chef Server Settings

* [Manage Chef Web Login](https://10.194.15.21/login)
  * Username: delivery
  * Organisation: emea_org
  
## Analytics Server Settings

* [Analytics Web Login](https://10.194.14.170/#/)
  * Username: delivery
  * Organisation: emea_org
  * Hipchat Room: Analytics Demo Notifications
 
## Splunk Server Settings 

* [Splunk Web Login](http://10.194.15.203:8000/en-US/account/login?return_to=%2Fen-US%2F)
  * Username: admin

## Delivery Demo Instructions

1. [Submit a change](delivery-demo.md)

## LICENSE AND AUTHORS
- Author: Alex Manly (<amanly@chef.io>)

```text
Copyright:: 2015 Chef Software, Inc

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
``
