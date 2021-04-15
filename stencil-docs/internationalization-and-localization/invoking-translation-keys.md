<h1>Invoking Translation Keys</h1>

<div class="otp" id="no-index">
	<h3> On This Page </h3>
	<ul>
		<li><a href="#invoking_translation">Translation Syntax</a></li>
    <li><a href="#invoking_video">Video Demo</a></li>
	</ul>
</div>

<a href='#invoking_translation' aria-hidden='true' class='block-anchor'  id='invoking_translation'></a>

## Translation Syntax

Once keys and values are defined in the [.json translation files](https://github.com/bigcommerce/cornerstone/tree/master/lang), you can invoke dynamic translation strings using the the [custom `{{lang}}` Handlebars helper](/stencil-docs/handlebars-syntax-and-helpers/handlebars-helpers-reference/string-helpers/custom-string-helpers#handlebars_lang). Your invocation would follow this generic format:

<!--
title: "Translation invocation"
subtitle: ""
lineNumbers: true
-->

```
{{lang "translation.key" optionalVariable=”someValue”}}
```

Here is how this works. In a non-internationalized theme, a storefront page might include a string like this:

<!--
title: "Non Internationalized string"
subtitle: ""
lineNumbers: true
-->

```html
<a href="{{ urls.account }}">Welcome Back <span>{{ customer.name }}</span></a>
```

The corresponding internationalized version would substitute the text with the fully dynamic `{{ lang }}` Handlebars helper shown below:

<!--
title: "Internationalized String using {{lang}} Handlebars Helper"
subtitle: ""
lineNumbers: true
-->

```html
<a href="{{ urls.account }}">{{ lang "header.welcome_back" name=customer.name }}</a>
```



<a href='#invoking_video' aria-hidden='true' class='block-anchor'  id='invoking_video'></a>

## Video Demo

Watch a video demonstration of how JSON translation files' key/value pairs interact with your templates' Handlebars statements to localize your storefront pages: 

<iframe width="560" height="315" src="https://www.youtube.com/embed/ygiRGfSrmnA" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<div class="HubBlock--callout">
<div class="CalloutBlock--warning">
<div class="HubBlock-content">
    
<!-- theme: warning -->

### File Permissions Required
> There is no way to re-display this pop-up after selecting Done, so be sure to securely store the credentials before leaving this screen.

</div>
</div>
</div>

