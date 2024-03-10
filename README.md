# Create-a-Repository
Main reference: https://blog.csdn.net/qq_44998513/article/details/133828886
# Step1. Create SSH keys
1. 登陆Github官网 -> 头像 -> Settings -> SSH and GPG keys-> New SSH key
![image](https://github.com/DaydayXtt/Create-a-Repository/blob/main/pics/Quick%20start.png)
2. **Title** isn't matter. **Key type** is Authentication Key.

3. Type in "ssh-keygen -t rsa -C YOUR_EMAIL in Terminal:
    ssh-keygen -t rsa -C YOUR_EMAIL
"YOUR_EMAIL" is the E-mail of your account.

4. 前往 ~/.ssh/id_rsa.pub文件，将其中的内容复制到“1.”中的 **Key** :

5. 设置本地 git 的用户名和邮箱，Terminal输入(保留双引号 **""** )：
    git config --global user.name "yourname"
    git config --global user.email "email@email.com"
6.Type in "ssh -T git@github.com" in Termial:
    ssh -T git@github.com
提示如下信息，说明成功连接Github。

否则，输入以下内容，再重新连接：
    ssh-agent -s
    ssh-add ~/.ssh/id_rsa

# Step2. Upload project to Github
1. 登陆Github官网 -> 头像 -> Settings