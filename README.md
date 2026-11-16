# Sedução PDV para Windows

Instaladores Windows x64 e notas de versão do Sedução PDV.

[Baixar a versão estável](https://github.com/seducao-delivery/pdv-releases/releases/latest)

## Instalação

Baixe o arquivo `.msi` da Release e instale com o usuário Windows que operará o caixa. A instalação inclui o runtime .NET necessário.

Ao abrir, informe a URL da API e a chave do computador cadastrada no painel administrativo. Cada atendente entra com seu próprio usuário.

## Atualizações

O PDV instalado verifica novas versões ao abrir, antes do login. O manifesto assinado e o hash SHA256 do MSI são conferidos antes da instalação. Configurações protegidas e rascunhos ficam fora da pasta do aplicativo e são preservados no upgrade.

As Releases incluem o instalador, `latest.json`, `SHA256SUMS` e a proveniência assinada `bundle.json`. A [chave pública do manifesto](manifest-public.pem) também está disponível neste repositório. Executáveis portáteis e a prévia local não se atualizam automaticamente.

O certificado Authenticode inicial é dedicado ao produto e autoassinado. Ele não representa um editor validado por uma CA pública do Windows; o Windows pode exibir aviso de editor não reconhecido na primeira instalação. O atualizador confere sua própria chave pública fixada e o manifesto RSA-PSS/SHA256, sem adicionar certificados à raiz confiável do Windows.

Este repositório publica os binários e o workflow de distribuição. O código do produto permanece em repositório privado.
