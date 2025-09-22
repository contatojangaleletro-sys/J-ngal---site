# J-ngal---site
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Jangal - Eletrônicos e Variedades</title>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
  <style>
    /* Reset básico */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Roboto', sans-serif;
    }

    body {
      background-color: #f8f8f8;
      color: #333;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    /* Cabeçalho */
    header {
      background-color: #ffffff;
      padding: 15px 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    header .logo {
      font-size: 28px;
      font-weight: bold;
    }

    header .logo span {
      color: orange; /* "Gal" laranja */
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 20px;
    }

    nav ul li a {
      font-weight: 500;
      transition: color 0.3s;
    }

    nav ul li a:hover {
      color: #007bff;
    }

    /* Banner principal */
    .banner {
      background: url('https://images.unsplash.com/photo-1519389950473-47ba0277781c') center/cover no-repeat;
      height: 400px;
      display: flex;
      justify-content: center;
      align-items: center;
      color: white;
      text-align: center;
      position: relative;
    }

    .banner::after {
      content: '';
      position: absolute;
      inset: 0;
      background: rgba(0,0,0,0.4);
    }

    .banner-content {
      position: relative;
      z-index: 1;
    }

    .banner-content h1 {
      font-size: 36px;
      margin-bottom: 15px;
    }

    .banner-content p {
      font-size: 18px;
      margin-bottom: 20px;
    }

    .banner-content a {
      background-color: #007bff;
      color: white;
      padding: 12px 25px;
      border-radius: 5px;
      font-weight: bold;
      transition: background 0.3s;
    }

    .banner-content a:hover {
      background-color: #0056b3;
    }

    /* Seção de produtos */
    .produtos {
      padding: 50px 20px;
      max-width: 1200px;
      margin: 0 auto;
    }

    .produtos h2 {
      text-align: center;
      margin-bottom: 40px;
      font-size: 32px;
      color: #007bff;
    }

    .produto-lista {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 30px;
    }

    .produto-card {
      background-color: white;
      border-radius: 10px;
      padding: 20px;
      text-align: center;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
      transition: transform 0.3s;
    }

    .produto-card:hover {
      transform: translateY(-5px);
    }

    .produto-card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      border-radius: 10px;
      margin-bottom: 15px;
    }

    .produto-card h3 {
      font-size: 20px;
      margin-bottom: 10px;
      color: #333;
    }

    .produto-card p {
      font-size: 18px;
      margin-bottom: 15px;
      font-weight: bold;
      color: #007bff;
    }

    .produto-card a {
      display: inline-block;
      background-color: orange;
      color: white;
      padding: 10px 20px;
      border-radius: 5px;
      font-weight: bold;
      transition: background 0.3s;
    }

    .produto-card a:hover {
      background-color: #e69500;
    }

    /* Sobre a loja */
    .sobre {
      background-color: #ffffff;
      padding: 60px 20px;
      text-align: center;
    }

    .sobre h2 {
      font-size: 32px;
      margin-bottom: 20px;
      color: #007bff;
    }

    .sobre p {
      font-size: 18px;
      max-width: 800px;
      margin: 0 auto;
      line-height: 1.6;
    }

    /* Formas de pagamento */
    .pagamento {
      padding: 50px 20px;
      text-align: center;
    }

    .pagamento h2 {
      font-size: 32px;
      margin-bottom: 30px;
      color: #007bff;
    }

    .pagamento img {
      max-width: 300px;
      margin: 0 10px;
      vertical-align: middle;
    }

    /* Contato */
    .contato {
      background-color: #ffffff;
      padding: 60px 20px;
      text-align: center;
    }

    .contato h2 {
      font-size: 32px;
      margin-bottom: 20px;
      color: #007bff;
    }

    .contato form {
      max-width: 500px;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      gap: 15px;
    }

    .contato input, .contato textarea {
      padding: 12px;
      border-radius: 5px;
      border: 1px solid #ccc;
      font-size: 16px;
      width: 100%;
    }

    .contato button {
      padding: 12px;
      background-color: #007bff;
      color: white;
      border: none;
      border-radius: 5px;
      font-weight: bold;
      cursor: pointer;
      transition: background 0.3s;
    }

    .contato button:hover {
      background-color: #0056b3;
    }

    /* Rodapé */
    footer {
      background-color: #222;
      color: white;
      padding: 20px;
      text-align: center;
    }

    footer a {
      color: orange;
      margin: 0 5px;
    }

    @media(max-width: 768px){
      .banner-content h1 {
        font-size: 28px;
      }
      .banner-content p {
        font-size: 16px;
      }
    }

  </style>
</head>
<body>

  <!-- Cabeçalho -->
  <header>
    <div class="logo">Jan<span>gal</span></div>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#produtos">Produtos</a></li>
        <li><a href="#sobre">Sobre</a></li>
        <li><a href="#contato">Contato</a></li>
      </ul>
    </nav>
  </header>

  <!-- Banner -->
  <section class="banner" id="home">
    <div class="banner-content">
      <h1>Eletrônicos e Variedades para você</h1>
      <p>Encontre os melhores produtos com qualidade e preços acessíveis!</p>
      <a href="#produtos">Compre Agora</a>
    </div>
  </section>

  <!-- Produtos -->
  <section class="produtos" id="produtos">
    <h2>Produtos em Destaque</h2>
    <div class="produto-lista">
      <div class="produto-card">
        <img src="https://images.unsplash.com/photo-1511707171634-5f897ff02aa9" alt="Produto 1">
        <h3>Fone de Ouvido</h3>
        <p>R$ 120,00</p>
        <a href="#">Comprar via WhatsApp</a>
      </div>
      <div class="produto-card">
        <img src="https://images.unsplash.com/photo-1510557880182-3a83505b4b94" alt="Produto 2">
        <h3>Caixa de Som</h3>
        <p>R$ 250,00</p>
        <a href="#">Comprar via WhatsApp</a>
      </div>
      <div class="produto-card">
        <img src="https://images.unsplash.com/photo-1563245376-2c18e3e9fa42" alt="Produto 3">
        <h3>Pote de Cozinha</h3>
        <p>R$ 35,00</p>
        <a href="#">Comprar via WhatsApp</a>
      </div>
      <div class="produto-card">
        <img src="https://images.unsplash.com/photo-1571689936073-0be68e6faedf" alt="Produto 4">
        <h3>Bacia Plástica</h3>
        <p>R$ 25,00</p>
        <a href="#">Comprar via WhatsApp</a>
      </div>
    </div>
  </section>

  <!-- Sobre a loja -->
  <section class="sobre" id="sobre">
    <h2>Sobre a Jangal</h2>
    <p>Somos a <strong>Jangal</strong>, especializados em eletrônicos e variedades. Aqui você encontra produtos de qualidade, preços acessíveis e atendimento rápido. Nossa missão é facilitar o seu dia a dia com soluções práticas e confiáveis.</p>
  </section>

  <!-- Formas de pagamento -->
  <section class="pagamento">
    <h2>Formas de Pagamento</h2>
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/Visa_2014_logo_detail.svg/2560px-Visa_2014_logo_detail.svg.png" alt="Visa">
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2a/Mastercard-logo.svg/2560px-Mastercard-logo.svg.png" alt="Mastercard">
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f0/Boleto_Banc%C3%A1rio_Logo.svg/2560px-Boleto_Banc%C3%A1rio_Logo.svg.png" alt="Boleto">
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e4/PIX_logo.svg/2560px-PIX_logo.svg.png" alt="PIX">
  </section>

  <!-- Contato -->
  <section class="contato" id="contato">
    <h2>Contato</h2>
    <form>
      <input type="text" placeholder="Nome" required>
      <input type="email" placeholder="E-mail" required>
      <textarea rows="5" placeholder="Mensagem" required></textarea>
      <button type="submit">Enviar</button>
    </form>
  </section>

  <!-- Rodapé -->
  <footer>
    <p>&copy; 2025 Jangal. Todos os direitos reservados.</p>
    <p>Siga-nos: 
      <a href="#">Instagram</a> | 
      <a href="#">Facebook</a> | 
      <a href="#">WhatsApp</a>
    </p>
  </footer>

</body>
</html>
