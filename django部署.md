1. 从github下载项目源代码

   `git clone https://github.com/allenmitnick/shopsport.git`

2. 创建数据库

   `create database market charset utf8;`

3. 安装依赖

   `pip3 install -i https://pypi.douban.com/simple django==2.0`

   `pip3 install pymysql`

   `pip3 install -i https://pypi.douban.com/simple Pillow`

4. 生成表（切换到项目目录 含有manage.py的同目录下）

   #生成django默认需要的表

   `python3 manage.py makemigrations`

   `python3 manage.py migrate`
   
   #生成每个app的表  appname=market
   
   `python3 manage.py makemigrations market`
   
   `python3 manage.py migrate market`



5. 收集静态资源

   创建文件夹  static

   从STATICFILES_DIRS配置的文件夹里复制到 STATIC_ROOT

   `python3 manage.py collectstatic`

   收集资源时可能需要临时将STATIC_ROOT = os.path.join(BASE_DIR, '/static/')改为

   STATIC_ROOT = os.path.join(BASE_DIR, 'static')

   

6. 创建管理员账号

   `python manage.py createsuperuser`

   

7. 启动调试服务器

   `python manage.py runserver 0.0.0.0:8000`

   

    

   

   

   

   

   

   

   

   

   

   

   

   