# Create-a-Repository
Main reference: https://blog.csdn.net/qq_44998513/article/details/133828886
# Step1. Create SSH keys
1. 登陆Github官网 -> 头像 -> Settings -> SSH and GPG keys-> New SSH key
![image](https://github.com/DaydayXtt/Create-a-Repository/blob/main/pics/SSH_1.png)
一般为空，此处作者先前已经配置。

2. **Title** isn't matter. **Key type** is Authentication Key.
![image](https://github.com/DaydayXtt/Create-a-Repository/blob/main/pics/SSH_2.png)

3. Type in "ssh-keygen -t rsa -C YOUR_EMAIL in Terminal:
    ssh-keygen -t rsa -C YOUR_EMAIL
"YOUR_EMAIL" is the E-mail of your account.

4. 前往 ~/.ssh/id_rsa.pub文件，将其中的内容复制到“1.”中的 **Key** :
![image](https://github.com/DaydayXtt/Create-a-Repository/blob/main/pics/SSH_3.png)

5. 设置本地 git 的用户名和邮箱，Terminal输入(保留双引号 **""** )：
    git config --global user.name "yourname"
    git config --global user.email "email@email.com"
6.Type in "ssh -T git@github.com" in Termial:
    ssh -T git@github.com
提示如下信息，说明成功连接Github。
![image](https://github.com/DaydayXtt/Create-a-Repository/blob/main/pics/SSH_4.png)

否则，输入以下内容，再重新连接：
    ssh-agent -s
    ssh-add ~/.ssh/id_rsa

# Step2. Upload project to Github
1. 登陆Github官网 -> 头像 -> Settings -> Your repositories -> New
![image](https://github.com/DaydayXtt/Create-a-Repository/blob/main/pics/Git_1.png)
Enter your **Repository name** and the corresponding **Description** .
The others are default.

2. Click **Create repository** , 弹出如下界面：
![image](https://github.com/DaydayXtt/Create-a-Repository/blob/main/pics/Quick%20start.png)

3. 定位到文件加目录。Copy the following codes and fix to your project's name in Terminal:
    echo "# project_name" >> README.md
    git init
    git add README.md
    git commit -m "first commit"
    git branch -M main
    git remote add origin git@github.com:xygxgn/project_name.git
    git push -u origin main

4. 刷新Github官网，发现 **README.md** 已上传成功
![image](https://github.com/DaydayXtt/Create-a-Repository/blob/main/pics/Git_2.png)

5. 若要上传文件夹中所有文件，输入以下：
    git add . 
    git commit -m "first commit"
    git push -u origin main
    