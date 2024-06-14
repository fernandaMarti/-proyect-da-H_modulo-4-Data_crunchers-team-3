# Data Insights: ETL y Visualización Impactante en Tableau

---

## Descripción del Proyecto

¡Bienvenidas/os al emocionante proyecto "Data Insights: ETL y Visualización Impactante en Tableau" en nuestro bootcamp de análisis de datos!

En este desafío, nos sumergiremos en el apasionante mundo del reporting de datos 📊, donde adquiriremos las habilidades clave para transformar datos crudos en información significativa y visualmente impactante.

Comenzaremos explorando y limpiando un conjunto de datos proporcionado 🧹, identificando patrones y determinando las mejores prácticas para la limpieza y transformación de datos. A través de Pandas, abordaremos problemas comunes como datos faltantes o inconsistentes.

Además, nos adentraremos en el poderoso Tableau 💻, donde crearemos visualizaciones interactivas y atractivas que contarán historias con datos 📈. Gracias a esta herramienta, podremos comunicar de manera efectiva y persuasiva los insights obtenidos durante el análisis y limpieza previo.

Al finalizar, presentaremos nuestros informes finales y visualizaciones ante la clase 🎤, demostrando nuestra habilidad para comunicar hallazgos clave y conclusiones a través de datos bien presentados.

Este proyecto nos permitirá desarrollar habilidades esenciales en ETL y visualización, lo que supone una ventaja competitiva en el campo del análisis de datos y el reporting.

---

## Sobre Data Crunchers

**Data Crunchers** nació en una pequeña oficina en la ciudad de Analytica 🏢, fundada por cinco apasionadas de los datos que compartían una visión: convertir números y estadísticas en historias fascinantes 📚. Nuestra misión es ayudar a las empresas a descubrir los secretos ocultos en sus datos y transformarlos en decisiones inteligentes y estratégicas 💡.

Un día, mientras disfrutábamos de una pizza en nuestra oficina 🍕, María Fernanda Marti Levalle tuvo una idea brillante 💡: "¿Por qué no hacemos que los datos sean tan irresistibles como esta pizza?" Y así nació nuestra filosofía: hacer que los datos sean deliciosos y fáciles de digerir.

![Logo](https://your-logo-url.com/logo.png)

Nuestro equipo está compuesto por:

- **María Fernanda Marti Levalle** - La detective de los patrones 🔍
  - [LinkedIn](https://www.linkedin.com/in/maria-fernanda-marti-levalle)
- **Diana García Martín** - La narradora de historias con datos 📖
  - [LinkedIn](https://www.linkedin.com/in/diana-garcia-martin)
- **Gloria González Muñoz** - La arquitecta del dato 🏗️
  - [LinkedIn](https://www.linkedin.com/in/gloria-gonzalez-munoz)
- **Mábel Martínez Rodríguez** - La gurú de la visualización 🎨
  - [LinkedIn](https://www.linkedin.com/in/mabel-martinez-rodriguez)
- **Patricia Elena González Gruber** - La maga de los datos 🧙‍♀️
  - [LinkedIn](https://www.linkedin.com/in/patricia-elena-gonzalez-gruber)

---

## Descripción de los Datos

El conjunto de datos contiene información sobre reservas de hoteles 🏨, incluyendo las siguientes columnas:

- **hotel:** Tipo de hotel
- **is_canceled:** Indica si la reserva fue cancelada (True) o no (False)
- **lead_time:** Número de días entre la fecha de reserva y la fecha de llegada al hotel
- **arrival_date_year:** Año de llegada al hotel
- **arrival_date_month:** Mes de llegada al hotel
- **arrival_date_week_number:** Número de la semana de llegada al hotel
- **arrival_date_day_of_month:** Día del mes de llegada al hotel
- **stays_in_weekend_nights:** Número de noches que el cliente se quedó durante el fin de semana
- **stays_in_week_nights:** Número de noches que el cliente se quedó durante la semana
- **adults:** Número de adultos que acompañaban al cliente en la reserva
- **children:** Número de niños que acompañaban al cliente en la reserva
- **babies:** Número de bebés que acompañaban al cliente en la reserva
- **meal:** Tipo de comida incluida en la reserva (BB: Desayuno, HB: Media Pensión, FB: Pensión Completa)
- **country:** País de origen del cliente
- **market_segment:** Segmento de mercado al que pertenece la reserva
- **distribution_channel:** Canal de distribución utilizado para realizar la reserva
- **is_repeated_guest:** Indica si el cliente es un huésped repetido (1) o no (0)
- **previous_cancellations:** Número de reservas canceladas por el cliente antes de esta reserva
- **previous_bookings_not_canceled:** Número de reservas no canceladas por el cliente antes de esta reserva
- **reserved_room_type:** Tipo de habitación reservada
- **assigned_room_type:** Tipo de habitación asignada en la reserva
- **booking_changes:** Número de cambios realizados en la reserva
- **agent:** Identificador del agente involucrado en la reserva
- **company:** Identificador de la compañía involucrada en la reserva
- **days_in_waiting_list:** Número de días que la reserva estuvo en lista de espera
- **customer_type:** Tipo de cliente que realizó la reserva (Transient, Contract, Group, Transient-Party)
- **adr:** Tarifa promedio diaria pagada por la reserva
- **required_car_parking_spaces:** Número de espacios de estacionamiento requeridos por el cliente
- **total_of_special_requests:** Número total de solicitudes especiales realizadas por el cliente
- **reservation_status:** Estado de la reserva (Check-Out: Salida, Canceled: Cancelada)
- **reservation_status_date:** Fecha del estado de la reserva

---

## Problema del Conjunto de Datos: Análisis y Optimización de Cancelaciones de Reservas

El hotel ha notado un aumento en el número de cancelaciones de reservas en los últimos meses 📉 y necesita comprender las causas y patrones detrás de estas cancelaciones para tomar medidas correctivas 🚀. El objetivo es llevar a cabo un análisis exhaustivo de las cancelaciones de reservas y crear visualizaciones impactantes para que la gerencia pueda identificar áreas de mejora y tomar decisiones informadas para reducir la tasa de cancelación.

---

## Preguntas a Responder

1. ¿Cuál es la tasa de cancelación de este hotel? 📊
2. ¿Ha cambiado la tasa de cancelación con el tiempo? 📈
3. ¿Se cancelan más las reservas de verano que de invierno? ❄️🌞 ¿Se cancelan más las reservas de entre semana que las de los fines de semana? 🗓️
4. Los clientes que cancelan, ¿presentan algún tipo de característica demográfica? 🌍
5. Las reservas que se hacen con mayor anticipación, ¿tienen mucho riesgo de cancelarse? ⏳
6. Las reservas que incluyen hijos, ¿tienen menor riesgo de cancelación? 👶
7. Los usuarios que realizaron algún cambio en su reserva, ¿tienen menor riesgo de cancelación? 🔄
8. ¿Cuándo el usuario ha realizado una solicitud especial, el riesgo de cancelación es menor? 📋
9. Las reservas que tienen un “adr” bajo, ¿tienen un riesgo menor de cancelación? 💵
10. ¿Existe una relación entre el número de días en lista de espera y la probabilidad de cancelación? 🕒
11. ¿En qué meses del año se produce un mayor número de cancelaciones? 📅
12. ¿Qué tipo de habitación reservada tiene una mayor tasa de cancelación? 🛏️
13. ¿Hay algún canal de distribución que presente una mayor tasa de cancelación en comparación con otros? 🌐
14. ¿Hay agentes específicos asociados con una mayor tasa de cancelación? 🕵️‍♀️
15. ¿Hay alguna empresa en particular que tenga un mayor número de cancelaciones en sus reservas? 🏢
16. ¿Qué segmento de mercado (Transient, Contract, Group, Transient-Party) tiene una mayor tendencia a cancelar las reservas? 📈
17. ¿Cómo se comparan las tasas de cancelación entre los diferentes segmentos de mercado? 📊
18. ¿Qué países tienen la mayor tasa de cancelación de reservas? 🌎
19. ¿Existe una correlación entre el número de adultos en una reserva y la tasa de cancelación? 👨‍👩‍👧‍👦
20. ¿Las reservas con una mayor duración de estadía tienen una menor o mayor tasa de cancelación? 🏖️
21. ¿Cómo afecta el número de cambios realizados en una reserva a la probabilidad de cancelación? 🔄
22. ¿Existe una relación significativa entre la tarifa promedio diaria pagada y la probabilidad de cancelación? 💰
23. ¿Cómo afecta el número total de solicitudes especiales realizadas a la tasa de cancelación? 📋
24. ¿Hay algún tipo de comida incluida en la reserva (BB, HB, FB) que tenga una mayor incidencia en la cancelación de reservas? 🍽️
25. ¿Las reservas que requieren espacios de estacionamiento tienen una menor o mayor tasa de cancelación? 🚗

---

¡Claro! Continuemos con la implementación en Tableau y las secciones finales:

---

## Implementación en Tableau

1. **Cargar Datos:**
   - Importar el archivo CSV en Tableau 📥.
   - Revisar los tipos de datos y realizar ajustes necesarios 🔍.

2. **Crear Gráficos:**
   - Usar el panel de “Sheets” para crear cada gráfico individualmente según las preguntas 📊.
   - Configurar ejes, colores y filtros 🎨.

3. **Dashboard:**
   - Combinar los gráficos en un dashboard para una presentación coherente 📋.
   - Añadir filtros y acciones interactivas 🖱️.

4. **Publicación:**
   - Publicar el dashboard en Tableau Server o Tableau Public 🌐.

5. **Análisis Adicional:**
   - Añadir anotaciones, líneas de referencia y pop-ups informativos para enriquecer la visualización ✨.

---

## Contribuciones

Para contribuir a este proyecto, por favor sigue los siguientes pasos:

1. Haz un fork del repositorio 🍴.
2. Crea una rama (`git checkout -b feature/AmazingFeature`) 🌿.
3. Realiza tus cambios (`git commit -m 'Add some AmazingFeature'`) ✍️.
4. Sube los cambios (`git push origin feature/AmazingFeature`) 🚀.
5. Abre una Pull Request 📬.


---

¡Gracias por tu interés en nuestro proyecto "Data Insights: ETL y Visualización Impactante en Tableau"! Si tienes alguna pregunta o sugerencia, no dudes en ponerte en contacto con nosotras.
