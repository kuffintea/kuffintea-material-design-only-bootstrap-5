<script setup>
    import { ref } from 'vue'

    const showActivePage = ref('home')
    const showThemeMode = ref('light')

    let toggleTheme = () => {
        showThemeMode.value = showThemeMode.value == 'light' ? 'dark' : 'light'
    }
</script>

<template>
    <main :class="['vh-100', showThemeMode=='light' ? 'bg-white' : 'bg-black text-light']">
        <div class="row g-0 h-100">
            <nav :class="['col-auto navbar d-xl-flex flex-column d-none justify-content-between position-fixed h-100', showThemeMode=='dark' ? 'text-bg-dark' : 'bg-body-tertiary']" width="40px">
                <ul class="navbar-nav w-100">
                    <li class="nav-item px-4 py-3">
                        <a :class="['btn rounded-4 py-3 w-100', showThemeMode=='dark' ? 'bg-success text-light' : 'bg-success-subtle']">
                            <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" fill="currentcolor" height="20" width="20" version="1.1" id="Capa_1" viewBox="0 0 488.4 488.4" xml:space="preserve"><g><g><path d="M0,203.25c0,112.1,91.2,203.2,203.2,203.2c51.6,0,98.8-19.4,134.7-51.2l129.5,129.5c2.4,2.4,5.5,3.6,8.7,3.6    s6.3-1.2,8.7-3.6c4.8-4.8,4.8-12.5,0-17.3l-129.6-129.5c31.8-35.9,51.2-83,51.2-134.7c0-112.1-91.2-203.2-203.2-203.2    S0,91.15,0,203.25z M381.9,203.25c0,98.5-80.2,178.7-178.7,178.7s-178.7-80.2-178.7-178.7s80.2-178.7,178.7-178.7S381.9,104.65,381.9,203.25z" /></g></g></svg>
                        </a>
                    </li>
                    <li class="nav-item d-flex flex-column px-2 py-3 position-relative" @click.prevent="showActivePage='home'">
                        <a :class="['nav-link d-flex justify-content-center rounded-pill stretched-link p-0 mx-3', {'active bg-info-subtle' : showActivePage=='home'&&showThemeMode=='light', 'active bg-primary' : showActivePage=='home'&&showThemeMode=='dark', 'text-light' : showThemeMode=='dark'}]" href="/">
                            <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 24 24" fill="none"><path fill-rule="evenodd" clip-rule="evenodd" d="M16 8H8C7.45 8 7.005 8.45 7.005 9L7 15C7 15.55 7.45 16 8 16H16C16.55 16 17 15.55 17 15V9C17 8.45 16.55 8 16 8ZM8.00001 9.99997L12 12.5L16 9.99997V15H8.00001V9.99997ZM8.00001 9.00001L12 11.5L16 9.00001H8.00001Z" fill="currentcolor" /><path fill-rule="evenodd" clip-rule="evenodd" d="M12 22C17.5228 22 22 17.5228 22 12C22 6.47715 17.5228 2 12 2C6.47715 2 2 6.47715 2 12C2 17.5228 6.47715 22 12 22ZM12 20C16.4183 20 20 16.4183 20 12C20 7.58172 16.4183 4 12 4C7.58172 4 4 7.58172 4 12C4 16.4183 7.58172 20 12 20Z" fill="currentcolor" /></svg>
                        </a>
                        <span class="text-center">
                            Home
                        </span>
                    </li>
                    <li class="nav-item d-flex flex-column px-2 py-3 position-relative" @click.prevent="showActivePage='getstarted'">
                        <a :class="['nav-link d-flex justify-content-center rounded-pill stretched-link p-0 mx-3', {'active bg-info-subtle' : showActivePage=='getstarted'&&showThemeMode=='light', 'active bg-primary' : showActivePage=='getstarted'&&showThemeMode=='dark', 'text-light' : showThemeMode=='dark'}]" href="/">
                            <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" fill="currentcolor" version="1.1" id="Capa_1" width="20" height="20" viewBox="0 0 276.167 276.167" xml:space="preserve"><g><g><path d="M33.144,2.471C15.336,2.471,0.85,16.958,0.85,34.765s14.48,32.293,32.294,32.293s32.294-14.486,32.294-32.293    S50.951,2.471,33.144,2.471z" /><path d="M137.663,2.471c-17.807,0-32.294,14.487-32.294,32.294s14.487,32.293,32.294,32.293c17.808,0,32.297-14.486,32.297-32.293    S155.477,2.471,137.663,2.471z" /><path d="M243.873,67.059c17.804,0,32.294-14.486,32.294-32.293S261.689,2.471,243.873,2.471s-32.294,14.487-32.294,32.294    S226.068,67.059,243.873,67.059z" /><path d="M32.3,170.539c17.807,0,32.297-14.483,32.297-32.293c0-17.811-14.49-32.297-32.297-32.297S0,120.436,0,138.246    C0,156.056,14.493,170.539,32.3,170.539z" /><path d="M136.819,170.539c17.804,0,32.294-14.483,32.294-32.293c0-17.811-14.478-32.297-32.294-32.297    c-17.813,0-32.294,14.486-32.294,32.297C104.525,156.056,119.012,170.539,136.819,170.539z" /><path d="M243.038,170.539c17.811,0,32.294-14.483,32.294-32.293c0-17.811-14.483-32.297-32.294-32.297    s-32.306,14.486-32.306,32.297C210.732,156.056,225.222,170.539,243.038,170.539z" /><path d="M33.039,209.108c-17.807,0-32.3,14.483-32.3,32.294c0,17.804,14.493,32.293,32.3,32.293s32.293-14.482,32.293-32.293    S50.846,209.108,33.039,209.108z" /><path d="M137.564,209.108c-17.808,0-32.3,14.483-32.3,32.294c0,17.804,14.487,32.293,32.3,32.293    c17.804,0,32.293-14.482,32.293-32.293S155.368,209.108,137.564,209.108z" /><path d="M243.771,209.108c-17.804,0-32.294,14.483-32.294,32.294c0,17.804,14.49,32.293,32.294,32.293    c17.811,0,32.294-14.482,32.294-32.293S261.575,209.108,243.771,209.108z" /></g></g></svg>
                        </a>
                        <span class="text-center">
                            Get started
                        </span>
                    </li>
                    <li class="nav-item d-flex flex-column px-2 py-3 position-relative" @click.prevent="showActivePage='develop'">
                        <a :class="['nav-link d-flex justify-content-center rounded-pill stretched-link p-0 mx-3', {'active bg-info-subtle' : showActivePage=='develop'&&showThemeMode=='light', 'active bg-primary' : showActivePage=='develop'&&showThemeMode=='dark', 'text-light' : showThemeMode=='dark'}]" href="/">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="currentcolor" width="30" height="30" viewBox="0 0 32 32" version="1.1"><path d="M30 16l-8.485 8.485-2.828-2.828 5.656-5.657-5.657-5.657 2.828-2.828 8.486 8.485zM2 16l8.485-8.485 2.828 2.828-5.656 5.657 5.657 5.657-2.828 2.828-8.486-8.485z" /></svg>
                        </a>
                        <span class="text-center">
                            Develop
                        </span>
                    </li>
                    <li class="nav-item d-flex flex-column px-2 py-3 position-relative" @click.prevent="showActivePage='foundation'">
                        <a :class="['nav-link d-flex justify-content-center rounded-pill stretched-link p-0 mx-3', {'active bg-info-subtle' : showActivePage=='foundation'&&showThemeMode=='light', 'active bg-primary' : showActivePage=='foundation'&&showThemeMode=='dark', 'text-light' : showThemeMode=='dark'}]" href="/">
                            <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" fill="currentcolor" version="1.1" id="Layer_1" width="22" height="25" viewBox="0 0 20 20" enable-background="new 0 0 20 20" xml:space="preserve"><path d="M18,20H2c-0.6,0-1-0.4-1-1V1c0-0.6,0.4-1,1-1h5v2H3v16h14V0h2v19C19,19.6,18.6,20,18,20z" /><polygon points="15,9 12,7 9,9 9,0 15,0 " /></svg>
                        </a>
                        <span class="text-center">
                            Foundation
                        </span>
                    </li>
                    <li class="nav-item d-flex flex-column px-2 py-3 position-relative" @click.prevent="showActivePage='styles'">
                        <a :class="['nav-link d-flex justify-content-center rounded-pill stretched-link p-0 mx-3', {'active bg-info-subtle' : showActivePage=='styles'&&showThemeMode=='light', 'active bg-primary' : showActivePage=='styles'&&showThemeMode=='dark', 'text-light' : showThemeMode=='dark'}]" href="/">
                            <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" fill="currentcolor" height="25" width="25" version="1.1" id="Capa_1" viewBox="0 0 324.99 324.99" xml:space="preserve"><g><path d="M307.6,129.885c-11.453-11.447-23.783-16.778-38.805-16.778c-6.189,0-12.056,0.858-17.729,1.688   c-5.094,0.745-9.905,1.449-14.453,1.45c-8.27,0-14.197-2.397-19.82-8.017c-10.107-10.101-8.545-20.758-6.569-34.25   c2.357-16.096,5.291-36.127-15.101-56.508C183.578,5.932,167.848,0.081,148.372,0.081c-37.296,0-78.367,21.546-99.662,42.829   C17.398,74.205,0.1,115.758,0,159.917c-0.1,44.168,17.018,85.656,48.199,116.82c31.077,31.061,72.452,48.168,116.504,48.171   c0.005,0,0.007,0,0.013,0c44.315,0,86.02-17.289,117.428-48.681c17.236-17.226,32.142-44.229,38.9-70.471   C329.291,173.738,324.517,146.793,307.6,129.885z M309.424,202.764c-6.16,23.915-20.197,49.42-35.763,64.976   c-29.145,29.129-67.833,45.17-108.946,45.169c-0.002,0-0.009,0-0.011,0c-40.849-0.003-79.211-15.863-108.023-44.659   C27.777,239.36,11.908,200.896,12,159.944c0.092-40.962,16.142-79.512,45.191-108.545c19.071-19.061,57.508-39.317,91.18-39.317   c16.18,0,29.056,4.669,38.269,13.877c16.127,16.118,13.981,30.769,11.71,46.28c-2.067,14.116-4.41,30.115,9.96,44.478   c7.871,7.866,16.864,11.529,28.304,11.528c5.421-0.001,10.895-0.802,16.189-1.576c5.248-0.768,10.676-1.562,15.992-1.562   c7.938,0,18.557,1.508,30.322,13.267C317.724,156.971,313.562,186.699,309.424,202.764z" /><path d="M142.002,43.531c-1.109,0-2.233,0.065-3.342,0.192c-15.859,1.824-27.33,16.199-25.571,32.042   c1.613,14.631,13.93,25.665,28.647,25.665c1.105,0,2.226-0.065,3.332-0.191c15.851-1.823,27.326-16.191,25.581-32.031   C169.032,54.57,156.716,43.531,142.002,43.531z M143.7,89.317c-0.652,0.075-1.313,0.113-1.963,0.113   c-8.59,0-15.778-6.441-16.721-14.985c-1.032-9.296,5.704-17.729,15.016-18.8c0.655-0.075,1.317-0.114,1.971-0.114   c8.587,0,15.775,6.446,16.72,14.993C159.747,79.816,153.006,88.247,143.7,89.317z" /><path d="M102.997,113.64c-1.72-7.512-6.261-13.898-12.784-17.984c-4.597-2.881-9.889-4.404-15.304-4.404   c-10.051,0-19.254,5.079-24.618,13.587c-4.14,6.566-5.472,14.34-3.75,21.888c1.715,7.52,6.261,13.92,12.799,18.018   c4.596,2.88,9.888,4.402,15.303,4.402c10.051,0,19.255-5.078,24.624-13.593C103.401,128.975,104.726,121.193,102.997,113.64z    M89.111,129.16c-3.153,5.001-8.563,7.986-14.469,7.986c-3.158,0-6.246-0.889-8.93-2.57c-3.817-2.393-6.471-6.128-7.472-10.518   c-1.008-4.417-0.227-8.97,2.2-12.819c3.153-5.001,8.562-7.987,14.468-7.987c3.158,0,6.246,0.89,8.933,2.573   c3.806,2.384,6.454,6.11,7.458,10.493C92.312,120.743,91.534,125.306,89.111,129.16z" /><path d="M70.131,173.25c-3.275,0-6.516,0.557-9.63,1.654c-15.055,5.301-23.05,21.849-17.821,36.892   c4.032,11.579,14.984,19.358,27.254,19.358c3.276,0,6.517-0.556,9.637-1.652c15.065-5.301,23.053-21.854,17.806-36.896   C93.346,181.029,82.397,173.25,70.131,173.25z M75.589,218.182c-1.836,0.646-3.738,0.973-5.655,0.973   c-7.168,0-13.566-4.543-15.921-11.302c-3.063-8.814,1.636-18.518,10.476-21.63c1.83-0.645,3.729-0.973,5.643-0.973   c7.165,0,13.56,4.542,15.914,11.304C89.12,205.37,84.429,215.072,75.589,218.182z" /><path d="M140.817,229.415c-3.071-1.066-6.266-1.606-9.496-1.606c-12.307,0-23.328,7.804-27.431,19.429   c-2.566,7.317-2.131,15.185,1.229,22.151c3.349,6.943,9.204,12.163,16.486,14.696c3.075,1.071,6.274,1.614,9.51,1.614   c12.3,0,23.314-7.811,27.409-19.439c2.574-7.31,2.143-15.175-1.216-22.145C153.958,237.165,148.103,231.945,140.817,229.415z    M147.206,262.275c-2.407,6.834-8.873,11.425-16.091,11.425c-1.888,0-3.759-0.318-5.563-0.947c-4.253-1.48-7.67-4.524-9.623-8.575   c-1.965-4.074-2.219-8.68-0.718-12.957c2.408-6.825,8.883-11.411,16.11-11.411c1.888,0,3.759,0.317,5.561,0.942   c4.248,1.475,7.663,4.52,9.616,8.573C148.46,253.399,148.711,257.998,147.206,262.275z" /><path d="M212.332,213.811c-5.466,0-10.81,1.55-15.448,4.479c-13.525,8.521-17.652,26.427-9.193,39.927   c5.315,8.445,14.463,13.488,24.469,13.488c5.458,0,10.796-1.545,15.434-4.464c13.541-8.507,17.663-26.419,9.19-39.926   C231.486,218.86,222.345,213.811,212.332,213.811z M221.205,257.082c-2.725,1.715-5.853,2.622-9.045,2.622   c-5.857,0-11.207-2.946-14.307-7.87c-4.947-7.896-2.513-18.39,5.433-23.395c2.724-1.72,5.852-2.629,9.047-2.629   c5.854,0,11.192,2.944,14.283,7.878C231.577,241.597,229.151,252.09,221.205,257.082z" /><path d="M255.384,141.998c-1.06-0.117-2.134-0.176-3.194-0.176c-14.772,0-27.174,11.068-28.846,25.747   c-0.876,7.698,1.297,15.266,6.118,21.311c4.812,6.03,11.686,9.821,19.369,10.676c1.053,0.114,2.12,0.173,3.175,0.173   c14.754,0,27.164-11.067,28.869-25.748c0.886-7.688-1.277-15.247-6.091-21.288C269.97,146.651,263.082,142.853,255.384,141.998z    M268.955,172.602c-1.001,8.624-8.287,15.127-16.948,15.127c-0.621,0-1.251-0.034-1.86-0.101c-4.48-0.498-8.494-2.712-11.303-6.231   c-2.819-3.534-4.089-7.963-3.575-12.47c0.98-8.611,8.255-15.104,16.922-15.104c0.623,0,1.256,0.035,1.875,0.104   c4.498,0.499,8.523,2.717,11.334,6.244C268.209,163.697,269.472,168.114,268.955,172.602z" /></g></svg>
                        </a>
                        <span class="text-center">
                            Styles
                        </span>
                    </li>
                    <li class="nav-item d-flex flex-column px-2 py-3 position-relative" @click.prevent="showActivePage='components'">
                        <a :class="['nav-link d-flex justify-content-center rounded-pill stretched-link p-0 mx-3', {'active bg-info-subtle' : showActivePage=='components'&&showThemeMode=='light', 'active bg-primary' : showActivePage=='components'&&showThemeMode=='dark', 'text-light' : showThemeMode=='dark'}]" href="/">
                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentcolor" fill-rule="evenodd" clip-rule="evenodd"><path d="M11.5 0c6.347 0 11.5 5.153 11.5 11.5s-5.153 11.5-11.5 11.5-11.5-5.153-11.5-11.5 5.153-11.5 11.5-11.5zm0 1c5.795 0 10.5 4.705 10.5 10.5s-4.705 10.5-10.5 10.5-10.5-4.705-10.5-10.5 4.705-10.5 10.5-10.5zm.5 10h6v1h-6v6h-1v-6h-6v-1h6v-6h1v6z" /></svg>
                        </a>
                        <span class="text-center">
                            Components
                        </span>
                    </li>
                    <li class="nav-item d-flex flex-column px-2 py-3 position-relative" @click.prevent="showActivePage='blog'">
                        <a :class="['nav-link d-flex justify-content-center rounded-pill stretched-link p-0 mx-3', {'active bg-info-subtle' : showActivePage=='blog'&&showThemeMode=='light', 'active bg-primary' : showActivePage=='blog'&&showThemeMode=='dark', 'text-light' : showThemeMode=='dark'}]" href="/">
                            <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" fill="currentcolor" height="20" width="20" version="1.1" id="Capa_1" viewBox="0 0 297 297" xml:space="preserve"><g><path d="M263.535,0H33.465C15.013,0,0,15.013,0,33.465v230.07C0,281.987,15.013,297,33.465,297h230.07   C281.987,297,297,281.987,297,263.535V33.465C297,15.013,281.987,0,263.535,0z M276.085,263.535c0,6.92-5.63,12.549-12.55,12.549   H33.465c-6.92,0-12.55-5.629-12.55-12.549V33.465c0-6.92,5.63-12.55,12.55-12.55h230.07c6.92,0,12.55,5.63,12.55,12.55V263.535z" /><path d="M255.237,114.583l-66.652-10.704l-30.777-60.083c-1.789-3.494-5.383-5.69-9.308-5.69s-7.519,2.196-9.308,5.69   l-30.777,60.083l-66.652,10.704c-3.876,0.622-7.075,3.36-8.289,7.094c-1.212,3.731-0.233,7.829,2.536,10.609l47.632,47.838   l-10.417,66.699c-0.605,3.878,1.01,7.768,4.185,10.073c3.176,2.309,7.375,2.643,10.875,0.868l60.216-30.518l60.216,30.518   c1.493,0.757,3.112,1.13,4.727,1.13c2.169,0,4.327-0.674,6.147-1.998c3.176-2.306,4.791-6.195,4.186-10.073l-10.417-66.699   l47.632-47.838c2.77-2.78,3.748-6.878,2.536-10.609C262.313,117.943,259.113,115.205,255.237,114.583z M194.798,169.122   c-2.351,2.361-3.437,5.701-2.922,8.992l8.084,51.766l-46.733-23.686c-1.486-0.753-3.106-1.13-4.727-1.13s-3.241,0.377-4.727,1.13   L97.039,229.88l8.085-51.766c0.515-3.291-0.571-6.631-2.922-8.992l-36.966-37.126l51.728-8.307c3.291-0.528,6.132-2.592,7.65-5.558   l23.886-46.63l23.886,46.63c1.519,2.966,4.359,5.029,7.65,5.558l51.729,8.307L194.798,169.122z" /></g></svg>
                        </a>
                        <span class="text-center">
                            Blog
                        </span>
                    </li>
                </ul>
                <button class="btn rounded-circle border-secondary p-3" type="button" @click.prevent="toggleTheme">
                    <svg v-if="showThemeMode=='light'" class="mb-1 mx-1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" height="20" width="20" version="1.1" id="Capa_1" viewBox="0 0 47.539 47.539" xml:space="preserve"><g><g><path style="fill:#010002;" d="M24.997,47.511C11.214,47.511,0,36.298,0,22.515C0,12.969,5.314,4.392,13.869,0.132    c0.385-0.191,0.848-0.117,1.151,0.186s0.381,0.766,0.192,1.15C13.651,4.64,12.86,8.05,12.86,11.601    c0,12.681,10.316,22.997,22.997,22.997c3.59,0,7.033-0.809,10.236-2.403c0.386-0.191,0.848-0.117,1.151,0.186    c0.304,0.303,0.381,0.766,0.192,1.15C43.196,42.153,34.597,47.511,24.997,47.511z M12.248,3.372C5.862,7.608,2,14.709,2,22.515    c0,12.68,10.316,22.996,22.997,22.996c7.854,0,14.981-3.898,19.207-10.343c-2.668,0.95-5.464,1.43-8.346,1.43    c-13.783,0-24.997-11.214-24.997-24.997C10.861,8.761,11.327,6.005,12.248,3.372z" /></g></g></svg>            
                    <svg v-else xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" fill="#f8f9fa" height="30" width="30" version="1.1" id="Capa_1" viewBox="0 0 207.628 207.628" xml:space="preserve"><circle cx="103.814" cy="103.814" r="45.868" /><path d="M103.814,157.183c-29.427,0-53.368-23.941-53.368-53.368s23.941-53.368,53.368-53.368s53.368,23.941,53.368,53.368  S133.241,157.183,103.814,157.183z M103.814,65.446c-21.156,0-38.368,17.212-38.368,38.368s17.212,38.368,38.368,38.368  s38.368-17.212,38.368-38.368S124.97,65.446,103.814,65.446z" /><path d="M103.814,39.385c-4.142,0-7.5-3.358-7.5-7.5V7.5c0-4.142,3.358-7.5,7.5-7.5s7.5,3.358,7.5,7.5v24.385  C111.314,36.027,107.956,39.385,103.814,39.385z" /><path d="M103.814,207.628c-4.142,0-7.5-3.358-7.5-7.5v-24.385c0-4.142,3.358-7.5,7.5-7.5s7.5,3.358,7.5,7.5v24.385  C111.314,204.271,107.956,207.628,103.814,207.628z" /><path d="M200.128,111.314h-24.385c-4.142,0-7.5-3.358-7.5-7.5s3.358-7.5,7.5-7.5h24.385c4.142,0,7.5,3.358,7.5,7.5  S204.271,111.314,200.128,111.314z" /><path d="M31.885,111.314H7.5c-4.142,0-7.5-3.358-7.5-7.5s3.358-7.5,7.5-7.5h24.385c4.142,0,7.5,3.358,7.5,7.5  S36.027,111.314,31.885,111.314z" /><path d="M154.676,60.452c-1.919,0-3.839-0.732-5.303-2.197c-2.929-2.929-2.929-7.678,0-10.606l17.243-17.242  c2.929-2.929,7.678-2.93,10.606,0c2.929,2.929,2.929,7.678,0,10.606l-17.243,17.242C158.515,59.72,156.595,60.452,154.676,60.452z" /><path d="M35.709,179.419c-1.919,0-3.839-0.732-5.303-2.197c-2.929-2.929-2.929-7.678,0-10.606l17.243-17.243  c2.929-2.929,7.678-2.929,10.606,0c2.929,2.929,2.929,7.678,0,10.606l-17.243,17.243C39.548,178.687,37.629,179.419,35.709,179.419z  " /><path d="M171.918,179.419c-1.919,0-3.839-0.732-5.303-2.197l-17.243-17.243c-2.929-2.929-2.929-7.678,0-10.606  c2.929-2.929,7.678-2.929,10.606,0l17.243,17.243c2.929,2.929,2.929,7.678,0,10.606  C175.757,178.687,173.838,179.419,171.918,179.419z" /><path d="M52.952,60.452c-1.919,0-3.839-0.732-5.303-2.197L30.406,41.013c-2.929-2.929-2.929-7.677,0-10.606  c2.929-2.929,7.678-2.93,10.606,0l17.243,17.242c2.929,2.929,2.929,7.677,0,10.606C56.791,59.72,54.872,60.452,52.952,60.452z" /></svg>           
                </button>
            </nav>
            <nav :class="['col-12 navbar d-xl-none position-fixed z-2 py-3', showThemeMode=='dark' ? 'bg-black' : 'bg-white']">
                <button :class="['navbar-toggler border-0 position-fixed px-4', {'text-light' : showThemeMode=='dark'}]" type="button">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="currentcolor" viewBox="0 0 50 50" width="25" height="25"><path d="M 5 8 A 2.0002 2.0002 0 1 0 5 12 L 45 12 A 2.0002 2.0002 0 1 0 45 8 L 5 8 z M 5 23 A 2.0002 2.0002 0 1 0 5 27 L 45 27 A 2.0002 2.0002 0 1 0 45 23 L 5 23 z M 5 38 A 2.0002 2.0002 0 1 0 5 42 L 45 42 A 2.0002 2.0002 0 1 0 45 38 L 5 38 z" /></svg>                
                </button>
                <ul class="nav d-flex justify-content-between ps-4 mx-5 w-100">
                    <li class="nav-item">
                        <div class="d-flex">
                            <svg class="me-2" xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 24 24" fill="none"><path fill-rule="evenodd" clip-rule="evenodd" d="M16 8H8C7.45 8 7.005 8.45 7.005 9L7 15C7 15.55 7.45 16 8 16H16C16.55 16 17 15.55 17 15V9C17 8.45 16.55 8 16 8ZM8.00001 9.99997L12 12.5L16 9.99997V15H8.00001V9.99997ZM8.00001 9.00001L12 11.5L16 9.00001H8.00001Z" fill="currentcolor" /><path fill-rule="evenodd" clip-rule="evenodd" d="M12 22C17.5228 22 22 17.5228 22 12C22 6.47715 17.5228 2 12 2C6.47715 2 2 6.47715 2 12C2 17.5228 6.47715 22 12 22ZM12 20C16.4183 20 20 16.4183 20 12C20 7.58172 16.4183 4 12 4C7.58172 4 4 7.58172 4 12C4 16.4183 7.58172 20 12 20Z" fill="currentcolor" /></svg>
                            <span class="d-md-block d-none pt-1"><b>Material Design 3</b></span>
                        </div>
                    </li>
                    <li class="nav-item">
                        <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" fill="currentcolor" height="20" width="20" version="1.1" id="Capa_1" viewBox="0 0 488.4 488.4" xml:space="preserve"><g><g><path d="M0,203.25c0,112.1,91.2,203.2,203.2,203.2c51.6,0,98.8-19.4,134.7-51.2l129.5,129.5c2.4,2.4,5.5,3.6,8.7,3.6    s6.3-1.2,8.7-3.6c4.8-4.8,4.8-12.5,0-17.3l-129.6-129.5c31.8-35.9,51.2-83,51.2-134.7c0-112.1-91.2-203.2-203.2-203.2    S0,91.15,0,203.25z M381.9,203.25c0,98.5-80.2,178.7-178.7,178.7s-178.7-80.2-178.7-178.7s80.2-178.7,178.7-178.7S381.9,104.65,381.9,203.25z" /></g></g></svg>
                    </li>
                </ul>
            </nav>
            <div class="col-12 pt-xl-0 ps-xl-5 pt-5 h-100">
                <div class="ps-xl-5 h-100">
                    <div class="row d-xxl-flex d-md-none d-sm-flex d-none g-0 ps-xl-2 pt-2 mb-5 h-75">
                        <div class="col-12 p-2 pt-3 h-100">
                            <div class="card border-0 rounded-5 h-100">
                                <img v-if="showThemeMode=='light'" class="card-img rounded-5 h-100" src="https://lh3.googleusercontent.com/2OrUzHCRSI-V46Z1qJBh90usG6OkKwCbXN80FbrjkWoQz4VfoJjNAoQHLHPQRZWH7dI_m5I1gi48h6xMJ5pK6kkdXmUnXPe4VqwvEdo4QeWRjLV9Oew=w2400-rj" alt="Material Design">
                                <img v-else class="card-img rounded-5 h-100" src="https://lh3.googleusercontent.com/BvKj8kuRZqLpqPuuZxOl4IeHv5jaD5kT1jhn3P8EMBcmzyoHRAFXsCxNH6ZeHhQG4V1F_AegXIw2cJIBmETy7eHM27IdLQe7FqEgz6NLaXflHiHM4xyh=w2400-rj" alt="Material Design">
                                <div :class="['card-img-overlay d-flex justify-content-center p-5', {'text-light' : showThemeMode=='dark'}]">
                                    <div class="d-flex flex-column justify-content-center align-items-center p-xl-5">
                                        <h1 class="card-title text-center display-1"><b>Material Design</b></h1>
                                        <p class="card-text text-center h4">Material 3 is the latest version of Google's open-source design system. Design and build beautiful, usable products with Material 3.</p>
                                        <button :class="['btn btn-lg rounded-pill px-5 py-4 mt-3', showThemeMode=='dark' ? 'bg-primary-subtle text-primary' : ' bg-primary text-white']" type="button"><span class="h3">Get started</span></button>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="row d-xxl-none d-md-flex d-sm-none d-flex g-0 ps-xl-2 pt-2 mb-5 h-50">
                        <div class="col-12 p-2 pt-3 h-100">
                            <div class="card border-0 rounded-5 h-100">
                                <img v-if="showThemeMode=='light'" class="card-img rounded-5 h-100" src="https://lh3.googleusercontent.com/2OrUzHCRSI-V46Z1qJBh90usG6OkKwCbXN80FbrjkWoQz4VfoJjNAoQHLHPQRZWH7dI_m5I1gi48h6xMJ5pK6kkdXmUnXPe4VqwvEdo4QeWRjLV9Oew=w2400-rj" alt="Material Design">
                                <img v-else class="card-img rounded-5 h-100" src="https://lh3.googleusercontent.com/BvKj8kuRZqLpqPuuZxOl4IeHv5jaD5kT1jhn3P8EMBcmzyoHRAFXsCxNH6ZeHhQG4V1F_AegXIw2cJIBmETy7eHM27IdLQe7FqEgz6NLaXflHiHM4xyh=w2400-rj" alt="Material Design">
                                <div :class="['card-img-overlay d-flex justify-content-center p-5', {'text-light' : showThemeMode=='dark'}]">
                                    <div class="d-flex flex-column justify-content-center align-items-center p-xl-5">
                                        <h1 class="card-title text-center display-1"><b>Material Design</b></h1>
                                        <p class="card-text text-center h4">Material 3 is the latest version of Google's open-source design system. Design and build beautiful, usable products with Material 3.</p>
                                        <button :class="['btn btn-lg rounded-pill px-5 py-4 mt-3', showThemeMode=='dark' ? 'bg-primary-subtle text-primary' : ' bg-primary text-white']" type="button"><span class="h3">Get started</span></button>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div :class="['row g-0 ps-xl-2', showThemeMode=='light' ? 'bg-white' : 'bg-black']">
                        <div class="col-12 p-1">
                            <div class="row g-0 my-5">
                                <h2 class="display-5 ps-4 mb-4"><b>News & launches</b></h2>
                                <div class="col-xxl-4 col-6 p-1">
                                    <div :class="['card border-0 rounded-5 h-100', showThemeMode=='dark' ? 'text-bg-dark' : 'text-bg-light']">
                                        <img src="https://lh3.googleusercontent.com/mLGakWFjdX3zGBIhCUWqzjlj3gUXOY8hOed_ISzomlpNmjKWUiqCFyNGGAZFneVaK30v4GUpjn7lyIsI2Z7KPvMKrYkumzBr2nwbVe3BQKRkpam3sA=w960" class="card-img-top rounded-5" alt="...">
                                        <div class="card-body p-4">
                                            <p class="h3">Figma design kit</p>
                                            <p class="card-text">Jumpstart your M3 designs with the complete library of ready-made components</p>
                                        </div>
                                    </div>
                                </div>
                                <div class="col-xxl-4 col-6 p-1">
                                    <div :class="['card border-0 rounded-5 h-100', showThemeMode=='dark' ? 'text-bg-dark' : 'text-bg-light']">
                                        <img src="https://lh3.googleusercontent.com/aiJojq_gpPLqLhU0PZH6Dog-OjIMti_hiclF_6oqxucGuvywn_AEtu2Qrk2f4WxEhRWMjXkz8qXpTCGoj5TZ0DUCEZ5UIXnXTSIu_7ndg2dTNmQbdkCO=w960" class="card-img-top rounded-5" alt="...">
                                        <div class="card-body p-4">
                                            <p class="h3">Large screen guidance</p>
                                            <p class="card-text">Get started adapting your layouts for a range of window size classes and hardware</p>
                                        </div>
                                    </div>
                                </div>
                                <div class="col-xxl-4 col-6 p-1">
                                    <div :class="['card border-0 rounded-5 h-100', showThemeMode=='dark' ? 'text-bg-dark' : 'text-bg-light']">
                                        <img src="https://lh3.googleusercontent.com/51moDkmVWptBFXRReuACKocS_fsOoYtfT-C78onEUKeRr7ky4l_ZsuZMK2AnE7-MPRbLzcKTAIFmNyyN7ACo0-eygmXaGeR0ItYtRcYNE8-_L8RHqkA=w960" class="card-img-top rounded-5" alt="...">
                                        <div class="card-body p-4">
                                            <p class="h3">Material Design at Google I/O</p>
                                            <p class="card-text">See the full list of Material talks and tutorials launching at I/O 2023</p>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="col-12 p-1">
                            <div class="row g-0 my-5">
                                <h1 class="display-5 ps-4 mb-4"><b>Design system updates</b></h1>
                                <div class="col-xxl-4 col-6 p-1">
                                    <div :class="['card border-0 rounded-5 h-100', showThemeMode=='dark' ? 'text-bg-dark' : 'text-bg-light']">
                                        <img src="https://lh3.googleusercontent.com/AG8Da4Doz97XcS62XgVOYWiRwcwgZZdhJOeejfA9bhzY8K5cyhsy753fFaNgkZjcTXA7MwQnPOa9FjKaFFoOVDGVh33PutwuflvNCXkfBS7AR5GbeQ=w960" class="card-img-top rounded-5" alt="...">
                                        <div class="card-body p-4">
                                            <p class="h3">M3 for Jetpack Compose</p>
                                            <p class="card-text">With the latest stable release, use Jetpack Compose to build a complete M3 Android app</p>
                                        </div>
                                    </div>
                                </div>
                                <div class="col-xxl-4 col-6 p-1">
                                    <div :class="['card border-0 rounded-5 h-100', showThemeMode=='dark' ? 'text-bg-dark' : 'text-bg-light']">
                                        <img src="https://lh3.googleusercontent.com/IfqcD9hZWV1tohxFc8gyiP9kVjz0Igg1trtKkYD3qxvEziIxbnD2b8mCpmJqC015XWD14Pvwy-0vRUSJltvEa9tcY8TnWpO0zYJaR1IPjJlRrWpo3Q=w960" class="card-img-top rounded-5" alt="...">
                                        <div class="card-body p-4">
                                            <p class="h3">New component: M3 carousel</p>
                                            <p class="card-text">An expressive new component for displaying scrollable collections of content</p>
                                        </div>
                                    </div>
                                </div>
                                <div class="col-xxl-4 col-6 p-1">
                                    <div :class="['card border-0 rounded-5 h-100', showThemeMode=='dark' ? 'text-bg-dark' : 'text-bg-light']">
                                        <img src="https://lh3.googleusercontent.com/aLTg-FT4Ocgvjw1B_i3fOVK-rWoV3C7XCHyBkKwSbJFzIZtJjo-5atBHcSs9aZdHxiMw8-nP3lCnULJtFG_KdIVg7Gk-NV8sc1DJkeMRsTtir9pIu6IY=w960" class="card-img-top rounded-5" alt="...">
                                        <div class="card-body p-4">
                                            <p class="h3">Back navigation & gestures</p>
                                            <p class="card-text">Explore new motion and gesture capabilities for smooth navigation across screens</p>
                                        </div>
                                    </div>
                                </div>
                                <div class="col-xxl-4 col-6 p-1">
                                    <div :class="['card border-0 rounded-5 h-100', showThemeMode=='dark' ? 'text-bg-dark' : 'text-bg-light']">
                                        <img src="https://lh3.googleusercontent.com/QTSOFxOaVde6gu-lNjTZ_VrOh7ihpSgRc-hErsBVjQ4Te9tIj4cW4BNWXj2fy1WbDnWYNS3v6pO628xBLC-A74K7ylf0ODNz-jbNhM1OUCgTUvZSN3zP=w960" class="card-img-top rounded-5" alt="...">
                                        <div class="card-body p-4">
                                            <p class="h3">Motion system updates</p>
                                            <p class="card-text">Get started applying motion, from ready-to-use transition patterns to updated guidance</p>
                                        </div>
                                    </div>
                                </div>
                                <div class="col-xxl-4 col-6 p-1">
                                    <div :class="['card border-0 rounded-5 h-100', showThemeMode=='dark' ? 'text-bg-dark' : 'text-bg-light']">
                                        <img src="https://lh3.googleusercontent.com/w0mg7Iy0YoeV7ViHTp9XRzZFTbCX-ME87HPfbv_XFFZlQ-D6tjVwxsY1X_HUrFiXf-kNp8LePGcqv2Oh3OiNU6J28BYhiTf8UQKJBRDYPZejkpKE0NQ=w960" class="card-img-top rounded-5" alt="...">
                                        <div class="card-body p-4">
                                            <p class="h3">Material Theme Builder</p>
                                            <p class="card-text">Easily migrate or get started with the M3 color system and dynamic color</p>
                                        </div>
                                    </div>
                                </div>
                                <div class="col-xxl-4 col-6 p-1">
                                    <div :class="['card border-0 rounded-5 h-100', showThemeMode=='dark' ? 'text-bg-dark' : 'text-bg-light']">
                                        <img src="https://lh3.googleusercontent.com/560ITYkB-YZ3Hc2f0s-i9doX7kqOZ_CNnuzS7XtPolT6zfcKk7PW2TCSlD61OkSAu9eLXn1U404j5Sc4tZNZh-j4IscbCgHURVy1eC7fGtFESdOQMdhm=w960" class="card-img-top rounded-5" alt="...">
                                        <div class="card-body p-4">
                                            <p class="h3">New color guidance for tones</p>
                                            <p class="card-text">Updates include tone-based surface colors, contrast modes, and fixed accent colors</p>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="col-12 p-1 border-bottom">
                            <div class="row g-0 pb-5 my-5">
                                <h1 class="display-5 ps-4 mb-4"><b>Resources</b></h1>
                                <div class="col-lg-6 col-12 p-1">
                                    <div :class="['card border-0 rounded-5 h-100', showThemeMode=='dark' ? 'text-bg-dark' : 'text-bg-light']">
                                        <div class="card-body d-flex flex-column justify-content-end p-4">
                                            <p class="h3 card-title">Material blog</p>
                                            <p class="card-text">News, tutorials, and inspiration from the Material team</p>
                                        </div>
                                    </div>
                                </div>
                                <div class="col-lg-6 col-12 p-1">
                                    <div :class="['card border-0 rounded-5 h-100', showThemeMode=='dark' ? 'text-bg-dark' : 'text-bg-light']">
                                        <div class="card-body d-flex flex-column justify-content-end p-4">
                                            <h3 class="card-title">Figma design kit</h3>
                                            <p class="card-text">Customizable styles and components to help you design with Material 3</p>
                                        </div>
                                    </div>
                                </div>
                                <div class="col-lg-6 col-12 p-1">
                                    <div :class="['card border-0 rounded-5 h-100', showThemeMode=='dark' ? 'text-bg-dark' : 'text-bg-light']">
                                        <div class="card-body d-flex flex-column justify-content-end p-4">
                                            <p class="h3 card-title">Get started</p>
                                            <p class="card-text">Guides, videos, and tools to start building with Material</p>
                                        </div>
                                    </div>
                                </div>
                                <div class="col-lg-6 col-12 p-1">
                                    <div :class="['card border-0 rounded-5 h-100', showThemeMode=='dark' ? 'text-bg-dark' : 'text-bg-light']">
                                        <div class="card-body d-flex flex-column justify-content-end p-4">
                                            <p class="h3 card-title">Develop</p>
                                            <p class="card-text">Code and developer documentation for Android, Flutter, and the Web</p>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="col-12 p-5">
                            <div class="row g-0 mt-5">
                                <div class="col-lg-6 col-12 pe-5 mb-lg-0 mb-4">
                                    <div class="d-flex flex-column">
                                        <svg class="mb-4" xmlns="http://www.w3.org/2000/svg" width="50" height="50" viewBox="0 0 24 24" fill="none"><path fill-rule="evenodd" clip-rule="evenodd" d="M16 8H8C7.45 8 7.005 8.45 7.005 9L7 15C7 15.55 7.45 16 8 16H16C16.55 16 17 15.55 17 15V9C17 8.45 16.55 8 16 8ZM8.00001 9.99997L12 12.5L16 9.99997V15H8.00001V9.99997ZM8.00001 9.00001L12 11.5L16 9.00001H8.00001Z" fill="currentcolor" /><path fill-rule="evenodd" clip-rule="evenodd" d="M12 22C17.5228 22 22 17.5228 22 12C22 6.47715 17.5228 2 12 2C6.47715 2 2 6.47715 2 12C2 17.5228 6.47715 22 12 22ZM12 20C16.4183 20 20 16.4183 20 12C20 7.58172 16.4183 4 12 4C7.58172 4 4 7.58172 4 12C4 16.4183 7.58172 20 12 20Z" fill="currentcolor" /></svg>
                                        <span>
                                            Material Design is an adaptable system of guidelines, components, and tools that support the best practices of user interface design. Backed by open-source code, Material Design streamlines collaboration between designers and developers, and helps teams quickly build beautiful products.
                                        </span>
                                    </div>
                                </div>
                                <div class="col-lg-2 col-4">
                                    <ul class="nav flex-column">
                                        <li class="nav-item px-3 py-2">
                                            <span>Social</span>
                                        </li>
                                        <li class="nav-item">
                                            <a class="nav-link h6" href="/">
                                                GitHub
                                            </a>
                                        </li>
                                        <li class="nav-item">
                                            <a class="nav-link" href="/">
                                                Twitter
                                            </a>
                                        </li>
                                        <li class="nav-item">
                                            <a class="nav-link" href="/">
                                                YouTube
                                            </a>
                                        </li>
                                        <li class="nav-item">
                                            <a class="nav-link" href="/">
                                                Blog RSS
                                            </a>
                                        </li>
                                    </ul>
                                </div>
                                <div class="col-lg-2 col-4">
                                    <ul class="nav flex-column">
                                        <li class="nav-item px-3 py-2">
                                            <span>Libraries</span>
                                        </li>
                                        <li class="nav-item">
                                            <a class="nav-link" href="/">
                                                Android
                                            </a>
                                        </li>
                                        <li class="nav-item">
                                            <a class="nav-link" href="/">
                                                Compose
                                            </a>
                                        </li>
                                        <li class="nav-item">
                                            <a class="nav-link" href="/">
                                                Flutter
                                            </a>
                                        </li>
                                        <li class="nav-item">
                                            <a class="nav-link" href="/">
                                                Web
                                            </a>
                                        </li>
                                    </ul>
                                </div>
                                <div class="col-lg-2 col-4">
                                    <ul class="nav flex-column">
                                        <li class="nav-item px-3 py-2">
                                            <span>Archived versions</span>
                                        </li>
                                        <li class="nav-item">
                                            <a class="nav-link" href="/">
                                                Material Design 1
                                            </a>
                                        </li>
                                        <li class="nav-item">
                                            <a class="nav-link" href="/">
                                                Material Design 2
                                            </a>
                                        </li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                        <div class="col-12 p-5 pt-0">
                            <ul class="nav">
                                <li class="nav-item">
                                    <a class="nav-link" href="/">
                                        <svg :class="[showThemeMode=='dark' ? 'text-white' : 'text-black']" fill="currentcolor" width="71" height="23" xmlns="http://www.w3.org/2000/svg"><path d="M0 8.773C0 3.937 4.083 0 8.938 0c2.684 0 4.595 1.047 6.034 2.415l-1.695 1.693c-1.032-.962-2.429-1.712-4.339-1.712-3.545 0-6.317 2.847-6.317 6.377s2.772 6.381 6.317 6.381c2.297 0 3.607-.921 4.446-1.756.687-.686 1.137-1.67 1.307-3.02H8.938V7.982h8.097c.085.43.129.946.129 1.5 0 1.797-.494 4.025-2.084 5.608-1.547 1.603-3.524 2.462-6.142 2.462C4.083 17.55 0 13.61 0 8.773zm23.693 6.303c-1.719 0-3.198-1.413-3.198-3.425 0-2.032 1.479-3.423 3.198-3.423 1.718 0 3.201 1.391 3.201 3.423 0 2.012-1.483 3.425-3.201 3.425m0-9.076C20.557 6 18 8.375 18 11.65c0 3.257 2.557 5.652 5.693 5.652 3.137 0 5.692-2.395 5.692-5.651C29.385 8.375 26.83 6 23.693 6m13.003 9.076c-1.719 0-3.2-1.413-3.2-3.425 0-2.032 1.481-3.423 3.2-3.423 1.718 0 3.2 1.391 3.2 3.423 0 2.012-1.482 3.425-3.2 3.425m0-9.076C33.559 6 31 8.375 31 11.65c0 3.257 2.559 5.652 5.696 5.652 3.135 0 5.692-2.395 5.692-5.651C42.388 8.375 39.831 6 36.696 6m11.952 9.076c-1.716 0-3.156-1.432-3.156-3.403 0-1.991 1.44-3.445 3.156-3.445 1.697 0 3.031 1.454 3.031 3.445 0 1.971-1.334 3.403-3.031 3.403zm2.858-8.732v.918h-.085C50.861 6.601 49.789 6 48.434 6 45.6 6 43 8.485 43 11.673c0 3.168 2.6 5.63 5.434 5.63 1.355 0 2.427-.6 2.987-1.287h.085v.816c0 2.162-1.161 3.316-3.028 3.316-1.526 0-2.471-1.092-2.857-2.01l-2.171.9c.624 1.498 2.278 3.336 5.028 3.336 2.922 0 5.391-1.713 5.391-5.885V6.344h-2.363zM56 16.608h2.49V0H56zm9.434-8.425c.987 0 1.825.494 2.104 1.199l-5.069 2.096c-.065-2.182 1.697-3.295 2.965-3.295m.192 6.891c-1.267 0-2.169-.578-2.748-1.71l7.582-3.125-.259-.643C69.729 8.333 68.29 6 65.347 6 62.427 6 60 8.292 60 11.65c0 3.167 2.404 5.65 5.626 5.65 2.599 0 4.103-1.583 4.727-2.504l-1.934-1.284c-.643.942-1.525 1.562-2.793 1.562"></path></svg>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a :class="['nav-link', showThemeMode=='dark' ? 'text-white' : 'text-black']" href="/">
                                        Privacy Policy
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a :class="['nav-link', showThemeMode=='dark' ? 'text-white' : 'text-black']" href="/">
                                        Terms of Service
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a :class="['nav-link', showThemeMode=='dark' ? 'text-white' : 'text-black']" href="/">
                                        Join research studies
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a :class="['nav-link', showThemeMode=='dark' ? 'text-white' : 'text-black']" href="/">
                                        Feedback
                                    </a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>
