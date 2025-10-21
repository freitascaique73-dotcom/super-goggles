<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pousada Praia Grande Aviação</title>
  <style>
    body {font-family: Arial, sans-serif; margin: 0; padding: 0; background-color: #f8f8f8; color: #333;}
    header {background: #0077b6; color: white; text-align: center; padding: 20px;}
    section {padding: 20px;}
    h2 {color: #0077b6;}
    .packages {display: flex; flex-wrap: wrap; justify-content: space-around;}
    .package {background: white; padding: 20px; border-radius: 10px; box-shadow: 0 2px 6px rgba(0,0,0,0.1); margin: 10px; width: 300px; text-align: center;}
    .carousel {position: relative; max-width: 800px; margin: 40px auto; overflow: hidden; border-radius: 10px;}
    .carousel img {width: 100%; display: none; border-radius: 10px;}
    .carousel img.active {display: block;}
    .caption {text-align: center; background: rgba(0,0,0,0.6); color: white; position: absolute; bottom: 0; width: 100%; padding: 10px; font-size: 16px; border-radius: 0 0 10px 10px;}
    .thumbnails {display: grid; grid-template-columns: repeat(3, 1fr); gap: 10px; max-width: 800px; margin: 10px auto;}
    .thumbnails img {width: 100%; border-radius: 8px; cursor: pointer; opacity: 0.8; transition: 0.3s;}
    .thumbnails img:hover {opacity: 1; transform: scale(1.03);}
    .contact {background: #0077b6; color: white; text-align: center; padding: 20px;}
    .button {display: inline-block; background: #00b894; color: white; padding: 10px 20px; margin: 10px; border-radius: 6px; text-decoration: none;}
  </style>
</head>
<body>
  <header>
    <h1>Pousada Praia Grande Aviação</h1>
    <p>Conforto e tranquilidade à beira-mar</p>
  </header>

  <section>
    <h2>Pacotes de Fim de Ano</h2>
    <div class="packages">
      <div class="package">
        <h3>Com Café da Manhã</h3>
        <p>Até 5 pessoas</p>
        <p><strong>R$ 1.200,00</strong></p>
      </div>
      <div class="package">
        <h3>Com Café da Manhã, Almoço e Janta</h3>
        <p>Até 5 pessoas</p>
        <p><strong>R$ 1.800,00</strong></p>
      </div>
    </div>
  </section>

  <section>
    <h2>Galeria de Fotos</h2>
    <div class="carousel">
      <img src="foto1.jpeg" class="active" alt="Suíte Família">
      <div class="caption">Suíte Família — Conforto para até 5 pessoas</div>
      <img src="foto2.jpeg" alt="Área externa">
      <img src="foto3.jpeg" alt="Quarto casal">
      <img src="foto4.jpeg" alt="Vista da praia">
      <img src="foto5.jpeg" alt="Espaço aconchegante">
      <img src="foto6.jpeg" alt="Ambiente completo">
    </div>

    <div class="thumbnails">
      <img src="foto1.jpeg" onclick="showSlide(0)">
      <img src="foto2.jpeg" onclick="showSlide(1)">
      <img src="foto3.jpeg" onclick="showSlide(2)">
      <img src="foto4.jpeg" onclick="showSlide(3)">
      <img src="foto5.jpeg" onclick="showSlide(4)">
      <img src="foto6.jpeg" onclick="showSlide(5)">
    </div>
  </section>

  <section class="contact">
    <h2>Reserve pelo WhatsApp</h2>
    <a class="button" href="https://wa.me/55996479485?text=Olá! Gostaria de fazer uma reserva na Pousada Praia Grande Aviação." target="_blank">Pagar via WhatsApp</a>
    <a class="button" href="https://wa.me/55996479485?text=Olá! Estou enviando o comprovante de pagamento da minha reserva na Pousada Praia Grande Aviação." target="_blank">Enviar comprovante</a>
  </section>

  <script>
    let currentSlide = 0;
    const slides = document.querySelectorAll('.carousel img');
    const caption = document.querySelector('.caption');
    const captions = [
      'Suíte Família — Conforto para até 5 pessoas',
      'Área externa — Ambiente tranquilo e ventilado',
      'Quarto casal — Ideal para relaxar com conforto',
      'Vista da praia — Aproveite o melhor da Aviação',
      'Espaço aconchegante — Simplicidade e charme',
      'Ambiente completo — Hospedagem com o melhor custo-benefício'
    ];

    function showSlide(index) {
      slides[currentSlide].classList.remove('active');
      currentSlide = index;
      slides[currentSlide].classList.add('active');
      caption.textContent = captions[currentSlide];
    }

    function nextSlide() {
      showSlide((currentSlide + 1) % slides.length);
    }

    setInterval(nextSlide, 4000);
  </script>
</body>
</html>
