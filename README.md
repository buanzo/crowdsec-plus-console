CrowdSec + Console
==================

This role adds the CrowdSec PPA, then proceeds to install crowdsec per https://crowdsec.net/#join
along with crowdsec-firewall-bouncer. Optionally, it installs the
whitelist-good-actors collection. Finally, it enrolls it to the Console.

Supported platforms: Debian & Ubuntu

Requirements
------------

An existing account on app.crowdsec.net and the machine enroll code, found on the CrowdSec Console
dashboard, easily copy-pastable into the Role Variables (below).

Role Variables
--------------

crowdsec_enroll_key: A string shown in Crowdsec Console - Required
crowdsec_enroll_name: Name by which the instance will be known by. A
playbook could define it using the ansible_hostname variable.
crowdsec_whitelist_good_actors: false by default.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - role: crowdsec-plus-console
           crowdsec_enroll_key: ENROLL_KEY_ID
           crowdsec_enroll_name: "{{ ansible_hostname }}"
           crowdsec_whitelist_good_actors: true

License
-------

IT

Author Information
------------------

Mail buanzo at buanzo com ar
