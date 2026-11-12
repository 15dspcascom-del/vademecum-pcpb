# Vade Mecum da Polícia Civil da Paraíba — versão web

Versão 20, atualizada até 30/09/2026. 420 normativos, 484 verbetes.

Organização: ILAMILTO SIMPLICIO, Delegado de Polícia Civil/PB
(Pesquisa dos normativos e criação dos índices)

Diagramação e atualização a partir de 2026: Francisco Junio Torres Cavalcante,
Escrivão de Polícia/PB

## O que tem nesta pasta

| arquivo / pasta | o que é |
|---|---|
| `index.html` | a página: capa, índice alfabético remissivo, índice cronológico, índice temático e as relações de normativos revogados e revogadores |
| `partes/` | 47 arquivos, um por seção do corpo normativo. Cada um é baixado só quando o leitor abre aquela seção |
| `img/` | as 194 imagens e anexos do livro, baixadas só quando aparecem na tela |
| `ancoras.json` | diz em qual arquivo de `partes/` está cada normativo, para os links dos índices funcionarem |
| `normas.json` | títulos dos 420 normativos, para a busca por índices |
| `texto.json` | texto integral, baixado só quando se usa a busca "Texto integral" |
| `.nojekyll` | pede ao GitHub Pages para publicar os arquivos como estão |

**Não renomeie nem mova esses arquivos**: os nomes são usados pela própria página.

## Como publicar no GitHub Pages

Com o Git instalado, abra o Prompt de Comando **dentro desta pasta** e rode:

```bat
git init
git add .
git commit -m "Vade Mecum PC-PB v20"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/vademecum-pcpb.git
git push -u origin main
```

Troque `SEU-USUARIO` pelo seu usuário do GitHub. O repositório
(`vademecum-pcpb`) precisa ser criado antes, em <https://github.com/new>,
**vazio** — sem README, sem .gitignore.

Depois, no repositório: **Settings → Pages → Build and deployment**,
em *Source* escolha **Deploy from a branch**, em *Branch* escolha **main**
e a pasta **/ (root)**, e clique em *Save*.

Em dois ou três minutos o endereço fica no ar:

```
https://SEU-USUARIO.github.io/vademecum-pcpb/
```

### Se preferir pelo navegador, sem Git

Em <https://github.com/new> crie o repositório vazio, entre nele e use
**Add file → Upload files**. Arraste o `index.html`, o `README.md`, o
`.nojekyll`, os três `.json` e **as pastas `partes` e `img`**. Como são
cerca de 245 arquivos, o navegador costuma pedir para enviar em duas ou
três levas — pode mandar por partes, mas envie tudo antes de configurar o
Pages. Em seguida siga o mesmo passo de *Settings → Pages* acima.

## Para atualizar numa próxima versão

Substitua os arquivos pelos novos e repita:

```bat
git add .
git commit -m "Vade Mecum PC-PB v21"
git push
```

## Dados pessoais nesta versão

Esta versão é a que vai para a internet aberta, então os **números de documento
de pessoas identificadas foram mascarados**: 6 CPFs e 6 RGs que apareciam nos
preâmbulos de convênios e termos de cooperação, e um telefone celular dado como
contato de um núcleo. Os nomes e os cargos continuam no texto — some apenas o
número, em `partes/sec-2-8.html`, `sec-2-11.html`, `sec-3-4.html`,
`sec-3-2.html` e no `texto.json`.

O arquivo em Word e a versão offline em arquivo único **não** foram alterados:
a motivação do mascaramento é a exposição pública, e esses dois têm
distribuição interna.

## Observações

- A página funciona em qualquer hospedagem de arquivos estáticos, não só no
  GitHub Pages. Basta que a pasta inteira seja servida junta.
- Abrir o `index.html` com duplo clique, direto do disco, **não funciona
  por inteiro**: os navegadores bloqueiam a leitura dos arquivos de
  `partes/` nesse modo, então os índices abrem mas o texto dos normativos
  não carrega. Para uso offline existe a versão em arquivo único
  (`VadeMecum_PC-PB_v20.html`), que traz tudo embutido.
- O botão **Carregar tudo**, no alto, baixa o livro inteiro de uma vez —
  útil para quem quiser usar o Ctrl+F do navegador em todo o conteúdo.
