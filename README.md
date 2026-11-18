🌐 GitHub Pages: Registro de Ponto

Esta seção documenta a página estática criada e hospedada no **GitHub Pages** para capturar coordenadas geográficas em tempo real via celular/navegador e enviá-las de forma estruturada para a nossa planilha do Google Drive.

### 🔧 Integração com Google Forms
A página HTML faz uma submissão via método `POST` usando o modo `no-cors` diretamente para o endpoint de respostas públicas do Google Forms, mapeando os campos de entrada do usuário aos respectivos identificadores internos do formulário:

* **URL de Envio (`formResponse`):**  
  `https://docs.google.com/forms/d/e/1FAIpQLSfWxeVvkQ0Y3T5msuFVOmS5in4ybYmw86oVJk5J6J8R_8BKyw/formResponse`

* **Mapeamento de Parâmetros (Form Input Name):**
  * **Nome do Local:** `entry.1350129950`
  * **Latitude:** `entry.718109587`
  * **Longitude:** `entry.964245664`

---

### 📋 Funcionalidades Principais do Código Frontend
1. **Geolocalização Nativa (`navigator.geolocation`):** Captura a latitude e longitude precisas do dispositivo com tolerância de até 10 segundos e fallback para erros comuns (permissão negada, timeout ou falta de suporte).
2. **Preenchimento via Query String:** O formulário preenche automaticamente os campos de entrada caso receba parâmetros na URL (ex: `https://seu-usuario.github.io/?local=Matriz&lat=-23.55&lng=-46.63`).
3. **Interface Responsiva & Moderna:** Construído com CSS personalizado (Mobile First, temas usando variáveis nativas `:root`, suporte visual a feedback como spinners de loading e alertas de sucesso/erro).
