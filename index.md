---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: reveal
---
<script src="https://ncsu-libraries.github.io/annona/dist/annona.js"></script>
<link rel="stylesheet" type="text/css" href="https://ncsu-libraries.github.io/annona/dist/annona.css">

{% for slide in site.slides %}

{% if slide.website %}

<section data-background-iframe="{{slide.website}}" data-background-interactive>
</section>
{% elsif slide.type == 'script' %}
<section>
	{{slide.content}}
</section>
{% else %}
<section class="center">
	<h1>{{slide.title}}</h1>
{{slide.content}}
</section>
{% endif %}
{% endfor %}
<style>
	.annotation, .imagetitle > *{
		color: black!important;
	}
	.iiifannotation {
		height: 85vh;
		overflow: auto;
	}
	code {
		word-wrap: break-word!important;
		white-space: normal;
		word-break: break-all;
	}
	section {
	font-size: calc(1vw + 2.5vh);
	}
	.tagging:before {
		background: #191919;
	}
	.tagging:after {
		background: #191919;
	}
	iframe {
		background: white;
	}
</style>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.4.1/jquery.js" integrity="sha256-WpOohJOqMqqyKL9FccASB9O0KwACQJpFTUBLTYOVvVU=" crossorigin="anonymous"></script>
