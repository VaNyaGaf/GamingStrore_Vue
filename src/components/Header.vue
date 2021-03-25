<template>
    <div class="header-wrapper">
        <div class="navigation topnav">
            <a class="active">Games</a>
            <a>News</a>
            <a>Log In</a>
            <a>Register</a>
        </div>
    </div>
</template>

<script>
export default {
  name: "Header",
  props: {
    msg: String
  }
};
</script>

<style scoped>
    .topnav {
        background-color: #333;
        overflow: hidden;
    }
    
    .topnav a {
        float: left;
        color: #f2f2f2;
        text-align: center;
        padding: 14px 16px;
        text-decoration: none;
        font-size: 17px;
    }

    .topnav a:hover {
        background-color: #ddd;
        color: black;
    }

    .topnav a.active {
        background-color: #4CAF50;
        color: white;
    }
</style>