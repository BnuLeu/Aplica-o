<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sistema de Cadastro de Clientes</title>
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.bundle.min.js"></script>
</head>
<body>

<div class="container mt-5">
    <h2>Cadastro de Clientes</h2>

    <!-- Campo de Pesquisa -->
    <div class="search-container mb-4">
        <input type="text" id="search" class="form-control" placeholder="Pesquisar por nome, email, telefone, endereço ou veículo..." oninput="pesquisarClientes()">
        <button class="btn btn-primary mt-2" onclick="pesquisarClientes()">Pesquisar</button>
    </div>

    <!-- Lista de Clientes -->
    <ul id="lista-clientes" class="list-group">
        <!-- A lista de clientes é preenchida dinamicamente com JavaScript -->
    </ul>

    <!-- Botão para Adicionar Novo Cliente -->
    <button class="btn btn-success mt-4" data-toggle="modal" data-target="#addClientModal">Adicionar Cliente</button>
</div>

<!-- Modal para Adicionar/Editar Cliente -->
<div class="modal fade" id="addClientModal" tabindex="-1" role="dialog" aria-labelledby="addClientModalLabel" aria-hidden="true">
    <div class="modal-dialog" role="document">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title" id="addClientModalLabel">Adicionar Cliente</h5>
                <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                    <span aria-hidden="true">&times;</span>
                </button>
            </div>
            <div class="modal-body">
                <form id="cliente-form">
                    <div class="form-group">
                        <label for="nome">Nome</label>
                        <input type="text" class="form-control" id="nome" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" class="form-control" id="email" required>
                    </div>
                    <div class="form-group">
                        <label for="telefone">Telefone</label>
                        <input type="text" class="form-control" id="telefone" required>
                    </div>
                    <div class="form-group">
                        <label for="endereco">Endereço</label>
                        <input type="text" class="form-control" id="endereco" required>
                    </div>
                    <div class="form-group">
                        <label for="veiculo">Veiculo</label>
                        <input type="text" class="form-control" id="veiculo" required>
                    </div>
                    <button type="submit" class="btn btn-primary">Salvar</button>
                </form>
            </div>
        </div>
    </div>
</div>
    <script src="https://code.jquery.com/jquery-3.5.1.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.16.1/umd/popper.min.js"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
    <script src="{{ url_for('static', filename='js/cliente.js') }}"></script>
</body>
</html>
