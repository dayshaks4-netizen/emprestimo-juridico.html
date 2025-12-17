<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sistema de Empréstimo Jurídico</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 20px; background-color: #f4f4f4; }
        h1 { text-align: center; color: #333; }
        form { max-width: 600px; margin: 0 auto; background: white; padding: 20px; border-radius: 8px; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
        label { display: block; margin-top: 10px; }
        input, select { width: 100%; padding: 8px; margin-top: 5px; box-sizing: border-box; }
        button { margin-top: 20px; padding: 10px; background: #007bff; color: white; border: none; cursor: pointer; }
        button:hover { background: #0056b3; }
        #emprestimos-list { max-width: 800px; margin: 20px auto; }
        table { width: 100%; border-collapse: collapse; background: white; }
        th, td { border: 1px solid #ddd; padding: 8px; text-align: left; }
        th { background: #007bff; color: white; }
        .pago { background-color: #d4edda; }
        .atrasado { background-color: #f8d7da; }
    </style>
</head>
<body>
    <h1>Sistema de Gestão de Empréstimos Jurídicos</h1>
    
    <form id="emprestimo-form">
        <label for="devedor">Nome do Devedor:</label>
        <input type="text" id="devedor" required>
        
        <label for="valor">Valor do Empréstimo (R$):</label>
        <input type="number" id="valor" step="0.01" required>
        
        <label for="data-emprestimo">Data do Empréstimo:</label>
        <input type="date" id="data-emprestimo" required>
        
        <label for="parcelas">Número de Parcelas:</label>
        <input type="number" id="parcelas" min="1" value="1" required>
        
        <label for="intervalo">Intervalo entre Parcelas (dias):</label>
        <input type="number" id="intervalo" min="1" value="30" required>
        
        <label for="juros">Taxa de Juros Mensal (%):</label>
        <input type="number" id="juros" step="0.01" value="0">
        
        <button type="submit">Adicionar Empréstimo</button>
    </form>
    
    <div id="emprestimos-list">
        <h2>Empréstimos Registrados</h2>
        <table id="tabela-emprestimos">
            <thead>
                <tr>
                    <th>Devedor</th>
                    <th>Valor Total</th>
                    <th>Parcela</th>
                    <th>Data de Vencimento</th
