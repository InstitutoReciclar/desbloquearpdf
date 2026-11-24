# Desbloqueador de Boletos em Lote • Reciclar

Aplicação estática (HTML, CSS e JavaScript) que roda inteiramente no navegador. Não utiliza servidor, banco de dados ou API própria.

## Publicar no GitHub e na Vercel

1. Extraia o ZIP.
2. Crie um repositório no GitHub e envie os três arquivos desta pasta para a raiz do repositório.
3. Na Vercel, escolha **Add New → Project** e importe o repositório.
4. Em **Framework Preset**, selecione **Other**.
5. Deixe **Build Command** e **Output Directory** sem configuração (a raiz do projeto contém `index.html`) e clique em **Deploy**.

Não é necessário `npm install`, `npm run build` ou configurar variáveis de ambiente.

## Rodar localmente

Abra `index.html` no navegador. Para testar via servidor local, no terminal da pasta execute:

```bash
python -m http.server 5500
```

Depois acesse `http://localhost:5500`.

## Observações importantes

- O processamento dos PDFs e das planilhas acontece no navegador. Os arquivos selecionados não são enviados para a Vercel.
- A aplicação carrega bibliotecas públicas por CDN (Tailwind, JSZip, SheetJS, pdf-lib e PDF.js); portanto, precisa de conexão com a internet para carregar essas bibliotecas.
- As senhas salvas pelo botão **Salvar neste navegador** ficam no `localStorage` do navegador, sem criptografia. Não use essa opção em computadores compartilhados e limpe os dados do navegador quando necessário.
- O PDF gerado é reconstruído a partir de imagens das páginas. A aparência é mantida, mas texto selecionável, links, formulários, acessibilidade e metadados originais não são preservados. A qualidade e o tamanho do arquivo podem variar conforme o número e a resolução das páginas.
- Use somente arquivos e senhas que você esteja autorizado a acessar. A ferramenta não recupera senhas desconhecidas.

## Estrutura

```text
/
├── index.html
├── vercel.json
└── README.md
```
