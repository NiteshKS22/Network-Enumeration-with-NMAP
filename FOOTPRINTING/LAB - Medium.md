## Nmap the IP
<img width="857" height="175" alt="image" src="https://github.com/user-attachments/assets/dfc3f390-eaab-4e17-b917-e0d787927d96" />
<img width="708" height="439" alt="image" src="https://github.com/user-attachments/assets/0c1dd19c-91b7-4836-9fc0-4f2c309b3cd8" />

## Identified PORT -- 111 and 2049 for enumeration begginening

```
nmap --script nfs* IP -sV -p111,2049
```

<img width="490" height="82" alt="image" src="https://github.com/user-attachments/assets/3c85f622-f568-42e8-b238-f3cc41abef89" />

<img width="875" height="152" alt="image" src="https://github.com/user-attachments/assets/f4f8dfbf-91cc-4b5f-bd6b-9c3327ed3dd3" />

<img width="567" height="392" alt="image" src="https://github.com/user-attachments/assets/e26c56d4-b9f8-4bb8-bb29-b3f0b5a2e771" />

You will get lots of txt file

enumerate them by

```
grep -i 'htb' *.txt
```

this fill scan all the text file and find the htb content from the txt file

<img width="910" height="74" alt="image" src="https://github.com/user-attachments/assets/bf5ff029-871b-4ef7-a466-83dd670ae29e" />

u will get username and now u have to find password 

```
grep -i 'password' *.txt
```

<img width="598" height="79" alt="image" src="https://github.com/user-attachments/assets/68c5229c-2137-40f4-8a42-f322e8360037" />


now u have password also  `alex:lol123!mD`

### Enumerate with Xfreerdp

```
xfreerdp /v:IP /u:alex /p:’lol123!mD’
```

enumerate this server and u will get password for Administrator 

### login to mssm

```
xfreerdp /v:IP /u:Administrator /p:PASSWORD
```


<img width="852" height="511" alt="image" src="https://github.com/user-attachments/assets/1e94c208-3933-4109-8bbc-6f16cffbcd58" />





