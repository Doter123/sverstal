<template>
    <header class="relative" style="margin-bottom: 5em;">
        <nav class="flex justify-between items-center">
            <div class="logo">AK-DANIS</div>
            <div class="navigation item-center">
                <router-link class="navigation-item" :class="{
                    active: $route.path == '/'
                }" to="/">HOME</router-link>
                <router-link class="navigation-item" :class="{
                    active: $route.path == '/room'
                }" to="/room">ROOMS</router-link>
                <router-link class="navigation-item" :class="{
                    active: $route.path == '/about'
                }" to="/about">ABOUT</router-link>
                <router-link class="navigation-item" :class="{
                    active: $route.path == '/bookings'
                }" to="/bookings">BOOKINGS</router-link>
            </div>
            <div class="flex items-center">
                <div class="lang">ENG</div>
                <img v-if="isAuthorized" src="../assets/profile.png" class="profile-icon" alt="">
                <div v-else class="login select-none" @click="$emit('showModal')">Login</div>
            </div>
        </nav>
        <div class="header-title"> Welcome to Issyk-Kul</div>
    </header>
    <div class="pos-a items-pos-a">
        <div class="items">
            <div class="item">
                <div>
                    <div class="item_name">CHECK-IN</div>
                    <div class="item_description"><img src="../assets/Check_Date.png" alt="">Check-In Date</div>
                </div>
            </div>
            <div class="item">
                <div>
                    <div class="item_name">CHECK-OUT</div>
                    <div class="item_description"><img src="../assets/Check_Date.png" alt="">Check-Out Date</div>
                </div>
            </div>
            <div class="item">
                <div>
                    <div class="item_name">ROOMS</div>
                    <!--<div class="item_description"><i class="fa-solid fa-angle-down"></i>Suits</div>-->
                    <div class="item_description">
                        <i class="fa-solid fa-angle-down"></i>
                        <select>
                            <option value="1">Suits</option>
                        </select>
                    </div>
                </div>
            </div>
            <div class="item">
                <div>
                    <div class="item_name">GUESTS</div>
                    <!--<div class="item_description"><i class="fa-solid fa-angle-down"></i>1 Person</div>-->
                    <div class="item_description">
                        <i class="fa-solid fa-angle-down"></i>
                        <select>
                            <option value="1">1 Person</option>
                        </select>
                    </div>
                </div>
            </div>
            <div class="item active" style="height: 7.5em !important">
                <div class="item_name">CHECK AVAILABILITY</div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        isAuthorized: {
            type: Boolean,
            default: false
        }
    }
}
</script>

<style>
header {
    width: 100%;
    height: 43.625em;
    background: url(../assets/picture-2.jpg) 0 0/cover no-repeat;
}

.navigation {
    display: flex;
}

.navigation-item {
    width: 5.5em;
    height: 3em;
    margin-right: 1em;

    font-family: 'Inter';
    font-size: 1.25em;
    line-height: 24px;
    display: flex;
    align-items: center;
    justify-content: center;

    color: #FFFFFF;
}

.navigation-item.active,
.navigation-item:hover {
    color: white;
    border-bottom: 1px solid white;
}

.logo {

    /*width: 215px;*/

    font-family: 'IslandMoments';
    font-size: 2.1em;
    line-height: 41px;
    display: flex;
    align-items: center;

    color: #FFFFFF;
    cursor: pointer;
    white-space: nowrap;
}

.lang {
    cursor: pointer;
    width: 5.2em;
    height: 45px;

    font-family: 'Inter';
    font-size: 1.5em;
    line-height: 29px;
    display: flex;
    align-items: center;
    justify-content: center;

    color: #FFFFFF;
}

.login {
    cursor: pointer;
    height: 50px;

    font-family: 'Inter';
    font-size: 1.5em;
    line-height: 29px;
    display: flex;
    align-items: center;
    justify-content: center;

    color: #FFFFFF;



    width: 5.2em;
    height: 2.3em;
    left: 1248px;
    top: 13px;

    background: rgba(0, 0, 0, 0.4);
    border-radius: 0.5em;
}

header {
    padding: 12px 40px;
}

.header-title {
    display: flex;
    align-items: center;
    justify-content: center;


    font-family: 'IslandMoments';
    font-size: 6em;
    line-height: 42px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: auto;
    height: 100%;
    padding-bottom: 75px;

    color: #FFFFFF;
    text-align: center;
}

.item_description select {
    padding-left: 0;
    background: transparent;
    border: none;
    
    font-size: 1.0625em;
}
.item_description {
    display: flex;

    font-family: 'Inter';
    font-style: normal;
    font-weight: 400;
    font-size: 1.0625em;
    line-height: 21px;
    display: flex;
    align-items: center;

    color: #5C5C5C;
    white-space: nowrap;
    overflow: hidden;
    height: 20px;
    margin-top: 5px;
}

.item_description img {
    width: 1.6em;
    margin-right: 4px;
}

.item_description svg {
    margin-right: 4px;
    padding-top: 6px;
}

.pos-a {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 15px 0;
    margin-top: -9.6875em;
}

.items {
    margin: auto;
    display: flex;
    align-items: center;
    justify-content: center;
}

.item {
    background: #000;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    width: 11.875em;
    height: 9.375em !important;
}

.item:not(.item.active) {
    padding-left: 15px;
}

.item.active {
    width: 10.5em;
    font-family: 'Inter';
    font-weight: 700;
    font-size: 1.25em;
    /*line-height: 24px;*/
    display: flex;
    align-items: center;
    text-align: center;
    background: #8CAA14;
    height: 9.375em !important;

}

.item_name {

    font-family: 'Inter';
    font-weight: 600;
    font-size: 1.25em;
    line-height: 24px;
    display: flex;
    align-items: flex-end;
    text-align: center;
}

.profile-icon {
    border-bottom: 1px solid white;
    width: 4.75em;
    height: 3.1875em;
    padding: 0 1.09375em 0.625em;
    cursor: pointer;
    user-select: none;
}

</style>