
# method 1

# concatenate .CRT and .CA bundle
cat example.com.crt example.com.ca-bundle > ssl-bundle.crt
# concatenate .CRT with KEY
cat ssl-bundle.crt example_key.txt > ssl.pem

# method 2
cat example.com.crt example.com.ca-bundle > ssl-bundle.pem
upload .pem + key seperately

you can upload ssl.pem
test ssl 

openssl s_client -crlf -connect example.com:PORT
