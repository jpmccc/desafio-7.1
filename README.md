# desafios

Desafio 7.1

<?php
$senha= "FrutasVermelhas123";
$senha_usuario = readline("Digite sua senha: ");


if ($senha_usuario == $senha) {
   echo "Login correto! Acesso liberado." . PHP_EOL;
} else {
   echo "Senha incorreta! Tente novamente." . PHP_EOL;
}
?>

Desafio 7.2
<?php

echo "Quantos patinhos foram passear? ";
$patinhos = (int) trim(fgets(STDIN));

if ($patinhos > 0) {
    while ($patinhos > 0) {
        echo "$patinhos patinhos foram passear\n";
        echo "Além das montanhas, para brincar\n";
        echo "A mamãe gritou: Quá, quá, quá, quá\n";
        
        $patinhos--;

        if ($patinhos > 0) {
            echo "Mas só $patinhos patinhos voltaram de lá.\n\n";
        } else {
            echo "Mas nenhum patinho voltou de lá.\n\n";
        }
    }

    echo "A mamãe patinha foi procurar\n";
    echo "Além das montanhas, na beira do mar\n";
    echo "A mamãe gritou: Quá, quá, quá, quá\n";
    echo "E todos os patinhos voltaram de lá!\n";
} else {
    echo "Nenhum patinho foi passear!\n";
}

?>

Desafio 7.3

<?php
$contas = [
    [
        'numero_conta' => '12345',
        'cpf' => '123.456.789-01',
        'titular' => 'João Silva',
        'saldo' => 1500
    ],
    [
        'numero_conta' => '67890',
        'cpf' => '987.654.321-00',
        'titular' => 'Maria Oliveira',
        'saldo' => 2300
    ],
    [
        'numero_conta' => '11223',
        'cpf' => '555.666.777-88',
        'titular' => 'Carlos Souza',
        'saldo' => 500
    ]
];

function exibirInformacoesConta($numeroConta, $contas) {
    if ($numeroConta == '12345') {
        echo " Detalhes da Conta " . PHP_EOL;
        echo "Número da Conta: 12345" . PHP_EOL;
        echo "Titular: João Silva" . PHP_EOL;
        echo "CPF do Titular: 123.456.789-01" . PHP_EOL;
        echo "Saldo: R$ 1500" . PHP_EOL;
    } elseif ($numeroConta == '67890') {
        echo " Detalhes da Conta " . PHP_EOL;
        echo "Número da Conta: 67890" . PHP_EOL;
        echo "Titular: Maria Oliveira" . PHP_EOL;
        echo "CPF do Titular: 987.654.321-00" . PHP_EOL;
        echo "Saldo: R$ 2300" . PHP_EOL;
    } elseif ($numeroConta == '11223') {
        echo " Detalhes da Conta " . PHP_EOL;
        echo "Número da Conta: 11223" . PHP_EOL;
        echo "Titular: Carlos Souza" . PHP_EOL;
        echo "CPF do Titular: 555.666.777-88" . PHP_EOL;
        echo "Saldo: R$ 500" . PHP_EOL;
    } else {
        echo "Conta não encontrada!" . PHP_EOL;
    }
}

echo "Bem-vindo ao Sistema de Consultas Bancárias!" . PHP_EOL;
echo "Digite o número da conta que deseja consultar: ";
$numeroConta = readline();

exibirInformacoesConta($numeroConta, $contas);

?>




