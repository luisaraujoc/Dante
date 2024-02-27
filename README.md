# Dante 3 - É isso aí! 🔥

[![Rollup Build](https://github.com/michelson/Dante/actions/workflows/ci.yml/badge.svg)](https://github.com/michelson/Dante/actions/workflows/ci.yml)

**Apenas mais um clone médio construído sobre o ProseMirror / TipTap**
--------------------------------------------------------------------

> Dante3 é um port de [Dante2 (Draftjs) ](https://github.com/michelson/Dante/tree/master/packages/dante2). Essa versão é construída sobre o [TipTap](https://www.tiptap.dev/) e incorpora todos os recursos do Dante2 com uma arquitetura ultra mega super mantível.

https://user-images.githubusercontent.com/11976/120087165-bb5c4f00-c0b3-11eb-9002-97c480f3725a.mp4

Veja a demonstração em: [dante-editor.dev](https://dante-editor.dev)

**Por que reescrever uma nova versão do Dante?**
---------------------------------------

A versão anterior (Dante2) foi feita com o DraftJs, uma biblioteca do Facebook para construir editores WYSIWYG. Eu escolhi essa tecnologia porque ela implementou um modelo de dados muito interessante e abstraiu muitas partes da implementação de heurísticas que o [Dante1 (the previous version)](https://github.com/michelson/Dante/tree/master/packages/dante1-legacy)construiu como uma implementação ingênua, dependendo muito da manipulação do DOM. Dante2 foi ótimo e está funcionando em muitos sites de produção. Infelizmente, nos últimos anos, esta biblioteca não recebeu muita atenção dos mantenedores. Entre as ~700 questões não atendidas relatadas, algumas se tornaram impeditivas para mim:

-   Suporte ruim para dispositivos móveis.

-   ~1MB adicionado ao seu pacote (immutablejs é pesado).

-   Não criado para colaboração em tempo real.

**Minha aposta, TipTap**

Depois de experimentar muitas bibliotecas de editores, quero dizer, depois de tentar implementar o Dante em quase todas elas (Trix, Editorjs, Quilljs, Slate, Prosemirror), encontrei a biblioteca TipTap (que é baseada no Prosemirror). Eu acredito que todas as bibliotecas de editores têm suas falhas, mas depois de revisar todas elas, o TipTap é o melhor da sua classe, muito bem projetado/arquitetado, e eu amo a comunidade ao redor do ecossistema deles. Então é isso.

**Recursos:**

-   Extensões / plugins / componentes configuráveis e extensíveis.

-   Desfazer/refazer.

-   Salvar conteúdo como uma estrutura de dados JSON/HTML.

-   Carregar conteúdo como uma estrutura de dados JSON/HTML.

-   Suporte a temas de componentes estilizados (temas claros/escuros integrados).

**Conteúdo baseado em blocos**:

O editor Dante pode ser estendido com componentes (React), atualmente existem componentes padrão para serem usados como estão:

-   Upload de imagem para colar HTML.

-   Incorporar vídeo.

-   Gravador de vídeo.

-   Incorporar.

-   Divisor.

-   Fala.

-   Giphy.

**Instalação**
----------------

`npm install dante3` or `yarn add dante3`

**Uso**
---------

Baseado em componente

```
<DanteEditor
  content={'hello world'}
/>
```

### **Opções:**

Muitas opções de configuração e uso de plugins podem ser encontradas na página de documentação:

Veja em [dante-editor.dev](https://dante-editor.dev)

**Desenvolvimento**
---------------

### **Instalação**

-   `git clone https://github.com/michelson/dante`

**dependências**

-   `npm install` or `yarn install`

### **Compilação**

-   `npm dante3_build` or `yarn dante3_build`

### **instalação de desenvolvimento:**

-   lerna bootstrap

-   yarn dev

**Status**
----------

> Dante3 está em beta, ativamente mantido, com todos os recursos que Dante2 possui. Como depende do TipTap (que é baseado no Prosemirror) e tem um melhor suporte a navegadores e dispositivos móveis. Também possui capacidades de colaboração em tempo real.

**Monorepo**
------------

Este repositório agora contém versões anteriores do Dante, localizadas na pasta [packages](https://github.com/michelson/Dante/tree/master/packages), então Dante1*, Dante2 e Dante3 vivem no mesmo repositório.

> * Dante(1) não é mais mantido.

### **Licença de código aberto**

Dante é licenciado sob a MIT, então você é livre para fazer o que quiser. Se estiver usando comercialmente, torne-se um dos nossos maravilhosos patrocinadores para financiar a manutenção, suporte e desenvolvimento do Dante agora e no futuro.

### **💓 Seu patrocínio**

> Seu patrocínio ajuda a manter, atualizar, apoiar e desenvolver todos os nossos projetos de código aberto, incluindo tiptap e muitos mais.

### **Agradecimentos**

Biblioteca Prosemirror & autores do Tiptap


## Workspaces

Usamos espaços de trabalho npm para gerenciar o monorrepositório, por exemplo, para instalar uma dependência em algum pacote, use:

`npm install --workspace=Dante2`    

`npm install some-dep --workspace=Dante2`    


### construir

+ npm run dante3:build
+ npm run dante2:build

### implantar

+ npm run dante3:publish
+ npm run dante2:publish


npm install rollup-plugin-auto-external --save-dev --workspace=dante3


npm run dante3:build
