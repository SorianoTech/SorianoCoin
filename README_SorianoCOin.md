# Modificaciones realizadas en la configuración para la creación de SorianoCoin

  
1. Instalamos en nuestra VPS las dependencias necesarias, lo encontramos el github en la carpeta doc(build-unix.md).
2. Clonamos el repositorio de la moneda en la VPS desde github.
3. Modificamos los parámetros básicos en los ficheros de configuración según la documentación.
---


	const char     CRYPTONOTE_NAME[] = "SorianoCoin";

	const uint64_t MONEY_SUPPLY = UINT64_C(858986905600000000);

	const int      P2P_DEFAULT_PORT = 88088;

	const int      RPC_DEFAULT_PORT = 88089; //TODO Add here your network 



