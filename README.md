# Calculadora Android

## Visão Geral

O projeto **Calculadora Android** é um aplicativo desenvolvido em **Java** para realizar operações matemáticas básicas, como soma, subtração, multiplicação e divisão. O exercício teve como objetivo praticar conceitos de programação, organização de código e desenvolvimento de interfaces Android.

---

# Conceitos Aplicados

## Uso de Métodos

O projeto foi estruturado utilizando métodos específicos para cada responsabilidade:

* `onCreate()` → Inicializa a aplicação.
* `configuracoes()` → Realiza a configuração dos componentes da interface.
* `eventos()` → Define as ações dos botões.
* `executar()` → Centraliza a lógica dos cálculos.

Essa divisão torna o código mais organizado, legível e fácil de manter.

---

## Separação de Responsabilidades

O método `onCreate()` foi mantido simples, delegando tarefas para outros métodos específicos.

Essa abordagem melhora a organização do código e facilita futuras alterações ou expansões da aplicação.

---

## Reutilização de Código

A lógica das operações matemáticas foi centralizada no método `executar()`, evitando repetição de código para cada botão da calculadora.

### Exemplo

```java
btnSomar.setOnClickListener(v -> executar("+"));
btnSubtrair.setOnClickListener(v -> executar("-"));
btnMultiplicar.setOnClickListener(v -> executar("*"));
btnDividir.setOnClickListener(v -> executar("/"));
```

Essa estratégia segue o princípio **DRY (Don't Repeat Yourself)**, tornando a manutenção mais simples.

---

## Tratamento de Exceções

O projeto utiliza a estrutura `try-catch` para evitar falhas durante a conversão dos valores digitados pelo usuário.

### Exemplo

```java
try {
    Double n1 = Double.valueOf(edtPrimeiroNumero.getText().toString());
    Double n2 = Double.valueOf(edtSegundoNumero.getText().toString());
} catch (Exception e) {
    txvResultado.setText("Digite números válidos");
}
```

Isso garante maior robustez e melhora a experiência do usuário ao lidar com entradas inválidas.

---

# Funcionalidades

* Soma de números.
* Subtração de números.
* Multiplicação de números.
* Divisão de números.
* Validação de entrada de dados.
* Exibição de mensagens de erro quando necessário.


---

# Conclusão

O projeto **Calculadora Android** permitiu aplicar conceitos fundamentais de programação e desenvolvimento mobile, destacando a importância da organização do código, reutilização de funcionalidades e tratamento adequado de erros para criar aplicações mais eficientes e fáceis de manter.
