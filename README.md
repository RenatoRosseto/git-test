Exercicios
========

<!-- Renato Rosseto Neto - 31336353 -->

<!-- exercicio 3 -->

<?php 	
	$P1 = "10";
	$M1 = "10";
	$M2 = "10";
	$Ex = "10";
	$Proj1 = "10";
	$Proj2 = "10";
	$Proj3 = "10";
	$TrabF = "10";
	$Proc = "10";
	$PF  = "10"; 
	$MI = ((30*$P1 + 10*$M1 + 10*$M2 + 5*$Ex + 5*$Proj1 + 5*$Proj2 + 5*$Proj3 + 10*$TrabF + 20*$Proc)/100);        //Calculo da MI (media Intermediária)
?>

<html>
	<head>
		<meta charset="utf-8">
		<title> Calculo de Media </title>
	</head>
	<body>
	<?php 
	
	echo "---------- Exercicio 3 ----------<p/>";
	
	if ($MI >= 7.5){
	    $MF = $MI;
		
		echo "Aprovado sem Prova Final<p/>";
		echo "Parabens!!! Boas ferias<p/>";
	}
	
	else{
	    $MF = ($MI + $PF)/2;
		
		if ($MF >= 5.0){
			echo "Aprovado com Prova Final<p/>";
			echo "Agora ja pode descansar tranquilo.<p/>";
        }       
		else{ 
			echo "Reprovado<p/>";
			echo "Nao foi dessa vez. Ano que vem tem mais TWII.<p/>";
		}
	}
	?>
	</body>
</html>

 <!-- exercicio 4 -->

<!DOCTYPE html>
<html>
	<head>
	</head>
	<body>
		<?php
		echo "---------- Exercicio 4 ----------<p/>";
			$imp= "<table border='1'
				<tr>
					<th>ID</th>
					<th>NOME</th>
					<th>DESC</th>
				</tr>
				";
			$nlinha=7;
			
			for($i=0; $i<$nlinha; $i++)
			{
				$cor= "";
				if($i%2==0)
				{
					$cor = "bgcolor='#aaddbb'";
				}
				$imp .="<tr ". $cor .">";
				$imp .="<td> id </td>";
				$imp .="<td> nome </td>";
				$imp .="<td> desc </td>";
				$imp .="</tr>";			
			}
			"</table>";
			
			$fibo1=0;
			$fibo2=1;
			$fibo3;
			for($i=0; $i<15; $i++)
			{
				$fibo3 = $fibo1 + $fibo2;
				$fibo1 = $fibo2;
				$fibo2 = $fibo3;
				$imp .=$fibo3 . " ";
			}
			echo "<br>";
			
			
			for($i=1; $i<100; $i++)
			{
				$verdade=0;
				for($a=1; $a<=$i; $a++)
				{
					if($i%$a==0)
					{
						$verdade++ ;
					}
				}
				$imp .= "<br>" . $i . " "; 

				if($verdade==2)
				{
					$imp .= "PRIMO";
				}
				else
				{
					$imp .= "NAO PRIMO";
				}
				$imp .="<br>";
			}	
			echo $imp;
			
			
		?>
	</body>
</html>
