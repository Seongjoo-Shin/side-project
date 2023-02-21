<template>
    <header class="app-header">
        <div class="logo">
            <img src="/path/to/logo.png" alt="Logo" />
        </div>
        <nav class="nav-links">
            <ul>
                <li>
                    <router-link to="/">Home</router-link>
                </li>
                <li>
                    <router-link to="/about">About</router-link>
                </li>
                <li>
                    <router-link to="/posts">Posts</router-link>
                </li>
                <li>
                    <router-link to="/contact">Contact</router-link>
                </li>
            </ul>
        </nav>
        <div class="search-bar">
            <input type="text" placeholder="Search" />
            <button>Search</button>
        </div>
    </header>
</template>

<style scoped>
.app-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 60px;
    padding: 0 20px;
    background-color: #ffffff;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.logo img {
    height: 40px;
}

.nav-links ul {
    display: flex;
    list-style: none;
    margin: 0;
    padding: 0;
}

.nav-links li {
    margin-right: 20px;
}

.nav-links li:last-child {
    margin-right: 0;
}

.nav-links a {
    color: #333333;
    text-decoration: none;
    font-size: 16px;
}

.nav-links a:hover {
    color: #007bff;
}

.search-bar {
    display: flex;
    align-items: center;
}

.search-bar input[type='text'] {
    border: none;
    background-color: #f2f2f2;
    padding: 10px;
    font-size: 16px;
}

.search-bar button {
    border: none;
    background-color: #007bff;
    color: #ffffff;
    padding: 10px 20px;
    margin-left: 10px;
    cursor: pointer;
    font-size: 16px;
}

.search-bar button:hover {
    background-color: #0056b3;
}
</style>
