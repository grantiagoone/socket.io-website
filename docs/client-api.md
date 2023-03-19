<!DOCTYPE html>
<html>
<head>
	<title>Chat</title>
	<style>
		body {
			font-family: Arial, sans-serif;
		}

		#register-form, #login-form, #chat {
			width: 300px;
			margin: 0 auto;
			padding: 20px;
			border: 1px solid #ccc;
			border-radius: 5px;
		}

		#register-form h2, #login-form h2, #chat h2 {
			margin-top: 0;
		}

		#register-form input, #login-form input, #message {
			display: block;
			width: 100%;
			margin-bottom: 10px;
			padding: 5px;
			border: 1px solid #ccc;
			border-radius: 5px;
		}

		#register-form button, #login-form button, #chat button {
			display: block;
			width: 100%;
			padding: 10px;
			border: none;
			background-color: #4CAF50;
			color: #fff;
			cursor: pointer;
			border-radius: 5px;
		}

		#register-form button:hover, #login-form button:hover, #chat button:hover {
			background-color: #3e8e41;
		}

		#messages {
			height: 200px;
			overflow-y: scroll;
			border: 1px solid #ccc;
			border-radius: 5px;
			padding: 10px;
			margin-bottom: 10px;
		}
	</style>
</head>
<body>
	<div id="register-form">
		<h2>Register</h2>
		<input type="text" id="name" placeholder="Name">
		<input type="email" id="email" placeholder="Email">
		<input type="password" id="password" placeholder="Password">
		<button onclick="register()">Register</button>
	</div>
	<div id="login-form" style="display:none">
		<h2>Login</h2>
		<input type="email" id="login-email" placeholder="Email">
		<input type="password" id="login-password" placeholder="Password">
		<button onclick="login()">Login</button>
	</div>
	<div id="chat" style="display:none">
		<h2>Chat</h2>
		<div id="messages"></div>
		<input type="text" id="message" placeholder="Message">
		<button onclick="sendMessage()">Send</button>
	</div>
	<script src="https://www.gstatic.com/firebasejs/9.0.1/firebase-app.js"></script>
	<script src="https://www.gstatic.com/firebasejs/9.0.1/firebase-auth.js"></script>
	<script src="https://www.gstatic.com/firebasejs/9.0.1/firebase-firestore.js"></script>
	<script src="https://www.gstatic.com/firebasejs/9.0.1/firebase-storage.js"></script>
	<script src="app.js"></script>
</body>
</html>
