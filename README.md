<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="indes.css">
</head>
<body>
    <div id="form">
        <form action="#" name="myform" method="post">
            <div>
                <label>Name:</label>
                <input type="text" id="name" class="name">
                <span id="e-name"></span>
            </div>
            <div>
                <label>Email:</label>
                <input type="text" id="email">
                <span id="e-email"></span>
            </div>
            <div>
                    <label>Phone:</label>
                    <input type="number" id="phone">
                    <span id="e-phone"></span>
            </div>
            <div>
                    <label>Password:</label>
                    <input type="password" id="password">
                    <span id="e-password"></span>
            </div>
            <div>
                    <label>Conform-Password:</label>
                    <input type="password" id="c-password">
                    <span id="e-cpassword"></span>
            </div>
            <input type="submit" onclick="return validate();" value="submit">
        </form>
    </div>
    <script>
        function validate() {
            document.getElementById("e-name").innerHTML="";
            document.getElementById("e-phone").innerHTML="";
            document.getElementById("e-email").innerHTML="";
            document.getElementById("e-password").innerHTML="";
            document.getElementById("e-cpassword").innerHTML="";

            // var password = document.myform.password.value;
            // var c-password = document.myform.c-password.value;
           
         if (document.myform.name.value ==="" ) {
            document.getElementById("e-name").innerHTML = "Name should be filled"
            document.myform.name.focus();
            return false;
        }
        else if (document.myform.name.value.length<5){
            document.getElementById("e-name").innerHTML = "Name must be atleast 5  words"
            document.myform.name.focus();
            return false;
        }
        if (document.myform.email.value ==="" ) {
            document.getElementById("e-email").innerHTML = "Email must be filled"
            document.myform.email.focus();
            return false;       
        }
        if (document.myform.phone.value ==="" ){
            document.getElementById("e-phone").innerHTML = "Phone number must be filled"
            document.myform.phone.focus();
            return false;
        }
        else if(document.myform.phone.value.length < 10){
            document.getElementById("e-phone").innerHTML = "Phone number must be atleast 10 word"
            document.myform.phone.focus();
            return false;
        }
        if(document.myform.password.value.length < 10){
            document.getElementById("e-password").innerHTML = "Password must be of 8 words"
            document.myform.password.focus();
            return false;
        }
        if(document.myform.password.value !== document.myform.c-password.value){
                document.getElementById("e-cpassword").innerHTML = "password do not match"
                document.myform.c-password.focus();
                return false;
            }
        
        
        return true;
        }
        
    </script>
</body>
</html>
