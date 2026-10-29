# Teste Unitário com MSTest – Cálculo de IMC

Atividade 5 – UC 15 (Testes Back-End) – SENAI

Aplicação de teste unitário em C# usando **MSTest** para validar o sistema de cálculo de IMC
(valor e faixa de classificação a partir de peso e altura).

## Estrutura

```
teste-unitario-mstest-imc/
└── atividade_imc_mstest/
    ├── atividade_imc_mstest.csproj   # projeto MSTest (Nullable = disable)
    ├── imc.cs                        # classe IMC (namespace atividade_imc_mstest)
    ├── UnitTest1.cs                  # testes: Teste_Calculo_IMC e Teste_Categoria_IMC
    └── Usings.cs                     # global using do MSTest
```

## Como executar

Pré-requisito: .NET SDK instalado e VS Code com as extensões C# e .NET Core Test Explorer.

```bash
cd atividade_imc_mstest
dotnet build
dotnet test
```

## Testes implementados

| Teste | Tipo | Descrição |
|---|---|---|
| `Teste_Calculo_IMC` | `[TestMethod]` | Peso 80 kg e altura 1,60 m → IMC previsto **31,25** |
| `Teste_Categoria_IMC` | `[DataTestMethod]` | 6 entradas (`DataRow`), uma para cada faixa de IMC |

## Resultado esperado

Com peso 80 kg e altura 1,60 m o IMC é 31,25, que corresponde a **Obesidade Grau I**.
Como o teste de categoria recebe seis faixas, mas só uma entrada de dados de referência:

- **2 testes aprovados** (cálculo do IMC + categoria "Obesidade Grau I")
- **5 testes com falha** (as demais categorias)
- **Total: 7 testes**

Esse resultado é o esperado pela atividade e demonstra que o teste detecta divergências.
