<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />

<title>00 matplotlib_all_in_one</title>

<script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>



<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.7 (http://getbootstrap.com)
 * Copyright 2011-2016 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}
audio:not([controls]) {
  display: none;
  height: 0;
}
[hidden],
template {
  display: none;
}
a {
  background-color: transparent;
}
a:active,
a:hover {
  outline: 0;
}
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sup {
  top: -0.5em;
}
sub {
  bottom: -0.25em;
}
img {
  border: 0;
}
svg:not(:root) {
  overflow: hidden;
}
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}
button {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}
button[disabled],
html input[disabled] {
  cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
}
input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
  .navbar {
    display: none;
  }
  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }
  .label {
    border: 1px solid #000;
  }
  .table {
    border-collapse: collapse !important;
  }
  .table td,
  .table th {
    background-color: #fff !important;
  }
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
  content: "\20ac";
}
.glyphicon-minus:before {
  content: "\2212";
}
.glyphicon-cloud:before {
  content: "\2601";
}
.glyphicon-envelope:before {
  content: "\2709";
}
.glyphicon-pencil:before {
  content: "\270f";
}
.glyphicon-glass:before {
  content: "\e001";
}
.glyphicon-music:before {
  content: "\e002";
}
.glyphicon-search:before {
  content: "\e003";
}
.glyphicon-heart:before {
  content: "\e005";
}
.glyphicon-star:before {
  content: "\e006";
}
.glyphicon-star-empty:before {
  content: "\e007";
}
.glyphicon-user:before {
  content: "\e008";
}
.glyphicon-film:before {
  content: "\e009";
}
.glyphicon-th-large:before {
  content: "\e010";
}
.glyphicon-th:before {
  content: "\e011";
}
.glyphicon-th-list:before {
  content: "\e012";
}
.glyphicon-ok:before {
  content: "\e013";
}
.glyphicon-remove:before {
  content: "\e014";
}
.glyphicon-zoom-in:before {
  content: "\e015";
}
.glyphicon-zoom-out:before {
  content: "\e016";
}
.glyphicon-off:before {
  content: "\e017";
}
.glyphicon-signal:before {
  content: "\e018";
}
.glyphicon-cog:before {
  content: "\e019";
}
.glyphicon-trash:before {
  content: "\e020";
}
.glyphicon-home:before {
  content: "\e021";
}
.glyphicon-file:before {
  content: "\e022";
}
.glyphicon-time:before {
  content: "\e023";
}
.glyphicon-road:before {
  content: "\e024";
}
.glyphicon-download-alt:before {
  content: "\e025";
}
.glyphicon-download:before {
  content: "\e026";
}
.glyphicon-upload:before {
  content: "\e027";
}
.glyphicon-inbox:before {
  content: "\e028";
}
.glyphicon-play-circle:before {
  content: "\e029";
}
.glyphicon-repeat:before {
  content: "\e030";
}
.glyphicon-refresh:before {
  content: "\e031";
}
.glyphicon-list-alt:before {
  content: "\e032";
}
.glyphicon-lock:before {
  content: "\e033";
}
.glyphicon-flag:before {
  content: "\e034";
}
.glyphicon-headphones:before {
  content: "\e035";
}
.glyphicon-volume-off:before {
  content: "\e036";
}
.glyphicon-volume-down:before {
  content: "\e037";
}
.glyphicon-volume-up:before {
  content: "\e038";
}
.glyphicon-qrcode:before {
  content: "\e039";
}
.glyphicon-barcode:before {
  content: "\e040";
}
.glyphicon-tag:before {
  content: "\e041";
}
.glyphicon-tags:before {
  content: "\e042";
}
.glyphicon-book:before {
  content: "\e043";
}
.glyphicon-bookmark:before {
  content: "\e044";
}
.glyphicon-print:before {
  content: "\e045";
}
.glyphicon-camera:before {
  content: "\e046";
}
.glyphicon-font:before {
  content: "\e047";
}
.glyphicon-bold:before {
  content: "\e048";
}
.glyphicon-italic:before {
  content: "\e049";
}
.glyphicon-text-height:before {
  content: "\e050";
}
.glyphicon-text-width:before {
  content: "\e051";
}
.glyphicon-align-left:before {
  content: "\e052";
}
.glyphicon-align-center:before {
  content: "\e053";
}
.glyphicon-align-right:before {
  content: "\e054";
}
.glyphicon-align-justify:before {
  content: "\e055";
}
.glyphicon-list:before {
  content: "\e056";
}
.glyphicon-indent-left:before {
  content: "\e057";
}
.glyphicon-indent-right:before {
  content: "\e058";
}
.glyphicon-facetime-video:before {
  content: "\e059";
}
.glyphicon-picture:before {
  content: "\e060";
}
.glyphicon-map-marker:before {
  content: "\e062";
}
.glyphicon-adjust:before {
  content: "\e063";
}
.glyphicon-tint:before {
  content: "\e064";
}
.glyphicon-edit:before {
  content: "\e065";
}
.glyphicon-share:before {
  content: "\e066";
}
.glyphicon-check:before {
  content: "\e067";
}
.glyphicon-move:before {
  content: "\e068";
}
.glyphicon-step-backward:before {
  content: "\e069";
}
.glyphicon-fast-backward:before {
  content: "\e070";
}
.glyphicon-backward:before {
  content: "\e071";
}
.glyphicon-play:before {
  content: "\e072";
}
.glyphicon-pause:before {
  content: "\e073";
}
.glyphicon-stop:before {
  content: "\e074";
}
.glyphicon-forward:before {
  content: "\e075";
}
.glyphicon-fast-forward:before {
  content: "\e076";
}
.glyphicon-step-forward:before {
  content: "\e077";
}
.glyphicon-eject:before {
  content: "\e078";
}
.glyphicon-chevron-left:before {
  content: "\e079";
}
.glyphicon-chevron-right:before {
  content: "\e080";
}
.glyphicon-plus-sign:before {
  content: "\e081";
}
.glyphicon-minus-sign:before {
  content: "\e082";
}
.glyphicon-remove-sign:before {
  content: "\e083";
}
.glyphicon-ok-sign:before {
  content: "\e084";
}
.glyphicon-question-sign:before {
  content: "\e085";
}
.glyphicon-info-sign:before {
  content: "\e086";
}
.glyphicon-screenshot:before {
  content: "\e087";
}
.glyphicon-remove-circle:before {
  content: "\e088";
}
.glyphicon-ok-circle:before {
  content: "\e089";
}
.glyphicon-ban-circle:before {
  content: "\e090";
}
.glyphicon-arrow-left:before {
  content: "\e091";
}
.glyphicon-arrow-right:before {
  content: "\e092";
}
.glyphicon-arrow-up:before {
  content: "\e093";
}
.glyphicon-arrow-down:before {
  content: "\e094";
}
.glyphicon-share-alt:before {
  content: "\e095";
}
.glyphicon-resize-full:before {
  content: "\e096";
}
.glyphicon-resize-small:before {
  content: "\e097";
}
.glyphicon-exclamation-sign:before {
  content: "\e101";
}
.glyphicon-gift:before {
  content: "\e102";
}
.glyphicon-leaf:before {
  content: "\e103";
}
.glyphicon-fire:before {
  content: "\e104";
}
.glyphicon-eye-open:before {
  content: "\e105";
}
.glyphicon-eye-close:before {
  content: "\e106";
}
.glyphicon-warning-sign:before {
  content: "\e107";
}
.glyphicon-plane:before {
  content: "\e108";
}
.glyphicon-calendar:before {
  content: "\e109";
}
.glyphicon-random:before {
  content: "\e110";
}
.glyphicon-comment:before {
  content: "\e111";
}
.glyphicon-magnet:before {
  content: "\e112";
}
.glyphicon-chevron-up:before {
  content: "\e113";
}
.glyphicon-chevron-down:before {
  content: "\e114";
}
.glyphicon-retweet:before {
  content: "\e115";
}
.glyphicon-shopping-cart:before {
  content: "\e116";
}
.glyphicon-folder-close:before {
  content: "\e117";
}
.glyphicon-folder-open:before {
  content: "\e118";
}
.glyphicon-resize-vertical:before {
  content: "\e119";
}
.glyphicon-resize-horizontal:before {
  content: "\e120";
}
.glyphicon-hdd:before {
  content: "\e121";
}
.glyphicon-bullhorn:before {
  content: "\e122";
}
.glyphicon-bell:before {
  content: "\e123";
}
.glyphicon-certificate:before {
  content: "\e124";
}
.glyphicon-thumbs-up:before {
  content: "\e125";
}
.glyphicon-thumbs-down:before {
  content: "\e126";
}
.glyphicon-hand-right:before {
  content: "\e127";
}
.glyphicon-hand-left:before {
  content: "\e128";
}
.glyphicon-hand-up:before {
  content: "\e129";
}
.glyphicon-hand-down:before {
  content: "\e130";
}
.glyphicon-circle-arrow-right:before {
  content: "\e131";
}
.glyphicon-circle-arrow-left:before {
  content: "\e132";
}
.glyphicon-circle-arrow-up:before {
  content: "\e133";
}
.glyphicon-circle-arrow-down:before {
  content: "\e134";
}
.glyphicon-globe:before {
  content: "\e135";
}
.glyphicon-wrench:before {
  content: "\e136";
}
.glyphicon-tasks:before {
  content: "\e137";
}
.glyphicon-filter:before {
  content: "\e138";
}
.glyphicon-briefcase:before {
  content: "\e139";
}
.glyphicon-fullscreen:before {
  content: "\e140";
}
.glyphicon-dashboard:before {
  content: "\e141";
}
.glyphicon-paperclip:before {
  content: "\e142";
}
.glyphicon-heart-empty:before {
  content: "\e143";
}
.glyphicon-link:before {
  content: "\e144";
}
.glyphicon-phone:before {
  content: "\e145";
}
.glyphicon-pushpin:before {
  content: "\e146";
}
.glyphicon-usd:before {
  content: "\e148";
}
.glyphicon-gbp:before {
  content: "\e149";
}
.glyphicon-sort:before {
  content: "\e150";
}
.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}
.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}
.glyphicon-sort-by-order:before {
  content: "\e153";
}
.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}
.glyphicon-sort-by-attributes:before {
  content: "\e155";
}
.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}
.glyphicon-unchecked:before {
  content: "\e157";
}
.glyphicon-expand:before {
  content: "\e158";
}
.glyphicon-collapse-down:before {
  content: "\e159";
}
.glyphicon-collapse-up:before {
  content: "\e160";
}
.glyphicon-log-in:before {
  content: "\e161";
}
.glyphicon-flash:before {
  content: "\e162";
}
.glyphicon-log-out:before {
  content: "\e163";
}
.glyphicon-new-window:before {
  content: "\e164";
}
.glyphicon-record:before {
  content: "\e165";
}
.glyphicon-save:before {
  content: "\e166";
}
.glyphicon-open:before {
  content: "\e167";
}
.glyphicon-saved:before {
  content: "\e168";
}
.glyphicon-import:before {
  content: "\e169";
}
.glyphicon-export:before {
  content: "\e170";
}
.glyphicon-send:before {
  content: "\e171";
}
.glyphicon-floppy-disk:before {
  content: "\e172";
}
.glyphicon-floppy-saved:before {
  content: "\e173";
}
.glyphicon-floppy-remove:before {
  content: "\e174";
}
.glyphicon-floppy-save:before {
  content: "\e175";
}
.glyphicon-floppy-open:before {
  content: "\e176";
}
.glyphicon-credit-card:before {
  content: "\e177";
}
.glyphicon-transfer:before {
  content: "\e178";
}
.glyphicon-cutlery:before {
  content: "\e179";
}
.glyphicon-header:before {
  content: "\e180";
}
.glyphicon-compressed:before {
  content: "\e181";
}
.glyphicon-earphone:before {
  content: "\e182";
}
.glyphicon-phone-alt:before {
  content: "\e183";
}
.glyphicon-tower:before {
  content: "\e184";
}
.glyphicon-stats:before {
  content: "\e185";
}
.glyphicon-sd-video:before {
  content: "\e186";
}
.glyphicon-hd-video:before {
  content: "\e187";
}
.glyphicon-subtitles:before {
  content: "\e188";
}
.glyphicon-sound-stereo:before {
  content: "\e189";
}
.glyphicon-sound-dolby:before {
  content: "\e190";
}
.glyphicon-sound-5-1:before {
  content: "\e191";
}
.glyphicon-sound-6-1:before {
  content: "\e192";
}
.glyphicon-sound-7-1:before {
  content: "\e193";
}
.glyphicon-copyright-mark:before {
  content: "\e194";
}
.glyphicon-registration-mark:before {
  content: "\e195";
}
.glyphicon-cloud-download:before {
  content: "\e197";
}
.glyphicon-cloud-upload:before {
  content: "\e198";
}
.glyphicon-tree-conifer:before {
  content: "\e199";
}
.glyphicon-tree-deciduous:before {
  content: "\e200";
}
.glyphicon-cd:before {
  content: "\e201";
}
.glyphicon-save-file:before {
  content: "\e202";
}
.glyphicon-open-file:before {
  content: "\e203";
}
.glyphicon-level-up:before {
  content: "\e204";
}
.glyphicon-copy:before {
  content: "\e205";
}
.glyphicon-paste:before {
  content: "\e206";
}
.glyphicon-alert:before {
  content: "\e209";
}
.glyphicon-equalizer:before {
  content: "\e210";
}
.glyphicon-king:before {
  content: "\e211";
}
.glyphicon-queen:before {
  content: "\e212";
}
.glyphicon-pawn:before {
  content: "\e213";
}
.glyphicon-bishop:before {
  content: "\e214";
}
.glyphicon-knight:before {
  content: "\e215";
}
.glyphicon-baby-formula:before {
  content: "\e216";
}
.glyphicon-tent:before {
  content: "\26fa";
}
.glyphicon-blackboard:before {
  content: "\e218";
}
.glyphicon-bed:before {
  content: "\e219";
}
.glyphicon-apple:before {
  content: "\f8ff";
}
.glyphicon-erase:before {
  content: "\e221";
}
.glyphicon-hourglass:before {
  content: "\231b";
}
.glyphicon-lamp:before {
  content: "\e223";
}
.glyphicon-duplicate:before {
  content: "\e224";
}
.glyphicon-piggy-bank:before {
  content: "\e225";
}
.glyphicon-scissors:before {
  content: "\e226";
}
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
  content: "\20bd";
}
.glyphicon-scale:before {
  content: "\e230";
}
.glyphicon-ice-lolly:before {
  content: "\e231";
}
.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}
.glyphicon-education:before {
  content: "\e233";
}
.glyphicon-option-horizontal:before {
  content: "\e234";
}
.glyphicon-option-vertical:before {
  content: "\e235";
}
.glyphicon-menu-hamburger:before {
  content: "\e236";
}
.glyphicon-modal-window:before {
  content: "\e237";
}
.glyphicon-oil:before {
  content: "\e238";
}
.glyphicon-grain:before {
  content: "\e239";
}
.glyphicon-sunglasses:before {
  content: "\e240";
}
.glyphicon-text-size:before {
  content: "\e241";
}
.glyphicon-text-color:before {
  content: "\e242";
}
.glyphicon-text-background:before {
  content: "\e243";
}
.glyphicon-object-align-top:before {
  content: "\e244";
}
.glyphicon-object-align-bottom:before {
  content: "\e245";
}
.glyphicon-object-align-horizontal:before {
  content: "\e246";
}
.glyphicon-object-align-left:before {
  content: "\e247";
}
.glyphicon-object-align-vertical:before {
  content: "\e248";
}
.glyphicon-object-align-right:before {
  content: "\e249";
}
.glyphicon-triangle-right:before {
  content: "\e250";
}
.glyphicon-triangle-left:before {
  content: "\e251";
}
.glyphicon-triangle-bottom:before {
  content: "\e252";
}
.glyphicon-triangle-top:before {
  content: "\e253";
}
.glyphicon-console:before {
  content: "\e254";
}
.glyphicon-superscript:before {
  content: "\e255";
}
.glyphicon-subscript:before {
  content: "\e256";
}
.glyphicon-menu-left:before {
  content: "\e257";
}
.glyphicon-menu-right:before {
  content: "\e258";
}
.glyphicon-menu-down:before {
  content: "\e259";
}
.glyphicon-menu-up:before {
  content: "\e260";
}
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
a {
  color: #337ab7;
  text-decoration: none;
}
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
[role="button"] {
  cursor: pointer;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.text-center {
  text-align: center;
}
.text-justify {
  text-align: justify;
}
.text-nowrap {
  white-space: nowrap;
}
.text-lowercase {
  text-transform: lowercase;
}
.text-uppercase {
  text-transform: uppercase;
}
.text-capitalize {
  text-transform: capitalize;
}
.text-muted {
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
}
.col-xs-12 {
  width: 100%;
}
.col-xs-11 {
  width: 91.66666667%;
}
.col-xs-10 {
  width: 83.33333333%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-8 {
  width: 66.66666667%;
}
.col-xs-7 {
  width: 58.33333333%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-5 {
  width: 41.66666667%;
}
.col-xs-4 {
  width: 33.33333333%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-2 {
  width: 16.66666667%;
}
.col-xs-1 {
  width: 8.33333333%;
}
.col-xs-pull-12 {
  right: 100%;
}
.col-xs-pull-11 {
  right: 91.66666667%;
}
.col-xs-pull-10 {
  right: 83.33333333%;
}
.col-xs-pull-9 {
  right: 75%;
}
.col-xs-pull-8 {
  right: 66.66666667%;
}
.col-xs-pull-7 {
  right: 58.33333333%;
}
.col-xs-pull-6 {
  right: 50%;
}
.col-xs-pull-5 {
  right: 41.66666667%;
}
.col-xs-pull-4 {
  right: 33.33333333%;
}
.col-xs-pull-3 {
  right: 25%;
}
.col-xs-pull-2 {
  right: 16.66666667%;
}
.col-xs-pull-1 {
  right: 8.33333333%;
}
.col-xs-pull-0 {
  right: auto;
}
.col-xs-push-12 {
  left: 100%;
}
.col-xs-push-11 {
  left: 91.66666667%;
}
.col-xs-push-10 {
  left: 83.33333333%;
}
.col-xs-push-9 {
  left: 75%;
}
.col-xs-push-8 {
  left: 66.66666667%;
}
.col-xs-push-7 {
  left: 58.33333333%;
}
.col-xs-push-6 {
  left: 50%;
}
.col-xs-push-5 {
  left: 41.66666667%;
}
.col-xs-push-4 {
  left: 33.33333333%;
}
.col-xs-push-3 {
  left: 25%;
}
.col-xs-push-2 {
  left: 16.66666667%;
}
.col-xs-push-1 {
  left: 8.33333333%;
}
.col-xs-push-0 {
  left: auto;
}
.col-xs-offset-12 {
  margin-left: 100%;
}
.col-xs-offset-11 {
  margin-left: 91.66666667%;
}
.col-xs-offset-10 {
  margin-left: 83.33333333%;
}
.col-xs-offset-9 {
  margin-left: 75%;
}
.col-xs-offset-8 {
  margin-left: 66.66666667%;
}
.col-xs-offset-7 {
  margin-left: 58.33333333%;
}
.col-xs-offset-6 {
  margin-left: 50%;
}
.col-xs-offset-5 {
  margin-left: 41.66666667%;
}
.col-xs-offset-4 {
  margin-left: 33.33333333%;
}
.col-xs-offset-3 {
  margin-left: 25%;
}
.col-xs-offset-2 {
  margin-left: 16.66666667%;
}
.col-xs-offset-1 {
  margin-left: 8.33333333%;
}
.col-xs-offset-0 {
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
    float: left;
  }
  .col-sm-12 {
    width: 100%;
  }
  .col-sm-11 {
    width: 91.66666667%;
  }
  .col-sm-10 {
    width: 83.33333333%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-8 {
    width: 66.66666667%;
  }
  .col-sm-7 {
    width: 58.33333333%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-5 {
    width: 41.66666667%;
  }
  .col-sm-4 {
    width: 33.33333333%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-2 {
    width: 16.66666667%;
  }
  .col-sm-1 {
    width: 8.33333333%;
  }
  .col-sm-pull-12 {
    right: 100%;
  }
  .col-sm-pull-11 {
    right: 91.66666667%;
  }
  .col-sm-pull-10 {
    right: 83.33333333%;
  }
  .col-sm-pull-9 {
    right: 75%;
  }
  .col-sm-pull-8 {
    right: 66.66666667%;
  }
  .col-sm-pull-7 {
    right: 58.33333333%;
  }
  .col-sm-pull-6 {
    right: 50%;
  }
  .col-sm-pull-5 {
    right: 41.66666667%;
  }
  .col-sm-pull-4 {
    right: 33.33333333%;
  }
  .col-sm-pull-3 {
    right: 25%;
  }
  .col-sm-pull-2 {
    right: 16.66666667%;
  }
  .col-sm-pull-1 {
    right: 8.33333333%;
  }
  .col-sm-pull-0 {
    right: auto;
  }
  .col-sm-push-12 {
    left: 100%;
  }
  .col-sm-push-11 {
    left: 91.66666667%;
  }
  .col-sm-push-10 {
    left: 83.33333333%;
  }
  .col-sm-push-9 {
    left: 75%;
  }
  .col-sm-push-8 {
    left: 66.66666667%;
  }
  .col-sm-push-7 {
    left: 58.33333333%;
  }
  .col-sm-push-6 {
    left: 50%;
  }
  .col-sm-push-5 {
    left: 41.66666667%;
  }
  .col-sm-push-4 {
    left: 33.33333333%;
  }
  .col-sm-push-3 {
    left: 25%;
  }
  .col-sm-push-2 {
    left: 16.66666667%;
  }
  .col-sm-push-1 {
    left: 8.33333333%;
  }
  .col-sm-push-0 {
    left: auto;
  }
  .col-sm-offset-12 {
    margin-left: 100%;
  }
  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-sm-offset-9 {
    margin-left: 75%;
  }
  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-sm-offset-6 {
    margin-left: 50%;
  }
  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-sm-offset-3 {
    margin-left: 25%;
  }
  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-sm-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
    float: left;
  }
  .col-md-12 {
    width: 100%;
  }
  .col-md-11 {
    width: 91.66666667%;
  }
  .col-md-10 {
    width: 83.33333333%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-8 {
    width: 66.66666667%;
  }
  .col-md-7 {
    width: 58.33333333%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-5 {
    width: 41.66666667%;
  }
  .col-md-4 {
    width: 33.33333333%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-2 {
    width: 16.66666667%;
  }
  .col-md-1 {
    width: 8.33333333%;
  }
  .col-md-pull-12 {
    right: 100%;
  }
  .col-md-pull-11 {
    right: 91.66666667%;
  }
  .col-md-pull-10 {
    right: 83.33333333%;
  }
  .col-md-pull-9 {
    right: 75%;
  }
  .col-md-pull-8 {
    right: 66.66666667%;
  }
  .col-md-pull-7 {
    right: 58.33333333%;
  }
  .col-md-pull-6 {
    right: 50%;
  }
  .col-md-pull-5 {
    right: 41.66666667%;
  }
  .col-md-pull-4 {
    right: 33.33333333%;
  }
  .col-md-pull-3 {
    right: 25%;
  }
  .col-md-pull-2 {
    right: 16.66666667%;
  }
  .col-md-pull-1 {
    right: 8.33333333%;
  }
  .col-md-pull-0 {
    right: auto;
  }
  .col-md-push-12 {
    left: 100%;
  }
  .col-md-push-11 {
    left: 91.66666667%;
  }
  .col-md-push-10 {
    left: 83.33333333%;
  }
  .col-md-push-9 {
    left: 75%;
  }
  .col-md-push-8 {
    left: 66.66666667%;
  }
  .col-md-push-7 {
    left: 58.33333333%;
  }
  .col-md-push-6 {
    left: 50%;
  }
  .col-md-push-5 {
    left: 41.66666667%;
  }
  .col-md-push-4 {
    left: 33.33333333%;
  }
  .col-md-push-3 {
    left: 25%;
  }
  .col-md-push-2 {
    left: 16.66666667%;
  }
  .col-md-push-1 {
    left: 8.33333333%;
  }
  .col-md-push-0 {
    left: auto;
  }
  .col-md-offset-12 {
    margin-left: 100%;
  }
  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-md-offset-9 {
    margin-left: 75%;
  }
  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-md-offset-6 {
    margin-left: 50%;
  }
  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-md-offset-3 {
    margin-left: 25%;
  }
  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-md-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
    float: left;
  }
  .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
  .col-lg-10 {
    width: 83.33333333%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-8 {
    width: 66.66666667%;
  }
  .col-lg-7 {
    width: 58.33333333%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-5 {
    width: 41.66666667%;
  }
  .col-lg-4 {
    width: 33.33333333%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-2 {
    width: 16.66666667%;
  }
  .col-lg-1 {
    width: 8.33333333%;
  }
  .col-lg-pull-12 {
    right: 100%;
  }
  .col-lg-pull-11 {
    right: 91.66666667%;
  }
  .col-lg-pull-10 {
    right: 83.33333333%;
  }
  .col-lg-pull-9 {
    right: 75%;
  }
  .col-lg-pull-8 {
    right: 66.66666667%;
  }
  .col-lg-pull-7 {
    right: 58.33333333%;
  }
  .col-lg-pull-6 {
    right: 50%;
  }
  .col-lg-pull-5 {
    right: 41.66666667%;
  }
  .col-lg-pull-4 {
    right: 33.33333333%;
  }
  .col-lg-pull-3 {
    right: 25%;
  }
  .col-lg-pull-2 {
    right: 16.66666667%;
  }
  .col-lg-pull-1 {
    right: 8.33333333%;
  }
  .col-lg-pull-0 {
    right: auto;
  }
  .col-lg-push-12 {
    left: 100%;
  }
  .col-lg-push-11 {
    left: 91.66666667%;
  }
  .col-lg-push-10 {
    left: 83.33333333%;
  }
  .col-lg-push-9 {
    left: 75%;
  }
  .col-lg-push-8 {
    left: 66.66666667%;
  }
  .col-lg-push-7 {
    left: 58.33333333%;
  }
  .col-lg-push-6 {
    left: 50%;
  }
  .col-lg-push-5 {
    left: 41.66666667%;
  }
  .col-lg-push-4 {
    left: 33.33333333%;
  }
  .col-lg-push-3 {
    left: 25%;
  }
  .col-lg-push-2 {
    left: 16.66666667%;
  }
  .col-lg-push-1 {
    left: 8.33333333%;
  }
  .col-lg-push-0 {
    left: auto;
  }
  .col-lg-offset-12 {
    margin-left: 100%;
  }
  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-lg-offset-9 {
    margin-left: 75%;
  }
  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-lg-offset-6 {
    margin-left: 50%;
  }
  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-lg-offset-3 {
    margin-left: 25%;
  }
  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-lg-offset-0 {
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
}
input[type="file"] {
  display: block;
}
input[type="range"] {
  display: block;
  width: 100%;
}
select[multiple],
select[size] {
  height: auto;
}
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.form-control:-ms-input-placeholder {
  color: #999;
}
.form-control::-webkit-input-placeholder {
  color: #999;
}
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
}
.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}
.has-success .input-group-addon {
  color: #3c763d;
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
  color: #8a6d3b;
}
.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}
.has-warning .input-group-addon {
  color: #8a6d3b;
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}
.has-error .input-group-addon {
  color: #a94442;
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
}
a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}
.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
  background-color: #fff;
  border-color: #ccc;
}
.btn-default .badge {
  color: #fff;
  background-color: #333;
}
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}
.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
  width: 100%;
}
.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}
.fade.in {
  opacity: 1;
}
.collapse {
  display: none;
}
.collapse.in {
  display: block;
}
tr.collapse.in {
  display: table-row;
}
tbody.collapse.in {
  display: table-row-group;
}
.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
}
.dropdown-toggle:focus {
  outline: 0;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
  z-index: 2;
}
.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}
.btn-toolbar {
  margin-left: -5px;
}
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
}
.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}
.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}
.btn-group-vertical > .btn-group > .btn {
  float: none;
}
.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}
.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}
.input-group[class*="col-"] {
  float: none;
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}
.input-group-addon {
  padding: 6px 12px;
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.input-group-addon:last-child {
  border-left: 0;
}
.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}
.input-group-btn > .btn {
  position: relative;
}
.input-group-btn > .btn + .btn {
  margin-left: -1px;
}
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
  z-index: 2;
}
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}
.nav {
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.nav > li > a > img {
  max-width: none;
}
.nav-tabs {
  border-bottom: 1px solid #ddd;
}
.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}
.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.tab-content > .tab-pane {
  display: none;
}
.tab-content > .active {
  display: block;
}
.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
    box-shadow: none;
  }
  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }
  .navbar-collapse.in {
    overflow-y: visible;
  }
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
}
.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}
.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}
.navbar-brand {
  float: left;
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
}
.navbar-toggle:focus {
  outline: 0;
}
.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}
.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
  }
  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}
.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}
.navbar-default .navbar-brand {
  color: #777;
}
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
  background-color: #ddd;
}
.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}
.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}
.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #ccc;
    background-color: transparent;
  }
}
.navbar-default .navbar-link {
  color: #777;
}
.navbar-default .navbar-link:hover {
  color: #333;
}
.navbar-default .btn-link {
  color: #777;
}
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
  background-color: #333;
}
.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}
.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}
.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #444;
    background-color: transparent;
  }
}
.navbar-inverse .navbar-link {
  color: #9d9d9d;
}
.navbar-inverse .navbar-link:hover {
  color: #fff;
}
.navbar-inverse .btn-link {
  color: #9d9d9d;
}
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.pager .next > a,
.pager .next > span {
  float: right;
}
.pager .previous > a,
.pager .previous > span {
  float: left;
}
.pager .disabled > a,
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}
.list-group-item > .badge {
  float: right;
}
.list-group-item > .badge + .badge {
  margin-right: 5px;
}
.nav-pills > li > a > .badge {
  margin-left: 3px;
}
.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
}
.jumbotron .container {
  max-width: 100%;
}
@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }
  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
}
.alert > p,
.alert > ul {
  margin-bottom: 0;
}
.alert > p + p {
  margin-top: 5px;
}
.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}
.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
}
.alert-danger hr {
  border-top-color: #e4b9c0;
}
.alert-danger .alert-link {
  color: #843534;
}
@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
}
.media-object.img-thumbnail {
  max-width: none;
}
.media-right,
.media > .pull-right {
  padding-left: 10px;
}
.media-left,
.media > .pull-left {
  padding-right: 10px;
}
.media-left,
.media-right,
.media-body {
  display: table-cell;
  vertical-align: top;
}
.media-middle {
  vertical-align: middle;
}
.media-bottom {
  vertical-align: bottom;
}
.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.media-list {
  padding-left: 0;
  list-style: none;
}
.list-group {
  margin-bottom: 20px;
  padding-left: 0;
}
.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
.list-group-item:first-child {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
  color: #c7ddef;
}
.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}
a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}
a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}
.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}
a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}
a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}
.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}
a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}
a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}
.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}
a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}
a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
  border-top: 1px solid #ddd;
}
.panel-group .panel-footer {
  border-top: 0;
}
.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}
.panel-default {
  border-color: #ddd;
}
.panel-default > .panel-heading {
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
}
.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}
.panel-primary {
  border-color: #337ab7;
}
.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}
.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}
.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}
.panel-success {
  border-color: #d6e9c6;
}
.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}
.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}
.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}
.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}
.panel-info {
  border-color: #bce8f1;
}
.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}
.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}
.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}
.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}
.panel-warning {
  border-color: #faebcc;
}
.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}
.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}
.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}
.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}
.panel-danger {
  border-color: #ebccd1;
}
.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}
.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}
.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}
.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}
.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
  border: 0;
}
.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}
.embed-responsive-4by3 {
  padding-bottom: 75%;
}
.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
}
.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}
.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}
.modal-content {
  position: relative;
  background-color: #fff;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}
.modal-header .close {
  margin-top: -2px;
}
.modal-title {
  margin: 0;
  line-height: 1.42857143;
}
.modal-body {
  position: relative;
  padding: 15px;
}
.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}
.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0;
}
.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}
.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}
.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}
@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }
  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }
  .modal-sm {
    width: 300px;
  }
}
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
}
.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-left .tooltip-arrow {
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}
.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
.popover.top {
  margin-top: -10px;
}
.popover.right {
  margin-left: 10px;
}
.popover.bottom {
  margin-top: 10px;
}
.popover.left {
  margin-left: -10px;
}
.popover-title {
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
}
.popover-content {
  padding: 9px 14px;
}
.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
  }
}
.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}
.carousel-inner > .active {
  left: 0;
}
.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}
.carousel-inner > .next {
  left: 100%;
}
.carousel-inner > .prev {
  left: -100%;
}
.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}
.carousel-inner > .active.left {
  left: -100%;
}
.carousel-inner > .active.right {
  left: 100%;
}
.carousel-control {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.pull-right {
  float: right !important;
}
.pull-left {
  float: left !important;
}
.hide {
  display: none !important;
}
.show {
  display: block !important;
}
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
}
@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }
  table.visible-xs {
    display: table !important;
  }
  tr.visible-xs {
    display: table-row !important;
  }
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }
  table.visible-sm {
    display: table !important;
  }
  tr.visible-sm {
    display: table-row !important;
  }
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }
  table.visible-md {
    display: table !important;
  }
  tr.visible-md {
    display: table-row !important;
  }
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }
  table.visible-lg {
    display: table !important;
  }
  tr.visible-lg {
    display: table-row !important;
  }
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
  }
}
@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}
@media (min-width: 1200px) {
  .hidden-lg {
    display: none !important;
  }
}
.visible-print {
  display: none !important;
}
@media print {
  .visible-print {
    display: block !important;
  }
  table.visible-print {
    display: table !important;
  }
  tr.visible-print {
    display: table-row !important;
  }
  th.visible-print,
  td.visible-print {
    display: table-cell !important;
  }
}
.visible-print-block {
  display: none !important;
}
@media print {
  .visible-print-block {
    display: block !important;
  }
}
.visible-print-inline {
  display: none !important;
}
@media print {
  .visible-print-inline {
    display: inline !important;
  }
}
.visible-print-inline-block {
  display: none !important;
}
@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.7.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.7.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.7.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff2?v=4.7.0') format('woff2'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.7.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.7.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.7.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.fa-pull-left {
  float: left;
}
.fa-pull-right {
  float: right;
}
.fa.fa-pull-left {
  margin-right: .3em;
}
.fa.fa-pull-right {
  margin-left: .3em;
}
/* Deprecated as of 4.4.0 */
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
.fa-pulse {
  -webkit-animation: fa-spin 1s infinite steps(8);
  animation: fa-spin 1s infinite steps(8);
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=1)";
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2)";
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=3)";
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1)";
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1)";
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook-f:before,
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-feed:before,
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before,
.fa-gratipay:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper-pp:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-resistance:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-y-combinator-square:before,
.fa-yc-square:before,
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
.fa-buysellads:before {
  content: "\f20d";
}
.fa-connectdevelop:before {
  content: "\f20e";
}
.fa-dashcube:before {
  content: "\f210";
}
.fa-forumbee:before {
  content: "\f211";
}
.fa-leanpub:before {
  content: "\f212";
}
.fa-sellsy:before {
  content: "\f213";
}
.fa-shirtsinbulk:before {
  content: "\f214";
}
.fa-simplybuilt:before {
  content: "\f215";
}
.fa-skyatlas:before {
  content: "\f216";
}
.fa-cart-plus:before {
  content: "\f217";
}
.fa-cart-arrow-down:before {
  content: "\f218";
}
.fa-diamond:before {
  content: "\f219";
}
.fa-ship:before {
  content: "\f21a";
}
.fa-user-secret:before {
  content: "\f21b";
}
.fa-motorcycle:before {
  content: "\f21c";
}
.fa-street-view:before {
  content: "\f21d";
}
.fa-heartbeat:before {
  content: "\f21e";
}
.fa-venus:before {
  content: "\f221";
}
.fa-mars:before {
  content: "\f222";
}
.fa-mercury:before {
  content: "\f223";
}
.fa-intersex:before,
.fa-transgender:before {
  content: "\f224";
}
.fa-transgender-alt:before {
  content: "\f225";
}
.fa-venus-double:before {
  content: "\f226";
}
.fa-mars-double:before {
  content: "\f227";
}
.fa-venus-mars:before {
  content: "\f228";
}
.fa-mars-stroke:before {
  content: "\f229";
}
.fa-mars-stroke-v:before {
  content: "\f22a";
}
.fa-mars-stroke-h:before {
  content: "\f22b";
}
.fa-neuter:before {
  content: "\f22c";
}
.fa-genderless:before {
  content: "\f22d";
}
.fa-facebook-official:before {
  content: "\f230";
}
.fa-pinterest-p:before {
  content: "\f231";
}
.fa-whatsapp:before {
  content: "\f232";
}
.fa-server:before {
  content: "\f233";
}
.fa-user-plus:before {
  content: "\f234";
}
.fa-user-times:before {
  content: "\f235";
}
.fa-hotel:before,
.fa-bed:before {
  content: "\f236";
}
.fa-viacoin:before {
  content: "\f237";
}
.fa-train:before {
  content: "\f238";
}
.fa-subway:before {
  content: "\f239";
}
.fa-medium:before {
  content: "\f23a";
}
.fa-yc:before,
.fa-y-combinator:before {
  content: "\f23b";
}
.fa-optin-monster:before {
  content: "\f23c";
}
.fa-opencart:before {
  content: "\f23d";
}
.fa-expeditedssl:before {
  content: "\f23e";
}
.fa-battery-4:before,
.fa-battery:before,
.fa-battery-full:before {
  content: "\f240";
}
.fa-battery-3:before,
.fa-battery-three-quarters:before {
  content: "\f241";
}
.fa-battery-2:before,
.fa-battery-half:before {
  content: "\f242";
}
.fa-battery-1:before,
.fa-battery-quarter:before {
  content: "\f243";
}
.fa-battery-0:before,
.fa-battery-empty:before {
  content: "\f244";
}
.fa-mouse-pointer:before {
  content: "\f245";
}
.fa-i-cursor:before {
  content: "\f246";
}
.fa-object-group:before {
  content: "\f247";
}
.fa-object-ungroup:before {
  content: "\f248";
}
.fa-sticky-note:before {
  content: "\f249";
}
.fa-sticky-note-o:before {
  content: "\f24a";
}
.fa-cc-jcb:before {
  content: "\f24b";
}
.fa-cc-diners-club:before {
  content: "\f24c";
}
.fa-clone:before {
  content: "\f24d";
}
.fa-balance-scale:before {
  content: "\f24e";
}
.fa-hourglass-o:before {
  content: "\f250";
}
.fa-hourglass-1:before,
.fa-hourglass-start:before {
  content: "\f251";
}
.fa-hourglass-2:before,
.fa-hourglass-half:before {
  content: "\f252";
}
.fa-hourglass-3:before,
.fa-hourglass-end:before {
  content: "\f253";
}
.fa-hourglass:before {
  content: "\f254";
}
.fa-hand-grab-o:before,
.fa-hand-rock-o:before {
  content: "\f255";
}
.fa-hand-stop-o:before,
.fa-hand-paper-o:before {
  content: "\f256";
}
.fa-hand-scissors-o:before {
  content: "\f257";
}
.fa-hand-lizard-o:before {
  content: "\f258";
}
.fa-hand-spock-o:before {
  content: "\f259";
}
.fa-hand-pointer-o:before {
  content: "\f25a";
}
.fa-hand-peace-o:before {
  content: "\f25b";
}
.fa-trademark:before {
  content: "\f25c";
}
.fa-registered:before {
  content: "\f25d";
}
.fa-creative-commons:before {
  content: "\f25e";
}
.fa-gg:before {
  content: "\f260";
}
.fa-gg-circle:before {
  content: "\f261";
}
.fa-tripadvisor:before {
  content: "\f262";
}
.fa-odnoklassniki:before {
  content: "\f263";
}
.fa-odnoklassniki-square:before {
  content: "\f264";
}
.fa-get-pocket:before {
  content: "\f265";
}
.fa-wikipedia-w:before {
  content: "\f266";
}
.fa-safari:before {
  content: "\f267";
}
.fa-chrome:before {
  content: "\f268";
}
.fa-firefox:before {
  content: "\f269";
}
.fa-opera:before {
  content: "\f26a";
}
.fa-internet-explorer:before {
  content: "\f26b";
}
.fa-tv:before,
.fa-television:before {
  content: "\f26c";
}
.fa-contao:before {
  content: "\f26d";
}
.fa-500px:before {
  content: "\f26e";
}
.fa-amazon:before {
  content: "\f270";
}
.fa-calendar-plus-o:before {
  content: "\f271";
}
.fa-calendar-minus-o:before {
  content: "\f272";
}
.fa-calendar-times-o:before {
  content: "\f273";
}
.fa-calendar-check-o:before {
  content: "\f274";
}
.fa-industry:before {
  content: "\f275";
}
.fa-map-pin:before {
  content: "\f276";
}
.fa-map-signs:before {
  content: "\f277";
}
.fa-map-o:before {
  content: "\f278";
}
.fa-map:before {
  content: "\f279";
}
.fa-commenting:before {
  content: "\f27a";
}
.fa-commenting-o:before {
  content: "\f27b";
}
.fa-houzz:before {
  content: "\f27c";
}
.fa-vimeo:before {
  content: "\f27d";
}
.fa-black-tie:before {
  content: "\f27e";
}
.fa-fonticons:before {
  content: "\f280";
}
.fa-reddit-alien:before {
  content: "\f281";
}
.fa-edge:before {
  content: "\f282";
}
.fa-credit-card-alt:before {
  content: "\f283";
}
.fa-codiepie:before {
  content: "\f284";
}
.fa-modx:before {
  content: "\f285";
}
.fa-fort-awesome:before {
  content: "\f286";
}
.fa-usb:before {
  content: "\f287";
}
.fa-product-hunt:before {
  content: "\f288";
}
.fa-mixcloud:before {
  content: "\f289";
}
.fa-scribd:before {
  content: "\f28a";
}
.fa-pause-circle:before {
  content: "\f28b";
}
.fa-pause-circle-o:before {
  content: "\f28c";
}
.fa-stop-circle:before {
  content: "\f28d";
}
.fa-stop-circle-o:before {
  content: "\f28e";
}
.fa-shopping-bag:before {
  content: "\f290";
}
.fa-shopping-basket:before {
  content: "\f291";
}
.fa-hashtag:before {
  content: "\f292";
}
.fa-bluetooth:before {
  content: "\f293";
}
.fa-bluetooth-b:before {
  content: "\f294";
}
.fa-percent:before {
  content: "\f295";
}
.fa-gitlab:before {
  content: "\f296";
}
.fa-wpbeginner:before {
  content: "\f297";
}
.fa-wpforms:before {
  content: "\f298";
}
.fa-envira:before {
  content: "\f299";
}
.fa-universal-access:before {
  content: "\f29a";
}
.fa-wheelchair-alt:before {
  content: "\f29b";
}
.fa-question-circle-o:before {
  content: "\f29c";
}
.fa-blind:before {
  content: "\f29d";
}
.fa-audio-description:before {
  content: "\f29e";
}
.fa-volume-control-phone:before {
  content: "\f2a0";
}
.fa-braille:before {
  content: "\f2a1";
}
.fa-assistive-listening-systems:before {
  content: "\f2a2";
}
.fa-asl-interpreting:before,
.fa-american-sign-language-interpreting:before {
  content: "\f2a3";
}
.fa-deafness:before,
.fa-hard-of-hearing:before,
.fa-deaf:before {
  content: "\f2a4";
}
.fa-glide:before {
  content: "\f2a5";
}
.fa-glide-g:before {
  content: "\f2a6";
}
.fa-signing:before,
.fa-sign-language:before {
  content: "\f2a7";
}
.fa-low-vision:before {
  content: "\f2a8";
}
.fa-viadeo:before {
  content: "\f2a9";
}
.fa-viadeo-square:before {
  content: "\f2aa";
}
.fa-snapchat:before {
  content: "\f2ab";
}
.fa-snapchat-ghost:before {
  content: "\f2ac";
}
.fa-snapchat-square:before {
  content: "\f2ad";
}
.fa-pied-piper:before {
  content: "\f2ae";
}
.fa-first-order:before {
  content: "\f2b0";
}
.fa-yoast:before {
  content: "\f2b1";
}
.fa-themeisle:before {
  content: "\f2b2";
}
.fa-google-plus-circle:before,
.fa-google-plus-official:before {
  content: "\f2b3";
}
.fa-fa:before,
.fa-font-awesome:before {
  content: "\f2b4";
}
.fa-handshake-o:before {
  content: "\f2b5";
}
.fa-envelope-open:before {
  content: "\f2b6";
}
.fa-envelope-open-o:before {
  content: "\f2b7";
}
.fa-linode:before {
  content: "\f2b8";
}
.fa-address-book:before {
  content: "\f2b9";
}
.fa-address-book-o:before {
  content: "\f2ba";
}
.fa-vcard:before,
.fa-address-card:before {
  content: "\f2bb";
}
.fa-vcard-o:before,
.fa-address-card-o:before {
  content: "\f2bc";
}
.fa-user-circle:before {
  content: "\f2bd";
}
.fa-user-circle-o:before {
  content: "\f2be";
}
.fa-user-o:before {
  content: "\f2c0";
}
.fa-id-badge:before {
  content: "\f2c1";
}
.fa-drivers-license:before,
.fa-id-card:before {
  content: "\f2c2";
}
.fa-drivers-license-o:before,
.fa-id-card-o:before {
  content: "\f2c3";
}
.fa-quora:before {
  content: "\f2c4";
}
.fa-free-code-camp:before {
  content: "\f2c5";
}
.fa-telegram:before {
  content: "\f2c6";
}
.fa-thermometer-4:before,
.fa-thermometer:before,
.fa-thermometer-full:before {
  content: "\f2c7";
}
.fa-thermometer-3:before,
.fa-thermometer-three-quarters:before {
  content: "\f2c8";
}
.fa-thermometer-2:before,
.fa-thermometer-half:before {
  content: "\f2c9";
}
.fa-thermometer-1:before,
.fa-thermometer-quarter:before {
  content: "\f2ca";
}
.fa-thermometer-0:before,
.fa-thermometer-empty:before {
  content: "\f2cb";
}
.fa-shower:before {
  content: "\f2cc";
}
.fa-bathtub:before,
.fa-s15:before,
.fa-bath:before {
  content: "\f2cd";
}
.fa-podcast:before {
  content: "\f2ce";
}
.fa-window-maximize:before {
  content: "\f2d0";
}
.fa-window-minimize:before {
  content: "\f2d1";
}
.fa-window-restore:before {
  content: "\f2d2";
}
.fa-times-rectangle:before,
.fa-window-close:before {
  content: "\f2d3";
}
.fa-times-rectangle-o:before,
.fa-window-close-o:before {
  content: "\f2d4";
}
.fa-bandcamp:before {
  content: "\f2d5";
}
.fa-grav:before {
  content: "\f2d6";
}
.fa-etsy:before {
  content: "\f2d7";
}
.fa-imdb:before {
  content: "\f2d8";
}
.fa-ravelry:before {
  content: "\f2d9";
}
.fa-eercast:before {
  content: "\f2da";
}
.fa-microchip:before {
  content: "\f2db";
}
.fa-snowflake-o:before {
  content: "\f2dc";
}
.fa-superpowers:before {
  content: "\f2dd";
}
.fa-wpexplorer:before {
  content: "\f2de";
}
.fa-meetup:before {
  content: "\f2e0";
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box 
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this 
new spec completely include:

    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+ 
    Opera 17.0+

Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
div.traceback-wrapper pre.traceback {
  max-height: 600px;
  overflow: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 5px;
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
[dir="rtl"] #ipython_notebook {
  margin-right: 10px;
  margin-left: 0;
}
[dir="rtl"] #ipython_notebook.pull-left {
  float: right !important;
  float: right;
}
.flex-spacer {
  flex: 1;
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#kernel_logo_widget {
  margin: 0 10px;
}
span#login_widget {
  float: right;
}
[dir="rtl"] span#login_widget {
  float: left;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
.modal-header {
  cursor: move;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
[dir="rtl"] .center-nav form.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] .center-nav .navbar-text {
  float: right;
}
[dir="rtl"] .navbar-inner {
  text-align: right;
}
[dir="rtl"] div.text-left {
  text-align: right;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  position: absolute;
  display: block;
  width: 100%;
  height: 100%;
  overflow: hidden;
  cursor: pointer;
  opacity: 0;
  z-index: 2;
}
.alternate_upload .btn-xs > input.fileinput {
  margin: -1px -5px;
}
.alternate_upload .btn-upload {
  position: relative;
  height: 22px;
}
::-webkit-file-upload-button {
  cursor: pointer;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
ul#tabs {
  margin-bottom: 4px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
[dir="rtl"] ul#tabs.nav-tabs > li {
  float: right;
}
[dir="rtl"] ul#tabs.nav.nav-tabs {
  padding-right: 0;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
[dir="rtl"] .list_toolbar .tree-buttons .pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .list_toolbar .col-sm-4,
[dir="rtl"] .list_toolbar .col-sm-8 {
  float: right;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: text-bottom;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
[dir="rtl"] .list_item > div input {
  margin-right: 0;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_modified {
  margin-right: 7px;
  margin-left: 7px;
}
[dir="rtl"] .item_modified.pull-right {
  float: left !important;
  float: left;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
[dir="rtl"] .item_buttons.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .item_buttons .kernel-name {
  margin-left: 7px;
  float: right;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
.sort_button {
  display: inline-block;
  padding-left: 7px;
}
[dir="rtl"] .sort_button.pull-right {
  float: left !important;
  float: left;
}
#tree-selector {
  padding-right: 0px;
}
#button-select-all {
  min-width: 50px;
}
[dir="rtl"] #button-select-all.btn {
  float: right ;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
  margin-top: 2px;
  height: 16px;
}
[dir="rtl"] #select-all.pull-left {
  float: right !important;
  float: right;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.fa-pull-left {
  margin-right: .3em;
}
.folder_icon:before.fa-pull-right {
  margin-left: .3em;
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.fa-pull-left {
  margin-right: .3em;
}
.file_icon:before.fa-pull-right {
  margin-left: .3em;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
#new-menu .dropdown-header {
  font-size: 10px;
  border-bottom: 1px solid #e5e5e5;
  padding: 0 0 3px;
  margin: -3px 20px 0;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.move-button {
  display: none;
}
.download-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
.CodeMirror-dialog {
  background-color: #fff;
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI escape sequences */
/* The color values are a mix of
   http://www.xcolors.net/dl/baskerville-ivorylight and
   http://www.xcolors.net/dl/euphrasia */
.ansi-black-fg {
  color: #3E424D;
}
.ansi-black-bg {
  background-color: #3E424D;
}
.ansi-black-intense-fg {
  color: #282C36;
}
.ansi-black-intense-bg {
  background-color: #282C36;
}
.ansi-red-fg {
  color: #E75C58;
}
.ansi-red-bg {
  background-color: #E75C58;
}
.ansi-red-intense-fg {
  color: #B22B31;
}
.ansi-red-intense-bg {
  background-color: #B22B31;
}
.ansi-green-fg {
  color: #00A250;
}
.ansi-green-bg {
  background-color: #00A250;
}
.ansi-green-intense-fg {
  color: #007427;
}
.ansi-green-intense-bg {
  background-color: #007427;
}
.ansi-yellow-fg {
  color: #DDB62B;
}
.ansi-yellow-bg {
  background-color: #DDB62B;
}
.ansi-yellow-intense-fg {
  color: #B27D12;
}
.ansi-yellow-intense-bg {
  background-color: #B27D12;
}
.ansi-blue-fg {
  color: #208FFB;
}
.ansi-blue-bg {
  background-color: #208FFB;
}
.ansi-blue-intense-fg {
  color: #0065CA;
}
.ansi-blue-intense-bg {
  background-color: #0065CA;
}
.ansi-magenta-fg {
  color: #D160C4;
}
.ansi-magenta-bg {
  background-color: #D160C4;
}
.ansi-magenta-intense-fg {
  color: #A03196;
}
.ansi-magenta-intense-bg {
  background-color: #A03196;
}
.ansi-cyan-fg {
  color: #60C6C8;
}
.ansi-cyan-bg {
  background-color: #60C6C8;
}
.ansi-cyan-intense-fg {
  color: #258F8F;
}
.ansi-cyan-intense-bg {
  background-color: #258F8F;
}
.ansi-white-fg {
  color: #C5C1B4;
}
.ansi-white-bg {
  background-color: #C5C1B4;
}
.ansi-white-intense-fg {
  color: #A1A6B2;
}
.ansi-white-intense-bg {
  background-color: #A1A6B2;
}
.ansi-default-inverse-fg {
  color: #FFFFFF;
}
.ansi-default-inverse-bg {
  background-color: #000000;
}
.ansi-bold {
  font-weight: bold;
}
.ansi-underline {
  text-decoration: underline;
}
/* The following styles are deprecated an will be removed in a future version */
.ansibold {
  font-weight: bold;
}
.ansi-inverse {
  outline: 0.5px dotted;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  position: relative;
  overflow: visible;
}
div.cell:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: transparent;
}
div.cell.jupyter-soft-selected {
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected,
div.cell.selected.jupyter-soft-selected {
  border-color: #ababab;
}
div.cell.selected:before,
div.cell.selected.jupyter-soft-selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #42A5F5;
}
@media print {
  div.cell.selected,
  div.cell.selected.jupyter-soft-selected {
    border-color: transparent;
  }
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
}
.edit_mode div.cell.selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #66BB6A;
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  /* Note that this should set vertical padding only, since CodeMirror assumes
       that horizontal padding will be set on CodeMirror pre */
  padding: 0.4em 0;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. This sets horizontal padding only,
    use .CodeMirror-lines for vertical */
  padding: 0 0.4em;
  border: 0;
  border-radius: 0;
}
.CodeMirror-cursor {
  border-left: 1.4px solid black;
}
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .CodeMirror-cursor {
    border-left: 2px solid black;
  }
}
@media screen and (min-width: 4320px) {
  .CodeMirror-cursor {
    border-left: 4px solid black;
  }
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
div.output_area .mglyph > img {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 1px 0 1px 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul:not(.list-inline),
.rendered_html ol:not(.list-inline) {
  padding-left: 2em;
}
.rendered_html ul {
  list-style: disc;
}
.rendered_html ul ul {
  list-style: square;
  margin-top: 0;
}
.rendered_html ul ul ul {
  list-style: circle;
}
.rendered_html ol {
  list-style: decimal;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin-top: 0;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
  padding: 0px;
  background-color: #fff;
}
.rendered_html code {
  background-color: #eff0f1;
}
.rendered_html p code {
  padding: 1px 5px;
}
.rendered_html pre code {
  background-color: #fff;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  color: #000;
  font-size: 100%;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: none;
  border-collapse: collapse;
  border-spacing: 0;
  color: black;
  font-size: 12px;
  table-layout: fixed;
}
.rendered_html thead {
  border-bottom: 1px solid black;
  vertical-align: bottom;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  text-align: right;
  vertical-align: middle;
  padding: 0.5em 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html tbody tr:nth-child(odd) {
  background: #f5f5f5;
}
.rendered_html tbody tr:hover {
  background: rgba(66, 165, 245, 0.2);
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
.rendered_html .alert {
  margin-bottom: initial;
}
.rendered_html * + .alert {
  margin-top: 1em;
}
[dir="rtl"] .rendered_html p {
  text-align: right;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.rendered .rendered_html tr,
.text_cell.rendered .rendered_html th,
.text_cell.rendered .rendered_html td {
  max-width: none;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.text_cell .dropzone .input_area {
  border: 2px dashed #bababa;
  margin: -1px;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
.jupyter-keybindings {
  padding: 1px;
  line-height: 24px;
  border-bottom: 1px solid gray;
}
.jupyter-keybindings input {
  margin: 0;
  padding: 0;
  border: none;
}
.jupyter-keybindings i {
  padding: 6px;
}
.well code {
  background-color: #ffffff;
  border-color: #ababab;
  border-width: 1px;
  border-style: solid;
  padding: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.tags_button_container {
  width: 100%;
  display: flex;
}
.tag-container {
  display: flex;
  flex-direction: row;
  flex-grow: 1;
  overflow: hidden;
  position: relative;
}
.tag-container > * {
  margin: 0 4px;
}
.remove-tag-btn {
  margin-left: 4px;
}
.tags-input {
  display: flex;
}
.cell-tag:last-child:after {
  content: "";
  position: absolute;
  right: 0;
  width: 40px;
  height: 100%;
  /* Fade to background color of cell toolbar */
  background: linear-gradient(to right, rgba(0, 0, 0, 0), #EEE);
}
.tags-input > * {
  margin-left: 4px;
}
.cell-tag,
.tags-input input,
.tags-input button {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  box-shadow: none;
  width: inherit;
  font-size: inherit;
  height: 22px;
  line-height: 22px;
  padding: 0px 4px;
  display: inline-block;
}
.cell-tag:focus,
.tags-input input:focus,
.tags-input button:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.cell-tag::-moz-placeholder,
.tags-input input::-moz-placeholder,
.tags-input button::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.cell-tag:-ms-input-placeholder,
.tags-input input:-ms-input-placeholder,
.tags-input button:-ms-input-placeholder {
  color: #999;
}
.cell-tag::-webkit-input-placeholder,
.tags-input input::-webkit-input-placeholder,
.tags-input button::-webkit-input-placeholder {
  color: #999;
}
.cell-tag::-ms-expand,
.tags-input input::-ms-expand,
.tags-input button::-ms-expand {
  border: 0;
  background-color: transparent;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
.cell-tag[readonly],
.tags-input input[readonly],
.tags-input button[readonly],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  background-color: #eeeeee;
  opacity: 1;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  cursor: not-allowed;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button {
  height: auto;
}
select.cell-tag,
select.tags-input input,
select.tags-input button {
  height: 30px;
  line-height: 30px;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button,
select[multiple].cell-tag,
select[multiple].tags-input input,
select[multiple].tags-input button {
  height: auto;
}
.cell-tag,
.tags-input button {
  padding: 0px 4px;
}
.cell-tag {
  background-color: #fff;
  white-space: nowrap;
}
.tags-input input[type=text]:focus {
  outline: none;
  box-shadow: none;
  border-color: #ccc;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
[dir="rtl"] #kernel_logo_widget {
  float: left !important;
  float: left;
}
.modal .modal-body .move-path {
  display: flex;
  flex-direction: row;
  justify-content: space;
  align-items: center;
}
.modal .modal-body .move-path .server-root {
  padding-right: 20px;
}
.modal .modal-body .move-path .path-input {
  flex: 1;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
[dir="rtl"] #menubar .navbar-toggle {
  float: right;
}
[dir="rtl"] #menubar .navbar-collapse {
  clear: right;
}
[dir="rtl"] #menubar .navbar-nav {
  float: right;
}
[dir="rtl"] #menubar .nav {
  padding-right: 0px;
}
[dir="rtl"] #menubar .navbar-nav > li {
  float: right;
}
[dir="rtl"] #menubar .navbar-right {
  float: left !important;
}
[dir="rtl"] ul.dropdown-menu {
  text-align: right;
  left: auto;
}
[dir="rtl"] ul#new-menu.dropdown-menu {
  right: auto;
  left: 0;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
[dir="rtl"] i.menu-icon.pull-right {
  float: left !important;
  float: left;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
[dir="rtl"] ul#help_menu li a {
  padding-left: 2.2em;
}
[dir="rtl"] ul#help_menu li a i {
  margin-right: 0;
  margin-left: -1.2em;
}
[dir="rtl"] ul#help_menu li a i.pull-right {
  float: left !important;
  float: left;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
[dir="rtl"] .dropdown-submenu > .dropdown-menu {
  right: 100%;
  margin-right: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.fa-pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.fa-pull-right {
  margin-left: .3em;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
[dir="rtl"] .dropdown-submenu > a:after {
  float: left;
  content: "\f0d9";
  margin-right: 0;
  margin-left: -10px;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
[dir="rtl"] #notification_area {
  float: left !important;
  float: left;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] .indicator_area {
  float: left !important;
  float: left;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
[dir="rtl"] #kernel_indicator {
  float: left !important;
  float: left;
  border-left: 0;
  border-right: 1px solid;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] #modal_indicator {
  float: left !important;
  float: left;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for 
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 21ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  height: 30px;
  margin-top: 4px;
  display: flex;
  justify-content: flex-start;
  align-items: baseline;
  width: 50%;
  flex: 1;
}
span.save_widget span.filename {
  height: 100%;
  line-height: 1em;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  text-overflow: ellipsis;
  overflow: hidden;
  white-space: nowrap;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
[dir="rtl"] span.save_widget.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] span.save_widget span.filename {
  margin-left: 0;
  margin-right: 16px;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
  white-space: nowrap;
  padding: 0 5px;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
    padding: 0 0 0 5px;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
.toolbar-btn-label {
  margin-left: 6px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
[dir="rtl"] .btn-group > .btn,
.btn-group-vertical > .btn {
  float: right;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
[dir="rtl"] ul.typeahead-list i {
  margin-left: 0;
  margin-right: -10px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
ul.typeahead-list  > li > a.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .typeahead-list {
  text-align: right;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  min-width: 20px;
  color: transparent;
}
[dir="rtl"] .no-shortcut.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .command-shortcut.pull-right {
  float: left !important;
  float: left;
}
.command-shortcut:before {
  content: "(command mode)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
[dir="rtl"] .edit-shortcut.pull-right {
  float: left !important;
  float: left;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
[dir="ltr"] #find-and-replace .input-group-btn + .form-control {
  border-left: none;
}
[dir="rtl"] #find-and-replace .input-group-btn + .form-control {
  border-right: none;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  width: 100%;
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal .xterm-rows {
  padding: 10px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>
<style type="text/css">
    
/* Temporary definitions which will become obsolete with Notebook release 5.0 */
.ansi-black-fg { color: #3E424D; }
.ansi-black-bg { background-color: #3E424D; }
.ansi-black-intense-fg { color: #282C36; }
.ansi-black-intense-bg { background-color: #282C36; }
.ansi-red-fg { color: #E75C58; }
.ansi-red-bg { background-color: #E75C58; }
.ansi-red-intense-fg { color: #B22B31; }
.ansi-red-intense-bg { background-color: #B22B31; }
.ansi-green-fg { color: #00A250; }
.ansi-green-bg { background-color: #00A250; }
.ansi-green-intense-fg { color: #007427; }
.ansi-green-intense-bg { background-color: #007427; }
.ansi-yellow-fg { color: #DDB62B; }
.ansi-yellow-bg { background-color: #DDB62B; }
.ansi-yellow-intense-fg { color: #B27D12; }
.ansi-yellow-intense-bg { background-color: #B27D12; }
.ansi-blue-fg { color: #208FFB; }
.ansi-blue-bg { background-color: #208FFB; }
.ansi-blue-intense-fg { color: #0065CA; }
.ansi-blue-intense-bg { background-color: #0065CA; }
.ansi-magenta-fg { color: #D160C4; }
.ansi-magenta-bg { background-color: #D160C4; }
.ansi-magenta-intense-fg { color: #A03196; }
.ansi-magenta-intense-bg { background-color: #A03196; }
.ansi-cyan-fg { color: #60C6C8; }
.ansi-cyan-bg { background-color: #60C6C8; }
.ansi-cyan-intense-fg { color: #258F8F; }
.ansi-cyan-intense-bg { background-color: #258F8F; }
.ansi-white-fg { color: #C5C1B4; }
.ansi-white-bg { background-color: #C5C1B4; }
.ansi-white-intense-fg { color: #A1A6B2; }
.ansi-white-intense-bg { background-color: #A1A6B2; }

.ansi-bold { font-weight: bold; }

    </style>
<style type="text/css">
    %%HTML
<style type="text/css">
table.dataframe td, table.dataframe th {
    border: 1px  black solid !important;
  color: black !important;}
    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="matplotlib">matplotlib<a class="anchor-link" href="#matplotlib">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>matplotlib is the most popular library for python</li>
<li>It give you control  over every aspect of figure</li>
<li>it was designed to have a similar feel to  MatLab's graphical plotting</li>
</ul>
<h3 id="Official-website-https://matplotlib.org/">Official website <a href="https://matplotlib.org/">https://matplotlib.org/</a><a class="anchor-link" href="#Official-website-https://matplotlib.org/">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="o">%</span><span class="k">matplotlib</span> inline
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="n">x</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span><span class="mi">5</span><span class="p">,</span><span class="mi">11</span><span class="p">)</span>
<span class="n">y</span><span class="o">=</span><span class="n">x</span> <span class="o">**</span><span class="mi">2</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[11]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">x</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[11]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([ 0. ,  0.5,  1. ,  1.5,  2. ,  2.5,  3. ,  3.5,  4. ,  4.5,  5. ])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[12]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">y</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[12]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([  0.  ,   0.25,   1.  ,   2.25,   4.  ,   6.25,   9.  ,  12.25,
        16.  ,  20.25,  25.  ])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Using-two-way-we-can-create-matplotlib-graph">Using two way we can create matplotlib graph<a class="anchor-link" href="#Using-two-way-we-can-create-matplotlib-graph">&#182;</a></h3><ul>
<li>Functional method </li>
<li>object oriented method</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Functional-method">Functional method<a class="anchor-link" href="#Functional-method">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[23]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Adding-lable-to-graph">Adding lable to graph<a class="anchor-link" href="#Adding-lable-to-graph">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[24]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s2">&quot;X lable&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s2">&quot;Y Lable&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s2">&quot;First grap from Matplot lib&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[24]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0.5, 1.0, &#39;First grap from Matplot lib&#39;)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Multiplot-on-same-canvas">Multiplot on same canvas<a class="anchor-link" href="#Multiplot-on-same-canvas">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[25]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">2</span><span class="p">,</span><span class="mi">1</span><span class="p">)</span> <span class="c1"># 1=Number of row  , 2= NUmer of column and #1 Number of plot you are refering to </span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[25]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.axes._subplots.AxesSubplot at 0x1976fc31898&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[26]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">2</span><span class="p">,</span><span class="mi">1</span><span class="p">)</span> <span class="c1"># 1=Number of row  , 2= NUmer of column and #1 Number of plot you are refering to </span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">,</span><span class="s1">&#39;r-&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[26]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x19773201c18&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[28]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">2</span><span class="p">,</span><span class="mi">1</span><span class="p">)</span> <span class="c1"># 1=Number of row  , 2= NUmer of column and #1 Number of plot you are refering to </span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">,</span><span class="s1">&#39;r-&#39;</span><span class="p">)</span>

<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">2</span><span class="p">,</span><span class="mi">2</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">,</span><span class="n">x</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[28]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x197736c5da0&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="object-oriented-method">object oriented method<a class="anchor-link" href="#object-oriented-method">&#182;</a></h1><ul>
<li>figure object and call the method </li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[29]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span> <span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_text output_subarea ">
<pre>&lt;Figure size 432x288 with 0 Axes&gt;</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[32]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span> <span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mf">0.1</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mf">0.8</span><span class="p">,</span><span class="mf">0.8</span><span class="p">])</span>  <span class="c1"># List tabking four argument LEFT BOttom width and height </span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[33]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span> <span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mf">0.1</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mf">0.8</span><span class="p">,</span><span class="mf">0.8</span><span class="p">])</span>  <span class="c1"># List tabking four argument LEFT BOttom width and height </span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[33]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x19774ab3e48&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAX8AAAEJCAYAAAB8Pye7AAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADl0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uIDMuMC4yLCBodHRwOi8vbWF0cGxvdGxpYi5vcmcvOIA7rQAAFypJREFUeJzt3Xl4VfWdx/HPFwhlD1uIyGIURUUQkIBSplotWsfWtXVhlEGxE1yL1U5r7UxpbZ/W6dPiNlMUkU1UoCOMWrAVd1FbSADZooCAskQIsu9ZvvNHrm3EQJZ77j333vN+PU+eJDc3nO+14c3tL+een7m7AADR0ijsAQAAyUf8ASCCiD8ARBDxB4AIIv4AEEHEHwAiiPgDQAQRfwCIIOIPABHUJJkH69ixo+fl5SXzkAAQKUVFRdvcPae2+yU1/nl5eSosLEzmIQEgUszs47rcj2UfAIgg4g8AEUT8ASCCiD8ARBDxB4AIqjX+ZtbNzF43s2IzW2Fmo2O3/9zMNpnZktjbJYkfFwAQhLqc6lku6R53X2RmrSUVmdm82NcedPffJW48AEAi1Bp/dy+RVBL7eI+ZFUvqkujBACBqDpZVqFlW46Qcq15r/maWJ6m/pL/FbrrDzJaa2UQzaxfwbAAQGQfLKnTN4+/pd3/5MCnHq3P8zayVpOck3eXuuyWNk9RDUj9V/T+D3x/l+wrMrNDMCktLSwMYGQAyi7vrZ88v19KNu3Rm1+ykHLNO8TezLFWF/2l3nyVJ7r7F3SvcvVLSE5IG1fS97j7e3fPdPT8np9bLTQBA5Dy7YINmFm7UnRecrIvOOC4px6zL2T4m6UlJxe4+ttrtnavd7UpJy4MfDwAy26JPdmjMC8t1Xs8c3TW0Z9KOW5ezfYZIGi5pmZktid12n6RhZtZPkktaL2lUQiYEgAxVuueQbpu2SMdlN9PD1/VT40aWtGPX5Wyf+ZJqmmhu8OMAQDSUVVTq9mcWaeeBw5p16xC1bdE0qcdP6iWdAQBVfjP3Ay1Yt10PXdtPvY5vk/Tjc3kHAEiy55ds0sR31ummIXm6on84L5si/gCQRMUlu/Xj55ZqUF573XfJ6aHNQfwBIEl27S/TqKeKlN08S/99fX9lNQ4vwaz5A0ASVFa6Rs9YrJJdBzS9YLA6tW4W6jw88weAJHjo1dV648NSjbn0DA04Ifyr4RB/AEiwV1Zu0SOvrtbVA7rq+rO7hz2OJOIPAAm1bts+/WDGEvXpkq1fXtFbVRdNCB/xB4AE2XeoXAVTC5XVpJHG3XBW0i7XXBfEHwASwN31o/9dqo9K9+rRYf3VtV2LsEf6AuIPAAnwxNtrNWdZiX588WkacnLHsMf5EuIPAAF7d802PfDSB7qkz3EqOPeksMepEfEHgABt2nlAdzy7WD1yWum33+2bMr/gPRLxB4CAHCyr0K3TilRWXqnHhg9Qq6+k7utoU3cyAEgj1bdiHD98gHrktAp7pGPimT8ABCCMrRjjQfwBIE5hbcUYD+IPAHEo3XNIt04rUufs5knfijEerPkDQAN9vhXjrgNlmnXroKRvxRgP4g8ADRT2VozxYNkHABogFbZijAfxB4B6SpWtGONB/AGgHlJpK8Z4sOYPAHWUalsxxiM9/8kCgBA89MqqlNqKMR7EHwDqYN7KLXrktTUptRVjPIg/ANRibele3Z2CWzHGg/gDwDHsO1SuUU8VKatJIz02fEBKbcUYD+IPAEdx5FaMXdo2D3ukwBB/ADiKVN+KMR7EHwBqkA5bMcaD+APAEdJlK8Z4EH8AqCadtmKMR63xN7NuZva6mRWb2QozGx27vb2ZzTOz1bH36f2KBwCRV30rxt9f0zflt2KMR12e+ZdLusfdT5d0jqTbzayXpHslverup0h6NfY5AKStSe+sT6utGONRa/zdvcTdF8U+3iOpWFIXSZdLmhK72xRJVyRqSABItJeWleiXc1bqm2fkps1WjPGo15q/meVJ6i/pb5Jy3b1EqvoHQlKnoIcDgGQoXL9do2csUf9ubfXwdf3TZivGeNQ5/mbWStJzku5y9931+L4CMys0s8LS0tKGzAgACbNm6159b2qhurZtrgkjBmbMK3hrU6f4m1mWqsL/tLvPit28xcw6x77eWdLWmr7X3ce7e7675+fk5AQxMwAEYuueg7px0gI1aWSafNMgtW+ZPnvwxqsuZ/uYpCclFbv72GpfekHSiNjHIyQ9H/x4AJAY+w6Va+Tkhfps72FNvHGgundoEfZISVWXE1iHSBouaZmZLYnddp+kByTNNLObJX0i6erEjAgAwSqvqNTtzyzSys27NWFEvs7s2jbskZKu1vi7+3xJR/vtxzeCHQcAEsvd9R//t1xvfFiqX1/ZRxeclhv2SKHgFb4AIuXR19Zo+sINuvOCk/UvGbApS0MRfwCR8cfCDRo7b5WuOquL7r4w88/lPxbiDyAS3lxVqp/MWqavndJRD1x1ZkZerK0+iD+AjLd80y7dNq1Ip+S21h+uP0tNm5A+/gsAyGgbd+zXTZMXKrt5libfNFCtm2WFPVJKIP4AMtbO/Yd146SFOlRWockjBym3TbOwR0oZmXmhagCRd7CsQgVTi/TJZ/s19eZB6pnbOuyRUgrxB5BxKitd9/zxfS1Yv12PDOuvc07qEPZIKYdlHwAZ5zcvFWvO0hLdd8lpuqzv8WGPk5KIP4CMMnH+Oj3x9jrd+NU8/dvXMm/j9aAQfwAZo/qGLP/57V6RP5f/WIg/gIwQxQ1Z4kH8AaS9qG7IEg/iDyCtRXlDlnhwqieAtFV9Q5YZo86J3IYs8SD+ANJSWUWlbnt6kYpL9mjCv0ZzQ5Z4sOwDIO24u/5j9nK9uapUv7qit84/rVPYI6Ud4g8g7Tz62hrNKKzakGXYoOhuyBIP4g8grbAhSzCIP4C0wYYswSH+ANICG7IEi/96AFIeG7IEj/gDSGlsyJIYnOcPIGWxIUviEH8AKamy0nXPzKoNWR5lQ5bAsewDICX9em6x5iyr2pDlUjZkCRzxB5ByJs5fpwnz2ZAlkYg/gJQylw1ZkoL4A0gZL6/4VKOnL9ZZ3duxIUuCEX8AKeHlFZ/q9mcWqdfx2Zp0ExuyJBrxBxC66uF/6uZBasOLuBKO+AMIFeEPB/EHEBrCH55a429mE81sq5ktr3bbz81sk5ktib1dktgxAWQawh+uujzznyzp4hpuf9Dd+8Xe5gY7FoBMRvjDV2v83f0tSduTMAuACCD8qSGeNf87zGxpbFmoXWATAchYhD91NDT+4yT1kNRPUomk3x/tjmZWYGaFZlZYWlrawMMBSHeEP7U0KP7uvsXdK9y9UtITkgYd477j3T3f3fNzcnIaOieANEb4U0+D4m9mnat9eqWk5Ue7L4BoI/ypqdbr+ZvZs5K+LqmjmW2UNEbS182snySXtF7SqATOCCBNEf7UVWv83X1YDTc/mYBZAGQQwp/aeIUvgMAR/tRH/AEEivCnB+IPIDCEP30QfwCBIPzphfgDiBvhTz/EH0BcCH96Iv4AGozwpy/iD6BBCH96I/4A6o3wpz/iD6BeCH9mIP4A6ozwZw7iD6BOCH9mIf4AakX4Mw/xB3BMhD8zEX8AR0X4MxfxB1Ajwp/ZiD+ALyH8mY/4A/iCWYs2Ev4IqHUbRwDR4O56+NXVeuiV1fpqjw56bPgAwp/BiD8AHS6v1L2zlmrWok36zlld9Zur+qhpExYGMhnxByJu14Ey3fJUkd5b+5nuvrCn7rzgZJlZ2GMhwYg/EGEbtu/XyMkLtf6zfRp7TV9ddVbXsEdCkhB/IKKWbtypkZMLdbi8QlNHnq3BPTqEPRKSiPgDEfTyik81evoSdWjVVNMLztbJnVqHPRKSjPgDETPpnXW6/08rdWaXbE0YMVA5rb8S9kgIAfEHIqKi0vWrOSs16Z31uqhXrh6+rr+aN20c9lgICfEHImD/4XKNnr5E81Zu0cghJ+qn3zpdjRtxRk+UEX8gw5XuOaTvTVmopZt2acylvXTTkBPDHgkpgPgDGWzN1j26cdJCfbb3sMYPz9eFvXLDHgkpgvgDGerdj7bplqeK1LRJY80YdY7O7No27JGQQog/kIGeK9qoe2ct1QkdWmrSjQPVrX2LsEdCiiH+QAY58uJs424YoOzmXJwNX0b8gQzBxdlQH7X+ZJjZRDPbambLq93W3szmmdnq2Pt2iR0TwLHsOlCmERMXaNaiTfrB0J763dVnEn4cU11+OiZLuviI2+6V9Kq7nyLp1djnAEKwYft+fXfcuyr8eLvGXtNXo4eewlU5Uata4+/ub0nafsTNl0uaEvt4iqQrAp4LQB0s3bhTV/7hXX26+6CmjBzEVTlRZw1d88919xJJcvcSM+sU4EwA6oCLsyEeCV8UNLMCMys0s8LS0tJEHw6IhEnvrNOoaUXqmdtKs28bQvhRbw2N/xYz6yxJsfdbj3ZHdx/v7vnunp+Tk9PAwwGQqi7O9osXV+gXL67U0NNzNb1gMFflRIM0NP4vSBoR+3iEpOeDGQfA0ew/XK5bphVp0jvrNXLIiXrshgFclRMNVuuav5k9K+nrkjqa2UZJYyQ9IGmmmd0s6RNJVydySCDquDgbglZr/N192FG+9I2AZwFQg88vzrZt7yE9fsMAXXTGcWGPhAzAK3yBFPaFi7MVDFbfblycDcEg/kCK4uJsSCTiD6SYsopKjZ23SuPe+EiDT+qgx4ZzcTYEj/gDKWTjjv36/rOLteiTnbpuYDfdf3lvrtGDhCD+QIp4aVmJfvzcUlW69Miw/rqs7/Fhj4QMRvyBkB0sq9Cv5qzUtL9+or5ds/XIsP46oUPLsMdChiP+QIjWbN2jO55ZrA8+3aOCc0/SDy86lWUeJAXxB0Lg7ppZuEFjXlihlk2baNJNA3X+qVwfEclD/IEk232wTD+dvVwvvr9ZX+3RQQ9d20+d2jQLeyxEDPEHkuj9DTt157OLtWnnAf37N0/VLef1UONGbLyC5CP+QBJUVromzF+r3/75Q+W2aaYZBecoP6992GMhwog/kGDb9h7SPTPf15urSvXNM3L12+/0VXYLXrSFcBF/IIHmr96mH8xcol0HyvTLK3rrhrO7s78uUgLxBxKgrKJSD72ySn944yP1yGmlqSMH6fTObcIeC/g74g8ErPolGq7N76Yxl/VSi6b8VUNq4ScSCBCXaEC6IP5AALhEA9IN8QfixCUakI6IP9BAXKIB6Yz4Aw3AJRqQ7og/UE9cogGZgPgDdcQlGpBJiD9QB1yiAZmG+AO1eGfNNt01g0s0ILMQf+Aoyisq9WDsEg0ndWzJJRqQUYg/UIPikt26b/YyLf5kp67J76qfX3YGl2hARuGnGahm98EyPThvlaa+97Gym2fp4ev66fJ+XcIeCwgc8QdU9YKt2Ys36ddzP9Bn+w7p+rO764cXnaq2LZqGPRqQEMQfkVdcsls/e365Fq7foX7d2mrSjQPVp2t22GMBCUX8EVlHLvH813f66OoB3dSIF2whAog/IoclHoD4I2JY4gGqEH9EAks8wBfFFX8zWy9pj6QKSeXunh/EUEBQWOIBahbEM//z3X1bAH8OECiWeICjY9kHGYclHqB28cbfJb1sZi7pcXcff+QdzKxAUoEkde/ePc7DAUfHEg9Qd/HGf4i7bzazTpLmmdkH7v5W9TvE/kEYL0n5+fke5/GAGrHEA9RPXPF3982x91vNbLakQZLeOvZ3AcFhiQdomAbH38xaSmrk7ntiH18k6f7AJgOOgSUeID7xPPPPlTQ7tqlFE0nPuPufA5kKOAaWeID4NTj+7r5WUt8AZwGOiSUeIDic6omUxxIPEDzij5TGEg+QGMQfKWnVlj167M2P9PySzSzxAAlA/JFSij7ernFvfKRXireqeVZjjRicp+9/42SWeICAEX+Ezt31+odbNe6Nj7Rw/Q61a5Glu4aeohGD89SuJdEHEoH4IzRlFZV68f3NevzNtfpwyx4dn91MYy7tpWsHdlOLpvxoAonE3zAk3f7D5ZqxcIMmvL1Om3YeUM/cVhp7TV9d2vd4ZTVuFPZ4QCQQfyTNjn2HNeW99Zry7nrt2F+mgXntdP/lZ+j8Uzvxi1wgyYg/Em7TzgOa8PZaTV+wQQfKKjT09E665bweys9rH/ZoQGQRfyTM56drvrBksyTpsn7Ha9S5PXTqca1DngwA8UfgCtdv12Nv/uN0zeGDT9D3vnaSurRtHvZoAGKIPwLB6ZpAeiH+iMuRp2t2aduc0zWBNMDfTjQIp2sC6Y34o144XRPIDMQfdcLpmkBmIf44KnfXypLdenL+ui+crnnLeT3UM5fTNYF0RvzxBe6uDz7do7nLSjRnaYnWbtvH6ZpABiL+qDH4jUw656QOGvlPJ+pbfTpzuiaQYYh/RNUW/It7H6eOrb4S9pgAEoT4RwjBB/A54p/hCD6AmhD/DETwAdSG+GcIgg+gPoh/GiP4ABqK+KcZgg8gCMQ/DRB8AEEj/inoYFmFVpbs1rKNu7Rs0y4VfbxD6wg+gAAR/5AdGfrlm3Zp9da9qqh0SVLHVk3Vp0u2bib4AAJE/JOoLqHv3SVbF/bKVe8u2erTJVuds5vJjEslAwgW8U8QQg8glRH/ANQW+g4tm6pPV0IPIHUQ/3oi9AAyQVzxN7OLJT0sqbGkCe7+QCBThaCsolK7D5Rp54Ey7Yq97f784/1l+nj7fkIPIGM0OP5m1ljS/0i6UNJGSQvN7AV3XxnUcPVVVlH593DXFPAjv1b96/sOVxzzzyb0ADJJPM/8B0la4+5rJcnMpku6XFLg8d97qFyzFm2MO+DNsxoru3lW1VuLLHVr3+Ifnx/x1uaIz5s2aRT0wwKA0MQT/y6SNlT7fKOks4+8k5kVSCqQpO7duzfoQAfLKvSz51dIIuAAEIR44l/Teod/6Qb38ZLGS1J+fv6Xvl4X7Vs01cKfDiXgABCQeOK/UVK3ap93lbQ5vnFq1qiRKac1r2wFgKDE8zR6oaRTzOxEM2sq6TpJLwQzFgAgkRr8zN/dy83sDkl/UdWpnhPdfUVgkwEAEiau8/zdfa6kuQHNAgBIEn57CgARRPwBIIKIPwBEEPEHgAgi/gAQQebeoBfdNuxgZqWSPo7jj+goaVtA46STqD5uicfOY4+eeB/7Ce6eU9udkhr/eJlZobvnhz1HskX1cUs8dh579CTrsbPsAwARRPwBIILSLf7jwx4gJFF93BKPPap47AmWVmv+AIBgpNszfwBAANIi/mZ2sZl9aGZrzOzesOdJFjObaGZbzWx52LMkm5l1M7PXzazYzFaY2eiwZ0oWM2tmZgvM7P3YY/9F2DMlk5k1NrPFZvansGdJJjNbb2bLzGyJmRUm/HipvuwT2yh+laptFC9pWJgbxSeLmZ0raa+kqe7eO+x5ksnMOkvq7O6LzKy1pCJJV0Tkf3eT1NLd95pZlqT5kka7+19DHi0pzOxuSfmS2rj7t8OeJ1nMbL2kfHdPyusb0uGZ/983inf3w5I+3yg+47n7W5K2hz1HGNy9xN0XxT7eI6lYVftGZzyvsjf2aVbsLbWfpQXEzLpK+pakCWHPkunSIf41bRQfiQigipnlSeov6W/hTpI8saWPJZK2Sprn7lF57A9J+pGkyrAHCYFLetnMisysINEHS4f412mjeGQmM2sl6TlJd7n77rDnSRZ3r3D3fqraG3uQmWX8sp+ZfVvSVncvCnuWkAxx97Mk/bOk22PLvgmTDvFP2kbxSC2x9e7nJD3t7rPCnicM7r5T0huSLg55lGQYIumy2Nr3dEkXmNm0cEdKHnffHHu/VdJsVS15J0w6xJ+N4iMo9kvPJyUVu/vYsOdJJjPLMbO2sY+bSxoq6YNwp0o8d/+Ju3d19zxV/T1/zd1vCHmspDCzlrETG2RmLSVdJCmhZ/mlfPzdvVzS5xvFF0uaGZWN4s3sWUnvSTrVzDaa2c1hz5REQyQNV9WzvyWxt0vCHipJOkt63cyWqurJzzx3j9RpjxGUK2m+mb0vaYGkOe7+50QeMOVP9QQABC/ln/kDAIJH/AEggog/AEQQ8QeACCL+ABBBxB8AIoj4A0AEEX8AiKD/B4aRDHimD99eAAAAAElFTkSuQmCC
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Setting-lable">Setting lable<a class="anchor-link" href="#Setting-lable">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[36]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span> <span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mf">0.1</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mf">0.8</span><span class="p">,</span><span class="mf">0.8</span><span class="p">])</span>  <span class="c1"># List tabking four argument LEFT BOttom width and height </span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">)</span>
<span class="n">axes</span><span class="o">.</span><span class="n">set_xlabel</span><span class="p">(</span><span class="s2">&quot;X lable &quot;</span><span class="p">)</span>
<span class="n">axes</span><span class="o">.</span><span class="n">set_ylabel</span><span class="p">(</span><span class="s2">&quot;Y Lable &quot;</span><span class="p">)</span>
<span class="n">axes</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s2">&quot;Title of graph&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[36]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0.5, 1.0, &#39;Title of graph&#39;)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[54]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span> <span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes1</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mf">0.1</span><span class="p">,</span><span class="mf">0.1</span><span class="p">,</span><span class="mf">0.8</span><span class="p">,</span><span class="mf">0.8</span><span class="p">])</span>  <span class="c1">#LEFT BOttom width and height </span>
<span class="n">axes2</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mf">0.1</span><span class="p">,</span><span class="mf">0.6</span><span class="p">,</span><span class="mf">0.4</span><span class="p">,</span><span class="mf">0.3</span><span class="p">])</span>  <span class="c1">#LEFT BOttom width and height </span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[70]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span> <span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes1</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mf">0.1</span><span class="p">,</span><span class="mf">0.1</span><span class="p">,</span><span class="mf">0.8</span><span class="p">,</span><span class="mf">0.8</span><span class="p">])</span>  <span class="c1">#LEFT BOttom width and height </span>
<span class="n">axes2</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mf">0.7</span><span class="p">,</span><span class="mf">0.1</span><span class="p">,</span><span class="mf">0.2</span><span class="p">,</span><span class="mf">0.2</span><span class="p">])</span>  <span class="c1">#LEFT BOttom width and height </span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[75]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span> <span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes1</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mf">0.1</span><span class="p">,</span><span class="mf">0.1</span><span class="p">,</span><span class="mf">0.8</span><span class="p">,</span><span class="mf">0.8</span><span class="p">])</span>  <span class="c1">#LEFT BOttom width and height </span>
<span class="n">axes2</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mf">0.2</span><span class="p">,</span><span class="mf">0.5</span><span class="p">,</span><span class="mf">0.4</span><span class="p">,</span><span class="mf">0.3</span><span class="p">])</span>  <span class="c1">#LEFT BOttom width and height </span>

<span class="n">axes1</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">)</span>
<span class="n">axes2</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">,</span><span class="n">x</span><span class="p">)</span>

<span class="n">axes1</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s2">&quot;Larger Plot&quot;</span><span class="p">)</span>
<span class="n">axes2</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s2">&quot;Smaller Plot&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[75]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0.5, 1.0, &#39;Smaller Plot&#39;)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Subplot-using-Object-oriented-method">Subplot using Object oriented method<a class="anchor-link" href="#Subplot-using-Object-oriented-method">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[79]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="p">,</span><span class="n">axes</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="n">nrows</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">ncols</span><span class="o">=</span><span class="mi">2</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[80]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="p">,</span><span class="n">axes</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="n">nrows</span><span class="o">=</span><span class="mi">3</span><span class="p">,</span><span class="n">ncols</span><span class="o">=</span><span class="mi">3</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Tight-layout">Tight layout<a class="anchor-link" href="#Tight-layout">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[81]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="p">,</span><span class="n">axes</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="n">nrows</span><span class="o">=</span><span class="mi">3</span><span class="p">,</span><span class="n">ncols</span><span class="o">=</span><span class="mi">3</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">tight_layout</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[90]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">axes</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[90]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([[&lt;matplotlib.axes._subplots.AxesSubplot object at 0x00000197783E9358&gt;,
        &lt;matplotlib.axes._subplots.AxesSubplot object at 0x000001977841D6A0&gt;,
        &lt;matplotlib.axes._subplots.AxesSubplot object at 0x00000197783F8908&gt;],
       [&lt;matplotlib.axes._subplots.AxesSubplot object at 0x00000197783D5AC8&gt;,
        &lt;matplotlib.axes._subplots.AxesSubplot object at 0x000001977846A390&gt;,
        &lt;matplotlib.axes._subplots.AxesSubplot object at 0x00000197784915C0&gt;],
       [&lt;matplotlib.axes._subplots.AxesSubplot object at 0x00000197784B97F0&gt;,
        &lt;matplotlib.axes._subplots.AxesSubplot object at 0x00000197784E29E8&gt;,
        &lt;matplotlib.axes._subplots.AxesSubplot object at 0x000001977850AC50&gt;]], dtype=object)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[97]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">type</span><span class="p">(</span><span class="n">axes</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[97]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>numpy.ndarray</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[103]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="p">,</span><span class="n">axes</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="n">nrows</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">ncols</span><span class="o">=</span><span class="mi">3</span><span class="p">)</span>
<span class="k">for</span> <span class="n">curr_axes</span> <span class="ow">in</span>  <span class="n">axes</span><span class="p">:</span>
    <span class="n">curr_axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[104]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="p">,</span><span class="n">axes</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="n">nrows</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">ncols</span><span class="o">=</span><span class="mi">3</span><span class="p">)</span>
<span class="n">axes</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[104]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x1977524e208&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[107]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="p">,</span><span class="n">axes</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="n">nrows</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">ncols</span><span class="o">=</span><span class="mi">3</span><span class="p">)</span>
<span class="n">axes</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">)</span>
<span class="n">axes</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s2">&quot;Axxess 1&quot;</span><span class="p">)</span>

<span class="n">axes</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s2">&quot;Empty&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[107]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0.5, 1.0, &#39;Empty&#39;)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAXwAAAEICAYAAABcVE8dAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADl0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uIDMuMC4yLCBodHRwOi8vbWF0cGxvdGxpYi5vcmcvOIA7rQAAIABJREFUeJzt3Xl8VfWd//HXB0IAQQjIIpKw7+ACBnSqtVrpoGmLXaYd6Wh16tT2NzjTTjvTsZ2O7aOdPqazdIe2Y6ujtlZrq63YAo6yjINVEkCQJWoCCWRhSQj7lu3z++OepJeYkJvk3py7vJ+Px31wz3JPPufe+31z7vds5u6IiEj66xN2ASIi0jsU+CIiGUKBLyKSIRT4IiIZQoEvIpIhFPgiIhlCgS8ikiEyMvDNrNzMzpjZyajHsgT8HTezKfFebqYzs/VmdsTM+oddSyzMbIyZrTCz6uA7MSHsmiQzZWTgB97v7oOjHveFXZB0LgjLdwIOLA61mNg1A6uBD4ddiGS2TA78tzGzu83sZTP7jpkdNbM9ZvaOYHyFmR0ys7ui5n/EzH5sZi+Y2Qkz+18zGx9MeymYbVvwC+LPzWyHmb0/6vX9zKzWzK7q5VVNZR8HXgUeAaI/i2wz22pmfxMM9w0+yweC4ZVm9q2o+X9pZg9HDX/CzIqDXw7PR32OFnwfDpnZMTN73czmBNMKzGxX8NlXmdnft1ewux909x8CRXF/N0S6wt0z7gGUAwvbGX830Aj8JdAX+BdgH7Ac6A/8KXACGBzM/0gwfEMw/XvAhqjlOTAlavgLwC+jhm8Dtof9fqTSAygF/hq4GmgARkdNmwMcAWYC/0TkP4a+wbRLgUPAu4G/APYAFwfTPhAsdyaQBXwZ+EMwbRGwGcgBLJhnTDBtP/DO4PkwYF4ntWcF34kJYb+PemTmI/QCQlnpSOCfBI5GPT4ZBH5J1HyXBw00OlQOA1cFzx8BnoyaNhhoAvKC4baBf1nwH8SQYPjXwBfCfj9S5QFcH4T8iGD4DeDv2szz+WD8EWBqm2kfAiqAWuD6qPGrgHuihvsAp4HxwX8QbwHXAn3aLG8f8KmWzzOG+hX4eoT6yOQunQ+4e07U4yfB+INR85yByE/yNuMGRw1XtDxx95NAHZFgfxt3rwZeBj5sZjnArcDjPV6TzHEX8D/uXhsM/4Kobp3Ao8AEYKW7l7SZ9jsiv9zedPcNUePHA98LuvGOEvkMDRjr7muBZUR+5R00swfNbEjwug8DBcDeoDvvT+KyliIJksmBHy95LU/MbDAwHKi+wPyPAncAHwFecfeqxJaXHsxsIPBR4F1mdsDMDgB/B1xpZldGzfpDIsG+yMyub7OYbwDFwBgzWxI1vgL4VJsNgIHu/gcAd/++u18NzAamAf8QjC9y99uAUcBvgafivd4i8aTA77kCM7vezLKBrwMb3b1lq/8gMKnN/L8F5gGfAR7rvTJT3geIdJfNAq4KHjOB/yOyIxczu5NI3/7dwN8Cjwb/CWNmNxDZN/Px4PEDMxsbLPvHwBfNbHYw71Az+0jwfL6ZXWNm/YBTwFmgKdhJ/BdmNtTdG4DjQX3tMrMBRPbzAPQPhkV6VSYH/nNtjsP/TTeX8wvgK0S6Aa4mskOwxVeJhM5RM/sogLufAZ4GJgLPdLv6zHMX8N/uvs/dD7Q8iHS3/IWZjQO+C3zc3U+6+y+ATcB3gi6Yx4D73L0q6M55CPhvMzN3/w3wb8CTZnYc2EGkuw1gCPATIvsE9hLZh/OfwbQ7gfLgNZ8m8sutI2eI7DeCyD6GMz1+R0S6yNx1A5TuMrNHgEp3/3IXX/cAMM3dLxQQIiJxlRV2AZnGzIYD9xDZOhQR6TWddumY2cPBSSc7OphuZvZ9MysNTkqZF/8y04OZfZLIDsJV7v5SZ/OLdIfarHSk0y6dYGfXSeAxd5/TzvQC4G+IHJ52DfA9d78mAbWKSAzUZqUjnW7hB1uidReY5TYiXyx391eBHDMbE68CRaRr1GalI/Howx9L1MlHQGUwbn/bGc3sXuBegEGDBl09Y8aMOPx56anNmzfXuvvIeCxrxIgRPmHChHgsSnpgzpw57Nixo6PDRGNqs2qvyakn7TUegW/tjGu3n8jdHwQeBMjPz/dNmzbF4c9LT5nZ3ngta8KECehzDV95eTkTJ05s6GByTG1W7TU59aS9xuM4/EqizjYFcrnwmaYiEi612QwVj8BfAXw82PN/LXDM3d/WnSMiSUNtNkN12qVjZk8ANwIjzKySyFml/QDc/cfASiJ7+0uJXGHwLxNVrIh0bsmSJaxfvx4il3BQm5VWnQa+uy/pZLoDS+NWkYj0yBNPPAGAmW1x9/y209VmM1cmX0tHRCSjKPAFoJ+ZrQtu8bfTzD4DYGZfDW7dtzV4FIRdqIh0n66lIy0+7+5bzOxiYLOZvRCM/467/+eFXigiqUFb+ALQ4O5bANz9BJGbhIy98EskWfxhdy0/XF/K2YYOL8cvAijwpQ0zmwDMBTYGo+4LLrD1sJkN6+A195rZJjPbVFNT00uVSovntlXz4/W7ye6r5iwXpm+ItAruDvU08Fl3Pw78CJhM5O5S+4Fvtfc6d3/Q3fPdPX/kyLhcoUG6oLCsjvwJw+nTp70TaEX+SIEvAAS38HsaeNzdn4HIzdvdvcndm4nc9WlBmDXK2x0+eY7dNaeYP2F42KVIClDgS4uHgGJ3/3bLiDZXUPwgkVv/SRIpKj8CwIKJ7fa2iZxHR+kIwGAid+DabmZbg3FfApaY2VVELqxVDnwqnPKkI0XldfTP6sPlY3PCLkVSgAJfAE66e3sdwCt7vRLpkqLyOq7KyyE7Sz/WpXP6loikqFPnGtlZfZwFE9V/L7FR4IukqC37jtDU7NphKzFT4IukqKKyOvoYzBuvHbYSGwW+SIoqLK9j9mVDGdxfu+IkNgp8kRRU39jMa/uOqjtHukSBL5KCtlcd41xjs46/ly5R4IukoKLyOgDytYUvXaDAF0lBRWV1TBo5iBGD+4ddiqQQBb5IimludjbtPcICbd1LFynwRVLMW4dOcOxMg3bYSpcp8EVSTFFZpP9eZ9hKVynwRVJMYfkRLh0ygNxhA8MuRVKMAl8khbg7RWV1zJ84HDPd8ES6RoEvkkIqj5zhwPGzLJig4++l6xT4IimkMOi/n6/+e+kGBb5ICikqr2PowH5MG3Vx2KVIClLgi6SQwvI68scP0w3LpVsU+CIpovbkOfbUnFJ3jnSbAl8kRWwKrp+jE66kuxT4IimisOwIA/r14fKxQ8MuRVKUAl8kRRSWH9YNy6VH9M0RSQEnzjawq/q4LpgmPaLAF0kBW/Ydpdl1/L30jAJfJAUUldXRt48xb5zOsJXuU+CLpIDIDcuHMEg3LJceiCnwzewWM3vTzErN7P52po8zs3Vm9pqZvW5mBfEvVSQznWtsYmtF7DcsX716NdOnTweYo/Yq0ToNfDPrCywHbgVmAUvMbFab2b4MPOXuc4HbgR/Gu1CRTLW98hj1jc0xBX5TUxNLly5l1apVADtRe5UosWzhLwBK3X2Pu9cDTwK3tZnHgSHB86FAdfxKFMlsha0nXHXef19YWMiUKVOYNGkSRNql2qu0iiXwxwIVUcOVwbhoXwXuMLNKYCXwN+0tyMzuNbNNZrappqamG+WKZJ6isjomjxzEJTHcsLyqqoq8vLzoUWqv0iqWwG/vKk3eZngJ8Ii75wIFwM/M7G3LdvcH3T3f3fNHjhzZ9WpFMkxTyw3LYzwc071t04yMbjOs9pqhYgn8SiB6kyGXt/8EvAd4CsDdXwEGACPiUaBIJnvzwAlOnG2MeYdtbm4uFRUV541C7VUCsQR+ETDVzCaaWTaRnTwr2syzD7gZwMxmEvkC6Tdg6ugXHLVRbGY7zewzAGY23MxeMLOS4F8dBN7Lirp4wbT58+dTUlJCWVkZRH6dq71Kq04D390bgfuA54FiInv3d5rZ18xscTDb54FPmtk24Angbu/gt6Ukrc+7+0zgWmBpcGTH/cAad58KrAmGpRe9XFpL3vCB5A2/KKb5s7KyWLZsGYsWLQKYjdqrRInpLA53X0lk5070uAeinu8CrotvadKLGtx9C4C7nzCzYiI7+m4DbgzmeRRYD/xjGAVmosamZl7Zc5j3XTGmS68rKCigoKAAM9vh7t8AtVeJ0Jm2ch4zmwDMBTYCo919P0Dw76gOXqOjORJge9UxTpxt5Lop6l6X+FDgSyszGww8DXzW3Y/H+jodzZEYL5fWAvCOyQp8iQ8FvgBgZv2IhP3j7v5MMPqgmY0Jpo8BDoVVXyb6v5JaZl82hOGDssMuRdKEAl9aPAQUu/u3o8atAO4Knt8FPNvrVWWo0/WNbNl3hOunaute4keX3hOAwcCdwHYz2xqM+xLwTeApM7uHyKF8HwmpvoxTWFZHQ5NzvfrvJY4U+AJw0t3bO6MaguO1pXe9XFpLdlYf3bBc4kpdOiJJaEPpYfLHD2NAv75hlyJpRIEvkmRqTpyjeP9xHY4pcafAF0kyf9gdORxT/fcSbwp8kSTzcmktQwf2Y87YoWGXImlGgS+SRNydDSW1vGPyJfTt09F+dJHuUeCLJJHyw6epPnZW/feSEAp8kSSyoVT995I4CnyRJLKhpIaxOQMZf0lsl0MW6QoFvkiSaGp2/rD7MO+cOgIz9d9L/CnwRZKELocsiabAF0kSf7wc8iUhVyLpSoEvkiQ2lNQya8wQLhncP+xSJE0p8EWSwJn6Jjbv1eWQJbEU+CJJoLC8jvqmZh2OKQmlwBdJAi+X1pLdV5dDlsRS4IskgQ0ltVw9fhgDs3U5ZEkcBb5IyA6fPMeu/cfVfy8Jp8AXCdnLuw8D6Ph7STgFvkjIXi6pZciALC7X5ZAlwRT4IiFydzaU1vKOySN0OWRJOAW+SIj2Hj5N1dEzXKf+e+kFCnyREOlyyNKbFPgiIdpQUsvYnIFM0OWQpRco8EVCErkcci3XT9HlkKV3KPBFQrKj6hjHzzaq/156jQJfJCQvvVWDmS6HLL1HgS8SkhffOMSVuTmM0OWQpZco8EVCcOj4WbZVHGXhzFFhlyIZJKbAN7NbzOxNMys1s/s7mOejZrbLzHaa2S/iW6ZIeln7xiEAbp45Ou7LXr16NdOnTweYo/Yq0bI6m8HM+gLLgfcAlUCRma1w911R80wFvghc5+5HzEybLSIX8GLxIcbmDGTGpRfHdblNTU0sXbqUF154gcmTJ+8Elqi9SotYtvAXAKXuvsfd64EngdvazPNJYLm7HwFw90PxLVMSzcweNrNDZrYjatxXzazKzLYGj4Iwa0wXZxua2FBaw8KZo+J+OGZhYSFTpkxh0qRJAI7aq0SJJfDHAhVRw5XBuGjTgGlm9rKZvWpmt7S3IDO718w2mdmmmpqa7lUsifII0N7n9h13vyp4rOzlmtLSy6W1nG1oTkh3TlVVFXl5edGj1F6lVSyB394miLcZzgKmAjcCS4CfmlnO217k/qC757t7/siRI7taqySQu78E1IVdRyZ4sfgQg7L7cs2k+N/dyr1t04yMbjOs9pqhYgn8SiB6kyEXqG5nnmfdvcHdy4A3iXyhJPXdZ2avB10+w9qbQVuCsWtudta+cZB3TR9J/6z4390qNzeXioqK80ah9iqBWAK/CJhqZhPNLBu4HVjRZp7fAjcBmNkIIj8Z98SzUAnFj4DJwFXAfuBb7c2kLcHY7ag+xsHj57h5Rvy7cwDmz59PSUkJZWVlEPl1rvYqrToNfHdvBO4DngeKgafcfaeZfc3MFgezPQ8cNrNdwDrgH9z9cKKKlt7h7gfdvcndm4GfENmBLz3wYvEh+hjcNCMxB8ZkZWWxbNkyFi1aBDAbtVeJ0ulhmQDBzrqVbcY9EPXcgc8FD0kTZjbG3fcHgx8EdlxofuncmuKDXD1+GMMHZSfsbxQUFFBQUICZ7XD3b4Daq0TEFPiS/szsCSI78UaYWSXwFeBGM7uKyE6/cuBToRWYBqqPnmFn9XHuv3VG2KVIhlLgCwDuvqSd0Q/1eiFpbE1wdq0upyBh0bV0RHrJmuKDjL/kIiaPHBx2KZKhFPgiveDUuUb+UHqYhTNH62YnEhoFvkgv+L+SWuqbmrlZ3TkSIgW+SC9YU3yQiwdkMX9C/M+uFYmVAl8kwZqanbVvHOLG6aPo11dNTsKjb59Igm2tOMrhU/U6OkdCp8AXSbA1xQfp28e4cZoCX8KlwBdJsDXFh5g/YRhDL+oXdimS4RT4IglUUXeaNw+eYGECrn0v0lUKfJEEerH4IJCYe9eKdJUCXySB1hQfYvLIQUwcMSjsUkQU+CKJcvxsA6/uOazuHEkaCnyRBHnprRoam13dOZI0FPgiCbKm+BDDLurHvHFvu12sSCgU+CIJ0NjUzLo3D3HT9FFk6exaSRL6JookwOa9Rzh6ukHdOZJUFPgiCbBy+36ys/pww7QRYZci0kqBLxJnjU3N/H77fm6eMYqLB+jsWkkeCnyROHtlz2FqT9az+MrLwi5F5DwKfJE4e3ZrNYP7Z3HTDF0sTZKLAl8kjs42NPH8jgMsmn0pA/r1DbsckfMo8EXiaP2bNZw418jiq9SdI8lHgS8SR89tq+aSQdlcN/mSsEsReRsFvkicnDzXyIvFBym4fIxOtpKkpG+lSJy8sOsA5xqb1Z0jSUuBLxInz26tZmzOQK4eNyzsUkTapcAXiYO6U/VsKKnlfVeOoU8fC7sckXYp8EXiYOX2/TQ2u062kqSmwBeJgxXbqpk8chCzxgwJuxSRDinwRXpo/7EzFJXXsfjKsZipO0eSlwJfpId+t20/7ujoHEl6CnwBwMweNrNDZrYjatxwM3vBzEqCf3X4STtWbKvmityhulG5JD0FvrR4BLilzbj7gTXuPhVYEwxLlD01J9ledUw7ayUlxBT4ZnaLmb1pZqVm1mGjN7M/MzM3s/z4lSi9wd1fAurajL4NeDR4/ijwgV4tKgWs2FaNGbzviuQJ/NWrVzN9+nSAOWqvEq3TwDezvsBy4FZgFrDEzGa1M9/FwN8CG+NdpIRmtLvvBwj+bfd6v2Z2r5ltMrNNNTU1vVpgmNydFduqWTBhOJcOHRB2OQA0NTWxdOlSVq1aBbATtVeJEssW/gKg1N33uHs98CSRLb+2vg78O3A2jvVJCnD3B909393zR44cGXY5vWZn9XH21JzitqvGhl1Kq8LCQqZMmcKkSZMAHLVXiRJL4I8FKqKGK4NxrcxsLpDn7r+70IIydUswhR00szEAwb+HQq4nqTy3rZqsPsatcy4Nu5RWVVVV5OXlRY9Se5VWsQR+ewcWe+tEsz7Ad4DPd7agTN0STGErgLuC53cBz4ZYS1Jpbnae21bNDdNGMmxQdtjltHL3dke3PFF7zWyxBH4lEL3JkAtURw1fDMwB1ptZOXAtsEI7glKLmT0BvAJMN7NKM7sH+CbwHjMrAd4TDAuwae8Rqo+dTbqjc3Jzc6moqDhvFGqvEsiKYZ4iYKqZTQSqgNuBj7VMdPdjwIiWYTNbD/y9u2+Kb6mSSO6+pINJN/dqISlixbYqBvTrw3tmjQ67lPPMnz+fkpISysrKIPLrXO1VWnW6he/ujcB9wPNAMfCUu+80s6+Z2eJEFyiSbBqamlm5/QALZ45mUP9Ytpl6T1ZWFsuWLWPRokUAs1F7lSgxfVvdfSWwss24BzqY98aelyWSvDaU1FJ3qj7punNaFBQUUFBQgJntcPdvgNqrROhMW5EuenzjPkYMzubG6e2eliCStBT4Il1QdfQMa984yJ/PzyM7S81HUou+sSJd8MTGfQAsWTAu5EpEuk6BLxKj+sZmnizax7tnjCJ32EVhlyPSZQp8kRg9v/MAtSfruePa8WGXItItCnyRGP381b2MG34RN0zVWaeSmhT4IjF46+AJNpbV8bFrxtGnj25jKKlJgS8Sg8df3Ut2Vh8+mp/X+cwiSUqBL9KJU+caeXpLFe+9fAzDk+hCaSJdpcAX6cSzW6s5ea5RO2sl5SnwRS7A3fn5q3uZOWYI88blhF2OSI8o8EUuYMu+o+zaf5w7rh2HmXbWSmpT4ItcwOOv7mVw/yw+kES3MRTpLgW+SAfqTtXzu9f386F5Y5PuMsgi3aHAF+nArzZVUN/UrJ21kjYU+CLtaG52Ht+4jwUThzNt9MVhlyMSFwp8kXa8VFLDvrrT3Kmte0kjCnyRdvz81X2MGNyfRbMvDbsUkbhR4Iu08cebnOTqJieSVvRtFmlDNzmRdKXAF4kSuclJhW5yImlJgS8S5blt1dSePKdDMSUtKfBFAo1NzfxgbQmzLxvCu6bpJieSfhT4IoHfvFZF+eHTfHbhNF03R9KSAl8EaGhq5gdrS7l87FAWzhwVdjkiCaHAFwF+s6WKfXWn+ezCqdq6l7SlwJeM19DUzA/WlXBF7lDePUNb95K+FPiS8Z7ZUklF3Rlt3Uva0zVfpVNmVg6cAJqARnfPD7ei+KlvjPTdX5mXw03TtXUv6U2BL7G6yd1rwy4i3p7eUknlkTN8/QNztHUvaU9dOpKx6hubWba2lKvycrhRx91LBlDgSywc+B8z22xm97adaGb3mtkmM9tUU1MTQnnd86vNFVQdVd+9ZA4FvsTiOnefB9wKLDWzG6InuvuD7p7v7vkjR6bGlnJ9YzPL15Yyd1yOzqqVjKHAl065e3Xw7yHgN8CCcCvquac2VVB97Cx/p7NqJYPEFPhmdouZvWlmpWZ2fzvTP2dmu8zsdTNbY2a68lSaMLNBZnZxy3PgT4Ed4VbVM+cam1i+rpSrxw/jnVNHhF1O3K1evZrp06cDzFF7lWidBr6Z9QWWE/k5PwtYYmaz2sz2GpDv7lcAvwb+Pd6FSmhGAxvMbBtQCPze3VeHXFOPPFVUwf403bpvampi6dKlrFq1CmAnaq8SJZbDMhcApe6+B8DMngRuA3a1zODu66LmfxW4I55FSniCz/3KsOuIl7MNTSxft5v5E4Zx3ZRLwi4n7goLC5kyZQqTJk2CyM52tVdpFUuXzligImq4MhjXkXuAVe1NSNWjOSR9/LKoggPHz6btFTGrqqrIy8uLHqX2Kq1iCfz2WoW3O6PZHUA+8B/tTU/FozkkfZxtaOKH60tZMGE475icflv3AO7tNk21VwFi69KpBKI3GXKB6rYzmdlC4J+Ad7n7ufiUJxI/y9eVcvD4Ob7753PTcuseIDc3l4qKivNGofYqgVi28IuAqWY20cyygduBFdEzmNlc4L+AxcGheyJJpXj/cX60fjcfmjeWP0nTrXuA+fPnU1JSQllZGUR+nau9SqtOA9/dG4H7gOeBYuApd99pZl8zs8XBbP8BDAZ+ZWZbzWxFB4sT6XWNTc3849OvM3RgP/75vW0PWEkvWVlZLFu2jEWLFgHMRu1VosR08TR3XwmsbDPugajnC+Ncl0jcPPxyGa9XHmPZx+YybFB22OUkXEFBAQUFBZjZDnf/Bqi9SoTOtJW0Vl57im+/8BYLZ47mvZePCbsckVAp8CVtuTtffGY7/fr04V90+WMRBb6kr18WVfDKnsN86b0zuXTogLDLEQmdAl/S0oFjZ/nG74u5dtJwbp+f1/kLRDKAAl/Sjrvzz8/uoL6pmW9+6Ap15YgEFPiSdlZuP8ALuw7yufdMY8KIQWGXI5I0FPiSVo6cqucrK3Zw+dih3HP9xLDLEUkquom5pJWv/34XR0838NgnriGrr7ZnRKKpRUja+N+3anhmSxWfftdkZl02JOxyRJKOAl/SwrEzDXzpme1MHjmI+949JexyRJKSunQk5Z1taOKTj23i0ImzPHnvtQzo1zfskkSSkgJfUlpTs/OZJ1+jsKyO7y+Zy9Xjh4ddkkjSUpeOpCx358u/3cHzOw/ywPtmsfjKy8IuSSSpKfAlZX33xRKeKNzH/7txMp/QIZginVLgS0r62at7+d6aEj5ydS5fWDQ97HJEUoICX1LOyu37eeDZHdw8YxT/+qHLdekEkRgp8CWlvLL7MJ99citz83JY9rF5OrlKpAvUWiRl7Ko+zr2PbWLcJRfx8N3zGZitwy9FukKBLymhou40d/13IYMHZPHYJxaQc1H636pQJN4U+JL03jhwnDsf2kh9YzOPfWIBl+UMDLskkZSkE68kaTU0NfOj9bv5wdoShg7sx8N3z2fq6IvDLkskZSnwJSntrD7GP/zqdXbtP87iKy/jq4tnM3yQunFEekKBL0mlvrGZ5etKWb6ulJyLsvmvO69m0exLwy5LJC0o8CVp7Kg6xt//ahtvHDjBB+eO5Svvn6WdsyJxpMCX0J1rbGLZ2lJ+uH43lwzK5qcfz2fhrNFhlyWSdhT40ikzuwX4HtAX+Km7f7Mny3N3Ko+cYcu+I2zZe4T/fauG8sOn+fC8XB543yyGXtQvLnWLyPkU+HJBZtYXWA68B6gEisxshbvvinUZp+sbeb3yGFv2HeG1fUd5bd8Rak/WA3BRdl+uzM3hK++fzU0zRiVkHUQkQoEvnVkAlLr7HgAzexK4Deg08I+cqueOhzbyxoETNDU7AJNGDOJd00Yxd1wO88YNY9rowbo8gkgvUeBLZ8YCFVHDlcA10TOY2b3AvQDjxo1rHZ9zUT9yhw3k5hmjmDtuGFfl5TBMh1aKhEaBL51p71KUft6A+4PAgwD5+fmt08yM/7ozP7HViUjM9FtaOlMJ5EUN5wLVIdUiIj2gwJfOFAFTzWyimWUDtwMrQq5JRLpBXTpyQe7eaGb3Ac8TOSzzYXffGXJZItINCnzplLuvBFaGXYeI9Iy6dEREMkRMgW9mt5jZm2ZWamb3tzO9v5n9Mpi+0cwmxLtQEYnN6tWrmT59OsActVeJ1mngR51peSswC1hiZrPazHYPcMTdpwDfAf4t3oWKSOeamppYunQpq1atAtiJ2qtEiWULv/VMS3evB1rOtIx2G/Bo8PzXwM1m1t7x2yKSQIWFhUyZMoVJkyZB5HwJtVdpFctO207PtIyeJziq4xhwCVAbPVP0GZnAOTPb0Z2ik8gI2qxjipoerwVt3ry51sz2thmdbO9TMtUT71qGAUOCz2A8aq9tJdNn313dbq+xBH6nZ1rGOM95Z2Sa2SZ3T+nTMNNhHSDpc37BAAADQElEQVSyHvFalruPbG/5yfQ+JVM98a7FzD4CLHL3vwqG70TttVU6rEdP2mssXTqxnGnZOo+ZZQFDgbruFiUi3ab2Kh2KJfBjOdNyBXBX8PzPgLXu/rYtBhFJOLVX6VCnXTodnWlpZl8DNrn7CuAh4GdmVkpkS+H2GP72gz2oO1mkwzpA4tcj2d6nZKonrrWovXYqHdaj2+tg+o9dRCQz6ExbEZEMocAXEckQCQ/8dLgsQwzrcLeZ1ZjZ1uDxV2HUeSFm9rCZHeroWGqL+H6wjq+b2bw4/M0Lvm+9yczyzGydmRWb2U4z+0yY9bQws75m9pqZ/S7sWkDtNVkkrL26e8IeRHYa7QYmAdnANmBWm3n+Gvhx8Px24JeJrClB63A3sCzsWjtZjxuAecCODqYXAKuIHKN9LbAx0e9bL6//GGBe8Pxi4K0w64mq63PAL4DfJUEtaq9J8khUe030Fn46XJYhlnVIeu7+Ehc+1vo24DGPeBXIMbMxPfiTSfW+uft+d98SPD8BFBM54zQ0ZpYLvBf4aZh1RFF7TRKJaq+JDvz2LsvQtpGdd5o30HKad7KIZR0APhz8tPq1meW1Mz3ZxbqeYS0vboJuiLnAxnAr4bvAF4DmkOtoofaaOrrVvhId+HG7LEOIYqnvOWCCu18BvMgft4BSSbw/h6T8XM1sMPA08Fl3Px5iHe8DDrn75rBqaIfaa+ro1ueQ6MBPh9O8O10Hdz/s7ueCwZ8AV/dSbfEU75uVJ93Nz82sH5Gwf9zdnwmzFuA6YLGZlRPpdni3mf083JLUXlNIt9pXogM/HU7z7nQd2vSdLSbSP5xqVgAfD/b+Xwscc/f9PVheUt38POhnfggodvdvh1VHC3f/orvnuvsEIu/NWne/I+Sy1F5TR/faay/sbS4gckTEbuCfgnFfAxYHzwcAvwJKgUJgUth7yLuxDv9K5GYT24B1wIywa25nHZ4A9gMNRLYO7gE+DXw6mG5EbnSzG9gO5CfifQtx/a8n8pP3dWBr8CgI+3MJaruRJDhKp6PPTO01lHVISHvVpRVERDKEzrQVEckQCnwRkQyhwBcRyRAKfBGRDKHAFxHJEAp8EZEMocAXEckQ/x9JkaHp1FyEtwAAAABJRU5ErkJggg==
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="figure-Size-,-aspect-ratio-and-DPI-(Dots-Per-Inch)">figure Size , aspect ratio and DPI (Dots Per Inch)<a class="anchor-link" href="#figure-Size-,-aspect-ratio-and-DPI-(Dots-Per-Inch)">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[114]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">8</span><span class="p">,</span><span class="mi">2</span><span class="p">))</span>  
<span class="n">ax</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">])</span>
<span class="n">ax</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[114]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x19774f6ebe0&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[135]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="p">,</span><span class="n">axes</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="n">nrows</span><span class="o">=</span><span class="mi">2</span><span class="p">,</span><span class="n">ncols</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">8</span><span class="p">,</span><span class="mi">2</span><span class="p">))</span>  
<span class="n">axes</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">)</span>
<span class="n">axes</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">,</span><span class="n">x</span><span class="p">)</span>  
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[135]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x19778f1e400&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[137]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="p">,</span><span class="n">axes</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="n">nrows</span><span class="o">=</span><span class="mi">2</span><span class="p">,</span><span class="n">ncols</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">8</span><span class="p">,</span><span class="mi">2</span><span class="p">))</span>  
<span class="n">axes</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">)</span>
<span class="n">axes</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">,</span><span class="n">x</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">tight_layout</span><span class="p">()</span>    <span class="c1"># it is optionl but it is recommend to use for fixing layout and overlapping</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAjgAAACICAYAAADqIJGqAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADl0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uIDMuMC4yLCBodHRwOi8vbWF0cGxvdGxpYi5vcmcvOIA7rQAAGwtJREFUeJzt3X2M5PZ5H/DvwyE5nNed2d273b27Xa1l2bIcuZLcjVL0XMeJX6q4Ru380SAOmsZxABloDNhtgTZ1UdTpC+AWiZH8EQRVbQcOmsQI4ChVHMG2gDpwDbSO7iTZernYMQxZd7r17b3s3u7szHCG5NM/yJnhvOz7C3c53w8w+JEccuZ3JEb71cMfSVFVEBEREaWJkXQHiIiIiA4bAw4RERGlDgMOERERpQ4DDhEREaUOAw4RERGlDgMOERERpQ4DDhEREaXOjgFHROZF5BsickVEXhaRT0TLPy0ir4vIC9Hr/UffXSIiIqKdyU43+hOROQBzqvqciJQAXAbwIQC/AKCmqr919N0kIiIi2j1zpxVUdRnAcjS9ISJXAJzfz5dNT0/r4uLifjYlIiKiEyxQRcsLECiQtzNH9j2XL1++papndlpvx4ATJyKLAB4B8G0AFwF8XET+GYBLAP6Vqq5ut/3i4iIuXbq0l68kIiKiE2DT9XBttYFrq3VcW23g6p2wvbYWtmv1NgDgzTNFfP1f/PSR9UNEfrSb9XYdcESkCODLAD6pqusi8vsA/hMAjdrfBvDREds9DuBxAFhYWNjt1xEREdExarR8vL5Wx9U7vRBzbbWBq9H0nc1W3/pZ08CFag7zk3k8PF/BhWoe89U87pnKJ/Qv6LfjGBwAEBELwFcAfE1VPzvi/UUAX1HVB7f7nKWlJWUFh4iI6Pg12z5eX2t0qzD9QaaOW7X+AGNnwgBzPgoxF6q5KMSE7XTRhogc+79DRC6r6tJO6+1YwZGw958HcCUebkRkLhqfAwA/D+Cl/XaWiIiIDsb1fCyvNbsVl8EQs7Lh9q1vZQTnKjnMV/N4zwMz3WpMJ8icKWZhGMcfYA7Lbk5RXQTwywBeFJEXomWfAvBhEXkY4SmqVwF87Eh6SERERGj7AZbXmmFwiZ9CisbC3NhoIn5SJmMIzlUcXKjk8a77z+BCNVaFmczhbMlB5hQHmJ3s5iqqbwEYtQeePvzuEBERjaeWF+DGerNXfYkN6H19tYHluw0EsQBjCDA3kcOFag4X75seqMDkMFt2YGbG936+e7qKioiIiPbODxQrG01cX2ti+W4Dy2tNXI/a5bsNXL/bxK2a21eBEQFmyw4uVHN49A2T3bEvnSAzO+HAGuMAsxMGHCIiogMIAsWtTbcXVjoh5m4zfK01cGPDhR/0X9STtzOYm3BwrpLD/bMlzE3kMDfhdEPMXMVB1jy6+8mkHQMOERHRFlQVa/X2ULVleS1q7zZw466Llh/0bWebBs5NOJidcPD37p3CXMXB3EQO5zrtRA7lnJnIVUjjggGHiIjG1nqzPXy6qK8C00Cz3R9eTEMwU3ZwruLgkfkq5t7m4FxUfTlXCdvJQjKXUFMPAw4REaVSveX1h5WBCszy3SZqrte3jSHA2ZKDuYqDt86V8e63nMVcJYdzEw7movAyXcym+uqjtGDAISKiU8XzA9zebOHGehMr6y5ubITtykYTN9ZdXI/Cy91Ge2jb6WIW5yoO7j1TwMX7pjEXBZdOgJkpZcf6yqM0YcAhIqITwfMD3KpFwWXD7bYrA/O3ay4GxutCBJgq2DhTcnC+ksPSYnVozMvMRJaDdscIAw4RER2pth/gVs0Nqy2x0HIjVnVZ2XBxe7P/MmmgE1yymClncbaUxdvOT+BsKYuzZQdnS1nMlB2cLWcxXczykmnqw4BDRET70vYD3Nxwh6stA6eNbm+2hoKLIcBUMQwusxMOHpqfwJmSEwWZXjtdtHnKiPaFAYeIiPq0vAA3a70qy82N4WrLynoYXAYZEo5zmSk7mJtw8NB8pVdpiVVcpgoMLnS0GHCIiFJOVVFv+bhda+HWpovbtRZu11zcqrm4VWvh9mY4f7vWws2aizsjgkvGEEwXbcyUHZyvOHhkYURwKWUxxSuM6IRgwCEiOoXafoDVzVYUUMJwcqvm9oWVXoBxh+7l0lHKmpguhRWVxek8/u5iFTOdU0TRaaKw4sLgQqcLAw4R0QmgqthwvV5Q6YSTLQLMan34EmgAsDKCqUIWU0Ub08Us3ni2iOliGGCmitHy6P3Jgg3H4lVFlE4MOERER8T1fNzZbMVCSy+kdOZvd08ZtYZu999RyVvdgPLmmSKm7p0KQ0vRxnQxCi7R+2WHt/8nAhhwiIh2xfV83K23sVpvY7Xewlq9jbV6C6v1NtYaLaxthsvvbLa6AWaj6Y38rKxpYLqYxXTRxtmSgwdmy5iK5juVl6lCOF8t2Lz8mWgfGHCIaKz4gWK9EYaR1XobdxstrG7GQksjCi3dEBO+V2/5W36mbRqo5i1U8+FpnwfPT2CqMFxdmY7CS97OsMpCdMQYcIjoVFJV1FyvL4SsNaKqymZUVanHgkzUrjfbQ/dk6TAEqORtVKKwMlt28JbZMqp5C5W8hUreRjVvo5q3MBGtU83bcCyDgYXohGHAIaJEBYGi1vKw0fSw0WyH4SQKK0Onguqd0BJWXtr+FkkF4dVBlUIYQiZyFu6ZzEfBxO5WW3qhJWxLWRMGrxQiSgUGHCLaN1VFo+13w8l608N6ox3Ne1hvtrHRDOeHl4dtzfW2rKgA4XiVXhixcN/ZYqzK0quqxOcnchbHrRCNOQYcojHmen43dGw021hveL1AEgWWoYDi9q/nDT71cEDGEJQcEyXHRNmxUHJMzE/mu/Nlx0TJsVDOhW0lF4WWgoVKzkbO5mXMRLR3DDhEp1DLC1Bvedhs+ai7vbbmen3VlHhYCdv+ION6oy9LjitlzSighOHkbMnBG8/EA0u4vJyL2oHlHFBLRElgwCE6QkEQnsLZbHmou1Hb8rHpemi0/DCYtDxsugNtN7iE69fjQablbTv2JM6xjLA60qmSOCYuVHN9892AErXxakoxa/LutUR0KjHgECEcS+J6AZptf6gq0gkVnWBSbw0EllhwqQ8Elu0uLR4kAhTssOJRyEatbWKyYONCNYO8baJgZ5DPRq1topAdaG2zezqo5FiwTY5DIaLxdKCAIyKPAfhdABkAn1PVzxxKr2hsdYKG2w7Q9PzRbdvvhpHtWneX63XavbBNY2TImCzYKNgZ5AbDyFahxDKRz4ZBhpcaExEdnn0HHBHJAPg9AO8FcA3AsyLylKq+clido6OhqvAChecr2kEAz1d4foCWH00HAdr+8PvtIGp9RdsP+tbrTLsDYWRwfqfQstegMcjOGMhaBrJmBo5lIGsacKxMty05Zt98vM1aGThWBsURVZF8NoN8FFDydoZX6BARnXAHqeA8CuAHqvpDABCRLwH4IIBEAs6N9SY2oht4BQoEqtF0rEVnXvvWC1SB+Hax9YIA228XvTe4XqCIfX/0mYF2t+1uF1svCLQbIrwgChF9gWNEyIi/H4WRdrS952sUWoL+sLLDVS+HwTaHw0WndSwD5ZwVBZBMt80OzO+1zZoG72FCREQADhZwzgO4Gpu/BuCnDtad/fvPf3kFf/Gd60l9/aEyDYGZEViGATMjMDMGLCNsO8stU2AaBqxM2DqWwMoYMI2ozfTe78x33o9/Xrh9bzpcd/j7wu3Dz+x81uD3WUZYPbEzDBpERJSsgwScUX/BhkoDIvI4gMcBYGFh4QBft72P/P178N63zsAQwBCBhN/dm4+1g8sF0byxw3YQGEY4H/79Hr3eyO2ks50Agi23Mw3hOAwiIqIDOkjAuQZgPjZ/AcBQCUVVnwDwBACIyE0R+dEBvnMn0wBuHeHn0854DJLF/Z88HoNkcf8n76iPwT27WUl0u3ukb7ehiAng+wDeDeB1AM8C+CVVfXlfH3gIROSSqi4l9f3EY5A07v/k8Rgki/s/eSflGOy7gqOqnoh8HMDXEF4m/oUkww0RERFRx4Hug6OqTwN4+pD6QkRERHQo0nYzjyeS7gDxGCSM+z95PAbJ4v5P3ok4Bvseg0NERER0UqWtgkNERETEgENERETpk5qAIyKPicj3ROQHIvIbSfdn3IjIF0RkRUReSrov40hE5kXkGyJyRUReFpFPJN2ncSIijoj8tYh8J9r/v5l0n8aViGRE5HkR+UrSfRlHIvKqiLwoIi+IyKVE+5KGMTjRgz+/j9iDPwF8mA/+PD4i8k4ANQB/qKoPJt2fcSMicwDmVPU5ESkBuAzgQ/wNHA8Jbz9eUNWaiFgAvgXgE6r6/xLu2tgRkX8JYAlAWVU/kHR/xo2IvApgSVUTv9liWio43Qd/qmoLQOfBn3RMVPWbAO4k3Y9xparLqvpcNL0B4ArC58XRMdBQLZq1otfp/7/HU0ZELgD4RwA+l3RfKHlpCTijHvzJ/7jTWBKRRQCPAPh2sj0ZL9GpkRcArAB4RlW5/4/f7wD41wCCpDsyxhTA10XkcvQsysSkJeDs6sGfRGknIkUAXwbwSVVdT7o/40RVfVV9GOFz+R4VEZ6qPUYi8gEAK6p6Oem+jLmLqvp2AD8H4Nej4QuJSEvA2dWDP4nSLBr78WUAf6Sqf5Z0f8aVqq4B+CsAjyXclXFzEcA/jsaAfAnAz4rI/0y2S+NHVa9H7QqAJxEOIUlEWgLOswDeJCJvEBEbwC8CeCrhPhEdm2iQ6+cBXFHVzybdn3EjImdEpBJN5wC8B8DfJNur8aKq/1ZVL6jqIsK/Af9bVf9pwt0aKyJSiC5ygIgUALwPQGJX1qYi4KiqB6Dz4M8rAP6UD/48XiLyJwD+L4D7ReSaiPxa0n0aMxcB/DLC/2t9IXq9P+lOjZE5AN8Qke8i/B+uZ1SVlynTuJkB8C0R+Q6Avwbwl6r61aQ6k4rLxImIiIjiUlHBISIiIopjwCEiIqLUYcAhIiKi1GHAISIiotRhwCEiIqLUYcAhIiKi1GHAISIiotRhwCEiIqLUYcAhIiKi1GHAISIiotRhwCEiIqLUYcAhIiKi1GHAISIiotQxD7KxiLwKYAOAD8BT1aXD6BQRERHRQRxGBednVPXh3YQbEfnqIXwfERERjandZokDVXD2qlwu/8OlpSU9zu8kIiKinakCgSoCBVR1YHq4DVTDbaCxbRWWYWB2wjnKrq7vZqWDBhwF8HURUQD/XVWfGFxBRB4H8DgALCws4NKlSwf8SiIiovRSVbR9RdPz0Wz7cNsBXM9Hsx2g2Y61fct8uF5vurdO7P120PtMr/+zXC/Ycz8letmGwLEycCwDWTODN88U8Qe/+uih75fu94r87W7WO2jAuaiq10XkLIBnRORvVPWb8RWi0PMEALB6Q0REp00Q6FCYaMbDwojAMRwgtto+gNtZFgsjwT7/WooAWdMIA4cZhg7HyiBrZeCYBqp5u7ts6H3LiJb1lndCS6+Nvxd+ppk5mdcrHSjgqOr1qF0RkScBPArgm9tvRUREdDBtP0Cj7aPZ8tFoR69outn20WgF3eXNlj8UQDoBw42m+wJIPKi0A7T8vVc3OuyMgWwsLMQDRDFrYqqQCd83+0NFfL1sLEx0g8VASOkEFDtjQEQOcU+fXvsOOCJSAGCo6kY0/T4A//HQekZERKdOEChcL+gLHc2RAcTvCyC99QM02l7s/aDv/c60t48ShyHoqzwMVi6mi2ZfgBiqWHS36QWQ7IhqSHz7jMGwkZSDVHBmADwZJUUTwB+rKq+SIiI6gTrjOnYOGPFAEoxef5vtm+19jOUQIGdlkIvCQc7OdOcnchZmy9lw3o7e77zi8/bo7R27F0CsjLC6MUb2HXBU9YcAHjrEvhARja2WF6DR8rHZ8lBvhQGi3vJ6gWK7wLFVQIm26cz7+6h62KYxIlAYyNkZVPLWLgJGPJAYI9fPmjytQofvWC8TJyI6zYIgrIBstrwogIQhpD4w3Wj52HR91KNTLZuuj0Y7Wi9a3p2OQkzb31v4MDpVj4EqhmNlUMnbmBt6z9hFABkOHzzFQqcVAw4RpYqqouUHUZDw0Wh5YdhohSFj0+1VRza7lZJtgkoUZjZb3p5Pv9imgbydQcE2kbMzyEevsyUHOTuDgp1BPnqvYGeQs83uOnnbHBk6OqddOJiUaHsMOESUCD/QsHoRhYpdVUVa8SpIL7w02tF60fK9nIoxBAMBJAwZJcfEbNlB3g7DRSEbBo68nUE+ayIfn47CR6EzbWeQtzIn9vJZonHAgENEu6KqaLYD1FwPm67XbTdbHmquH07Hltdcf3hdt7duo+3v6fsdy+iGj3xU7SjYGZyrWN3pwZASn85FlZT4dM7m+A+itGLAIUoxzw+w6fqotXpBo9YcDCijgog/EErC9XZbGelUM0qOiUI2DBOzZQeFrIlC1kQxG75fsE3ks1FgscJ149O52KkajgUhor1gwCE6QVQ1PF3TDRv+QKWkvwpSa3rd8BJf3tl+t7dfNw1B0QkDRzEbhouSY2JuwokCSRRUsiZKUUjpLY8Flii0MIwQUdIYcIgOSRAoNlwPG802Npoe1htRG593+5evNz3Umu1ekGl50F0OHylE40KK3cCRwflKr0rSH0Qy/aHE7g8tPE1DRGnDgEOEsHLiekF/GBkMJzvM13YRThzLQMmxUHJMlB0LZcfE+YoTq4QMhBJ7cJmJohMOcDVYJSEi2hIDDqWCHyhq3arILkPJwPKdnjdjCFByLJRzJkrZsJ2fzKPcDSwmyrleeOmuGwWZkmPBNnlVDRHRcWDAoRNDVbHe9LBWb2G13sZqvRVOb7axVm9hrdHG3cbosFJzvR0/P2dl+gJHNW/jnqlCLJCEASUMI8MhpWBneBqHiOiUYMChI+F6PtaikNIJKH2hpR6Flu6yNtYa7S2v0hEByo6FSr5XIVmczkdhpRdO4qd+4vNFx4TFe5IQEY0NBhzaVhAo1pvtbji52wkt9U5oiU3Hgsx29zhxLAPVvI1K3kY1b+Ets2VU8la0zOou77TVvI1yzuKVOUREtGsMOGOm2fZxq+ZiZcPFzQ0Xt2puWEXZ7A8tncrK3UYbW936xBCgkrdRyYWVlbkJBw/MlcNQUrD7Q0vORrUQzjtW5nj/0URENHYYcFIgCBRrjTZubrhY2WjiZhReOiEmvny9OXqsSt7OdMNINW/jXCU3VFGJv1/N2yg5Jq/kISKiE4kB5wRrtv1YUBkRXGouVtbDKow3oswSPtQvizOlLO6fLeEd903jbNnBmWK47Ewpi+liFtWChazJqgoREaUHA04Caq6Ha6t1rKyPrrLcrLm4ue5iY8SVQYYAU8VsL7jMlHCm1Jl3YtNZFLI8vERENJ74F/AI+IHix+tNvHa7jqt36ngt9rp6p47bm62hbYpZs1tVeWCujHe+KdsXVsJpB5MFm4NtiYiIdsCAs08bzXY3sPQCTANX79RxbbWOtt87ZZQxBOcrOSxM5vG+n5jFwmQe85M5zJadbnjJ2zwUREREh4V/Vbfg+QGW7zZHVmBeu1PHar3dt34lb2FhMo+3nivjsQfDENN5zU04MHkPFiIiomPDgIPwDrrXVht47rVVPP/aGp5/bRWvLK/3VWFMQ3ChmsP8ZB7vf9tcN7zMR6+JnJXgv4CIiIjixjLgNFo+vnttDc9fXcNzP1rF81fXcHPDBRDezv+h+Ql89B1vwL3TBcx3qzA5jn0hIiI6JVIfcFQVV++E1ZlOhebK8nr3surFqTz+wX3TeOSeKh6Zr+AtsyWeTiIiIjrlUhtw1uot/Nevfg/PvPJj3KqFVy0V7Awemq/gYz99L96+UMUjC1VMFuyEe0pERESH7UABR0QeA/C7ADIAPqeqnzmUXh3QM6/cwKeefBGrmy184O/MYWlxEm9fqOL+2RJPMxEREY2BfQccEckA+D0A7wVwDcCzIvKUqr5yWJ3bq9XNFn7zL17Gn79wHQ/MlfEHH/lJPHh+IqnuEBERUUIOUsF5FMAPVPWHACAiXwLwQQCJBJyvvfxj/LsnX8JavYVPvudN+Ofvug+2ybE0RERE4+ggAec8gKux+WsAfmpwJRF5HMDjALCwsHCAr9veX31vBWdKWXzxoz+JnzjHqg0REdE4O0jAGTWYZeiJj6r6BIAnAGBpaWn4iZCH5N9/4K2wMgYsXgFFREQ09g4ScK4BmI/NXwBwfbsNLl++fEtEfnSA79zJNIBbR/j5tDMeg2Rx/yePxyBZ3P/JO+pjcM9uVhLV/RVVRMQE8H0A7wbwOoBnAfySqr68rw88BCJySVWXkvp+4jFIGvd/8ngMksX9n7yTcgz2XcFRVU9EPg7gawgvE/9CkuGGiIiIqONA98FR1acBPH1IfSEiIiI6FGkbkftE0h0gHoOEcf8nj8cgWdz/yTsRx2DfY3CIiIiITqq0VXCIiIiIGHCIiIgofVITcETkMRH5noj8QER+I+n+jBsReVVEXhSRF0TkUtL9GQci8gURWRGRl2LLJkXkGRH526itJtnHtNviGHxaRF6PfgsviMj7k+xjmonIvIh8Q0SuiMjLIvKJaDl/B8dgm/1/In4DqRiDEz348/uIPfgTwIeTfPDnuBGRVwEsqSpvsHVMROSdAGoA/lBVH4yW/TcAd1T1M1HQr6rqv0myn2m2xTH4NICaqv5Wkn0bByIyB2BOVZ8TkRKAywA+BOAj4O/gyG2z/38BJ+A3kJYKTvfBn6raAtB58CdRaqnqNwHcGVj8QQBfjKa/iPA/NnREtjgGdExUdVlVn4umNwBcQficRP4OjsE2+/9ESEvAGfXgzxOzk8eEAvi6iFyOHrBKyZhR1WUg/I8PgLMJ92dcfVxEvhudwuLpkWMgIosAHgHwbfB3cOwG9j9wAn4DaQk4u3rwJx2pi6r6dgA/B+DXo9I90Tj6fQBvBPAwgGUAv51sd9JPRIoAvgzgk6q6nnR/xs2I/X8ifgNpCTh7fvAnHS5VvR61KwCeRHjakI7fjei8eOf8+ErC/Rk7qnpDVX1VDQD8D/C3cKRExEL4x/WPVPXPosX8HRyTUfv/pPwG0hJwngXwJhF5g4jYAH4RwFMJ92lsiEghGmAGESkAeB+Al7bfio7IUwB+JZr+FQD/K8G+jKXOH9bIz4O/hSMjIgLg8wCuqOpnY2/xd3AMttr/J+U3kIqrqAAgugztd9B78Od/SbhLY0NE7kVYtQHC55v9Mff/0RORPwHwLgDTAG4A+A8A/hzAnwJYAPAagH+iqhwEe0S2OAbvQliaVwCvAvhYZzwIHS4ReQeA/wPgRQBBtPhTCMeB8HdwxLbZ/x/GCfgNpCbgEBEREXWk5RQVERERURcDDhEREaUOAw4RERGlDgMOERERpQ4DDhEREaUOAw4RERGlDgMOERERpc7/ByQHy5/twuOeAAAAAElFTkSuQmCC
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Save-figure">Save figure<a class="anchor-link" href="#Save-figure">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[138]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[138]:</div>




<div class="output_png output_subarea output_execute_result">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[139]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">.</span><span class="n">savefig</span><span class="p">(</span><span class="s1">&#39;My_picture.png&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[140]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">.</span><span class="n">savefig</span><span class="p">(</span><span class="s1">&#39;My_picture1.png&#39;</span><span class="p">,</span><span class="n">dpi</span><span class="o">=</span><span class="mi">200</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Legned">Legned<a class="anchor-link" href="#Legned">&#182;</a></h1><p>The legend is often located on the right-hand side of the chart or graph and is sometimes surrounded by a border. <br>
The legend is linked to the data being graphically displayed in the plot area of the chart</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span> <span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mf">0.1</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mf">0.8</span><span class="p">,</span><span class="mf">0.8</span><span class="p">])</span>  <span class="c1"># List tabking four argument LEFT BOttom width and height </span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">)</span>
<span class="n">axes</span><span class="o">.</span><span class="n">set_xlabel</span><span class="p">(</span><span class="s2">&quot;X lable &quot;</span><span class="p">)</span>
<span class="n">axes</span><span class="o">.</span><span class="n">set_ylabel</span><span class="p">(</span><span class="s2">&quot;Y Lable &quot;</span><span class="p">)</span>
<span class="n">axes</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s2">&quot;Title of graph&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[157]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mf">0.1</span><span class="p">,</span><span class="mf">0.1</span><span class="p">,</span><span class="mf">0.8</span><span class="p">,</span><span class="mf">0.8</span><span class="p">])</span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">x</span><span class="o">**</span><span class="mi">2</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="s2">&quot;X Square&quot;</span><span class="p">)</span>  <span class="c1"># Label is mandatory  for legend</span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">x</span><span class="o">**</span><span class="mi">3</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="s2">&quot;X Cube&quot;</span><span class="p">)</span>

<span class="n">axes</span><span class="o">.</span><span class="n">legend</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[157]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.legend.Legend at 0x19777f788d0&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Legend-location-https://matplotlib.org/3.1.0/api/_as_gen/matplotlib.pyplot.legend.html">Legend location <a href="https://matplotlib.org/3.1.0/api/_as_gen/matplotlib.pyplot.legend.html">https://matplotlib.org/3.1.0/api/_as_gen/matplotlib.pyplot.legend.html</a><a class="anchor-link" href="#Legend-location-https://matplotlib.org/3.1.0/api/_as_gen/matplotlib.pyplot.legend.html">&#182;</a></h3><p>Location String Location Code<br>
'best'  0 <br>
'upper right'   1<br>
'upper left'    2<br>
'lower left'    3<br>
'lower right'   4<br>
'right' 5<br>
'center left'   6<br>
'center right'  7<br>
'lower center'  8<br>
'upper center'  9<br>
'center'    10<br></p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[161]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mf">0.1</span><span class="p">,</span><span class="mf">0.1</span><span class="p">,</span><span class="mf">0.8</span><span class="p">,</span><span class="mf">0.8</span><span class="p">])</span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">x</span><span class="o">**</span><span class="mi">2</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="s2">&quot;X Square&quot;</span><span class="p">)</span>  <span class="c1"># Label is mandatory  for legend</span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">x</span><span class="o">**</span><span class="mi">3</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="s2">&quot;X Cube&quot;</span><span class="p">)</span>

<span class="n">axes</span><span class="o">.</span><span class="n">legend</span><span class="p">(</span><span class="n">loc</span><span class="o">=</span><span class="mi">10</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[161]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.legend.Legend at 0x197781f6ba8&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAYUAAAEJCAYAAAB7UTvrAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADl0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uIDMuMC4yLCBodHRwOi8vbWF0cGxvdGxpYi5vcmcvOIA7rQAAIABJREFUeJzt3Xl4VOXd//H3NyF7AoQkrAESEFBABIkIikrdq9alWoVqtbaWp1qttbWVPtali9Y++lTr09b+aF1b61L3uhW04BpUgqjIouyENQkBsm9z//44wzRgFEhm5sxMPq/ryjUzZ87M+UwC5zv3fZ9zH3POISIiApDkdwAREYkdKgoiIhKioiAiIiEqCiIiEqKiICIiISoKIiISoqIgIiIhKgoiIhKioiAiIiE9/A4AkJ+f74qKivyOISKSsMrKyiqdcwX7Wi8mikJRURELFy70O4aISMIys3X7s566j0REJERFQUREQlQUREQkREVBRERCVBRERCRERUFEREJUFEREJERFQUQk1rU2QZQunayiICIS6+beCA9+BdpaI74pFQURkVhWtQre+wvkDYfkyE9CoaIgIhLLXrkZktNg2n9HZXMqCiIisWr9Alj2HBx9NeT0i8omVRRERGKRczDnZ5DdH466MmqbjYlZUkVEZC9Ln4Hy9+DM30NqVtQ2u8+WgpndZ2bbzGxJu2W3m9lyM/vQzJ42s97tnvupma00sxVmdkqkgouIJKzWJm8soe8YGP/1qG56f7qPHgBO3WvZXGCsc24c8AnwUwAzGw1MB8YEX/NHM0sOW1oRke7gvXuhei2c/AtIiu4udJ9FwTn3OrB9r2VznHO7D5hdABQG758FPOqca3LOrQFWApPCmFdEJLE1VMNrv4Hhx8NBJ0Z98+EYaP4W8FLw/iBgQ7vnyoPLPsPMZprZQjNbWFFREYYYIiIJ4PU7oHEnnPRLXzbfpaJgZtcDrcDDuxd1sFqH52Y752Y750qccyUFBfu8bKiISOKrXgvvzobxF0L/sb5E6PTRR2Z2CXAGcIJzoUk5yoHB7VYrBDZ1Pp6ISDfy6i/AkuH4632L0KmWgpmdClwHnOmcq2/31HPAdDNLM7NiYATwbtdjiogkuPIyWPIkHHUV9BzoW4x9thTM7BFgGpBvZuXATXhHG6UBc80MYIFz7rvOuY/N7HFgKV630vecc22RCi8ikhB2n6iWVQBHf9/XKPssCs65GR0svvcL1r8FuKUroUREupXlL8D6t+GMOyEtx9comuZCRMRPbS3e1Nj5o2DCxX6n0TQXIiK+Wng/bF8FMx6LytTY+6KWgoiIXxp3wmu3QdExMDI2ZgVSURAR8cubd0J9FZz8K7COTvOKPhUFERE/7NgApX+EcRfAwPF+pwlRURAR8cO/f+XdHn+Dvzn2oqIgIhJtmxbDh4/ClCug9+B9rx9FKgoiItG0+0S1zDyYeo3faT5DRUFEJJo+nQNr34DjZkF6L7/TfIaKgohItLS1wpwboM9wKLnU7zQd8v9MCRGR7uL9h6ByBVzwN0hO8TtNh9RSEBGJhqYamPdrGDIFDj7D7zSfSy0FEZFoeOtuqNsGMx6JmRPVOqKWgohIpO3aBG//H4w9FwpL/E7zhVQUREQibd4t4NrghBv9TrJPKgoiIpG0ZQm8/zBMmgm5RX6n2ScVBRGRSJp7g3c+wrHX+p1kv6goiIhEyspXYNW/4bifQEau32n2i4qCiEgkBNpgzo1el9ERl/mdZr/pkFQRkUhY/HfY9jF87QHokeZ3mv2mloKISLg113lTYxceAaPP9jvNAVFLQUQk3Er/ALVb4PwHY/pEtY6opSAiEk41W+HNu+CQM2HIZL/THDAVBRGRcJp/K7Q1wYk3+52kU/ZZFMzsPjPbZmZL2i3rY2ZzzezT4G1ucLmZ2d1mttLMPjSzwyMZXkQkpmxbDose8o42yhvud5pO2Z+WwgPAqXstmwW86pwbAbwafAzwZWBE8GcmcE94YoqIxIG5N0JqDhz7E7+TdNo+i4Jz7nVg+16LzwIeDN5/EDi73fKHnGcB0NvMBoQrrIhIzFr9Gnz6Lzjmh5CV53eaTuvsmEI/59xmgOBt3+DyQcCGduuVB5eJiCSuQMC77nKvwXDkd/1O0yXhHmju6Ngr1+GKZjPNbKGZLayoqAhzDBGRKProcdjyIZxwE6Sk+52mSzpbFLbu7hYK3m4LLi8HBrdbrxDY1NEbOOdmO+dKnHMlBQUFnYwhIuKzlgZ49ZcwcIJ3vYQ419mi8BxwSfD+JcCz7ZZfHDwKaTKwc3c3k4hIQlpwD+wqh5N/BUnxf5T/Ps9oNrNHgGlAvpmVAzcBtwGPm9m3gfXA14KrvwicBqwE6oFLI5BZRCQ21FXCG7+FUadB0VS/04TFPouCc27G5zx1QgfrOuB7XQ0lIhIX5t8GLfVw4s/9ThI28d/WERHxQ+WnsPA+mPhNKBjpd5qwUVEQEemMV26GlEyY9lO/k4SVioKIyIFa+xYsfx6m/gCyE+voSRUFEZEDsftEtZyBMPkKv9OEna6nICJyID5+CjYtgrPvgdRMv9OEnVoKIiL7q6URXvk59D8Uxl3gd5qIUEtBRGR/vTsbdq6HM5+BpGS/00SEWgoiIvujfju8cQccdBIM/5LfaSJGRUFEZH+8fjs01cBJv/A7SUSpKIiI7MvWj+HdP8OEi6DfaL/TRJSKgojIF2ltgqdmQkauNzV2gtNAs4jIF5l3K2xdAjMeg6x8v9NEnFoKIiKfZ10pvPU7OPxiGLX3peoTk4qCiEhHmmrg6f+C3kPglFv9ThM16j4SEenIv/4bdqyHS1+CtBy/00SNWgoiIntb8RIsegiOvhqGTvE7TVSpKIiItFdXCc9dBf3Gwpf+2+80UafuIxGR3ZyDf14NjTvh4mehR5rfiaJOLQURkd0+eMS7TsLxP4N+Y/xO4wsVBRER8AaVX/wJDDkKplzpdxrfqCiIiAQC8MwVgINz7knYGVD3h8YUREQW/BHWvgFn/h5yi/xO4yu1FESke9u2DF79BYw6zZvwrptTURCR7qu1GZ76jndy2lfuBjO/E/lO3Uci0n29dhts+Qim/x2yC/xOExO61FIws2vM7GMzW2Jmj5hZupkVm9k7ZvapmT1mZqnhCisiEjbr34E374TxF8HBp/udJmZ0uiiY2SDg+0CJc24skAxMB34D3OmcGwFUA98OR1ARkbBpqvUmu+tVCKf+2u80MaWrYwo9gAwz6wFkApuB44Engs8/CJzdxW2IiITXnJ9B9Vo4+0+Q3tPvNDGl00XBObcRuANYj1cMdgJlwA7nXGtwtXJgUEevN7OZZrbQzBZWVFR0NoaIyIH5ZA6U3Q9HXQlFR/udJuZ0pfsoFzgLKAYGAlnAlztY1XX0eufcbOdciXOupKBAAzwiEgV1VfDcldB3NHzpZ36niUldOfroRGCNc64CwMyeAo4CeptZj2BroRDY1PWYIiJd5By8cA3Ub4eLnoSUdL8TxaSujCmsByabWaaZGXACsBSYB5wXXOcS4NmuRRQRCYOP/gFLn/Wmw+5/qN9pYlZXxhTewRtQXgR8FHyv2cB1wA/NbCWQB9wbhpwiIp23sxxeuBYGT/YunCOfq0snrznnbgJu2mvxamBSV95XRCRsdk92F2jt9pPd7Q+d0Swiie3d2bDmNfjK76DPML/TxDzNfSQiiatiBbxyE4w8FQ6/xO80cUFFQUQSU1sLPDUTUjI12d0BUPeRiCSm12+HzYvh/L9CTj+/08QNtRREJPGUl8Hrd8BhM2D0mX6niSsqCiKSWJrr4emZkDMAvvwbv9PEHXUfiUhimXsjVK2Ei5+D9F5+p4k7KgoSc1paWigvL6exsdHvKHErPT2dwsJCUlJS/I4SXStfhff+DJOvgGHH+Z0mLqkoSMwpLy8nJyeHoqIiTEeMHDDnHFVVVZSXl1NcXOx3nOip3w7Pfg/yR8EJN/qdJm5pTEFiTmNjI3l5eSoInWRm5OXldb+W1ovXQl0FfHU2pGT4nSZuqShITFJB6Jpu9/v76AlY8iQcNwsGjvc7TVxTURDZy4YNGyguLmb79u0AVFdXU1xczLp16z6z7i233MKYMWMYN24c48eP55133ol2XNm1CV74IRQeAVOv8TtN3NOYgsheBg8ezOWXX86sWbOYPXs2s2bNYubMmQwdOnSP9UpLS3n++edZtGgRaWlpVFZW0tzcHNFsbW1tJCdrQrcQ57xxhLYWOOf/QbJ2aV2lloJIB6655hoWLFjAXXfdxZtvvsmPfvSjz6yzefNm8vPzSUtLAyA/P5+BAwcC8PLLL3PwwQczdepUvv/973PGGWcAcPPNN3PHHXeE3mPs2LGsXbsWgLPPPpuJEycyZswYZs+eHVonOzubG2+8kSOPPJLS0lLKyso47rjjmDhxIqeccgqbN2+O1K8h9r33F1j1bzj5l5A33O80CUFFQaQDKSkp3H777VxzzTXcddddpKamfmadk08+mQ0bNjBy5EiuuOIKXnvtNcAbKP/Od77DP//5T9544w22bNmyX9u87777KCsrY+HChdx9991UVVUBUFdXx9ixY3nnnXc48sgjueqqq3jiiScoKyvjW9/6Ftdff334Png8qfwU5twAB50IJd/2O03CUFtLYtrP//kxSzftCut7jh7Yk5u+Mmaf67300ksMGDCAJUuWcNJJJ33m+ezsbMrKynjjjTeYN28eF1xwAbfddhvjx4+nuLiYESNGAHDRRRft8c3/89x99908/fTTgDeu8emnn5KXl0dycjLnnnsuACtWrNgjT1tbGwMGDNjvz54w2lrh6f/yLql55u812V0YqSiIdGDx4sXMnTuXBQsWMHXqVKZPn97hzjc5OZlp06Yxbdo0Dj30UB588EHGjx//uUf/9OjRg0AgEHq8+7DR+fPn88orr1BaWkpmZibTpk0LPZeenh4aR3DOMWbMGEpLS8P9kePLG/8LG8vgvPuhZzcsihGkoiAxbX++0Yebc47LL7+cu+66iyFDhvDjH/+Ya6+9locffniP9VasWEFSUlKoRbB48WKGDh3KwQcfzJo1a1i1ahXDhw/nkUceCb2mqKiI559/HoBFixaxZs0aAHbu3Elubi6ZmZksX76cBQsWdJht1KhRVFRUUFpaypQpU2hpaeGTTz5hzJjo/558s3ERvPYbOPRrMParfqdJOBpTENnLn//8Z4YMGRLqorniiitYvnx5aMxgt9raWi655BJGjx7NuHHjWLp0KTfffDPp6enMnj2b008/nalTp+5x1NK5557L9u3bGT9+PPfccw8jR44E4NRTT6W1tZVx48Zxww03MHny5A6zpaam8sQTT3Dddddx2GGHMX78eN5+++0I/SZiUEuD122U3Q9Ou93vNAnJnHN+Z6CkpMQtXLjQ7xgSI5YtW8Yhhxzid4ywmT9/PnfccUeohRAtifZ7BOCl6+CdP8E3noHhX/I7TVwxszLnXMm+1lNLQUTiw8pXvIIw6b9UECJIYwoiEbZ7IFq6YMsS+Mel0Hc0nHiz32kSmloKIhLbdmyAh8+D1Gy48B+Qmul3ooSmloKIxK6Gaq8gNNfBt16GXoV+J0p4XWopmFlvM3vCzJab2TIzm2Jmfcxsrpl9GrzNDVdYEelGWhrh0QuhahVMfxj6daPDbn3U1e6j3wEvO+cOBg4DlgGzgFedcyOAV4OPRUT2XyDgHXq67i04509QfKzfibqNThcFM+sJHAvcC+Cca3bO7QDOAh4MrvYgcHZXQ4pE04FMnb1lyxamT5/O8OHDGT16NKeddhqffPLJF75/UVERlZWVEcmeMOZcD0ufgZN+CYee53eabqUrLYVhQAVwv5m9b2Z/MbMsoJ9zbjNA8LZvGHKKRE37qbOBz5062znHOeecw7Rp01i1ahVLly7l1ltvZevWrX7EThxv/x4W/BGO/C4cdZXfabqdrhSFHsDhwD3OuQlAHQfQVWRmM81soZktrKio6EIMkfDbn6mz582bR0pKCt/97ndDy8aPH88xxxzD/PnzQ9NlA1x55ZU88MADoce33347kyZNYtKkSaxcuRKAiooKzj33XI444giOOOII3nrrrch9wFi15EmvlXDImXDKrZrozgddKQrlQLlzbvelpp7AKxJbzWwAQPB2W0cvds7Nds6VOOdKCgoKuhBDJPz2Z+rsJUuWMHHixE69f8+ePXn33Xe58sor+cEPfgDA1VdfzTXXXMN7773Hk08+yWWXXdalzxB31rwBT38XhkyBr/4ZknQxIT90+pBU59wWM9tgZqOccyuAE4ClwZ9LgNuCt8+GJal0Ty/Ngi0fhfc9+x8KX75t35vex9TZXTFjxozQ7TXXeJeQfOWVV1i6dGlonV27dlFTU0NOTk5Ytx2Tti71jjTKLYbpf/emxBZfdPU8hauAh80sFVgNXIrX+njczL4NrAe+1sVtiETd/kydPWbMGJ544okOX/95U2Tv1n5q7d33A4EApaWlZGRkhOtjxIedG+Fv50JKBlz0JGT28TtR9+ac8/1n4sSJTmS3pUuX+rr9QCDgJk+e7ObMmeOcc+7uu+92X//61ztcb9KkSW727NmhZe+++66bP3++W79+vRs6dKhrbGx0O3bscEVFRe7+++93zjk3dOhQ9+tf/9o559xf//pXd8YZZzjnnJsxY4b7n//5n9B7vf/++136HH7/HvdLfbVzf5js3C2DnNv8od9pEhqw0O3H/ljTXIjsZX+nzjYznn76aebOncvw4cMZM2YMN998MwMHDmTw4MGcf/75jBs3jgsvvJAJEybs8dqmpiaOPPJIfve733HnnXcC3pXXFi5cyLhx4xg9ejR/+tOfovOB/dLaBI9dBJWfwAV/9br1xHeaOltiTkJO+eyDmP49BgLw1GXe0UbnzIbDLvA7UcLT1NkiErvm3uAVhBNvVkGIMSoKIhJdC+6B0t/DEd+Bo3/gdxrZi4qCiETPx8/Ayz+Fg8+AL/9GJ6fFIBUFiUmxMNYVz2Ly97fubXhqJgyeBOf+RSenxSgVBYk56enpVFVVxeaOLQ4456iqqiI9PYZOANu2HB6ZDr2HwIxHvXMSJCbpIjsScwoLCykvL0dzYnVeeno6hYUxckGaXZu8k9N6pOvktDigoiAxJyUlheLiYr9jSDg07oSHvwaNO+DSFyF36L5fI75SURCRyGhthse+ARXL4euPw4DD/E4k+0FFQUTCLxCAZ78Ha16Ds/8EB53gdyLZTxpoFpHwe/Xn8NHjcPwNMH6G32nkAKgoiEh4vTMb3roLSr4Fx3z24kQS21QURCR8lj4HL/0ERp0Op92hk9PikIqCiITH+gXw1HegsEQnp8UxFQUR6bqKT+DvF0DPQTDjMUjN9DuRdJKKgoh0Tc0W7+S05BTv5LSsPL8TSRfokFQR6bzGXfDweVBfBZe+AH100mG8U1EQkc5pbYbHL4atS72T0wZO2PdrJOapKIjIgXMO/vl9WD0PzvojjDjR70QSJhpTEJED9+9fwgePwJeuhwkX+p1GwkhFQUQOzHt/gTf+Fw6/BI79sd9pJMxUFERk/y1/AV78MYw8FU7/rU5OS0AqCiKyfxb/HR6/xBtQPu8+SNaQZCLSX1VEvlgg4I0hvPlbKD4Ozn8QUrP8TiUR0uWWgpklm9n7ZvZ88HGxmb1jZp+a2WNmltr1mCLii+Z6+MclXkGY+E3v5LSMXL9TSQSFo/voamBZu8e/Ae50zo0AqoFvh2EbIhJtNVvggdNg2T/h5FvgjLu8s5YloXWpKJhZIXA68JfgYwOOB54IrvIgcHZXtiEiPtj8Ifz5eG9Oo+l/h6Ou1KByN9HVlsJdwE+AQPBxHrDDOdcafFwODOrohWY208wWmtlCXaBdJIaseAnuO9W7/62X4eDT/M0jUdXpomBmZwDbnHNl7Rd3sKrr6PXOudnOuRLnXElBQUFnY4hIuDgHb/8eHpkBBSPhO/+GAeP8TiVR1pWjj44GzjSz04B0oCdey6G3mfUIthYKgU1djykiEdXWAi9eC2UPwCFnwjn/T9Nfd1Odbik4537qnCt0zhUB04F/O+cuBOYB5wVXuwR4tsspRSRyGqq9qa/LHoCpP4SvPaiC0I1F4uS164AfmtlKvDGGeyOwDREJh+2r4d6TYd3b3sR2J94ESTqntTsLy8lrzrn5wPzg/dXApHC8r4hE0Lq34dELAQcXPwtFR/udSGKAvhKIdEeLH4EHz4TMPnDZqyoIEqJpLkS6k0AA5t0Cb9wBxcfC+Q/pDGXZg4qCSHfRXA/PfBeWPutNe336/+oMZfkMFQWR7qBmi3f+wab34eRfwRSdoSwdU1EQSXRbPoK/T4eG7TD9YTj4dL8TSQxTURBJZCtehie/DWk9vSkrBhzmdyKJcTr6SCQROQelf4RHZ0DeQcEpK1QQZN/UUhBJNG0t3iUzy+6HQ74SnLJCF8WR/aOiIJJIGnbAP74Jq+fB0T+AE3SGshwYFQWRRLF9Dfz9Am/qirP+ABMu8juRxCEVBZFEsK4UHv063pQVz0DRVL8TSZxSu1Ik3n3wGDx0pndm8mWvqiBIl6ilIBKvAgGYfyu8fjsUHeNNWZHZx+9UEudUFETiUUsDPHM5fPw0TPgGnP5b6JHqdypJACoKIvGmZqt3/sHGRXDSL+GoqzRlhYSNioJIPFn7Fjz9X1BfBRf8DQ45w+9EkmBUFETiQe02mHMDfPgo9BoCl74EA8f7nUoSkIqCSCwLtMF798K/fwUt9XDMj+CYa3UNZYkYFQWRWFW+EF74IWz+AIZNg9PugPwRfqeSKGsLOJZt3kVlbRPTRvWN+PZUFERiTf12eOVmWPQQ5PSH8+6DMV/VYHI3EQg4VmytoXRVFaWrq3h3zXZ2NrQwsFc6b806HovwvwMVBZFYEQjA4r/B3JugcSdM+R5MmwVpOX4nkwhyzvHptloWrK6idFUVC1ZXUV3fAsDgPhmcMqYfU4bnMXlYXsQLAqgoiMSGzR/CCz+C8ndhyBTvUpn9xvidSiLAOcfqyrpQS+Cd1VVU1jYDMKh3Bscf3I/Jw/owZXgehbnRHztSURDxU+NOmHcrvDsbMvrA2ffAYTPUVZRAnHOs314fKgKlq6rYVtMEQL+eaUw9KJ8pw/OYMiyfwX0yotIa+CIqCiJ+cA4++gfM+Zl3uGnJt+CEG7z5iyTubdheT+nqKhYEu4M27WwEID87LVgA8pg8rA/F+Vm+F4G9dboomNlg4CGgPxAAZjvnfmdmfYDHgCJgLXC+c66661FFEsS25fDitbD2DRh4OMx4FAYd7ncq6YJNOxpCYwKlq6sor24AoE9WKpOH9eHyYXlMGZ7H8ILsmCsCe+tKS6EV+JFzbpGZ5QBlZjYX+CbwqnPuNjObBcwCrut6VJE411QLr/8PlP4BUrO9+YomfhOSkv1OJgdo267GUFdQ6eoq1lXVA9A7M4Uji/tw2dRipgzPZ0TfbJKSYrsI7K3TRcE5txnYHLxfY2bLgEHAWcC04GoPAvNRUZDuzDlY9k94+aewqxzGXwQn/Ryy8v1OJvtp884GFq6t9loDq6tYXVEHQE56D44szuPiKUVMHtaHQ/r3jLsisLewjCmYWREwAXgH6BcsGDjnNptZ5M+2EIlVVavgpZ/Ayleg31g4714YMtnvVPIFWtoCLNu8i7J11ZStq2bRuurQmEB2Wg+OKMpl+hGDmTIsn9EDe5Ic50Vgb10uCmaWDTwJ/MA5t2t/+8vMbCYwE2DIkCFdjSESW1oa4M274M07ITkVTvk1TJoJyTq2I9ZU1zWzaH11qAh8UL6DxpYAAAN7pXP40Fy+MzSXw4fkMmZgT3okJ/a1ybr0L9TMUvAKwsPOuaeCi7ea2YBgK2EAsK2j1zrnZgOzAUpKSlxXcojElE/mwEs/huq1MPZcOPkW6DnA71SCd7bwqoparwUQLASrgl1BPZKMMQN7MmPSECYGi8DA3hk+J46+rhx9ZMC9wDLn3G/bPfUccAlwW/D22S4lFIkXOzbAy7Ng+fOQNwIuftabs0h8U9fUygflO1i0uyto/Q52NnhnC+dmpjBxaC7nTixk4pBcxhX2JiNVg/5daSkcDXwD+MjMFgeX/TdeMXjczL4NrAe+1rWIIjGutRlKf+9dFtM5OOFGmHKVroQWZc45Nu5oCI0DlK2vZtnmGtoCXkfEyH7ZnHZofw4fksvEobkxeY5ALOjK0UdvAp/3Gz2hs+8rElfWvO5NT1H5CRx8Bpz6a+itMbJoaG4N8PGmnXt0BW3d5Z0pnJmazIQhvfnetOEcPjSXCYNz6ZWZ4nPi+KBRL5HOqNkC/7oeljwBvYfC1x+Hkaf4nSqhbd3VyAcbdlC23msJfFC+k+ZWb0B4cJ8MpgzL88YChuYyql9Owg8IR4qKgsiBqK2ARQ96Rxa1NcFx18HUayCl+w1IRtLWXY18VL6TjzbuZMlG73b3fEGpyUmMHdSTS6YMDQ0I9+2Z7nPixKGiILIvzsG6t2DhfbD0OQi0wIiT4dTbIG+43+ni3hcVgCSD4QXZTD0on7GDenHY4F6MGdiL9BQNCEeKioLI52mohg8e84pB5QpI7wVHXAYll0LBKL/TxaUDKQDjCnsxemBPMlO1m4om/bZF2nMONi7yCsGSJ6G1AQaVwFl/hDHn6NrIB2DvAvDhxp1UqADEPP0FRMCbrO6jf3jFYMuHkJIFh033WgUDDvM7XczbnwJwjApAXNBfRbq3LUu8QvDh49BcA33HeFc9O/R8SO/pd7qYdCAF4NDCXowe0JOsNO1q4oX+UtL9tDTA0mfhvXu9y18mp8HYr3oXuik8Qlc9C6prauXTbbWs2LKLFVtq+WRrDcu31FBZqwKQyPTXk+6jciWU3Q+LH/YGkfMOglNu9S5/mdnH73S+aW4NsKayjhVba0IFYMXWXWzY3hBaJz0liZH9cpg2qoDRA3qqACQw/UUlsbU2w4oXvC6iNa9DUg845Cteq6DomG7VKggEHOXVDazYWhP61v/JlhpWV9bS0uZNBZGcZAzLz2JcYW/OnziYkf1zGNUvh8F9MhNuimjpmIqCJKbqdd5JZov+CnXboNcQOP4GmPANyOnnd7qIcs5RWdtSzxTKAAAKzElEQVTMii01XgHYUsPyrTV8urWG+ua20HqFuRmM6pfD8Yf05eD+OYzsl8OwgizSeugcgO5MRUESR6ANPp3rtQo+neO1Akac4rUKDjohIS97WdPYwidba1mxxfv2v7sQbK9rDq2Tl5XKqP45nF8ymFH9cxjVP4cRfbPJSddcQPJZKgoS/2q2eC2Csge8y11m94djfwyHXwy9B/udrsucc1TVNbO2so7VlXWsrqgLFYCNO/7T75+VmsyIfjmcPLofI/vleN/+++eQn53mY3qJNyoKEp8CAVjzmtcqWPEiBFph2Je8WUpHfRmS4+9b8M6GFtZW1rG2ytvxr62qY02l91PT2BpaLyXZGF6QTUlRLl/vN4RR/bxv/4N6Z8T99YHFfyoKEj9qtsK6N2HtW7DqVe/KZhl9YPLlMPHSuJiHqKG5bY+d/ZrKOtYGb6vadfmYwaDeGRTnZ3HOhEEU5WVRXJBFcV4WhbkZmgFUIkZFQWLXzo3eRHRr3/Ruq1Z6y1OzYcgU+NL1cMiZkBJbM2Q2twbYUF3PmuC3/dXtdvybgxeA361vThrF+VmcNLofxflZFOVnMSw/i8F9MjXpm/hCRUFix471Xitgd2ugeo23PK0XDJ0Ch18CRUdD/8Mg2d9/um0Bx6YdDXt8418T7PrZsL2eQLurjvfOTKE4P4spw/JCO/7dt9k6zl9ijP5Fij+c87p/drcC1r4FO9d7z6X3hqFHw6SZXhHoNzbqRw61tAXYsrORjTsa2FjdwKYdDd794OPy6gaa2wKh9bNSkynKz+LQQb0487CB/9n552WRm6XLckr8UFGQ6HAOqlb9pxWw7i3YtdF7LjPPKwJHXend9h0NSZHtM69ramXTjgbKgzv5jTuCO/7g/a27Gvf4tg+Qn53KoN4ZHDwg5zPdPQU5abreryQEFQWJDOe86xa3bwnUbvGey+rrtQCKpsLQqd61CcK4Q919CGf7nXz5Xt/2d9S37PGaHknGgN7pDOyVwZTheRT2zmBg7wwG5WYwKHhfffzSHagoSHgEAlCx7D9jAuvehroK77mcgVB8jNcKKJrqzTnUhSLQ2NJGRU3Tf3by1e26doLf+BtbAnu8Jis1mUG53s59/ODeoZ39oOCOv29OuqZxEEFFQTqrrQW2LWt3dNDb0LDde67XYBh+gtcaGHo09Bm2zyLQ2hZge10z22qaqKhtojJ4W1HT7if4uP0x+7uFunb653D8qL7/2ekHb3tlpKh7R2Q/qChIxwJtsGuTd0TQjnXB2/XenEI71nvjAS44j07vod4JY0VTvSKQOxTwunF2NrRQsa12j5363jv7ytomquqace6zMbLTelCQk0ZBdhqH9O/JsSPSKMhJIz871eveUdeOSFipKHRXgYDXx7/Hzn7dfwrAznLvLOEQg5wBBHoNpnngEdQfdA47MotYlz2eDYE+3g5+VROVH2yjomZDaOe/e/bN9lKTk7wde04ahbmZTBiS6+34gzv/gpw0+uakkZ+dRkaqdvYi0aSikKic8/r0q9vt6IO3rnod7NyAtTXv8ZKG1Dx2pA2kKmUEW/tMZSMFrA/ks7oln5VNvancCfUVbXttaDOwmSSDvGxvp56fk8ZBfXP+s6Nvt7MvyEmjZ3oPdeWIxKiIFQUzOxX4HZAM/MU5d1ukttXdtLW10VBfS2PtDhqqymmuXIOrXkfSzvWk1paTWbeRnKZNpASa9nhdNT3Z4Lwdfbk7hHJXQLkrYIMrYKPLp7HRmzgtMzWZXhkp9MpIoWdGCr16pzAp+Lh3Rgq9MoP3M1NDO/s+WakaqBVJABEpCmaWDPwBOAkoB94zs+ecc0sjsb1Y0hZwNLS00dDcRmNLG/UNjTQ31NBcX0NrYw0tDTW0NdbS1lSLa6rFNdVBcy1JLXVYSz3JrXUkt9aT0lZPSlsDqW0NpLkG0gINZNBAhmskg2ayzZG917Z3uCzKXQEfuQK2Jo2mKmUAO9MGUJcxiKbsQtKzeoZ29r0yUjgiM4UT2j3ulZFCz/QUUntoXh2R7ipSLYVJwErn3GoAM3sUOAsIe1FY+Nw9tNZux7mA9xNof+twLgCBtnb3Azicd+sC4Lz1CN0PQMBb19jzOdrdN+e9T7JrIyW440533k4705rIopG+NJFmLfv+EEHN9KCBDBqT0mm2DJqSMmhJyaS+Ry41yRm0pWQR6JGFS8nCpWZiqdm4nP4k5Q4lJb+Inr3z6J+Rwkjt2EWkkyJVFAYBG9o9LgeObL+Cmc0EZgIMGTKk0xvqu/j/GBLYeECv8Xb3hiMJBziSCGCA4TACloTb6zEYzrzXtL/vLImWtExakzNp7VFAoEcm9SlZ1KZmQWoWlppNUloWSWk5JKdn0yMjh9SMHFIyckjNyiEtI4ce6dmQkkVqj1RSgV6d/m2IiHRNpIpCR53LexyG4pybDcwGKCkp6eBgxP3T68r57HJgyUaPpB4kJRvJSUkkJydjlgyW5B0jb0mh+0mAvkeLiHxWpIpCOdD+kleFwKZIbKhXn76ReFsRkW4pUl+Y3wNGmFmxmaUC04HnIrQtEREJk4i0FJxzrWZ2JfAvvENS73POfRyJbYmISPhE7DwF59yLwIuRen8REQk/jbeKiEiIioKIiISoKIiISIiKgoiIhKgoiIhIiLmOrmwS7RBmFcC6LrxFPlAZpjjxRp+9++munxv02bvy2Yc65wr2tVJMFIWuMrOFzrkSv3P4QZ+9+3327vq5QZ89Gp9d3UciIhKioiAiIiGJUhRm+x3AR/rs3U93/dygzx5xCTGmICIi4ZEoLQUREQmDuC4KZnaqma0ws5VmNsvvPNFkZveZ2TYzW+J3lmgys8FmNs/MlpnZx2Z2td+ZosXM0s3sXTP7IPjZf+53pmgzs2Qze9/Mnvc7SzSZ2Voz+8jMFpvZwohuK167j8wsGfgEOAnvoj7vATOcc2G/DnQsMrNjgVrgIefcWL/zRIuZDQAGOOcWmVkOUAac3R3+7mZmQJZzrtbMUoA3gaudcwt8jhY1ZvZDoATo6Zw7w+880WJma4ES51zEz9GI55bCJGClc261c64ZeBQ4y+dMUeOcex3Y7neOaHPObXbOLQrerwGW4V0TPOE5T23wYUrwJz6/1XWCmRUCpwN/8TtLIovnojAI2NDucTndZOcgHjMrAiYA7/ibJHqC3SeLgW3AXOdct/nswF3AT4CA30F84IA5ZlZmZjMjuaF4LgrWwbJu862puzOzbOBJ4AfOuV1+54kW51ybc2483nXPJ5lZt+g6NLMzgG3OuTK/s/jkaOfc4cCXge8Fu48jIp6LQjkwuN3jQmCTT1kkioL96U8CDzvnnvI7jx+cczuA+cCpPkeJlqOBM4N9648Cx5vZ3/yNFD3OuU3B223A03jd5xERz0XhPWCEmRWbWSowHXjO50wSYcHB1nuBZc653/qdJ5rMrMDMegfvZwAnAsv9TRUdzrmfOucKnXNFeP/X/+2cu8jnWFFhZlnBgyowsyzgZCBiRx3GbVFwzrUCVwL/whtsfNw597G/qaLHzB4BSoFRZlZuZt/2O1OUHA18A++b4uLgz2l+h4qSAcA8M/sQ70vRXOdctzo0s5vqB7xpZh8A7wIvOOdejtTG4vaQVBERCb+4bSmIiEj4qSiIiEiIioKIiISoKIiISIiKgoiIhKgoiIhIiIqCiIiEqCiIiEjI/wep//FoouPT2AAAAABJRU5ErkJggg==
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[163]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mf">0.1</span><span class="p">,</span><span class="mf">0.1</span><span class="p">,</span><span class="mf">0.8</span><span class="p">,</span><span class="mf">0.8</span><span class="p">])</span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">x</span><span class="o">**</span><span class="mi">2</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="s2">&quot;X Square&quot;</span><span class="p">)</span>  <span class="c1"># Label is mandatory  for legend</span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">x</span><span class="o">**</span><span class="mi">3</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="s2">&quot;X Cube&quot;</span><span class="p">)</span>

<span class="n">axes</span><span class="o">.</span><span class="n">legend</span><span class="p">(</span><span class="n">loc</span><span class="o">=</span><span class="p">(</span><span class="mf">0.1</span><span class="p">,</span><span class="mf">0.1</span><span class="p">))</span>   <span class="c1"># one more method for setting legend </span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[163]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.legend.Legend at 0x19778081be0&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Setting-colour,-line-size-,-line-size-and-cutomization">Setting colour, line size , line size and cutomization<a class="anchor-link" href="#Setting-colour,-line-size-,-line-size-and-cutomization">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Color">Color<a class="anchor-link" href="#Color">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[170]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">])</span>
<span class="c1">#axes.plot(x,y,color=&#39;green&#39;)</span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">,</span><span class="n">color</span><span class="o">=</span><span class="s1">&#39;#FF8C00&#39;</span><span class="p">)</span>  <span class="c1">#RGB HEX code </span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[170]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x19776a3a630&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Linewidth">Linewidth<a class="anchor-link" href="#Linewidth">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[183]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">])</span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">,</span><span class="n">color</span><span class="o">=</span><span class="s1">&#39;purple&#39;</span><span class="p">,</span> <span class="n">linewidth</span><span class="o">=</span><span class="mi">10</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[183]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x1977863e0f0&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[184]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">])</span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">,</span><span class="n">color</span><span class="o">=</span><span class="s1">&#39;purple&#39;</span><span class="p">,</span> <span class="n">lw</span><span class="o">=</span><span class="mi">10</span><span class="p">)</span> <span class="c1"># alternative to linewidth is &quot;lw&quot;</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[184]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x197786b22e8&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Alfha-argumnet-to-control-transparnat-line">Alfha argumnet to control transparnat line<a class="anchor-link" href="#Alfha-argumnet-to-control-transparnat-line">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[181]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">])</span>

<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">,</span><span class="n">color</span><span class="o">=</span><span class="s1">&#39;green&#39;</span><span class="p">,</span> <span class="n">linewidth</span><span class="o">=</span><span class="mi">5</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[181]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x19776659160&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[182]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">])</span>

<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">,</span><span class="n">color</span><span class="o">=</span><span class="s1">&#39;green&#39;</span><span class="p">,</span> <span class="n">linewidth</span><span class="o">=</span><span class="mi">5</span><span class="p">,</span><span class="n">alpha</span><span class="o">=</span><span class="mf">0.5</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[182]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x197787717b8&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Line-Style">Line Style<a class="anchor-link" href="#Line-Style">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[189]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">])</span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">,</span><span class="n">color</span><span class="o">=</span><span class="s1">&#39;red&#39;</span><span class="p">,</span><span class="n">lw</span><span class="o">=</span><span class="mi">5</span><span class="p">,</span><span class="n">linestyle</span><span class="o">=</span><span class="s1">&#39;--&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[189]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x1977b4fa6d8&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[205]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">])</span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">,</span><span class="n">color</span><span class="o">=</span><span class="s1">&#39;purple&#39;</span><span class="p">,</span><span class="n">lw</span><span class="o">=</span><span class="mi">5</span><span class="p">,</span><span class="n">ls</span><span class="o">=</span><span class="s1">&#39;:&#39;</span><span class="p">)</span>   <span class="c1"># Shortcut is ls for line size</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[205]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x1977cb1db70&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[206]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">])</span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">,</span><span class="n">color</span><span class="o">=</span><span class="s2">&quot;Green&quot;</span><span class="p">,</span><span class="n">lw</span><span class="o">=</span><span class="mi">5</span><span class="p">,</span><span class="n">linestyle</span><span class="o">=</span><span class="s1">&#39;steps&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[206]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x1977cb7da58&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Markers">Markers<a class="anchor-link" href="#Markers">&#182;</a></h1><ul>
<li>tom mark  the point in graph</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[213]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">])</span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">,</span><span class="n">color</span><span class="o">=</span><span class="s1">&#39;red&#39;</span><span class="p">,</span><span class="n">lw</span><span class="o">=</span><span class="s1">&#39;3&#39;</span><span class="p">,</span><span class="n">marker</span><span class="o">=</span><span class="s1">&#39;o&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[213]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x1977cd8d9e8&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[221]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">])</span>
<span class="c1">#axes.plot(x,y,color=&#39;purple&#39;,lw=&#39;3&#39;,marker=&#39;+&#39;)</span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">,</span><span class="n">color</span><span class="o">=</span><span class="s1">&#39;purple&#39;</span><span class="p">,</span><span class="n">lw</span><span class="o">=</span><span class="s1">&#39;1&#39;</span><span class="p">,</span><span class="n">marker</span><span class="o">=</span><span class="s1">&#39;*&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[221]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x1977d0d9fd0&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[225]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">])</span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">,</span><span class="n">lw</span><span class="o">=</span><span class="mi">2</span><span class="p">,</span><span class="n">marker</span><span class="o">=</span><span class="s1">&#39;+&#39;</span><span class="p">,</span><span class="n">markersize</span><span class="o">=</span><span class="mi">20</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[225]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x1977e1c4390&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[227]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">])</span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">,</span><span class="n">lw</span><span class="o">=</span><span class="mi">2</span><span class="p">,</span><span class="n">marker</span><span class="o">=</span><span class="s1">&#39;o&#39;</span><span class="p">,</span><span class="n">markersize</span><span class="o">=</span><span class="mi">20</span><span class="p">,</span><span class="n">markerfacecolor</span><span class="o">=</span><span class="s2">&quot;yellow&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[227]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x1977e20f518&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[228]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">])</span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">,</span><span class="n">lw</span><span class="o">=</span><span class="mi">2</span><span class="p">,</span><span class="n">marker</span><span class="o">=</span><span class="s1">&#39;o&#39;</span><span class="p">,</span><span class="n">markersize</span><span class="o">=</span><span class="mi">20</span><span class="p">,</span><span class="n">markerfacecolor</span><span class="o">=</span><span class="s2">&quot;yellow&quot;</span><span class="p">,</span><span class="n">markeredgewidth</span><span class="o">=</span><span class="mi">3</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[228]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x1977d0c4208&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[229]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">])</span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">,</span><span class="n">lw</span><span class="o">=</span><span class="mi">2</span><span class="p">,</span><span class="n">marker</span><span class="o">=</span><span class="s1">&#39;o&#39;</span><span class="p">,</span><span class="n">markersize</span><span class="o">=</span><span class="mi">20</span><span class="p">,</span><span class="n">markerfacecolor</span><span class="o">=</span><span class="s2">&quot;yellow&quot;</span><span class="p">,</span><span class="n">markeredgewidth</span><span class="o">=</span><span class="mi">3</span><span class="p">,</span><span class="n">markeredgecolor</span><span class="o">=</span><span class="s1">&#39;black&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[229]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x1977e32b390&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Control--over-axis-appearance">Control  over axis appearance<a class="anchor-link" href="#Control--over-axis-appearance">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[234]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">])</span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">,</span><span class="n">lw</span><span class="o">=</span><span class="mi">2</span><span class="p">,</span><span class="n">ls</span><span class="o">=</span><span class="s1">&#39;--&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[234]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x197769de400&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[241]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">axes</span><span class="o">=</span><span class="n">fig</span><span class="o">.</span><span class="n">add_axes</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">])</span>
<span class="n">axes</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">,</span><span class="n">lw</span><span class="o">=</span><span class="mi">2</span><span class="p">,</span><span class="n">ls</span><span class="o">=</span><span class="s1">&#39;--&#39;</span><span class="p">)</span>
<span class="n">axes</span><span class="o">.</span><span class="n">set_xlim</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">])</span>   <span class="c1"># Disply x till 1 </span>
<span class="n">axes</span><span class="o">.</span><span class="n">set_ylim</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">2</span><span class="p">])</span>   <span class="c1"># Disply y till 2</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[241]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(0, 2)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Special-Plot-Type">Special Plot Type<a class="anchor-link" href="#Special-Plot-Type">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="http://dana.loria.fr/doc/tutorial.html"><a href="http://dana.loria.fr/doc/tutorial.html">http://dana.loria.fr/doc/tutorial.html</a><a class="anchor-link" href="#http://dana.loria.fr/doc/tutorial.html">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
    </div>
  </div>
</body>

 


</html>
