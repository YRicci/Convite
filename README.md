# 💌 Convite interativo

Um site de uma página só (HTML, CSS e JavaScript puro, sem instalar nada) para convidar alguém para sair de um jeito divertido.

- **Convite:** pergunta "Quer sair comigo?". O botão **Não** foge para outro ponto da tela a cada clique e a frase muda, em loop. O **Sim** cresce um pouco a cada recusa.
- **Etapas:** se a resposta for Sim, a pessoa escolhe **Dia → Programa → Horário → Flores** (a aba Flores é opcional), uma etapa por vez, e pode voltar nas abas já concluídas.
- **Pronto:** mostra o resumo e abre o WhatsApp com a mensagem já escrita.
- **Extras:** emojis caindo devagar no fundo e uma chuva de confete ao aceitar.

## Como usar

1. Baixe ou clone este repositório.
2. Abra o `index.html` em um editor de texto (Bloco de Notas, VS Code, etc.).
3. Faça as mudanças da seção abaixo e salve.
4. Dê dois cliques no `index.html` para testar no navegador.

## O que personalizar (arquivo `index.html`)

Os números de linha são os do arquivo original. Se não achar a linha, procure pelo nome da constante (Ctrl+F).

| Linha | O que é | O que fazer |
|---|---|---|
| 55 | `SEU_NOME` | Troque `"Seu Nome"` pelo seu nome. Ele aparece na mensagem de WhatsApp que a pessoa envia. |
| 56 | `WHATSAPP_NUMERO` | Opcional. Vazio: a pessoa escolhe o contato ao abrir o WhatsApp. Preenchido: a mensagem vai direto para você. Use DDI + DDD + número, só dígitos (ex.: `"5521999999999"`). |
| 57 | `MOSTRAR_FLORES` | `true` mostra a aba Flores; `false` esconde. |
| 58 | `IGNORAR_REDUZIR_MOVIMENTO` | `true` mostra as animações mesmo em aparelhos com "reduzir movimento" ligado; `false` respeita essa configuração. |
| 59 | `CHUVA_DE_EMOJIS` | `true` liga a chuva de emojis no fundo; `false` desliga. |
| 61 a 63 | `FRASES_NAO` | As frases que aparecem ao clicar em Não, uma por linha, entre aspas e separadas por vírgula. Podem ser quantas quiser, elas repetem em loop. |
| 67 | Etapa **Dia** | `q` é a pergunta, `s` é a frase pequena embaixo e `o` é a lista de opções. |
| 68 | Etapa **Programa** | Mesmo formato. Troque, adicione ou apague opções. |
| 69 | Etapa **Horário** | Mesmo formato. |
| 70 | Etapa **Flores** | Mesmo formato. |
| 75 | `NOTAS` | Legenda pequena de uma opção. A chave precisa ser **idêntica** ao texto da opção na linha 68 (com o emoji). Para não usar legenda, deixe `const NOTAS = {};`. |
| 145 | `EMOJIS_CHUVA` | Os emojis que caem no fundo. |
| 6 | `<title>` | Título que aparece na aba do navegador. |
| 90 | Título principal | A pergunta "Quer sair comigo?". |
| 96 | Mensagem do WhatsApp | O texto enviado quando a pessoa aceita. |
| 9, 11 e 12 | Cores | A primeira é o tema claro; as outras duas, o tema escuro. `--bg` é o fundo, `--ink` o texto e `--accent` a cor de destaque. |

Exemplo de opção nova: na linha 68, acrescente `,"🎳 Boliche"` antes do `]`.

> A opção "🏠 Minha casa, talvez?" (linhas 68 e 75) é um exemplo pessoal. Edite ou apague, se não fizer sentido para você.

## Privacidade antes de publicar

Repositórios públicos podem ser vistos por qualquer pessoa. Antes de enviar para o GitHub:

- Não coloque seu número de telefone em `WHATSAPP_NUMERO` se não quiser que ele fique público. Deixando vazio, o site funciona do mesmo jeito e a pessoa escolhe o contato.
- Use só o primeiro nome, ou um apelido, em `SEU_NOME`.
- Prefira um nome de repositório discreto, sem o nome da pessoa.
- Se quiser mais controle, deixe o repositório **privado** e só compartilhe o link do site publicado.

## Publicar no GitHub Pages

1. Crie um repositório e envie os arquivos:
   ```bash
   git init
   git add .
   git commit -m "Primeira versão do convite"
   git branch -M main
   git remote add origin https://github.com/SEU_USUARIO/NOME_DO_REPO.git
   git push -u origin main
   ```
2. No repositório, vá em **Settings → Pages**.
3. Em **Build and deployment**, escolha **Deploy from a branch**, branch `main`, pasta `/ (root)`, e salve.
4. Depois de um minuto, o link fica em `https://SEU_USUARIO.github.io/NOME_DO_REPO/`.

> O GitHub Pages em repositório privado depende do plano da sua conta. Se não estiver disponível, use um repositório público com as precauções acima.
