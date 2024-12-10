# Explicação da Solução / Solution Explanation

## 🇧🇷 Português:

A solução utiliza a seguinte abordagem:
1. Criamos um dicionário que mapeia cada símbolo romano para seu valor inteiro.
2. Percorremos a string do numeral romano da direita para a esquerda.
3. Para cada caractere:
   - Se o valor do caractere for menor que o valor do caractere anterior, subtraímos esse valor.
   - Caso contrário, somamos o valor ao total.
4. Retornamos o total ao final.

Essa abordagem considera corretamente as regras de subtração dos numerais romanos.

### Código:
```python
def roman_to_int(s):
    roman_values = {
        'I': 1, 'V': 5, 'X': 10, 'L': 50,
        'C': 100, 'D': 500, 'M': 1000
    }
    total = 0
    prev_value = 0
    for char in reversed(s):
        value = roman_values[char]
        if value < prev_value:
            total -= value
        else:
            total += value
        prev_value = value
    return total
```
_____________________________________________________________________________________________


## 🇺🇸 English:

The solution uses the following approach:
1. Create a dictionary mapping each Roman numeral to its integer value.
2. Traverse the Roman numeral string from right to left.
3. For each character:
   - If the character’s value is smaller than the previous character’s value, subtract it.
   - Otherwise, add it to the total.
4. Return the total at the end.

This approach correctly accounts for the subtraction rules of Roman numerals.

### Code:
```python
def roman_to_int(s):
    roman_values = {
        'I': 1, 'V': 5, 'X': 10, 'L': 50,
        'C': 100, 'D': 500, 'M': 1000
    }
    total = 0
    prev_value = 0
    for char in reversed(s):
        value = roman_values[char]
        if value < prev_value:
            total -= value
        else:
            total += value
        prev_value = value
    return total
```
