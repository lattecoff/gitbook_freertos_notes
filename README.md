# gitbook_freertos_notes

Создание задачи
```c
portBASE_TYPE xTaskCreate( pdTASK_CODE pvTaskCode,
                           const signed portCHAR * const pcName,
                           unsigned portSHORT usStackDepth,
                           void *pvParameters,
                           unsigned portBASE_TYPE uxPriority,
                           xTaskHandle *pxCreatedTask );
```

``pvTaskCode`` -  Параметр pvTaskCode - простой указатель на функцию (т. е. просто имя функции).

``const signed portCHAR * const pcName`` - Описательное имя для задачи. Оно никак не используется внутри FreeRTOS, и нужно только для целей отладки.


``unsigned portSHORT usStackDepth`` - Значение usStackDepth указывает количество слов, которое можно сохранить в стеке, а не количество байт.

``void *pvParameters`` - Значение, указанное в pvParameters, будет передано в задачу.

``unsigned portBASE_TYPE uxPriority`` - 	Задает приоритет, с которым будет выполняться задача. Приоритеты могут быть назначены в любое значение от 0 минимальный приоритет до (configMAX_PRIORITIES – 1) максимальный приоритет.

``xTaskHandle *pxCreatedTask`` - Параметр pxCreatedTask может использоваться для передачи наружу хендла созданной задачи.

1. ``pdTRUE`` показывает, что задача успешно создана.
2. ``errCOULD_NOT_ALLOCATE_REQUIRED_MEMORY`` показывает, что задача не создана, так как в куче (heap) недостаточно свободной памяти для FreeRTOS
 
 
 
 