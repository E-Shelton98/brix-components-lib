<template>
    <header class="header-light">
        <nav class="header-navbar">
            <div class="container-f">
                <a class="header-brand" href="">Brand</a>
                <div class="nav-list">
                    <a class="nav-link" href="#">Home</a>
                    <a class="nav-link" href="">About</a>
                    <a class="nav-link" href="">Contact</a>
                    <a class="nav-link" href="">Info</a>
                    <form class="nav-form">
                        <input class="search-1" type="search" placeholder="Search">
                        <button class="btn-1" type="submit">Search</button>
                    </form>
                </div>
            </div>
        </nav>
    </header>
</template>

<script>
export default {
    name: "brix-header-one",
}
</script>

<style scoped lang="scss">
    .header-light {
        box-sizing: border-box;
        display: block;
        width: 100%;
        background: $light;
        padding: .5rem;
    }
    .header-dark {
        box-sizing: border-box;
        display: block;
        width: 100%;
        background: $dark;
        text-align: center;
    }
    .container-f {
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
    }
    .header-brand {
        font-size: 25px;
        padding: .25em;
        text-decoration: none;
        color: black;
    }
    .nav-list {
        width: 70%;
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        align-items: center;
        
    }
    .nav-link {
        text-decoration: none;
        color: gray;
    }
    .nav-link:hover {
        color: black;
    }
    .nav-form {
        display: flex;
        justify-content: space-between;
        width: auto;
    }
    .search-1 {
        margin-right: 4px;
    }
    .search-1:focus {
        outline:  green solid 2px;
    }
</style>