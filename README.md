# Ansible Collection - f_pmor.assertions

A reusable collection of assertions roles.


This collection provide :

* `f_pmor.assertions/var_exist_not_null` - assertions on vars to check if a var (or list of vars) are well defined and are not null.
* `f_pmor.assertions/hashi_kv2_test_connect` - assertions to check if the connexion to and hashicorps vault (v2) is passed with success or not.

## requirements
nothing

## installing the collection
Install this collection locally:

```
ansible-galaxy collection install f_pmor.assertions -p /path/to/collections
```
Then you can use the roles from the collection in your playbooks.


## using

please, have a look in the readme of earch roles

# Other collection of assertions

Another assertions collection is available in ansible galaxy, so the assertions that ever exist in the 'marcwrobel' collection will not be reimplemented in this collection.

* [marcwrobel collection](https://github.com/marcwrobel/ansible-collection-assertions)

 Documentation for the collection.


# Comments

this is my first collections, so update will be available quicky with news roles and updates.

