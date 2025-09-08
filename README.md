# 📘 O Futuro da Aprendizagem

Landing page oficial do livro **O Futuro da Aprendizagem – Inteligência Artificial e os Caminhos da Educação 5.0**, de *Tiago Scatolini*.

🔗 **Acesse agora:** https://tiagoscatolini-ops.github.io/futurodaaprendizagem/

---

## 📖 Sobre o livro
“O Futuro da Aprendizagem” mergulha na revolução da IA na educação. Mais do que um livro, é um **mapa prático** para navegar e liderar na Educação 5.0.

- ✅ Estratégias aplicáveis para educadores e gestores  
- ✅ Integração entre tecnologia e propósito humano  
- ✅ Casos práticos e diretrizes sobre ética e dados  
- ✅ Um olhar direto e acionável para o futuro da aprendizagem

---

## 🛠️ Tecnologias
- **HTML5** + **CSS3** (leve e responsivo)
- Deploy via **GitHub Pages**

---

## 🚀 Como atualizar a landing page
1. Gere/edite o `index.html` (ex.: via Colab).
2. Baixe o arquivo pronto.
3. No GitHub, faça upload substituindo o `index.html` existente.
4. Commit — em ~1–2 minutos a página no ar é atualizada.

> Dica: antes do build, ajuste variáveis como `AMAZON_URL`, `COUNTDOWN_DEADLINE` e o `GOOGLE_FORM_IFRAME` do Google Forms.

---

## ✨ Destaques da landing page

### UX/UI e conversão
- **Hero persuasivo** com badges de autoridade, subtítulo claro e CTAs múltiplas (Comprar, PDF, LinkedIn, WhatsApp, **“Quero o bônus”**).
- **Carrossel/Galeria** com cartões e sombras; correção de bug nas imagens (checs robustos + suporte a `.svg`).
- **Seção de Benefícios/Pilares** com bullets orientados a resultado (“comece em 1 hora”, checklists, templates).
- **Prova social**: grade de depoimentos (“O que dizem os leitores”).
- **Preço com ancoragem**: “Preço de referência” vs. “Hoje (lançamento -42%)” com CTA direta.
- **FAQ** em `details/summary` (reduz objeções).
- **CTA final** repetindo a ação principal.
- **Sticky CTA** flutuante no mobile (Comprar / Dúvidas).
- **Menu superior com âncoras internas** (Sobre, Benefícios, Preço, FAQ) + **scroll suave**; nada abre nova página.
- **Formulário deslocado** para a seção `#form-section`, com botão no hero que rola até lá.

### Captura de leads / Forms
- Substituição do form nativo por **Google Forms embutido** (iframe) em duas áreas:  
  - Seção “**Quero receber o bônus!**” (principal)  
  - **Modal de saída (exit-intent)** — o modal incorpora o **mesmo** Google Forms (não usa mais Typeform/Formspree).
- Iframe responsivo dentro de um wrapper (`.embed-wrap`) — largura 100%, altura ajustável, bordas/sombra.

### Gatilhos mentais
- **Urgência**: countdown corrigido (`${COUNTDOWN_DEADLINE}T23:59:59`) e badge “Oferta por tempo limitado”.
- **Escassez/âncora**: comparação de preço.
- **Autoridade/segurança**: badges, LinkedIn, depoimentos e FAQ.

### Acessibilidade
- Rótulos ARIA, `aria-live` no countdown, foco visível (`outline`), `aria-modal`/`aria-labelledby` no modal,
  labels “sr-only” e `rel="noopener"` nos links externos.

### SEO & Metadados
- Open Graph / Twitter (título, descrição, imagem).
- **JSON-LD (Schema.org/Book)** com `offers` e autor.
- Meta description + robots.
- Favicon via data URI (quando disponível).

### Performance & arquitetura
- **Auto-detecção de assets** em `/content` (autor, hero, capa, favicon, PDF) com fallback e ordenação por tamanho/data.
- Geração de **data URIs** somente quando o arquivo existe.
- Sanitização leve de textos.
- Slot para **ANALYTICS** injetável.
- **A/B simples** por `?variant=B` (reordena CTAs do hero e persiste em `localStorage`).

### Correções de bugs
- **KeyError `LINKEDIN_SVG`**: placeholder agora é passado ao `tpl.substitute`.
- **KeyError ‘d’** (countdown) eliminado — cálculo 100% em JS.
- **Imagens “bugadas”**: lista de extensões ampliada + verificações de existência; o carrossel só rende imagens válidas.
- **Menu**: âncoras internas com `scroll-margin-top` para compensar a navbar fixa.

---

## 👨‍💻 Autor
**Tiago Scatolini**  
MSc. Ciência Política, especialista em Ciência de Dados e Inteligência Artificial (graduação em Ciências Biológicas).  
[Perfil no LinkedIn](https://www.linkedin.com/in/tiagoscatolini/)

---

## 📝 Licença
Projeto de uso pessoal e educacional.  
A distribuição do livro está sujeita aos direitos autorais do autor.
