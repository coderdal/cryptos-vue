<template>
  <header>

    <section class="header-top">

        <div class="brand">
            <router-link to="/">
                <h1>ErdalCoin</h1>
            </router-link>
        </div>

        <div class="stats">

            <div class="stat">
                <h4>9,450 USD</h4>
                <p>Last trade price</p>
            </div>
            <div class="stat">
                <h4>+5.26%</h4>
                <p>24 hour price</p>
            </div>
            <div class="stat">
                <h4>9,12.820 BTC</h4>
                <p>24 hour volume</p>
            </div>
            
            <div class="stat">
                <h4>2,231,775</h4>
                <p>active traders</p>
            </div>
                        
            <div class="stat">
                <h4 class="top">$23855.66</h4>
                <p>Live Bitcoin price</p>
            </div>

        </div>

    </section>

    <section class="header-bottom">

    </section>

  </header>
</template>

<script>
export default {
name: "headerMain"
}
</script>

<style scoped>

header{
    width: 100%;
    height: 140px;
    background: var(--container-bg-color);
}

/* header top */

header .header-top{
    height: 90px;
    width: 100%;
    padding: 15px 40px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
}

header .header-top .brand a{
    text-decoration: none;
    color: var(--text-color);
}

header .header-top .brand a h1{
    font-weight: 700;
}

header .header-top .brand a h1::first-letter{
    color: var(--orange-color);
    font-weight: 700;
    font-size: 1.3em;
}

/* stats */

header .header-top .stats{
    display: flex;
    flex-direction: row;
    gap: 20px;
}

header .header-top .stats .stat h4{
    font-size: 0.8em;
    color: var(--text-light-gray-color);
}

header .header-top .stats .stat .top{
    font-size: 0.8em;
    color: var(--orange-color);
    position: relative;
}

header .header-top .stats .stat .top::after{
    content: "";
    width: 24px;
    height: 24px;
    top: 50%;
    transform: translateY(-50%);
    position: absolute;
    background-image: url("data:image/svg+xml,%3Csvg clip-rule='evenodd' fill='green' stroke-linejoin='round' stroke-miterlimit='2' viewBox='0 0 24 24' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='m16.843 13.789c.108.141.157.3.157.456 0 .389-.306.755-.749.755h-8.501c-.445 0-.75-.367-.75-.755 0-.157.05-.316.159-.457 1.203-1.554 3.252-4.199 4.258-5.498.142-.184.36-.29.592-.29.23 0 .449.107.591.291 1.002 1.299 3.044 3.945 4.243 5.498z'/%3E%3C/svg%3E");
}

header .header-top .stats .stat p{
    font-size: 0.7em;
    color: var(--text-light-color);
}

/* header bottom */

header .header-bottom{
    height: 50px;
    width: 100%;
    background: red;
}

</style>