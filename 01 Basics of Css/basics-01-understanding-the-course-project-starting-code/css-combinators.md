# CSS combinators

1. Adjacent Sibling

An adjacent sibling a combinator that applies the style to every element that matches the combination described by the expression '+'. This means that the style will be applied to the next element after the first placed.

For example:

````css
h2 + p {
    color: red
}
````

Which on HTML code can be seen like this:

````html
<div>
    <h2>Not applied</h2>
    <p>CSS applied</p>
    <h2>Not applied</h2>
    <h2>Not applied</h2>
    <h3>Not applied</h2>
    <p>Not applied</p>
    <h2>Not applied</h2>
    <p>CSS applied</p>
</div>
````

2. General sibling

Related to adjacent sibling, the difference is that in this case the sibling can be just in the same parent and not right before the desired element.

For example:

````css
h2 ~ p {
    color: red
}
````

Which on HTML code can be seen like this:

````html
<div>
    <h2>Not applied</h2>
    <p>CSS applied</p>
    <h2>Not applied</h2>
    <h3>Not applied</h2>
    <p>CSS applied</p>
</div>
````

3. Child combinator

Affects only to direct children of the element, not the nested ones.

````css
h2 > p {
    color: red
}
````

Which on HTML code can be seen like this:

````html
<div>
    <h2>Not applied</h2>
    <p>CSS applied</p>
    <div>Not applied</div>
    <article>
        <p>Not applied</p>
    </article>
    <p>CSS applied</p>
</div>
````

4. Descendant combinator

Will affect all elements nested in the parent element.

````css
h2 p {
    color: red
}
````

Which on HTML code can be seen like this:

````html
<div>
    <h2>Not applied</h2>
    <p>CSS applied</p>
    <div>Not applied</div>
    <article>
        <p>CSS applied</p>
    </article>
    <p>CSS applied</p>
</div>
````
