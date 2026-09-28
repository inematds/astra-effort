# Astra Effort — guia em português

**🇧🇷 [Português](README.md) · 🇺🇸 [English](README.en.md) · 🇪🇸 [Español](README.es.md)**

[![Astra Effort: níveis de esforço na prática](capa/capa.png)](https://inematds.github.io/astra-effort/guia/)

**[Abrir o guia de uso](https://inematds.github.io/astra-effort/guia/)** · **[Ler o guia completo](https://inematds.github.io/astra-effort/guia/leitura.html)** · **[Baixar o PDF em português](Astra-Effort-Guia-pt-BR.pdf)**

Edição em português do **GPT-6 Astra Effort Super Guide**, de Mark Kashef / Early AI Dopters: sete primeiras tentativas documentadas, dez prompts reutilizáveis, quadros editáveis e um método para comparar níveis de esforço no seu trabalho.

O projeto reúne a tradução do kit e materiais complementares enviados pelo usuário. Os resultados são do experimento original de 7 de setembro de 2026, com pesquisa encerrada em 8 de setembro. A tradução não executa novamente os testes nem revalida preços ou funcionalidades.

## Comece aqui

1. Leia [START-HERE.md](START-HERE.md) e o [guia completo em português](SUPER-GUIDE.md).
2. Escolha um dos [dez prompts](PROMPTS.md) e adapte os campos à sua tarefa.
3. Compare os [resultados em português — CSV](evidence/results.pt-BR.csv) ou [JSON](evidence/results.pt-BR.json).
4. Consulte as [verificações do produtor](evidence/PRODUCER-CHECKS.md) antes de tirar conclusões.
5. Registre um teste próprio usando [experiment/YOUR-RUN-LOG.csv](experiment/YOUR-RUN-LOG.csv).

Medium foi a preferência inicial do autor **para esta tarefa de pesquisa e construção**. Tempos são observações individuais; tokens processados incluem entrada em cache e **não representam custo financeiro**. Ultra foi a condição com delegação habilitada.

**Ver também:** [Esforço na prática](https://inematds.github.io/modelos/guia/esforco/), no repositório `modelos`. A página cruza estes dados com um teste do Claude Opus 5.5 por nível de esforço. É uma referência externa e não altera esta tradução.

## Biblioteca

| Caminho | Conteúdo e idioma |
| --- | --- |
| [guia/](guia/) | Página pública e cinco páginas de leitura em português |
| [SUPER-GUIDE.md](SUPER-GUIDE.md) | Guia completo traduzido |
| [Astra-Effort-Guia-pt-BR.pdf](Astra-Effort-Guia-pt-BR.pdf) | PDF da tradução |
| [PROMPTS.md](PROMPTS.md) e [prompts/](prompts/) | Dez modelos de prompt em português |
| [SOURCE-NOTES.md](SOURCE-NOTES.md) | Oito complementos com fontes, traduzidos |
| [experiment/](experiment/) | Enunciado e condições traduzidos; quadro e cabeçalhos originais |
| [evidence/](evidence/) | Explicações em português, dados bilíngues e capturas originais |
| [canvases/](canvases/) | Sete planos originais editáveis em Excalidraw, em inglês |
| [docs/](docs/) | Planilha XLSX, resumo, transcrição traduzida, referência visual e glossário |
| [original-en/](original-en/) | Kit descompactado e transcrição originais em inglês |
| [files/](files/) | PDF e ZIP originais em inglês |
| [source/](source/) | Apresentação, metadados e procedência da importação |

## Português e inglês

Textos de estudo, explicações e prompts estão em português. Comandos, nomes próprios, identificadores como `reasoning.effort`, chaves JSON/CSV e nomes de configurações como `low`, `medium` e `xhigh` permanecem em inglês. PDF original, capturas, quadros e dados brutos foram preservados para auditoria.

O [glossário da tradução](docs/TRADUCAO.md) explica as escolhas e os campos dos dados. Os resumos, planilha e referência visual enviados pelo usuário trazem aproximações e interpretações próprias; para comparar, use os números exatos e limites do guia original traduzido.

## Uso local

Não há dependências para ler o material nem para servir os arquivos já gerados:

```bash
git clone https://github.com/inematds/astra-effort.git
cd astra-effort
python3 -m http.server 8000
```

Abra `http://localhost:8000/guia/`. Para editar os quadros, abra os arquivos `.excalidraw` no Excalidraw.

Para regenerar as páginas de leitura após editar os documentos:

```bash
python3 -m venv .venv
.venv/bin/pip install -r scripts/requirements.txt
.venv/bin/python scripts/build_docs.py
```

O PDF em português foi gerado a partir de `guia/leitura.html` com Chromium, em A4; a página também tem estilos de impressão para exportar pelo navegador. O HTML da landing é mantido diretamente em `guia/index.html`. O GitHub Pages publica os arquivos estáticos por [.github/workflows/pages.yml](.github/workflows/pages.yml).

## Integridade e origem

```bash
python3 scripts/verify.py
```

Depois de alterações intencionais, atualize o manifesto e confira novamente:

```bash
python3 scripts/verify.py --write-manifest
python3 scripts/verify.py
```

- [Pasta original no GitHub](https://github.com/earlyaidopters/gumroad-resources/tree/ecfbc2cc3d212672404d346043e47e492fb30198/resources/gpt-6-astra-effort-super-guide).
- Commit de origem: `ecfbc2cc3d212672404d346043e47e492fb30198`.
- Importação e tradução: 10 de setembro de 2026.
- [source/provenance.json](source/provenance.json): registro dos 45 arquivos importados, com hashes anteriores à tradução.
- [original-en/MANIFEST.json](original-en/MANIFEST.json): manifesto original do kit.
- [MANIFEST.json](MANIFEST.json): manifesto da edição atual.

Os documentos em `source/` são cópias da apresentação original; seus links relativos refletem a estrutura de origem. Use o índice acima para navegar nesta edição. A autoria e os direitos dos materiais originais permanecem com seus respectivos titulares.
