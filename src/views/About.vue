<template>
  <main>
    <div id="sobre-header">
      <nav>
        <ul class="lista-horizontal">
          <li class="item-horizontal"><a href="#sobre">História</a></li>
          <li class="item-horizontal"><a href="#produtos">Produtos</a></li>
          <li class="item-horizontal"><a href="#contato">Contato</a></li>
        </ul>
      </nav>
    </div>
    <section id="sobre">
      <h2>Nossa história</h2>
      <p>
        Há alguns anos, Juliana sempre foi apaixonada por beleza e cuidados
        pessoais. Ela tinha um sonho de criar sua própria linha de cosméticos,
        mas sabia que o mercado já estava saturado de marcas e produtos.
      </p>
      <p>
        Foi então que Juliana teve uma ideia: em vez de criar uma nova linha de
        cosméticos, por que não criar uma loja que vendesse as melhores marcas
        de cosméticos do mundo em um só lugar? Ela queria que sua loja fosse
        conhecida por oferecer a experiência de compra mais luxuosa e exclusiva
        para seus clientes.
      </p>
      <p>
        Com essa ideia em mente, Juliana começou a trabalhar duro em seu plano
        de negócios e pesquisa de mercado. Ela pesquisou as marcas mais
        populares de cosméticos, fez uma lista dos produtos mais vendidos e
        procurou por tendências de beleza que estavam em alta.
      </p>
      <p>
        Depois de muita pesquisa e trabalho duro, Juliana finalmente lançou a
        "Luxo Cosméticos", sua loja de varejo de cosméticos exclusivos e
        luxuosos. Ela começou a negociar com fornecedores e fabricantes para
        oferecer os melhores produtos do mercado em um só lugar.
      </p>
      <p>
        Juliana queria que a experiência de compra na Luxo Cosméticos fosse
        única e luxuosa, então ela criou uma loja elegante e sofisticada que
        oferecia um serviço de atendimento ao cliente excepcional. Os clientes
        eram recebidos com bebidas e petiscos enquanto exploravam os corredores
        repletos de produtos exclusivos e luxuosos.
      </p>
      <p>
        Com o passar do tempo, a Luxo Cosméticos se tornou uma das lojas de
        cosméticos mais populares e bem-sucedidas da cidade, atraindo uma
        clientela fiel e exigente. Juliana estava orgulhosa de sua criação e
        continuou a inovar e oferecer os melhores produtos e serviços para seus
        clientes, mantendo a qualidade e a exclusividade da marca.
      </p>

      <div id="imagem-juliana">
        <figure>
          <img
            src="../../public/img/dona.jpg"
            alt="Fota da desenvolvedora da Luxo Cosméticos"
          />
          <figcaption>Juliana, fundadora da Luxo Cosméticos</figcaption>
        </figure>
      </div>
    </section>

    <section id="produtos">
      <h2>Produtos</h2>
      <p>
        A Luxo Cosméticos oferece uma ampla variedade de produtos exclusivos e
        luxuosos, incluindo:
      </p>
      <ul>
        <li>Maquiagem</li>
        <li>Perfumes</li>
        <li>Cuidados para a pele</li>
        <li>Cuidados para o cabelo</li>
        <li>Acessórios de beleza</li>
      </ul>
      <p>
        Nossa seleção de produtos é cuidadosamente escolhida para atender às
        necessidades de nossos clientes, oferecendo as marcas mais populares e
        renomadas do mercado, como Chanel, Dior, Estée Lauder, entre outras.
      </p>
      <p>
        Também temos produtos exclusivos que você não encontrará em outras
        lojas, como a linha de maquiagem orgânica da RMS Beauty e a coleção de
        fragrâncias artesanais da Le Labo.
      </p>
      <p>
        Nós nos esforçamos para manter nossos preços competitivos, sem
        comprometer a qualidade e a exclusividade de nossos produtos. Além
        disso, oferecemos promoções especiais e descontos frequentes para nossos
        clientes fiéis.
      </p>
    </section>
    <section id="contato">
      <h2>Entre em contato</h2>
      <p>
        Se você tiver alguma dúvida sobre nossos produtos ou serviços, ou
        simplesmente quiser dizer oi, não hesite em nos contatar:
      </p>
      <ul>
        <li>Telefone: (11) 1234-5678</li>
        <li>E-mail: contato@luxocosmeticos.com.br</li>
        <li>Endereço: Rua das Flores, 123, São Paulo, SP</li>
      </ul>
      <p>
        Nós também estamos nas redes sociais! Siga-nos no Instagram e no
        Facebook para ficar por dentro das novidades e promoções:
      </p>
      <ul>
        <li>
          <a href="https://www.instagram.com/luxocosmeticos/">Instagram</a>
        </li>
        <li><a href="https://www.facebook.com/luxocosmeticos/">Facebook</a></li>
      </ul>
    </section>
  </main>
</template>

<style scoped>
body {
  width: 940px;
  margin-left: auto;
  margin-right: auto;
}

footer {
  margin: 40px 0px 10px 0px;
  justify-content: center;
  color: gray;
  text-align: center;
}

footer img {
  margin-right: 30px;
}

figure {
  border: 1px #cccccc solid;
  background-color: #f2eded;
  padding: 10px;
  margin: auto;
}

figcaption {
  font-style: italic;
  padding: 5px;
  text-align: center;
}

#imagem-juliana {
  width: 300px;
  margin: auto;
}

#familia-pelho {
  float: right;
  margin-left: 10px;
}

#sobre-header {
  padding: 9px;
  margin-top: 25px;
  text-align: center;
}

#sobre-header a {
  margin-left: 10px;
}

.lista-horizontal {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #f43f5e;
}

li {
  list-style-type: none;
}

.item-horizontal {
  float: left;
}

.item-horizontal a {
  display: block;
  color: white;
  text-align: center;
  padding: 16px;
  text-decoration: none;
}

.item-horizontal a:hover {
  background-color: #e11d48;
}
</style>
