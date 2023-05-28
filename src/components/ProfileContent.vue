<template>
    <div class="flex profile-container">
        <div class="profile">
            <h3>PROFILE</h3>
            <div class="flex">
                <img src="../assets/profile-black.png" class="profile-black-img" alt="">
                <div class="profile-info flex flex-col">
                    <input type="text" value="Иван Иванов">
                    <input type="email" value="ivaninvanov@mail.com">
                    <input type="tel" value="+0 (848) 894-32-32">
                    <input type="text" value="Возраст: 18">
                    <input type="text" value="Дата рождения: 08.12.2001">
                </div>
            </div>
        </div>
        <div class="profile">
            <h3>BOOKINGS</h3>
            <div class="booking-table">
                <table class="w-full">
                    <tr>
                        <th>STATUS</th>
                        <th>CHECK-IN</th>
                        <th>CHECK-OUT</th>
                        <th>ROOM</th>
                        <th>PRICE</th>
                        <th>&nbsp;</th>
                    </tr>
                    <tr>
                        <td>NEW</td>
                        <td>01.02.2023</td>
                        <td>10.02.2023</td>
                        <td>DELUX</td>
                        <td class="booking-td-price">270 $</td>
                        <td class="border-none"><i class="fa-solid fa-pen"></i></td>
                    </tr>
                    <tr>
                        <td>CANCELED</td>
                        <td>01.02.2023</td>
                        <td>10.02.2023</td>
                        <td>DELUX</td>
                        <td class="booking-td-price">270 $</td>
                        <td class="border-none"></td>
                    </tr>
                    <tr>
                        <td>CONFIRMED</td>
                        <td>01.02.2023</td>
                        <td>10.02.2023</td>
                        <td>DELUX</td>
                        <td class="booking-td-price">270 $</td>
                        <td class="border-none"><i class="fa-solid fa-pen"></i></td>
                    </tr>
                    <tr>
                        <td class="border-none">ACTIVE</td>
                        <td class="border-none">01.02.2023</td>
                        <td class="border-none">10.02.2023</td>
                        <td class="border-none">DELUX</td>
                        <td class="border-none booking-td-price">270 $</td>
                        <td class="border-none"><i class="fa-solid fa-pen"></i></td>
                    </tr>
                </table>
            </div>
        </div>
    </div>
</template>

<style>

h3 {
    font-family: 'Inter';
    font-weight: 600;
    font-size: 1.8em;
    line-height: 24px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: .625em;
}

.profile {
    width: 50%;
    margin-top: 2em;
}
.profile > div {
    padding-top: 2.1875em;
}
.profile-black-img {
    margin: 0 2.2em auto;
}
.profile-info input {
    background: transparent;
    border: none;
    border-bottom: 1px solid #8CAA14;
    /*width: 342px;*/
    height: 1.5em;
    
    font-family: 'Inter';
    font-weight: 500;
    font-size: 1.3em;

    margin-bottom: 2.1875em;
}
.profile-info input:focus {
    outline: none !important;
}
.booking-table {
    border-left: 1px solid #3A3943;
    padding: 1.875em 0.625em 1.875em 1.875em;
}

th {
    
    text-align: center;
    font-family: 'Inter';
    font-weight: 600;
    font-size: 12px;

    color: #5C5C5C;
}
.booking-td-price {
    border-left: 1px solid #8CAA14;
}
td {
    height: 4.2em;
    text-align: center;
    border-bottom: 1px solid #8CAA14;

    font-family: 'Inter';
    font-weight: 600;
    font-size: 1.125em;
}

.fa-pen {
    width: 1.2em;
    height: 1.2em;
    color: #8CAA14;
    cursor: pointer;
}

@media (max-width: 1050px) {
    .profile-container {
        flex-wrap: wrap !important;
    }
    .profile-container > .profile {
        width: 100%;
    }
    .profile-container > .profile > .flex {
        justify-content: center;
    }
}

@media (max-width: 680px) {
    .profile-container {
        font-size: 10px !important;
    }
}
@media (max-width: 430px) {
    .profile-container {
        font-size: 9px !important;
    }
    .profile-container .fa-pen {
        height: .8em !important;
        width: 1.2em !important;
    }
    .profile-black-img {
        max-width: 110px;
        margin-left: 0;
    }
}
@media (max-width: 380px) {
    .profile-container {
        font-size: 8px !important;
    }
    .profile-container .fa-pen {
        height: .8em !important;
        width: 1.2em !important;
    }
    .booking-table {
        padding: 1em 0.45em 1em 1em;
    }
    
    .profile-container .border-none > svg {
        max-width: .7em !important;
        margin-left: 5px !important;
    }
}
</style>