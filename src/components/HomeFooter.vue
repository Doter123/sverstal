<template>
    <footer>
        <i class="fa-brands fa-instagram text-white" style="font-size: 30px;margin-left: 30px;"></i>
        <i class="fa-brands fa-whatsapp text-white" style="font-size: 30px;margin-left: 30px;"></i>
        <span style="padding-right: 90px;">Ak-Danis - since 2006</span>
    </footer>
</template>

<style>


footer {
    margin-top: 50px;
    height: 111px;
    background: #222222;
    display: flex;
    align-items: center;
}

footer span {
    margin: auto;

    font-family: 'IslandMoments';
    font-style: normal;
    font-weight: 400;
    font-size: 36px;
    line-height: 41px;
    display: flex;
    align-items: center;
    text-align: center;

    color: #FFFFFF;
}


@media (max-width: 600px) {
    svg {
        margin-left: 15px !important;
    }
    footer {
        height: 81px;
    }
    footer span {
        padding-right: 0 !important;
    }
}

@media (max-width: 424px) {
    svg {
        font-size: 23px !important;
        margin-left: 10px !important;
    }
    footer {
        height: 70px;
    }
    footer span {
        font-size: 30px;
        padding-right: 10px !important;
        padding-left: 10px !important;
        line-height: 20px;
    }
}


</style>