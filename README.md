# Recomendador-de-Filmes
let filme;
let campoIdade;
let campoAcao;
let campoRomance;
let campoComedia;
let campoMachao;
let campoEspecial;

function setup() {
  createCanvas(600, 400);
  createElement('h3',  'Recomendador de Filmes');
  createSpan("Idade: ")
  campoIdade = createInput();
  campoAcao = createCheckbox('Ação');
  campoRomance = createCheckbox('Romance');
  campoComedia = createCheckbox('Comédia');
  campoMachao = createCheckbox('Machão');
  campoEspecial = createCheckbox('Especial')
}

function draw() {
  background(220);
  textSize(40);
  textAlign( CENTER, CENTER);
  
  let idade = campoIdade.value();
  let acao = campoAcao.checked();
  let romance = campoRomance.checked();
  let comedia = campoComedia.checked();
  let Machao = campoMachao.checked();
  let especial = campoEspecial.checked();
  
  filme = geraRecomendacao(idade, acao, romance, comedia, Machao, especial,);
  
  text(filme, width/2, height/2);
}

function geraRecomendacao(idade, acao, romance, comedia, machao, especial){
  if(idade >= 25){
    if(acao){
      return 'Ja foi no passeio?';
    }else if(romance){
      return 'Rafael e o careca perdido';
    }else if(comedia){
      return 'Jakson e o anel perdido';
    }else if(machao){
      return 'Clannad'
    }
  }else if(idade >= 18){
    if(acao){
      return 'Berserk';
    }else if(romance){
      return 'Gustavo e Jackson o encontro ';
    }else if(comedia){
      return 'Gustavo em um dia normal'
    }else if(machao){
      return 'Plastic Memories'
    }else if(especial){
      return 'Jackson o pisca pisca sem fim'
    }
  }else if(idade >= 14){
    if(acao){
      return 'Maze Runner';
    }else if(romance){
      return 'Depois do Universo';
    }else if(comedia){
      return 'Vovozona'
    }else if(machao){
      return 'Hotarubi no mori e'
    }else if(especial){
      return 'carrinhos 2'
    }
  }else{
      
if(acao){
      return 'KarateKid';
    }else if(romance){
      return 'Carros 2';
    }else if(comedia){
      return 'Jackson no multiverso'
    }else if(machao){
      return 'Ano hana a flor que vimos'
    }else if(especial){
      return 'Up'
    }
  }
}
