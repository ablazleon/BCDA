# BCDA

1- Dime el comando de truflle que hace no se qué. . .

```
truffle compile migrate test
--reset --compile-all
```

2- Teoría de drizzle

- Qué componentes están predefinidos?

Se referirá a AccountData y COntractData, imagino

- Cómo funciona cacheCAll o cacheSend?
```
cacheCall permite realizar llamadas a los métodos de los contratos

drizzle.contracts.CONTRATO.methods.METODO().call(ARGS)

cuando lo recibe drizzle actualiza el store con los nuevos valores

es apra realizar una transacción para lo que se ejecuta cacheSend

=> usamos cahceCall para registra que estamos enterados en el resutlado dle método valor()

se usa cahceSend para lanzar una transacción que ejecturaá el contrato intelegietne
```

- QUé hay dentro de drizzle?

```
el estado
el objeto para cacheCall y cacheSend
methods 
contract
```

3- Ejercicio práctico: me dan un contrato con un nuveo método y me pidne un form



```
Cambiar esto con lo que sea:


const MatricularV1 = ({drizzle, drizzleState}) => <article className="AppMisDatos">
    <h3>Matricular</h3>
    <ContractData drizzle={drizzle} drizzleState={drizzleState}
        contract={"Asignatura"} method={"profesor"} methodArgs={[]}
        render={addr => {
            if (addr == drizzleState.accounts[0]) {
                return <p>"NO SOY ALUMNO"</p>
            }
        return <ContractForm drizzle={drizzle}
                      drizzleState={drizzleState}
                      contract="Asignatura"
                      method="automatricula"
                      labels={["Nombre Alumno", "Email Alumno"]}
                />
       }}
     />
  </article>
```





