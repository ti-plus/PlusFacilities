<div align="center">

<img src="logo.png" alt="TI Plus Facilities" height="90">

# TI Plus Facilities

**Painel de produtividade da equipe de TI da Plus Facilities.**
Uma página única, simples e atualizada automaticamente todos os dias.

[Ver o site](https://plusfacilities.github.io/) · [Perfil da organização](https://github.com/PlusFacilities) · [Site da Plus Facilities](https://plusfacilities.com.br)

</div>

---

## Sobre o projeto

Este repositório abriga a landing page que mostra, de forma pública e transparente, a produtividade da TI da Plus Facilities: atividades por dia e por semana, a partir dos dados de commits registrados na organização [PlusFacilities](https://github.com/PlusFacilities).

O site é estático (HTML e CSS em um único arquivo), sem build, sem dependências e hospedado gratuitamente no GitHub Pages.

## Como os dados chegam ao site

Os gráficos não ficam neste repositório. Eles são gerados pela automação do perfil da organização e publicados em:

```
https://raw.githubusercontent.com/PlusFacilities/.github/main/profile/assets/diario.svg
https://raw.githubusercontent.com/PlusFacilities/.github/main/profile/assets/semanal.svg
```

A página carrega essas duas imagens diretamente. Quando a automação atualiza os gráficos, o site reflete a mudança sozinho, sem nenhuma ação neste repositório.

## Estrutura

```
.
├── index.html     # a página inteira (estilos e scripts embutidos)
├── logo.png       # símbolo TI exibido no menu superior
├── favicon.png    # ícone da aba do navegador
└── README.md
```

## Publicação no GitHub Pages

1. Envie os arquivos para a branch `main`.
2. Em **Settings → Pages**, escolha **Deploy from a branch**, depois `main` e `/ (root)`.
3. Aguarde de 1 a 2 minutos. O endereço aparece no topo da mesma tela.

O endereço depende do nome do repositório:

| Nome do repositório | Endereço |
| --- | --- |
| `plusfacilities.github.io` (na organização) | `https://plusfacilities.github.io/` |
| qualquer outro nome | `https://plusfacilities.github.io/nome-do-repositorio` |

Para usar um domínio próprio, como `ti.plusfacilities.com.br`, preencha **Custom domain** em Settings → Pages e crie um registro `CNAME` no DNS apontando para `plusfacilities.github.io`.

## Personalização

**Cartões de números no topo (opcional).** Crie um arquivo `data.json` na raiz com até quatro itens. Se o arquivo não existir, os cartões simplesmente não aparecem.

```json
[
  { "label": "Commits no ano", "value": "1.240" },
  { "label": "Dias ativos", "value": "212" }
]
```

**Cores e fonte.** Ficam no bloco `:root` do `index.html`, em variáveis CSS:

| Variável | Cor | Uso |
| --- | --- | --- |
| `--bg` | `#EAF6FD` | fundo da página |
| `--line` | `#BFE7F9` | bordas dos cartões |
| `--cyan` | `#4FD3F5` | destaques |
| `--blue` | `#2C4E79` | botões e títulos secundários |
| `--navy` | `#1B334F` | títulos e faixas escuras |

A fonte é a Poppins, carregada do Google Fonts.

**Textos.** Títulos, descrições e os três blocos de "Como trabalhamos" estão direto no `index.html` e podem ser editados à mão.

## Testar localmente

Não há nada para instalar. Basta abrir o `index.html` no navegador. Para simular o comportamento do GitHub Pages, sirva a pasta com qualquer servidor estático:

```bash
python3 -m http.server 8000
```

Depois acesse `http://localhost:8000`.

## Observações

- Os gráficos só aparecem se o repositório `.github` da organização estiver público. Se estiver privado, a página mostra um aviso com link para o GitHub no lugar das imagens.
- O GitHub Pages em repositório privado depende do plano da organização.

---

<div align="center">

Feito pela TI da **Plus Facilities** · Sua parceira em soluções de Facilities

</div>
