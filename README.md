# :sparkles: LibreELEC

LibreELEC (LE) é um sistema operacional com o necessário para rodar o Kodi.<br>
O Tvheadend é usado como servidor de streaming (o que permite ver até três canais de diferentes frequências) no aparelho.

## :hammer: Status <br>
Aparelho: <i>Pixel Plus</i><br>
SoC: <i>Hi3798Cv200</i><br>
Decodificação de vídeo (via hardware): <i>MPEG-4 / MPEG-2 / H.264 / H.265 / VC1</i><br>
HDR: <i>HDR10/HLG</i><br>
Tuner: <i>DVB-C (cabo)</i><br>
Versão: <i>LibreELEC 12</i><br>
Kernel: <i>v6.1.38</i><br>
Kodi: <i>Omega - v21</i><br>
Status: <i>Andamento</i><br>

## :information_source: Instalação <br>

A instalação é similar a do Debian/E2. E roda no SD.<br>
Baixe os arquivos .upk e .img.gz mais recentes [aqui](https://github.com/HisiELEC/LibreELEC/releases/tag/11.80.5.2023.12.28).

1. Aplique a atualização .upk no Android
2. Grave a imagem do LibreELEC no SD usando dd (Linux) ou Win32DiskImager (Windows - descompacte img.gz e use o programa).<br>
`gunzip -c LibreELEC-Hisilicon.arm-*.img.gz | sudo dd of=/dev/sdX conv=fsync`
3. Insira o SD no aparelho e aperte a tecla azul para iniciar o LibreELEC.
4. Ao iniciar o Kodi, será necessário instalar alguns add-ons para o funcionamento da TV. Pode-se instalar manualmente os add-ons (lista abaixo) e configurá-los ou restaurar uma imagem.
5. Vamos restaurar uma imagem com os add-ons. No kodi, aperte a tecla vermelha e vá em <b>Restaurar imagem</b>.
<img src="https://i.imgur.com/IEYlqq4.png">
6. Após baixar a imagem, confirme a restauração. Vai reiniciar e aparecerá RSTR no visor do aparelho. Aguarde.<br>
7. Ao fim. Configure oscam em http://ip_do_aparelho:8888/ com os respectivos dados.<br>
8. Faça busca de canais diretamente em http://ip_do_aparelho:9981/ ou aperte a tecla verde e vá em <b>Busca de canais</b> e entre com frequência onde tenha canais na sua região (ex: 465).<br>
<img src="https://i.imgur.com/42IiNaU.png">
<img src="https://i.imgur.com/OawbK4U.png">
9. Talvez seja necessário reiniciar.<br>
10. Para atualizar EPG enquanto assiste TV, desative "Impedir atualizações durante a reprodução".<br>
<img src="https://i.imgur.com/6zUOrEW.png">


## :heavy_check_mark: Add-ons necessários
* Tvheadend HTSP Client - pvr.hts
* Tvheadend Server 4.3 (Alpha) - service.tvheadend43
* OSCam - service.softcam.oscam
* TVheadend Setup

## :cd: Atualizações
Não é necessário aplicar .upk no Android. <br>
Já que o kernel do LE é atualizado junto com o sistema.<br>
Para atualizar, envie o arquivo .tar para pasta /storage/.update ou ponha o canal em <br>LibreELEC-11.0</b> e vá em Atualizações-> Versões Disponíveis.<br>

<img src="https://i.imgur.com/mmpovHJ.png">

## :blue_book: A ser implementado (quem sabe):
* Transcode de vídeo via hardware para TV
* Configuração de imagem: brilho, contraste, nitidez etc.
* Configuração recursos de imagem 


## :six_pointed_star: Informações adicionais
* TVheadend => http://ip_do_aparelho:9981/ <br>
* oscam => http://ip_do_aparelho:8888/ - usuário: oscam | senha: oscam<br>
* Samba => Usuário: libreelec | Senha: libreelec<br>
* SSH =>  Usuário: root | Senha: libreelec

