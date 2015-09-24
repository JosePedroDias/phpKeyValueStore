A simple key value store in PHP using a directory in the file system.
Reused most of my code from the paste repos.



# supported operations


`GET ?op=list`

returns array of keys



`GET ?op=exists&id=<key>`

returns true iif key exists



`GET ?op=load&id=<key>`

return JSON document



`POST ?op=save&id=<key>`

if body is empty, deletes the key and should return "deleted"
otherwise saves the document and should return "saved"



# setup

i. the current directory must be served by a PHP-capable webserver such as Apache 2.


ii. in it create a directory named pastes

    mkdir pastes


iiia. its ownership to the apache user

    chown www-data pastes


iiib. (alternative) add permission for everyone to write in it

    chmod a+w pastes
