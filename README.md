# Sajid Nisar
sajidnisar.github.io


<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />
<title>2RP Manipulator Kinematics DH</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
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
    color: #000 !important;
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
 *  Font Awesome 4.2.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.2.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.2.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.2.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.2.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.2.0#fontawesomeregular') format('svg');
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
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=1);
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2);
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=3);
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1);
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1);
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
.fa-gittip:before {
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
.fa-pied-piper:before {
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
@media (max-width: 991px) {
  #ipython_notebook {
    margin-left: 10px;
  }
}
[dir="rtl"] #ipython_notebook {
  float: right !important;
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
span#login_widget {
  float: right;
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
  text-align: center;
  vertical-align: middle;
  display: inline;
  opacity: 0;
  z-index: 2;
  width: 12ex;
  margin-right: -12ex;
}
.alternate_upload .btn-upload {
  height: 22px;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
[dir="rtl"] #tabs li {
  float: right;
}
ul#tabs {
  margin-bottom: 4px;
}
[dir="rtl"] ul#tabs {
  margin-right: 0px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
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
[dir="rtl"] .list_toolbar .tree-buttons {
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-right {
  padding-top: 1px;
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-left {
  float: right !important;
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
  vertical-align: baseline;
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
#tree-selector {
  padding-right: 0px;
}
[dir="rtl"] #tree-selector a {
  float: right;
}
#button-select-all {
  min-width: 50px;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
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
[dir="rtl"] #new-menu {
  text-align: right;
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
[dir="rtl"] #running .col-sm-8 {
  float: right !important;
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
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI colors. */
.ansibold {
  font-weight: bold;
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
  border-left-width: 1px;
  padding-left: 5px;
  background: linear-gradient(to right, transparent -40px, transparent 1px, transparent 1px, transparent 100%);
}
div.cell.jupyter-soft-selected {
  border-left-color: #90CAF9;
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
div.cell.selected {
  border-color: #ababab;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 5px, transparent 5px, transparent 100%);
}
@media print {
  div.cell.selected {
    border-color: transparent;
  }
}
div.cell.selected.jupyter-soft-selected {
  border-left-width: 0;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 7px, #E3F2FD 7px, #E3F2FD 100%);
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #66BB6A -40px, #66BB6A 5px, transparent 5px, transparent 100%);
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
  padding: 0.4em;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. We need the 0 value because of how we size */
  /* .CodeMirror-lines */
  padding: 0;
  border: 0;
  border-radius: 0;
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
  padding: 0;
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
.rendered_html ul {
  list-style: disc;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ul ul {
  list-style: square;
  margin: 0em 2em;
}
.rendered_html ul ul ul {
  list-style: circle;
  margin: 0em 2em;
}
.rendered_html ol {
  list-style: decimal;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
  margin: 0em 2em;
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
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  background-color: #fff;
  color: #000;
  font-size: 100%;
  padding: 0px;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: 1px solid black;
  border-collapse: collapse;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  border: 1px solid black;
  border-collapse: collapse;
  margin: 1em 2em;
}
.rendered_html td,
.rendered_html th {
  text-align: left;
  vertical-align: middle;
  padding: 4px;
}
.rendered_html th {
  font-weight: bold;
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
.text_cell.unrendered .text_cell_render {
  display: none;
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
#kernel_logo_widget {
  float: right !important;
  float: right;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
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
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
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
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
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
  margin-top: 6px;
}
span.save_widget span.filename {
  height: 1em;
  line-height: 1em;
  padding: 3px;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
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
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
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
  display: none;
}
.command-shortcut:before {
  content: "(command)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
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
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Analytical-Drivation-of-Kinematics-and-Workspace-Evaluation-of-a-2-Link-Planar-Manipulator-Using-Python">Analytical Drivation of Kinematics and Workspace Evaluation of a 2-Link Planar Manipulator Using Python<a class="anchor-link" href="#Analytical-Drivation-of-Kinematics-and-Workspace-Evaluation-of-a-2-Link-Planar-Manipulator-Using-Python">&#182;</a></h1><h2 id="Based-on-Denavit-Hartenberg-(DH)-Convention">Based on Denavit-Hartenberg (DH) Convention<a class="anchor-link" href="#Based-on-Denavit-Hartenberg-(DH)-Convention">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>This is first in a series of articles which aim to explain and interactivey let you develop serial robot kinematics and carry out various useful analyses to understand the design and kienmatic perfromance of robotic manipulators using <strong>Python programing language</strong>.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><h1>Table of Contents<span class="tocSkip"></span></h1></p>
<div class="toc" style="margin-top: 1em;"><ul class="toc-item"><li><span><a href="#Analytical-Drivation-of-Kinematics-and-Workspace-Evaluation-of-a-2-Link-Planar-Manipulator-Using-Python" data-toc-modified-id="Analytical-Drivation-of-Kinematics-and-Workspace-Evaluation-of-a-2-Link-Planar-Manipulator-Using-Python-1">Analytical Drivation of Kinematics and Workspace Evaluation of a 2-Link Planar Manipulator Using Python</a></span><ul class="toc-item"><li><span><a href="#Based-on-Denavit-Hartenberg-(DH)-Convention" data-toc-modified-id="Based-on-Denavit-Hartenberg-(DH)-Convention-1.1">Based on Denavit-Hartenberg (DH) Convention</a></span></li><li><span><a href="#Purpose" data-toc-modified-id="Purpose-1.2">Purpose</a></span></li><li><span><a href="#Prerequisites" data-toc-modified-id="Prerequisites-1.3">Prerequisites</a></span></li><li><span><a href="#Environment-Setup" data-toc-modified-id="Environment-Setup-1.4">Environment Setup</a></span></li><li><span><a href="#2-Link-Planar-(2RP)-Manipulator" data-toc-modified-id="2-Link-Planar-(2RP)-Manipulator-1.5">2-Link Planar (2RP) Manipulator</a></span><ul class="toc-item"><li><ul class="toc-item"><li><span><a href="#Why-2RP-Manipulator?" data-toc-modified-id="Why-2RP-Manipulator?-1.5.0.1">Why 2RP Manipulator?</a></span></li></ul></li></ul></li></ul></li><li><span><a href="#Kinematics-Using-DH-Method" data-toc-modified-id="Kinematics-Using-DH-Method-2">Kinematics Using DH Method</a></span><ul class="toc-item"><li><ul class="toc-item"><li><span><a href="#DH-Table" data-toc-modified-id="DH-Table-2.0.1">DH Table</a></span></li></ul></li><li><span><a href="#Homogenous-Transformation" data-toc-modified-id="Homogenous-Transformation-2.1">Homogenous Transformation</a></span><ul class="toc-item"><li><ul class="toc-item"><li><span><a href="#Transformation:-frame-'0'-to-'1'" data-toc-modified-id="Transformation:-frame-'0'-to-'1'-2.1.0.1">Transformation: frame '0' to '1'</a></span></li><li><span><a href="#Transformation:-frame-'1'-to-'2'" data-toc-modified-id="Transformation:-frame-'1'-to-'2'-2.1.0.2">Transformation: frame '1' to '2'</a></span></li></ul></li><li><span><a href="#Homogenous-transformation:-frame-'0'-to-'2'" data-toc-modified-id="Homogenous-transformation:-frame-'0'-to-'2'-2.1.1">Homogenous transformation: frame '0' to '2'</a></span></li></ul></li><li><span><a href="#Forward-Kinematic-Equations" data-toc-modified-id="Forward-Kinematic-Equations-2.2">Forward Kinematic Equations</a></span><ul class="toc-item"><li><ul class="toc-item"><li><span><a href="#Position-in-x-direction" data-toc-modified-id="Position-in-x-direction-2.2.0.1">Position in x-direction</a></span></li><li><span><a href="#Position-in-y-direction" data-toc-modified-id="Position-in-y-direction-2.2.0.2">Position in y-direction</a></span></li></ul></li></ul></li></ul></li><li><span><a href="#Numerical-evlaution-of-tip-position" data-toc-modified-id="Numerical-evlaution-of-tip-position-3">Numerical evlaution of tip position</a></span></li><li><span><a href="#Manipulator-Workspace" data-toc-modified-id="Manipulator-Workspace-4">Manipulator Workspace</a></span></li></ul></div>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Purpose">Purpose<a class="anchor-link" href="#Purpose">&#182;</a></h2><p>This post provides a basic workflow to derive and analyze kinematics of serial robotic manipulators using Python. Our goal is to provide a staright forward scheme to learn, derive and understand kinematics of serial robots in a nice and interactive manner.</p>
<p>For this purpose, we will be using Jupyter Notebook\Lab environmnt which provides a flexible way to interact with code and display inline plots. You may download and use this book as it is, or just grab the code and run it in any other Python development environment.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Prerequisites">Prerequisites<a class="anchor-link" href="#Prerequisites">&#182;</a></h2><p><strong>Technical side:</strong> Know-how of robot kinemaics is recommened, but not necessary. For advanced usage, e.g. to extend this example to more complex designs, knwoeldge of DH (classic) notation is required. If you don't feel confident about DH parameters, don't worry! You would be able to learn this key concept in robotics through interactive playing here.</p>
<p><strong>Programing side:</strong> Beginner to intermediate level skills with Python and Jupyter Notebooks would be handy. 
The python libraries we will use are:</p>
<ul>
<li>Sympy (for symbolic computation)</li>
<li>Numpy (for numerical computaion) </li>
<li>Plotly (for 3D interactive plotting) </li>
</ul>
<p><strong>Note:</strong> Assuming that you already know how to setup Python and Jupyter Notebook environment, it is not explained here.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Environment-Setup">Environment Setup<a class="anchor-link" href="#Environment-Setup">&#182;</a></h2><p>First, we import the SymPy libraray that will allow us to develop and manipulate symbolic expressions.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">sympy</span> <span class="k">as</span> <span class="nn">sp</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>In SymPy, we initialize printing so that all of the mathematical expressions can be rendered in standard mathematical notation.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[2]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sympy.physics.vector</span> <span class="k">import</span> <span class="n">init_vprinting</span>
<span class="n">init_vprinting</span><span class="p">(</span><span class="n">use_latex</span><span class="o">=</span><span class="s1">&#39;mathjax&#39;</span><span class="p">,</span> <span class="n">pretty_print</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="2-Link-Planar-(2RP)-Manipulator">2-Link Planar (2RP) Manipulator<a class="anchor-link" href="#2-Link-Planar-(2RP)-Manipulator">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The Jupyter notebook can use IPython to display rich content. Here, We will use the Image function to import the geometric represnttion of 2-link manipulator example.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[3]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">IPython.display</span> <span class="k">import</span> <span class="n">Image</span>
<span class="n">Image</span><span class="p">(</span><span class="s1">&#39;fig/2rp.png&#39;</span><span class="p">,</span> <span class="n">width</span><span class="o">=</span><span class="mi">300</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[3]:</div>




<div class="output_png output_subarea output_execute_result">
<img src="data:image/png;base64,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
"
width=300
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Why-2RP-Manipulator?">Why 2RP Manipulator?<a class="anchor-link" href="#Why-2RP-Manipulator?">&#182;</a></h4><p>Almost every (under)gradute level robotics textbook, as far as I know, starts teaching robot kinematics using a simple and basic manipulator example called 2-link planar manipulator (sometimes called as 2RP manipulator, R stands for the revolute joints). For sake of simplicity and as a starting point, we also start with the 2-link planar manipulator example which should be easy to follow and understad the underlying science.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Now, we declare the symbols (link lenghts, joint variables etc.) which will be used for further formulation.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sympy.physics.mechanics</span> <span class="k">import</span> <span class="n">dynamicsymbols</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[5]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">theta1</span><span class="p">,</span> <span class="n">theta2</span><span class="p">,</span> <span class="n">l1</span><span class="p">,</span> <span class="n">l2</span><span class="p">,</span> <span class="n">theta</span><span class="p">,</span> <span class="n">alpha</span><span class="p">,</span> <span class="n">a</span><span class="p">,</span> <span class="n">d</span> <span class="o">=</span> <span class="n">dynamicsymbols</span><span class="p">(</span><span class="s1">&#39;theta1 theta2 l1 l2 theta alpha a d&#39;</span><span class="p">)</span>
<span class="n">theta1</span><span class="p">,</span> <span class="n">theta2</span><span class="p">,</span> <span class="n">l1</span><span class="p">,</span> <span class="n">l2</span><span class="p">,</span> <span class="n">theta</span><span class="p">,</span> <span class="n">alpha</span><span class="p">,</span> <span class="n">a</span><span class="p">,</span> <span class="n">d</span> 
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[5]:</div>




<div class="output_latex output_subarea output_execute_result">
$$\left ( \theta_{1}, \quad \theta_{2}, \quad l_{1}, \quad l_{2}, \quad \theta, \quad \alpha, \quad a, \quad d\right )$$
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Kinematics-Using-DH-Method">Kinematics Using DH Method<a class="anchor-link" href="#Kinematics-Using-DH-Method">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>We assign the frames to our manipulator according to DH classic convention. DH method provides a convenient way to express the position and orienation of a rigid-body in matrix forms using the relevant link lengths, joint angles, twist angles and joint offsets.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="DH-Table">DH Table<a class="anchor-link" href="#DH-Table">&#182;</a></h3><p>The DH table for 2-Link Planar Mnipulator shown above can be formulated as,</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>\begin{array}{cccc}
\hline 
\hline
i &amp; \alpha_{i} &amp; a_{i} &amp; d_i &amp; \theta_i \\ 
\hline
\hline
1 &amp; 0 &amp; l_1 &amp; 0 &amp; \theta_1 \\
2 &amp; 0 &amp; l_2 &amp; 0 &amp; \theta_2 \\
%3 &amp; -\frac{\pi}{2} &amp; 0 &amp; 0 &amp; -\frac{\pi}{2} - \phi_1 \\
%4 &amp; 0 &amp; 0 &amp; l_1 &amp; 0 \\
\hline
\end{array}</p>
<p>$i$: joint number, $\alpha_i$: twist angle, $a_i$: length of link $i$, $d_i$: joint offset and $\theta_i$: joint angle.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Homogenous-Transformation">Homogenous Transformation<a class="anchor-link" href="#Homogenous-Transformation">&#182;</a></h2><p>The standard homogenous transformation matrix (transaformation from base to tip frame) is represnted as,</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">rot</span> <span class="o">=</span> <span class="n">sp</span><span class="o">.</span><span class="n">Matrix</span><span class="p">([[</span><span class="n">sp</span><span class="o">.</span><span class="n">cos</span><span class="p">(</span><span class="n">theta</span><span class="p">),</span> <span class="o">-</span><span class="n">sp</span><span class="o">.</span><span class="n">sin</span><span class="p">(</span><span class="n">theta</span><span class="p">)</span><span class="o">*</span><span class="n">sp</span><span class="o">.</span><span class="n">cos</span><span class="p">(</span><span class="n">alpha</span><span class="p">),</span> <span class="n">sp</span><span class="o">.</span><span class="n">sin</span><span class="p">(</span><span class="n">theta</span><span class="p">)</span><span class="o">*</span><span class="n">sp</span><span class="o">.</span><span class="n">sin</span><span class="p">(</span><span class="n">alpha</span><span class="p">)],</span>
             <span class="p">[</span><span class="n">sp</span><span class="o">.</span><span class="n">sin</span><span class="p">(</span><span class="n">theta</span><span class="p">),</span> <span class="n">sp</span><span class="o">.</span><span class="n">cos</span><span class="p">(</span><span class="n">theta</span><span class="p">)</span><span class="o">*</span><span class="n">sp</span><span class="o">.</span><span class="n">cos</span><span class="p">(</span><span class="n">alpha</span><span class="p">),</span> <span class="o">-</span><span class="n">sp</span><span class="o">.</span><span class="n">cos</span><span class="p">(</span><span class="n">theta</span><span class="p">)</span><span class="o">*</span><span class="n">sp</span><span class="o">.</span><span class="n">sin</span><span class="p">(</span><span class="n">alpha</span><span class="p">)],</span>
             <span class="p">[</span><span class="mi">0</span><span class="p">,</span> <span class="n">sp</span><span class="o">.</span><span class="n">sin</span><span class="p">(</span><span class="n">alpha</span><span class="p">),</span> <span class="n">sp</span><span class="o">.</span><span class="n">cos</span><span class="p">(</span><span class="n">alpha</span><span class="p">)]])</span>

<span class="n">trans</span> <span class="o">=</span> <span class="n">sp</span><span class="o">.</span><span class="n">Matrix</span><span class="p">([</span><span class="n">a</span><span class="o">*</span><span class="n">sp</span><span class="o">.</span><span class="n">cos</span><span class="p">(</span><span class="n">theta</span><span class="p">),</span><span class="n">a</span><span class="o">*</span><span class="n">sp</span><span class="o">.</span><span class="n">sin</span><span class="p">(</span><span class="n">theta</span><span class="p">),</span><span class="n">d</span><span class="p">])</span>

<span class="n">last_row</span> <span class="o">=</span> <span class="n">sp</span><span class="o">.</span><span class="n">Matrix</span><span class="p">([[</span><span class="mi">0</span><span class="p">,</span> <span class="mi">0</span><span class="p">,</span> <span class="mi">0</span><span class="p">,</span> <span class="mi">1</span><span class="p">]])</span>

<span class="n">m</span> <span class="o">=</span> <span class="n">sp</span><span class="o">.</span><span class="n">Matrix</span><span class="o">.</span><span class="n">vstack</span><span class="p">(</span><span class="n">sp</span><span class="o">.</span><span class="n">Matrix</span><span class="o">.</span><span class="n">hstack</span><span class="p">(</span><span class="n">rot</span><span class="p">,</span> <span class="n">trans</span><span class="p">),</span> <span class="n">last_row</span><span class="p">)</span>
<span class="n">m</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[6]:</div>




<div class="output_latex output_subarea output_execute_result">
$$\left[\begin{matrix}\operatorname{cos}\left(\theta\right) & - \operatorname{sin}\left(\theta\right) \operatorname{cos}\left(\alpha\right) & \operatorname{sin}\left(\alpha\right) \operatorname{sin}\left(\theta\right) & a \operatorname{cos}\left(\theta\right)\\\operatorname{sin}\left(\theta\right) & \operatorname{cos}\left(\alpha\right) \operatorname{cos}\left(\theta\right) & - \operatorname{sin}\left(\alpha\right) \operatorname{cos}\left(\theta\right) & a \operatorname{sin}\left(\theta\right)\\0 & \operatorname{sin}\left(\alpha\right) & \operatorname{cos}\left(\alpha\right) & d\\0 & 0 & 0 & 1\end{matrix}\right]$$
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Transformation:-frame-'0'-to-'1'">Transformation: frame '0' to '1'<a class="anchor-link" href="#Transformation:-frame-'0'-to-'1'">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">m01</span> <span class="o">=</span> <span class="n">m</span><span class="o">.</span><span class="n">subs</span><span class="p">({</span><span class="n">alpha</span><span class="p">:</span><span class="mi">0</span><span class="p">,</span> <span class="n">a</span><span class="p">:</span><span class="n">l1</span><span class="p">,</span> <span class="n">theta</span><span class="p">:</span><span class="n">theta1</span><span class="p">,</span> <span class="n">d</span><span class="p">:</span><span class="mi">0</span><span class="p">})</span>
<span class="n">m01</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[7]:</div>




<div class="output_latex output_subarea output_execute_result">
$$\left[\begin{matrix}\operatorname{cos}\left(\theta_{1}\right) & - \operatorname{sin}\left(\theta_{1}\right) & 0 & l_{1} \operatorname{cos}\left(\theta_{1}\right)\\\operatorname{sin}\left(\theta_{1}\right) & \operatorname{cos}\left(\theta_{1}\right) & 0 & l_{1} \operatorname{sin}\left(\theta_{1}\right)\\0 & 0 & 1 & 0\\0 & 0 & 0 & 1\end{matrix}\right]$$
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Transformation:-frame-'1'-to-'2'">Transformation: frame '1' to '2'<a class="anchor-link" href="#Transformation:-frame-'1'-to-'2'">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">m12</span> <span class="o">=</span> <span class="n">m</span><span class="o">.</span><span class="n">subs</span><span class="p">({</span><span class="n">alpha</span><span class="p">:</span><span class="mi">0</span><span class="p">,</span> <span class="n">a</span><span class="p">:</span><span class="n">l2</span><span class="p">,</span> <span class="n">theta</span><span class="p">:</span><span class="n">theta2</span><span class="p">,</span> <span class="n">d</span><span class="p">:</span><span class="mi">0</span><span class="p">})</span>
<span class="n">m12</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[8]:</div>




<div class="output_latex output_subarea output_execute_result">
$$\left[\begin{matrix}\operatorname{cos}\left(\theta_{2}\right) & - \operatorname{sin}\left(\theta_{2}\right) & 0 & l_{2} \operatorname{cos}\left(\theta_{2}\right)\\\operatorname{sin}\left(\theta_{2}\right) & \operatorname{cos}\left(\theta_{2}\right) & 0 & l_{2} \operatorname{sin}\left(\theta_{2}\right)\\0 & 0 & 1 & 0\\0 & 0 & 0 & 1\end{matrix}\right]$$
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Homogenous-transformation:-frame-'0'-to-'2'">Homogenous transformation: frame '0' to '2'<a class="anchor-link" href="#Homogenous-transformation:-frame-'0'-to-'2'">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[9]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">m02</span> <span class="o">=</span> <span class="p">(</span><span class="n">m01</span><span class="o">*</span><span class="n">m12</span><span class="p">)</span>
<span class="n">m02</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[9]:</div>




<div class="output_latex output_subarea output_execute_result">
$$\left[\begin{matrix}- \operatorname{sin}\left(\theta_{1}\right) \operatorname{sin}\left(\theta_{2}\right) + \operatorname{cos}\left(\theta_{1}\right) \operatorname{cos}\left(\theta_{2}\right) & - \operatorname{sin}\left(\theta_{1}\right) \operatorname{cos}\left(\theta_{2}\right) - \operatorname{sin}\left(\theta_{2}\right) \operatorname{cos}\left(\theta_{1}\right) & 0 & l_{1} \operatorname{cos}\left(\theta_{1}\right) - l_{2} \operatorname{sin}\left(\theta_{1}\right) \operatorname{sin}\left(\theta_{2}\right) + l_{2} \operatorname{cos}\left(\theta_{1}\right) \operatorname{cos}\left(\theta_{2}\right)\\\operatorname{sin}\left(\theta_{1}\right) \operatorname{cos}\left(\theta_{2}\right) + \operatorname{sin}\left(\theta_{2}\right) \operatorname{cos}\left(\theta_{1}\right) & - \operatorname{sin}\left(\theta_{1}\right) \operatorname{sin}\left(\theta_{2}\right) + \operatorname{cos}\left(\theta_{1}\right) \operatorname{cos}\left(\theta_{2}\right) & 0 & l_{1} \operatorname{sin}\left(\theta_{1}\right) + l_{2} \operatorname{sin}\left(\theta_{1}\right) \operatorname{cos}\left(\theta_{2}\right) + l_{2} \operatorname{sin}\left(\theta_{2}\right) \operatorname{cos}\left(\theta_{1}\right)\\0 & 0 & 1 & 0\\0 & 0 & 0 & 1\end{matrix}\right]$$
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Using Sympy's built-in simplification methods, we simplify the transformation matrix as</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">mbee</span><span class="o">=</span> <span class="n">sp</span><span class="o">.</span><span class="n">Matrix</span><span class="p">([[</span><span class="n">m02</span><span class="p">[</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">simplify</span><span class="p">(),</span> <span class="n">m02</span><span class="p">[</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">simplify</span><span class="p">(),</span> <span class="n">sp</span><span class="o">.</span><span class="n">trigsimp</span><span class="p">(</span><span class="n">m02</span><span class="p">[</span><span class="mi">0</span><span class="p">,</span><span class="mi">3</span><span class="p">]</span><span class="o">.</span><span class="n">simplify</span><span class="p">())],</span>
              <span class="p">[</span><span class="n">m02</span><span class="p">[</span><span class="mi">1</span><span class="p">,</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">simplify</span><span class="p">(),</span> <span class="n">m02</span><span class="p">[</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">simplify</span><span class="p">(),</span> <span class="n">sp</span><span class="o">.</span><span class="n">trigsimp</span><span class="p">(</span><span class="n">m02</span><span class="p">[</span><span class="mi">1</span><span class="p">,</span><span class="mi">3</span><span class="p">]</span><span class="o">.</span><span class="n">simplify</span><span class="p">())],</span>
              <span class="p">[</span><span class="n">m02</span><span class="p">[</span><span class="mi">2</span><span class="p">,</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">simplify</span><span class="p">(),</span> <span class="n">m02</span><span class="p">[</span><span class="mi">2</span><span class="p">,</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">simplify</span><span class="p">(),</span> <span class="n">m02</span><span class="p">[</span><span class="mi">2</span><span class="p">,</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">simplify</span><span class="p">()]])</span>

<span class="n">mbee</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[10]:</div>




<div class="output_latex output_subarea output_execute_result">
$$\left[\begin{matrix}\operatorname{cos}\left(\theta_{1} + \theta_{2}\right) & - \operatorname{sin}\left(\theta_{1} + \theta_{2}\right) & l_{1} \operatorname{cos}\left(\theta_{1}\right) + l_{2} \operatorname{cos}\left(\theta_{1} + \theta_{2}\right)\\\operatorname{sin}\left(\theta_{1} + \theta_{2}\right) & \operatorname{cos}\left(\theta_{1} + \theta_{2}\right) & l_{1} \operatorname{sin}\left(\theta_{1}\right) + l_{2} \operatorname{sin}\left(\theta_{1} + \theta_{2}\right)\\0 & 0 & 1\end{matrix}\right]$$
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The first two columns in above matrix describe the orienation of the tip of manipulator in X, Y and Z directions. Whereas, the last column represnts the position in respective directions.
As our manipulator does not carry any end-effector, analyses of orientaion becomes meaningless.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Forward-Kinematic-Equations">Forward Kinematic Equations<a class="anchor-link" href="#Forward-Kinematic-Equations">&#182;</a></h2><p>The tip position can be expressed as,</p>
<h4 id="Position-in-x-direction">Position in x-direction<a class="anchor-link" href="#Position-in-x-direction">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[11]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">px</span> <span class="o">=</span> <span class="n">mbee</span><span class="p">[</span><span class="mi">0</span><span class="p">,</span><span class="mi">2</span><span class="p">]</span>
<span class="n">px</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[11]:</div>




<div class="output_latex output_subarea output_execute_result">
$$l_{1} \operatorname{cos}\left(\theta_{1}\right) + l_{2} \operatorname{cos}\left(\theta_{1} + \theta_{2}\right)$$
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Position-in-y-direction">Position in y-direction<a class="anchor-link" href="#Position-in-y-direction">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[12]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">py</span> <span class="o">=</span> <span class="n">mbee</span><span class="p">[</span><span class="mi">1</span><span class="p">,</span><span class="mi">2</span><span class="p">]</span>
<span class="n">py</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[12]:</div>




<div class="output_latex output_subarea output_execute_result">
$$l_{1} \operatorname{sin}\left(\theta_{1}\right) + l_{2} \operatorname{sin}\left(\theta_{1} + \theta_{2}\right)$$
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Numerical-evlaution-of-tip-position">Numerical evlaution of tip position<a class="anchor-link" href="#Numerical-evlaution-of-tip-position">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>To evaluate tip position numerically, we make use of Sympy's lambdify function which takes $l_1$, $l_2$, $\theta_1$ and $\phi_1$ as arguments.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[13]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fx</span> <span class="o">=</span> <span class="n">sp</span><span class="o">.</span><span class="n">lambdify</span><span class="p">((</span><span class="n">l1</span><span class="p">,</span> <span class="n">l2</span><span class="p">,</span> <span class="n">theta1</span><span class="p">,</span> <span class="n">theta2</span><span class="p">),</span> <span class="n">px</span><span class="p">,</span> <span class="s1">&#39;numpy&#39;</span><span class="p">)</span>
<span class="n">fy</span> <span class="o">=</span> <span class="n">sp</span><span class="o">.</span><span class="n">lambdify</span><span class="p">((</span><span class="n">l1</span><span class="p">,</span> <span class="n">l2</span><span class="p">,</span> <span class="n">theta1</span><span class="p">,</span> <span class="n">theta2</span><span class="p">),</span> <span class="n">py</span><span class="p">,</span> <span class="s1">&#39;numpy&#39;</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>To plot tip position in X and Y, we import Matplotlib and Numpy. For inline plot display, we use Ipython magic.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[14]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="o">%</span><span class="k">matplotlib</span> inline
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="n">d2r</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">deg2rad</span> <span class="c1"># for degree to radian conversion</span>
<span class="n">r2d</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">rad2deg</span> <span class="c1"># for radian to degree conversion</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[15]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">theta1s</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="n">d2r</span><span class="p">(</span><span class="mi">0</span><span class="p">),</span> <span class="n">d2r</span><span class="p">(</span><span class="mi">360</span><span class="p">))</span> <span class="c1"># desired range of motion for joint 1</span>
<span class="n">theta2s</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="n">d2r</span><span class="p">(</span><span class="mi">0</span><span class="p">),</span> <span class="n">d2r</span><span class="p">(</span><span class="mi">360</span><span class="p">))</span> <span class="c1"># desired range of motion for joint 2</span>

<span class="n">zx</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">(</span><span class="n">fx</span><span class="p">(</span><span class="mf">15.0</span><span class="p">,</span> <span class="mf">15.0</span><span class="p">,</span> <span class="n">theta1s</span><span class="p">,</span> <span class="n">theta2s</span><span class="p">))</span>
<span class="n">zy</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">(</span><span class="n">fy</span><span class="p">(</span><span class="mf">15.0</span><span class="p">,</span> <span class="mf">15.0</span><span class="p">,</span> <span class="n">theta1s</span><span class="p">,</span> <span class="n">theta2s</span><span class="p">))</span>

<span class="n">fig</span><span class="p">,</span> <span class="n">ax1</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">()</span>
<span class="n">ax1</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">r2d</span><span class="p">(</span><span class="n">theta1s</span><span class="p">),</span> <span class="n">zx</span><span class="p">,</span> <span class="n">label</span> <span class="o">=</span> <span class="sa">r</span><span class="s1">&#39;$p_x$&#39;</span><span class="p">)</span>
<span class="n">ax1</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">r2d</span><span class="p">(</span><span class="n">theta1s</span><span class="p">),</span> <span class="n">zy</span><span class="p">,</span> <span class="n">label</span> <span class="o">=</span> <span class="sa">r</span><span class="s1">&#39;$p_y$&#39;</span><span class="p">)</span>
<span class="n">ax1</span><span class="o">.</span><span class="n">set_xlabel</span><span class="p">(</span><span class="sa">r</span><span class="s1">&#39;($\theta_1$, $\theta_2$) [deg]&#39;</span><span class="p">)</span>
<span class="n">ax1</span><span class="o">.</span><span class="n">set_ylabel</span><span class="p">(</span><span class="sa">r</span><span class="s1">&#39; tip position [mm]&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">()</span>
<span class="n">plt</span><span class="o">.</span><span class="n">grid</span><span class="p">()</span>
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
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Manipulator-Workspace">Manipulator Workspace<a class="anchor-link" href="#Manipulator-Workspace">&#182;</a></h1><p>The next step is to visualize the workspce of our manipulator. For this purpose, we will import Plotly and make sure that it displays inline plot in our notebook environment.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[16]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">plotly.offline</span> <span class="k">import</span> <span class="n">download_plotlyjs</span><span class="p">,</span> <span class="n">init_notebook_mode</span><span class="p">,</span> <span class="n">plot</span><span class="p">,</span> <span class="n">iplot</span>
<span class="n">init_notebook_mode</span><span class="p">(</span><span class="n">connected</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span> <span class="c1"># for offline mode in Jupyter Notebook use</span>

<span class="kn">import</span> <span class="nn">plotly.offline</span> <span class="k">as</span> <span class="nn">py</span>
<span class="kn">import</span> <span class="nn">plotly.graph_objs</span> <span class="k">as</span> <span class="nn">go</span>
<span class="kn">from</span> <span class="nn">numpy</span> <span class="k">import</span> <span class="o">*</span> <span class="c1"># Not recommended, but we use to avoid rewriting the forward kinematic equations with prefix &#39;np&#39;</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
<script>requirejs.config({paths: { 'plotly': ['https://cdn.plot.ly/plotly-latest.min']},});if(!window.Plotly) {{require(['plotly'],function(plotly) {window.Plotly=plotly;});}}</script>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[17]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">theta11</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="n">d2r</span><span class="p">(</span><span class="mi">0</span><span class="p">),</span><span class="n">d2r</span><span class="p">(</span><span class="mi">90</span><span class="p">))</span>
<span class="n">theta22</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="n">d2r</span><span class="p">(</span><span class="mi">0</span><span class="p">),</span> <span class="n">d2r</span><span class="p">(</span><span class="mi">360</span><span class="p">))</span>
<span class="n">theta1</span><span class="p">,</span> <span class="n">theta2</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">meshgrid</span><span class="p">(</span><span class="n">theta11</span><span class="p">,</span> <span class="n">theta22</span><span class="p">)</span>
<span class="n">l_range</span> <span class="o">=</span> <span class="p">[</span><span class="mi">5</span><span class="p">]</span> <span class="c1"># we can use more than one value here</span>

<span class="n">px1</span> <span class="o">=</span> <span class="p">{}</span>
<span class="n">py1</span> <span class="o">=</span> <span class="p">{}</span>
<span class="n">pz1</span> <span class="o">=</span> <span class="p">{}</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">l_range</span><span class="p">:</span>
    <span class="n">l1</span> <span class="o">=</span> <span class="n">i</span>
    <span class="n">l2</span> <span class="o">=</span> <span class="n">i</span> <span class="o">-</span> <span class="mi">4</span>
    
    <span class="n">pxa</span> <span class="o">=</span> <span class="n">l1</span><span class="o">*</span><span class="n">cos</span><span class="p">(</span><span class="n">theta1</span><span class="p">)</span> <span class="o">+</span> <span class="n">l2</span><span class="o">*</span><span class="n">cos</span><span class="p">(</span><span class="n">theta1</span> <span class="o">+</span> <span class="n">theta2</span><span class="p">)</span>
    <span class="n">pya</span> <span class="o">=</span> <span class="n">l1</span><span class="o">*</span><span class="n">sin</span><span class="p">(</span><span class="n">theta1</span><span class="p">)</span> <span class="o">+</span> <span class="n">l2</span><span class="o">*</span><span class="n">sin</span><span class="p">(</span><span class="n">theta1</span> <span class="o">+</span> <span class="n">theta2</span><span class="p">)</span>
    
    <span class="n">px1</span><span class="p">[</span><span class="s1">&#39;x</span><span class="si">{0}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">i</span><span class="p">)]</span> <span class="o">=</span> <span class="n">pxa</span>
    <span class="n">py1</span><span class="p">[</span><span class="s1">&#39;x</span><span class="si">{0}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">i</span><span class="p">)]</span> <span class="o">=</span> <span class="n">pya</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[18]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">pxx</span> <span class="o">=</span> <span class="n">px1</span><span class="p">[</span><span class="s1">&#39;x5&#39;</span><span class="p">]</span>
<span class="n">pyy</span> <span class="o">=</span> <span class="n">py1</span><span class="p">[</span><span class="s1">&#39;x5&#39;</span><span class="p">]</span>
<span class="n">pzz</span> <span class="o">=</span> <span class="n">pyy</span><span class="o">*</span><span class="mi">0</span> <span class="c1">#dummy zero points for z-axis, as it doesn&#39;t exist</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[19]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">trace1</span> <span class="o">=</span> <span class="n">go</span><span class="o">.</span><span class="n">Surface</span><span class="p">(</span><span class="n">z</span><span class="o">=</span><span class="n">pzz</span><span class="p">,</span> <span class="n">x</span><span class="o">=</span><span class="n">pyy</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="n">pxx</span><span class="p">,</span>
                    <span class="n">colorscale</span><span class="o">=</span><span class="s1">&#39;Reds&#39;</span><span class="p">,</span> 
                    <span class="n">showscale</span><span class="o">=</span><span class="kc">False</span><span class="p">,</span> 
                    <span class="n">opacity</span><span class="o">=</span><span class="mf">0.7</span><span class="p">,</span>
                   <span class="p">)</span>
<span class="n">data</span> <span class="o">=</span> <span class="p">[</span><span class="n">trace1</span><span class="p">]</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[20]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">layout</span> <span class="o">=</span> <span class="n">go</span><span class="o">.</span><span class="n">Layout</span><span class="p">(</span>
    <span class="n">scene</span> <span class="o">=</span> <span class="nb">dict</span><span class="p">(</span>
                    <span class="n">xaxis</span> <span class="o">=</span> <span class="nb">dict</span><span class="p">(</span>
                        <span class="n">title</span><span class="o">=</span><span class="s1">&#39;Trans (mm)&#39;</span><span class="p">,</span>
                    <span class="p">),</span>
                    <span class="n">yaxis</span> <span class="o">=</span> <span class="nb">dict</span><span class="p">(</span>
                        <span class="n">title</span><span class="o">=</span><span class="s1">&#39;Yaw (mm)&#39;</span><span class="p">,</span> 
                    <span class="p">),</span>
                    <span class="n">zaxis</span> <span class="o">=</span> <span class="nb">dict</span><span class="p">(</span>
                        <span class="n">title</span><span class="o">=</span><span class="s1">&#39;Pitch (mm)&#39;</span><span class="p">,</span>
                    <span class="p">),),</span>
<span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[21]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span> <span class="o">=</span> <span class="n">go</span><span class="o">.</span><span class="n">Figure</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">data</span><span class="p">,</span> <span class="n">layout</span><span class="o">=</span><span class="n">layout</span><span class="p">)</span>
<span class="n">py</span><span class="o">.</span><span class="n">iplot</span><span class="p">(</span><span class="n">fig</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>



<div class="output_html rendered_html output_subarea ">
<div id="38ab2aa3-3adb-4a3d-b9c1-df3e236fc588" style="height: 525px; width: 100%;" class="plotly-graph-div"></div><script type="text/javascript">require(["plotly"], function(Plotly) { window.PLOTLYENV=window.PLOTLYENV || {};window.PLOTLYENV.BASE_URL="https://plot.ly";Plotly.newPlot("38ab2aa3-3adb-4a3d-b9c1-df3e236fc588", [{"type": "surface", "z": [[0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, -0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, -0.0, -0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, -0.0, -0.0, -0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, -0.0, -0.0, -0.0, -0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, -0.0, -0.0, -0.0, -0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, -0.0, -0.0, -0.0, -0.0, -0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, -0.0, -0.0, -0.0, -0.0, -0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, -0.0, -0.0, -0.0, -0.0, -0.0, -0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, -0.0, -0.0, -0.0, -0.0, -0.0, -0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, -0.0, -0.0, -0.0, -0.0, -0.0, -0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, -0.0, -0.0, -0.0, -0.0, -0.0, -0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, -0.0, -0.0, -0.0, -0.0, -0.0, -0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, -0.0, -0.0, -0.0, -0.0, -0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, -0.0, -0.0, -0.0, -0.0, -0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, -0.0, -0.0, -0.0, -0.0, -0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, -0.0, -0.0, -0.0, -0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, -0.0, -0.0, -0.0, -0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, -0.0, -0.0, -0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, -0.0, -0.0, -0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, -0.0, -0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, -0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, -0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [-0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0]], "x": [[0.0, 0.19230946542993102, 0.3844213198842775, 0.5761381554460905, 0.767262970107036, 0.9575993702002752, 1.1469517722082336, 1.3351256037378862, 1.5219275034570443, 1.7071655197861944, 1.890649308141724, 2.0721903265278456, 2.2516020292762446, 2.428700058734363, 2.603302434705349, 2.7752297414450116, 2.944305312023627, 3.1103554098631494, 3.273209407263292, 3.4326999607330175, 3.5886631829472955, 3.7409388111524007, 3.88937037184673, 4.033805341567901, 4.174095303620918, 4.310096100586365, 4.441667982451893, 4.568675750214806, 4.690988894808179, 4.808481731207739, 4.921033527581736, 5.028528629351044, 5.130856578032076, 5.2279122247403365, 5.319595838238, 5.405813207414515, 5.4864757380948745, 5.5615005440761305, 5.630810532298563, 5.694334482064012, 5.752007118219963, 5.803769178234176, 5.849567473090942, 5.889354941946392, 5.923090700486701, 5.950740082939477, 5.972274677695189, 5.987672356502019, 5.996917297204127, 6.0], [0.127877161684506, 0.319857782891655, 0.5115097286049368, 0.7026360634947231, 0.8930403923320374, 1.0825270617979283, 1.270901361530482, 1.4579697242028795, 1.6435399244269109, 1.8274212762775557, 2.0094248292356616, 2.1893635623473733, 2.367052576400808, 2.542309283922494, 2.714953596798339, 2.884808111326346, 3.051698290510905, 3.215452643411358, 3.3759029013605315, 3.5328841908721644, 3.6862352030595655, 3.835798359391395, 3.981419973614257, 4.122950409675719, 4.2602442354854615, 4.393160372356594, 4.521562239973534, 4.645317896737512, 4.764300175345495, 4.878386813463172, 4.98746057935778, 5.091409392361622, 5.190126438042543, 5.283510277962969, 5.37146495391476, 5.453900086522765, 5.530730968115723, 5.601878649769138, 5.667270022430626, 5.726837892044409, 5.780521048597753, 5.828264329018392, 5.870018673858317, 5.9057411777056625, 5.935395133272938, 5.958950069116231, 5.976381780946679, 5.987672356502019, 5.9928101939526375, 5.9917900138232465], [0.25365458390950735, 0.4447854744893083, 0.6354593179271852, 0.8254801839597163, 1.0146528133019042, 1.2027828182892897, 1.3896768826244195, 1.5751429600224072, 1.7589904715514746, 1.9410305014656868, 2.121075991328652, 2.2989419322287077, 2.4744455548880864, 2.6474065174707024, 2.817647090895579, 2.9849923414654933, 3.1492703106231756, 3.310312191650352, 3.4679525031280587, 3.6220292589799823, 3.772384134924109, 3.918862631161624, 4.061314231135897, 4.199592556198425, 4.333555516022778, 4.4630654546120265, 4.587989291749578, 4.708198659748091, 4.823570035355962, 4.933984866685805, 5.0393296950345405, 5.139496271469872, 5.23438166806339, 5.3238883836559765, 5.407924444046824, 5.486403496503161, 5.559244898493512, 5.626373800553355, 5.687721223198, 5.74322412780368, 5.79282548138399, 5.836474315195146, 5.874125777109806, 5.9057411777056625, 5.931288030021449, 5.950740082939477, 5.964077348160441, 5.9712861207427474, 5.972358993185263, 5.9672948630390295], [0.3752670048793741, 0.5650412309806696, 0.7542348390211226, 0.942653419779244, 1.1301033604264679, 1.3163920434774208, 1.50132804471741, 1.6847213299037416, 1.8663834500387528, 2.0461277350138953, 2.2237694854258914, 2.399126162367855, 2.572017575000357, 2.7422660657096967, 2.9096966926631063, 3.0741374095733107, 3.235419242487719, 3.393376463420581, 3.547846760649699, 3.6986714055026884, 3.8456954154614253, 3.9887677134170567, 4.127741282911941, 4.262473319209003, 4.392825376033245, 4.51866350783466, 4.639858407426338, 4.75628553885634, 4.86782526537681, 4.974362972378812, 5.075789185166603, 5.171999681450268, 5.2628955984411805, 5.3483835344401935, 5.428375644814198, 5.502789732262432, 5.5715493312797495, 5.634583786730109, 5.69182832644949, 5.74322412780368, 5.788718378132501, 5.828264329018393, 5.861821344323569, 5.889354941946392, 5.910836829254074, 5.92624493215526, 5.935563417782652, 5.938782710762351, 5.9358995030532, 5.926916757346022], [0.49071755200393785, 0.6786504561688008, 0.8658860011141132, 1.0522317896605782, 1.2374963389137459, 1.4214892770256293, 1.6040215388146497, 1.7849055600428887, 1.9639554701510233, 2.1409872832528896, 2.315819087193419, 2.4882712304756724, 2.6581665068649003, 2.825330337479926, 2.9895909501847466, 3.150779556096017, 3.3087305230250355, 3.463281545676014, 3.6142738124257434, 3.761552168513267, 3.9049652754718918, 4.0443657666396895, 4.179610398588702, 4.310560198317253, 4.437080606054092, 4.559041613527667, 4.676317897558401, 4.7887889488367374, 4.896339195754599, 4.998858123163029, 5.096240385933978, 5.188385917209539, 5.275200031227418, 5.356593520616947, 5.432482748065688, 5.502789732262432, 5.56744222802826, 5.626373800553355, 5.679523893663252, 5.726837892044409, 5.768267177365126, 5.803769178234176, 5.8333074139457795, 5.8568515319659955, 5.874377339122011, 5.8858668264622525, 5.891308187761804, 5.890695831654101, 5.8840303873764395, 5.871318704123389], [0.5981105304912159, 0.7837476897170094, 0.9685794952113529, 1.1524160197997255, 1.3350683590260162, 1.5163488252646236, 1.696071140582177, 1.874050628150706, 2.0501044020155668, 2.2240515550231184, 2.395713344715059, 2.5649133769983785, 2.7314777874022163, 2.8952354197353585, 3.0560180019607905, 3.2136603191065953, 3.3680003830355014, 3.5188795988986463, 3.6661429281025035, 3.8096390476215163, 3.94922050549274, 4.084743872332696, 4.2160698887207655, 4.3430636082976495, 4.465594536431882, 4.583536764311884, 4.696769098325776, 4.805175184596008, 4.908643628540837, 5.007068109339783, 5.100347489185467, 5.188385917209539, 5.271092927975928, 5.3483835344401935, 5.4201783152794505, 5.486403496503161, 5.546991027260885, 5.601878649769138, 5.651009963285463, 5.694334482064012, 5.731807687233063, 5.763391072541168, 5.789052183924931, 5.808764652857746, 5.822508223445251, 5.83026877323962, 5.832038327751338, 5.827815068643523, 5.8176033356003956, 5.801413621867956], [0.6956825506034864, 0.8786072379560034, 1.06062909697888, 1.241561087907543, 1.4212172908905598, 1.5994130970348526, 1.7759653981038173, 1.9506927746734126, 2.123415682552883, 2.2939566372785514, 2.4621403964911033, 2.627794140008957, 2.7907476474126827, 2.950833472957991, 3.107887117637551, 3.261747198214845, 3.4122556130563497, 3.559257704591654, 3.7026024182345667, 3.842142457601913, 3.9777344358705298, 4.109239023116913, 4.236521089488139, 4.35944984405692, 4.47789896921812, 4.591746750488637, 4.700876201577265, 4.805175184596008, 4.904536525289347, 4.998858123163029, 5.08804305639923, 5.171999681450268, 5.250641727208554, 5.3238883836559765, 5.391664384901661, 5.453900086522765, 5.510531537128823, 5.5615005440761305, 5.606754733264615, 5.6462476029557624, 5.679938571556303, 5.707793019318536, 5.729782323914464, 5.745883889847168, 5.756081171669207, 5.760363690984188, 5.7587270472140215, 5.7511729221208165, 5.737709078078755, 5.718349350097728], [0.7818314824680298, 0.9616715097262325, 1.1405233545005204, 1.3182032344302494, 1.494528571427876, 1.6693181792902854, 1.8423924498798614, 2.013573537683991, 2.182685542563349, 2.3495546905011837, 2.514009512167864, 2.675881019117207, 2.835002877433531, 2.9912115786509985, 3.1443466077696143, 3.2942506081952416, 3.440769543434139, 3.5837528553758706, 3.7230536190019414, 3.858528693361184, 3.990038868656767, 4.117449009293667, 4.24062819273963, 4.35944984405692, 4.47379186596663, 4.583536764311884, 4.688571768791028, 4.7887889488367374, 4.884085324521973, 4.974362972378812, 5.059529126021441, 5.139496271469872, 5.214182237076491, 5.283510277962969, 5.347409154880813, 5.405813207414515, 5.458662421452062, 5.505902490853498, 5.547484873254149, 5.583366839945184, 5.613511519780259, 5.637887937063103, 5.656471043377149, 5.669241743324461, 5.676186914147566, 5.677299419213958, 5.672578115349477, 5.662027854012999, 5.645659476311228, 5.623489801858733], [0.8551427630053461, 1.0315765919816653, 1.2069504062765646, 1.381083997440828, 1.5537984314383424, 1.7249162325129177, 1.8942615655566217, 2.0616604167922405, 2.2269407725841974, 2.3899327961941914, 2.550469002299927, 2.7083844290976034, 2.8635168078113207, 3.015706729435215, 3.164797808536989, 3.3106368439545126, 3.4530739762203773, 3.5919628415526246, 3.727160722253431, 3.858528693361184, 3.9859317654052777, 4.109239023116913, 4.228323759953391, 4.3430636082976495, 4.4533406651992555, 4.559041613527667, 4.6600578384132385, 4.75628553885634, 4.84762583438991, 4.933984866685805, 5.0152738960005925, 5.091409392361622, 5.16231312139973, 5.2279122247403365, 5.288139294870347, 5.342932444403937, 5.392235369676018, 5.435997408598065, 5.4741735927168325, 5.506724693422478, 5.533617262258618, 5.554823665292874, 5.5703221115126045, 5.580096675216644, 5.584137312380039, 5.582439870974964, 5.575006095237208, 5.561843623873852, 5.542965982213988, 5.518392568310525], [0.9144126230158124, 1.0871746452042976, 1.258819521953325, 1.4291708765490774, 1.5980536614591907, 1.7652943382059254, 1.930721055688685, 2.094163826772637, 2.2554547029619867, 2.414427946978408, 2.5709202030673017, 2.7247706648568744, 2.875821240597558, 3.023916715611969, 3.168904911788479, 3.3106368439545126, 3.4489668729688874, 3.5837528553758706, 3.7148562894671935, 3.842142457601913, 3.965480564637903, 4.084743872332696, 4.199809829575602, 4.310560198317253, 4.416881175067193, 4.51866350783466, 4.61580260839239, 4.708198659748091, 4.795756718713149, 4.878386813463172, 4.9560040359901265, 5.028528629351044, 5.0958860696236865, 5.158007142484903, 5.21482801433303, 5.2662902978812305, 5.312341112154377, 5.352933136827836, 5.388024660852289, 5.41757962531466, 5.441567660491091, 5.45996411705388, 5.472750091400335, 5.479912445077496, 5.481443818282799, 5.477342637426756, 5.467613116749929, 5.452265253992517, 5.431314820120997, 5.404783343122394], [0.9586678530366606, 1.1275527508973051, 1.295279012085388, 1.461674286529474, 1.62656759183698, 1.789789488990142, 1.9511722564560596, 2.1105500625319085, 2.267759135748225, 2.422637933155162, 2.575027306318791, 2.7247706648568744, 2.8717141373460686, 3.015706729435215, 3.156600479002241, 3.2942506081952416, 3.4285156722015127, 3.559257704591654, 3.6863423590894038, 3.8096390476215167, 3.9290210745058403, 4.0443657666396895, 4.155554599554754, 4.262473319209003, 4.365012059390432, 4.463065454612027, 4.556532748381924, 4.645317896737513, 4.729329666937105, 4.80848173120774, 4.88269275545281, 4.951886482828337, 5.015991812102046, 5.074942870714675, 5.128679082468487, 5.177145229773413, 5.220291510386851, 5.258073588588842, 5.2904526407400185, 5.317395395175513, 5.338874166393851, 5.354866883505672, 5.365357112913056, 5.370334075196162, 5.369792656189809, 5.363733412238624, 5.352162569625365, 5.335092018172991, 5.31253929902706, 5.284527586631032], [0.9871817834144501, 1.152047901681522, 1.3157302128527628, 1.478060522288745, 1.6388720246232178, 1.797999475166896, 1.9552793597075493, 2.1105500625319085, 2.263652032496735, 2.414427946978408, 2.5627228735325533, 2.7083844290976034, 2.851262936578694, 2.9912115786509985, 3.1280865486244513, 3.261747198214845, 3.3920561820694495, 3.5188795988986463, 3.642087129068556, 3.761552168513267, 3.8771519588290797, 3.9887677134170567, 4.096284739544288, 4.199592556198425, 4.298585007614388, 4.393160372356594, 4.483221467844608, 4.5686757502148065, 4.649435409415465, 4.7254174594375105, 4.796543823588266, 4.86274141472052, 4.923942210334519, 4.98008332247568, 5.031107062356217, 5.076960999634266, 5.117598016289611, 5.152976355040634, 5.18305966225274, 5.207817025294179, 5.2272230043008605, 5.24125765831754, 5.249906565788493, 5.253160839376635, 5.251017135095871, 5.243477655747263, 5.230550148655499, 5.2122478977079965, 5.188589709704812, 5.15959989503338], [0.9994862162006879, 1.1602578878582759, 1.3198373161042525, 1.478060522288745, 1.6347649213717284, 1.789789488990142, 1.9429749269213117, 2.094163826772637, 2.2432008317293604, 2.3899327961941914, 2.534208943154764, 2.675881019117207, 2.8148034464466307, 2.950833472957991, 3.083831318603603, 3.2136603191065953, 3.3401870663926894, 3.463281545676014, 3.5828172690580895, 3.6986714055026884, 3.8107249070530353, 3.918862631161624, 4.0229734590069715, 4.122950409675719, 4.2186907500927475, 4.310096100586366, 4.3970725359800635, 4.479530682106988, 4.557385807647938, 4.630557911198516, 4.698971803475996, 4.762557184581373, 4.821248716237279, 4.874986088927472, 4.923714083868938, 4.967382629752931, 5.00594685419662, 5.0393671298525025, 5.067609115128176, 5.090643789474652, 5.108447483206923, 5.121001901826179, 5.128294144818626, 5.130316718911641, 5.127067545773623, 5.118549964149611, 5.104772726430498, 5.085749989659364, 5.061501300984152, 5.032051577571655], [0.9953791129491982, 1.152047901681522, 1.3075328833180149, 1.461674286529474, 1.6143137206043536, 1.7652943382059254, 1.914460996543522, 2.0616604167922405, 2.206741341597297, 2.3495546905011837, 2.489953713133916, 2.627794140008957, 2.7629343307698706, 2.8952354197353585, 3.024561458593137, 3.1507795560960172, 3.273760014616645, 3.3933764634205814, 3.509505988520773, 3.6220292589799823, 3.730830649531395, 3.8357983593913954, 3.936824527142428, 4.033805341567901, 4.126641148325221, 4.215236552347371, 4.299500515867794, 4.379346451967842, 4.454692313550698, 4.525460677650308, 4.5915788249887175, 4.652978814700038, 4.709597554144288, 4.761376863739341, 4.8082635367443745, 4.8502093939334046, 4.887171333102683, 4.919111373361141, 4.94599669415831, 4.967799669009658, 4.984497893884675, 4.996074210228526, 5.002516722593625, 5.003818810863009, 4.999979137052963, 4.991001646687886, 4.976895564745991, 4.957675386180028, 4.933360861022726, 4.903976974092319], [0.9749279121818236, 1.1275527508973053, 1.2790189529402252, 1.4291708765490774, 1.5778542304722905, 1.7249162325129177, 1.870205766522674, 2.013573537683991, 2.154872225920537, 2.2939566372785514, 2.4306838531234494, 2.564913376998379, 2.6965072789938263, 2.825330337479926, 2.9512501780558207, 3.0741374095733107, 3.193865757095005, 3.310312191650352, 3.4233570566562297, 3.532884190872165, 3.638781047763868, 3.740938811152401, 3.8392525070301575, 3.933621111428754, 4.023947654227981, 4.110139318799162, 4.192107537380515, 4.269768082086507, 4.343041151457707, 4.411851452462177, 4.476128277864154, 4.5358055788805105, 4.590822033050351, 4.641121107247979, 4.686651115774508, 4.72736527346841, 4.763221743780434, 4.794183681763489, 4.820219271933309, 4.841301760961025, 4.857409485164015, 4.868525892766802, 4.874639560909118, 4.875744207383672, 4.871838697091538, 4.86292704320855, 4.849018403061486, 4.830127068718303, 4.806272452302067, 4.777479066043686], [0.9384684220497604, 1.0871746452042976, 1.234763722919377, 1.381083997440828, 1.5259851147955301, 1.6693181792902854, 1.8109359065122077, 1.9506927746734126, 2.0884451741444927, 2.2240515550231184, 2.357372572586133, 2.4882712304756724, 2.616613021472186, 2.7422660657096967, 2.8651012461912773, 2.9849923414654933, 3.1018161553274775, 3.215452643411358, 3.325785036543959, 3.432699960733018, 3.5360875536666283, 3.6358415776041926, 3.7318595285428797, 3.8240427415474194, 3.91229649213499, 3.9965300936110317, 4.076656990255952, 4.15259484626698, 4.22426563036377, 4.291595695970815, 4.354515856894287, 4.412961458415517, 4.466872443728103, 4.516193415650327, 4.560873693549507, 4.600867365419778, 4.636133335059775, 4.666635364301764, 4.692342110248802, 4.713227157481689, 4.72926904520259, 4.740451289287465, 4.746762399224613, 4.748195889921948, 4.744750288370878, 4.736429135159916, 4.723240980836484, 4.70519937712065, 4.682322862979819, 4.654634945578692], [0.8865993063730001, 1.0315765919816653, 1.175493862908911, 1.3182032344302494, 1.459558063019486, 1.5994130970348528, 1.7376246259748913, 1.8740506281507066, 2.008550916622853, 2.14098728325289, 2.2712236407215896, 2.399126162367855, 2.524563419704659, 2.647406517470703, 2.7675292260790068, 2.884808111326346, 2.9991226612302384, 3.11035540986315, 3.2183920580566814, 3.3231215908516836, 3.4244363915736376, 3.5222323524160615, 3.6164089814183162, 3.706869505727892, 3.793520971041053, 3.8762743371196704, 3.9550445692860854, 4.0297507258019865, 4.100316041041522, 4.166668004373163, 4.228738434669286, 4.286463550366885, 4.339784035007443, 4.3886450981886025, 4.432996531865, 4.4727927619404415, 4.507992895098349, 4.538560760822428, 4.5644649485642965, 4.585678840019964, 4.602180636481931, 4.613953381238832, 4.620984976999611, 4.623268198324294, 4.6208006990486306, 4.613585014694924, 4.601628559866617, 4.584943620629288, 4.563547341885881, 4.537461709759165], [0.820172254596956, 0.9616715097262328, 1.1021825823715945, 1.2415610879075434, 1.3796638054978456, 1.516348825264624, 1.651475694110348, 1.784905560042889, 1.9165013148553256, 2.0461277350138953, 2.1736516206093195, 2.2989419322287077, 2.421869925607419, 2.5423092839224943, 2.660136247591729, 2.775229741445012, 2.887471499137247, 2.9967461846750187, 3.1029415109321175, 3.205948355032156, 3.305660870479701, 3.4019765959247, 3.4947965604484494, 3.5840253852628985, 3.6695713817188045, 3.751346645522017, 3.829267147061084, 3.903252817753354, 3.9732276323208624, 4.039119686911438, 4.10086127298478, 4.158388946887548, 4.211643595046017, 4.260570494709266, 4.305119370180495, 4.345244444478717, 4.38090448637769, 4.412062852773794, 4.438687526339295, 4.460751148422311, 4.4782310471596825, 4.49110926077384, 4.499372556029744, 4.503012441832933, 4.5020251779546925, 4.4964117788753954, 4.486178012742053, 4.471334395441158, 4.451896179792891, 4.42788333987783], [0.7402779970753157, 0.8786072379560038, 1.016033650507051, 1.1524160197997257, 1.2876142037303189, 1.4214892770256298, 1.5539036739980774, 1.6847213299037418, 1.8138078207580859, 1.9410305014656875, 2.0662586421220412, 2.1893635623473737, 2.310218763514429, 2.4287000587343632, 2.5446857004671655, 2.6580565056254843, 2.7686959780433105, 2.8764904281836574, 2.981329089962251, 3.0831042345671626, 3.181711281157452, 3.2770489043270468, 3.369019138223448, 3.4575274772142666, 3.5424829729981453, 3.623798328060293, 3.701389985376578, 3.7751782142740167, 3.8450871923594367, 3.9110450834321018, 3.972984111300274, 4.030840629425824, 4.084555186325359, 4.134072586660633, 4.179341947955493, 4.220316752881064, 4.256954897055442, 4.289218732308802, 4.317075105369429, 4.34049539193095, 4.359455526065744, 4.373936024954311, 4.383922008905181, 4.389403216644802, 4.390374015861703, 4.386833408994062, 4.378785034254776, 4.366237161892949, 4.349202685695651, 4.327699109738684], [0.6482283953077888, 0.7837476897170098, 0.9184616303947807, 1.0522317896605786, 1.184920709633079, 1.3163920434774214, 1.4465106955107996, 1.5751429600224076, 1.7021566586650954, 1.8274212762775561, 1.9508080949974778, 2.072190326527846, 2.1914432424204917, 2.308444302243002, 2.4230732794972987, 2.535212385160491, 2.6447463887210616, 2.751562736586004, 2.8555516677372497, 2.9566063265185303, 3.054622872436793, 3.1495005868653227, 3.241141976538942, 3.329452873734929, 3.4143425330367196, 3.4957237245809565, 3.573512823692072, 3.647629896812293, 3.717998783638777, 3.784547175383469, 3.8472066890752727, 3.905912937828171, 3.96060559700311, 4.01122846619564, 4.057729526985627, 4.100060996389702, 4.138179375961505, 4.1720454964892735, 4.201624558244864, 4.226886166742819, 4.2478043639727545, 4.264357655072978, 4.276529030417903, 4.284305983096593, 4.287680521764463, 4.286649178854915, 4.281213014142505, 4.271377613653955, 4.257153083928124, 4.2385540416308665], [0.545534901210549, 0.6786504561688014, 0.8110686519075028, 0.9426534197792444, 1.0732695475400886, 1.2027828182892903, 1.3310601483862359, 1.45796972420288, 1.5833811375711582, 1.7071655197861952, 1.829195674027611, 1.949346206062853, 2.0674936530982433, 2.1835166106453485, 2.2972958572722972, 2.4087144771118587, 2.517657980000403, 2.62401441912428, 2.7276745060527436, 2.8285317230391933, 2.926482432475367, 3.0214259833859862, 3.113264814854436, 3.2019045562732056, 3.28725412431606, 3.3692258165323237, 3.447735401467071, 3.5227022052146397, 3.594049194316529, 3.6617030549184757, 3.7255942681054064, 3.7856571813368096, 3.8418300759091726, 3.894055230376112, 3.9422789798610625, 3.9864517712015717, 4.026528213868514, 4.06246712660794, 4.094231579757587, 4.12178893319461, 4.145110869875515, 4.16417342493383, 4.178957010305632, 4.189446434857599, 4.195630919996935, 4.197504110747097, 4.195064082277962, 4.188313341883726, 4.177258826406484, 4.16191189510816], [0.43388373911755823, 0.5650412309806699, 0.6956181047829386, 0.8254801839597163, 0.9544940264461509, 1.0825270617979288, 1.2094477274163689, 1.3351256037378865, 1.4594315482489093, 1.5822378281885416, 1.7034182518026093, 1.82284829801422, 1.9404052443775837, 2.055968293183624, 2.1694186955877908, 2.2806398736325213, 2.3895175400389768, 2.495939815644943, 2.599797344368237, 2.700983405577469, 2.799394023754707, 2.894928075337353, 2.9874873926294345, 3.076976864675552, 3.1633045349938116, 3.24638169606733, 3.3261229804972037, 3.402446448723278, 3.475273673222591, 3.5445298190989476, 3.610143720980842, 3.672047956148678, 3.730178913816182, 3.7844768604947774, 3.834886001373784, 3.8813545376533627, 3.9238347197712735, 3.962282896468792, 3.996659559645316, 4.026929384955616, 4.053061268107987, 4.075028356826012, 4.092808078441089, 4.10638216308737, 4.115736662475295, 4.120861964224391, 4.121752801740645, 4.118408259628293, 4.110831774630439, 4.099031132097581], [0.3151082180236209, 0.4447854744893086, 0.5740056838130719, 0.7026360634947233, 0.8305444371239026, 0.9575993702002755, 1.0836703051913674, 1.2086276956892539, 1.3323431395282501, 1.4546895107268172, 1.5755410901181035, 1.694773694534883, 1.8122648044161578, 1.9278936897042873, 2.0415415339032847, 2.1530915561707973, 2.2624291313183167, 2.3694419075963102, 2.474019922143236, 2.576055713979816, 2.6754444344324595, 2.7720839548723597, 2.8658749716595677, 2.9567211081841904, 3.044529013899874, 3.1292084602478027, 3.2106724333726397, 3.288837223535147, 3.3636225111296008, 3.4349514492176136, 3.5027507424935638, 3.5669507226004695, 3.627485419718942, 3.6842926303556305, 3.737313981261514, 3.7864949894143685, 3.8317851180037463, 3.8731378283609743, 3.9105106277807726, 3.943865113185387, 3.973167010586347, 3.998386210303306, 4.019496797903773, 4.036477080831937, 4.04930961069925, 4.057981201213812, 4.062482941730178, 4.06281020640566, 4.058962658953679, 4.050944252989332], [0.19115862870137254, 0.31985778289165545, 0.4482282615880706, 0.5761381554460907, 0.7034560284032433, 0.8300510527385516, 0.9557931435068615, 1.080553092209917, 1.2042026995668242, 1.3266149072474807, 1.4476639284335975, 1.567225377073159, 1.6851763956954986, 1.8013957816556547, 1.9157641116782838, 2.0281638645731443, 2.1384795419960687, 2.246597787131317, 2.3524075011733694, 2.4557999574884546, 2.5566689133385214, 2.6549107190528325, 2.7504244245350042, 2.8431118829960598, 2.9328778518068837, 3.0196300903664683, 3.103279454885362, 3.1837399899869383, 3.260929017032361, 3.3347672190784663, 3.4051787223812937, 3.4720911743614753, 3.5354358179514147, 3.5951475622478126, 3.6511650493969707, 3.7034307176441397, 3.7518908604821064, 3.7964956818382682, 3.8371993472434562, 3.873960030929954, 3.9067399588103027, 3.9355054472927273, 3.960226937893306, 3.980879027609305, 3.99744049502249, 4.009894322105563, 4.01822771170933, 4.022432100712653, 4.022503168821616, 4.018440843008935], [0.06407021998071323, 0.19230946542993146, 0.3203510999035647, 0.4480635519667538, 0.5753155884418175, 0.7019764492592147, 0.8279159818223556, 0.953004774748193, 1.077114290846165, 1.2001169991988476, 1.321886506208596, 1.442297685475506, 1.5612268063732502, 1.6785516611906617, 1.794151690708417, 1.907908108081783, 2.019704020902131, 2.1294245513117893, 2.2369569540488055, 2.342190732300323, 2.4450177512455316, 2.545332349171498, 2.643031446047726, 2.738014649447851, 2.8301843577096437, 2.919445860227321, 3.0057074347730914, 3.0888804417479445, 3.1688794152648336, 3.2456221509706484, 3.3190297905167503, 3.3890269025912465, 3.455541560429775, 3.5185054157251066, 3.5778537688596543, 3.6335256353887067, 3.685463808706062, 3.7336149188276897, 3.77792948723299, 3.8183619777073217, 3.854870843133542, 3.887418568184478, 3.915971707872458, 3.940500921916297, 3.960981004890427, 3.9773909121251654, 3.989713781331541, 3.997936949928436, 4.002051968054241, 4.002054607249663], [-0.06407021998071255, 0.0642348619505946, 0.19247393821905875, 0.32051523450502983, 0.4482271797211581, 0.5754785412105821, 0.7021385595973543, 0.8280770831505398, 0.9531647015239166, 1.0772728787338548, 1.2002740852387295, 1.3220419289841447, 1.4424512852793128, 1.561378425371134, 1.6787011435838533, 1.7942988828936517, 1.908052858809141, 2.0198461814304554, 2.1295639755615277, 2.237093498752115, 2.342324257148291, 2.4451481190323507, 2.5454594259354555, 2.643155101208857, 2.7381347559421165, 2.8303007921195036, 2.919558502908548, 3.0058161699777153, 3.0889851577431937, 3.1689800044479424, 3.245718509979434, 3.319121820335814, 3.3891145086537304, 3.455624652714528, 3.518583908849188, 3.5779275821660743, 3.6335946930293015, 3.6855280397194403, 3.733674257212142, 3.777983872014314, 3.818411353001479, 3.854915158204081, 3.887457777494668, 3.9160057711320806, 3.9405298041230523, 3.9610046763658944, 3.9774093485453035, 3.989726963751682, 3.9979448648027516, 4.002054607249663], [-0.19115862870137187, -0.06226304609803798, 0.06669651599405746, 0.19558754290737668, 0.3242775903989098, 0.4526344207455889, 0.5805261386274876, 0.7078213266591785, 0.8343891804299792, 0.9600996429143269, 1.0848235381141658, 1.2084327037960134, 1.3308001231863222, 1.4518000554897998, 1.5713081650965752, 1.6892016493454434, 1.8053593647119008, 1.919661951291308, 2.031991955449257, 2.1422339505131207, 2.2502746553807644, 2.3560030509245333, 2.4593104940709116, 2.5600908294386278, 2.6582404984204766, 2.753658645596797, 2.8462472223712316, 2.9359110877222827, 3.0225581059671494, 3.106099241437364, 3.1864486499689675, 3.263523767113181, 3.33724539297697, 3.4075377736062786, 3.47432867882834, 3.5375494764730666, 3.5971352028972383, 3.6530246297390434, 3.705160326834352, 3.7534887212300974, 3.797960152234104, 3.83852892244481, 3.8751533447084308, 3.9077957849553266, 3.936422700871563, 3.9610046763658944, 3.981516451796793, 3.997936949928436, 4.010249297588989, 4.018440843008935], [-0.3151082180236202, -0.1851071665630312, -0.05491590497580923, 0.07533178641601534, 0.2055020693049724, 0.3354611849260613, 0.4650755915029239, 0.5942121014710473, 0.7227380183369887, 0.850521273032993, 0.9774305596268877, 1.103335470247805, 1.2281066290890825, 1.3516158253506525, 1.4737361449843047, 1.5943421011064491, 1.713309762944374, 1.8305168831834906, 1.9458430235847135, 2.0591696787428915, 2.170380397859124, 2.279360904401827, 2.3859992135335957, 2.490185747183195, 2.5918134466444323, 2.6907778825862185, 2.786977362360765, 2.88031303449965, 2.970688990290389, 3.0580123623291144, 3.1421934199481196, 3.2231456614201734, 3.3007859028449067, 3.3750343636258817, 3.44581474845055, 3.51305432568885, 3.5766840021298636, 3.6366383939797724, 3.6928558940481144, 3.7452787350533434, 3.7938530489826148, 3.83852892244481, 3.87926044795992, 3.9160057711320806, 3.9487271336578003, 3.9773909121251654, 4.001967652564168, 4.022432100712653, 4.038763227966778, 4.050944252989331], [-0.433883739117558, -0.30228040238255915, -0.17036645210037332, -0.0382774387721162, 0.09385090721198153, 0.22588281504472663, 0.3576826130156454, 0.48911486792283854, 0.6200445242397487, 0.7503370428938455, 0.879858539514617, 1.0084759220088106, 1.1360570273215551, 1.2624707572428346, 1.387587213119761, 1.51127782933622, 1.6334155054227335, 1.753874736660784, 1.8725317430473973, 1.9892645964874585, 2.1039533460830793, 2.2164801413912483, 2.3267293535231293, 2.4345876939605624, 2.5399443309676717, 2.642691003477969, 2.742722132339917, 2.8399349288066422, 2.9342295001583256, 3.0255089523487175, 3.1136794895703295, 3.198650510635957, 3.280334702077532, 3.3586481278666107, 3.4335103156643125, 3.504844339512096, 3.572576898878374, 3.6366383939797724, 3.696962997299604, 3.7534887212300974, 3.806157481768852, 3.854915158204081, 3.899711648727295, 3.940500921916297, 3.9772410640355895, 4.009894322105562, 4.03842714269623, 4.06281020640566, 4.0830184579876265, 4.099031132097581], [-0.5455349012105485, -0.41185877226389345, -0.2777594305876514, -0.14337467232032464, -0.008842586885258186, 0.1256985849055795, 0.2601105929033751, 0.39425531968384453, 0.5279949224722216, 0.6611919747860275, 0.7937096076500736, 0.9254116502385815, 1.0561627697999147, 1.1858286107201286, 1.314275932582445, 1.4413727470807869, 1.5669884536466892, 1.6909939736502055, 1.813261883036931, 1.9336665432648261, 2.052084230406319, 2.168393262282999, 2.282474123502281, 2.3942095882675547, 2.5034848408356085, 2.6101875934975722, 2.714208201962127, 2.8154397780224256, 2.913778299390951, 3.0091227165894465, 3.101375056784092, 3.190440524459203, 3.2762275988260425, 3.3586481278666107, 3.437617418915802, 3.51305432568885, 3.5848813316646115, 3.6530246297390434, 3.7174141980669786, 3.777983872014314, 3.8346714121466414, 3.8874185681844775, 3.9361711388593577, 3.980879027609305, 4.021496294056438, 4.057981201213812, 4.090296258372991, 4.118408259628293, 4.1422883179980925, 4.161911895108159], [-0.6482283953077882, -0.5120430024030406, -0.3753314506999217, -0.23823422055931864, -0.10089218865278526, 0.03655351679776153, 0.1739616610388317, 0.3111910479136154, 0.4481006649505812, 0.5845498282633216, 0.7203983271127574, 0.8555065679831486, 0.9897357180238704, 1.12294784770955, 1.2550060725719785, 1.3857746938581545, 1.5151193379699288, 1.6429070945419562, 1.7690066530160826, 1.8932884375718184, 2.015624740274256, 2.135889852302602, 2.2539601931244917, 2.369714437483338, 2.483033640068234, 2.5938013577383012, 2.70190376917589, 2.8072297918456717, 2.9096711961394615, 3.0091227165894465, 3.1054821600355815, 3.198650510635957, 3.28853203161228, 3.3750343636258817, 3.4580686196831767, 3.5375494764730666, 3.613395262042401, 3.68552803971944, 3.7538736881990413, 3.8183619777073217, 3.8789266421674897, 3.9355054472927273, 3.988040254536118, 4.036477080831937, 4.080766154066904, 4.12086196422439, 4.156723310149035, 4.188313341883725, 4.215599598535409, 4.238554041630866], [-0.7402779970753153, -0.6011880705108585, -0.4614803825644651, -0.32129849232954777, -0.18078644617442563, -0.040088629724944425, 0.10065038050151554, 0.2412859656581825, 0.38167361317453685, 0.5216690652527429, 0.6611284671022909, 0.7999085147605164, 0.9378666023471102, 1.0748609686013006, 1.2107508425511302, 1.3453965881651468, 1.4786598478378656, 1.6104036845615592, 1.7404927226382931, 1.8687932867876018, 1.9951735395068813, 2.119503616543331, 2.2416557603382534, 2.361504451306584, 2.4789265368167444, 2.5938013577383012, 2.7060108724273793, 2.8154397780224256, 2.921975628925699, 3.0255089523487175, 3.1259333608029563, 3.2231456614201734, 3.317045961990069, 3.407537773606278, 3.4945281098152394, 3.5779275821660743, 3.657650492063249, 3.7336149188276897, 3.805742803875802, 3.873960030929954, 3.938196502177956, 3.9983862103033054, 4.054467306312162, 4.106382163087369, 4.15407743460422, 4.197504110747096, 4.236617567670676, 4.2713776136539545, 4.301748530399952, 4.327699109738683], [-0.8201722545969556, -0.6778302170335645, -0.5347916631017813, -0.39120357458498023, -0.24721349795046998, -0.10296939273552308, 0.04138052049104901, 0.18568791243555027, 0.3298044974977766, 0.47358218614449354, 0.6168732370814429, 0.7595304090675086, 0.9014071122150468, 1.0423575586209037, 1.1822369121733407, 1.3209014373809302, 1.458208647070491, 1.5940174488022882, 1.7281882898520555, 1.8605833006108479, 1.9910664362553916, 2.119503616543331, 2.2457628635897433, 2.369714437483338, 2.4912309696029817, 2.610187593497572, 2.726462073194754, 2.8399349288066422, 2.950489559303488, 3.058012362329114, 3.162392850935019, 3.2635237671131807, 3.3613011920109175, 3.455624652714528, 3.546397225492, 3.6335256353887067, 3.7169203520737155, 3.796495681838268, 3.872169855651846, 3.943865113185386, 4.011507782715272, 4.075028356826012, 4.134361563833803, 4.189446434857599, 4.240226366468764, 4.286649178854914, 4.3286671694382015, 4.366237161892949, 4.399320550512223, 4.42788333987783], [-0.886599306373, -0.7407109800441432, -0.5940615231122478, -0.4468016278076129, -0.29908261362723054, -0.1510562718437728, -0.002874709529799291, 0.14530980674254246, 0.29334500736571323, 0.44107877616409663, 0.5883593067036532, 0.7350352582832919, 0.8809559114476722, 1.0259713228616327, 1.1699324793871029, 1.3126914512041763, 1.4541015438190013, 1.5940174488022882, 1.732295393103545, 1.8687932867876018, 2.003370869041629, 2.135889852302602, 2.266214064357118, 2.3942095882675547, 2.519744899980771, 2.642691003477969, 2.762921563326817, 2.88031303449965, 2.9947447893243364, 3.106099241437364, 3.2142619666117795, 3.3191218203358135, 3.4205710520213843, 3.5185054157251066, 3.6128242772680443, 3.7034307176441392, 3.790231632611032, 3.8731378283609743, 3.952064113173486, 4.026929384955616, 4.0976567145798155, 4.164173424933829, 4.22641116560133, 4.284305983096593, 4.337798386581034, 4.386833408994061, 4.431360663535443, 4.471334395441157, 4.5067135289995015, 4.537461709759165], [-0.9384684220497602, -0.7887978591523925, -0.6383167531330958, -0.4871797335006205, -0.3355421037592936, -0.18355968182416937, -0.03138863990758867, 0.12081465595832586, 0.27289380659833873, 0.4246925404048256, 0.5760548739174155, 0.726825272106538, 0.8768488081961825, 1.0259713228616327, 1.1740395826385925, 1.3209014373809302, 1.4664059766052389, 1.610403684561559, 1.7527465938709197, 1.8932884375718184, 2.0318847994194185, 2.1683932622829984, 2.3026735544891808, 2.434587693960562, 2.5640001300016193, 2.690777882586218, 2.8147906790035773, 2.9359110877222823, 3.054014649334803, 3.168980004447942, 3.2806890183878235, 3.3890269025912456, 3.4938823325587003, 3.5951475622478126, 3.6927185347896843, 3.786494989414368, 3.876380564475575, 3.9622828964687913, 4.0441137149410125, 4.12178893319461, 4.195228734692085, 4.264357655072977, 4.32910465969857, 4.389403216644801, 4.445191365068312, 4.496411778875395, 4.543011825628433, 4.5849436206292875, 4.622164076124065, 4.6546349455786915], [-0.9749279121818236, -0.8213012691327894, -0.6668306835108855, -0.5116748842848373, -0.3559933045266682, -0.19994591758344038, -0.043693072693826496, 0.11260466978157191, 0.26878670334684895, 0.4246925404048256, 0.580161977168905, 0.735035258283292, 0.8891532409824202, 1.0423575586209037, 1.1944907834059673, 1.3453965881651468, 1.4949199069830283, 1.6429070945419557, 1.7892060840029824, 1.9336665432648261, 2.0761400294402668, 2.216480141391248, 2.3545426701659413, 2.4901857471831947, 2.6232699900120857, 2.7536586455967966, 2.8812177307796216, 3.005816169977715, 3.127325929872119, 3.2456221509706484, 3.360583275909464, 3.472091174361475, 3.5800312644232433, 3.68429263035563, 3.784768136557212, 3.8813545376533622, 3.9739525845878454, 4.062467126607939, 4.146807209038253, 4.226886166742818, 4.302621713179365, 4.373936024954311, 4.44075582179156, 4.503012441832933, 4.560641912192876, 4.613585014694922, 4.661787346722369, 4.70519937712065, 4.743776497093932, 4.777479066043686], [-0.9953791129491981, -0.8376875048920605, -0.6791351162971232, -0.5198848704615913, -0.3601004077781579, -0.19994591758344038, -0.03958596944233683, 0.12081465595832575, 0.28109113613308656, 0.4410787761640964, 0.6006131779362794, 0.7595304090675086, 0.9176671713602096, 1.0748609686013002, 1.23095027353803, 1.385774693858154, 1.5391751370038764, 1.690993973650205, 1.8410751996797425, 1.9892645964874585, 2.135409889450733, 2.2793609044018264, 2.4209697219419852, 2.560090829438627, 2.6965812705494017, 2.8303007921195023, 2.9611119883012615, 3.0888804417479436, 3.213474861736662, 3.3347672190784654, 3.4526328776769906, 3.5669507226004686, 3.6776032845355133, 3.784476860494777, 3.887461630654451, 3.9864517712015703, 4.081345563075123, 4.172045496489273, 4.258458371131243, 4.340495391930949, 4.418072260303928, 4.491109260773838, 4.559531342885497, 4.623268198324293, 4.682254333162742, 4.7364291351599155, 4.785736936044618, 4.830127068718302, 4.869553919318933, 4.903976974092317], [-0.9994862162006879, -0.8376875048920605, -0.6750280130456336, -0.5116748842848374, -0.34779597499192016, -0.18355968182416937, -0.01913476867496222, 0.14530980674254246, 0.30960506651087605, 0.4735821861444931, 0.6370726680683426, 0.7999085147605163, 0.9619224013810579, 1.1229478477095498, 1.2828193892147906, 1.4413727470807869, 1.5984449970143428, 1.7538747366607836, 1.9075022514557873, 2.059169678742891, 2.2087211699880496, 2.3560030509245324, 2.5008639794636256, 2.643155101208856, 2.782730202413945, 2.919445860227321, 3.053161590068789, 3.183739989986938, 3.3110468818489327, 3.4349514492176128, 3.5553263717742305, 3.672047956148677, 3.7849962630227925, 3.894055230376112, 3.9991127927474417, 4.100060996389702, 4.196796110199688, 4.2892187323088, 4.37723389222518, 4.460751148422311, 4.539684681273794, 4.613953381238832, 4.683480932207746, 4.748195889921947, 4.808031755387744, 4.862927043208548, 4.912825344765278, 4.957675386180026, 4.997431081003439, 5.0320515775716546], [-0.9871817834144503, -0.8213012691327897, -0.6545768122782593, -0.48717973350062094, -0.3192820446141308, -0.1510562718437729, 0.017324721457100734, 0.18568791243554983, 0.353860296531724, 0.5216690652527424, 0.6889417837451026, 0.8555065679831485, 1.021192261391524, 1.1858286107201281, 1.3492464409908345, 1.511277829336219, 1.6717562775516588, 1.8305168831834893, 1.9873965089774273, 2.14223395051312, 2.2948701018525925, 2.44514811903235, 2.5929135812311523, 2.73801464944785, 2.880302222526215, 3.0196300903664675, 3.1558550841660282, 3.288837223535146, 3.4184398603362105, 3.5445298190989467, 3.666977533867221, 3.785657181336808, 3.9004468101473555, 4.0112284661956386, 4.117888313841378, 4.220316752881063, 4.3184085311695535, 4.4120628527737935, 4.501183481547429, 4.5856788400199635, 4.665462103498795, 4.7404512892874635, 4.810569340928405, 4.87574420738367, 4.93590891707225, 4.991001646687884, 5.040965784726704, 5.085749989659362, 5.125308242687945, 5.159599895033378], [-0.9586678530366608, -0.788797859152393, -0.6181173221461961, -0.44680162780761334, -0.2750268145932825, -0.1029693927355233, 0.06919383713386118, 0.2412859656581824, 0.41313015654219043, 0.5845498282633209, 0.7553688355211469, 0.9254116502385813, 1.0945035419288405, 1.2624707572428344, 1.4291406985124748, 1.5943421011064483, 1.7579052094162022, 1.9196619512913071, 2.079446110744954, 2.237093498752114, 2.392442121964863, 2.545332349171497, 2.6956070753283923, 2.8431118829960584, 2.9876952010134934, 3.1292084602478014, 3.267506246259019, 3.4024464487232775, 3.5338904074607744, 3.661703054918475, 3.7857530549611584, 3.9059129378281696, 4.022059231117222, 4.134072586660633, 4.241837903163628, 4.345244444478716, 4.444185953394555, 4.538560760822426, 4.628271890268088, 4.713227157481687, 4.7933392651833024, 4.868525892766801, 4.938709780889831, 5.003818810863008, 5.063786078756756, 5.118549964149609, 5.168054193447363, 5.2122478977079965, 5.251085664912946, 5.284527586631032], [-0.9144126230158128, -0.7407109800441437, -0.5662482064694361, -0.39120357458498123, -0.2157569545828164, -0.04008862972494509, 0.13562088890990498, 0.3111910479136146, 0.4864414370795064, 0.6611919747860268, 0.8352630930427868, 1.00847592200881, 1.1806524737933835, 1.3516158253506516, 1.5211903002800016, 1.689201649345442, 1.8554772295284723, 2.019846181430454, 2.1821396048421935, 2.342190732300322, 2.499835100452141, 2.654910719052831, 2.8072582374213826, 2.956721108184189, 3.1031457481380564, 3.2463816960673286, 3.386281767352956, 3.5227022052146384, 3.655502828430641, 3.784547175383467, 3.9097026442834064, 4.030840629425822, 4.147836653342223, 4.260570494709264, 4.3689263118842865, 4.47279276194044, 4.572063115079061, 4.666635364301762, 4.756412330229514, 4.841301760961024, 4.921216426867808, 4.9960742102285245, 5.06579818961049, 5.13031671891164, 5.189563500981757, 5.243477655747262, 5.29200378276961, 5.335092018172989, 5.372698085882813, 5.404783343122393], [-0.8551427630053464, -0.6778302170335652, -0.49982115469339183, -0.32129849232954855, -0.1424456740454999, 0.03655351679776131, 0.21551514643154557, 0.394255319683844, 0.5725903689440499, 0.7503370428938445, 0.9273126948103141, 1.1033354702478042, 1.2782244939056542, 1.451800055489799, 1.6238837943772415, 1.7942988828936506, 1.9628702080157505, 2.1294245513117884, 2.2937907669351847, 2.4557999574884537, 2.615285647576705, 2.7720839548723593, 2.92603375851532, 3.076976864675551, 3.2247581691079237, 3.369225816532323, 3.510231356675205, 3.6476298968122918, 3.7812802506556427, 3.9110450834321004, 4.036791053004066, 4.158388946887547, 4.27571381502673, 4.388645098188602, 4.497066751845713, 4.600867365419777, 4.699940276763567, 4.794183681763487, 4.883500738950174, 4.967799669009658, 5.046993849092809, 5.121001901826178, 5.189747778932738, 5.253160839376633, 5.311175921951624, 5.3637334122386235, 5.410779303863549, 5.4522652539925165, 5.488148633007377, 5.518392568310524], [-0.7818314824680299, -0.6011880705108588, -0.41992689717175125, -0.2382342205593192, -0.05629674218095626, 0.12569858490557917, 0.307564748199073, 0.4891148679228382, 0.6701623890563206, 0.850521273032992, 1.0300061889075542, 1.2084327037960132, 1.3856174723929326, 1.5613784253711338, 1.7355349564702325, 1.9079081080817821, 2.0783207551403144, 2.2465977871313165, 2.412566288029122, 2.5760557139798155, 2.736898068546572, 2.8949280753373525, 3.049983347837569, 3.2019045562732042, 3.3505355913329256, 3.495723724580955, 3.6373197653958647, 3.7751782142740162, 3.9091574123401487, 4.039119686911437, 4.164931492965493, 4.286463550366884, 4.403590976711236, 4.516193415650326, 4.624155160566373, 4.72736527346841, 4.825717698988569, 4.91911137336114, 5.007450328272422, 5.09064378947465, 5.168606270062677, 5.24125765831754, 5.3085233000266765, 5.370334075196162, 5.426626469076188, 5.477342637426755, 5.522430465956539, 5.561843623873852, 5.595541611494655, 5.623489801858733], [-0.6956825506034869, -0.5120430024030416, -0.3278772954042246, -0.14337467232032564, 0.0412752779313138, 0.22588281504472596, 0.41025824229631225, 0.5942121014710463, 0.7775553675435982, 0.9600996429143258, 1.141657351000544, 1.3220419289841439, 1.5010680195174957, 1.6785516611906608, 1.8543104775641694, 2.028163864573143, 2.199933176110181, 2.369441907596309, 2.53651587735137, 2.700983405577468, 2.862675490771573, 3.021425983385985, 3.177071756558228, 3.329452873734928, 3.4784127530174307, 3.6237983280602917, 3.76546020535729, 3.9032528177533528, 4.037034574024655, 4.166668004373161, 4.292019901686151, 4.412961458415516, 4.529368398936237, 4.641121107247979, 4.74810474988862, 4.850209393933403, 4.947330119958435, 5.039367129852502, 5.126225849366359, 5.207817025294178, 5.28405681718724, 5.354866883505671, 5.420174462119666, 5.479912445077495, 5.534019447563466, 5.582439870974963, 5.625123960053779, 5.662027854012998, 5.693113631606925, 5.718349350097727], [-0.5981105304912162, -0.4118587722638941, -0.22518380130698457, -0.03827743877211687, 0.14866825641859216, 0.3354611849260606, 0.5219094043893031, 0.7078213266591777, 0.8930059146681623, 1.0772728787338537, 1.260432872094482, 1.4422976854755056, 1.622680440487363, 1.8013957816556545, 1.978260066886418, 2.1530915561707964, 2.3257105983351827, 2.495939815644942, 2.6636042860720304, 2.8285317230391924, 2.990552652456079, 3.1495005868653223, 3.305212196519654, 3.4575274772142652, 3.606289914701937, 3.751346645522017, 3.8925486140779495, 4.029750725801986, 4.162811996249657, 4.291595695970814, 4.4159694910084, 4.53580557888051, 4.6509808199061045, 4.761376863739341, 4.866880270982558, 4.967382629752931, 5.062780667083, 5.152976355040633, 5.23787701145935, 5.317395395175513, 5.391449795674518, 5.45996411705388, 5.522867956216906, 5.580096675216643, 5.631591467675737, 5.677299419213957, 5.717173561821307, 5.751172922120816, 5.779262563471469, 5.801413621867956], [-0.49071755200393863, -0.30228040238256026, -0.11353263921399454, 0.07533178641601379, 0.2641188035431554, 0.45263442074558774, 0.6406849254832401, 0.8280770831505386, 1.0146183356380285, 1.2001169991988465, 1.3843824614167297, 1.5672253770731583, 1.7484578627123637, 1.9278936897042867, 2.105348475607077, 2.28063987363252, 2.453587760019688, 2.6240144191242787, 2.7917447260334556, 2.956606326518529, 3.1184298141405846, 3.277048904327046, 3.4323006052403127, 3.5840253852628976, 3.732067336926938, 3.8762743371196695, 4.0164982034001975, 4.152594846266979, 4.2844244172195225, 4.411851452462176, 4.534745012102337, 4.652978814700037, 4.766431367030668, 4.874986088927471, 4.978531433075548, 5.076960999634265, 5.1701736455702765, 5.258073588588841, 5.34057050555659, 5.4175796253146595, 5.489021815786788, 5.554823665292873, 5.614917557984433, 5.66924174332446, 5.717740399540279, 5.760363690984186, 5.797067819342947, 5.827815068643522, 5.852573844008785, 5.8713187041233885], [-0.3752670048793746, -0.18510716656303236, 0.005242881879943206, 0.19558754290737546, 0.3857312245130225, 0.5754785412105813, 0.7646345148054887, 0.9530047747481922, 1.1403957578630302, 1.3266149072474795, 1.5114708701373896, 1.6947736945348828, 1.8763350243968702, 2.055968293183624, 2.233488915568503, 2.4087144771118574, 2.5814649217041943, 2.7515627365860027, 2.9188331347541143, 3.083104234567162, 3.2442072363655865, 3.4019765959246993, 3.5562501945625615, 3.706869505727891, 3.8536797578968054, 3.9965300936110304, 4.1352737244941355, 4.2697680820865065, 4.399874964344087, 4.525460677650307, 4.646396174195328, 4.762557184581372, 4.873824345517946, 4.98008332247568, 5.081224927172788, 5.177145229773412, 5.267745665682548, 5.3529331368278354, 5.432620107324117, 5.506724693422477, 5.575170747651332, 5.637887937063103, 5.694811815506074, 5.745883889847167, 5.791051680077596, 5.830268773239619, 5.8634948711189905, 5.890695831654101, 5.911843704019251, 5.926916757346022], [-0.25365458390950835, -0.06226304609803965, 0.12919247120219104, 0.32051523450502817, 0.5115086467380234, 0.7019764492592134, 0.8917229235261476, 1.0805530922099158, 1.2682729195475357, 1.4546895107268158, 1.6396113100988148, 1.822848298014219, 2.0042121860813755, 2.1835166106453476, 2.360577324289162, 2.5352123851604897, 2.7072423439291953, 2.8764904281836556, 3.0427827240763623, 3.205948355032155, 3.365819657335453, 3.52223235241606, 3.6750257156564987, 3.8240427415474185, 3.969130305021369, 4.1101393187991615, 4.246924886587125, 4.379346451967841, 4.507267942831364, 4.630557911198515, 4.749089668292568, 4.862741414720519, 4.971396365630215, 5.074942870714674, 5.173274528940315, 5.26629029788123, 5.353894597547091, 5.435997408598064, 5.5125143648457575, 5.5833668399451835, 5.648482028188648, 5.707793019318535, 5.761238867282118, 5.808764652857745, 5.850321540088062, 5.885866826462252, 5.915363986795751, 5.93878271076235, 5.956098934040099, 5.9672948630390295], [-0.12787716168450664, 0.06423486195059334, 0.25628087992285076, 0.44806355196675257, 0.6393858084225298, 0.8300510527385507, 1.0198633634875738, 1.208627695689253, 1.396150081232042, 1.5822378281885403, 1.7666997188194746, 1.9493462060628521, 2.1299896083063774, 2.308444302243001, 2.4845269136114108, 2.658056505625483, 2.8288547648990625, 2.9967461846750174, 3.1615582451703013, 3.3231215908516827, 3.481270204460017, 3.6358415776041917, 3.7866768777494895, 3.933621111428753, 4.076523283508648, 4.2152365523473705, 4.349618380684365, 4.479530682106988, 4.604839962943635, 4.72541745943751, 4.841139270060094, 4.951886482828336, 5.05754529749476, 5.158007142484903, 5.253168786461956, 5.342932444403936, 5.427205878084408, 5.505902490853497, 5.578941416621801, 5.6462476029557624, 5.707751888199114, 5.763391072541168, 5.813107982958878, 5.8568515319659955, 5.894576770108911, 5.92624493215526, 5.951823476927815, 5.9712861207427474, 5.9846128644178895, 5.9917900138232465], [-2.4492935982947064e-16, 0.19230946542993066, 0.384421319884277, 0.5761381554460898, 0.7672629701070361, 0.9575993702002752, 1.1469517722082336, 1.335125603737886, 1.5219275034570439, 1.707165519786194, 1.8906493081417235, 2.0721903265278456, 2.2516020292762446, 2.428700058734363, 2.603302434705349, 2.775229741445011, 2.9443053120236264, 3.110355409863149, 3.273209407263291, 3.4326999607330175, 3.5886631829472955, 3.7409388111524007, 3.88937037184673, 4.0338053415679, 4.174095303620918, 4.310096100586365, 4.441667982451893, 4.568675750214806, 4.690988894808179, 4.808481731207739, 4.921033527581735, 5.028528629351043, 5.130856578032076, 5.2279122247403365, 5.319595838238, 5.405813207414515, 5.4864757380948745, 5.5615005440761305, 5.630810532298562, 5.694334482064011, 5.752007118219963, 5.803769178234176, 5.849567473090942, 5.889354941946392, 5.923090700486701, 5.950740082939477, 5.972274677695189, 5.987672356502019, 5.996917297204127, 6.0]], "y": [[6.0, 5.996917297204127, 5.987672356502019, 5.972274677695189, 5.950740082939477, 5.923090700486701, 5.889354941946392, 5.849567473090942, 5.803769178234177, 5.752007118219963, 5.694334482064012, 5.630810532298563, 5.5615005440761305, 5.486475738094875, 5.405813207414515, 5.319595838238, 5.2279122247403365, 5.130856578032077, 5.028528629351045, 4.921033527581736, 4.80848173120774, 4.690988894808179, 4.5686757502148065, 4.441667982451894, 4.3100961005863665, 4.174095303620919, 4.033805341567901, 3.8893703718467316, 3.740938811152401, 3.588663182947296, 3.432699960733018, 3.2732094072632925, 3.110355409863151, 2.9443053120236273, 2.775229741445012, 2.603302434705349, 2.428700058734364, 2.251602029276245, 2.072190326527847, 1.8906493081417248, 1.707165519786196, 1.521927503457045, 1.3351256037378865, 1.146951772208235, 0.957599370200276, 0.7672629701070374, 0.5761381554460913, 0.384421319884279, 0.192309465429932, 3.67394039744206e-16], [5.9917900138232465, 5.9846128644178895, 5.9712861207427474, 5.951823476927815, 5.92624493215526, 5.894576770108911, 5.8568515319659955, 5.813107982958879, 5.763391072541169, 5.707751888199115, 5.6462476029557624, 5.578941416621802, 5.505902490853498, 5.427205878084409, 5.342932444403937, 5.253168786461956, 5.158007142484903, 5.057545297494761, 4.951886482828338, 4.841139270060095, 4.725417459437511, 4.604839962943636, 4.479530682106989, 4.349618380684366, 4.215236552347372, 4.0765232835086485, 3.9336211114287543, 3.7866768777494917, 3.635841577604193, 3.4812702044600177, 3.3231215908516836, 3.1615582451703017, 2.99674618467502, 2.828854764899064, 2.658056505625485, 2.4845269136114116, 2.308444302243003, 2.1299896083063787, 1.9493462060628537, 1.7666997188194764, 1.5822378281885427, 1.3961500812320438, 1.208627695689254, 1.0198633634875756, 0.830051052738552, 0.6393858084225315, 0.4480635519667544, 0.25628087992285326, 0.06423486195059512, -0.12787716168450558], [5.9672948630390295, 5.956098934040099, 5.938782710762351, 5.915363986795752, 5.8858668264622525, 5.850321540088063, 5.808764652857746, 5.761238867282119, 5.707793019318537, 5.648482028188648, 5.583366839945184, 5.512514364845758, 5.435997408598065, 5.353894597547092, 5.2662902978812305, 5.173274528940316, 5.074942870714675, 4.971396365630218, 4.862741414720521, 4.7490896682925685, 4.630557911198517, 4.507267942831366, 4.379346451967842, 4.246924886587126, 4.110139318799163, 3.9691303050213707, 3.82404274154742, 3.675025715656501, 3.522232352416062, 3.365819657335454, 3.205948355032156, 3.0427827240763645, 2.8764904281836587, 2.707242343929197, 2.535212385160491, 2.3605773242891632, 2.1835166106453494, 2.004212186081377, 1.822848298014221, 1.6396113100988172, 1.4546895107268187, 1.2682729195475375, 1.0805530922099171, 0.8917229235261498, 0.7019764492592149, 0.5115086467380252, 0.32051523450503044, 0.12919247120219393, -0.06226304609803768, -0.25365458390950685], [5.926916757346022, 5.911843704019252, 5.890695831654101, 5.863494871118991, 5.83026877323962, 5.791051680077596, 5.745883889847168, 5.694811815506075, 5.637887937063104, 5.575170747651332, 5.506724693422478, 5.432620107324118, 5.352933136827836, 5.267745665682549, 5.177145229773413, 5.081224927172789, 4.98008332247568, 4.8738243455179475, 4.7625571845813734, 4.646396174195329, 4.525460677650309, 4.399874964344087, 4.269768082086507, 4.135273724494136, 3.9965300936110326, 3.8536797578968067, 3.7068695057278926, 3.5562501945625637, 3.4019765959247, 3.2442072363655874, 3.0831042345671626, 2.918833134754116, 2.7515627365860054, 2.5814649217041956, 2.4087144771118587, 2.2334889155685036, 2.0559682931836254, 1.876335024396871, 1.6947736945348841, 1.5114708701373911, 1.3266149072474818, 1.1403957578630317, 0.9530047747481929, 0.7646345148054903, 0.5754785412105823, 0.38573122451302394, 0.19558754290737707, 0.005242881879945371, -0.18510716656303083, -0.37526700487937376], [5.871318704123389, 5.852573844008785, 5.827815068643523, 5.7970678193429475, 5.760363690984187, 5.71774039954028, 5.669241743324461, 5.614917557984434, 5.554823665292875, 5.4890218157867885, 5.41757962531466, 5.340570505556591, 5.258073588588842, 5.170173645570279, 5.076960999634266, 4.978531433075549, 4.874986088927472, 4.766431367030669, 4.652978814700039, 4.534745012102338, 4.4118514524621775, 4.284424417219523, 4.15259484626698, 4.016498203400198, 3.8762743371196713, 3.73206733692694, 3.584025385262899, 3.4323006052403153, 3.277048904327047, 3.118429814140586, 2.9566063265185303, 2.791744726033457, 2.6240144191242813, 2.4535877600196896, 2.2806398736325217, 2.105348475607078, 1.9278936897042884, 1.7484578627123653, 1.5672253770731601, 1.3843824614167317, 1.2001169991988492, 1.0146183356380303, 0.8280770831505397, 0.6406849254832419, 0.4526344207455891, 0.26411880354315725, 0.07533178641601573, -0.1135326392139922, -0.30228040238255843, -0.49071755200393724], [5.801413621867956, 5.77926256347147, 5.7511729221208165, 5.717173561821307, 5.677299419213958, 5.631591467675737, 5.580096675216644, 5.522867956216907, 5.459964117053881, 5.391449795674519, 5.317395395175513, 5.237877011459351, 5.152976355040634, 5.0627806670830005, 4.967382629752931, 4.866880270982558, 4.761376863739341, 4.650980819906105, 4.535805578880511, 4.415969491008401, 4.291595695970816, 4.162811996249657, 4.0297507258019865, 3.8925486140779504, 3.751346645522018, 3.6062899147019385, 3.4575274772142666, 3.305212196519656, 3.149500586865323, 2.99055265245608, 2.8285317230391933, 2.6636042860720313, 2.4959398156449444, 2.3257105983351836, 2.1530915561707977, 1.9782600668864185, 1.8013957816556558, 1.6226804404873638, 1.442297685475507, 1.2604328720944835, 1.0772728787338561, 0.8930059146681637, 0.7078213266591784, 0.5219094043893043, 0.33546118492606153, 0.14866825641859355, -0.0382774387721152, -0.2251838013069823, -0.4118587722638928, -0.5981105304912157], [5.718349350097728, 5.693113631606925, 5.662027854012999, 5.62512396005378, 5.582439870974964, 5.534019447563467, 5.479912445077496, 5.420174462119667, 5.3548668835056725, 5.28405681718724, 5.207817025294179, 5.12622584936636, 5.0393671298525025, 4.947330119958437, 4.850209393933404, 4.748104749888621, 4.641121107247979, 4.5293683989362385, 4.412961458415518, 4.292019901686152, 4.166668004373164, 4.037034574024655, 3.903252817753354, 3.765460205357291, 3.623798328060294, 3.4784127530174325, 3.3294528737349296, 3.17707175655823, 3.021425983385986, 2.862675490771574, 2.7009834055774693, 2.5365158773513716, 2.3694419075963116, 2.1999331761101826, 2.028163864573145, 1.8543104775641701, 1.6785516611906623, 1.5010680195174972, 1.3220419289841456, 1.1416573510005459, 0.9600996429143283, 0.7775553675436, 0.5942121014710471, 0.4102582422963139, 0.22588281504472718, 0.04127527793131547, -0.14337467232032408, -0.32787729540422234, -0.5120430024030399, -0.695682550603486], [5.623489801858733, 5.595541611494655, 5.561843623873852, 5.52243046595654, 5.477342637426756, 5.426626469076188, 5.370334075196162, 5.3085233000266765, 5.241257658317541, 5.168606270062677, 5.090643789474651, 5.007450328272423, 4.919111373361141, 4.82571769898857, 4.72736527346841, 4.624155160566373, 4.516193415650326, 4.403590976711237, 4.286463550366886, 4.164931492965493, 4.039119686911439, 3.909157412340149, 3.775178214274017, 3.637319765395865, 3.4957237245809565, 3.3505355913329264, 3.2019045562732056, 3.049983347837571, 2.8949280753373534, 2.736898068546573, 2.576055713979816, 2.412566288029123, 2.2465977871313183, 2.0783207551403153, 1.907908108081783, 1.7355349564702327, 1.561378425371135, 1.3856174723929335, 1.2084327037960145, 1.0300061889075556, 0.8505212730329939, 0.6701623890563215, 0.48911486792283865, 0.3075647481990742, 0.12569858490558006, -0.05629674218095493, -0.2382342205593181, -0.4199268971717495, -0.6011880705108578, -0.7818314824680294], [5.518392568310525, 5.488148633007377, 5.452265253992517, 5.410779303863549, 5.363733412238624, 5.311175921951625, 5.253160839376634, 5.189747778932739, 5.12100190182618, 5.04699384909281, 4.967799669009658, 4.883500738950175, 4.794183681763488, 4.699940276763569, 4.600867365419778, 4.497066751845713, 4.3886450981886025, 4.275713815026731, 4.158388946887549, 4.036791053004067, 3.911045083432102, 3.781280250655643, 3.647629896812293, 3.510231356675206, 3.369225816532324, 3.2247581691079255, 3.0769768646755526, 2.9260337585153224, 2.77208395487236, 2.615285647576706, 2.4557999574884546, 2.2937907669351856, 2.1294245513117906, 1.962870208015752, 1.7942988828936521, 1.6238837943772424, 1.4518000554898005, 1.278224493905655, 1.1033354702478055, 0.9273126948103158, 0.7503370428938467, 0.5725903689440515, 0.39425531968384464, 0.215515146431547, 0.0365535167977622, -0.14244567404549857, -0.3212984923295471, -0.4998211546933898, -0.6778302170335637, -0.8551427630053458], [5.404783343122394, 5.3726980858828135, 5.33509201817299, 5.292003782769612, 5.243477655747263, 5.189563500981758, 5.130316718911641, 5.065798189610491, 4.996074210228527, 4.921216426867809, 4.841301760961025, 4.756412330229515, 4.666635364301764, 4.572063115079063, 4.4727927619404415, 4.368926311884287, 4.260570494709265, 4.1478366533422255, 4.030840629425825, 3.9097026442834077, 3.7845471753834694, 3.655502828430642, 3.52270220521464, 3.3862817673529575, 3.246381696067331, 3.1031457481380587, 2.9567211081841913, 2.807258237421385, 2.6549107190528325, 2.499835100452142, 2.342190732300324, 2.1821396048421953, 2.0198461814304567, 1.8554772295284736, 1.6892016493454434, 1.5211903002800025, 1.3516158253506534, 1.180652473793385, 1.008475922008812, 0.8352630930427886, 0.6611919747860291, 0.4864414370795078, 0.3111910479136156, 0.13562088890990676, -0.04008862972494376, -0.21575695458281474, -0.3912035745849798, -0.5662482064694341, -0.7407109800441424, -0.914412623015812], [5.284527586631032, 5.251085664912947, 5.2122478977079965, 5.168054193447364, 5.118549964149611, 5.063786078756757, 5.003818810863009, 4.938709780889831, 4.868525892766803, 4.7933392651833024, 4.713227157481689, 4.628271890268089, 4.538560760822427, 4.444185953394557, 4.345244444478717, 4.241837903163629, 4.134072586660633, 4.022059231117224, 3.905912937828172, 3.7857530549611593, 3.6617030549184766, 3.5338904074607753, 3.402446448723279, 3.26750624625902, 3.129208460247803, 2.9876952010134947, 2.8431118829960598, 2.695607075328395, 2.545332349171498, 2.3924421219648644, 2.237093498752115, 2.0794461107449553, 1.9196619512913093, 1.7579052094162035, 1.5943421011064496, 1.4291406985124753, 1.2624707572428358, 1.0945035419288414, 0.9254116502385826, 0.7553688355211483, 0.5845498282633229, 0.41313015654219165, 0.24128596565818294, 0.06919383713386251, -0.10296939273552241, -0.27502681459328127, -0.44680162780761223, -0.6181173221461944, -0.7887978591523919, -0.9586678530366602], [5.159599895033379, 5.125308242687945, 5.085749989659364, 5.040965784726704, 4.991001646687886, 4.9359089170722505, 4.875744207383672, 4.810569340928406, 4.740451289287465, 4.665462103498797, 4.585678840019964, 4.50118348154743, 4.412062852773794, 4.318408531169555, 4.220316752881064, 4.117888313841379, 4.011228466195639, 3.9004468101473573, 3.78565718133681, 3.6669775338672217, 3.5445298190989485, 3.4184398603362114, 3.288837223535147, 3.1558550841660296, 3.0196300903664692, 2.8803022225262165, 2.7380146494478512, 2.5929135812311546, 2.445148119032351, 2.2948701018525934, 2.1422339505131207, 1.9873965089774281, 1.8305168831834915, 1.67175627755166, 1.5112778293362203, 1.3492464409908351, 1.1858286107201295, 1.021192261391525, 0.85550656798315, 0.6889417837451038, 0.5216690652527443, 0.3538602965317251, 0.1856879124355505, 0.017324721457102177, -0.15105627184377202, -0.31928204461412946, -0.48717973350062005, -0.6545768122782578, -0.8213012691327887, -0.9871817834144497], [5.032051577571655, 4.997431081003439, 4.957675386180028, 4.912825344765278, 4.862927043208549, 4.808031755387745, 4.748195889921948, 4.683480932207746, 4.613953381238833, 4.539684681273795, 4.460751148422311, 4.377233892225181, 4.289218732308801, 4.1967961101996885, 4.100060996389702, 3.999112792747442, 3.894055230376112, 3.7849962630227934, 3.6720479561486794, 3.5553263717742314, 3.434951449217614, 3.311046881848933, 3.1837399899869387, 3.0531615900687896, 2.919445860227322, 2.7827302024139464, 2.643155101208857, 2.5008639794636274, 2.3560030509245333, 2.20872116998805, 2.059169678742892, 1.907502251455788, 1.7538747366607854, 1.5984449970143435, 1.4413727470807876, 1.2828193892147906, 1.122947847709551, 0.9619224013810587, 0.7999085147605175, 0.6370726680683437, 0.47358218614449477, 0.30960506651087694, 0.14530980674254268, -0.019134768674961222, -0.1835596818241687, -0.34779597499191894, -0.5116748842848367, -0.6750280130456323, -0.8376875048920597, -0.9994862162006876], [4.903976974092318, 4.869553919318934, 4.830127068718303, 4.785736936044619, 4.736429135159916, 4.682254333162743, 4.623268198324294, 4.5595313428854976, 4.49110926077384, 4.418072260303928, 4.34049539193095, 4.258458371131244, 4.1720454964892735, 4.081345563075125, 3.9864517712015717, 3.887461630654452, 3.7844768604947774, 3.6776032845355155, 3.5669507226004704, 3.4526328776769915, 3.334767219078467, 3.213474861736663, 3.0888804417479445, 2.9611119883012624, 2.8303007921195045, 2.6965812705494026, 2.560090829438628, 2.4209697219419875, 2.2793609044018273, 2.1354098894507336, 1.9892645964874591, 1.8410751996797439, 1.6909939736502069, 1.5391751370038773, 1.385774693858155, 1.2309502735380304, 1.0748609686013015, 0.9176671713602105, 0.7595304090675098, 0.6006131779362803, 0.44107877616409796, 0.28109113613308745, 0.12081465595832608, -0.03958596944233572, -0.19994591758343971, -0.3601004077781568, -0.5198848704615906, -0.679135116297122, -0.8376875048920597, -0.9953791129491979], [4.777479066043686, 4.743776497093932, 4.70519937712065, 4.66178734672237, 4.613585014694923, 4.560641912192876, 4.503012441832933, 4.44075582179156, 4.373936024954312, 4.302621713179365, 4.226886166742818, 4.146807209038253, 4.062467126607939, 3.9739525845878467, 3.8813545376533627, 3.784768136557212, 3.6842926303556305, 3.5800312644232446, 3.472091174361476, 3.3605832759094643, 3.2456221509706493, 3.1273259298721197, 3.0058161699777157, 2.881217730779622, 2.753658645596798, 2.623269990012086, 2.4901857471831956, 2.3545426701659427, 2.2164801413912487, 2.0761400294402677, 1.9336665432648266, 1.7892060840029833, 1.6429070945419573, 1.494919906983029, 1.3453965881651473, 1.1944907834059673, 1.0423575586209046, 0.889153240982421, 0.7350352582832931, 0.5801619771689057, 0.42469254040482696, 0.2687867033468496, 0.11260466978157213, -0.043693072693825497, -0.19994591758343971, -0.3559933045266671, -0.5116748842848368, -0.6668306835108844, -0.8213012691327887, -0.9749279121818233], [4.654634945578692, 4.622164076124065, 4.584943620629288, 4.543011825628433, 4.4964117788753954, 4.445191365068313, 4.389403216644801, 4.32910465969857, 4.264357655072978, 4.195228734692087, 4.12178893319461, 4.044113714941014, 3.962282896468792, 3.876380564475576, 3.7864949894143685, 3.6927185347896847, 3.5951475622478126, 3.4938823325587016, 3.3890269025912474, 3.2806890183878243, 3.1689800044479433, 3.0540146493348033, 2.9359110877222827, 2.8147906790035777, 2.6907778825862194, 2.56400013000162, 2.434587693960563, 2.3026735544891825, 2.168393262282999, 2.0318847994194194, 1.8932884375718189, 1.7527465938709201, 1.6104036845615606, 1.4664059766052395, 1.3209014373809307, 1.1740395826385925, 1.0259713228616336, 0.8768488081961832, 0.7268252721065391, 0.576054873917416, 0.42469254040482696, 0.2728938065983393, 0.12081465595832597, -0.03138863990758778, -0.1835596818241687, -0.3355421037592925, -0.48717973350062005, -0.6383167531330949, -0.7887978591523922, -0.9384684220497601], [4.537461709759165, 4.5067135289995015, 4.471334395441157, 4.431360663535442, 4.386833408994061, 4.337798386581035, 4.284305983096593, 4.226411165601331, 4.16417342493383, 4.097656714579816, 4.026929384955616, 3.9520641131734866, 3.8731378283609743, 3.7902316326110332, 3.7034307176441397, 3.612824277268045, 3.5185054157251066, 3.4205710520213852, 3.3191218203358144, 3.21426196661178, 3.1060992414373647, 2.994744789324337, 2.8803130344996504, 2.7629215633268176, 2.64269100347797, 2.519744899980772, 2.394209588267555, 2.2662140643571194, 2.1358898523026024, 2.00337086904163, 1.8687932867876023, 1.7322953931035454, 1.5940174488022896, 1.4541015438190017, 1.3126914512041767, 1.1699324793871029, 1.0259713228616336, 0.8809559114476728, 0.735035258283293, 0.5883593067036538, 0.44107877616409785, 0.2933450073657139, 0.14530980674254268, -0.0028747095297982916, -0.15105627184377224, -0.29908261362722954, -0.44680162780761246, -0.5940615231122468, -0.7407109800441425, -0.8865993063729999], [4.42788333987783, 4.399320550512224, 4.366237161892949, 4.328667169438203, 4.286649178854914, 4.2402263664687645, 4.189446434857599, 4.134361563833803, 4.075028356826013, 4.011507782715273, 3.943865113185387, 3.8721698556518467, 3.7964956818382682, 3.716920352073717, 3.6335256353887067, 3.5463972254920004, 3.455624652714528, 3.361301192010919, 3.263523767113182, 3.1623928509350194, 3.0580123623291153, 2.9504895593034886, 2.8399349288066427, 2.7264620731947544, 2.610187593497573, 2.4912309696029826, 2.3697144374833385, 2.2457628635897446, 2.1195036165433314, 1.991066436255392, 1.8605833006108483, 1.7281882898520557, 1.5940174488022896, 1.4582086470704914, 1.3209014373809307, 1.1822369121733405, 1.0423575586209046, 0.9014071122150474, 0.7595304090675097, 0.6168732370814433, 0.47358218614449443, 0.32980449749777685, 0.18568791243555027, 0.04138052049104968, -0.10296939273552252, -0.2472134979504691, -0.3912035745849801, -0.5347916631017806, -0.6778302170335644, -0.8201722545969558], [4.327699109738683, 4.301748530399953, 4.2713776136539545, 4.236617567670676, 4.197504110747096, 4.154077434604221, 4.10638216308737, 4.054467306312163, 3.9983862103033068, 3.9381965021779566, 3.873960030929954, 3.8057428038758023, 3.7336149188276897, 3.6576504920632504, 3.5779275821660743, 3.49452810981524, 3.4075377736062786, 3.3170459619900705, 3.2231456614201743, 3.1259333608029563, 3.0255089523487184, 2.921975628925699, 2.815439778022426, 2.7060108724273797, 2.593801357738302, 2.4789265368167444, 2.3615044513065846, 2.241655760338255, 2.1195036165433314, 1.9951735395068817, 1.8687932867876023, 1.7404927226382934, 1.6104036845615606, 1.478659847837866, 1.3453965881651473, 1.2107508425511302, 1.074860968601301, 0.9378666023471104, 0.799908514760517, 0.6611284671022912, 0.5216690652527439, 0.3816736131745373, 0.2412859656581826, 0.10065038050151598, -0.040088629724944425, -0.18078644617442519, -0.32129849232954755, -0.4614803825644643, -0.601188070510858, -0.7402779970753155], [4.238554041630866, 4.21559959853541, 4.188313341883726, 4.156723310149036, 4.120861964224391, 4.080766154066905, 4.036477080831937, 3.9880402545361187, 3.935505447292728, 3.87892664216749, 3.8183619777073217, 3.7538736881990418, 3.6855280397194403, 3.613395262042402, 3.5375494764730666, 3.4580686196831767, 3.3750343636258817, 3.288532031612281, 3.1986505106359577, 3.1054821600355815, 3.0091227165894474, 2.9096711961394615, 2.807229791845672, 2.70190376917589, 2.593801357738302, 2.4830336400682342, 2.3697144374833385, 2.2539601931244926, 2.1358898523026024, 2.015624740274256, 1.8932884375718189, 1.769006653016083, 1.642907094541957, 1.5151193379699288, 1.3857746938581545, 1.255006072571978, 1.1229478477095505, 0.9897357180238708, 0.8555065679831496, 0.7203983271127575, 0.5845498282633222, 0.4481006649505812, 0.3111910479136152, 0.17396166103883226, 0.036553516797761976, -0.10089218865278471, -0.23823422055931853, -0.37533145069992097, -0.5120430024030407, -0.6482283953077888], [4.16191189510816, 4.142288317998093, 4.118408259628293, 4.090296258372991, 4.057981201213812, 4.021496294056439, 3.980879027609305, 3.936171138859358, 3.887418568184479, 3.8346714121466423, 3.777983872014314, 3.7174141980669786, 3.6530246297390434, 3.5848813316646124, 3.51305432568885, 3.437617418915802, 3.3586481278666107, 3.2762275988260434, 3.190440524459204, 3.101375056784092, 3.0091227165894474, 2.913778299390951, 2.815439778022426, 2.7142082019621276, 2.610187593497573, 2.5034848408356085, 2.394209588267555, 2.2824741235022823, 2.168393262282999, 2.052084230406319, 1.9336665432648261, 1.813261883036931, 1.6909939736502064, 1.5669884536466894, 1.4413727470807873, 1.3142759325824445, 1.185828610720129, 1.0561627697999147, 0.925411650238582, 0.7937096076500738, 0.6611919747860284, 0.5279949224722217, 0.3942553196838442, 0.26011059290337557, 0.12569858490557928, -0.008842586885257964, -0.1433746723203243, -0.277759430587651, -0.41185877226389334, -0.5455349012105488], [4.099031132097581, 4.0830184579876265, 4.06281020640566, 4.03842714269623, 4.009894322105562, 3.97724106403559, 3.940500921916297, 3.899711648727295, 3.854915158204082, 3.806157481768852, 3.7534887212300974, 3.696962997299604, 3.6366383939797724, 3.572576898878375, 3.504844339512096, 3.4335103156643125, 3.3586481278666107, 3.280334702077533, 3.1986505106359577, 3.1136794895703295, 3.0255089523487184, 2.9342295001583256, 2.8399349288066427, 2.7427221323399174, 2.64269100347797, 2.539944330967672, 2.434587693960563, 2.32672935352313, 2.2164801413912487, 2.1039533460830797, 1.989264596487459, 1.8725317430473973, 1.7538747366607852, 1.6334155054227337, 1.51127782933622, 1.3875872131197609, 1.2624707572428353, 1.1360570273215553, 1.0084759220088113, 0.8798585395146175, 0.7503370428938463, 0.6200445242397491, 0.4891148679228384, 0.3576826130156462, 0.22588281504472663, 0.09385090721198197, -0.0382774387721162, -0.17036645210037193, -0.30228040238255866, -0.43388373911755795], [4.050944252989331, 4.038763227966779, 4.022432100712653, 4.001967652564168, 3.9773909121251654, 3.9487271336578003, 3.9160057711320806, 3.87926044795992, 3.838528922444811, 3.7938530489826148, 3.7452787350533434, 3.6928558940481144, 3.6366383939797724, 3.5766840021298645, 3.51305432568885, 3.44581474845055, 3.3750343636258817, 3.3007859028449076, 3.2231456614201743, 3.142193419948119, 3.058012362329115, 2.970688990290389, 2.8803130344996504, 2.7869773623607657, 2.6907778825862194, 2.5918134466444323, 2.490185747183195, 2.3859992135335966, 2.279360904401827, 2.170380397859124, 2.0591696787428915, 1.9458430235847137, 1.8305168831834913, 1.7133097629443736, 1.5943421011064487, 1.4737361449843043, 1.351615825350653, 1.2281066290890825, 1.1033354702478055, 0.9774305596268877, 0.8505212730329933, 0.7227380183369884, 0.5942121014710465, 0.4650755915029246, 0.3354611849260613, 0.20550206930497283, 0.07533178641601529, -0.05491590497580867, -0.1851071665630315, -0.315108218023621], [4.018440843008935, 4.010249297588989, 3.997936949928436, 3.981516451796793, 3.9610046763658944, 3.936422700871563, 3.9077957849553266, 3.8751533447084308, 3.838528922444811, 3.797960152234104, 3.7534887212300974, 3.705160326834352, 3.6530246297390434, 3.597135202897239, 3.5375494764730666, 3.4743286788283396, 3.407537773606278, 3.3372453929769708, 3.263523767113182, 3.186448649968967, 3.1060992414373647, 3.022558105967149, 2.9359110877222827, 2.8462472223712316, 2.753658645596798, 2.6582404984204766, 2.5600908294386278, 2.459310494070913, 2.3560030509245333, 2.250274655380764, 2.1422339505131203, 2.031991955449257, 1.919661951291309, 1.8053593647119013, 1.689201649345443, 1.5713081650965746, 1.4518000554897998, 1.330800123186322, 1.2084327037960136, 1.0848235381141662, 0.9600996429143271, 0.8343891804299792, 0.707821326659178, 0.5805261386274878, 0.45263442074558846, 0.3242775903989098, 0.19558754290737707, 0.06669651599405757, -0.06226304609803793, -0.1911586287013723], [4.002054607249663, 3.9979448648027516, 3.989726963751682, 3.9774093485453035, 3.9610046763658944, 3.9405298041230523, 3.9160057711320806, 3.887457777494668, 3.854915158204082, 3.818411353001479, 3.777983872014314, 3.7336742572121415, 3.68552803971944, 3.6335946930293024, 3.5779275821660743, 3.5185839088491875, 3.455624652714528, 3.389114508653731, 3.3191218203358144, 3.2457185099794335, 3.168980004447943, 3.088985157743193, 3.0058161699777153, 2.919558502908548, 2.8303007921195036, 2.7381347559421165, 2.6431551012088565, 2.545459425935456, 2.4451481190323507, 2.3423242571482916, 2.2370934987521145, 2.1295639755615277, 2.019846181430456, 1.9080528588091403, 1.794298882893651, 1.678701143583853, 1.5613784253711338, 1.4424512852793128, 1.322041928984145, 1.2002740852387295, 1.0772728787338552, 0.9531647015239162, 0.8280770831505397, 0.7021385595973542, 0.5754785412105821, 0.44822717972115855, 0.3205152345050297, 0.1924739382190593, 0.06423486195059422, -0.06407021998071255], [4.002054607249663, 4.002051968054241, 3.997936949928436, 3.989713781331541, 3.9773909121251654, 3.960981004890427, 3.940500921916297, 3.915971707872458, 3.8874185681844784, 3.8548708431335417, 3.8183619777073217, 3.7779294872329894, 3.7336149188276893, 3.6854638087060625, 3.6335256353887067, 3.577853768859654, 3.518505415725106, 3.455541560429775, 3.389026902591247, 3.3190297905167494, 3.2456221509706493, 3.168879415264833, 3.088880441747944, 3.005707434773091, 2.9194458602273214, 2.8301843577096433, 2.738014649447851, 2.6430314460477264, 2.5453323491714976, 2.4450177512455307, 2.3421907323003226, 2.236956954048805, 2.1294245513117898, 2.0197040209021315, 1.9079081080817826, 1.7941516907084163, 1.678551661190662, 1.5612268063732497, 1.4422976854755059, 1.3218865062085956, 1.2001169991988487, 1.0771142908461648, 0.9530047747481925, 0.8279159818223558, 0.7019764492592142, 0.5753155884418174, 0.4480635519667533, 0.3203510999035657, 0.19230946542993152, 0.06407021998071279], [4.018440843008935, 4.022503168821616, 4.022432100712653, 4.01822771170933, 4.009894322105562, 3.9974404950224898, 3.980879027609305, 3.9602269378933057, 3.9355054472927278, 3.9067399588103022, 3.873960030929954, 3.837199347243456, 3.796495681838268, 3.7518908604821064, 3.7034307176441392, 3.65116504939697, 3.5951475622478126, 3.535435817951415, 3.4720911743614757, 3.405178722381293, 3.3347672190784663, 3.26092901703236, 3.1837399899869383, 3.103279454885362, 3.0196300903664683, 2.932877851806883, 2.843111882996059, 2.7504244245350042, 2.6549107190528316, 2.5566689133385214, 2.455799957488454, 2.352407501173369, 2.246597787131318, 2.1384795419960683, 2.0281638645731435, 1.9157641116782824, 1.8013957816556554, 1.6851763956954984, 1.5672253770731595, 1.4476639284335975, 1.3266149072474809, 1.2042026995668238, 1.080553092209916, 0.9557931435068622, 0.8300510527385515, 0.7034560284032436, 0.5761381554460906, 0.44822826158807116, 0.31985778289165506, 0.19115862870137168], [4.050944252989331, 4.0589626589536785, 4.06281020640566, 4.062482941730178, 4.057981201213812, 4.04930961069925, 4.036477080831937, 4.019496797903772, 3.9983862103033063, 3.973167010586346, 3.9438651131853866, 3.9105106277807717, 3.873137828360974, 3.8317851180037468, 3.786494989414368, 3.7373139812615133, 3.6842926303556296, 3.627485419718942, 3.56695072260047, 3.5027507424935633, 3.4349514492176136, 3.3636225111296, 3.2888372235351464, 3.2106724333726393, 3.1292084602478023, 3.044529013899874, 2.9567211081841904, 2.865874971659568, 2.7720839548723597, 2.6754444344324586, 2.576055713979815, 2.4740199221432353, 2.369441907596311, 2.262429131318317, 2.1530915561707973, 2.0415415339032843, 1.9278936897042875, 1.8122648044161573, 1.694773694534883, 1.5755410901181037, 1.4546895107268172, 1.33234313952825, 1.2086276956892532, 1.0836703051913676, 0.957599370200275, 0.8305444371239025, 0.7026360634947236, 0.574005683813072, 0.44478547448930866, 0.3151082180236205], [4.099031132097581, 4.110831774630439, 4.118408259628293, 4.121752801740645, 4.12086196422439, 4.115736662475294, 4.10638216308737, 4.092808078441088, 4.075028356826013, 4.053061268107987, 4.026929384955616, 3.9966595596453156, 3.9622828964687917, 3.9238347197712744, 3.8813545376533622, 3.8348860013737838, 3.784476860494777, 3.730178913816182, 3.672047956148678, 3.610143720980842, 3.5445298190989485, 3.475273673222591, 3.402446448723278, 3.3261229804972032, 3.2463816960673304, 3.163304534993811, 3.076976864675552, 2.9874873926294354, 2.894928075337353, 2.7993940237547075, 2.700983405577469, 2.599797344368237, 2.4959398156449435, 2.3895175400389768, 2.2806398736325213, 2.1694186955877908, 2.055968293183625, 1.9404052443775834, 1.8228482980142204, 1.7034182518026093, 1.5822378281885425, 1.4594315482489097, 1.3351256037378865, 1.2094477274163695, 1.0825270617979286, 0.9544940264461512, 0.8254801839597163, 0.6956181047829401, 0.5650412309806704, 0.4338837391175583], [4.161911895108159, 4.177258826406483, 4.188313341883726, 4.195064082277961, 4.197504110747096, 4.195630919996935, 4.189446434857599, 4.178957010305632, 4.16417342493383, 4.145110869875514, 4.12178893319461, 4.094231579757586, 4.062467126607939, 4.026528213868514, 3.9864517712015703, 3.9422789798610625, 3.894055230376112, 3.841830075909173, 3.7856571813368096, 3.725594268105405, 3.6617030549184757, 3.594049194316528, 3.5227022052146397, 3.4477354014670705, 3.3692258165323237, 3.28725412431606, 3.201904556273205, 3.1132648148544364, 3.0214259833859853, 2.926482432475367, 2.828531723039193, 2.7276745060527436, 2.624014419124281, 2.517657980000402, 2.408714477111858, 2.297295857272296, 2.1835166106453494, 2.0674936530982433, 1.9493462060628532, 1.829195674027611, 1.7071655197861952, 1.5833811375711577, 1.457969724202879, 1.3310601483862365, 1.2027828182892903, 1.073269547540089, 0.9426534197792444, 0.8110686519075033, 0.6786504561688012, 0.5455349012105484], [4.238554041630866, 4.257153083928124, 4.2713776136539545, 4.281213014142505, 4.286649178854914, 4.287680521764462, 4.284305983096593, 4.276529030417902, 4.264357655072978, 4.247804363972754, 4.226886166742818, 4.201624558244864, 4.1720454964892735, 4.138179375961505, 4.100060996389702, 4.057729526985626, 4.0112284661956386, 3.9606055970031098, 3.9059129378281714, 3.8472066890752723, 3.784547175383469, 3.7179987836387767, 3.6476298968122927, 3.5735128236920715, 3.495723724580956, 3.4143425330367196, 3.329452873734929, 3.241141976538943, 3.1495005868653227, 3.0546228724367923, 2.9566063265185294, 2.8555516677372488, 2.7515627365860054, 2.644746388721062, 2.535212385160491, 2.423073279497298, 2.308444302243002, 2.1914432424204913, 2.072190326527846, 1.9508080949974782, 1.8274212762775561, 1.7021566586650954, 1.5751429600224072, 1.4465106955107998, 1.3163920434774212, 1.1849207096330792, 1.052231789660579, 0.918461630394781, 0.78374768971701, 0.6482283953077884], [4.327699109738683, 4.3492026856956505, 4.366237161892949, 4.378785034254775, 4.386833408994061, 4.390374015861702, 4.389403216644801, 4.383922008905181, 4.373936024954312, 4.359455526065744, 4.34049539193095, 4.317075105369428, 4.2892187323088, 4.256954897055442, 4.220316752881064, 4.179341947955493, 4.134072586660633, 4.084555186325359, 4.030840629425824, 3.9729841113002733, 3.9110450834321013, 3.8450871923594363, 3.7751782142740167, 3.701389985376578, 3.6237983280602934, 3.542482972998145, 3.4575274772142657, 3.369019138223448, 3.277048904327047, 3.181711281157452, 3.0831042345671626, 2.9813290899622507, 2.876490428183658, 2.7686959780433096, 2.658056505625484, 2.544685700467165, 2.428700058734363, 2.310218763514429, 2.189363562347374, 2.0662586421220412, 1.9410305014656877, 1.8138078207580857, 1.6847213299037418, 1.5539036739980776, 1.42148927702563, 1.2876142037303193, 1.152416019799726, 1.0160336505070517, 0.8786072379560037, 0.7402779970753159], [4.42788333987783, 4.45189617979289, 4.471334395441157, 4.4861780127420525, 4.4964117788753954, 4.5020251779546925, 4.503012441832933, 4.499372556029744, 4.491109260773839, 4.478231047159682, 4.46075114842231, 4.438687526339295, 4.412062852773794, 4.38090448637769, 4.345244444478716, 4.305119370180494, 4.260570494709264, 4.211643595046017, 4.1583889468875475, 4.10086127298478, 4.039119686911438, 3.9732276323208615, 3.903252817753353, 3.829267147061083, 3.751346645522017, 3.669571381718804, 3.584025385262899, 3.49479656044845, 3.4019765959246997, 3.3056608704797, 3.2059483550321555, 3.102941510932117, 2.9967461846750187, 2.8874714991372477, 2.7752297414450116, 2.660136247591728, 2.5423092839224943, 2.421869925607419, 2.298941932228708, 2.173651620609319, 2.0461277350138967, 1.9165013148553256, 1.7849055600428887, 1.6514756941103483, 1.5163488252646236, 1.379663805497846, 1.2415610879075432, 1.1021825823715956, 0.961671509726233, 0.820172254596956], [4.537461709759165, 4.563547341885881, 4.584943620629288, 4.601628559866617, 4.613585014694923, 4.62080069904863, 4.623268198324294, 4.620984976999611, 4.613953381238833, 4.60218063648193, 4.5856788400199635, 4.5644649485642965, 4.538560760822427, 4.50799289509835, 4.472792761940441, 4.432996531865, 4.388645098188602, 4.339784035007444, 4.286463550366886, 4.228738434669286, 4.166668004373163, 4.100316041041522, 4.0297507258019865, 3.955044569286085, 3.8762743371196704, 3.7935209710410533, 3.7068695057278926, 3.616408981418317, 3.5222323524160615, 3.424436391573638, 3.323121590851683, 3.218392058056681, 3.110355409863151, 2.9991226612302384, 2.8848081113263464, 2.7675292260790068, 2.6474065174707033, 2.524563419704659, 2.3991261623678555, 2.2712236407215904, 2.1409872832528904, 2.0085509166228532, 1.8740506281507066, 1.7376246259748922, 1.599413097034853, 1.4595580630194869, 1.3182032344302503, 1.1754938629089116, 1.0315765919816662, 0.8865993063730003], [4.6546349455786915, 4.682322862979818, 4.705199377120649, 4.723240980836483, 4.736429135159916, 4.744750288370878, 4.748195889921947, 4.746762399224612, 4.740451289287464, 4.729269045202589, 4.713227157481687, 4.692342110248802, 4.666635364301763, 4.6361333350597755, 4.600867365419777, 4.560873693549506, 4.516193415650325, 4.466872443728103, 4.412961458415518, 4.354515856894287, 4.291595695970816, 4.224265630363769, 4.152594846266979, 4.076656990255952, 3.9965300936110313, 3.9122964921349905, 3.8240427415474194, 3.73185952854288, 3.635841577604192, 3.536087553666628, 3.432699960733017, 3.3257850365439587, 3.2154526434113593, 3.1018161553274775, 2.9849923414654933, 2.865101246191277, 2.742266065709697, 2.616613021472186, 2.488271230475673, 2.357372572586134, 2.2240515550231192, 2.088445174144493, 1.9506927746734124, 1.8109359065122081, 1.6693181792902856, 1.5259851147955308, 1.3810839974408284, 1.2347637229193777, 1.0871746452042983, 0.9384684220497606], [4.777479066043686, 4.806272452302067, 4.830127068718302, 4.849018403061485, 4.862927043208549, 4.871838697091538, 4.875744207383671, 4.874639560909118, 4.868525892766802, 4.857409485164015, 4.8413017609610245, 4.820219271933309, 4.794183681763488, 4.763221743780435, 4.72736527346841, 4.686651115774508, 4.641121107247979, 4.590822033050351, 4.5358055788805105, 4.476128277864154, 4.4118514524621775, 4.343041151457707, 4.269768082086507, 4.192107537380515, 4.110139318799163, 4.023947654227981, 3.9336211114287543, 3.839252507030159, 3.740938811152401, 3.6387810477638682, 3.532884190872165, 3.4233570566562297, 3.310312191650353, 3.193865757095005, 3.074137409573311, 2.9512501780558207, 2.8253303374799263, 2.6965072789938267, 2.5649133769983794, 2.43068385312345, 2.2939566372785527, 2.1548722259205375, 2.013573537683991, 1.8702057665226748, 1.7249162325129181, 1.5778542304722913, 1.4291708765490778, 1.2790189529402265, 1.127552750897306, 0.9749279121818238], [4.903976974092317, 4.9333608610227255, 4.957675386180026, 4.97689556474599, 4.991001646687885, 4.999979137052963, 5.003818810863008, 5.002516722593624, 4.996074210228525, 4.984497893884674, 4.967799669009657, 4.94599669415831, 4.919111373361141, 4.887171333102683, 4.850209393933403, 4.808263536744374, 4.76137686373934, 4.709597554144288, 4.652978814700038, 4.5915788249887175, 4.525460677650308, 4.454692313550697, 4.379346451967841, 4.299500515867793, 4.215236552347371, 4.12664114832522, 4.033805341567901, 3.936824527142429, 3.835798359391395, 3.730830649531395, 3.622029258979982, 3.5095059885207727, 3.393376463420582, 3.273760014616645, 3.1507795560960172, 3.0245614585931366, 2.895235419735359, 2.7629343307698706, 2.627794140008958, 2.489953713133916, 2.349554690501185, 2.2067413415972976, 2.0616604167922405, 1.9144609965435229, 1.7652943382059259, 1.6143137206043545, 1.4616742865294745, 1.307532883318016, 1.1520479016815228, 0.9953791129491985], [5.0320515775716546, 5.061501300984152, 5.085749989659363, 5.104772726430497, 5.11854996414961, 5.127067545773623, 5.130316718911641, 5.128294144818626, 5.12100190182618, 5.108447483206922, 5.09064378947465, 5.067609115128176, 5.0393671298525025, 5.005946854196621, 4.967382629752931, 4.923714083868938, 4.874986088927471, 4.821248716237279, 4.7625571845813734, 4.698971803475995, 4.630557911198517, 4.557385807647937, 4.479530682106988, 4.3970725359800635, 4.310096100586366, 4.218690750092748, 4.122950409675719, 4.022973459006972, 3.918862631161624, 3.810724907053036, 3.6986714055026884, 3.5828172690580895, 3.4632815456760153, 3.34018706639269, 3.2136603191065958, 3.083831318603603, 2.9508334729579917, 2.814803446446631, 2.6758810191172078, 2.5342089431547645, 2.3899327961941923, 2.243200831729361, 2.0941638267726375, 1.9429749269213126, 1.7897894889901427, 1.6347649213717292, 1.4780605222887457, 1.3198373161042536, 1.1602578878582768, 0.9994862162006882], [5.159599895033378, 5.188589709704811, 5.212247897707996, 5.230550148655498, 5.243477655747263, 5.2510171350958705, 5.253160839376633, 5.249906565788492, 5.24125765831754, 5.22722300430086, 5.207817025294178, 5.18305966225274, 5.152976355040633, 5.117598016289611, 5.076960999634265, 5.031107062356216, 4.9800833224756795, 4.923942210334518, 4.86274141472052, 4.796543823588266, 4.7254174594375105, 4.649435409415464, 4.568675750214806, 4.483221467844607, 4.393160372356594, 4.298585007614388, 4.199592556198425, 4.096284739544289, 3.9887677134170567, 3.8771519588290797, 3.761552168513267, 3.6420871290685555, 3.5188795988986477, 3.39205618206945, 3.261747198214845, 3.1280865486244513, 2.991211578650999, 2.8512629365786943, 2.7083844290976042, 2.562722873532554, 2.4144279469784093, 2.2636520324967355, 2.1105500625319085, 1.9552793597075502, 1.7979994751668966, 1.6388720246232191, 1.4780605222887457, 1.3157302128527641, 1.1520479016815228, 0.9871817834144506], [5.284527586631032, 5.312539299027059, 5.335092018172989, 5.3521625696253645, 5.363733412238624, 5.369792656189809, 5.370334075196162, 5.365357112913056, 5.354866883505672, 5.33887416639385, 5.317395395175512, 5.290452640740018, 5.258073588588842, 5.220291510386851, 5.177145229773412, 5.128679082468486, 5.074942870714674, 5.015991812102046, 4.951886482828337, 4.882692755452809, 4.80848173120774, 4.7293296669371045, 4.645317896737512, 4.556532748381923, 4.463065454612027, 4.365012059390432, 4.262473319209004, 4.155554599554756, 4.0443657666396895, 3.9290210745058403, 3.8096390476215167, 3.686342359089404, 3.559257704591655, 3.428515672201513, 3.294250608195242, 3.1566004790022406, 3.015706729435216, 2.871714137346069, 2.7247706648568757, 2.5750273063187916, 2.4226379331551633, 2.2677591357482254, 2.1105500625319085, 1.9511722564560605, 1.789789488990143, 1.6265675918369813, 1.461674286529475, 1.2952790120853894, 1.1275527508973062, 0.9586678530366611], [5.404783343122393, 5.431314820120996, 5.4522652539925165, 5.467613116749928, 5.477342637426755, 5.4814438182827985, 5.479912445077495, 5.472750091400334, 5.45996411705388, 5.44156766049109, 5.4175796253146595, 5.388024660852288, 5.3529331368278354, 5.312341112154377, 5.26629029788123, 5.21482801433303, 5.158007142484903, 5.0958860696236865, 5.028528629351044, 4.956004035990126, 4.878386813463173, 4.7957567187131485, 4.708198659748091, 4.61580260839239, 4.51866350783466, 4.416881175067193, 4.310560198317253, 4.199809829575603, 4.084743872332697, 3.9654805646379034, 3.8421424576019136, 3.7148562894671935, 3.583752855375872, 3.448966872968888, 3.310636843954513, 3.1689049117884784, 3.02391671561197, 2.875821240597559, 2.7247706648568757, 2.570920203067302, 2.4144279469784093, 2.2554547029619876, 2.094163826772638, 1.9307210556886862, 1.7652943382059263, 1.598053661459192, 1.4291708765490787, 1.2588195219533265, 1.0871746452042987, 0.9144126230158133], [5.518392568310524, 5.542965982213987, 5.561843623873851, 5.575006095237207, 5.582439870974964, 5.584137312380038, 5.580096675216643, 5.5703221115126045, 5.554823665292874, 5.533617262258617, 5.506724693422477, 5.474173592716832, 5.435997408598065, 5.392235369676018, 5.342932444403936, 5.288139294870346, 5.2279122247403365, 5.16231312139973, 5.091409392361623, 5.0152738960005925, 4.9339848666858055, 4.847625834389909, 4.756285538856341, 4.6600578384132385, 4.5590416135276675, 4.453340665199256, 4.3430636082976495, 4.228323759953393, 4.109239023116913, 3.985931765405278, 3.8585286933611846, 3.7271607222534313, 3.591962841552626, 3.4530739762203773, 3.310636843954513, 3.164797808536989, 3.015706729435216, 2.8635168078113216, 2.7083844290976047, 2.5504690022999275, 2.389932796194193, 2.2269407725841983, 2.061660416792241, 1.894261565556623, 1.7249162325129186, 1.5537984314383442, 1.3810839974408287, 1.2069504062765666, 1.0315765919816662, 0.8551427630053469], [5.623489801858733, 5.645659476311227, 5.662027854012998, 5.672578115349477, 5.677299419213958, 5.676186914147566, 5.669241743324461, 5.656471043377148, 5.637887937063104, 5.613511519780258, 5.5833668399451835, 5.547484873254148, 5.505902490853498, 5.458662421452063, 5.405813207414515, 5.347409154880813, 5.283510277962969, 5.214182237076491, 5.139496271469872, 5.05952912602144, 4.974362972378813, 4.884085324521973, 4.7887889488367374, 4.688571768791028, 4.5835367643118845, 4.47379186596663, 4.359449844056921, 4.2406281927396305, 4.117449009293668, 3.990038868656768, 3.8585286933611846, 3.723053619001942, 3.583752855375872, 3.44076954343414, 3.294250608195242, 3.1443466077696143, 2.9912115786509994, 2.835002877433532, 2.6758810191172078, 2.5140095121678647, 2.349554690501185, 2.18268554256335, 2.0135735376839916, 1.8423924498798625, 1.6693181792902863, 1.4945285714278778, 1.3182032344302503, 1.1405233545005218, 0.9616715097262334, 0.7818314824680302], [5.718349350097727, 5.737709078078754, 5.751172922120816, 5.758727047214021, 5.760363690984187, 5.756081171669206, 5.745883889847167, 5.729782323914464, 5.707793019318537, 5.679938571556302, 5.6462476029557624, 5.606754733264615, 5.5615005440761305, 5.510531537128823, 5.453900086522765, 5.39166438490166, 5.3238883836559765, 5.250641727208555, 5.171999681450269, 5.08804305639923, 4.99885812316303, 4.904536525289347, 4.805175184596008, 4.700876201577266, 4.591746750488639, 4.477898969218121, 4.359449844056921, 4.236521089488141, 4.109239023116914, 3.97773443587053, 3.8421424576019136, 3.7026024182345676, 3.559257704591656, 3.4122556130563506, 3.2617471982148456, 3.1078871176375515, 2.950833472957992, 2.790747647412684, 2.627794140008959, 2.4621403964911046, 2.293956637278553, 2.123415682552884, 1.950692774673413, 1.7759653981038188, 1.599413097034854, 1.4212172908905618, 1.2415610879075447, 1.0606290969788819, 0.8786072379560047, 0.6956825506034873], [5.801413621867956, 5.817603335600395, 5.827815068643522, 5.832038327751337, 5.83026877323962, 5.822508223445251, 5.808764652857746, 5.789052183924931, 5.763391072541169, 5.731807687233062, 5.694334482064011, 5.651009963285462, 5.601878649769138, 5.546991027260886, 5.486403496503161, 5.4201783152794505, 5.3483835344401935, 5.271092927975929, 5.188385917209541, 5.100347489185467, 5.007068109339784, 4.908643628540837, 4.805175184596008, 4.696769098325776, 4.5835367643118845, 4.465594536431882, 4.3430636082976495, 4.216069888720766, 4.084743872332697, 3.9492205054927405, 3.809639047621517, 3.6661429281025044, 3.5188795988986477, 3.3680003830355023, 3.213660319106596, 3.056018001960791, 2.89523541973536, 2.7314777874022176, 2.5649133769983803, 2.39571334471506, 2.2240515550231206, 2.0501044020155677, 1.8740506281507068, 1.6960711405821782, 1.5163488252646247, 1.335068359026018, 1.1524160197997262, 0.9685794952113551, 0.7837476897170104, 0.5981105304912167], [5.871318704123389, 5.884030387376439, 5.890695831654101, 5.891308187761803, 5.8858668264622525, 5.87437733912201, 5.8568515319659955, 5.833307413945779, 5.803769178234177, 5.768267177365126, 5.726837892044409, 5.679523893663252, 5.626373800553354, 5.567442228028261, 5.502789732262432, 5.432482748065688, 5.356593520616947, 5.275200031227419, 5.188385917209541, 5.096240385933978, 4.99885812316303, 4.896339195754599, 4.7887889488367374, 4.676317897558402, 4.559041613527668, 4.437080606054093, 4.310560198317253, 4.179610398588704, 4.0443657666396895, 3.904965275471893, 3.761552168513268, 3.6142738124257443, 3.4632815456760158, 3.3087305230250363, 3.1507795560960177, 2.989590950184747, 2.8253303374799272, 2.6581665068649016, 2.4882712304756742, 2.31581908719342, 2.1409872832528922, 1.9639554701510245, 1.7849055600428896, 1.6040215388146515, 1.421489277025631, 1.237496338913748, 1.0522317896605795, 0.8658860011141158, 0.6786504561688024, 0.490717552003939], [5.926916757346022, 5.935899503053199, 5.93878271076235, 5.935563417782651, 5.92624493215526, 5.910836829254074, 5.889354941946392, 5.861821344323569, 5.828264329018394, 5.788718378132501, 5.74322412780368, 5.69182832644949, 5.634583786730109, 5.57154933127975, 5.502789732262432, 5.428375644814198, 5.3483835344401935, 5.262895598441181, 5.171999681450269, 5.075789185166603, 4.974362972378813, 4.86782526537681, 4.756285538856341, 4.639858407426338, 4.518663507834661, 4.392825376033246, 4.262473319209004, 4.127741282911943, 3.988767713417057, 3.8456954154614262, 3.6986714055026892, 3.5478467606497, 3.393376463420583, 3.2354192424877195, 3.0741374095733116, 2.9096966926631067, 2.742266065709698, 2.572017575000358, 2.399126162367857, 2.223769485425893, 2.046127735013897, 1.8663834500387537, 1.6847213299037422, 1.5013280447174115, 1.3163920434774223, 1.1301033604264699, 0.9426534197792455, 0.7542348390211242, 0.5650412309806709, 0.375267004879375], [5.9672948630390295, 5.972358993185263, 5.9712861207427474, 5.964077348160441, 5.950740082939477, 5.931288030021449, 5.9057411777056625, 5.874125777109806, 5.836474315195147, 5.79282548138399, 5.74322412780368, 5.687721223198, 5.626373800553355, 5.559244898493513, 5.486403496503161, 5.407924444046824, 5.3238883836559765, 5.234381668063392, 5.139496271469873, 5.0393296950345405, 4.9339848666858055, 4.823570035355962, 4.708198659748092, 4.587989291749579, 4.463065454612028, 4.33355551602278, 4.199592556198426, 4.061314231135899, 3.918862631161625, 3.7723841349241107, 3.6220292589799836, 3.46795250312806, 3.310312191650355, 3.1492703106231765, 2.984992341465494, 2.81764709089558, 2.6474065174707047, 2.474445554888088, 2.29894193222871, 2.121075991328654, 1.941030501465689, 1.7589904715514761, 1.5751429600224083, 1.3896768826244217, 1.2027828182892917, 1.0146528133019066, 0.8254801839597186, 0.6354593179271872, 0.44478547448931, 0.25365458390950874], [5.9917900138232465, 5.9928101939526375, 5.987672356502019, 5.976381780946679, 5.958950069116231, 5.935395133272938, 5.9057411777056625, 5.870018673858317, 5.828264329018394, 5.780521048597753, 5.726837892044409, 5.667270022430626, 5.601878649769138, 5.530730968115724, 5.453900086522765, 5.371464953914761, 5.283510277962969, 5.190126438042544, 5.091409392361623, 4.98746057935778, 4.878386813463173, 4.764300175345496, 4.645317896737513, 4.521562239973535, 4.393160372356595, 4.260244235485462, 4.1229504096757195, 3.981419973614259, 3.835798359391396, 3.686235203059567, 3.5328841908721658, 3.375902901360533, 3.2154526434113597, 3.051698290510906, 2.884808111326347, 2.71495359679834, 2.5423092839224957, 2.36705257640081, 2.1893635623473755, 2.0094248292356625, 1.8274212762775583, 1.6435399244269122, 1.4579697242028804, 1.2709013615304838, 1.08252706179793, 0.8930403923320396, 0.7026360634947241, 0.5115097286049395, 0.31985778289165645, 0.127877161684507], [6.0, 5.996917297204127, 5.987672356502019, 5.972274677695189, 5.950740082939477, 5.923090700486701, 5.889354941946392, 5.849567473090942, 5.803769178234177, 5.7520071182199635, 5.694334482064012, 5.630810532298563, 5.5615005440761305, 5.486475738094875, 5.405813207414515, 5.319595838238, 5.2279122247403365, 5.130856578032078, 5.028528629351045, 4.921033527581736, 4.80848173120774, 4.690988894808179, 4.5686757502148065, 4.441667982451894, 4.3100961005863665, 4.17409530362092, 4.033805341567901, 3.8893703718467316, 3.7409388111524016, 3.5886631829472964, 3.4326999607330184, 3.273209407263293, 3.1103554098631516, 2.9443053120236273, 2.775229741445012, 2.6033024347053493, 2.428700058734364, 2.2516020292762455, 2.0721903265278474, 1.8906493081417253, 1.7071655197861957, 1.5219275034570452, 1.335125603737887, 1.1469517722082352, 0.9575993702002764, 0.7672629701070378, 0.5761381554460919, 0.38442131988427886, 0.19230946542993202, 6.123233995736766e-16]], "colorscale": "Reds", "showscale": false, "opacity": 0.7}], {"scene": {"xaxis": {"title": "Trans (mm)"}, "yaxis": {"title": "Yaw (mm)"}, "zaxis": {"title": "Pitch (mm)"}}}, {"showLink": true, "linkText": "Export to plot.ly"})});</script>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>This concludes our post. To summarize, we symbolically derived the kinematics of the 2-link manipulator and plotted visualized it's workspace.</p>
<p>In the next post, we will learn how to achieve the same results without using DH parameters. We will use Sympy to derive the kinematics and will show that the obtained results by both method are mathematically identical.</p>

</div>
</div>
</div>
    </div>
  </div>
</body>

 


</html>
