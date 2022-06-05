## DESAFIO ALURA

You can use the [editor on GitHub](https://github.com/DntasDaniel/Desafio-Alura-ONE/edit/main/docs/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### CÓDIGO USADO

var i = 0;
var lista = [];
function verificacrip(x){
    console.log(x);
    limpar;
    imprime(x);
}

function limpar(){
    document.getElementById("descript").value = "";
}

function imprime(lista1){
    var aux1 = [];
    var aux2 = [];
    var aux3 = [];
    aux2 = lista1;
    var n = 0;
        for(i=0; i < aux2.length; i++){
            if(aux2[n] == "e"){
                    aux3.push("enter");
                    console.log("1 " + aux3);
                    n = n+1;
            //escreve a variavel e não a lista
                }else if(aux2[n] == "a"){
                    aux3.push("ai");
                    console.log("2 " + aux3);
                    n = n+1;
            //escreve a variavel e não a lista
                    } else if(aux2[n] == "i"){
                        aux3.push("imes");
                        console.log("3 " + aux3);
                        n = n+1;
                //escreve a variavel e não a lista
                        }else if(aux2[n] == "o"){
                            aux3.push("ober");
                            console.log("4 " + aux3);
                            n = n+1;
                    //escreve a variavel e não a lista
                            }else if(aux2[n] == "u"){
                                    aux3.push("ufat");
                                    console.log("5 " + aux3);
                                    n = n+1;
                            //escreve a variavel e não a lista
                                }else{
                                        aux3.push(aux2[n]);
                                        console.log("4 " + aux3);
                                        n = n+1;
                                //escreve a variavel e não a lista
                                }
        }
    return finalcrip(aux3);
}

function finalcrip(acabar){
    var aux = acabar.join([separador = '']);
    document.getElementById('descript').innerHTML= aux;
}

//-----------///-------------------------//////-----------------//////-----------------//////----------

function verificadescrip(){
    var listadescrip = '';
    erase;
    listadescrip = document.getElementById("descript").value;
    imprime1(listadescrip);
}

function erase(){
    document.getElementById("descript").value = "";
}

function imprime1(lista2){
    var aux1 = [];
    var aux2 = [];
    var aux1 = lista2;
    aux1 = aux1.toLowerCase();
    var aux2 = aux1.split("");
    var aux3= [];
    var n = 0;
    var k = 0;
    console.log(aux2);
    for(i=0; i <aux2.length; i++){
        if(aux2[n] =="e"){
            n = n+1;
            if(aux2[n] =="n"){
                n = n+1;
                if(aux2[n] =="t"){
                    n = n+1;
                    if(aux2[n] =="e"){
                        n = n+1;
                        if(aux2[n] =="r"){
                            aux3.push("e");
                            n = n+1;

                        }
                    }
                }
            }
        }else if(aux2[n] =="a"){
            n = n+1;
                if(aux2[n] =="i"){
                    aux3.push("a");
                    n = n+1;
                }
        } else if(aux2[n] =="i"){
            n = n+1;
            if(aux2[n] =="m"){
                n = n+1;
                if(aux2[n] =="e"){
                    n = n+1;
                    if(aux2[n] =="s"){
                            aux3.push("i");
                            n = n+1;
                    }
                }
            }
        } else if(aux2[n] =="o"){
            n = n+1;
            if(aux2[n] =="b"){
                n = n+1;
                if(aux2[n] =="e"){
                    n = n+1;
                    if(aux2[n] =="r"){
                            aux3.push("o");
                            n = n+1;
                    }
                }
            }
        }else if(aux2[n] =="u"){
            n = n+1;
            if(aux2[n] =="f"){
                n = n+1;
                if(aux2[n] =="a"){
                    n = n+1;
                    if(aux2[n] =="t"){
                            aux3.push("u");
                            n = n+1;
                    }
                }
            }
        }else{
            aux3.push(aux2[n]);
            console.log("4 " + aux3);
            n = n+1;
        }

    } 

    return final(aux3);

}

function final(acaba){
    console.log("lista " +acaba);
    var aux = acaba.join([separador = '']);
    document.getElementById('cript').innerHTML= aux;
}



const criptInput = document.querySelector("#cript");

criptInput.addEventListener("keypress",function(e,char){
        if(!checkChar1(e)){
            e.preventDefault();
        }

    });

function checkChar1(e){

    const char = String.fromCharCode(e.keyCode);
    const pattern ='[a-z0-9 ]';
    if(char.match(pattern)){
        console.log(char);
        lista.push(char);
        verificacrip(lista);
        return true;
    }
    //----------//----------//
}

btn2.onclick = verificadescrip, erase;





<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Criptografia</title>
    <script src = "aluraDesafio.js" defer>  </script>

    <img class="alura" src="https://www.alura.com.br/assets/img/alura-share.1647533642.png" height="110" width="110">
    <br>
</head>

<body>
    <textarea type="text" id="cript" name="cript" cols="50" rows="20" placeholder="Digita aqui a mensagem a ser criptografada"></textarea>
    <textarea type="text" id="descript" name="cript" cols="50" rows="20" placeholder="Digita aqui a mensagem a ser descriptografada"></textarea>
    <img class="alura" src="https://trello.com/1/cards/627ab96c5cfb52798dc4d162/attachments/627ab96c5cfb52798dc4d324/download/1.PNG"height="450">
    <br>
    <p class="alerta">Digite apenas letras minúsculas e sem acento</p>
    <p class="alerta">Ao escrever já criptograva automaticamente!<p>
        <button  id = "btn" class="btnreflesh" onclick="window.location.reload()" >REFLESH</button>
    <button  id = "btn2" class="bdescrip" >Descriptografar</button>

        <style>
            body{
                background-color: rgb(185, 242, 224);
            }

            .alura{
                border-radius: 20px;

            }

            textarea{
                width: 300px;
                height: 400px;
                border-radius: 5px;
                margin-left: 30px;
                margin-right: 30px;
            }

            .alerta{
                margin-left: 32px;
                color: rgb(97, 93, 93);
            }


            button {
                border:solid 1px black;

            }

            textarea{
                border: solid 2px black;
            }

            .btnreflesh{
                margin-left: 30px;
                background-color: rgb(0, 139, 253);
                border-radius: 5px;
                cursor:pointer;
                font-size: 30px;
            }

            .bdescrip{
                margin-left: 220px;
                background-color: rgb(0, 139, 253);
                border-radius: 5px;
                cursor:pointer;
                font-size: 30px;
            }

        </style>


</body>
</html>
}
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/DntasDaniel/Desafio-Alura-ONE/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
