<template>
    <header>
        <nav>
            <ul class="topLeft">
                <li><img src="data:image/png;base64,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" alt=""></li>
                <li class="brandname">Adilo</li>
            </ul>
            <ul class="topCenter">
                <li class="active">projects</li>
                <div class="dropdown">
                <li @onclick="myFunction()" class="dropbtn">Apps and Tools</li>
                <div id="myDropdown" class="dropdown-content">
                    <a href="#home">Home</a>
                    <a href="#about">About</a>
                    <a href="#contact">Contact</a>
                </div>
                </div>
                <li>channels</li>
                <li>contacts</li>
                <li>analytics</li>
                <li>settings</li>
            </ul>
            <ul class="topRight">
                <li>Help</li>
                <li class="stroke">|</li>
                <li><img src="https://media.istockphoto.com/photos/studio-portrait-of-a-smiling-young-latin-woman-picture-id1357723739?b=1&k=20&m=1357723739&s=170667a&w=0&h=TocMmpiVPhpoCekB2a4MQNi87Sc6yqR0s8b7MK9vXNA=" alt=""></li>
                <li class="person-info">
                    <span class="person-name">Cody Fisher</span>
                    <span class="person-website">codyfisherweb.com</span>
                </li>
            </ul>
        </nav>
    </header>
</template>

<script>
    export default {
        name: 'Header',
        props: ['title'],

        methods: {
            myFunction() {
            document.getElementById("myDropdown").classList.toggle("show");
            window.onclick = function(event) {
            if (!event.target.matches('.dropbtn')) {
                var dropdowns = document.getElementsByClassName("dropdown-content");
                var i;
                for (i = 0; i < dropdowns.length; i++) {
                var openDropdown = dropdowns[i];
                if (openDropdown.classList.contains('show')) {
                    openDropdown.classList.remove('show');
                }
                }
            }
            }
            } 
        }
        
        }
</script>   

<style scope>
    header {
        width: 100%;
        background-color: white;
        height: 50px;
        position: sticky;
        display: flex;
        align-items: center;
        font-family: 'Josefin Sans', sans-serif; 
        z-index: 999;
        border-bottom: 2px solid rgb(214, 206, 206);
    }
    header nav {
        display: flex;
        width: 100%;
        height: 100%;
        top: 50%;
        align-items: center;
    }
    nav ul {
        display: flex;
        list-style: none;
        justify-content: space-between;
        margin: 0;
        padding: 0;
        list-style: none;
    }
    
    li img {
        height: 40px;
        width: 50px;
        border-radius: 30%;
        margin-left: 10px;
        object-fit: cover;
    }
    .topLeft, .topRight {
    flex:3;
    display: flex;
    align-items: center;
    justify-content: center;
    }
    .brandname {
        margin-left: 5px;
        font-size: 20px;
        font-weight: 700;
    }
    .person-info {
        display: flex;
        flex-direction: column;
    }
    .person-name {
        font-size: 15px;
        font-weight: 800;
    }
    .person-website {
        color: rgb(114, 114, 223);
    }
.topCenter {
    flex: 5;
}
.stroke {
    margin-left: 5px;
}
li.active {
    border-top: 3px solid rgb(116, 85, 232);
}
.dropbtn {
  border: none;
  cursor: pointer;
}

.dropdown {
  position: relative;
  display: inline-block;
}

.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f1f1f1;
  min-width: 160px;
  overflow: auto;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  z-index: 1;
}

.dropdown-content a {
  color: black;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
}

.dropdown a:hover {background-color: #ddd;}

.show {display: block;}
</style>
 