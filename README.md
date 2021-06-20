# jquery-syntax

---

kod sonları **( ; )** ile belirtilir, stringler alert veya console.log **( ``,''," )( option+, )** ile belirtilir

jquery de **{ }** kullanılır.

## References

```jsx
//Google gibi bir tarayıcıya "Jquery cdn" yazıp ilk çıkana tıkla
//index.html dosyana şunu. yaz => <script src="https://code.jquery.com/jquery-3.2.1.js"/>
```

## Selector

 

```jsx
/*
javascript == document.getElementById('container')

jquery == $('selectors')
selectors == id  => $('#container');
						class => $('.item');
						Element => $('ul');
*/
//örnek

alert($('#liste')); //ekrana ul yazdıracak

console.log($("h3")); // konsola h3 yazacak ve yanına textini vericek
//bu şekilde dilediğiniz gibi kullanabilirsiniz

console.log($('ul li a')); //ul etiketinin altındaki li etiketinin altındaki a
```

## Styling content

```jsx
//jquery ile css özelliği verme V2
$('#container').css('border','1px solid green');

//V2
var style = {
border:1px solid green,
background:black,
color:white,
}
$('#container').css(styles);
//şeklinde jquery ile css ile oynayabilirsiniz
```

## Methods

```jsx
/*
css()
text()
val()
attr().       Daha çok bilgi ve metot için https://api.jquery.com
html()
addClass()
removeClass()
toggleClass()
*/
//Örnek
console.log($('h1').text()); //h1 in içeriğini bize verir

console.log($("input").val())//input taki valu yu input a ekler

$("#ad").addClass("highlight");//class ekledi
$("#soyad").removeClass("green");//class çıkarıldı
//şekillerinde kullanılabilir
```

## Click event

```jsx
$(function() {
$("selector").click(function(){
	console.log('click event çalıştı');
});
//şeklinde kullanabilirsin
```

## Change event

```jsx
/*
$(document).ready()
click()
dbclick()
change()
mouseenter()
mouseleave()
mousedown()
mouseup()
hover()
focus()
blur()
on()
*/
$(document).ready(function () {
$(".control").change(function () {
console.log("change event çalıştı");
});
});
```

## jquery effect

### show-hide

```jsx
$(document).ready(function(){

$("#hide").click(function () { //hide id sini seçtik

	$("p").hide(); //hide id sindeki paragrafı gizledik

});

$("#show").click(function () { //show id sini seçtik

	$("p").show(); //show id sindeki paragrafı açtık

});

});

//Eğer bunu tek buton ile yapmak istiyorsak show ve hide tek id de

$("#toggle").click(function () { //toggle id sini seçtik

	$("p").toggle(); //toggle id sindeki paragrafı açar veya kapatır sana kalmış

});
/*
toggle(speed,callback);
hide(speed,callback)
show(speed,callback);

Şeklindede süresini ayarlayabilirsiniz
*/

$("#show").click(function () { //show id sini seçtik

	$("p").show(1000,function() { //show id sindeki paragrafı 1 saniyede açar

	alert("paragraf gösterildi");

		});

});
```

### Fading

```jsx
/*
$(selector).fadeIn(speed,callback);
$(selector).fadeOut(speed,callback);
$(selector).fadeToggle(speed,callback);
$(selector).fadeTo(speed,callback);

Bunlar geçiş animasyonu fadeIn de senin. ayarladığın hıza göre içe kapanır
fadeOut dışa doğru açılır 

$(selector).slideDown(speed,callback);
$(selector).slideUp(speed,callback);
$(selector).slideToggle(speed,callback);

slideDown yukardan aşağı animasyon gerçekleşir slideUp aşağıdan yukarı 
slideToggle ikisinide gerçekleştirir
*/
```

## Animation

```jsx
$(document).ready(function () {

	$('#animate').click(function () {

$('#box').animate({
left:"200px", //200 px sola gider animasyonlu bir şekilde
with:"300px"; //büyüklüğünü 300 px yapar animayonlu bir şekilde
)};

	});
});

//Bu tarz kullanım şekilleri bulunmakta
```
