# Desafio de Ransomware

### Ferramentas

- Kali Linux
- Python

### Procedimento

 - No bash do Kali, crie um diretório chamado "projeto-ransomware"
 - Navegue até o diretório:
   ![mkdir](https://github.com/user-attachments/assets/fecb5852-789b-40ca-91ec-43b09a759088)

- Crie 3 arquivos usando "touch":
   - "teste.txt" (que será o arquivo a ser criptografado)
   - "encrypter.py" (arquivo python que irá criptografar o conteúdo do "teste.txt")
   - "decrypter.py" (arquivo python que irá descriptografar o conteúdo do arquivo "teste.txt.ransomwaretroll", gerado a partir da execução do "encrypter.py")
  ![touch](https://github.com/user-attachments/assets/4b94a8d9-c90d-4617-a4f3-3377982f7c32)

- Insira qualquer texto no arquivo "teste.txt" e salve o documento
  ![teste cript](https://github.com/user-attachments/assets/27de722b-4fe0-4f0e-9b9b-7a85ae2b90c0)

- Crie a lógica dó código de criptografia (encrypter.py) em seu editor de código de sua preferência. Neste exemplo foi utilizado o Nano do Kali:
  ![encrypterpy](https://github.com/user-attachments/assets/369acb3f-457c-4691-848d-7450ecc15a4f)

- Faça o mesmo para o "decrypter.py":
  ![decrypterpy](https://github.com/user-attachments/assets/4b599801-6a08-4889-80ad-b6d44996e219)

### Criptografando

- Para testar o ransomware, execute o "encrypter.py" com o comando ``` python encrypter.py ```. Verifique que após executar o comando, um novo arquivo foi criado, "teste.txt.ransomwaretroll", no lugar do "teste.txt":
  ![teste cript2](https://github.com/user-attachments/assets/27442f1e-d712-4a51-8331-5b2bfe0abe03)

## ObservaçãO: 

- Caso o linux apresente erro ao executar o comando ``` python encrypter.py ``` e exiba o texto abaixo, abra o bash como admin com o ``` sudo su ``` execute o comando ``` pip install pyaes ``` e tente executar o comando novamente.

Traceback (most recent call last):
  File "/home/daniel/projeto-ransomware/encrypter.py", line 2, in <module>
    import pyaes       # Importa a biblioteca 'pyaes' que fornece funcionalidades para criptografia AES.
    ^^^^^^^^^^^^
ModuleNotFoundError: No module named 'pyaes' 

- Abra o arquivo "teste.txt.ransomwaretroll" e veja que a mensagem anterior foi criptografada:
  ![teste cript3](https://github.com/user-attachments/assets/696e6671-5496-4e68-8166-8069587fc423)

### Descriptografando

- Para descriptografar o arquivo, execute o comando ``` python decrypter.py ```. Veja que o arquivo "teste.txt.ransomwaretroll" foi convertido novamente em "teste.txt":
  ![teste cript4](https://github.com/user-attachments/assets/390603cf-b770-4788-a4d9-429087a03e83)

- Abra o arquivo "teste.txt" e veja que a mensagem foi descriptografada:
![teste cript5](https://github.com/user-attachments/assets/5cc8b892-9318-4033-93e2-f20506979f40)
