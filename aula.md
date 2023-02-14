O passo abaixo é necessário, pois tinha desativado a mudança de página com o preventDefault

window.history toda vez que clicar no href muda o histórico dele

Coloque um estado no history
window.history.pushState(dados não tem para colocar, como não tem dado não tem string, url que quer colocar no histórico, que está no event)

event.target = quem disparou o evento, no caso o <a> .href que é a propriedade


function handle()
- const route = route[pathname] 
É dentro de parenteses e não ponto para buscar os itens desse objeto

- fetch = é uma promisse (ou seja é assíncrono)
ele sai do linha a linha
porém em que momento o JS volta a computar esse fetch?
 com o .then() -> quando concluir de buscar (fetch()) eu executo uma função
 .then(data) -> ele buscou o objeto .html que o route informou
 data.text() -> transforma o objeto em texto


no fim é preciso executar o handle() para aparecer já na primeira vez que abre a página
window.onpopstate -> dispara um evento nas setas do navegador
No caso é preciso disparar o handle() para que a página seja atualizada

windows.route -> não existe por padrão, porém eu crio ela e já atribuo uma função
- isso é feito pois o route() não estava sendo "puxado" e coloco ele já direto no window


----
Separando em dois arquivos
---

Criando class
- é necessário criar o add(routeName, link)
  this.routes[routeName] = page   ->   significa que a propriedade é igual ao valor