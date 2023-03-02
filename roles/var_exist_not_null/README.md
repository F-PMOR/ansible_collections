# pmorry.assertions.var_exist_not_null

assertion that `var` is defined and not null.

## Requirements

none

## Role Variables


This role is using the following variables:

All optionals vars have default values defined in the __role/defaults/mains.yml__ file.

- `vars_to_check` (`list`, required) - the list of the var to test 
- `failed_msg` (`string`, optional) - Message shown when the var will exist but be empty.
  - the message will be preceed by the 'ko' emoji (see below)
  - {{ item }} car be used in message to show the 'var' that is tested
- `success_msg` (`string`, optional) - Message shown when the var exist and not null.
  - the message will be preceed by the 'ok' emoji (see below)
  - {{ item }} car be used in message to show the 'var' that is tested
- `rescue_msg` (`string`, optional) - Message shown in the rescue block, when a var does not exist or is empty. This message will be the last one before the playbook stop. Can be used as a resume of the assert role.
  - the message will be preceed by the 'death of the playbook' emoji (see below)


### default values : 

* `failed_msg`: "var {{ item }} définie mais vide !"  
* `success_msg`: "var {{ item }} bien définie et non vide."  
* `rescue_msg`: "Une variable n'est pas définie ou vide - ARRET du playbook"  




## Dependencies

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

## Example Playbook


Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
- name: test assert via collection
  hosts: server
  gather_facts: false
  vars:
    toto: "test"

  roles:
    - role: pmorry.assertions.var_exist_not_null
      vars:
        vars_to_check:
          - toto
          - tata
        # failed_msg: "La variable {{ item }} n'est pas définie."
        # success_msg: "La variable {{ item }} est bien définie !"
        # rescue_msg: "Une variable n'est pas définie ou vide - ARRET du playbook"

```

## License

BSD

## Author Information

created by : Philippe Morry (philippe 'at' morry.fr)

## emoji used : 


```
ok : 👍✔️
ko : 😞❌
death of the playbook :☠️💥
alerte: ⚠️
```