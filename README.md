# Generate-rsa-keys-in-pem
  
run the find_d.py with python 2.7  
  
command:  
python find_d.py > 1.key  
openssl asn1parse -genconf 1.key -out newkey.der  
openssl rsa -in newkey.der -inform der -text -check > key.pem  
  
after running the command above, edit key.pem into following format(delete everything else):  
-----BEGIN RSA PRIVATE KEY-----  
...  
-----END RSA PRIVATE KEY-----  
