# image-cdn

Repositório para hospedar imagens e gerar URLs prontas para usar em sites e páginas internas (HTML, e-mails, dashboards etc.).

As imagens ficam na pasta [`images/`](images/) e são servidas via **jsDelivr**, uma CDN global gratuita, com cache e sem rate limit.

---

## Como usar (passo a passo)

### 1. Subir a imagem
Pela interface do GitHub:
1. Entre na pasta [`images/`](images/)
2. Clique em **Add file → Upload files**
3. Arraste a imagem e clique em **Commit changes**

> Dica: use nomes sem espaços e sem acentos (ex.: `logo-header.png`, não `logo header.png`).

### 2. Montar a URL

```
https://cdn.jsdelivr.net/gh/__USUARIO__/image-cdn@main/images/NOME-DO-ARQUIVO
```

Exemplo, para um arquivo `logo.png`:

```
https://cdn.jsdelivr.net/gh/__USUARIO__/image-cdn@main/images/logo.png
```

### 3. Usar no HTML

```html
<img src="https://cdn.jsdelivr.net/gh/__USUARIO__/image-cdn@main/images/logo.png"
     alt="Logo" width="200">
```

Em CSS:

```css
.banner {
  background-image: url("https://cdn.jsdelivr.net/gh/__USUARIO__/image-cdn@main/images/banner.png");
}
```

---

## Observações

- **O repositório é público.** Qualquer pessoa com o link vê a imagem — não coloque nada confidencial aqui.
- **Cache da CDN:** a jsDelivr pode levar alguns minutos para atualizar depois do upload. Se precisar da versão nova na hora, troque `@main` por um commit específico, ou aguarde o cache expirar.
- **Versão fixa (opcional):** trocar `@main` pelo hash de um commit (`@a1b2c3d`) trava a imagem naquela versão e melhora o cache.
- Formatos suportados: `.png`, `.jpg`, `.jpeg`, `.gif`, `.webp`, `.svg`, `.avif`, `.ico`.

## Alternativa: URL direta do GitHub (raw)

Caso precise, também funciona (mas tem rate limit e é menos indicada para produção):

```
https://raw.githubusercontent.com/__USUARIO__/image-cdn/main/images/NOME-DO-ARQUIVO
```
