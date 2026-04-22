# criarPDF


Esse repositório contem um script que simula a funcionalidade de ação rápida do MacOS ⇢ Criar PDF.

Step by step
## Instalar ImageMagik

Para converter várias imagens em um único PDF, a ferramenta imagemagick é a alternativa mais rápida ao Ações Rápidas do Mac.

**Instalar:** ```sudo apt install imagemagick``` (em sistemas baseados em Debian/Ubuntu).

**Converter imagens:**``` convert *.jpg output.pdf```

**Melhorar ordenação:**```img2pdf $(find . -iname '*.jpg' | sort -V) -o document.pdf```


## Criar Menu de Clique Direito (Nautilus/Nemo Scripts)

Você pode criar seu próprio script de "Ação Rápida" para converter imagens para PDF com o botão direito no gerenciador de arquivos (Nautilus).

1. Vá para a pasta de scripts: ~/.local/share/nautilus/scripts
2. Crie um arquivo chamado "Converter para PDF".
3. Adicione o seguinte conteúdo:
```bash
#!/bin/bash
img2pdf "$@" -o "documento.pdf"
```

4. Torne o script executável: chmod +x "Converter para PDF".
5. Agora, ao clicar com o botão direito em imagens, a opção aparecerá em Scripts.


[artigo](https://www.google.com/search?q=a%C3%A7oes+r%C3%A1pidas+criar+pdf+no+mac+como+fazer+issso+no+linux&sca_esv=90400c0a8b8f484b&rlz=1C5OZZY_enBR1208BR1208&biw=1554&bih=794&sxsrf=ANbL-n5cCSakgWpfsmKKWd9LJkUBHEDFsQ%3A1776815499595&ei=iw3oae7vI8vn1sQP7rTciQ8&ved=0ahUKEwiu4bzFkYCUAxXLs5UCHW4aN_EQ4dUDCBE&uact=5&oq=a%C3%A7oes+r%C3%A1pidas+criar+pdf+no+mac+como+fazer+issso+no+linux&gs_lp=Egxnd3Mtd2l6LXNlcnAiOmHDp29lcyByw6FwaWRhcyBjcmlhciBwZGYgbm8gbWFjIGNvbW8gZmF6ZXIgaXNzc28gbm8gbGludXgyBRAAGO8FMgUQABjvBTIFEAAY7wVI51tQ7ARY_VhwA3gBkAEAmAHxAaAB7SeqAQYwLjIyLja4AQPIAQD4AQGYAh-gAoYpwgIKEAAYRxjWBBiwA8ICBRAhGKABwgIFECEYnwXCAgcQIRgKGKABmAMAiAYBkAYIkgcGMy4yMS43oAerbLIHBjAuMjEuN7gH-ijCBwYwLjI4LjPIB0GACAE&sclient=gws-wiz-serp)
