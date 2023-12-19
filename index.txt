<%@ page language="java" contentType="text/html; charset=UTF-8" pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Login Page</title>
</head>
<body>

    <h2>Login</h2>

    <%
        String validUsername = "sai";
        String validPassword = "422";
        if (request.getMethod().equalsIgnoreCase("post")) {
            String username = request.getParameter("username");
            String password = request.getParameter("password");
            if (validUsername.equals(username) && validPassword.equals(password)) {
    %>
                <h2>Login Successful</h2>
    <%
            } else {
    %>
                <h2>Login Failed. Please check your username and password.</h2>
    <%
            }
        }
    %>

    <form action="" method="post">
        <input type="text" id="username" name="username" required><br>
        <input type="password" id="password" name="password" required><br>
        <input type="submit" value="Login">
    </form>

</body>
</html>
