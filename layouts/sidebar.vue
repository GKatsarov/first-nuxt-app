<template>
    <main class="user-layout">
    <article class="sidebar">
        <p>Dashboard</p>
        <p>Settings</p>
    </article>
    <br/>
    <hr/>

    <slot></slot>
    </main>
</template>

<style>
.sidebar {
    display: flex;
    flex-direction: column;
}
</style>