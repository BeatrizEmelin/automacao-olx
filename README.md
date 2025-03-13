# Automação de Login no Site da OLX com Power Automate Desktop

Este repositório contém um código de automação para realizar o login no site da OLX utilizando o Power Automate Desktop.

## Funcionalidades

* Abre o navegador Chrome e navega até a URL da OLX.
* Realiza o login no site da OLX utilizando credenciais armazenadas.
* Utiliza seletores de elementos da página e espera por imagens para garantir a execução correta.

## Estrutura do Código

1.  **REGIÃO AbrindoSite (Abrir Site)**
    * Abre o navegador Chrome com a URL da OLX.
    * Aguarda o carregamento do botão "Entrar".

2.  **REGIÃO LogarSite (Logar no Site)**
    * Verifica a presença do botão "Entrar" e clica nele.
    * Preenche o campo de email com as credenciais.
    * Clica no botão "Entrar Login".
    * Clica no campo de senha.
    * Preenche o campo de senha com as credenciais.
    * Clica no botão "Entrar" final.

3.  **[ControlRepository][PowerAutomateDesktop] (Repositório de Controles)**
    * Define os seletores de elementos da página web usados nas ações de automação.
    * Contém informações detalhadas sobre os seletores de cada elemento (botão "Entrar", campo de email, campo de senha etc.).
    * Especifica os atributos usados para identificar cada elemento na página (classe, ID, título etc.).
    * Contém screenshots dos elementos.

## Variáveis

* `Credenciais['UrlSite']`: URL do site da OLX.
* `NavSiteOlx`: Instância do navegador Chrome.
* `appmask['Web Page 'https://www.olx.com.br/']['BtnEntrar']`: Seletor do botão "Entrar".
* `Credenciais['EmailLogin']`: Email de login.
* `Credenciais['SenhaOlx']`: Senha de login.
* `imgrepo['Image']`: imagem utilizada para o comando de espera por imagem.
* `X, Y`: coordenadas da tela.

## Considerações

* O código depende de um repositório de credenciais (`Credenciais`) que contém a URL, email e senha de login.
* O repositório de seletores de elementos (`appmask`) é crucial para o funcionamento correto da automação.
* O uso de espera por imagem indica um método de espera híbrido, utilizando seletores de elementos HTML e seletores de imagem.
* Os comandos `WAIT (UIAutomation.WaitForImage.ToAppearOnScreen)` são adicionados para dar tempo para a página carregar elementos dinâmicos.


