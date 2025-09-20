# Workpay - Sistema de Pagamento de Funcionários
## 📚 Visão Geral do Projeto
Workpay é um sistema de gerenciamento de pagamento de funcionários, projetado para calcular o valor diário que cada colaborador deve receber. Ele foi desenvolvido com uma arquitetura de microsserviços para garantir escalabilidade, flexibilidade e manutenção simplificada.

## ⚙️ Arquitetura de Microsserviços
O projeto Workpay é composto por quatro microsserviços distintos, cada um com sua própria responsabilidade. Embora cada serviço tenha seu próprio repositório, todos estão centralizados em um repositório principal, seguindo um padrão de multi-repo.

A comunicação entre os serviços é orquestrada por meio de um Eureka Server, que atua como um registro de serviços, permitindo que cada microsserviço se localize. Um Gateway Zuul gerencia o roteamento e a segurança das requisições, direcionando-as para o serviço correto. As chamadas de serviço a serviço são realizadas utilizando o Feign Client, que simplifica a criação de APIs RESTful.

---
## Microsserviços:
- User: Gerencia as informações dos usuários, como cadastro e perfil.
- Auth: Responsável pela autenticação e autorização, garantindo que apenas usuários válidos acessem o sistema.
- Worker: Lida com os dados dos trabalhadores e suas informações de jornada.
- Payroll: Executa o cálculo do pagamento diário, com base nas informações fornecidas pelo serviço Worker.

---
## 🛠️ Tecnologias Utilizadas
- Java: Linguagem de programação principal.
- Spring Boot: Framework para desenvolvimento dos microsserviços.
- Eureka Server: Registro de serviço para descoberta dos microsserviços.
- Gateway Zuul: Gateway de API para roteamento e filtragem de requisições.
- Feign Client: Cliente HTTP declarativo para comunicação entre serviços.
