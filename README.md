# 🍽️ Projeto Menu - Remasterização com Bootstrap

![Status](https://img.shields.io/badge/Status-Finalizado-green)

Este repositório é muito especial para mim, pois representa a evolução técnica de um projeto anterior. O objetivo foi "remasterizar" um sistema de pedidos que inicialmente utilizava apenas HTML e CSS puro, trazendo-o para o ecossistema do **Bootstrap** para alcançar uma interface moderna, profissional e totalmente responsiva.

## 🚀 Principais Aprendizados e Evolução

A transição para o framework permitiu uma nova visão sobre o desenvolvimento front-end:

- 🎨 **Upgrade de Interface**: Utilização de componentes nativos do Bootstrap para criar um layout visualmente mais atraente e limpo, sem a necessidade de centenas de linhas de CSS customizado.
- 📱 **Foco em Responsividade**: Domínio do sistema de grid e utilitários para garantir que o menu funcione perfeitamente tanto em desktops quanto em dispositivos móveis.
- 🧩 **Componente Modal**: Implementação do componente **Modal** para exibir o resumo do pedido, proporcionando uma experiência de usuário mais fluida e elegante.
- 🛡️ **Lógica de Validação**: Desenvolvimento de verificações via JavaScript para garantir que o nome seja válido e que pelo menos um item tenha sido selecionado antes de processar o pedido.
- 💰 **Formatação de Dados**: Uso de `Intl.NumberFormat` para garantir que todos os valores financeiros sejam exibidos corretamente no padrão brasileiro (BRL).

## 🛠️ Tecnologias Utilizadas

- **Linguagem**: JavaScript (ES6+).
- **Estruturação**: HTML5.
- **Design/UI**: Bootstrap 5 (Framework principal).
- **Lógica**: jQuery (para manipulação do DOM e eventos do Modal).

## 🖥️ Resultado Final

Confira abaixo as capturas de tela da nova interface e as validações do sistema:

### Interface Geral
![menu1](https://github.com/kauanzin222/bootcamp-devjr-projectmenu-bootstrap/blob/main/images/exemplos/menu1.png)
![menu2](https://github.com/kauanzin222/bootcamp-devjr-projectmenu-bootstrap/blob/main/images/exemplos/menu2.png)

### Resumo no Modal e Validações
![modal](https://github.com/kauanzin222/bootcamp-devjr-projectmenu-bootstrap/blob/main/images/exemplos/modal.png)
![nome](https://github.com/kauanzin222/bootcamp-devjr-projectmenu-bootstrap/blob/main/images/exemplos/nome.png)

## 🔍 Snippet: Lógica do Pedido

Abaixo, um exemplo da lógica utilizada para capturar os dados e renderizar o resumo dinamicamente no modal:

```js
modalResumo.on('show.bs.modal', function result() {
    var output = $("#output");
    var name = $("#name").val();
    
    // Validação de Nome
    if (name == '') {
        output.html(`<br><strong><h2 class="alert alert-warning">NOME INVÁLIDO!</h2><strong><br>`)
        return;
    }

    // Lógica de cálculo e formatação BRL...
    // (Código completo no arquivo script.js)
});
