# Simulando um Ataque de Brute-Force de Senhas com Medusa e Kali Linux

Passo a passo do que eu aprendi no curso de cibersegurança na DIO.

---

## Passo 1 - Virtualbox com Kali Linux e Metasploitable2

Configuração inicial do ambiente de laboratório utilizando o Oracle VirtualBox, contendo as máquinas virtuais do Kali Linux (sistema atacante) e do Metasploitable2 (sistema alvo vulnerável).


"<img width="813" height="573" alt="1VirtualboxKaliLinuxeMetasportable2" src="https://github.com/user-attachments/assets/9c902cf0-e7d2-42b8-940f-dd32ab34ec4b" />

---

## Configuração de Rede no Kali Linux

Ajuste das configurações de rede do Kali Linux no VirtualBox para garantir a comunicação isolada e segura com a máquina alvo através de uma Rede NAT.
"<img width="813" height="573" alt="<img width="903" height="518" alt="2configuracao deredenoKali Linux" src="https://github.com/user-attachments/assets/a7781438-bb7f-4da0-be79-e257d3fd2df8" />
" src="https://github.com/user-attachments/assets/9c902cf0-e7d2-42b8-940f-dd32ab34ec4b" />


---

## Configuração de Rede no Metasploitable2

Configuração idêntica da placa de rede para o Metasploitable2, permitindo que ambas as máquinas virtuais enxerguem uma a outra no mesmo ambiente de testes.

<p align="center">
  <img src="3configurcaoderedenoMeasploitable2.jpg" alt="Configuração de rede no Metasploitable2" width="700">
</p>
