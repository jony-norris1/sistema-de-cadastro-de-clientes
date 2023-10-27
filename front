npx create-react-app frontend-empresa --template typescript
cd frontend-empresa

npm install less less-loader

import React, { useState } from 'react';
import axios from 'axios';

const CadastroEmpresa: React.FC = () => {
  const [empresa, setEmpresa] = useState({
    nomeCliente: '',
    senha: '',
    razaoSocial: '',
    cnpj: '',
    cep: '',
    endereco: '',
    numero: '',
    telefone: '',
    email: '',
  });

  const preencherEndereco = async () => {
    try {
      const response = await axios.get(`https://viacep.com.br/ws/${empresa.cep.replace('-', '')}/json/`);
      setEmpresa({ ...empresa, endereco: response.data.logradouro });
    } catch (error) {
      console.error('Erro ao preencher endereço:', error);
    }
  };

  const enviarCadastro = () => {
    // Envie o formulário para o servidor
  };

  return (
    <div>
      <h1>Cadastro de Empresa</h1>
      <form>
        {/* Campos do formulário */}
        <button onClick={preencherEndereco}>Preencher Endereço</button>
        <button onClick={enviarCadastro}>Cadastrar Empresa</button>
      </form>
    </div>
  );
};

export default CadastroEmpresa;

#Lembre-se de substituir 'seu_usuario' e 'sua_senha' pelas informações de acesso ao seu banco de dados MySQL no back-end. Além disso, implemente a validação de campos e a lógica de envio do formulário de cadastro de empresa no front-end e no back-end, de acordo com os requisitos fornecidos.
