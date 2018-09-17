# 安装

- https://www.cnblogs.com/Leo_wl/p/7821254.html#_label0
- https://blog.csdn.net/zhou8572/article/details/54410771

# 解决lua5.3安装luasocket问题

- https://github.com/diegonehab/luasocket/issues/124

## 修改luasocket源码

mime.c与luasocket.c中需要加入下列代码

    #ifndef luaL_checkint
    #define luaL_checkint(L, n) ((int)luaL_checkinteger(L,n))
    #endif

    make macosx install-both
