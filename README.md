# Repositório APT Não-Oficial cicpoffs

Repositório APT Não-Oficial do [cicpoffs](https://github.com/adlerosn/cicpoffs).

Use este repositório para instalar e atualizar o pacote cicpoffs com facilidade usando o APT.

Antes de confiar neste repositório, verifique a integridade dos arquivos e considere sua segurança primeiro. Crie seu próprio repositório APT usando este como base ou utilize o meu que buscará atualizações diariamente.

## Requisitos

- Debian/Ubunto ou qualquer distro derivado destes.

## Como instalar o repositório APT

Para que o APT identifique este repositório e seja capaz de instalar e atualizar o Discord você deve executar os códigos abaixo.

```shell
sudo apt remove cicpoffs # Apenas se você instalou o cicpoffs usando o arquivo deb. Neste caso, desinstale primeiro.
wget -qO- https://maeglithier.github.io/cicpoffs-apt/pubkey.asc | sudo gpg --dearmor -o /usr/share/keyrings/cicpoffs-archive-keyring.gpg
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/cicpoffs-archive-keyring.gpg] https://maeglithier.github.io/cicpoffs-apt stable main" | sudo tee /etc/apt/sources.list.d/cicpoffs.list >/dev/null
sudo apt update
sudo apt install cicpoffs -y # Agora você está pronto para instalar e atualizar sempre que uma nova versão lançar.
```

## Como faço para desinstalar este repositório?

Para remover este repositório e sua chave pública você deve executar os códigos abaixo.

```shell
sudo apt remove cicpoffs # Apenas se você ainda não desinstalou o cicpoffs. Neste caso, desinstale primeiro.
sudo rm /usr/share/keyrings/cicpoffs-archive-keyring.gpg
sudo rm /etc/apt/sources.list.d/cicpoffs.list
```

## Checksum

1607fe3d997594e614444a0cf50a7e1f25a5b84a6fe6df5f2ead17e41f585d81  pool/main/c/cicpoffs/cicpoffs_0.2_amd64.deb

## Copyright

O instalador do cicpoffs (arquivos deb) são distribuidos sob a licença GPL-2.0.
