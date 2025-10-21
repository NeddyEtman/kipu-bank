KipuBank Smart Contract
Descripción
KipuBank es un contrato inteligente en Ethereum que permite a los usuarios depositar y guardar ETH en su propia bóveda personal. Los depósitos y retiros están regulados por límites configurables y el contrato emite eventos para cada acción realizada. Incluye prácticas avanzadas de seguridad como errores personalizados y validaciones estrictas.
Características principales:
•	Cada usuario tiene una bóveda personal para depositar ETH.
•	El banco tiene un límite global de depósitos (bankCap).
•	Hay un límite máximo fijo de retiro por transacción (withdrawalLimit).
•	Los depósitos y retiros exitosos emiten eventos en la blockchain.
•	El contrato lleva la cuenta automática de todos los movimientos.
•	No permite depósitos ni retiros de valor cero.
•	Incluye validaciones y errores personalizados para seguridad y claridad.
________________________________________
Instrucciones de despliegue
Herramientas necesarias
•	Remix IDE
•	Navegador con extensión MetaMask conectada a una testnet (recomendado Sepolia).
•	Algo de ETH de prueba en tu wallet (puedes obtenerlo en faucets públicos de Sepolia).
Pasos para desplegar el contrato
1.	Abre Remix y copia el código del contrato KipuBank.sol en un nuevo archivo.
2.	Selecciona el compilador Solidity compatible (ejemplo: 0.8.26 o superior).
3.	Haz clic en el botón Compile para verificar que el contrato no tiene errores.
4.	Dirígete a la pestaña Deploy & Run Transactions.
5.	Selecciona Injected Provider - MetaMask y asegúrate de estar en la testnet.
6.	En el apartado de despliegue, ingresa los valores para:
•	_bankCap: (por ejemplo, 1000000000000000000 para 1 ETH)
•	_withdrawalLimit: (por ejemplo, 10000000000000000 para 0.01 ETH)
7.	Haz clic en el botón transact para desplegar el contrato.
8.	Confirma la transacción en MetaMask y espera a que se mine.
________________________________________
Cómo interactuar con el contrato
Depositar ETH
1.	En Remix, localiza la sección de funciones del contrato desplegado.
2.	En el campo "VALUE", ingresa la cantidad de ETH que quieres depositar (en wei).
•	Ejemplo: Para 0.03 ETH escribe 30000000000000000.
3.	Haz clic en el botón deposit().
4.	Confirma la transacción en MetaMask.
5.	Si el depósito es exitoso, se emitirá el evento DepositMade.
Retirar ETH
1.	Ingresa el monto a retirar en el campo del parámetro de la función withdraw.
•	Ejemplo: Para retirar 0.01 ETH escribe 10000000000000000.
2.	Haz clic en el botón withdraw y confirma en MetaMask.
3.	Recuerda que hay un límite máximo por retiro (withdrawalLimit).
Consultar tu bóveda
•	Usa getMyVaultBalance() para ver tu saldo actual.
•	Usa getAvailableSpace() para ver el espacio global restante en el contrato.
Visualizar Eventos
•	Los eventos emitidos (DepositMade, WithdrawalMade) se pueden ver en la pestaña de terminal de Remix, en la blockchain (testnet) y usando Etherscan para la red que estés usando.
Errores Comunes
•	Depositar/retirar 0 ETH: No permitido.
•	Intentar superar los límites: Recibirás un error personalizado y la transacción fallará, ¡no perderás fondos!
________________________________________
Autor y contacto
•	Autor: Neddy Etman Choque Flores

