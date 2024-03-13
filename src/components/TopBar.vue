<template>
    <nav class="navbar navbar-expand-lg my-txt-dark bg-white py-4">
        <div class="container position-relative">
            <!-- LEFT SECTION -->
            <div class="left-section">
                <a href="#"><img class="align-middle" src="../images/Logo.svg" alt="logo-nature-agency"></a>
                <a class="navbar-brand fs-3 mx-3 align-middle" href="#"><span class="fw-bold">Nature</span>
                    Agency</a>
            </div>
            <!-- toggle button -->
            <button class="navbar-toggler text-primary " type="button" data-bs-toggle="collapse"
                data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false"
                aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <!-- RIGHT SECTION -->
            <div class="collapse navbar-collapse fs-6  " id="navbarNav">
                <ul class="navbar-nav ms-auto mt-4">
                    <li class="nav-item mx-3" v-for="item in menu">
                        <a class="nav-link active" aria-current="page" href="#">{{ item }}</a>
                    </li>
                    <li class="mx-3 ">
                        <!-- search-bar -->
                        <div class="searchbar">
                            <input class="search_input" type="text" placeholder="Search...">
                            <a href="#" class="search_icon"> <i
                                    class="fa-solid fa-magnifying-glass p-1 rounded my-txt-dark fs-4"></i></a>
                        </div>
                    </li>
                    <li>
                        <!-- call to action -->
                        <button class="btn bg-primary rounded-5 py-3 text-white fw-light align-middle">
                            Contact us
                        </button>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
    name: "TopBar",
    data() {
        return {
            menu: [
                'Who we are',
                'Services',
                'Products',
                'Blog',
            ],
        }
    },
}
</script>

<style lang="scss" scoped>
@use './../assets/style/partials/variables' as *;

//Hover FX
.left-section {
    img {
        transition: 1s ease-in-out;
        cursor: pointer;

        &:hover {
            transform: scale(1.2);
        }
    }

    .navbar-brand {
        transition: 0.4s linear;

        &:hover {
            filter: drop-shadow(5px 6px 3px $blue);
        }
    }
}

//Button call to action
ul li:last-child {
    margin-top: 1rem;

    button {
        font-size: 0.8em;
        padding: 2rem;

        &:hover {
            background-color: #262626 !important;
        }
    }

}


//SearchBar Small Nav
.search_input {
    border: 0;
    outline: 0;
    width: 100px;
    margin: 1rem 0;
    padding: 0 !important;
    transition: width 0.4s linear;
}

.searchbar:hover>.search_input {
    border-bottom: 1px solid #262626;
    padding: 0 10px;
    width: 150px;
    transition: width 0.4s linear;
}


//MEDIA QUERY
@media (min-width: 992px) {
    ul {
        display: flex;
        align-items: center;
        margin-top: 0 !important;

        li {
            transition: 0.4s linear;

            &:hover {
                transform: scale(1.2);
            }
        }
    }

    ul li:last-child {
        margin-left: 1rem;
        margin-top: 0px !important;


    }

    //SearchBar Large Nav
    .searchbar {
        margin-bottom: auto;
        margin-top: auto;
        height: 60px;
        border-radius: 30px;
        padding: 10px;
    }

    .search_input {
        border: 0;
        outline: 0;
        background: none;
        width: 0;
        caret-color: #262626;
        line-height: 40px;
        margin: 0 !important;
        transition: width 0.4s linear;
    }

    .searchbar:hover>.search_input {
        border-bottom: 1px solid #262626;
        padding: 0 10px;
        width: 100px;
        transition: width 0.4s linear;
    }

    .search_icon {
        height: 40px;
        width: 40px;
        float: right;
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 50%;
        color: white;
        text-decoration: none;
    }

}



//FIX Call to Action
@media (min-width: 992px) and (max-width: 1200px) {
    .left-section {
        min-width: 300px;
    }

    ul {
        display: flex;
        flex-wrap: wrap;
    }

    ul li {
        margin: 0 10px !important;
    }


}
</style>