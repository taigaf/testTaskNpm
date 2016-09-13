# testTaskNpm
テスト的なnpmで動くタスクランナー
```
"scripts": {
    "serve": "browser-sync start --server ./",
    "css:min": "csso ./test/common/css/style.css ./test/common/css/style.min.css",
    "css:sass": "node-sass --include-path scss ./test/common/_scss/**.scss ./test/common/css/**.css",
    "css:comb": "csscomb ./test/common/css/**.css",
    "css:prefix": "postcss --use autoprefixer --autoprefixer.browsers 'ios >= 8, android >= 4.1, last 2 versions' ./test/common/css/**.css -d ./dest/common/css/",
    "js:lint": "jshint ./test/common/js/**.js",
    "html:lint": "htmlhint ./test/**.html",
    "watch:css": "watch 'npm run css:sass && npm run css:comb && npm run css:prefix' ./test/common/_scss/",
    "watch:js": "watch 'npm run js:lint' ./test/common/js/",
    "watch:html": "watch 'npm run html:lint' ./test/",
    "start": "npm-run-all -p watch:*"
}
```

## serve  
  ローカルサーバ立ち上げる
## css:min
CSS圧縮

## css:sass
sassコンパイル

## css:comb
CSS整形（abc順）
→別途設定ファイルをアップする必要がある
```
{
    "exclude": [
        ".git/**",
        "node_modules/**",
        "bower_components/**"
    ],
    "always-semicolon": true,
    "block-indent": "",
    "color-case": "lower",
    "color-shorthand": true,
    "element-case": "lower",
    "eof-newline": true,
    "leading-zero": false,
    "quotes": "single",
    "remove-empty-rulesets": true,
    "space-after-colon": " ",
    "space-after-combinator": " ",
    "space-after-opening-brace": "\n",
    "space-after-selector-delimiter": "\n",
    "space-before-closing-brace": "\n",
    "space-before-colon": "",
    "space-before-combinator": " ",
    "space-before-opening-brace": " ",
    "space-before-selector-delimiter": "",
    "strip-spaces": true,
    "unitless-zero": true,
    "vendor-prefix-align": true,
    "sort-order": [
            [
                "-moz-animation-delay",
                "-moz-animation-direction",
                "-moz-animation-duration",
                "-moz-animation-iteration-count",
                "-moz-animation-name",
                "-moz-animation-play-state",
                "-moz-animation-timing-function",
                "-moz-animation",
                "-moz-background-clip",
                "-moz-background-size",
                "-moz-border-image-outset",
                "-moz-border-image-repeat",
                "-moz-border-image-slice",
                "-moz-border-image-source",
                "-moz-border-image-width",
                "-moz-border-image",
                "-moz-border-radius-bottomleft",
                "-moz-border-radius-bottomright",
                "-moz-border-radius-topleft",
                "-moz-border-radius-topright",
                "-moz-border-radius",
                "-moz-box-shadow",
                "-moz-box-sizing",
                "-moz-hyphens",
                "-moz-tab-size",
                "-moz-text-align-last",
                "-moz-transform-origin",
                "-moz-transform",
                "-moz-transition-delay",
                "-moz-transition-duration",
                "-moz-transition-property",
                "-moz-transition-timing-function",
                "-moz-transition",
                "-moz-user-select",
                "-ms-animation-delay",
                "-ms-animation-direction",
                "-ms-animation-duration",
                "-ms-animation-iteration-count",
                "-ms-animation-name",
                "-ms-animation-play-state",
                "-ms-animation-timing-function",
                "-ms-animation",
                "-ms-background-position-x",
                "-ms-background-position-y",
                "-ms-filter:\\'progid:DXImageTransform.Microsoft.Alpha",
                "-ms-filter:\\'progid:DXImageTransform.Microsoft.gradient",
                "-ms-interpolation-mode",
                "-ms-overflow-x",
                "-ms-overflow-y",
                "-ms-text-align-last",
                "-ms-text-justify",
                "-ms-text-overflow",
                "-ms-transform-origin",
                "-ms-transform",
                "-ms-transition-delay",
                "-ms-transition-duration",
                "-ms-transition-property",
                "-ms-transition-timing-function",
                "-ms-transition",
                "-ms-user-select",
                "-ms-word-break",
                "-ms-word-wrap",
                "-ms-writing-mode",
                "-o-animation-delay",
                "-o-animation-direction",
                "-o-animation-duration",
                "-o-animation-iteration-count",
                "-o-animation-name",
                "-o-animation-play-state",
                "-o-animation-timing-function",
                "-o-animation",
                "-o-background-size",
                "-o-border-image-outset",
                "-o-border-image-repeat",
                "-o-border-image-slice",
                "-o-border-image-source",
                "-o-border-image-width",
                "-o-border-image",
                "-o-tab-size",
                "-o-transform-origin",
                "-o-transform",
                "-o-transition-delay",
                "-o-transition-duration",
                "-o-transition-property",
                "-o-transition-timing-function",
                "-o-transition",
                "-webkit-animation-delay",
                "-webkit-animation-direction",
                "-webkit-animation-duration",
                "-webkit-animation-iteration-count",
                "-webkit-animation-name",
                "-webkit-animation-play-state",
                "-webkit-animation-timing-function",
                "-webkit-animation",
                "-webkit-background-clip",
                "-webkit-background-size",
                "-webkit-border-bottom-left-radius",
                "-webkit-border-bottom-right-radius",
                "-webkit-border-image-outset",
                "-webkit-border-image-repeat",
                "-webkit-border-image-slice",
                "-webkit-border-image-source",
                "-webkit-border-image-width",
                "-webkit-border-image",
                "-webkit-border-radius",
                "-webkit-border-top-left-radius",
                "-webkit-border-top-right-radius",
                "-webkit-box-shadow",
                "-webkit-box-sizing",
                "-webkit-hyphens",
                "-webkit-text-align-last",
                "-webkit-transform-origin",
                "-webkit-transform",
                "-webkit-transition-delay",
                "-webkit-transition-duration",
                "-webkit-transition-property",
                "-webkit-transition-timing-function",
                "-webkit-transition",
                "-webkit-user-select",
                "animation-delay",
                "animation-direction",
                "animation-duration",
                "animation-iteration-count",
                "animation-name",
                "animation-play-state",
                "animation-timing-function",
                "animation",
                "background-attachment",
                "background-clip",
                "background-color",
                "background-image",
                "background-origin",
                "background-position-x",
                "background-position-y",
                "background-position",
                "background-repeat",
                "background",
                "background-size",
                "border-bottom-color",
                "border-bottom-left-radius",
                "border-bottom-right-radius",
                "border-bottom-style",
                "border-bottom-width",
                "border-bottom",
                "border-collapse",
                "border-color",
                "border-image-outset",
                "border-image-repeat",
                "border-image-slice",
                "border-image-source",
                "border-image-width",
                "border-image",
                "border-left-color",
                "border-left-style",
                "border-left-width",
                "border-left",
                "border-radius",
                "border-right-color",
                "border-right-style",
                "border-right-width",
                "border-right",
                "border-spacing",
                "border-style",
                "border-top-color",
                "border-top-left-radius",
                "border-top-right-radius",
                "border-top-style",
                "border-top-width",
                "border-top",
                "border-width",
                "border",
                "bottom",
                "box-decoration-break",
                "box-shadow",
                "box-sizing",
                "caption-side",
                "clear",
                "clip",
                "color",
                "content",
                "counter-increment",
                "counter-reset",
                "cursor",
                "display",
                "empty-cells",
                "filter:progid:DXImageTransform.Microsoft.Alpha(Opacity",
                "filter:progid:DXImageTransform.Microsoft.AlphaImageLoader",
                "filter:progid:DXImageTransform.Microsoft.gradient",
                "flex-align",
                "flex-direction",
                "flex-order",
                "flex-pack",
                "float",
                "font-effect",
                "font-emphasize-position",
                "font-emphasize-style",
                "font-emphasize",
                "font-family",
                "font-size-adjust",
                "font-size",
                "font-smooth",
                "font-stretch",
                "font-style",
                "font-variant",
                "font-weight",
                "font",
                "height",
                "hyphens",
                "left",
                "letter-spacing",
                "line-height",
                "list-style-image",
                "list-style-position",
                "list-style-type",
                "list-style",
                "margin-bottom",
                "margin-left",
                "margin-right",
                "margin-top",
                "margin",
                "max-height",
                "max-width",
                "min-height",
                "min-width",
                "nav-down",
                "nav-index",
                "nav-left",
                "nav-right",
                "nav-up",
                "opacity",
                "outline-color",
                "outline-offset",
                "outline-style",
                "outline-width",
                "outline",
                "overflow-x",
                "overflow-y",
                "overflow",
                "padding-bottom",
                "padding-left",
                "padding-right",
                "padding-top",
                "padding",
                "pointer-events",
                "position",
                "quotes",
                "resize",
                "right",
                "tab-size",
                "table-layout",
                "text-align-last",
                "text-align",
                "text-decoration",
                "text-emphasis-color",
                "text-emphasis-position",
                "text-emphasis-style",
                "text-emphasis",
                "text-indent",
                "text-justify",
                "text-outline",
                "text-overflow-ellipsis",
                "text-overflow-mode",
                "text-overflow",
                "text-shadow",
                "text-transform",
                "text-wrap",
                "top",
                "transform-origin",
                "transform",
                "transition-delay",
                "transition-duration",
                "transition-property",
                "transition-timing-function",
                "transition",
                "user-select",
                "vertical-align",
                "visibility",
                "white-space",
                "width",
                "word-break",
                "word-spacing",
                "word-wrap",
                "z-index",
                "zoom"
            ]
        ]
}
```
上記内容を'node_modules/csscomb/config/csscomb.json'に保存する

## css:prefix
CSSのベンダープレフィックス

## js:lint
JS文法チェック

## html:lint
HTML文法チェック

## watch:*
上記各処理のwatch用

##start
watchタスクをまとめて回す
