# 💌 Convite interativo

Um site de uma página só (HTML, CSS e JavaScript puro, sem instalar nada) para convidar alguém para sair de um jeito divertido.

- **Convite:** pergunta "Quer sair comigo?". O botão **Não** foge para outro ponto da tela a cada clique e a frase muda, em loop. O **Sim** cresce um pouco a cada recusa.
- **Etapas:** se a resposta for Sim, a pessoa escolhe **Dia → Programa → Horário**, uma etapa por vez, e pode voltar nas abas já concluídas.
- **Pronto:** mostra o resumo e abre o WhatsApp com a mensagem já escrita.

## Como usar

1. Baixe ou clone este repositório.
2. Abra o `index.html` em um editor de texto (Bloco de Notas, VS Code, etc.).
3. Faça as mudanças da seção abaixo e salve.
4. Dê dois cliques no `index.html` para testar no navegador.

## O que personalizar (arquivo `index.html`)

Os números de linha abaixo são os do arquivo original. Se não achar a linha, procure pelo nome da constante (Ctrl+F).

| Linha | O que é | O que fazer |
|---|---|---|
| 54 | `SEU_NOME` | Troque `"Seu Nome"` pelo seu nome. Ele aparece na mensagem de WhatsApp que a pessoa envia. |
| 55 | `WHATSAPP_NUMERO` | Opcional. Se ficar vazio, a pessoa escolhe o contato ao abrir o WhatsApp. Se preencher, a mensagem já vai direto para você, com DDI + DDD + número, só dígitos (ex.: `"5521999999999"`). |
| 57 a 59 | `FRASES_NAO` | As frases que aparecem ao clicar em Não, uma por linha, entre aspas e separadas por vírgula. Pode ter quantas quiser, elas repetem em loop. |
| 63 | Etapa **Dia** | `q` é a pergunta, `s` é a frase pequena embaixo e `o` é a lista de opções. |
| 64 | Etapa **Programa** | Mesmo formato. Troque, adicione ou apague opções à vontade. |
| 65 | Etapa **Horário** | Mesmo formato. |
| 69 | `NOTAS` | Legenda pequena de uma opção. A chave precisa ser **idêntica** ao texto da opção na linha 64 (com o emoji). Para não usar legenda, deixe `const NOTAS = {};`. |
| 6 | `<title>` | Título que aparece na aba do navegador. |
| 84 | Título principal | A pergunta "Quer sair comigo?". |
| 90 | Mensagem do WhatsApp | O texto que será enviado quando a pessoa aceitar. |
| 9, 11 e 12 | Cores | Linha 9 é o tema claro; linhas 11 e 12 são o tema escuro. `--bg` é o fundo, `--ink` o texto e `--accent` a cor de destaque (botões). |

Exemplo de opção nova na linha 64: acrescente `,"🎳 Boliche"` antes do `]`.

> A opção "🏠 Minha casa, talvez?" (linhas 64 e 69) é um exemplo pessoal. Edite ou apague, se não fizer sentido para você.

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
