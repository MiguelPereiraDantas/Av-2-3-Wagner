# Taylor-Swift-s-Album-Collections
## Trabalho para apresentação da 2/3 Av

### Alunos:
 - Gabriel Dias Barros

 - Giovana Gouvêa Palomare

## Requesitos usados para a criação: 

Para criar este site, foram utilizadas as seguintes tecnologias e requisitos:

1. **HTML**: Utilizado para estruturar as páginas da web e definir seu conteúdo.

2. **CSS**: Utilizado para estilizar os elementos HTML, incluindo layout, cores, fontes e responsividade.


## 3. **JavaScript**

 - **Alternância da Navbar**: JavaScript foi utilizado para alternar a visibilidade da barra de navegação quando o ícone do menu é clicado.
- **Efeito de Rolagem do Cabeçalho**: JavaScript foi utilizado para adicionar um efeito de rolagem ao cabeçalho quando o usuário rola a página para baixo.
- **Alternador de Tema**: JavaScript foi utilizado para alternar entre temas claro e escuro.
 - **Galeria de Imagens**: JavaScript foi utilizado para implementar funcionalidade para uma galeria de imagens, permitindo que os usuários cliquem em imagens pequenas para visualizar versões maiores.
 - **Contador Regressivo**: JavaScript foi utilizado para criar um contador regressivo para uma data específica.
 - **Inicialização do Slider Swiper**: JavaScript foi utilizado para inicializar sliders Swiper para as seções de produto e revisão.

 ## Funcionalidades JavaScript:

Para implementar várias funcionalidades interativas no website das coleções de álbuns da Taylor Swift, foram utilizadas as seguintes técnicas e recursos do JavaScript:

1. **Alternância da Navbar**:
   - Foi implementada uma funcionalidade que permite alternar a visibilidade da barra de navegação quando o ícone do menu é clicado. Isso proporciona uma experiência de navegação mais amigável em dispositivos móveis.
   

    Exemplo de código:
   ```javascript
   let navbar = document.querySelector('.navbar')

   document.querySelector('#menu-bar').onclick = () =>{
       navbar.classList.toggle('active');
   }

   document.querySelector('#close').onclick = () =>{
       navbar.classList.remove('active');
   }

2. **Efeito de Rolagem do Cabeçalho**:
   - Foi adicionado um efeito de rolagem ao cabeçalho que altera sua aparência quando o usuário rola a página para baixo. Isso ajuda a manter a visibilidade do cabeçalho e da barra de navegação enquanto o usuário explora o conteúdo da página.


      Exemplo de código:
   ```javascript
    window.onscroll = () =>{
    navbar.classList.remove('active');

    if(window.scrollY > 100){
        document.querySelector('header').classList.add('active');
    }else{
        document.querySelector('header').classList.remove('active');
    }
}

3. **Alternador de Tema**:
   - Foi implementada uma funcionalidade que permite aos usuários alternar entre temas claro e escuro. Isso oferece personalização visual e melhora a experiência do usuário em diferentes condições de iluminação.
   
      Exemplo de código:
   ```javascript
    let themeToggler = document.querySelector('#theme-toggler');

    themeToggler.onclick = () =>{
    themeToggler.classList.toggle('fa-sun');
    if(themeToggler.classList.contains('fa-sun')){
        document.querySelector('body').classList.add('active');
    }else{
        document.querySelector('body').classList.remove('active');
    }
}

4. **Galeria de Imagens**:
   - Foi criada uma galeria de imagens onde os usuários podem clicar em imagens pequenas para visualizar versões maiores. Isso permite uma experiência de visualização mais detalhada e interativa do conteúdo visual.


       Exemplo de código:
   ```javascript
    document.querySelectorAll('.small-image-1').forEach(images =>{
    images.onclick = () =>{
        document.querySelector('.big-image-1').src = images.getAttribute('src');
    }
});


5. **Contador Regressivo**:
   - Foi desenvolvido um contador regressivo que exibe o tempo restante até uma data específica. Essa funcionalidade é útil para criar expectativa em torno de eventos futuros, como lançamentos de álbuns ou eventos especiais.

       Exemplo de código:
   ```javascript
    let countDate = new Date('aug 1, 2021 00:00:00').getTime();

    function countDown(){

    let now = new Date().getTime();
    gap = countDate - now;

    let seconds = 1000;
    let minutes = seconds * 60;
    let hours = minutes * 60;
    let days = hours * 24;

    let d = Math.floor(gap / (days));
    let h = Math.floor((gap % (days)) / (hours));
    let m = Math.floor((gap % (hours)) / (minutes));
    let s = Math.floor((gap % (minutes)) / (seconds));

    document.getElementById('days').innerText = d;
    document.getElementById('hours').innerText = h;
    document.getElementById('minutes').innerText = m;
    document.getElementById('seconds').innerText = s;

}

     setInterval(function(){
        countDown()
},1000);



6. **Inicialização do Slider Swiper**:
   - Foram inicializados sliders Swiper nas seções de produto e revisão do site. Isso proporciona uma experiência de visualização dinâmica e responsiva para os usuários que exploram essas seções.

       Exemplo de código:
   ```javascript
    var swiper = new Swiper(".product-slider", {
    slidesPerView: 3,
    loop:true,
    spaceBetween: 10,
    autoplay: {
        delay: 4000,
        disableOnInteraction: false,
    },
    navigation: {
        nextEl: ".swiper-button-next",
        prevEl: ".swiper-button-prev",
    },
    breakpoints: {
        0: {
            slidesPerView: 1,
        },
        550: {
          slidesPerView: 2,
        },
        800: {
          slidesPerView: 3,
        },
        1000: {
            slidesPerView: 3,
        },
    },
});

Essas funcionalidades JavaScript foram essenciais para tornar o website das coleções de álbuns da Taylor Swift mais interativo, envolvente e amigável ao usuário.

---

4. **Font Awesome**: Utilizado para ícones usados em todo o site, como o ícone da barra de menu, ícones de mídia social e alternador de temas.

5. **Swiper.js**: Utilizado para criar sliders responsivos para as seções de produto e revisão.

6. **Imagens Personalizadas**: Imagens personalizadas foram usadas para fundos, capas de álbuns e outros elementos visuais em todo o site.

7. **Fontes Personalizadas**: O site utiliza as famílias de fontes Verdana, Geneva, Tahoma e sans-serif.

8. **Cores Personalizadas**: Variáveis de cor personalizadas foram definidas usando CSS para uso consistente de cores em todo o site.

## Uso

Para usar ou contribuir com este site:
- Clone este repositório para a sua máquina local.
- Abra o arquivo `index.html` em um navegador da web para visualizar o site localmente.
- Faça alterações nos arquivos HTML, CSS ou JavaScript conforme necessário.
- Teste suas alterações localmente e certifique-se de que funcionam conforme o esperado.
- Faça commit das suas alterações e envie-as para o seu repositório.
- Crie uma pull request se desejar contribuir com suas alterações de volta para o repositório original.

## Créditos

Este site foi criado por Giovana Gouvêa Palomare e Gabriel Dias Barros como parte de um prova de laboratório de programação 3. 

Sobre a supervisão do Pofessor Wagner Palmeira.

## Conhecimentos adicionais de JavaScript

Utilizamos a opnião e conhecimento do Aluno Miguel Pereira do 7 período da instituição CESMAC.

Com a ajuda e a mentoria de Miguel dentro dos limites, foi passados alguns artigos de JavaScript e seus Frameworks com o intuito de aprendizado.

## Atendendo aos requisitos 

- O código segue as características de um design responsivo e mobile-first 
 tendo em vista que :

1. **Uso de Media Queries**: O código inclui media queries em várias partes para ajustar estilos com base no tamanho da tela. Isso garante que o layout e os elementos da página se ajustem corretamente em diferentes dispositivos.

2. **Tamanhos de Fonte Relativos**: O tamanho da fonte é definido em porcentagens ou em unidades relativas como "rem". Isso significa que o tamanho da fonte se ajustará automaticamente com base no tamanho da tela do dispositivo, tornando o conteúdo legível em dispositivos de diferentes tamanhos.

3. **Layout Flexível**: O layout da página usa flexbox em várias seções, o que facilita a adaptação do conteúdo em diferentes larguras de tela. Isso é particularmente útil em dispositivos móveis, onde o espaço é limitado e o conteúdo precisa ser organizado de maneira eficiente.

4. **Ordem de Estilos Prioritária para Dispositivos Móveis**: O código aplica estilos básicos primeiro e, em seguida, usa media queries para adicionar estilos específicos para dispositivos maiores. Essa abordagem segue o princípio do design mobile-first, garantindo que o layout e os estilos sejam otimizados para dispositivos móveis e, em seguida, aprimorados para dispositivos maiores.