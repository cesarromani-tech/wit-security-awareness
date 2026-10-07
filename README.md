# Security Awareness — Demo de Ataque com QR Code

<p align="center">
  <img src="cover.svg" alt="Security Awareness — Demo QR Code" width="100%"/>
</p>

> **Treinamento de conscientização em segurança digital para usuários corporativos**  
> Criado por [Cesar Romani](https://github.com/cesarromani-tech)

---

## 📋 Sobre o projeto

Demonstração interativa e animada de uma **cadeia de ataque real via QR Code malicioso**, desenvolvida para apresentações e treinamentos de conscientização em segurança digital (Security Awareness).

A simulação replica, passo a passo, como um usuário desavisado pode ser comprometido ao escanear um QR Code em um evento — desde a isca inicial até a exfiltração de dados e transferência bancária via Pix.

**Nenhum dado real é coletado. Nenhum arquivo é baixado. Nenhuma transferência é realizada.**  
Tudo é simulação visual para fins educativos.

---

## 📁 Arquivos

| Arquivo | Descrição |
|---|---|
| `demo-ataque.html` | Simulação completa da cadeia de ataque |
| `gerador-qrcode.html` | Gerador de QR Code com emoji ou letra no centro |

---

## 🎬 Fluxo da simulação (`demo-ataque.html`)

```
[1] Portal de isca       →  Página falsa de "brinde do evento"
[2] Download             →  Barra de progresso + diálogo de permissão
[3] Desktop fake         →  Terminal bash + editor VS Code + netcat reverse shell
[4] Comprovante Pix      →  Transferência de R$ 9.539,90 exibida em tempo real
[5] Revelação educativa  →  5 lições de segurança + fechamento automático
```

### Controles
| Ação | Resultado |
|---|---|
| Clique / Toque | Avança / pula animação |
| `Espaço` / `→` | Avança / pula animação |
| `R` | Reinicia do início |
| `F` | Alterna fullscreen |

---

## 🔲 Gerador de QR Code (`gerador-qrcode.html`)

Cria QR Codes personalizados com ícone central — ideal para materiais de treinamento e apresentações.

**Recursos:**
- Modo **Emoji** — grade com 32 emojis + campo personalizado
- Modo **Letra/Texto** — até 3 caracteres, 6 fontes, cor customizável
- Controle de tamanho, cor de fundo e arredondamento do ícone central
- Download em PNG com margem

---

## 🚀 Como usar

Não requer servidor, framework ou dependências locais.

```bash
# Clone o repositório
git clone https://github.com/cesarromani-tech/security-awareness-qrcode.git

# Abra diretamente no navegador
open demo-ataque.html
open gerador-qrcode.html
```

> **Recomendado:** Chrome ou Edge em modo fullscreen (`F11`) para apresentações em telão.

---

## 🎯 Casos de uso

- **Palestras** de conscientização em segurança
- **Treinamentos** corporativos e onboarding de TI
- **Demonstrações** para equipes de SOC e suporte
- **Eventos** de tecnologia e cibersegurança
- **Campanhas internas** de phishing simulado

---

## 🔐 Lições abordadas na simulação

1. **Desconfie** — a maioria dos ataques explora a confiança, não a tecnologia
2. **QR Code esconde a URL real** — você não sabe para onde vai antes de escanear
3. **Promoção legítima nunca pede instalação** — validadores e cupons executáveis são red flags
4. **Pressa é a ferramenta do golpe** — contadores regressivos existem para impedir o raciocínio
5. **Acesso remoto começa em silêncio** — quando o usuário percebe, os dados já foram

---

## ⚙️ Stack técnica

- HTML5 + CSS3 + JavaScript vanilla (zero dependências externas na demo)
- [`qrcodejs`](https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js) via CDN (apenas no gerador)
- Responsivo: mobile-first, adaptável a qualquer tela (celular → telão 4K)
- Safe-area support (`env(safe-area-inset-*)`) para dispositivos com notch
- `clamp()` para tipografia fluida
- Engine de animação própria com controle de geração, skip e abort

---

## 📄 Licença

Este projeto é disponibilizado para uso educacional e treinamentos internos.  
Proibida a utilização para fins maliciosos ou enganosos.

---

<div align="center">

Criado por [@cesarromani-tech](https://github.com/cesarromani-tech)

</div>
