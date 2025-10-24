# 🚀 Landing Pages — E-book Milionário

> Conjunto de **landing pages otimizadas para conversão**, desenvolvidas para um produto digital no nicho de infoprodutos.  
> As páginas foram construídas com foco em performance, automação de pagamento via **Asaas**, e entrega automática de produto digital (PDF) via e-mail.

---

## 🧰 Tecnologias Utilizadas

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)
![Asaas API](https://img.shields.io/badge/Asaas%20API-222222?style=for-the-badge&logo=api&logoColor=white)
![PHPMailer](https://img.shields.io/badge/PHPMailer-0072C6?style=for-the-badge&logo=maildotru&logoColor=white)
![HostGator](https://img.shields.io/badge/HostGator-0052CC?style=for-the-badge&logo=cloudflare&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)

---

## 🧩 Estrutura do Projeto

### 1️⃣ **Landing Page Principal**
- **Endereço:** [`/ebookmilionario.online`](https://ebookmilionario.online)  
- **Objetivo:** Conversão inicial (venda direta do e-book + 1 bônus)  
- **Checkout:** integrado ao **Asaas** (cartão e PIX)  
- **E-mail automático:** Envio via **PHPMailer (Titan SMTP)**  
- **Download seguro:** Link expira em 24h com token individual em JSON  
- **Automação:** Webhook PHP + API Asaas + entrega de PDF automatizada  

### 2️⃣ **Landing Page Remarketing**
- **Endereço:** [`/ebookmilionario.online/ultima_chance.html`](https://ebookmilionario.online/ultima_chance.html)  
- **Objetivo:** Captar leads que não converteram na primeira página  
- **Ofertas:** E-book + 2 bônus exclusivos  
- **Checkout:** mesmo fluxo, mas descrito como “Pacote RMK + 2 Bônus”  
- **Segmentação:** Origem detectada via `HTTP_REFERER` no PHP  
- **Entrega:** e-mail automático + link personalizado com 3 arquivos PDF  

---

## 🧠 Automação e Entrega de Produto

- **Webhook:** Recebe eventos do Asaas (`PAYMENT_CONFIRMED`, `PAYMENT_RECEIVED`, `CHECKOUT_PAID`)  
- **Token de download:** Gerado automaticamente e salvo em `/downloads/tokens/`  
- **Página de acesso:** `downloads/acesso.php` valida o token e libera os PDFs  
- **E-mail:** Enviado via PHPMailer com template HTML customizado e branding do produto  
- **Logs:** Registro completo de eventos e e-mails enviados em `/webhook/logs/`  

---

## ⚙️ Fluxo Técnico Simplificado

```
Cliente → Landing Page → Checkout Asaas → Webhook PHP
      ↓
 Confirmação de Pagamento (API)
      ↓
 Geração de Token e Link Seguro
      ↓
 Envio Automático de E-mail (PHPMailer)
      ↓
 Cliente acessa /downloads/acesso.php

```

---

## 💡 Destaques

- Automação 100% funcional sem plugins ou frameworks externos  
- Compatível com **cartão de crédito e PIX**  
- Sistema de **link expirável** com JSON local seguro  
- Logs de debug e auditoria incluídos (checkout e webhook)  
- Estrutura leve, adaptável para qualquer produto digital  
- Código limpo e documentado (PHP procedural + modularização em `utils.php`)  

---

## 🏁 Status

✅ **Versão atual:** v1.0.2  
📦 **Deploy ativo:** [ebookmilionario.online](https://ebookmilionario.online)  
🧠 **Repositório:** Privado

---

## 👨‍💻 Autor

**Julio Camargo**  
Especialista em TI — DevOps, Automação e Desenvolvimento Web  
🌐 [burititecnologia.com](https://burititecnologia.com)  
📧 julio@burititecnologia.com  

---

> 💬 *“Automação completa de checkout, pagamento e entrega digital — sem intermediários.”*  
> _Projeto E-book Milionário_
