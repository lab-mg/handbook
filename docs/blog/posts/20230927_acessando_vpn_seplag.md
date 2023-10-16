---
date: 2023-09-27
authors: [gabrielbdornas]
comments: true
categories:
  - DCD
---

# Acessando VPN SEPLAG

Neste post pretendo mostrar os passos seguidos para acessar a VPN da SEPLAG na CAMG.
Os tutoriais utilizados estavam, na maioria dos casos, voltados para utilização com Windows.
Como este não era meu caso, faço este registro para instalação e utilização em sistemas operacionais Linux[^1].

<!-- more -->

## VPN virtual

O primeiro passo sugerido no manual oficial (solicitar este pdf para equipe da [DDT](https://www.mg.gov.br/planejamento/pagina/geral/quem-e-quem#:~:text=Diretoria%20de%20Desenvolvimento%20Tecnol%C3%B3gico)) é a instalação do programa [Virtual Machine Viewer](https://releases.pagure.org/virt-viewer/virt-viewer-x64-11.0-1.0.msi), que no Linux realizei via `sudo apt install virt-viewer`.

Próximo passo solicita entrar [neste link](https://stsad.prodemge.gov.br/vpn/PROD_SEPLAG_VDI/vpn-n2.html)[^2].
Após autenticação será possível acessar o manual de [instalação](https://stsad.prodemge.gov.br/vpn/Manual-OpenVPN-Linux.pdf) da ferramenta OpenVPN e os arquivos necessários para seu funcionamento.
Para facilitar a ligação da VPN eu criei o seguinte alias:

```py
vpn='cd /home/<user>/vpnserver-UDP4-1237-User-1237/ \
     && sudo openvpn vpnserver-UDP4-1237-User-1237.ovpn' # (1)
```

1. :man_raising_hand: Os arquivos baixados foram salvos em uma pasta dentro de meu usuário e o comando de acionamento da VPN incluído posteriormente à mudança para este diretório.

VPN no ar, entrar [neste link](https://vdi.prodemge.gov.br/ovirt-engine) e clique no Portal da VM"[^3]. Clique em "Console SPICE" e no arquivo que será baixado. Realize o último login e a máquina será acessada.

## VPN física

O primeiro passo sugerido no manual oficial (solicitar POP para equipe da [DDT](https://www.mg.gov.br/planejamento/pagina/geral/quem-e-quem#:~:text=Diretoria%20de%20Desenvolvimento%20Tecnol%C3%B3gico)) é a instalação dos programa Cisco AnyConnect[^4] e Remmina.

Após baixar o [arquivo](https://expressomgdrive.mg.gov.br/index.php/s/BfYpd62CLmNy2jX) zipado para instalação do Cisco AnyConnect executar:

```
cd ~/Downloads
tar xvf anyconnect-linux64-4.9.06037-predeploy-k9.tar.gz
cd anyconnect-linux64-4.9.06037/vpn
sudo ./vpn_install.sh
```

Programa Cisco AnyConnect instalado basta acessar `seplag.ca.mg.gov.br` com as credenciais de rede[^4].

Para instalar Remmina execute:

```
sudo apt-get update && sudo apt-get upgrade
sudo apt-get install remmina remmina-plugin-rdp remmina-plugin-secret remmina-pluginspice
```

Com a VPN conectada via Cisco AnyConnect basta acessar a máquina utilizando o número da estação iniciado com `D`.

Em caso de dúvidas, consultar também [este](https://gist.github.com/gabrielbdornas/3e1455e0097879f56d58efca1368a3b0) tutorial.

[^1]: Distribuição [Pop!_OS](https://pop.system76.com/).
[^2]: Será solicitado login e senha da rede SEPLAG.
[^3]: Usuário no padrão `usuario@ca.mg.gov.br`.
[^4]: Usuário com padrão `@ca.mg.gov.br`.
