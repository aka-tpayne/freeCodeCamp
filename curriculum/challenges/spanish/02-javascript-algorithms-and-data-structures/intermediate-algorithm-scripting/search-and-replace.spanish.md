---
id: a0b5010f579e69b815e7c5d6
title: Search and Replace
localeTitle: Buscar y reemplazar
isRequired: true
challengeType: 5
---

## Description
<section id='description'> 
Realice una búsqueda y reemplace la oración usando los argumentos proporcionados y devuelva la nueva oración. 
primer argumento es la oración para realizar la búsqueda y reemplazar. 
Segundo argumento es la palabra que reemplazará (antes). 
Tercer argumento es con lo que reemplazará el segundo argumento por (después). 
<strong>Nota</strong> <br> Conserve el caso del primer carácter en la palabra original cuando lo reemplace. Por ejemplo, si quiere reemplazar la palabra &quot;Libro&quot; con la palabra &quot;perro&quot;, debe ser reemplazada como &quot;Perro&quot; 
Recuerde usar <a href='http://forum.freecodecamp.org/t/how-to-get-help-when-you-are-stuck/19514' target='_blank'>Lectura-Búsqueda-Preguntar</a> si se atasca. Trate de emparejar el programa. Escribe tu propio código. 
</section>

## Instructions
<section id='instructions'> 

</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: &#39; <code>myReplace(&quot;Let us go to the store&quot;, &quot;store&quot;, &quot;mall&quot;)</code> debe devolver &quot;Vamos <code>myReplace(&quot;Let us go to the store&quot;, &quot;store&quot;, &quot;mall&quot;)</code> &quot;.&#39;
    testString: 'assert.deepEqual(myReplace("Let us go to the store", "store", "mall"), "Let us go to the mall", "<code>myReplace("Let us go to the store", "store", "mall")</code> should return "Let us go to the mall".");'
  - text: &#39; <code>myReplace(&quot;He is Sleeping on the couch&quot;, &quot;Sleeping&quot;, &quot;sitting&quot;)</code> debe devolver &quot;Está sentado en el sofá&quot;.
    testString: 'assert.deepEqual(myReplace("He is Sleeping on the couch", "Sleeping", "sitting"), "He is Sitting on the couch", "<code>myReplace("He is Sleeping on the couch", "Sleeping", "sitting")</code> should return "He is Sitting on the couch".");'
  - text: &#39; <code>myReplace(&quot;This has a spellngi error&quot;, &quot;spellngi&quot;, &quot;spelling&quot;)</code> debe devolver &quot;Esto tiene un error de ortografía&quot;.&#39;
    testString: 'assert.deepEqual(myReplace("This has a spellngi error", "spellngi", "spelling"), "This has a spelling error", "<code>myReplace("This has a spellngi error", "spellngi", "spelling")</code> should return "This has a spelling error".");'
  - text: &#39; <code>myReplace(&quot;His name is Tom&quot;, &quot;Tom&quot;, &quot;john&quot;)</code> debe devolver &quot;Su nombre es John&quot;.
    testString: 'assert.deepEqual(myReplace("His name is Tom", "Tom", "john"), "His name is John", "<code>myReplace("His name is Tom", "Tom", "john")</code> should return "His name is John".");'
  - text: &#39; <code>myReplace(&quot;Let us get back to more Coding&quot;, &quot;Coding&quot;, &quot;algorithms&quot;)</code> debería devolver &quot;Regresemos a más Algoritmos&quot;.
    testString: 'assert.deepEqual(myReplace("Let us get back to more Coding", "Coding", "algorithms"), "Let us get back to more Algorithms", "<code>myReplace("Let us get back to more Coding", "Coding", "algorithms")</code> should return "Let us get back to more Algorithms".");'

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='js-seed'>

```js
function myReplace(str, before, after) {
  return str;
}

myReplace("A quick brown fox jumped over the lazy dog", "jumped", "leaped");
```

</div>



</section>

## Solution
<section id='solution'>


```js
function myReplace(str, before, after) {
  if (before.charAt(0) === before.charAt(0).toUpperCase()) {
    after = after.charAt(0).toUpperCase() + after.substring(1);
  } else {
    after = after.charAt(0).toLowerCase() + after.substring(1);
  }
  return str.replace(before, after);
}
```

</section>