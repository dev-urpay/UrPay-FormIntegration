# UrPay - Integración por formulario HTML


##### Esta integración es una de las más rápidas de desplegar dado que no requiere mucha programación.

  ### Campos requeridos

  * by_email: Email de la persona que esta realizando la compra.
  * by_name: Nombre de la persona que esta realizando la compra.
  * tx_commerce: Public Key de la cuenta.
  * tx_commerce_id: ID del comercio.
  * tx_reference: Referencia *única* por compra realizada al comercio.
  * tx_descripcion: Una breve descripción del producto que se esta comprando.
  * tx_amount: Monto total de la compra, incluido IVA *si aplica*. El formato debe ser el siguiente: 10000.00 o 10000,00. 
    En todos los casos el valor enviado debe ir sin separador de miles y con máximo dos decimales.
  * tx_tax: El valor del impuesto a aplicar, si no tiene ningún impuesto enviar *0*.
  * tx_currency: Solo se admiten dos valores: COP ó USD.
  * tx_signature: [Hash HMAC](https://es.wikipedia.org/wiki/HMAC) de los datos para comprobar la integridad de estos. La firma de los datos se puede realizar con alguno de los
    siguiente algoritmos:
      * sha512/256
      * sha512
      * sha384
      * sha256
      * md5
      
     Recomendamos el uso de cualquier función SHA por encima de MD5.
     
   * st_response: URL de respuesta por donde se enviara el estado de la transacción por medio del método GET.
        
Con estos datos se puede dar inicio a recibir pagos en línea con UrPay! Cualquier duda o bug escribirnos a dev-issues@urpay.co
