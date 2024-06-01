<h1>
    <a href="https://www.dio.me/">
     <img align="center" width="40px" src="https://hermes.digitalinnovation.one/assets/diome/logo-minimized.png"></a>
    <span>Formação CSS Web Developer</span>
</h1>

# :computer: Desafio 05: Clonando o Site da HBO Max com Animações em HTML e CSS

<p align="center">
  O projeto é um clone do site <a href="https://www.hbomax.com/br/pt">HBO Max</a>, com o intuito de reproduzir a interface, com algumas modificações, aplicando os temas abordados ao longo das aulas de CSS da plataforma da <a href="https://dio.me">Digital Innovation One</a>.
</p>
<p align="center">
  O clone do site HBO Max serve como desafio para os alunos da plataforma testarem seus conhecimentos e colocarem em prática os recursos de HTML e CSS abordados nos cursos.
</p>

<h2 id="topics">📦 Temas abordados</h2>

O projeto possui como intuito aplicar os conceitos abordados na Trilha de CSS da <a href="https://dio.me">DIO</a>, ministrada pela instrutora <a href="https://github.com/micheleambrosio">Michele Ambrosio</a>.

Recursos CSS presentes no projeto:

- Fundamentos do CSS
- Grid Layout
- Flexbox
- Responsividade
- Pseudo-elementos
- Pseudo-classes
- Transformações 2D e 3D
- Transições e animações
- Tratamento de campos inválidos no formulário

# :bulb: Solução do desafio

Foi feito um fork do projeto da instrutora (https://github.com/micheleambrosio/hbomax) para treinar principalmente transições e animações. 

Eu reduzi o ângulo de rotação e aumente o tempo da animação para o botão "ASSINE AGORA"

```css
.header__button {
  animation: wiggle 3.5s linear infinite;
}

@keyframes wiggle {
  0%,
  10% {
    transform: rotate(0);
  }
  15% {
    transform: rotate(-5deg);
  }
  20% {
    transform: rotate(2deg);
  }
  25% {
    transform: rotate(-2deg);
  }
  30% {
    transform: rotate(2deg);
  }
  35% {
    transform: rotate(-2deg);
  }
  40%,
  100% {
    transform: rotate(0);
  }
}
```

E, além de rotacionar, reduzi o brilho da carta do plano de assinatura não selecionado. 

```css
.subscription__plans:has(.subscription__card:nth-child(1):hover)
  .subscription__card:nth-child(2) {
  transform: rotateY(-45deg);
  filter: brightness(0.4);
}

.subscription__plans:has(.subscription__card:nth-child(2):hover)
  .subscription__card:nth-child(1) {
  transform: rotateY(45deg);
  filter: brightness(0.4);
}
```