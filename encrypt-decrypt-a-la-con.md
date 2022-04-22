# encrypt

On fait un  bin2hex, base64.

**Algo en php :**

    $basename = '64646464646464_testjpiouuu25.ts';  
	$aestoken = bin2hex($basename);  
	$aestoken = base64_encode($aestoken);
	var_dump($aestoken);

Cela donne :

	string(84) "MzYzNDM2MzQzNjM0MzYzNDM2MzQzNjM0MzYzNDVmNzQ2NTczNzQ2YTcwNjk2Zjc1NzU3NTMyMzUyZTc0NzM="

# decrypt

On fait un base64 decode, hex2bin.

**Algo en Pyhton**

	import binascii
	import base64

	token = 'MzYzNDM2MzQzNjM0MzYzNDM2MzQzNjM0MzYzNDVmNzQ2NTczNzQ2YTcwNjk2Zjc1NzU3NTMyMzUyZTc0NzM='
	token = base64.b64decode(token)
	file_path = binascii.unhexlify(token)
	file_path = file_path.decode()

	print(file_path)

Cela donne :

	64646464646464_testjpiouuu25.ts
