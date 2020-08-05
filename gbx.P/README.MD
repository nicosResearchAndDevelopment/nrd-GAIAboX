# GAIAboX Policy `P`

GAIAboX handles machine readable contracts (policies) in a way
 once can see them described in the
 [Open Digitals Right Language (ODRL Information Model 2.2)](https://www.w3.org/TR/odrl-model/).

## Decision Point `DP`

## Information Point `IP`

Notwithstnding the fact that GAIAboX at a whole
 acts as "Information Point", it holds some
 special informations like languages, currencies
 and chemical elements [here](./IP/README.md).

## Binary Operator `BO`

A Binary Operator (BO), understood as an operator returning
 a boolean value. See it as a part of a constraint
 like this:

|  operand | binary operator  | operand  | is |
|---|---|---|:---|
| 42    | `equals`   | 42  | true  |
| "abc" | `contains` | "b" | true  |
| alice | `loves`    | Bob | false |

GAIAboX brings binary operators to life 
 ("Binary Operator as a Service", BOaaS) as usable
 functions. Here they will be
 explained in their different contexts and in more
 [detail](./BO/README.md).

---