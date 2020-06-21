<script>
    export let product;
    import {link} from 'svelte-routing';

    console.log(product);

</script>

<article class="product">
    <div class="img-container">
        <img src="{product.image}" alt="{product.title}">
        <a href={`/products/${product.id}`} class="btn btn-primary product-link" use:link>details</a>
    </div>
    <div class="product-footer">
        <p class="product-title">{product.title}</p>
        <p class="product-title">${product.price}</p>
    </div>
</article>