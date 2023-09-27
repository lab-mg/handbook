---
date: 2023-09-27
authors: [gabrielbdornas]
categories:
  - DCD
---

# Acessando VPN SEPLAG

Neste post pretendo mostrar os passos seguidos para acessar a VPN da SEPLAG na CAMG.
Os tutoriais utilizados estavam, na maioria dos casos, voltados para utilização com Windows.
Como este não era meu caso, faço este registro para instalação e utilização em sistemas operacionais Linux[^1].

<!-- more -->

O primeiro passo sugerido no manual oficial (solicitar este pdf para equipe da [DDT](https://www.mg.gov.br/planejamento/pagina/geral/quem-e-quem#:~:text=Diretoria%20de%20Desenvolvimento%20Tecnol%C3%B3gico)) é a instalação do programa [Virtual Machine Viewer](https://releases.pagure.org/virt-viewer/virt-viewer-x64-11.0-1.0.msi), que não possível de ser realizado no Linux.

Próximo passo solicita entrar [neste link](link abaixo:
https://stsad.prodemge.gov.br/vpn/PROD_SEPLAG_VDI/vpn-n2.html)[^2].
Após autenticação será possível acessar o manual de [instalação](https://stsad.prodemge.gov.br/vpn/Manual-OpenVPN-Linux.pdf) da ferramenta OpenVPN e os arquivos necessários para seu funcionamento.
Para facilitar a ligação da VPN eu criei o seguinte alias:

```py
vpn='cd /home/<user>/vpnserver-UDP4-1237-User-1237/ \
     && sudo openvpn vpnserver-UDP4-1237-User-1237.ovpn' # (1)
```

1. :man_raising_hand: Os arquivos baixados foram salvos em uma pasta dentro de meu usuário e o comando de acionamento da VPN incluído posteriormente à mudança para este diretório.


[^1]: Distribuição [Pop!_OS](https://pop.system76.com/).
[^2]: Será solicitado login e senha da rede SEPLAG.
