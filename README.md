# clean-code-rocketseat

## Princípios do Clean Code: 
1. Teste automatizados
2. Revisão de código
3. Refatoração de código
4. Simplicidade -> Keep It Simple and Stupid (KISS)
5. Iterações curtas

___

## Nomenclatura de variaveis:
- Evite nomes genéricos (data, response, args, params)
- Utilize nomes legiveis para suas variaveis
- Evite uso de diminutivos (users.id -> u.id)

## Booleanos
- Escreva como se fosse uma pergunta (is, has, does, are, ...)
    - isDisabled = true
    - areEqual = true
    - hasEcryptation = true
    - isUserProfileLoading = false

## Causa vs Efeito
- Nomear as variaveis pela causa e não pelo efeito dela no código
Nomeando pelo efeito:
```
function Button(){
    const isDisabled = true

    return(
        <button disabled={isDisabled}>
        <span></span>
        {isDisabled ? 'Carregando' : 'Enviar'}
        </button>
    )
}
```
Nomeando pela causa:
```
function Button(){
    const isFormSubmitting = true

    return(
        <button disabled={isFormSubmitting}>
        <span></span>
        {isFormSubmitting ? 'Carregando' : 'Enviar'}
        </button>
    )
}
```