# Autocomplete (popup)

## Sem plugins

```vim
set wildmenu                " habilita menu
" https://vi.stackexchange.com/questions/5029/key-mapping-that-will-invoke-the-wildmenu
set wildcharm=<tab>         " char para chamar wildmenu de um map
set completeopt=menuone     " mostra menu de opções
set shortmess+=c            " remove mensagens inúteis do wildmenu

" origem das palavras do wildmenu:
"   - buffer corrente
"   - buffers escondidos
"   - dicinários
"   - de outras janelas (splits)
set complete=.,b,k,w
" tags no wildmenu afetam perf

" escolhe palavras do omnifunc de acordo com o filetype do buffer aberto
set omnifunc=syntaxcomplete#Complete    " <c-x><c-o>

" Não se esqueça de ignorar o arquivo de tags no projeto
" Para usar ctags o comando deve ser `ctags -R .` no terminal
" As tags vão aparecer com <c-x><c-o>
set tags=tags
```
