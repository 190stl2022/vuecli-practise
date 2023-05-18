<template>
  <div class="row">
    <div class="col-4">
      <div class="list-group">
        <router-link to="/newpage/a" class="list-group-item list-group-item-action" aria-current="true">
          元件A
        </router-link>
        <router-link to="/newpage/b" class="list-group-item list-group-item-action" aria-current="true">
          元件B
        </router-link>
        <router-link to="/newpage/namedView/c2a" class="list-group-item list-group-item-action" aria-current="true">
          命名視圖 c2a
        </router-link>
        <router-link to="/newpage/namedView/a2b" class="list-group-item list-group-item-action" aria-current="true">
          命名視圖 a2b
        </router-link>
        <router-link to="/newpage/dynamicRouter/ec1ba3c2bb2496d7" class="list-group-item list-group-item-action" aria-current="true">
          動態路由($route)
        </router-link>
        <router-link to="/newpage/dynamicRouterByProps/:id" class="list-group-item list-group-item-action" aria-current="true">
          動態路由(Props)
        </router-link>
        <router-link to="/newpage/routerNavigation" class="list-group-item list-group-item-action" aria-current="true">
          路由方法
        </router-link>
      </div>
    </div>
    <div class="col-8">
      <router-view></router-view>
    </div>
  </div>
</template>
