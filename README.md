# Aplicacion usando **servicios de sistema**
En esta aplicacion aprenderemos a usar los servicios de sistema, para ello deberas de estudiar la clase
[Chécala aquí](http://developer.android.com/reference/android/content/Context.html).

Para poder usar esta clase vamos a utilizar sobre nuestra **Activity** el método **getSystemSrvice(getApplicationContext().TU_SERVICIO)**, donde en este caso el nombre de servico es el nombre de servic icio que debes acceder, que en la clase abstracta **Service** vienen como constantes diferentes. 
Una vez que lo hagas verifica el tipo de retorno que tiene y haz el casting respectivo, como ejemplo esta el servicio  para vibrar **VIBRATOR_SERVICE**, a continuación se muestra el código. dentro de un evento de boton flotante.

```
FloatingActionButton fab = (FloatingActionButton) findViewById(R.id.fab);
        fab.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Snackbar.make(view, "Replace with your own action", Snackbar.LENGTH_LONG)
                        .setAction("Action", null).show();
           Vibrator vibrator= (Vibrator) getSystemService(getApplicationContext().VIBRATOR_SERVICE);
                vibrator.vibrate(2000);
            }
        });
```

Para cada servicio deberás verificar en als API's la referencia respectiva a hacer el casting
