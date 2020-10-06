function Sorteio(){
	let num= Math.floor(Math.random() * 60);
	let li = document.createElement("li");
    for (var i = 0; i < 6; i++){
		numSort[i] =num;
		if(numSort[i]<=9){
			numSort[i]='0'+numSort[i];
		}else{
			numSort[i]=''+numSort[i];
		}
		num= Math.floor(Math.random() * 60);
		while(numSort.indexOf(num)!=-1){
			num= Math.floor(Math.random() * 60);
		  }
    }
	for (var i = 0; i < 6; i++){
		li = document.createElement("li");
		li.innerHTML = numSort[i];
		document.getElementById("numSort").append(li);
	}
}


### Lendo os números digitados
Lê as entradas dos números digitados pelo usuário.

function addToList(num, pos){
    if(num.length == 2){
        if(numEsco.indexOf(num)!=-1){
            alert2("Erro","Número escolhido anteriormente. Digite outro número")
        }else if(parseInt(num)>60){
            alert2("Erro", "O números digitado não pode ser maior que 60")
        }else{
            numEsco[pos] = num;
        }
    }
}
