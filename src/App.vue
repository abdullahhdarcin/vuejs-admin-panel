<template>
 <el-badge :value="12" class="item">
    <el-button size="small">comments</el-button>
  </el-badge>
  <el-badge :value="3" class="item">
    <el-button size="small">replies</el-button>
  </el-badge>
  <el-badge :value="1" class="item" type="primary">
    <el-button size="small">comments</el-button>
  </el-badge>
  <el-badge :value="2" class="item" type="warning">
    <el-button size="small">replies</el-button>
  </el-badge>

  <el-dropdown trigger="click">
    <span class="el-dropdown-link">
      Click Me<i class="el-icon-caret-bottom el-icon--right"></i>
    </span>
    <template #dropdown>
      <el-dropdown-menu>
        <el-dropdown-item class="clearfix">
          comments
          <el-badge class="mark" :value="12" />
        </el-dropdown-item>
        <el-dropdown-item class="clearfix">
          replies
          <el-badge class="mark" :value="3" />
        </el-dropdown-item>
      </el-dropdown-menu>
    </template>
  </el-dropdown>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div>
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

.item {
  margin-top: 10px;
  margin-right: 40px;
}
</style>
