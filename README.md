no xammp ta dando erro no mysql_connect() ajuda ai 
# hello-word
<html>
<head>
	<title>Cadastrando...</title>
</head>

<body>
<?php
	$host = "localhost";
	$user = "root";
	$pass = "";
	$banco = "cadastro";
	$conexao = mysql_connect ($host, $user, $pass) or die(mysql_error());
	mysql_select_db($banco) or die(mysql_error());
?>
<?php
	$nome=$_POST['nome'];
	$sobrenome=$_POST['sobrenome'];
	$pais=$_POST['pais'];
	$estado=$_POST['estado'];
	$cidade=$_POST['cidade'];
	$email=$_POST['email'];
	$senha=$_POST['senha'];
	$sql = mysql_query("ISERT INTO usoarios(nome,sobrenome,pais,estado,cidade,e-mail,senha)
	VALUES('$nome', '$sobrenome', '$pais', '$estado', '$cidade', '$e-mail', '$senha')");
	echo "<centro><h1>cadastro efetuado com sucesso!</h1></center>";
?>
</body>
</html>
