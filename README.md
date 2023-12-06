# eps-api-express
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
POSMAN
get pacientes 
{
    "message": "Error al obtener los pacientes",
    "error": "Unknown column 'fecha_nacimiento' in 'field list'"
}
get doctores 

    "message": "Error al obtener los doctores",
    "error": "Unknown column 'telefono' in 'field list'"
}get citas
{
    "message": "Operación exitosa",
    "data": [
        {
            "fecha_hora": "1970-01-01T00:00:01.000Z",
            "id_profesional": 1,
            "id_numeroCedula": 1094882343
        }
    ]
}post citas 
{{
    "message": "No se pudo crear la cita",
    "error": "notNull Violation: Cita.fecha_hora cannot be null,\nnotNull Violation: Cita.id_profesional cannot be null,\nnotNull Violation: Cita.id_numeroCedula cannot be null"
}
        }
    ]
}
post doctores
{
    "message": "No se pudo crear el doctor",
    "error": "SequelizeValidationError: notNull Violation: Doctor.id_profesional cannot be null,\nnotNull Violation: Doctor.nombre cannot be null,\nnotNull Violation: Doctor.apellido cannot be null,\nnotNull Violation: Doctor.correo cannot be null,\nnotNull Violation: Doctor.telefono cannot be null,\nnotNull Violation: Doctor.especialidad cannot be null\n    at InstanceValidator._validate (C:\\Users\\LENOVO\\Desktop\\proyecto api\\eps-udistrital-express\\node_modules\\sequelize\\lib\\instance-validator.js:50:13)\n    at process.processTicksAndRejections (node:internal/process/task_queues:95:5)\n    at async InstanceValidator._validateAndRunHooks (C:\\Users\\LENOVO\\Desktop\\proyecto api\\eps-udistrital-express\\node_modules\\sequelize\\lib\\instance-validator.js:60:7)\n    at async InstanceValidator.validate (C:\\Users\\LENOVO\\Desktop\\proyecto api\\eps-udistrital-express\\node_modules\\sequelize\\lib\\instance-validator.js:54:12)\n    at async Doctor.save (C:\\Users\\LENOVO\\Desktop\\proyecto api\\eps-udistrital-express\\node_modules\\sequelize\\lib\\model.js:2426:7)\n    at async Doctor.create (C:\\Users\\LENOVO\\Desktop\\proyecto api\\eps-udistrital-express\\node_modules\\sequelize\\lib\\model.js:1362:12)"
}
post pacientes

    "message": "No se pudo crear el paciente",
    "error": "SequelizeValidationError: notNull Violation: Paciente.id_numeroCedula cannot be null,\nnotNull Violation: Paciente.nombre cannot be null,\nnotNull Violation: Paciente.apellido cannot be null,\nnotNull Violation: Paciente.fecha_nacimiento cannot be null,\nnotNull Violation: Paciente.telefono cannot be null\n    at InstanceValidator._validate (C:\\Users\\LENOVO\\Desktop\\proyecto api\\eps-udistrital-express\\node_modules\\sequelize\\lib\\instance-validator.js:50:13)\n    at process.processTicksAndRejections (node:internal/process/task_queues:95:5)\n    at async InstanceValidator._validateAndRunHooks (C:\\Users\\LENOVO\\Desktop\\proyecto api\\eps-udistrital-express\\node_modules\\sequelize\\lib\\instance-validator.js:60:7)\n    at async InstanceValidator.validate (C:\\Users\\LENOVO\\Desktop\\proyecto api\\eps-udistrital-express\\node_modules\\sequelize\\lib\\instance-validator.js:54:12)\n    at async Paciente.save (C:\\Users\\LENOVO\\Desktop\\proyecto api\\eps-udistrital-express\\node_modules\\sequelize\\lib\\model.js:2426:7)\n    at async Paciente.create (C:\\Users\\LENOVO\\Desktop\\proyecto api\\eps-udistrital-express\\node_modules\\sequelize\\lib\\model.js:1362:12)"
}
put paciente 
404: Page not found

put cita 
{
    "message": "Error al modificar la cita",
    "error": "WHERE parameter \"fecha_hora\" has invalid \"undefined\" value"
}
put doctores 
404: Page not found

delete doctores
404: Page not found
delete cita 
{
    "message": "Error al eliminar la cita",
    "error": "WHERE parameter \"fecha_hora\" has invalid \"undefined\" value"
}
delete paciente 
404: Page not found

