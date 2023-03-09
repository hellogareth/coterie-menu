<template>
  <div id="dynamicMenu">
    <PDFViewer/>
  </div>
</template>

<script>

import PDFViewer from './components/PDFViewer.vue';

export default {
  name: 'App',
  components: {
    PDFViewer
  }
}
</script>

<style>
/*
	Theme Name: Coterie
	Author: gareth.work
	Author URI: https://gareth.work/
	Version: 1.0.0
*/
@import url("https://fonts.googleapis.com/css2?family=Libre+Baskerville:ital@0;1&family=Montserrat:wght@300;600&display=swap");
.visually-hidden:not(:focus):not(:active) {
  clip: rect(0 0 0 0);
  clip-path: inset(50%);
  height: 1px;
  overflow: hidden;
  position: absolute;
  white-space: nowrap;
  width: 1px;
}

.wpcf7-list-item {
  margin: 1rem 0;
}

@media (prefers-reduced-motion: reduce) {
  *, ::before, ::after {
    animation-delay: -1ms !important;
    animation-duration: 1ms !important;
    animation-iteration-count: 1 !important;
    background-attachment: initial !important;
    scroll-behavior: auto !important;
    transition-duration: 0s !important;
    transition-delay: 0s !important;
  }
}
@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
.reveal {
  visibility: hidden;
  position: relative;
  overflow: hidden;
  width: 50%;
  padding-bottom: 50%;
}
.reveal:before {
  content: "";
  background-color: #d8c5a2;
  height: 100%;
  width: 50%;
  left: -4rem;
  top: -4rem;
}

.reveal img,
.reveal video {
  position: absolute;
  height: 100%;
  width: 100%;
  object-fit: cover;
  transform-origin: left;
}

html {
  margin: 0;
}

* *:before,
*:after,
body {
  box-sizing: border-box;
}

::selection {
  background: lightblue;
  color: white;
}

body {
  background-color: white;
  color: #678693;
  font-size: 20px;
  font-weight: 300;
  line-height: 1.65;
  padding: 0;
  margin: 0;
  min-width: 320px;
  font-family: "Montserrat", sans-serif;
  font-size: max(1rem, min(0.9545rem + 0.2273vw, 1.5rem));
}

::-webkit-scrollbar {
  width: 0.2rem;
}

/* Track */
::-webkit-scrollbar-track {
  background: white;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: #7dafa7;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #e8aa9e;
}

.siteHero {
  position: relative;
  max-width: 70rem;
  margin: 0 auto;
}

h1, h2, h3, h4, h5, h6 {
  font-family: "Libra Baskerville", serif;
  line-height: 1;
  font-weight: 400;
  color: #8a6892;
}

h1 {
  /* https://codesandbox.io/s/clamp-linear-intepolation-based-on-viewport-width-builder-xgkft?from-embed */
  font-size: max(5rem, min(4rem + 4vw, 25rem));
  margin: 2rem auto;
  text-align: center;
  max-width: 60rem;
  /* 320 / 3840 / 5 / 16 / 16 */
}

a {
  text-decoration: none;
  color: black;
  font-weight: 600;
}

a:hover {
  text-decoration: underline;
}

.siteHeader-wrapper {
  background-color: rgba(255, 255, 255, 0.975);
  position: sticky;
  top: 0;
  z-index: 1;
  opacity: 1;
}

.siteHeader {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1rem;
}
@media (min-width: 1080px) {
  .siteHeader {
    padding: 2rem;
  }
}

.siteHeader-logo {
  display: block;
  width: 12.5vw;
  min-width: 8rem;
  margin: 0 auto;
}

.secondaryNav-is-active .siteHeader-wrapper {
  transition-delay: 1s;
  z-index: 2;
  background-color: transparent;
  pointer-events: none;
}
.secondaryNav-is-active .siteHeader-wrapper #call-restaurant,
.secondaryNav-is-active .siteHeader-wrapper .siteMasthead,
.secondaryNav-is-active .siteHeader-wrapper .siteHeader-logo-link,
.secondaryNav-is-active .siteHeader-wrapper .siteNav {
  opacity: 0;
}
.secondaryNav-is-active .siteHeader-wrapper svg path {
  fill: white;
}
.secondaryNav-is-active .siteHeader-wrapper #toggle-secondary-nav {
  pointer-events: all;
}
.secondaryNav-is-active .siteHeader-wrapper #call-restaurant,
.secondaryNav-is-active .siteHeader-wrapper .siteMasthead,
.secondaryNav-is-active .siteHeader-wrapper .siteHeader-logo-link,
.secondaryNav-is-active .siteHeader-wrapper .siteNav,
.secondaryNav-is-active .siteHeader-wrapper svg path {
  transition-delay: 1s;
}

.inline-input-fields {
  display: flex;
}
.inline-input-fields label + label {
  margin-left: 2rem;
}

label {
  font-weight: 600;
  color: #8a6892;
  margin: 1rem 0;
}

label .wpcf7-form-control-wrap {
  display: block;
}

input[type=text],
input[type=email],
input[type=password],
input[type=search],
input[type=url],
input[type=tel],
input[type=number],
input[type=date],
select,
textarea {
  appearance: none !important;
  -webkit-appearance: none !important;
  all: unset;
  border: 1px solid #678693;
  padding: 0.5rem;
  box-shadow: inset 0 -2px 5px #eee;
}
input[type=text]:focus,
input[type=email]:focus,
input[type=password]:focus,
input[type=search]:focus,
input[type=url]:focus,
input[type=tel]:focus,
input[type=number]:focus,
input[type=date]:focus,
select:focus,
textarea:focus {
  outline: 1px solid purple;
}
input[type=text]:invalid,
input[type=email]:invalid,
input[type=password]:invalid,
input[type=search]:invalid,
input[type=url]:invalid,
input[type=tel]:invalid,
input[type=number]:invalid,
input[type=date]:invalid,
select:invalid,
textarea:invalid {
  outline: 1px solid red;
}
input[type=text]:disabled,
input[type=email]:disabled,
input[type=password]:disabled,
input[type=search]:disabled,
input[type=url]:disabled,
input[type=tel]:disabled,
input[type=number]:disabled,
input[type=date]:disabled,
select:disabled,
textarea:disabled {
  opacity: 0.5;
}

.select-wrapper {
  position: relative;
}

.siteMasthead {
  background-color: #f2e5dd;
  padding: 0.5rem;
  font-size: smaller;
  text-align: center;
}

.siteMasthead-button {
  display: flex;
  align-items: flex-start;
  justify-content: center;
  margin: 0 auto;
  font-weight: 300;
}

.siteMasthead p {
  margin: 0 0.5rem;
  color: black;
}

.siteNav {
  border-top: 1px solid;
  border-bottom: 1px solid;
  border-color: #f2e5dd;
}

.siteNav-list {
  display: flex;
  justify-content: center;
  list-style-type: none;
  padding: 0;
  margin: 0;
}

.siteNav-list li {
  position: relative;
  border-left: 1px solid #f2e5dd;
}

.siteNav-list li:last-child {
  border-right: 1px solid #f2e5dd;
}

.siteNav-list li button,
.siteNav-list li a,
.externalNav-list li a {
  color: black;
  display: block;
  padding: 1rem;
  text-transform: uppercase;
  font-weight: 300;
  letter-spacing: 0.15rem;
  font-size: smaller;
}
@media (min-width: 1080px) {
  .siteNav-list li button,
  .siteNav-list li a,
  .externalNav-list li a {
    padding: 2rem;
  }
}

.toggle-menu-nav,
#toggle-external-nav {
  position: relative;
}
.toggle-menu-nav:after,
#toggle-external-nav:after {
  content: "";
  pointer-events: none;
  position: absolute;
  right: 1rem;
  top: 50%;
  transform: translateY(-50%);
  background-position: center;
  background-size: 1rem;
  width: 1rem;
  height: 1rem;
  transform-origin: center 25%;
  margin-left: 1rem;
}

#toggle-external-nav {
  background-color: rgba(255, 255, 255, 0.975);
  border: 2px double;
  width: 2.5rem;
  height: 2.5rem;
}
#toggle-external-nav:after {
  left: 50%;
  transform: translate(-50%, -50%);
  transform-origin: center;
  width: 1.5rem;
  height: 1.5rem;
  background-size: 1.5rem;
  margin-left: 0;
}

.toggle-menu-nav {
  padding-right: 1rem;
}
@media (min-width: 1080px) {
  .toggle-menu-nav {
    padding-right: 0.5rem;
  }
}

.toggle-menu-nav.is-active:after {
  transform: rotate(180deg);
}

.externalNav.is-active #toggle-external-nav {
  transform: rotate(180deg);
}

.siteNav .sub-menu,
.externalNav-list {
  display: none;
  background-color: white;
  position: absolute;
  left: 50%;
  border: 1px solid;
  list-style-type: none;
  padding: 0;
  margin: 0;
  text-align: center;
  min-width: 15rem;
  transform: translateX(-50%);
}

.externalNav {
  position: fixed;
  z-index: 2;
  right: 2rem;
  top: 2rem;
}

.externalNav-list {
  transform: none;
  right: 0;
  left: auto;
}

.siteNav .sub-menu li + li,
.externalNav-list li + li {
  border-top: 1px solid;
}

.siteNav .sub-menu li a,
.externalNav-list li a {
  display: block;
  padding: 0.5rem;
}

.siteNav li.is-active > .sub-menu,
.externalNav.is-active .externalNav-list {
  display: block;
}

.secondaryNav-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #7dafa7;
  position: fixed;
  bottom: 0;
  width: 100%;
  height: 0;
  z-index: 1;
  transition: 1s;
  overflow: hidden;
  transform-origin: bottom;
}

.secondaryNav-is-active {
  overflow: hidden;
}

.secondaryNav-is-active .secondaryNav-wrapper {
  height: 100%;
}

.secondaryNav-wrapper:before {
  content: "";
  pointer-events: none;
  position: fixed;
  height: 100%;
  width: 100%;
  background-size: 33.3%;
  background-repeat: no-repeat;
  background-position: center;
  mix-blend-mode: color-burn;
  opacity: 0;
  transition: 1s;
}

.secondaryNav-is-active .secondaryNav-wrapper:before {
  opacity: 1;
  transition-delay: 1s;
}

.secondaryNav-list {
  text-align: center;
  list-style-type: none;
  margin: 0;
  padding: 0;
}

.secondaryNav-list li + li {
  margin-top: 1rem;
}

.secondaryNav-list li a {
  color: white;
  text-transform: uppercase;
  letter-spacing: 0.15rem;
  font-weight: 300;
  font-size: 1.5rem;
}
@media (min-width: 1080px) {
  .secondaryNav-list li a {
    font-size: 2rem;
  }
}



.dynamicMenu-nav {
  position: fixed;
  z-index: 1;
  background-color: rgba(103, 134, 147, 0.975);
  border: 0.1rem solid #678693;
  top: 2rem;
  left: 50%;
  transform: translate(-50%);
  border-radius: 2rem;
  overflow: hidden;
}

.dynamicMenu-nav-list {
  display: flex;
  list-style-type: none;
  padding: 0;
  margin: 0;
}

.dynamicMenu-nav-list li {
  white-space: nowrap;
}

.dynamicMenu-nav-list li button {
  color: white;
  padding: 0.5rem 1rem;
  font-weight: 600;
  font-size: small;
}

.dynamicMenu-nav-list li button.is-active,
.dynamicMenu-nav-list li button:hover {
  background-color: white;
  color: #678693;
}

#dynamicMenu canvas {
  height: 100%!important;
  width: 100%!important;
}


</style>