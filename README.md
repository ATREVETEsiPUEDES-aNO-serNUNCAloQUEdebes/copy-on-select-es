# TiddlyWiki5 Copy on Select

Copy what you are selecting inside the wiki into the clipboard when holding mouse for 1 second

## Motivacion Motivation

Me he acostumbrado a utilizar convenientes[[Copy On Select|https://addons.mozilla.org/en-US/firefox/addon/copy-on-select]] Firefox Complementos, ahora aqui TiddlyWiki A menudo pienso que lo he copiado despues de seleccionarlo, y luego lo pego en otro lugar solo para descubrir que en realidad no ha sido copiado. No estoy acostumbrado a ello.。

Asi que yo mismo reescribi una adaptacion. TiddlyWiki Seleccione y copie el guion.。

I've gotten used to using the handy [[Copy On Select|https://addons.mozilla.org/en-US/firefox/addon/copy-on-select]] Firefox plugin, but now in TiddlyWiki I often still think I've copied it when I select it, and then I found out that I hadn't copied it until I pasted it somewhere else, which was very uncomfortable.

So I rewrote my own copy-on-selection script for TiddlyWiki.

## Uso Usage

Seleccione cualquier texto fuera del area del editor, boton, etc. y mantenga presionado el mouse durante un segundo para copiar el contenido seleccionado.。

Las declaraciones condicionales de este complemento impiden que surta efecto en areas especiales como el editor para evitar interferencias.「Seleccione y pegue todo para cubrir el contenido original.」Espere la operacion。

Select any text outside the editor, buttons, etc., and hold the mouse down for a second to copy the selected content.

The conditional statement in this plugin makes it not work in special areas like the editor, so as not to interfere with operations like "select all and paste overwrite".

## Development

See [tiddly-gittly/Tiddlywiki-WikiText-Plugin-Template](https://github.com/tiddly-gittly/Tiddlywiki-WikiText-Plugin-Template) for detail.

There are some scripts you can run to boost your development.

After `npm i`:

- `npm run dev` to auto pack the plugin and run a demo site. Your change in the src directory will automatically refresh the site.
- `npm run dev-html` to see demo site with packed plugin after you finish your development, this can be your final check, this runs slower than `npm run dev`

### After the plugin is complete

#### Publish

Enable github action in your repo (in your github repo - setting - action - general) if it is not allowed, and when you tagging a new version `vx.x.x` in a git commit and push, it will automatically publish to the github release.

#### Demo

You will get a Github Pages demo site automatically after publish. If it is 404, you may need to manually enable Github Pages in your github repo:

Settings - Pages (on left side) - Build and deployment- Source - choose `"Github Actions"`

Next time you trigger a publish, the site will be updated. You can see the site link in Settings - Pages
