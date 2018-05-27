# Modificaciones realizadas en la configuración para la creación de SorianoCoin

  
1. Instalamos en nuestra VPS las dependencias necesarias, lo encontramos el github en la carpeta doc(build-unix.md).
2. Clonamos el repositorio de la moneda en la VPS desde github.
3. Modificamos los parámetros básicos en los ficheros de configuración según la documentación.
4. Compilamos.
5. Creamos el bloque génesis.
6. Compilamos de nuevo con el bloquegensis añadido en los ficheros de configuración.
7. Abrirmos los puertos necesaris en la VPS para poder recibir conexiones entrantes desde el exterior.
---

Fichero CryptoNoteCondig.h

	const char     CRYPTONOTE_NAME[] = "SorianoCoin";
	const uint64_t MONEY_SUPPLY = UINT64_C(858986905600000000);
	const int      P2P_DEFAULT_PORT = 17236;
	const int      RPC_DEFAULT_PORT = 18236; //TODO Add here your network
	
	seed nodes
	const std::initializer_list<const char*> SEED_NODES = {
 	 "localhost: 17236" //si queremos añadir mas nodos hay que poner una coma después de cada uno
	  //la ip debe ser la de cada uno de los nodos
	};


Paso 6 (Bloque génesis)

	const char     GENESIS_COINBASE_TX_HEX[]                     = "013c01ff0001c08f8af8ae5f029b2e4c0281c0b02e7c53291a94d1d0cbff8883f8024f5142ee494ffbbd088071210150c979713d4414ca35fad3f7b323edf07d8b0ae6dd325f64582d664e198fcf3f";

Fichero CMakeList.txt

	set_property(TARGET Daemon PROPERTY OUTPUT_NAME "sorianocoind")

