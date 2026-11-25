# Avistamos: versão de teste

O **Avistamos** é um app para descobrir, compartilhar e confirmar oportunidades perto de
você: a promoção do mercado, o horário livre no salão, a fornada que acabou de sair. Quem
vê publica com foto e localização, e quem passa por lá confirma se ainda vale. O que a
comunidade confirma ganha selo; o que acabou sai do feed.

## Instalar

**[avistamos.com.br/teste](https://avistamos.com.br/teste/)**: a página baixa a versão
mais recente e explica a instalação passo a passo. Só para Android.

Depois de instalado, o próprio app avisa quando sai versão nova.

## Este repositório

Aqui não tem código: cada versão de teste é uma
[release](https://github.com/carlosmorais-git/avistamos-releases/releases) com o APK
anexado. O app e a página de instalação leem a última release para saber qual é a versão
mais nova, e por isso o repositório é público.

### Publicar uma versão

```powershell
npm run versao:minor     # no repositório do app, pasta mobile/
npm run build:preview    # baixar o APK pelo link do EAS
gh release create v0.2.0 .\avistamos-0.2.0.apk --repo carlosmorais-git/avistamos-releases --title "0.2.0" --notes "O que mudou, em uma ou duas linhas"
```

- A tag é a versão do app com `v` na frente. Sem subir a versão, ninguém recebe o aviso.
- Um `.apk` anexado, do perfil `preview`. As notas aparecem no aviso do app.
- Publicada, não rascunho nem pré-release: os dois ficam fora da `latest`.
