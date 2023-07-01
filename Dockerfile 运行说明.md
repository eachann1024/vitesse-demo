1. 把@nginx.conf 放到项目根目录 (package.json 同一层级)

    [nginx.conf](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4876ba4c-6b44-4850-9145-8766334da116/nginx.conf)
    
2. 使用 Vitesse 项目自带的`Dockerfile` (没有后缀名)  
    
    [Dockerfile](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c6fc18f5-8e53-40aa-8c91-51cc9bcf6ea4/Dockerfile.txt)
    
3. 终端 `docker pull nginx:nginx:stable-alpine` (根据 `Dockerfile` 文件提到的版本来)
4. 终端 `docker build -t vite-web:v1 .`  

---

<aside>
😶‍🌫️ 其实 5,6,7 步可以直接在 `Dockerfile` 软件界面执行

</aside>

1. 构建完成后 终端 `docker images` 可以看到 **vite-web:v1** 镜像已经在 image 的列表中
2. 终端 `docker run -d --name my-web-1 -p 8080:80 vite-web:v1`
3. `docker ps` 查看正在运行的列表