---
title:  friend-斐波那契
date: 2018-10-4 11:43:55
top: true
img:
categories: 程序设计
tags: 
  - ACM
  - 水题
  - 快速幂
---
<html>
<head>
<meta charset='UTF-8'><meta name='viewport' content='width=device-width initial-scale=1'>
<title>friend-斐波那契</title><style type='text/css'>html {overflow-x: initial !important;}:root { --bg-color:#ffffff; --text-color:#333333; --select-text-bg-color:#B5D6FC; --select-text-font-color:auto; --monospace:"Lucida Console",Consolas,"Courier",monospace; }
html { font-size: 14px; background-color: var(--bg-color); color: var(--text-color); font-family: "Helvetica Neue", Helvetica, Arial, sans-serif; -webkit-font-smoothing: antialiased; }
body { margin: 0px; padding: 0px; height: auto; bottom: 0px; top: 0px; left: 0px; right: 0px; font-size: 1rem; line-height: 1.42857; overflow-x: hidden; background: inherit; }
iframe { margin: auto; }
a.url { word-break: break-all; }
a:active, a:hover { outline: 0px; }
.in-text-selection, ::selection { text-shadow: none; background: var(--select-text-bg-color); color: var(--select-text-font-color); }
#write { margin: 0px auto; height: auto; width: inherit; word-break: normal; word-wrap: break-word; position: relative; white-space: normal; padding-bottom: 70px; overflow-x: visible; }
.first-line-indent #write div, .first-line-indent #write li, .first-line-indent #write p { text-indent: 2em; }
.first-line-indent #write div :not(p):not(div), .first-line-indent #write div.md-htmlblock-container, .first-line-indent #write p *, .first-line-indent pre { text-indent: 0px; }
.for-image #write { padding-left: 8px; padding-right: 8px; }
body.typora-export { padding-left: 30px; padding-right: 30px; }
@media screen and (max-width: 500px) {
  body.typora-export { padding-left: 0px; padding-right: 0px; }
  .CodeMirror-sizer { margin-left: 0px !important; }
  .CodeMirror-gutters { display: none !important; }
}
#write > blockquote:first-child, #write > div:first-child, #write > figure:first-child, #write > ol:first-child, #write > p:first-child, #write > pre:first-child, #write > ul:first-child { margin-top: 30px; }
#write li > figure:first-child { margin-top: -20px; }
#write ol, #write ul { position: relative; }
img { max-width: 100%; vertical-align: middle; }
button, input, select, textarea { color: inherit; font-style: inherit; font-variant: inherit; font-weight: inherit; font-stretch: inherit; font-size: inherit; line-height: inherit; font-family: inherit; }
input[type="checkbox"], input[type="radio"] { line-height: normal; padding: 0px; }
*, ::after, ::before { box-sizing: border-box; }
#write h1, #write h2, #write h3, #write h4, #write h5, #write h6, #write p, #write pre { width: inherit; }
#write h1, #write h2, #write h3, #write h4, #write h5, #write h6, #write p { position: relative; }
h1, h2, h3, h4, h5, h6 { break-after: avoid-page; break-inside: avoid; orphans: 2; }
p { orphans: 4; }
h1 { font-size: 2rem; }
h2 { font-size: 1.8rem; }
h3 { font-size: 1.6rem; }
h4 { font-size: 1.4rem; }
h5 { font-size: 1.2rem; }
h6 { font-size: 1rem; }
.md-math-block, .md-rawblock, h1, h2, h3, h4, h5, h6, p { margin-top: 1rem; margin-bottom: 1rem; }
.hidden { display: none; }
.md-blockmeta { color: rgb(204, 204, 204); font-weight: 700; font-style: italic; }
a { cursor: pointer; }
sup.md-footnote { padding: 2px 4px; background-color: rgba(238, 238, 238, 0.7); color: rgb(85, 85, 85); border-radius: 4px; cursor: pointer; }
sup.md-footnote a, sup.md-footnote a:hover { color: inherit; text-transform: inherit; text-decoration: inherit; }
#write input[type="checkbox"] { cursor: pointer; width: inherit; height: inherit; }
figure { overflow-x: auto; margin: 1.2em 0px; max-width: calc(100% + 16px); padding: 0px; }
figure > table { margin: 0px !important; }
tr { break-inside: avoid; break-after: auto; }
thead { display: table-header-group; }
table { border-collapse: collapse; border-spacing: 0px; width: 100%; overflow: auto; break-inside: auto; text-align: left; }
table.md-table td { min-width: 80px; }
.CodeMirror-gutters { border-right: 0px; background-color: inherit; }
.CodeMirror { text-align: left; }
.CodeMirror-placeholder { opacity: 0.3; }
.CodeMirror pre { padding: 0px 4px; }
.CodeMirror-lines { padding: 0px; }
div.hr:focus { cursor: none; }
#write pre { white-space: pre-wrap; }
#write.fences-no-line-wrapping pre { white-space: pre; }
#write pre.ty-contain-cm { white-space: normal; }
.CodeMirror-gutters { margin-right: 4px; }
.md-fences { font-size: 0.9rem; display: block; break-inside: avoid; text-align: left; overflow: visible; white-space: pre; background: inherit; position: relative !important; }
.md-diagram-panel { width: 100%; margin-top: 10px; text-align: center; padding-top: 0px; padding-bottom: 8px; overflow-x: auto; }
#write .md-fences.mock-cm { white-space: pre-wrap; }
.md-fences.md-fences-with-lineno { padding-left: 0px; }
#write.fences-no-line-wrapping .md-fences.mock-cm { white-space: pre; overflow-x: auto; }
.md-fences.mock-cm.md-fences-with-lineno { padding-left: 8px; }
.CodeMirror-line, twitterwidget { break-inside: avoid; }
.footnotes { opacity: 0.8; font-size: 0.9rem; margin-top: 1em; margin-bottom: 1em; }
.footnotes + .footnotes { margin-top: 0px; }
.md-reset { margin: 0px; padding: 0px; border: 0px; outline: 0px; vertical-align: top; background: 0px 0px; text-decoration: none; text-shadow: none; float: none; position: static; width: auto; height: auto; white-space: nowrap; cursor: inherit; -webkit-tap-highlight-color: transparent; line-height: normal; font-weight: 400; text-align: left; box-sizing: content-box; direction: ltr; }
li div { padding-top: 0px; }
blockquote { margin: 1rem 0px; }
li .mathjax-block, li p { margin: 0.5rem 0px; }
li { margin: 0px; position: relative; }
blockquote > :last-child { margin-bottom: 0px; }
blockquote > :first-child, li > :first-child { margin-top: 0px; }
.footnotes-area { color: rgb(136, 136, 136); margin-top: 0.714rem; padding-bottom: 0.143rem; white-space: normal; }
#write .footnote-line { white-space: pre-wrap; }
@media print {
  body, html { border: 1px solid transparent; height: 99%; break-after: avoid; break-before: avoid; }
  #write { margin-top: 0px; border-color: transparent !important; }
  .typora-export * { -webkit-print-color-adjust: exact; }
  html.blink-to-pdf { font-size: 13px; }
  .typora-export #write { padding-left: 1cm; padding-right: 1cm; padding-bottom: 0px; break-after: avoid; }
  .typora-export #write::after { height: 0px; }
  @page { margin: 20mm 0px; }
}
.footnote-line { margin-top: 0.714em; font-size: 0.7em; }
a img, img a { cursor: pointer; }
pre.md-meta-block { font-size: 0.8rem; min-height: 0.8rem; white-space: pre-wrap; background: rgb(204, 204, 204); display: block; overflow-x: hidden; }
p > img:only-child { display: block; margin: auto; }
p > .md-image:only-child { display: inline-block; width: 100%; text-align: center; }
#write .MathJax_Display { margin: 0.8em 0px 0px; }
.md-math-block { width: 100%; }
.md-math-block:not(:empty)::after { display: none; }
[contenteditable="true"]:active, [contenteditable="true"]:focus { outline: 0px; box-shadow: none; }
.md-task-list-item { position: relative; list-style-type: none; }
.task-list-item.md-task-list-item { padding-left: 0px; }
.md-task-list-item > input { position: absolute; top: 0px; left: 0px; margin-left: -1.2em; margin-top: calc(1em - 10px); }
.math { font-size: 1rem; }
.md-toc { min-height: 3.58rem; position: relative; font-size: 0.9rem; border-radius: 10px; }
.md-toc-content { position: relative; margin-left: 0px; }
.md-toc-content::after, .md-toc::after { display: none; }
.md-toc-item { display: block; color: rgb(65, 131, 196); }
.md-toc-item a { text-decoration: none; }
.md-toc-inner:hover { }
.md-toc-inner { display: inline-block; cursor: pointer; }
.md-toc-h1 .md-toc-inner { margin-left: 0px; font-weight: 700; }
.md-toc-h2 .md-toc-inner { margin-left: 2em; }
.md-toc-h3 .md-toc-inner { margin-left: 4em; }
.md-toc-h4 .md-toc-inner { margin-left: 6em; }
.md-toc-h5 .md-toc-inner { margin-left: 8em; }
.md-toc-h6 .md-toc-inner { margin-left: 10em; }
@media screen and (max-width: 48em) {
  .md-toc-h3 .md-toc-inner { margin-left: 3.5em; }
  .md-toc-h4 .md-toc-inner { margin-left: 5em; }
  .md-toc-h5 .md-toc-inner { margin-left: 6.5em; }
  .md-toc-h6 .md-toc-inner { margin-left: 8em; }
}
a.md-toc-inner { font-size: inherit; font-style: inherit; font-weight: inherit; line-height: inherit; }
.footnote-line a:not(.reversefootnote) { color: inherit; }
.md-attr { display: none; }
.md-fn-count::after { content: "."; }
code, pre, samp, tt { font-family: var(--monospace); }
kbd { margin: 0px 0.1em; padding: 0.1em 0.6em; font-size: 0.8em; color: rgb(36, 39, 41); background: rgb(255, 255, 255); border: 1px solid rgb(173, 179, 185); border-radius: 3px; box-shadow: rgba(12, 13, 14, 0.2) 0px 1px 0px, rgb(255, 255, 255) 0px 0px 0px 2px inset; white-space: nowrap; vertical-align: middle; }
.md-comment { color: rgb(162, 127, 3); opacity: 0.8; font-family: var(--monospace); }
code { text-align: left; vertical-align: initial; }
a.md-print-anchor { white-space: pre !important; border-width: initial !important; border-style: none !important; border-color: initial !important; display: inline-block !important; position: absolute !important; width: 1px !important; right: 0px !important; outline: 0px !important; background: 0px 0px !important; text-decoration: initial !important; text-shadow: initial !important; }
.md-inline-math .MathJax_SVG .noError { display: none !important; }
.md-math-block .MathJax_SVG_Display { text-align: center; margin: 0px; position: relative; text-indent: 0px; max-width: none; max-height: none; min-height: 0px; min-width: 100%; width: auto; overflow-y: hidden; display: block !important; }
.MathJax_SVG_Display, .md-inline-math .MathJax_SVG_Display { width: auto; margin: inherit; display: inline-block !important; }
.MathJax_SVG .MJX-monospace { font-family: var(--monospace); }
.MathJax_SVG .MJX-sans-serif { font-family: sans-serif; }
.MathJax_SVG { display: inline; font-style: normal; font-weight: 400; line-height: normal; zoom: 90%; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; word-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; }
.MathJax_SVG * { transition: none; }
.MathJax_SVG_Display svg { vertical-align: middle !important; margin-bottom: 0px !important; }
.os-windows.monocolor-emoji .md-emoji { font-family: "Segoe UI Symbol", sans-serif; }
.md-diagram-panel > svg { max-width: 100%; }
[lang="mermaid"] svg, [lang="flow"] svg { max-width: 100%; }
[lang="mermaid"] .node text { font-size: 1rem; }
table tr th { border-bottom: 0px; }
video { max-width: 100%; display: block; margin: 0px auto; }
iframe { max-width: 100%; width: 100%; border: none; }
.highlight td, .highlight tr { border: 0px; }


.CodeMirror { height: auto; }
.CodeMirror.cm-s-inner { background: inherit; }
.CodeMirror-scroll { overflow-y: hidden; overflow-x: auto; z-index: 3; }
.CodeMirror-gutter-filler, .CodeMirror-scrollbar-filler { background-color: rgb(255, 255, 255); }
.CodeMirror-gutters { border-right: 1px solid rgb(221, 221, 221); background: inherit; white-space: nowrap; }
.CodeMirror-linenumber { padding: 0px 3px 0px 5px; text-align: right; color: rgb(153, 153, 153); }
.cm-s-inner .cm-keyword { color: rgb(119, 0, 136); }
.cm-s-inner .cm-atom, .cm-s-inner.cm-atom { color: rgb(34, 17, 153); }
.cm-s-inner .cm-number { color: rgb(17, 102, 68); }
.cm-s-inner .cm-def { color: rgb(0, 0, 255); }
.cm-s-inner .cm-variable { color: rgb(0, 0, 0); }
.cm-s-inner .cm-variable-2 { color: rgb(0, 85, 170); }
.cm-s-inner .cm-variable-3 { color: rgb(0, 136, 85); }
.cm-s-inner .cm-string { color: rgb(170, 17, 17); }
.cm-s-inner .cm-property { color: rgb(0, 0, 0); }
.cm-s-inner .cm-operator { color: rgb(152, 26, 26); }
.cm-s-inner .cm-comment, .cm-s-inner.cm-comment { color: rgb(170, 85, 0); }
.cm-s-inner .cm-string-2 { color: rgb(255, 85, 0); }
.cm-s-inner .cm-meta { color: rgb(85, 85, 85); }
.cm-s-inner .cm-qualifier { color: rgb(85, 85, 85); }
.cm-s-inner .cm-builtin { color: rgb(51, 0, 170); }
.cm-s-inner .cm-bracket { color: rgb(153, 153, 119); }
.cm-s-inner .cm-tag { color: rgb(17, 119, 0); }
.cm-s-inner .cm-attribute { color: rgb(0, 0, 204); }
.cm-s-inner .cm-header, .cm-s-inner.cm-header { color: rgb(0, 0, 255); }
.cm-s-inner .cm-quote, .cm-s-inner.cm-quote { color: rgb(0, 153, 0); }
.cm-s-inner .cm-hr, .cm-s-inner.cm-hr { color: rgb(153, 153, 153); }
.cm-s-inner .cm-link, .cm-s-inner.cm-link { color: rgb(0, 0, 204); }
.cm-negative { color: rgb(221, 68, 68); }
.cm-positive { color: rgb(34, 153, 34); }
.cm-header, .cm-strong { font-weight: 700; }
.cm-del { text-decoration: line-through; }
.cm-em { font-style: italic; }
.cm-link { text-decoration: underline; }
.cm-error { color: red; }
.cm-invalidchar { color: red; }
.cm-constant { color: rgb(38, 139, 210); }
.cm-defined { color: rgb(181, 137, 0); }
div.CodeMirror span.CodeMirror-matchingbracket { color: rgb(0, 255, 0); }
div.CodeMirror span.CodeMirror-nonmatchingbracket { color: rgb(255, 34, 34); }
.cm-s-inner .CodeMirror-activeline-background { background: inherit; }
.CodeMirror { position: relative; overflow: hidden; }
.CodeMirror-scroll { height: 100%; outline: 0px; position: relative; box-sizing: content-box; background: inherit; }
.CodeMirror-sizer { position: relative; }
.CodeMirror-gutter-filler, .CodeMirror-hscrollbar, .CodeMirror-scrollbar-filler, .CodeMirror-vscrollbar { position: absolute; z-index: 6; display: none; }
.CodeMirror-vscrollbar { right: 0px; top: 0px; overflow: hidden; }
.CodeMirror-hscrollbar { bottom: 0px; left: 0px; overflow: hidden; }
.CodeMirror-scrollbar-filler { right: 0px; bottom: 0px; }
.CodeMirror-gutter-filler { left: 0px; bottom: 0px; }
.CodeMirror-gutters { position: absolute; left: 0px; top: 0px; padding-bottom: 30px; z-index: 3; }
.CodeMirror-gutter { white-space: normal; height: 100%; box-sizing: content-box; padding-bottom: 30px; margin-bottom: -32px; display: inline-block; }
.CodeMirror-gutter-wrapper { position: absolute; z-index: 4; background: 0px 0px !important; border: none !important; }
.CodeMirror-gutter-background { position: absolute; top: 0px; bottom: 0px; z-index: 4; }
.CodeMirror-gutter-elt { position: absolute; cursor: default; z-index: 4; }
.CodeMirror-lines { cursor: text; }
.CodeMirror pre { border-radius: 0px; border-width: 0px; background: 0px 0px; font-family: inherit; font-size: inherit; margin: 0px; white-space: pre; word-wrap: normal; color: inherit; z-index: 2; position: relative; overflow: visible; }
.CodeMirror-wrap pre { word-wrap: break-word; white-space: pre-wrap; word-break: normal; }
.CodeMirror-code pre { border-right: 30px solid transparent; width: fit-content; }
.CodeMirror-wrap .CodeMirror-code pre { border-right: none; width: auto; }
.CodeMirror-linebackground { position: absolute; left: 0px; right: 0px; top: 0px; bottom: 0px; z-index: 0; }
.CodeMirror-linewidget { position: relative; z-index: 2; overflow: auto; }
.CodeMirror-wrap .CodeMirror-scroll { overflow-x: hidden; }
.CodeMirror-measure { position: absolute; width: 100%; height: 0px; overflow: hidden; visibility: hidden; }
.CodeMirror-measure pre { position: static; }
.CodeMirror div.CodeMirror-cursor { position: absolute; visibility: hidden; border-right: none; width: 0px; }
.CodeMirror div.CodeMirror-cursor { visibility: hidden; }
.CodeMirror-focused div.CodeMirror-cursor { visibility: inherit; }
.cm-searching { background: rgba(255, 255, 0, 0.4); }
@media print {
  .CodeMirror div.CodeMirror-cursor { visibility: hidden; }
}


:root { --side-bar-bg-color: #fff; --control-text-color: #777; }
@font-face { font-family: "Roboto Mono"; font-style: normal; font-weight: 400; src: local("Roboto Mono"), local("RobotoMono-Regular"), url("vue/L0x5DF4xlVMF-BfR8bXMIjhGq3-cXbKDO1w.woff2") format("woff2"); unicode-range: U+460-52F, U+1C80-1C88, U+20B4, U+2DE0-2DFF, U+A640-A69F, U+FE2E-FE2F; }
@font-face { font-family: "Roboto Mono"; font-style: normal; font-weight: 400; src: local("Roboto Mono"), local("RobotoMono-Regular"), url("vue/L0x5DF4xlVMF-BfR8bXMIjhPq3-cXbKDO1w.woff2") format("woff2"); unicode-range: U+400-45F, U+490-491, U+4B0-4B1, U+2116; }
@font-face { font-family: "Roboto Mono"; font-style: normal; font-weight: 400; src: local("Roboto Mono"), local("RobotoMono-Regular"), url("vue/L0x5DF4xlVMF-BfR8bXMIjhHq3-cXbKDO1w.woff2") format("woff2"); unicode-range: U+1F00-1FFF; }
@font-face { font-family: "Roboto Mono"; font-style: normal; font-weight: 400; src: local("Roboto Mono"), local("RobotoMono-Regular"), url("vue/L0x5DF4xlVMF-BfR8bXMIjhIq3-cXbKDO1w.woff2") format("woff2"); unicode-range: U+370-3FF; }
@font-face { font-family: "Roboto Mono"; font-style: normal; font-weight: 400; src: local("Roboto Mono"), local("RobotoMono-Regular"), url("vue/L0x5DF4xlVMF-BfR8bXMIjhEq3-cXbKDO1w.woff2") format("woff2"); unicode-range: U+102-103, U+110-111, U+1EA0-1EF9, U+20AB; }
@font-face { font-family: "Roboto Mono"; font-style: normal; font-weight: 400; src: local("Roboto Mono"), local("RobotoMono-Regular"), url("vue/L0x5DF4xlVMF-BfR8bXMIjhFq3-cXbKDO1w.woff2") format("woff2"); unicode-range: U+100-24F, U+259, U+1E00-1EFF, U+2020, U+20A0-20AB, U+20AD-20CF, U+2113, U+2C60-2C7F, U+A720-A7FF; }
@font-face { font-family: "Roboto Mono"; font-style: normal; font-weight: 400; src: local("Roboto Mono"), local("RobotoMono-Regular"), url("vue/L0x5DF4xlVMF-BfR8bXMIjhLq3-cXbKD.woff2") format("woff2"); unicode-range: U+0-FF, U+131, U+152-153, U+2BB-2BC, U+2C6, U+2DA, U+2DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD; }
@font-face { font-family: "Source Sans Pro"; font-style: normal; font-weight: 300; src: local("Source Sans Pro Light"), local("SourceSansPro-Light"), url("vue/6xKydSBYKcSV-LCoeQqfX1RYOo3ik4zwmhduz8A.woff2") format("woff2"); unicode-range: U+460-52F, U+1C80-1C88, U+20B4, U+2DE0-2DFF, U+A640-A69F, U+FE2E-FE2F; }
@font-face { font-family: "Source Sans Pro"; font-style: normal; font-weight: 300; src: local("Source Sans Pro Light"), local("SourceSansPro-Light"), url("vue/6xKydSBYKcSV-LCoeQqfX1RYOo3ik4zwkxduz8A.woff2") format("woff2"); unicode-range: U+400-45F, U+490-491, U+4B0-4B1, U+2116; }
@font-face { font-family: "Source Sans Pro"; font-style: normal; font-weight: 300; src: local("Source Sans Pro Light"), local("SourceSansPro-Light"), url("vue/6xKydSBYKcSV-LCoeQqfX1RYOo3ik4zwmxduz8A.woff2") format("woff2"); unicode-range: U+1F00-1FFF; }
@font-face { font-family: "Source Sans Pro"; font-style: normal; font-weight: 300; src: local("Source Sans Pro Light"), local("SourceSansPro-Light"), url("vue/6xKydSBYKcSV-LCoeQqfX1RYOo3ik4zwlBduz8A.woff2") format("woff2"); unicode-range: U+370-3FF; }
@font-face { font-family: "Source Sans Pro"; font-style: normal; font-weight: 300; src: local("Source Sans Pro Light"), local("SourceSansPro-Light"), url("vue/6xKydSBYKcSV-LCoeQqfX1RYOo3ik4zwmBduz8A.woff2") format("woff2"); unicode-range: U+102-103, U+110-111, U+1EA0-1EF9, U+20AB; }
@font-face { font-family: "Source Sans Pro"; font-style: normal; font-weight: 300; src: local("Source Sans Pro Light"), local("SourceSansPro-Light"), url("vue/6xKydSBYKcSV-LCoeQqfX1RYOo3ik4zwmRduz8A.woff2") format("woff2"); unicode-range: U+100-24F, U+259, U+1E00-1EFF, U+2020, U+20A0-20AB, U+20AD-20CF, U+2113, U+2C60-2C7F, U+A720-A7FF; }
@font-face { font-family: "Source Sans Pro"; font-style: normal; font-weight: 300; src: local("Source Sans Pro Light"), local("SourceSansPro-Light"), url("vue/6xKydSBYKcSV-LCoeQqfX1RYOo3ik4zwlxdu.woff2") format("woff2"); unicode-range: U+0-FF, U+131, U+152-153, U+2BB-2BC, U+2C6, U+2DA, U+2DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD; }
@font-face { font-family: "Source Sans Pro"; font-style: normal; font-weight: 400; src: local("Source Sans Pro Regular"), local("SourceSansPro-Regular"), url("vue/6xK3dSBYKcSV-LCoeQqfX1RYOo3qNa7lqDY.woff2") format("woff2"); unicode-range: U+460-52F, U+1C80-1C88, U+20B4, U+2DE0-2DFF, U+A640-A69F, U+FE2E-FE2F; }
@font-face { font-family: "Source Sans Pro"; font-style: normal; font-weight: 400; src: local("Source Sans Pro Regular"), local("SourceSansPro-Regular"), url("vue/6xK3dSBYKcSV-LCoeQqfX1RYOo3qPK7lqDY.woff2") format("woff2"); unicode-range: U+400-45F, U+490-491, U+4B0-4B1, U+2116; }
@font-face { font-family: "Source Sans Pro"; font-style: normal; font-weight: 400; src: local("Source Sans Pro Regular"), local("SourceSansPro-Regular"), url("vue/6xK3dSBYKcSV-LCoeQqfX1RYOo3qNK7lqDY.woff2") format("woff2"); unicode-range: U+1F00-1FFF; }
@font-face { font-family: "Source Sans Pro"; font-style: normal; font-weight: 400; src: local("Source Sans Pro Regular"), local("SourceSansPro-Regular"), url("vue/6xK3dSBYKcSV-LCoeQqfX1RYOo3qO67lqDY.woff2") format("woff2"); unicode-range: U+370-3FF; }
@font-face { font-family: "Source Sans Pro"; font-style: normal; font-weight: 400; src: local("Source Sans Pro Regular"), local("SourceSansPro-Regular"), url("vue/6xK3dSBYKcSV-LCoeQqfX1RYOo3qN67lqDY.woff2") format("woff2"); unicode-range: U+102-103, U+110-111, U+1EA0-1EF9, U+20AB; }
@font-face { font-family: "Source Sans Pro"; font-style: normal; font-weight: 400; src: local("Source Sans Pro Regular"), local("SourceSansPro-Regular"), url("vue/6xK3dSBYKcSV-LCoeQqfX1RYOo3qNq7lqDY.woff2") format("woff2"); unicode-range: U+100-24F, U+259, U+1E00-1EFF, U+2020, U+20A0-20AB, U+20AD-20CF, U+2113, U+2C60-2C7F, U+A720-A7FF; }
@font-face { font-family: "Source Sans Pro"; font-style: normal; font-weight: 400; src: local("Source Sans Pro Regular"), local("SourceSansPro-Regular"), url("vue/6xK3dSBYKcSV-LCoeQqfX1RYOo3qOK7l.woff2") format("woff2"); unicode-range: U+0-FF, U+131, U+152-153, U+2BB-2BC, U+2C6, U+2DA, U+2DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD; }
@font-face { font-family: "Source Sans Pro"; font-style: normal; font-weight: 600; src: local("Source Sans Pro SemiBold"), local("SourceSansPro-SemiBold"), url("vue/6xKydSBYKcSV-LCoeQqfX1RYOo3i54rwmhduz8A.woff2") format("woff2"); unicode-range: U+460-52F, U+1C80-1C88, U+20B4, U+2DE0-2DFF, U+A640-A69F, U+FE2E-FE2F; }
@font-face { font-family: "Source Sans Pro"; font-style: normal; font-weight: 600; src: local("Source Sans Pro SemiBold"), local("SourceSansPro-SemiBold"), url("vue/6xKydSBYKcSV-LCoeQqfX1RYOo3i54rwkxduz8A.woff2") format("woff2"); unicode-range: U+400-45F, U+490-491, U+4B0-4B1, U+2116; }
@font-face { font-family: "Source Sans Pro"; font-style: normal; font-weight: 600; src: local("Source Sans Pro SemiBold"), local("SourceSansPro-SemiBold"), url("vue/6xKydSBYKcSV-LCoeQqfX1RYOo3i54rwmxduz8A.woff2") format("woff2"); unicode-range: U+1F00-1FFF; }
@font-face { font-family: "Source Sans Pro"; font-style: normal; font-weight: 600; src: local("Source Sans Pro SemiBold"), local("SourceSansPro-SemiBold"), url("vue/6xKydSBYKcSV-LCoeQqfX1RYOo3i54rwlBduz8A.woff2") format("woff2"); unicode-range: U+370-3FF; }
@font-face { font-family: "Source Sans Pro"; font-style: normal; font-weight: 600; src: local("Source Sans Pro SemiBold"), local("SourceSansPro-SemiBold"), url("vue/6xKydSBYKcSV-LCoeQqfX1RYOo3i54rwmBduz8A.woff2") format("woff2"); unicode-range: U+102-103, U+110-111, U+1EA0-1EF9, U+20AB; }
@font-face { font-family: "Source Sans Pro"; font-style: normal; font-weight: 600; src: local("Source Sans Pro SemiBold"), local("SourceSansPro-SemiBold"), url("vue/6xKydSBYKcSV-LCoeQqfX1RYOo3i54rwmRduz8A.woff2") format("woff2"); unicode-range: U+100-24F, U+259, U+1E00-1EFF, U+2020, U+20A0-20AB, U+20AD-20CF, U+2113, U+2C60-2C7F, U+A720-A7FF; }
@font-face { font-family: "Source Sans Pro"; font-style: normal; font-weight: 600; src: local("Source Sans Pro SemiBold"), local("SourceSansPro-SemiBold"), url("vue/6xKydSBYKcSV-LCoeQqfX1RYOo3i54rwlxdu.woff2") format("woff2"); unicode-range: U+0-FF, U+131, U+152-153, U+2BB-2BC, U+2C6, U+2DA, U+2DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD; }
html { font-size: 16px; }
body { color: rgb(52, 73, 94); -webkit-font-smoothing: antialiased; line-height: 1.6rem; letter-spacing: 0px; margin: 0px; overflow-x: hidden; font-family: "Source Sans Pro", "Helvetica Neue", Arial, sans-serif !important; }
#write { max-width: 860px; margin: 0px auto; padding: 20px 30px 100px; }
#write p { line-height: 1.6rem; word-spacing: 0.05rem; }
#write ol li { padding-left: 0.5rem; }
#write > ul:first-child, #write > ol:first-child { margin-top: 30px; }
body > :first-child { margin-top: 0px !important; }
body > :last-child { margin-bottom: 0px !important; }
a { color: rgb(66, 185, 131); font-weight: 600; padding: 0px 2px; text-decoration: none; }
h1, h2, h3, h4, h5, h6 { position: relative; margin-top: 1rem; margin-bottom: 1rem; font-weight: bold; line-height: 1.4; cursor: text; }
h1:hover a.anchor, h2:hover a.anchor, h3:hover a.anchor, h4:hover a.anchor, h5:hover a.anchor, h6:hover a.anchor { text-decoration: none; }
h1 tt, h1 code { font-size: inherit; }
h2 tt, h2 code { font-size: inherit; }
h3 tt, h3 code { font-size: inherit; }
h4 tt, h4 code { font-size: inherit; }
h5 tt, h5 code { font-size: inherit; }
h6 tt, h6 code { font-size: inherit; }
h2 a, h3 a { color: rgb(52, 73, 94); }
h3 a::before { content: "#"; color: rgb(66, 185, 131); position: absolute; left: -0.7em; margin-top: -0.05em; padding-right: 0.5em; font-size: 1.2em; line-height: 1; font-weight: bold; }
h1 { padding-bottom: 0.4rem; font-size: 2.2rem; line-height: 1.3; }
h2 { font-size: 1.75rem; line-height: 1.225; margin: 35px 0px 15px; padding-bottom: 0.5em; border-bottom: 1px solid rgb(221, 221, 221); }
h3 { font-size: 1.4rem; line-height: 1.43; margin: 20px 0px 7px; }
h4 { font-size: 1.2rem; }
h5 { font-size: 1rem; }
h6 { font-size: 1rem; color: rgb(119, 119, 119); }
p, blockquote, ul, ol, dl, table { margin: 0.8em 0px; }
li > ol, li > ul { margin: 0px; }
hr { height: 2px; padding: 0px; margin: 16px 0px; background-color: rgb(231, 231, 231); border: 0px none; overflow: hidden; box-sizing: content-box; }
body > h2:first-child { margin-top: 0px; padding-top: 0px; }
body > h1:first-child { margin-top: 0px; padding-top: 0px; }
body > h1:first-child + h2 { margin-top: 0px; padding-top: 0px; }
body > h3:first-child, body > h4:first-child, body > h5:first-child, body > h6:first-child { margin-top: 0px; padding-top: 0px; }
a:first-child h1, a:first-child h2, a:first-child h3, a:first-child h4, a:first-child h5, a:first-child h6 { margin-top: 0px; padding-top: 0px; }
h1 p, h2 p, h3 p, h4 p, h5 p, h6 p { margin-top: 0px; }
li p.first { display: inline-block; }
ul, ol { padding-left: 30px; }
ul:first-child, ol:first-child { margin-top: 0px; }
ul:last-child, ol:last-child { margin-bottom: 0px; }
blockquote { border-left: 4px solid rgb(66, 185, 131); padding: 10px 0px 10px 15px; color: rgb(119, 119, 119); background-color: rgba(66, 185, 131, 0.1); }
table { padding: 0px; word-break: initial; }
table tr { border-top: 1px solid rgb(223, 226, 229); margin: 0px; padding: 0px; }
table tr:nth-child(2n), thead { background-color: rgb(250, 250, 250); }
table tr th { font-weight: bold; border-width: 1px 1px 0px; border-top-style: solid; border-right-style: solid; border-left-style: solid; border-top-color: rgb(223, 226, 229); border-right-color: rgb(223, 226, 229); border-left-color: rgb(223, 226, 229); border-image: initial; border-bottom-style: initial; border-bottom-color: initial; text-align: left; margin: 0px; padding: 6px 13px; }
table tr td { border: 1px solid rgb(223, 226, 229); text-align: left; margin: 0px; padding: 6px 13px; }
table tr th:first-child, table tr td:first-child { margin-top: 0px; }
table tr th:last-child, table tr td:last-child { margin-bottom: 0px; }
#write strong { padding: 0px 1px; }
#write em { padding: 0px 5px 0px 2px; }
#write table thead th { background-color: rgb(242, 242, 242); }
#write .CodeMirror-gutters { border-right: none; }
#write .md-fences { border: 1px solid rgb(244, 244, 244); -webkit-font-smoothing: initial; line-height: 1.43rem; border-radius: 2px; font-size: 0.85rem; word-wrap: normal; margin: 0.8rem 0px !important; padding: 0.3rem 0rem !important; background-color: rgb(248, 248, 248) !important; font-family: "Roboto Mono", "Source Sans Pro", Monaco, courier, monospace !important; }
#write .CodeMirror-wrap .CodeMirror-code pre { padding-left: 12px; }
#write code, tt { margin: 0px 2px; padding: 2px 4px; border-radius: 2px; font-size: 0.92rem; color: rgb(233, 105, 0); background-color: rgb(248, 248, 248); font-family: "Source Sans Pro", "Roboto Mono", Monaco, courier, monospace !important; }
#write .md-footnote { background-color: rgb(248, 248, 248); color: rgb(233, 105, 0); }
#write mark { background-color: rgb(235, 255, 235); border-radius: 2px; padding: 2px 4px; margin: 0px 2px; color: rgb(34, 34, 34); font-weight: 500; }
#write del { padding: 1px 2px; }
.cm-s-inner .cm-link, .cm-s-inner.cm-link { color: rgb(34, 162, 201); }
.cm-s-inner .cm-string { color: rgb(34, 162, 201); }
.md-task-list-item > input { margin-left: -1.3em; }
@media screen and (min-width: 914px) {
}
@media print {
  html { font-size: 13px; }
  table, pre { break-inside: avoid; }
  pre { word-wrap: break-word; }
}
.md-fences { background-color: rgb(248, 248, 248); }
#write pre.md-meta-block { padding: 1rem; font-size: 85%; line-height: 1.45; background-color: rgb(247, 247, 247); border: 0px; border-radius: 3px; color: rgb(119, 119, 119); margin-top: 0px !important; }
.mathjax-block > .code-tooltip { bottom: 0.375rem; }
#write > h3.md-focus::before { left: -1.5625rem; top: 0.375rem; }
#write > h4.md-focus::before { left: -1.5625rem; top: 0.285714rem; }
#write > h5.md-focus::before { left: -1.5625rem; top: 0.285714rem; }
#write > h6.md-focus::before { left: -1.5625rem; top: 0.285714rem; }
.md-image > .md-meta { border-radius: 3px; font-family: Consolas, "Liberation Mono", Courier, monospace; padding: 2px 0px 0px 4px; font-size: 0.9em; color: inherit; }
.md-tag { color: inherit; }
.md-toc { margin-top: 20px; padding-bottom: 20px; }
.sidebar-tabs { border-bottom: none; }
#typora-quick-open { border: 1px solid rgb(221, 221, 221); background-color: rgb(248, 248, 248); }
#typora-quick-open-item { background-color: rgb(250, 250, 250); border-color: rgb(254, 254, 254) rgb(229, 229, 229) rgb(229, 229, 229) rgb(238, 238, 238); border-style: solid; border-width: 1px; }
#md-notification::before { top: 10px; }
.on-focus-mode blockquote { border-left-color: rgba(85, 85, 85, 0.12); }
header, .context-menu, .megamenu-content, footer { font-family: "Segoe UI", Arial, sans-serif; }
.file-node-content:hover .file-node-icon, .file-node-content:hover .file-node-open-state { visibility: visible; }
.mac-seamless-mode #typora-sidebar { background-color: var(--side-bar-bg-color); }
.md-lang { color: rgb(180, 101, 77); }
.html-for-mac .context-menu { --item-hover-bg-color: #E6F0FE; }





 .typora-export p, .typora-export .footnote-line {white-space: normal;} 
</style>
</head>
<body class='typora-export os-windows' >
<div  id='write'  class = 'is-node'><h1><a name='header-n2' class='md-header-anchor '></a>6264. friend-斐波那契</h1><p> </p><hr /><p>Description</p><p>求f12+f22+f32+....+fn2， 其中 fi 代表斐波那契数列的第 i 项。 (f0=0,f1=1)当然结果会很大，请将它对 109+7取模。</p><p>输入格式</p><p>一行一个数 n.</p><p>输出格式</p><p>一行一个数，代表答案。</p><p>样例</p><p>样例输入</p><blockquote><p>6</p></blockquote><p>样例输出</p><blockquote><p>104</p></blockquote><p>数据范围与提示</p><p>对于30%的数据：n≤105。</p><p>对于另外20%的数据: 1000000∣n （即n是1000000的倍数），且n≤5∗109。</p><p>对于100%的数据：n≤1018。</p><p> </p><hr /><p> </p><p>解体思路：首先需要搞清楚斐波那契数列求和蕴含的规律，先找到它的递归形式：</p><p><img src='file:///C:/Users/LHL/AppData/Local/Temp/msohtmlclip1/01/clip_image002.jpg' alt='img' referrerPolicy='no-referrer' /></p><p>则其各项相加的平方和为：</p><p><img src='file:///C:/Users/LHL/AppData/Local/Temp/msohtmlclip1/01/clip_image004.jpg' alt='img' referrerPolicy='no-referrer' /></p><p>以几何的手段证明：12+12+22+32+52+82=8×13</p><p><img src='file:///C:/Users/LHL/AppData/Local/Temp/msohtmlclip1/01/clip_image006.jpg' alt='img' referrerPolicy='no-referrer' /></p><p>设斐波那契数列的各项为正方形边长，则所求平方和就是算正方形的面积，但是求幂运算需要循环逐个累乘，其复杂度为O(n)，这在很多时候是不够的，所以我们需要用快速幂——反复平方法来加速幂运算的过程，要想办法减少步骤，把其中的某一部分合成一步来进行。</p><p>比如，如果n能被2整除，那我们可以先计算一半，得到a^(n/2)的值，再把这个值平方得出结果。这样做虽然有优化，但优化的程度很小，仍是线性的复杂度。</p><p>再比如，如果我们能找到2k = n，那我们就能把原来的运算优化成((((a2) 2) 2)...)，只需要k次运算就可以完成，效率大大提升。可惜的是，这种条件显然太苛刻了，适用范围很小。不过这给了我们一种思路，虽然我们很难找到2k == n，但我们能够找到2k1 + 2k2 + 2k3 +......+ 2km =n。这样，我们可以通过层层递推，在很短的时间内求出各个项的值。可是又有新的问题出现了，我们并不清楚k1、k2...km具体的值是多少，对于不同的n，有不同分法，有没有一种规则能把这些分法统一起来。</p><p>我们都学习过进制与进制的转换，知道一个b进制数的值可以表示为各个数位的值与权值之积的总和。比如，2进制数1001，它的值可以表示为10进制的1<em>23 + 0</em>22 + 0<em>21 + 1</em>20，即9。这完美地符合了上面的要求。可以通过2进制来把n转化成2^km的序列之和，而2进制中第i位（从右边开始计数，值为1或是0）则标记了对应的2(i - 1)是否存在于序列之中。譬如，13为二进制的1101，他可以表示为23 + 22 + 20，其中由于第二位为0，21项被舍去。</p><p>如此一来，我们只需要计算a、a2、a4、a8......的值（这个序列中的项不一定都存在）并把它们乘起来即可完成整个幂运算。借助位运算的操作，可以很方便地实现这一算法，其复杂度为O(logn)。</p><p>套用以下模板：</p><pre spellcheck="false" class="md-fences md-end-block ty-contain-cm modeLoaded" lang="c++" style="break-inside: unset;"><div class="CodeMirror cm-s-inner CodeMirror-wrap" lang="c++"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 0px; left: 12px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><span><span>​</span>x</span></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation" style=""><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">typedef</span> <span class="cm-variable-3">long</span> <span class="cm-variable-3">long</span> <span class="cm-variable">ll</span>;</span></pre></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span cm-text="">​</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable">ll</span> <span class="cm-def">quick_pow</span>(<span class="cm-variable">ll</span> <span class="cm-variable">a</span>, <span class="cm-variable">ll</span> <span class="cm-variable">n</span>)<span class="cm-comment">//a^n</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span cm-text="">​</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;">{</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span cm-text="">​</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; <span class="cm-variable">ll</span> <span class="cm-variable">re</span> <span class="cm-operator">=</span> <span class="cm-number">1</span>;</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span cm-text="">​</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; <span class="cm-keyword">while</span>(<span class="cm-variable">n</span> <span class="cm-operator">!=</span> <span class="cm-number">0</span>)</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span cm-text="">​</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; {</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span cm-text="">​</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; <span class="cm-keyword">if</span>(<span class="cm-variable">n</span> <span class="cm-operator">&amp;</span> <span class="cm-number">1</span>)<span class="cm-comment">//判断n的最后一位是1还是0</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;<span class="cm-variable">re</span> <span class="cm-operator">*=</span> <span class="cm-variable">a</span>;</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; <span class="cm-variable">a</span> <span class="cm-operator">=</span> (<span class="cm-variable">a</span> <span class="cm-operator">*</span> <span class="cm-variable">a</span>);<span class="cm-comment">//将a平方，即把a^(2^i)变为a^(2^(i + 1))</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp;<span class="cm-variable">n</span> <span class="cm-operator">&gt;&gt;=</span> <span class="cm-number">1</span>;<span class="cm-comment">//n右移一位，舍去n的最后一位</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp;  }</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span cm-text="">​</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp;<span class="cm-keyword">return</span> <span class="cm-variable">re</span>;</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span cm-text="">​</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;">}</span></pre></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 476px;"></div><div class="CodeMirror-gutters" style="display: none; height: 476px;"></div></div></div></pre><p>本题需要取模，直接在每一步运算中对a和re取模即可。</p><p> AC代码：</p><pre spellcheck="false" class="md-fences md-end-block ty-contain-cm modeLoaded" lang="c" style="break-inside: unset;"><div class="CodeMirror cm-s-inner CodeMirror-wrap" lang="c"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 0px; left: 12px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation" style=""><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-meta">#include&lt;string.h&gt;</span></span></pre></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-meta">#include&lt;stdio.h&gt;</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-meta">#define ll long long</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-meta">#define MOD 1000000007</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">struct</span> <span class="cm-def">nobe</span>{ <span class="cm-variable">ll</span> <span class="cm-variable">a</span>[<span class="cm-number">2</span>][<span class="cm-number">2</span>];};</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable">ll</span> <span class="cm-variable">n</span>;</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable">ll</span> <span class="cm-variable">sum</span>;</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable">nobe</span> <span class="cm-def">mut</span>(<span class="cm-variable">nobe</span> <span class="cm-variable">x</span>,<span class="cm-variable">nobe</span> <span class="cm-variable">y</span>){</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable">nobe</span> <span class="cm-variable">res</span>;</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable">memset</span>(<span class="cm-variable">res</span>.<span class="cm-variable">a</span>,<span class="cm-number">0</span>,<span class="cm-keyword">sizeof</span>(<span class="cm-variable">res</span>.<span class="cm-variable">a</span>));</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">for</span>(<span class="cm-variable">ll</span> <span class="cm-variable">i</span><span class="cm-operator">=</span><span class="cm-number">0</span>;<span class="cm-variable">i</span><span class="cm-operator">&lt;</span><span class="cm-number">2</span>;<span class="cm-variable">i</span><span class="cm-operator">++</span>)</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp;<span class="cm-keyword">for</span>( <span class="cm-variable-3">int</span> <span class="cm-variable">j</span><span class="cm-operator">=</span><span class="cm-number">0</span>;<span class="cm-variable">j</span><span class="cm-operator">&lt;</span><span class="cm-number">2</span>;<span class="cm-variable">j</span><span class="cm-operator">++</span>)</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp;<span class="cm-keyword">for</span>( <span class="cm-variable-3">int</span> <span class="cm-variable">k</span><span class="cm-operator">=</span><span class="cm-number">0</span>;<span class="cm-variable">k</span><span class="cm-operator">&lt;</span><span class="cm-number">2</span>;<span class="cm-variable">k</span><span class="cm-operator">++</span>)</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp;<span class="cm-variable">res</span>.<span class="cm-variable">a</span>[<span class="cm-variable">i</span>][<span class="cm-variable">j</span>]<span class="cm-operator">=</span>(<span class="cm-variable">res</span>.<span class="cm-variable">a</span>[<span class="cm-variable">i</span>][<span class="cm-variable">j</span>]<span class="cm-operator">+</span><span class="cm-variable">x</span>.<span class="cm-variable">a</span>[<span class="cm-variable">i</span>][<span class="cm-variable">k</span>]<span class="cm-operator">*</span><span class="cm-variable">y</span>.<span class="cm-variable">a</span>[<span class="cm-variable">k</span>][<span class="cm-variable">j</span>])<span class="cm-operator">%</span><span class="cm-variable">MOD</span>;</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">return</span> <span class="cm-variable">res</span>;}</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable-3">void</span> <span class="cm-def">quick</span>(<span class="cm-variable">ll</span> <span class="cm-variable">n</span>){</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp;<span class="cm-variable">nobe</span> <span class="cm-variable">c</span>,<span class="cm-variable">res</span>;</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp;<span class="cm-variable">c</span>.<span class="cm-variable">a</span>[<span class="cm-number">0</span>][<span class="cm-number">0</span>]<span class="cm-operator">=</span><span class="cm-number">1</span>;</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp;<span class="cm-variable">c</span>.<span class="cm-variable">a</span>[<span class="cm-number">0</span>][<span class="cm-number">1</span>]<span class="cm-operator">=</span><span class="cm-number">1</span>;</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp;<span class="cm-variable">c</span>.<span class="cm-variable">a</span>[<span class="cm-number">1</span>][<span class="cm-number">0</span>]<span class="cm-operator">=</span><span class="cm-number">1</span>;</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp;<span class="cm-variable">c</span>.<span class="cm-variable">a</span>[<span class="cm-number">1</span>][<span class="cm-number">1</span>]<span class="cm-operator">=</span><span class="cm-number">0</span>;</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;<span class="cm-variable">memset</span>(<span class="cm-variable">res</span>.<span class="cm-variable">a</span>,<span class="cm-number">0</span>,<span class="cm-keyword">sizeof</span>(<span class="cm-variable">res</span>.<span class="cm-variable">a</span>));</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;<span class="cm-keyword">for</span>(<span class="cm-variable-3">int</span> <span class="cm-variable">i</span><span class="cm-operator">=</span><span class="cm-number">0</span>;<span class="cm-variable">i</span><span class="cm-operator">&lt;</span><span class="cm-number">2</span>;<span class="cm-variable">i</span><span class="cm-operator">++</span>)</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;<span class="cm-variable">res</span>.<span class="cm-variable">a</span>[<span class="cm-variable">i</span>][<span class="cm-variable">i</span>]<span class="cm-operator">=</span><span class="cm-number">1</span>;</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;<span class="cm-keyword">while</span>(<span class="cm-variable">n</span>)</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp;  { &nbsp;<span class="cm-variable">cont</span><span class="cm-operator">++</span>;</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;<span class="cm-keyword">if</span>(<span class="cm-variable">n</span><span class="cm-operator">&amp;</span><span class="cm-number">1</span>)<span class="cm-variable">res</span><span class="cm-operator">=</span><span class="cm-variable">mut</span>(<span class="cm-variable">res</span>,<span class="cm-variable">c</span>);</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;<span class="cm-variable">c</span><span class="cm-operator">=</span><span class="cm-variable">mut</span>(<span class="cm-variable">c</span>,<span class="cm-variable">c</span>);</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;<span class="cm-variable">n</span><span class="cm-operator">=</span><span class="cm-variable">n</span><span class="cm-operator">&gt;&gt;</span><span class="cm-number">1</span>; &nbsp;  }</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable">printf</span>(<span class="cm-string">"%ld\n"</span>,((<span class="cm-variable">res</span>.<span class="cm-variable">a</span>[<span class="cm-number">0</span>][<span class="cm-number">1</span>]<span class="cm-operator">%</span><span class="cm-variable">MOD</span>)<span class="cm-operator">*</span>(<span class="cm-variable">res</span>.<span class="cm-variable">a</span>[<span class="cm-number">0</span>][<span class="cm-number">1</span>]<span class="cm-operator">%</span><span class="cm-variable">MOD</span><span class="cm-operator">+</span><span class="cm-variable">res</span>.<span class="cm-variable">a</span>[<span class="cm-number">1</span>][<span class="cm-number">1</span>]<span class="cm-operator">%</span><span class="cm-variable">MOD</span>))<span class="cm-operator">%</span><span class="cm-variable">MOD</span>);</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;">}</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable-3">int</span> <span class="cm-def">main</span>(){</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp;<span class="cm-keyword">while</span>(<span class="cm-variable">scanf</span>(<span class="cm-string">"%ld"</span>,<span class="cm-operator">&amp;</span><span class="cm-variable">n</span>)<span class="cm-operator">!=</span><span class="cm-variable">EOF</span>)</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp;  { &nbsp; &nbsp; <span class="cm-variable">quick</span>(<span class="cm-variable">n</span>);</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp;  }</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span cm-text="">​</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">return</span> <span class="cm-number">0</span>;}</span></pre></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 839px;"></div><div class="CodeMirror-gutters" style="display: none; height: 839px;"></div></div></div></pre><p>&nbsp;</p></div>
</body>
</html>















```c
#include<string.h>
#include<stdio.h>
#define ll long long
#define MOD 1000000007
struct nobe{ ll a[2][2];};
ll n;
ll sum;
nobe mut(nobe x,nobe y){
nobe res;
memset(res.a,0,sizeof(res.a));
for(ll i=0;i<2;i++)
    for( int j=0;j<2;j++)
    for( int k=0;k<2;k++)
      res.a[i][j]=(res.a[i][j]+x.a[i][k]*y.a[k][j])%MOD;
return res;}
void quick(ll n){
      nobe c,res;
        c.a[0][0]=1;
        c.a[0][1]=1;
        c.a[1][0]=1;
        c.a[1][1]=0;
          memset(res.a,0,sizeof(res.a));
            for(int i=0;i<2;i++)
                res.a[i][i]=1;
            while(n)
          {  cont++;
            if(n&1)res=mut(res,c);
                      c=mut(c,c);
            n=n>>1;    }
printf("%ld\n",((res.a[0][1]%MOD)*(res.a[0][1]%MOD+res.a[1][1]%MOD))%MOD);
}
int main(){
    while(scanf("%ld",&n)!=EOF)
    {     quick(n);
    }

return 0;}
```

