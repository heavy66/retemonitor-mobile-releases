# Instalação do ReteMonitor Mobile no Android

Este guia descreve a instalação direta do APK oficial, sem utilizar a Play
Store. O ReteMonitor Mobile requer Android 8.0 ou superior e não exige root.

## Antes de instalar

1. Baixe o APK somente pela página oficial de Releases:
   https://github.com/heavy66/retemonitor-mobile-releases/releases/latest
2. Escolha o arquivo com nome semelhante a:
   `ReteMonitorMobile_vX_X_X_release_assinado.apk`.
3. Não instale APKs renomeados ou recebidos de origem desconhecida.
4. Se desejar conferir a integridade, compare o SHA-256 informado na Release
   com o hash do arquivo baixado.

## Primeira instalação em um Samsung

Os nomes das opções podem variar um pouco conforme a versão da One UI.

1. Abra o APK pela notificação de download ou pelo aplicativo **Meus Arquivos**.
2. O Android poderá informar que aquela fonte não tem permissão para instalar
   aplicativos. Toque em **Configurações**.
3. Ative **Permitir desta fonte** para o aplicativo que abriu o arquivo:
   **Meus Arquivos**, Chrome, Samsung Internet ou outro navegador utilizado.
4. Volte para a tela anterior.
5. Toque em **Instalar**.
6. Ao terminar, toque em **Abrir**.

Também é possível localizar essa autorização manualmente:

1. Abra **Configurações**.
2. Entre em **Segurança e privacidade**.
3. Abra **Mais configurações de segurança**.
4. Toque em **Instalar apps desconhecidos**.
5. Escolha o navegador ou **Meus Arquivos**.
6. Ative **Permitir desta fonte**.

Por segurança, essa permissão pode ser desativada novamente depois da
instalação.

## Atualizar sem perder os dados

Não desinstale a versão anterior.

1. Instale o novo APK sobre a versão existente.
2. O APK precisa ter versão superior e a mesma assinatura oficial.
3. O Android mostrará a opção **Atualizar**.
4. Relatórios, preferências, perfis e histórico local serão preservados.

As versões recentes também podem ser atualizadas pelo próprio aplicativo:

1. Abra o ReteMonitor Mobile.
2. Entre em **Ajustes**.
3. Abra **Atualizações**.
4. Toque em **Verificar novamente**.
5. Baixe a atualização encontrada.
6. Toque em **Instalar atualização**.
7. Se o Android solicitar autorização, habilite **Permitir desta fonte** para
   o **ReteMonitor Mobile**, retorne ao aplicativo e toque novamente em
   **Instalar atualização**.

A confirmação final sempre é apresentada pelo instalador do Android.

## Aviso do Google Play Protect

O Play Protect pode analisar um APK instalado fora da Play Store. Confirme que
o arquivo veio da Release oficial e que o SHA-256 corresponde ao publicado
antes de prosseguir. Não ignore alertas para APKs obtidos por outros canais.

## Solução de problemas

### “App não instalado” ou “Pacote em conflito”

- Confirme que o APK é a versão `release_assinado`.
- Não tente instalar uma versão mais antiga sobre uma mais nova.
- Um APK assinado por outra chave não pode atualizar a instalação oficial.
- Evite desinstalar o aplicativo, pois isso pode apagar dados locais ainda não
  exportados.

### A tela de instalação não abre

- Confirme a permissão **Instalar apps desconhecidos** para o aplicativo que
  abriu o APK.
- Baixe o arquivo novamente pela Release oficial.
- Verifique se há espaço livre no aparelho.
- Reinicie o aparelho caso o instalador do Android esteja preso.

### A atualização automática não aparece

- Confirme que o telefone está conectado à internet.
- Use o botão **Verificar novamente** em **Ajustes > Atualizações**.
- A verificação automática ocorre no máximo uma vez a cada 24 horas após uma
  consulta bem-sucedida.

## Instalação opcional por ADB

Para equipes técnicas com a Depuração USB autorizada:

```powershell
adb install -r "C:\caminho\ReteMonitorMobile_vX_X_X_release_assinado.apk"
```

O parâmetro `-r` atualiza a instalação existente preservando os dados.
