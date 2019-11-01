<template>
    <!-- <select name="dropdown" id="dropdown" v-model="selectedOption" v-on:change="optionChanged">
        <option value="null" disabled><span>MEIN BEREICH</span></option>
        <option value="My published jokes"><span>My published jokes</span></option>
        <option value="My saved jokes"><span>My saved jokes</span></option>
        <option value="Account Information"><span>Account Information</span></option>
        <option value="Publish new joke"><span>Publish new joke</span></option>
    </select> -->
    <div class="dropdown">
        <button type="button" @click="toggleDropdown" class="dropdown-button">
            <img class="personImage" src="../assets/Images/shape.png"/>
            <span> MEIN BEREICH </span>
            <img src="../assets/Images/path_2.png" />
            </button>
        <div class="dropdown-items" id="myDropdown">
            <a href="#">Item 1</a>
            <a href="#">Item 2</a>
            <a href="#">Item 3</a>
        </div>
    </div>
</template>

<script>
export default {
    name: "Dropdown",
    data() {
        return {
            showDropDown: true,
            links: [
                {id: "1", name: "Link 1" },
                {id: "2", name: "Link 2" },
                {id: "3", name: "Link 3" },
                {id: "4", name: "Link 4" },
            ]
        };
    },
    methods: {
        toggleDropdown: function() {
            var menuList = document.getElementById("myDropdown").children;
            for (let i = 0; i < menuList.length; i++) {
                menuList[i].style.display="block";
                
            }
            document.getElementById("myDropdown").classList.toggle("show");
        }
    }
    
}
</script>

<style lang="scss" scoped>

.dropdown .dropdown-button {
    font-family: inherit;
    background-color: #cfb995;
    color: white;
    width: 222px;
    height: 60px;
    display: flex;
    justify-content: space-around;
}

.dropdown-items {
  display: none;
}
.show {
    display: block;
}

</style>