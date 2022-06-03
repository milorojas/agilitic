<script setup>
import { Head, Link } from "@inertiajs/inertia-vue3";
import { defineComponent, h } from "vue";
import { Popover, PopoverButton, PopoverPanel } from "@headlessui/vue";
import {
    MenuIcon,
    XIcon,
    GlobeAltIcon,
    LightningBoltIcon,
    MailIcon,
    BeakerIcon,
    DatabaseIcon,
    ScaleIcon,
    TerminalIcon,
    ChartPieIcon,
} from "@heroicons/vue/outline";
import { ChevronRightIcon, ExternalLinkIcon } from "@heroicons/vue/solid";

const navigation = [
    { name: "Quienes somos", href: "#" },
    { name: "Que hacemos", href: "#" },
    { name: "Contacto", href: "#" },
];

const features = [
    {
        name: "Desarrollo de Software",
        description:
            "Utilizamos los últimos frameworks de desarrollo, aplicando sobre ellos las mejores prácticas en desarrollo de software.",
        icon: TerminalIcon,
    },
    {
        name: "Integración de Datos",
        description:
            "Contamos con basta experiencia en integración de datos, utilizando herramientas opensource y de pago.",
        icon: ChartPieIcon,
    },
    {
        name: "Business Intelligence",
        description:
            "Generamos estructuras de datos ideales para encontrar el valor agregado de tus datos y mejorar la toma de decisiones en su operación.",
        icon: DatabaseIcon,
    },
    {
        name: "Data Science",
        description:
            "Te ayudaremos a buscar mejoras en tu operación aplicando distintas herramientas y metodologías Machine Learning y Deep Learning.",
        icon: BeakerIcon,
    },
];

const social = [
    {
        name: "Facebook",
        href: "#",
        icon: defineComponent({
            render: () =>
                h("svg", { fill: "currentColor", viewBox: "0 0 24 24" }, [
                    h("path", {
                        "fill-rule": "evenodd",
                        d: "M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z",
                        "clip-rule": "evenodd",
                    }),
                ]),
        }),
    },
    {
        name: "Instagram",
        href: "#",
        icon: defineComponent({
            render: () =>
                h("svg", { fill: "currentColor", viewBox: "0 0 24 24" }, [
                    h("path", {
                        "fill-rule": "evenodd",
                        d: "M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 2.427.465a4.902 4.902 0 011.772 1.153 4.902 4.902 0 011.153 1.772c.247.636.416 1.363.465 2.427.048 1.067.06 1.407.06 4.123v.08c0 2.643-.012 2.987-.06 4.043-.049 1.064-.218 1.791-.465 2.427a4.902 4.902 0 01-1.153 1.772 4.902 4.902 0 01-1.772 1.153c-.636.247-1.363.416-2.427.465-1.067.048-1.407.06-4.123.06h-.08c-2.643 0-2.987-.012-4.043-.06-1.064-.049-1.791-.218-2.427-.465a4.902 4.902 0 01-1.772-1.153 4.902 4.902 0 01-1.153-1.772c-.247-.636-.416-1.363-.465-2.427-.047-1.024-.06-1.379-.06-3.808v-.63c0-2.43.013-2.784.06-3.808.049-1.064.218-1.791.465-2.427a4.902 4.902 0 011.153-1.772A4.902 4.902 0 015.45 2.525c.636-.247 1.363-.416 2.427-.465C8.901 2.013 9.256 2 11.685 2h.63zm-.081 1.802h-.468c-2.456 0-2.784.011-3.807.058-.975.045-1.504.207-1.857.344-.467.182-.8.398-1.15.748-.35.35-.566.683-.748 1.15-.137.353-.3.882-.344 1.857-.047 1.023-.058 1.351-.058 3.807v.468c0 2.456.011 2.784.058 3.807.045.975.207 1.504.344 1.857.182.466.399.8.748 1.15.35.35.683.566 1.15.748.353.137.882.3 1.857.344 1.054.048 1.37.058 4.041.058h.08c2.597 0 2.917-.01 3.96-.058.976-.045 1.505-.207 1.858-.344.466-.182.8-.398 1.15-.748.35-.35.566-.683.748-1.15.137-.353.3-.882.344-1.857.048-1.055.058-1.37.058-4.041v-.08c0-2.597-.01-2.917-.058-3.96-.045-.976-.207-1.505-.344-1.858a3.097 3.097 0 00-.748-1.15 3.098 3.098 0 00-1.15-.748c-.353-.137-.882-.3-1.857-.344-1.023-.047-1.351-.058-3.807-.058zM12 6.865a5.135 5.135 0 110 10.27 5.135 5.135 0 010-10.27zm0 1.802a3.333 3.333 0 100 6.666 3.333 3.333 0 000-6.666zm5.338-3.205a1.2 1.2 0 110 2.4 1.2 1.2 0 010-2.4z",
                        "clip-rule": "evenodd",
                    }),
                ]),
        }),
    },
    {
        name: "Twitter",
        href: "#",
        icon: defineComponent({
            render: () =>
                h("svg", { fill: "currentColor", viewBox: "0 0 24 24" }, [
                    h("path", {
                        d: "M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.713v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84",
                    }),
                ]),
        }),
    },
    {
        name: "GitHub",
        href: "#",
        icon: defineComponent({
            render: () =>
                h("svg", { fill: "currentColor", viewBox: "0 0 24 24" }, [
                    h("path", {
                        "fill-rule": "evenodd",
                        d: "M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z",
                        "clip-rule": "evenodd",
                    }),
                ]),
        }),
    },
];

defineProps({
    canLogin: Boolean,
    canRegister: Boolean,
    laravelVersion: String,
    phpVersion: String,
});
</script>

<template>
    <Head title="Agilitic" />

    <!-- Hero -->
    <div class="relative overflow-hidden">
        <Popover as="header" class="relative">
            <div class="bg-gray-900 pt-6">
                <nav
                    class="relative mx-auto flex max-w-7xl items-center justify-between px-4 sm:px-6"
                    aria-label="Global">
                    <div class="flex flex-1 items-center">
                        <div
                            class="flex w-full items-center justify-between md:w-auto">
                            <a href="#">
                                <span class="sr-only">Agilitic</span>
                                <img
                                    class="h-14 w-auto sm:h-14"
                                    src="/agilitic.png"
                                    alt="" />
                            </a>
                            <div class="-mr-2 flex items-center md:hidden">
                                <PopoverButton
                                    class="focus-ring-inset inline-flex items-center justify-center rounded-md bg-gray-900 p-2 text-gray-400 hover:bg-gray-800 focus:outline-none focus:ring-2 focus:ring-white">
                                    <span class="sr-only">Open main menu</span>
                                    <MenuIcon
                                        class="h-6 w-6"
                                        aria-hidden="true" />
                                </PopoverButton>
                            </div>
                        </div>
                        <div class="hidden space-x-8 md:ml-10 md:flex">
                            <a
                                v-for="item in navigation"
                                :key="item.name"
                                :href="item.href"
                                class="text-base font-medium text-white hover:text-gray-300"
                                >{{ item.name }}</a
                            >
                        </div>
                    </div>
                    <div class="hidden md:flex md:items-center md:space-x-6">
                        <a
                            href="#"
                            class="inline-flex items-center rounded-md border border-transparent bg-gray-600 px-4 py-2 text-base font-medium text-white hover:bg-gray-700">
                            Ingresar
                        </a>
                    </div>
                </nav>
            </div>

            <transition
                enter-active-class="duration-150 ease-out"
                enter-from-class="opacity-0 scale-95"
                enter-to-class="opacity-100 scale-100"
                leave-active-class="duration-100 ease-in"
                leave-from-class="opacity-100 scale-100"
                leave-to-class="opacity-0 scale-95">
                <PopoverPanel
                    focus
                    class="absolute inset-x-0 top-0 z-10 origin-top transform p-2 transition md:hidden">
                    <div
                        class="overflow-hidden rounded-lg bg-white shadow-md ring-1 ring-black ring-opacity-5">
                        <div
                            class="flex items-center justify-between px-5 pt-4">
                            <div>
                                <img
                                    class="h-8 w-auto"
                                    src="/agilitic.png"
                                    alt="" />
                            </div>
                            <div class="-mr-2">
                                <PopoverButton
                                    class="inline-flex items-center justify-center rounded-md bg-white p-2 text-gray-400 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-600">
                                    <span class="sr-only">Close menu</span>
                                    <XIcon class="h-6 w-6" aria-hidden="true" />
                                </PopoverButton>
                            </div>
                        </div>
                        <div class="pt-5 pb-6">
                            <div class="space-y-1 px-2">
                                <a
                                    v-for="item in navigation"
                                    :key="item.name"
                                    :href="item.href"
                                    class="block rounded-md px-3 py-2 text-base font-medium text-gray-900 hover:bg-gray-50"
                                    >{{ item.name }}</a
                                >
                            </div>
                            <div class="mt-6 px-5">
                                <a
                                    href="#"
                                    class="block w-full rounded-md bg-indigo-600 py-3 px-4 text-center font-medium text-white shadow hover:bg-indigo-700"
                                    >Start free trial</a
                                >
                            </div>
                            <div class="mt-6 px-5">
                                <p
                                    class="text-center text-base font-medium text-gray-500">
                                    Existing customer?
                                    <a
                                        href="#"
                                        class="text-gray-900 hover:underline"
                                        >Login</a
                                    >
                                </p>
                            </div>
                        </div>
                    </div>
                </PopoverPanel>
            </transition>
        </Popover>

        <main>
            <div
                class="bg-gray-900 pt-10 sm:pt-16 lg:overflow-hidden lg:pt-8 lg:pb-14">
                <div class="mx-auto max-w-7xl lg:px-8">
                    <div class="lg:grid lg:grid-cols-2 lg:gap-8">
                        <div
                            class="mx-auto max-w-md px-4 sm:max-w-2xl sm:px-6 sm:text-center lg:flex lg:items-center lg:px-0 lg:text-left">
                            <div class="lg:py-24">
                                <!--
                                    <a
                                    href="#"
                                    class="inline-flex items-center rounded-full bg-black p-1 pr-2 text-white hover:text-gray-200 sm:text-base lg:text-sm xl:text-base">
                                    <span
                                        class="rounded-full bg-indigo-500 px-3 py-0.5 text-xs font-semibold uppercase leading-5 tracking-wide text-white"
                                        >Estamos buscando profesionales</span
                                    >
                                    <span class="ml-4 text-sm"
                                        >Visita nuestro sitio de empleos</span
                                    >
                                    <ChevronRightIcon
                                        class="ml-2 h-5 w-5 text-gray-500"
                                        aria-hidden="true" />
                                </a>-->
                                <h1
                                    class="mt-4 text-4xl font-extrabold tracking-tight text-white sm:mt-5 sm:text-6xl lg:mt-6 xl:text-6xl">
                                    <span class="block">Transformación</span>
                                    <span class="block text-indigo-400"
                                        >Digital</span
                                    >
                                </h1>
                                <p
                                    class="mt-3 text-base text-gray-300 sm:mt-5 sm:text-xl lg:text-lg xl:text-xl">
                                    Potencia tu negocio a través de los datos,
                                    te apoyamos en el desarrollo de soluciones
                                    analíticas y software que permitan optimizar
                                    procesos y disminuir costos a través de la
                                    automatización de tareas y toma de
                                    decisiones inteligentes sustentadas por tus
                                    datos.
                                </p>
                                <div class="mt-10 sm:mt-12">
                                    <form
                                        action="#"
                                        class="sm:mx-auto sm:max-w-xl lg:mx-0">
                                        <div class="sm:flex">
                                            <div class="min-w-0 flex-1">
                                                <label
                                                    for="email"
                                                    class="sr-only"
                                                    >Correo electrónico</label
                                                >
                                                <input
                                                    id="email"
                                                    type="email"
                                                    placeholder="Ingresa tu email"
                                                    class="block w-full rounded-md border-0 px-4 py-3 text-base text-gray-900 placeholder-gray-500 focus:outline-none focus:ring-2 focus:ring-indigo-300 focus:ring-offset-2 focus:ring-offset-gray-900" />
                                            </div>
                                            <div class="mt-3 sm:mt-0 sm:ml-3">
                                                <button
                                                    type="submit"
                                                    class="block w-full rounded-md bg-indigo-500 py-3 px-4 font-medium text-white shadow hover:bg-indigo-600 focus:outline-none focus:ring-2 focus:ring-indigo-300 focus:ring-offset-2 focus:ring-offset-gray-900">
                                                    Enviar
                                                </button>
                                            </div>
                                        </div>
                                        <p
                                            class="mt-3 text-sm text-gray-300 sm:mt-4">
                                            Si estas interesado en algunos de
                                            nuestros servicios, dejanos tu
                                            correo.
                                        </p>
                                    </form>
                                </div>
                            </div>
                        </div>
                        <div class="mt-12 -mb-16 sm:-mb-48 lg:relative lg:m-0">
                            <div
                                class="mx-auto max-w-md px-4 sm:max-w-2xl sm:px-6 lg:max-w-none lg:px-0">
                                <!-- Illustration taken from Lucid Illustrations: https://lucid.pixsellz.io/ -->
                                <img
                                    class="w-full lg:absolute lg:inset-y-0 lg:left-0 lg:h-full lg:w-auto lg:max-w-none"
                                    src="https://tailwindui.com/img/component-images/cloud-illustration-indigo-400.svg"
                                    alt="" />
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- More main page content here... -->
        </main>
    </div>

    <!-- About us -->
    <div class="relative bg-gray-800">
        <div
            class="h-56 bg-indigo-600 sm:h-72 md:absolute md:left-0 md:h-full md:w-1/2">
            <img
                class="h-full w-full object-cover"
                src="https://images.unsplash.com/photo-1525130413817-d45c1d127c42?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1920&q=60&blend=6366F1&sat=-100&blend-mode=multiply"
                alt="" />
        </div>
        <div
            class="relative mx-auto max-w-7xl px-4 py-12 sm:px-6 lg:px-8 lg:py-16">
            <div class="md:ml-auto md:w-1/2 md:pl-10">
                <h2
                    class="text-base font-semibold uppercase tracking-wider text-gray-300">
                    Quienes somos
                </h2>
                <p
                    class="mt-3 text-3xl font-extrabold tracking-tight text-white sm:text-4xl">
                    Somos una empresa joven.
                </p>
                <p class="mt-3 text-lg text-gray-300">
                    Nuestro equipo está compuesto por profesionales jovenes,
                    expertos en cada una de sus áreas de conocimiento.
                </p>
                <p
                    class="mt-2 text-3xl font-extrabold tracking-tight text-white sm:text-4xl">
                    Nuestro objetivo
                </p>
                <p class="mt-3 text-lg text-gray-300">
                    Ayudar a compañias de distinto rubro a mejorar la toma de
                    decisiones explorando y explotando su información, así como
                    también contribuimos en la mejora y optimización de procesos
                    por medio de distintas tecnologías.
                </p>
                <div class="mt-8">
                    <div class="inline-flex rounded-md shadow">
                        <a
                            href="#"
                            class="inline-flex items-center justify-center rounded-md border border-transparent bg-white px-5 py-3 text-base font-medium text-gray-900 hover:bg-gray-50">
                            Contactanos
                            <ExternalLinkIcon
                                class="-mr-1 ml-3 h-5 w-5 text-gray-400"
                                aria-hidden="true" />
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Features -->
    <div class="overflow-hidden bg-gray-50">
        <div class="relative mx-auto max-w-7xl py-12 px-4 sm:px-6 lg:px-8">
            <svg
                class="absolute top-0 left-full -translate-x-1/2 -translate-y-3/4 transform lg:left-auto lg:right-full lg:translate-x-2/3 lg:translate-y-1/4"
                width="404"
                height="784"
                fill="none"
                viewBox="0 0 404 784"
                aria-hidden="true">
                <defs>
                    <pattern
                        id="8b1b5f72-e944-4457-af67-0c6d15a99f38"
                        x="0"
                        y="0"
                        width="20"
                        height="20"
                        patternUnits="userSpaceOnUse">
                        <rect
                            x="0"
                            y="0"
                            width="4"
                            height="4"
                            class="text-gray-200"
                            fill="currentColor" />
                    </pattern>
                </defs>
                <rect
                    width="404"
                    height="784"
                    fill="url(#8b1b5f72-e944-4457-af67-0c6d15a99f38)" />
            </svg>

            <div class="relative lg:grid lg:grid-cols-3 lg:gap-x-8">
                <div class="lg:col-span-1">
                    <h2
                        class="text-3xl font-extrabold tracking-tight text-gray-900 sm:text-4xl">
                        ¿Que hacemos?
                    </h2>
                </div>
                <dl
                    class="mt-10 space-y-10 sm:grid sm:grid-cols-2 sm:gap-x-8 sm:gap-y-10 sm:space-y-0 lg:col-span-2 lg:mt-0">
                    <div v-for="feature in features" :key="feature.name">
                        <dt>
                            <div
                                class="flex h-12 w-12 items-center justify-center rounded-md bg-indigo-500 text-white">
                                <component
                                    :is="feature.icon"
                                    class="h-6 w-6"
                                    aria-hidden="true" />
                            </div>
                            <p
                                class="mt-5 text-lg font-medium leading-6 text-gray-900">
                                {{ feature.name }}
                            </p>
                        </dt>
                        <dd class="mt-2 text-base text-gray-500">
                            {{ feature.description }}
                        </dd>
                    </div>
                </dl>
            </div>
        </div>
    </div>

    <!-- Logos -->
    <div class="bg-white">
        <div class="mx-auto max-w-7xl py-12 px-4 sm:px-6 lg:py-16 lg:px-8">
            <p
                class="text-center text-base font-semibold uppercase tracking-wider text-gray-600">
                Quienes confían en nosotros
            </p>
            <div class="mt-6 grid grid-cols-2 gap-0.5 md:grid-cols-3 lg:mt-8">
                <div
                    class="col-span-1 flex justify-center bg-gray-50 py-8 px-8">
                    <img
                        class="max-h-24 grayscale"
                        src="/rc.png"
                        alt="Redcapital" />
                </div>
                <div
                    class="col-span-1 flex justify-center bg-gray-50 py-8 px-8">
                    <img
                        class="max-h-24 grayscale"
                        src="/renca.png"
                        alt="Renca" />
                </div>
                <div
                    class="col-span-1 flex justify-center bg-gray-50 py-8 px-8">
                    <img class="max-h-24 grayscale" src="vets.png" alt="Vets" />
                </div>
                <div
                    class="col-span-1 flex justify-center bg-gray-50 py-8 px-8">
                    <img
                        class="max-h-24 grayscale"
                        src="/corpo.png"
                        alt="Corporacion renca" />
                </div>
                <div
                    class="col-span-1 flex justify-center bg-gray-50 py-8 px-8">
                    <img
                        class="max-h-24 grayscale"
                        src="/daily.png"
                        alt="Dailyfresh" />
                </div>
                <div
                    class="col-span-1 flex justify-center bg-gray-50 py-8 px-8">
                    <img
                        class="max-h-24 grayscale"
                        src="/gimo.png"
                        alt="Gimo" />
                </div>
            </div>
        </div>
    </div>

    <!-- Contact -->
    <div class="relative bg-gray-50">
        <div class="absolute inset-0">
            <div class="absolute inset-y-0 left-0 w-1/2 bg-gray-50" />
        </div>
        <div class="relative mx-auto max-w-7xl lg:grid lg:grid-cols-5">
            <div
                class="bg-gray-50 py-16 px-4 sm:px-6 lg:col-span-2 lg:px-8 lg:py-24 xl:pr-12">
                <div class="mx-auto max-w-lg">
                    <h2
                        class="text-2xl font-extrabold tracking-tight text-gray-900 sm:text-3xl">
                        Contactanos
                    </h2>
                    <p class="mt-3 text-lg leading-6 text-gray-500">
                        Si tienes alguna idea en mente, o necesitas que te
                        asesoremos, escribenos y nuestro equipo se pondra en
                        contacto contigo
                    </p>
                    <dl class="mt-8 text-base text-gray-500">
                        <div>
                            <dt class="sr-only">Postal address</dt>
                            <dd>
                                <p>Guardia Vieja 202</p>
                                <p>Providencia, Santiago</p>
                            </dd>
                        </div>
                        <div class="mt-6">
                            <dt class="sr-only">Phone number</dt>
                            <dd class="flex">
                                <PhoneIcon
                                    class="h-6 w-6 flex-shrink-0 text-gray-400"
                                    aria-hidden="true" />
                                <span class="ml-3"> +569 508 40 507 </span>
                            </dd>
                        </div>
                        <div class="mt-3">
                            <dt class="sr-only">Email</dt>
                            <dd class="flex">
                                <MailIcon
                                    class="h-6 w-6 flex-shrink-0 text-gray-400"
                                    aria-hidden="true" />
                                <span class="ml-3"> contacto@agilitic.cl </span>
                            </dd>
                        </div>
                    </dl>
                    <!--<p class="mt-6 text-base text-gray-500">
                        Buscas alguna ?
                        {{ " " }}
                        <a href="#" class="font-medium text-gray-700 underline"
                            >View all job openings</a
                        >.
                    </p>-->
                </div>
            </div>
            <div
                class="bg-gray-50 py-16 px-4 sm:px-6 lg:col-span-3 lg:py-24 lg:px-8 xl:pl-12">
                <div class="mx-auto max-w-lg lg:max-w-none">
                    <form
                        action="#"
                        method="POST"
                        class="grid grid-cols-1 gap-y-6">
                        <div>
                            <label for="full-name" class="sr-only"
                                >Nombre</label
                            >
                            <input
                                type="text"
                                name="full-name"
                                id="full-name"
                                autocomplete="name"
                                class="block w-full rounded-md border-gray-300 py-3 px-4 placeholder-gray-500 shadow-sm focus:border-indigo-500 focus:ring-indigo-500"
                                placeholder="Tu nombre completo" />
                        </div>
                        <div>
                            <label for="email" class="sr-only">Email</label>
                            <input
                                id="email"
                                name="email"
                                type="email"
                                autocomplete="email"
                                class="block w-full rounded-md border-gray-300 py-3 px-4 placeholder-gray-500 shadow-sm focus:border-indigo-500 focus:ring-indigo-500"
                                placeholder="Tu correo electrónico" />
                        </div>
                        <div>
                            <label for="phone" class="sr-only">Telefono</label>
                            <input
                                type="text"
                                name="phone"
                                id="phone"
                                autocomplete="tel"
                                class="block w-full rounded-md border-gray-300 py-3 px-4 placeholder-gray-500 shadow-sm focus:border-indigo-500 focus:ring-indigo-500"
                                placeholder="Telefono" />
                        </div>
                        <div>
                            <label for="message" class="sr-only">Mensaje</label>
                            <textarea
                                id="message"
                                name="message"
                                rows="4"
                                class="block w-full rounded-md border border-gray-300 py-3 px-4 placeholder-gray-500 shadow-sm focus:border-indigo-500 focus:ring-indigo-500"
                                placeholder="Escribe aquí tu mensaje" />
                        </div>
                        <div>
                            <button
                                type="submit"
                                class="inline-flex justify-center rounded-md border border-transparent bg-indigo-600 py-3 px-6 text-base font-medium text-white shadow-sm hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2">
                                Enviar
                            </button>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="bg-gray-800" aria-labelledby="footer-heading">
        <h2 id="footer-heading" class="sr-only">Footer</h2>
        <div class="mx-auto max-w-7xl py-12 px-4 sm:px-6 lg:py-16 lg:px-8">
            <div
                class="mt-8 border-t border-gray-700 pt-8 md:flex md:items-center md:justify-between">
                <div class="flex space-x-6 md:order-2">
                    <a
                        v-for="item in social"
                        :key="item.name"
                        :href="item.href"
                        class="text-gray-400 hover:text-gray-300">
                        <span class="sr-only">{{ item.name }}</span>
                        <component
                            :is="item.icon"
                            class="h-6 w-6"
                            aria-hidden="true" />
                    </a>
                </div>
                <p class="mt-8 text-base text-gray-400 md:order-1 md:mt-0">
                    &copy; 2020 Agilitic. Todos los derechos reservados.
                </p>
            </div>
        </div>
    </footer>
</template>
