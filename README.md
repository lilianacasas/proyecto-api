# eps-udistrital-express
//citas.controller.ts 
RequestHandler = controlador con una unica accion 
tenemos un bloque  try con una setencia
  const citas 
rest estatus 200 = operacion esxitosa o ok 
tenemos un bloque catch
const err= error 
 con  res estatus 500 =error al tener citas 
tenemos un export   el cual se utiliza para exportar funciones o objertos  o un tipo dato el cual puede ser utilizado 
export const getonecita  
tenemos un bloque try con la sentencia  const donde teneos profesional ,paciente ,fecha con un res query la cual contiene informacion que llega al servidor desde el cliente incluyendo los paramertos de la url  
tenemos una const cita con un await  cita.findone el cual nos devuelve un documento que satisface un determiando criterio de consulta  es decir el preimero apartir de un orden natuaral  
esta fecha hora , id profesional  id ,paciente 
tenemos una estructura if que permite una sentencia o  bloque de sentencias en caso de que la condicion sea verdadera o si en dado caso salta su ejecucion sea falsa   
tenemos un res status con 200 = cita actualizada 
tenemos un else en caso de s i no enviar un res. status 404 cita no existe 
tenemos un bloque  catchcon res status 500 =error al modificar cita 
ts config.ts
importamos ts paciente ,ts cita,ts doctor 
importamos sequelize ,dotenv
tenemos una constante de connection  sequelize  con my sql  con un host = localhost un username y un port y password que tenemos cada una en msql 
con los models paciente cita y doctor 
generamos  una conexion por defecto =export defaul connection
models 
importamos varios clases como doctor,pacientes,cita 
y exportamos las clases cita, doctor , paciente  
y sus respectivas columnas
 @PrimaryKey
  @ForeignKey( () => Doctor)
  @Column({
    type: DataType.INTEGER,
    allowNull: false,
  })
  id_profesional!: number
y asi sucesivamente con paciente y cita 
routes 
tenemos una direccionamiento  get, pos, put y delete   en cada ts routes como lo es citas doctores y paciente 
