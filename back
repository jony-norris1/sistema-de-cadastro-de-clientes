mkdir backend-empresa
cd backend-empresa
npm init -y

npm install express mysql2 reflect-metadata typeorm class-validator

{
  "type": "mysql",
  "host": "localhost",
  "port": 3306,
  "username": "seu_usuario",
  "password": "sua_senha",
  "database": "empresa_db",
  "synchronize": true,
  "logging": true,
  "entities": ["src/entities/*.ts"],
  "migrations": ["src/migrations/*.ts"],
  "subscribers": ["src/subscribers/*.ts"],
  "cli": {
    "entitiesDir": "src/entities",
    "migrationsDir": "src/migrations",
    "subscribersDir": "src/subscribers"
  }
}

import { Entity, PrimaryGeneratedColumn, Column } from 'typeorm';

@Entity()
export class Empresa {
  @PrimaryGeneratedColumn()
  id: number;

  @Column()
  nomeCliente: string;

  @Column()
  senha: string;

  @Column()
  razaoSocial: string;

  @Column()
  cnpj: string;

  @Column()
  cep: string;

  @Column()
  endereco: string;

  @Column()
  numero: number;

  @Column()
  telefone: string;

  @Column()
  email: string;
}

import { Request, Response } from 'express';
import { getRepository } from 'typeorm';
import { Empresa } from '../entities/Empresa';
import axios from 'axios';

class EmpresaController {
  async criarEmpresa(req: Request, res: Response) {
    // Valide e salve a empresa usando o TypeORM
  }

  async listarEmpresas(req: Request, res: Response) {
    // Liste todas as empresas cadastradas
  }

  async consultarEmpresaPorCnpj(req: Request, res: Response) {
    // Consulte uma empresa específica por CNPJ
  }

  async atualizarEmpresa(req: Request, res: Response) {
    // Atualize os dados de uma empresa
  }

  async excluirEmpresa(req: Request, res: Response) {
    // Exclua uma empresa
  }

  async preencherEndereco(req: Request, res: Response) {
    // Use a API do ViaCEP para preencher automaticamente o campo de endereço
  }
}

export default new EmpresaController();

import express from 'express';
import 'reflect-metadata';
import { createConnection } from 'typeorm';
import EmpresaController from './controllers/EmpresaController';

const app = express();
app.use(express.json());

createConnection().then(async () => {
  // Defina as rotas aqui
});

app.listen(3000, () => {
  console.log('Servidor está rodando na porta 3000');
});
