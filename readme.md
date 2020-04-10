基于Django开发的注册登录页面
## 路由设置：

from django.contrib import admin
from django.urls import path, include
from login import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('index/', views.index),
    path('login/', views.login),
    path('register/', views.register),
    path('logout/', views.logout),
    path('confirm/', views.user_confirm),
    path('captcha/', include('captcha.urls'))   
]



## settings配置：

1. 在INSTALLED_APPS中添加‘login’，'captcha'
2. 默认使用Sqlite数据库
3. LANGUAGE_CODE = 'zh-hans'
4. TIME_ZONE = 'Asia/Shanghai'
5. USE_TZ = False