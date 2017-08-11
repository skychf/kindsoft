<template>
  <div class="kindeditor">
    <textarea :id="id">{{ outContent }}</textarea>
  </div>
</template>

<style type="text/css">
/* common */
.ke-inline-block {
  display: -moz-inline-stack;
  display: inline-block;
  vertical-align: middle;
  zoom: 1;
  *display: inline;
}
.ke-clearfix {
  zoom: 1;
}
.ke-clearfix:after {
  content: ".";
  display: block;
  clear: both;
  font-size: 0;
  height: 0;
  line-height: 0;
  visibility: hidden;
}
.ke-shadow {
  box-shadow: 1px 1px 3px #A0A0A0;
  -moz-box-shadow: 1px 1px 3px #A0A0A0;
  -webkit-box-shadow: 1px 1px 3px #A0A0A0;
  filter: progid:DXImageTransform.Microsoft.Shadow(color='#A0A0A0', Direction=135, Strength=3);
  background-color: #F0F0EE;
}
.ke-menu a,
.ke-menu a:hover,
.ke-dialog a,
.ke-dialog a:hover {
  color: #337FE5;
  text-decoration: none;
}
/* icons */
.ke-icon-source {
  background-position: 0px 0px;
  width: 16px;
  height: 16px;
}
.ke-icon-preview {
  background-position: 0px -16px;
  width: 16px;
  height: 16px;
}
.ke-icon-print {
  background-position: 0px -32px;
  width: 16px;
  height: 16px;
}
.ke-icon-undo {
  background-position: 0px -48px;
  width: 16px;
  height: 16px;
}
.ke-icon-redo {
  background-position: 0px -64px;
  width: 16px;
  height: 16px;
}
.ke-icon-cut {
  background-position: 0px -80px;
  width: 16px;
  height: 16px;
}
.ke-icon-copy {
  background-position: 0px -96px;
  width: 16px;
  height: 16px;
}
.ke-icon-paste {
  background-position: 0px -112px;
  width: 16px;
  height: 16px;
}
.ke-icon-selectall {
  background-position: 0px -128px;
  width: 16px;
  height: 16px;
}
.ke-icon-justifyleft {
  background-position: 0px -144px;
  width: 16px;
  height: 16px;
}
.ke-icon-justifycenter {
  background-position: 0px -160px;
  width: 16px;
  height: 16px;
}
.ke-icon-justifyright {
  background-position: 0px -176px;
  width: 16px;
  height: 16px;
}
.ke-icon-justifyfull {
  background-position: 0px -192px;
  width: 16px;
  height: 16px;
}
.ke-icon-insertorderedlist {
  background-position: 0px -208px;
  width: 16px;
  height: 16px;
}
.ke-icon-insertunorderedlist {
  background-position: 0px -224px;
  width: 16px;
  height: 16px;
}
.ke-icon-indent {
  background-position: 0px -240px;
  width: 16px;
  height: 16px;
}
.ke-icon-outdent {
  background-position: 0px -256px;
  width: 16px;
  height: 16px;
}
.ke-icon-subscript {
  background-position: 0px -272px;
  width: 16px;
  height: 16px;
}
.ke-icon-superscript {
  background-position: 0px -288px;
  width: 16px;
  height: 16px;
}
.ke-icon-date {
  background-position: 0px -304px;
  width: 25px;
  height: 16px;
}
.ke-icon-time {
  background-position: 0px -320px;
  width: 25px;
  height: 16px;
}
.ke-icon-formatblock {
  background-position: 0px -336px;
  width: 25px;
  height: 16px;
}
.ke-icon-fontname {
  background-position: 0px -352px;
  width: 21px;
  height: 16px;
}
.ke-icon-fontsize {
  background-position: 0px -368px;
  width: 23px;
  height: 16px;
}
.ke-icon-forecolor {
  background-position: 0px -384px;
  width: 20px;
  height: 16px;
}
.ke-icon-hilitecolor {
  background-position: 0px -400px;
  width: 23px;
  height: 16px;
}
.ke-icon-bold {
  background-position: 0px -416px;
  width: 16px;
  height: 16px;
}
.ke-icon-italic {
  background-position: 0px -432px;
  width: 16px;
  height: 16px;
}
.ke-icon-underline {
  background-position: 0px -448px;
  width: 16px;
  height: 16px;
}
.ke-icon-strikethrough {
  background-position: 0px -464px;
  width: 16px;
  height: 16px;
}
.ke-icon-removeformat {
  background-position: 0px -480px;
  width: 16px;
  height: 16px;
}
.ke-icon-image {
  background-position: 0px -496px;
  width: 16px;
  height: 16px;
}
.ke-icon-flash {
  background-position: 0px -512px;
  width: 16px;
  height: 16px;
}
.ke-icon-media {
  background-position: 0px -528px;
  width: 16px;
  height: 16px;
}
.ke-icon-div {
  background-position: 0px -544px;
  width: 16px;
  height: 16px;
}
.ke-icon-formula {
  background-position: 0px -576px;
  width: 16px;
  height: 16px;
}
.ke-icon-hr {
  background-position: 0px -592px;
  width: 16px;
  height: 16px;
}
.ke-icon-emoticons {
  background-position: 0px -608px;
  width: 16px;
  height: 16px;
}
.ke-icon-link {
  background-position: 0px -624px;
  width: 16px;
  height: 16px;
}
.ke-icon-unlink {
  background-position: 0px -640px;
  width: 16px;
  height: 16px;
}
.ke-icon-fullscreen {
  background-position: 0px -656px;
  width: 16px;
  height: 16px;
}
.ke-icon-about {
  background-position: 0px -672px;
  width: 16px;
  height: 16px;
}
.ke-icon-plainpaste {
  background-position: 0px -704px;
  width: 16px;
  height: 16px;
}
.ke-icon-wordpaste {
  background-position: 0px -720px;
  width: 16px;
  height: 16px;
}
.ke-icon-table {
  background-position: 0px -784px;
  width: 16px;
  height: 16px;
}
.ke-icon-tablemenu {
  background-position: 0px -768px;
  width: 16px;
  height: 16px;
}
.ke-icon-tableinsert {
  background-position: 0px -784px;
  width: 16px;
  height: 16px;
}
.ke-icon-tabledelete {
  background-position: 0px -800px;
  width: 16px;
  height: 16px;
}
.ke-icon-tablecolinsertleft {
  background-position: 0px -816px;
  width: 16px;
  height: 16px;
}
.ke-icon-tablecolinsertright {
  background-position: 0px -832px;
  width: 16px;
  height: 16px;
}
.ke-icon-tablerowinsertabove {
  background-position: 0px -848px;
  width: 16px;
  height: 16px;
}
.ke-icon-tablerowinsertbelow {
  background-position: 0px -864px;
  width: 16px;
  height: 16px;
}
.ke-icon-tablecoldelete {
  background-position: 0px -880px;
  width: 16px;
  height: 16px;
}
.ke-icon-tablerowdelete {
  background-position: 0px -896px;
  width: 16px;
  height: 16px;
}
.ke-icon-tablecellprop {
  background-position: 0px -912px;
  width: 16px;
  height: 16px;
}
.ke-icon-tableprop {
  background-position: 0px -928px;
  width: 16px;
  height: 16px;
}
.ke-icon-checked {
  background-position: 0px -944px;
  width: 16px;
  height: 16px;
}
.ke-icon-code {
  background-position: 0px -960px;
  width: 16px;
  height: 16px;
}
.ke-icon-map {
  background-position: 0px -976px;
  width: 16px;
  height: 16px;
}
.ke-icon-baidumap {
  background-position: 0px -976px;
  width: 16px;
  height: 16px;
}
.ke-icon-lineheight {
  background-position: 0px -992px;
  width: 16px;
  height: 16px;
}
.ke-icon-clearhtml {
  background-position: 0px -1008px;
  width: 16px;
  height: 16px;
}
.ke-icon-pagebreak {
  background-position: 0px -1024px;
  width: 16px;
  height: 16px;
}
.ke-icon-insertfile {
  background-position: 0px -1040px;
  width: 16px;
  height: 16px;
}
.ke-icon-quickformat {
  background-position: 0px -1056px;
  width: 16px;
  height: 16px;
}
.ke-icon-template {
  background-position: 0px -1072px;
  width: 16px;
  height: 16px;
}
.ke-icon-tablecellsplit {
  background-position: 0px -1088px;
  width: 16px;
  height: 16px;
}
.ke-icon-tablerowmerge {
  background-position: 0px -1104px;
  width: 16px;
  height: 16px;
}
.ke-icon-tablerowsplit {
  background-position: 0px -1120px;
  width: 16px;
  height: 16px;
}
.ke-icon-tablecolmerge {
  background-position: 0px -1136px;
  width: 16px;
  height: 16px;
}
.ke-icon-tablecolsplit {
  background-position: 0px -1152px;
  width: 16px;
  height: 16px;
}
.ke-icon-anchor {
  background-position: 0px -1168px;
  width: 16px;
  height: 16px;
}
.ke-icon-search {
  background-position: 0px -1184px;
  width: 16px;
  height: 16px;
}
.ke-icon-new {
  background-position: 0px -1200px;
  width: 16px;
  height: 16px;
}
.ke-icon-specialchar {
  background-position: 0px -1216px;
  width: 16px;
  height: 16px;
}
.ke-icon-multiimage {
  background-position: 0px -1232px;
  width: 16px;
  height: 16px;
}
/* container */
.ke-container {
  display: block;
  border: 1px solid #CCCCCC;
  background-color: #FFF;
  overflow: hidden;
  margin: 0;
  padding: 0;
}
/* toolbar */
.ke-toolbar {
  border-bottom: 1px solid #CCC;
  background-color: #F0F0EE;
  padding: 2px 5px;
  text-align: left;
  overflow: hidden;
  zoom: 1;
}
.ke-toolbar-icon {
  background-repeat: no-repeat;
  font-size: 0;
  line-height: 0;
  overflow: hidden;
  display: block;
}
.ke-toolbar-icon-url {
  background-image: url(../images/default.png);
}
.ke-toolbar .ke-outline {
  border: 1px solid #F0F0EE;
  margin: 1px;
  padding: 1px 2px;
  font-size: 0;
  line-height: 0;
  overflow: hidden;
  cursor: pointer;
  display: block;
  float: left;
}
.ke-toolbar .ke-on {
  border: 1px solid #5690D2;
}
.ke-toolbar .ke-selected {
  border: 1px solid #5690D2;
  background-color: #E9EFF6;
}
.ke-toolbar .ke-disabled {
  cursor: default;
}
.ke-toolbar .ke-separator {
  height: 16px;
  margin: 2px 3px;
  border-left: 1px solid #A0A0A0;
  border-right: 1px solid #FFFFFF;
  border-top:0;
  border-bottom:0;
  width: 0;
  font-size: 0;
  line-height: 0;
  overflow: hidden;
  display: block;
  float: left;
}
.ke-toolbar .ke-hr {
  overflow: hidden;
  height: 1px;
  clear: both;
}
/* edit */
.ke-edit {
  padding: 0;
}
.ke-edit-iframe,
.ke-edit-textarea {
  border: 0;
  margin: 0;
  padding: 0;
  overflow: auto;
}
.ke-edit-textarea {
  font: 12px/1.5 "Consolas", "Monaco", "Bitstream Vera Sans Mono", "Courier New", Courier, monospace;
  color: #000;
  overflow: auto;
  resize: none;
}
.ke-edit-textarea:focus {
  outline: none;
}
/* statusbar */
.ke-statusbar {
  position: relative;
  background-color: #F0F0EE;
  border-top: 1px solid #CCCCCC;
  font-size: 0;
  line-height: 0;
  *height: 12px;
  overflow: hidden;
  text-align: center;
  cursor: s-resize;
}
.ke-statusbar-center-icon {
  background-position: -0px -754px;
  width: 15px;
  height: 11px;
  background-image: url(../images/default.png);
}
.ke-statusbar-right-icon {
  position: absolute;
  right: 0;
  bottom: 0;
  cursor: se-resize;
  background-position: -5px -741px;
  width: 11px;
  height: 11px;
  background-image: url(../images/default.png);
}
/* menu */
.ke-menu {
  border: 1px solid #A0A0A0;
  background-color: #F1F1F1;
  color: #222222;
  padding: 2px;
  font-family: "sans serif",tahoma,verdana,helvetica;
  font-size: 12px;
  text-align: left;
  overflow: hidden;
}
.ke-menu-item {
  border: 1px solid #F1F1F1;
  background-color: #F1F1F1;
  color: #222222;
  height: 24px;
  overflow: hidden;
  cursor: pointer;
}
.ke-menu-item-on {
  border: 1px solid #5690D2;
  background-color: #E9EFF6;
}
.ke-menu-item-left {
  width: 27px;
  text-align: center;
  overflow: hidden;
}
.ke-menu-item-center {
  width: 0;
  height: 24px;
  border-left: 1px solid #E3E3E3;
  border-right: 1px solid #FFFFFF;
  border-top: 0;
  border-bottom: 0;
}
.ke-menu-item-center-on {
  border-left: 1px solid #E9EFF6;
  border-right: 1px solid #E9EFF6;
}
.ke-menu-item-right {
  border: 0;
  padding: 0 0 0 5px;
  line-height: 24px;
  text-align: left;
  overflow: hidden;
}
.ke-menu-separator {
  margin: 2px 0;
  height: 0;
  overflow: hidden;
  border-top: 1px solid #CCCCCC;
  border-bottom: 1px solid #FFFFFF;
  border-left: 0;
  border-right: 0;
}
/* colorpicker */
.ke-colorpicker {
  border: 1px solid #A0A0A0;
  background-color: #F1F1F1;
  color: #222222;
  padding: 2px;
}
.ke-colorpicker-table {
  border:0;
  margin:0;
  padding:0;
  border-collapse: separate;
}
.ke-colorpicker-cell {
  font-size: 0;
  line-height: 0;
  border: 1px solid #F0F0EE;
  cursor: pointer;
  margin:3px;
  padding:0;
}
.ke-colorpicker-cell-top {
  font-family: "sans serif",tahoma,verdana,helvetica;
  font-size: 12px;
  line-height: 24px;
  border: 1px solid #F0F0EE;
  cursor: pointer;
  margin:0;
  padding:0;
  text-align: center;
}
.ke-colorpicker-cell-on {
  border: 1px solid #5690D2;
}
.ke-colorpicker-cell-selected {
  border: 1px solid #2446AB;
}
.ke-colorpicker-cell-color {
  width: 14px;
  height: 14px;
  margin: 3px;
  padding: 0;
  border: 0;
}
/* dialog */
.ke-dialog {
  position: absolute;
  margin: 0;
  padding: 0;
}
.ke-dialog .ke-header {
  width: 100%;
  margin-bottom: 10px;
}
.ke-dialog .ke-header .ke-left {
  float: left;
}
.ke-dialog .ke-header .ke-right {
  float: right;
}
.ke-dialog .ke-header label {
  margin-right: 0;
  cursor: pointer;
  font-weight: normal;
  display: inline;
  vertical-align: top;
}
.ke-dialog-content {
  background-color: #FFF;
  width: 100%;
  height: 100%;
  color: #333;
  border: 1px solid #A0A0A0;
}
.ke-dialog-shadow {
  position: absolute;
  z-index: -1;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  box-shadow: 3px 3px 7px #999;
  -moz-box-shadow: 3px 3px 7px #999;
  -webkit-box-shadow: 3px 3px 7px #999;
  filter: progid:DXImageTransform.Microsoft.Blur(PixelRadius='3', MakeShadow='true', ShadowOpacity='0.4');
  background-color: #F0F0EE;
}
.ke-dialog-header {
  border:0;
  margin:0;
  padding: 0 10px;
  background: url(../images/background.png) repeat scroll 0 0 #F0F0EE;
  border-bottom: 1px solid #CFCFCF;
  height: 24px;
  font: 12px/24px "sans serif",tahoma,verdana,helvetica;
  text-align: left;
  color: #222;
  cursor: move;
}
.ke-dialog-icon-close {
  display: block;
  background: url(../images/default.png) no-repeat scroll 0px -688px;
  width: 16px;
  height: 16px;
  position: absolute;
  right: 6px;
  top: 6px;
  cursor: pointer;
}
.ke-dialog-body {
  font: 12px/1.5 "sans serif",tahoma,verdana,helvetica;
  text-align: left;
  overflow: hidden;
  width: 100%;
}
.ke-dialog-body textarea {
  display: block;
  overflow: auto;
  padding: 0;
  resize: none;
}
.ke-dialog-body textarea:focus,
.ke-dialog-body input:focus,
.ke-dialog-body select:focus {
  outline: none;
}
.ke-dialog-body label {
  margin-right: 10px;
  cursor: pointer;
  display: -moz-inline-stack;
  display: inline-block;
  vertical-align: middle;
  zoom: 1;
  *display: inline;
}
.ke-dialog-body img {
  display: -moz-inline-stack;
  display: inline-block;
  vertical-align: middle;
  zoom: 1;
  *display: inline;
}
.ke-dialog-body select {
  display: -moz-inline-stack;
  display: inline-block;
  vertical-align: middle;
  zoom: 1;
  *display: inline;
  width: auto;
}
.ke-dialog-body .ke-textarea {
  display: block;
  width: 408px;
  height: 260px;
  font-family: "sans serif",tahoma,verdana,helvetica;
  font-size: 12px;
  border-color: #848484 #E0E0E0 #E0E0E0 #848484;
  border-style: solid;
  border-width: 1px;
}
.ke-dialog-body .ke-form {
  margin: 0;
  padding: 0;
}
.ke-dialog-loading {
  position: absolute;
  top: 0;
  left: 1px;
  z-index: 1;
  text-align: center;
}
.ke-dialog-loading-content {
  background: url("../images/loading.gif") no-repeat;
    color: #666;
    font-size: 14px;
    font-weight: bold;
    height: 31px;
    line-height: 31px;
    padding-left: 36px;
}
.ke-dialog-row {
  margin-bottom: 10px;
}
.ke-dialog-footer {
  font: 12px/1 "sans serif",tahoma,verdana,helvetica;
  text-align: right;
  padding:0 0 5px 0;
  background-color: #FFF;
  width: 100%;
}
.ke-dialog-preview,
.ke-dialog-yes {
  margin: 5px;
}
.ke-dialog-no {
  margin: 5px 10px 5px 5px;
}
.ke-dialog-mask {
  background-color:#FFF;
  filter:alpha(opacity=50);
  opacity:0.5;
}
.ke-button-common {
  background: url(../images/background.png) no-repeat scroll 0 -25px transparent;
  cursor: pointer;
  height: 23px;
  line-height: 23px;
  overflow: visible;
  display: inline-block;
  vertical-align: top;
  cursor: pointer;
}
.ke-button-outer {
  background-position: 0 -25px;
  padding: 0;
  position: relative;
  display: -moz-inline-stack;
  display: inline-block;
  vertical-align: middle;
  zoom: 1;
  *display: inline;
}
.ke-button {
  background-position: right -25px;
  padding: 0 12px;
  margin: 0;
  font-family: "sans serif",tahoma,verdana,helvetica;
  border: 0 none;
  color: #333;
  font-size: 12px;
  left: 2px;
  text-decoration: none;
}
/* inputbox */
.ke-input-text {
  background-color:#FFFFFF;
  font-family: "sans serif",tahoma,verdana,helvetica;
  font-size: 12px;
  line-height: 17px;
  height: 17px;
  padding: 2px 4px;
  border-color: #848484 #E0E0E0 #E0E0E0 #848484;
  border-style: solid;
  border-width: 1px;
  display: -moz-inline-stack;
  display: inline-block;
  vertical-align: middle;
  zoom: 1;
  *display: inline;
}
.ke-input-number {
  width: 50px;
}
.ke-input-color {
  border: 1px solid #A0A0A0;
  background-color: #FFFFFF;
  font-size: 12px;
  width: 60px;
  height: 20px;
  line-height: 20px;
  padding-left: 5px;
  overflow: hidden;
  cursor: pointer;
  display: -moz-inline-stack;
  display: inline-block;
  vertical-align: middle;
  zoom: 1;
  *display: inline;
}
.ke-upload-button {
  position: relative;
}
.ke-upload-area {
  position: relative;
  overflow: hidden;
  margin: 0;
  padding: 0;
  *height: 25px;
}
.ke-upload-area .ke-upload-file {
  position: absolute;
  font-size: 60px;
  top: 0;
  right: 0;
  padding: 0;
  margin: 0;
  z-index: 811212;
  border: 0 none;
  opacity: 0;
  filter: alpha(opacity=0);
}
/* tabs */
.ke-tabs {
  font: 12px/1 "sans serif",tahoma,verdana,helvetica;
  border-bottom:1px solid #A0A0A0;
  padding-left:5px;
  margin-bottom:20px;
}
.ke-tabs-ul  {
  list-style-image:none;
  list-style-position:outside;
  list-style-type:none;
  margin:0;
  padding:0;
}
.ke-tabs-li {
  position: relative;
  border: 1px solid #A0A0A0;
  background-color: #F0F0EE;
  margin: 0 2px -1px 0;
  padding: 0 20px;
  float: left;
  line-height: 25px;
  text-align: center;
  color: #555555;
  cursor: pointer;
}
.ke-tabs-li-selected {
  background-color: #FFF;
  border-bottom: 1px solid #FFF;
  color: #000;
  cursor: default;
}
.ke-tabs-li-on {
  background-color: #FFF;
  color: #000;
}
/* progressbar */
.ke-progressbar {
  position: relative;
  margin: 0;
  padding: 0;
}
.ke-progressbar-bar {
  border: 1px solid #6FA5DB;
  width: 80px;
  height: 5px;
  margin: 10px 10px 0 10px;
  padding: 0;
}
.ke-progressbar-bar-inner {
  width: 0;
  height: 5px;
  background-color: #6FA5DB;
  overflow: hidden;
  margin: 0;
  padding: 0;
}
.ke-progressbar-percent {
  position: absolute;
  top: 0;
  left: 40%;
  display: none;
}
/* swfupload */
.ke-swfupload-top {
  position: relative;
  margin-bottom: 10px;
  _width: 608px;
}
.ke-swfupload-button {
  height: 23px;
  line-height: 23px;
}
.ke-swfupload-desc {
  padding: 0 10px;
  height: 23px;
  line-height: 23px;
}
.ke-swfupload-startupload {
  position: absolute;
  top: 0;
  right: 0;
}
.ke-swfupload-body {
  overflow: scroll;
  background-color:#FFFFFF;
  border-color: #848484 #E0E0E0 #E0E0E0 #848484;
  border-style: solid;
  border-width: 1px;
  width: auto;
  height: 370px;
  padding: 5px;
}
.ke-swfupload-body .ke-item {
  width: 100px;
  margin: 5px;
}
.ke-swfupload-body .ke-photo {
  position: relative;
  border: 1px solid #DDDDDD;
  background-color:#FFFFFF;
  padding: 10px;
}
.ke-swfupload-body .ke-delete {
  display: block;
  background: url(../images/default.png) no-repeat scroll 0px -688px;
  width: 16px;
  height: 16px;
  position: absolute;
  right: 0;
  top: 0;
  cursor: pointer;
}
.ke-swfupload-body .ke-status  {
  position: absolute;
  left: 0;
  bottom: 5px;
  width: 100px;
  height: 17px;
}
.ke-swfupload-body .ke-message  {
  width: 100px;
  text-align: center;
  overflow: hidden;
  height:17px;
}
.ke-swfupload-body .ke-error  {
  color: red;
}
.ke-swfupload-body .ke-name {
  width: 100px;
  text-align: center;
  overflow: hidden;
  height:16px;
}
.ke-swfupload-body .ke-on {
  border: 1px solid #5690D2;
  background-color: #E9EFF6;
}

/* emoticons */
.ke-plugin-emoticons {
  position: relative;
}
.ke-plugin-emoticons .ke-preview {
  position: absolute;
  text-align: center;
  margin: 2px;
  padding: 10px;
  top: 0;
  border: 1px solid #A0A0A0;
  background-color: #FFFFFF;
  display: none;
}
.ke-plugin-emoticons .ke-preview-img {
  border:0;
  margin:0;
  padding:0;
}
.ke-plugin-emoticons .ke-table {
  border:0;
  margin:0;
  padding:0;
  border-collapse:separate;
}
.ke-plugin-emoticons .ke-cell {
  margin:0;
  padding:1px;
  border:1px solid #F0F0EE;
  cursor:pointer;
}
.ke-plugin-emoticons .ke-on {
  border: 1px solid #5690D2;
  background-color: #E9EFF6;
}
.ke-plugin-emoticons .ke-img {
  display:block;
  background-repeat:no-repeat;
  overflow:hidden;
  margin:2px;
  width:24px;
  height:24px;
  margin: 0;
  padding: 0;
  border: 0;
}
.ke-plugin-emoticons .ke-page {
  text-align: right;
  margin: 5px;
  padding: 0;
  border: 0;
  font: 12px/1 "sans serif",tahoma,verdana,helvetica;
  color: #333;
  text-decoration: none;
}
.ke-plugin-plainpaste-textarea,
.ke-plugin-wordpaste-iframe {
  display: block;
  width: 408px;
  height: 260px;
  font-family: "sans serif",tahoma,verdana,helvetica;
  font-size: 12px;
  border-color: #848484 #E0E0E0 #E0E0E0 #848484;
  border-style: solid;
  border-width: 1px;
}
/* filemanager */
.ke-plugin-filemanager-header {
  width: 100%;
  margin-bottom: 10px;
}
.ke-plugin-filemanager-header .ke-left {
  float: left;
}
.ke-plugin-filemanager-header .ke-right {
  float: right;
}
.ke-plugin-filemanager-body {
  overflow: scroll;
  background-color:#FFFFFF;
  border-color: #848484 #E0E0E0 #E0E0E0 #848484;
  border-style: solid;
  border-width: 1px;
  width: auto;
  height: 370px;
  padding: 5px;
}
.ke-plugin-filemanager-body .ke-item {
  width: 100px;
  margin: 5px;
}
.ke-plugin-filemanager-body .ke-photo {
  border: 1px solid #DDDDDD;
  background-color:#FFFFFF;
  padding: 10px;
}
.ke-plugin-filemanager-body .ke-name {
  width: 100px;
  text-align: center;
  overflow: hidden;
  height:16px;
}
.ke-plugin-filemanager-body .ke-on {
  border: 1px solid #5690D2;
  background-color: #E9EFF6;
}
.ke-plugin-filemanager-body .ke-table {
  width: 95%;
  border: 0;
  margin: 0;
  padding: 0;
  border-collapse: separate;
}
.ke-plugin-filemanager-body .ke-table .ke-cell {
  margin: 0;
  padding: 0;
  border: 0;
}
.ke-plugin-filemanager-body .ke-table .ke-name {
  width: 55%;
  text-align: left;
}
.ke-plugin-filemanager-body .ke-table .ke-size {
  width: 15%;
  text-align: left;
}
.ke-plugin-filemanager-body .ke-table .ke-datetime {
  width: 30%;
  text-align: center;
}
</style>

<script>
export default {
  name: 'kindeditor',
  data () {
    return {
      editor: null,
      outContent: this.content
    }
  },
  props: {
    apiurl: {
      type:String,
    },
    content: {
      type: String,
      default: ''
    },
    id: {
      type: String,
      required: true
    },
    width: {
      type: String,
      default: '100%'
    },
    height: {
      type: String,
      default: '500'
    },
    minWidth: {
      type: Number,
      default: 650
    },
    minHeight: {
      type: Number,
      default: 100
    },
    items: {
      type: Array,
      default: function () {
        return [
          'source', '|', 'undo', 'redo', '|', 'preview', 'print', 'template', 'code', 'cut', 'copy', 'paste',
          'plainpaste', 'wordpaste', '|', 'justifyleft', 'justifycenter', 'justifyright',
          'justifyfull', 'insertorderedlist', 'insertunorderedlist', 'indent', 'outdent', 'subscript',
          'superscript', 'clearhtml', 'quickformat', 'selectall', '|', 'fullscreen', '/',
          'formatblock', 'fontname', 'fontsize', '|', 'forecolor', 'hilitecolor', 'bold',
          'italic', 'underline', 'strikethrough', 'lineheight', 'removeformat', '|', 'image', 'multiimage',
          'flash', 'media', 'insertfile', 'table', 'hr', 'emoticons', 'baidumap', 'pagebreak',
          'anchor', 'link', 'unlink', '|', 'about'
        ]
      }
    },
    noDisableItems: {
      type: Array,
      default: function () {
        return ['source', 'fullscreen']
      }
    },
    filterMode: {
      type: Boolean,
      default: true
    },
    htmlTags: {
      type: Object,
      default: function () {
        return {
          font: ['color', 'size', 'face', '.background-color'],
          span: ['style'],
          div: ['class', 'align', 'style'],
          table: ['class', 'border', 'cellspacing', 'cellpadding', 'width', 'height', 'align', 'style'],
          'td,th': ['class', 'align', 'valign', 'width', 'height', 'colspan', 'rowspan', 'bgcolor', 'style'],
          a: ['class', 'href', 'target', 'name', 'style'],
          embed: ['src', 'width', 'height', 'type', 'loop', 'autostart', 'quality',
            'style', 'align', 'allowscriptaccess', '/'],
          img: ['src', 'width', 'height', 'border', 'alt', 'title', 'align', 'style', '/'],
          hr: ['class', '/'],
          br: ['/'],
          'p,ol,ul,li,blockquote,h1,h2,h3,h4,h5,h6': ['align', 'style'],
          'tbody,tr,strong,b,sub,sup,em,i,u,strike': []
        }
      }
    },
    wellFormatMode: {
      type: Boolean,
      default: true
    },
    resizeType: {
      type: Number,
      default: 2
    },
    themeType: {
      type: String,
      default: 'default'
    },
    langType: {
      type: String,
      default: 'zh-CN'
    },
    designMode: {
      type: Boolean,
      default: true
    },
    fullscreenMode: {
      type: Boolean,
      default: false
    },
    basePath: {
      type: String
    },
    themesPath: {
      type: String
    },
    pluginsPath: {
      type: String,
      default: '/static/'
    },
    langPath: {
      type: String
    },
    minChangeSize: {
      type: Number,
      default: 5
    },
    loadStyleMode: {
      type: Boolean,
      default: true
    },
    urlType: {
      type: String,
      default: ''
    },
    newlineTag: {
      type: String,
      default: 'p'
    },
    pasteType: {
      type: Number,
      default: 2
    },
    dialogAlignType: {
      type: String,
      default: 'page'
    },
    shadowMode: {
      type: Boolean,
      default: true
    },
    zIndex: {
      type: Number,
      default: 811213
    },
    useContextmenu: {
      type: Boolean,
      default: true
    },
    syncType: {
      type: String,
      default: 'form'
    },
    indentChar: {
      type: String,
      default: '\t'
    },
    cssPath: {
      type: [ String, Array ]
    },
    cssData: {
      type: String
    },
    bodyClass: {
      type: String,
      default: 'ke-content'
    },
    colorTable: {
      type: Array
    },
    afterCreate: {
      type: Function
    },
    afterChange: {
      type: Function
    },
    afterTab: {
      type: Function
    },
    afterFocus: {
      type: Function
    },
    afterBlur: {
      type: Function
    },
    afterUpload: {
      type: Function
    },
    uploadJson: {
      type: String
    },
    fileManagerJson: {
      type: Function
    },
    allowPreviewEmoticons: {
      type: Boolean,
      default: true
    },
    allowImageUpload: {
      type: Boolean,
      default: true
    },
    allowFlashUpload: {
      type: Boolean,
      default: true
    },
    allowMediaUpload: {
      type: Boolean,
      default: true
    },
    allowFileUpload: {
      type: Boolean,
      default: true
    },
    allowFileManager: {
      type: Boolean,
      default: false
    },
    fontSizeTable: {
      type: Array,
      default: function () {
        return ['9px', '10px', '12px', '14px', '16px', '18px', '24px', '32px']
      }
    },
    imageTabIndex: {
      type: Number,
      default: 0
    },
    formatUploadUrl: {
      type: Boolean,
      default: true
    },
    fullscreenShortcut: {
      type: Boolean,
      default: false
    },
    extraFileUploadParams: {
      type: Array,
      default: function () {
        return []
      }
    },
    filePostName: {
      type: String,
      default: 'imgFile'
    },
    fillDescAfterUploadImage: {
      type: Boolean,
      default: false
    },
    afterSelectFile: {
      type: Function
    },
    pagebreakHtml: {
      type: String,
      default: '<hr style=”page-break-after: always;” class=”ke-pagebreak” />'
    },
    allowImageRemote: {
      type: Boolean,
      default: true
    },
    autoHeightMode: {
      type: Boolean,
      default: false
    },
    fixToolBar: {
      type: Boolean,
      default: false
    },
    tabIndex: {
      type: Number
    }
  },
  watch: {
    content (val) {
      this.editor && val !== this.outContent && this.editor.html(val)
    },
    outContent (val) {
      this.$emit('update:content', val)
      this.$emit('on-content-change', val)
    }
  },
  mounted () {
    var _this = this
    _this.editor = window.KindEditor.create('#' + this.id, {
      apiurl: _this.apiurl,
      width: _this.width,
      height: _this.height,
      minWidth: _this.minWidth,
      minHeight: _this.minHeight,
      items: _this.items,
      noDisableItems: _this.noDisableItems,
      filterMode: _this.filterMode,
      htmlTags: _this.htmlTags,
      wellFormatMode: _this.wellFormatMode,
      resizeType: _this.resizeType,
      themeType: _this.themeType,
      langType: _this.langType,
      designMode: _this.designMode,
      fullscreenMode: _this.fullscreenMode,
      basePath: _this.basePath,
      themesPath: _this.cssPath,
      pluginsPath: _this.pluginsPath,
      langPath: _this.langPath,
      minChangeSize: _this.minChangeSize,
      loadStyleMode: _this.loadStyleMode,
      urlType: _this.urlType,
      newlineTag: _this.newlineTag,
      pasteType: _this.pasteType,
      dialogAlignType: _this.dialogAlignType,
      shadowMode: _this.shadowMode,
      zIndex: _this.zIndex,
      useContextmenu: _this.useContextmenu,
      syncType: _this.syncType,
      indentChar: _this.indentChar,
      cssPath: _this.cssPath,
      cssData: _this.cssData,
      bodyClass: _this.bodyClass,
      colorTable: _this.colorTable,
      afterCreate: _this.afterCreate,
      afterChange: function () {
        _this.afterChange
        _this.outContent = this.html()
      },
      afterTab: _this.afterTab,
      afterFocus: _this.afterFocus,
      afterBlur: _this.afterBlur,
      afterUpload: _this.afterUpload,
      uploadJson: _this.uploadJson,
      fileManagerJson: _this.fileManagerJson,
      allowPreviewEmoticons: _this.allowPreviewEmoticons,
      allowImageUpload: _this.allowImageUpload,
      allowFlashUpload: _this.allowFlashUpload,
      allowMediaUpload: _this.allowMediaUpload,
      allowFileUpload: _this.allowFileUpload,
      allowFileManager: _this.allowFileManager,
      fontSizeTable: _this.fontSizeTable,
      imageTabIndex: _this.imageTabIndex,
      formatUploadUrl: _this.formatUploadUrl,
      fullscreenShortcut: _this.fullscreenShortcut,
      extraFileUploadParams: _this.extraFileUploadParams,
      filePostName: _this.filePostName,
      fillDescAfterUploadImage: _this.fillDescAfterUploadImage,
      afterSelectFile: _this.afterSelectFile,
      pagebreakHtml: _this.pagebreakHtml,
      allowImageRemote: _this.allowImageRemote,
      autoHeightMode: _this.autoHeightMode,
      fixToolBar: _this.fixToolBar,
      tabIndex: _this.tabIndex
    })
  }
}
</script>
