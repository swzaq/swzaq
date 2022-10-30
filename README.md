# YJCMS file upload vulnerability

### 1. Vulnerability Background

Yunjing cms is developed by gansu yunjing digital technology co., ltd. YJcms (Cloudscape cms) is an open source PHP enterprise website building management system developed based on ThinkPaPHP5.0.24. Yjcms adheres to the concept of minimalist, fast and extreme development, integrates enterprise, tourism and mall modules for development, and is a module and plug-in that can be easily and rapidly expanded. To facilitate developers to quickly build their own applications.

### 2. Vulnerability exploitation process

The homepage of the normal website is shown as follows

```
https://xx.com/
```

![](images/57.jpg)

This cms has the registration function

```
https://xx.com/user   
```

Entering the user path will jump to the login and registration page, as shown below

![]images/58.jpg)

![](images/59.jpg)

You can register and log in here

![](images/60.jpg)

After registering the account, log in to the background as follows

![](images/61.jpg)

After the account is registered, log in to the background and there is a file upload vulnerability in the modified avatar. However, the front-end verification is done here, so first change the php file to the image format



![]images/62.jpg)

![](images/63.jpg)

The successful upload is shown as follows

![](images/64.jpg)

Click OK to capture the package and return to the address of the uploaded file

```
/uploads/user_img/62c3aaf37efed.php
```

![](images/65.jpg)

Accessing this file shows that the PHP file has been uploaded successfully

![](images/66.jpg)



