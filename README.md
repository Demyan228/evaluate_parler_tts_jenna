План:

1 Так как модель дообучалась на датасете jenna, причем самом большом с таким голосом, придется тестировать модель на тех же данных,на которых она обучалась, ведь голос должен точно быть тот же, а доп записей с ним нет.

тестировать будем на случайной подвыборке из этого датасета(текст-аудио), в этом особо нет разницы.

Самое надежное оценивание tts это ручное с помощью экспертов(mos), к сожалению нам такой роскоши не дано, поэтому ограничимся оценкой качества аудио по сравнению с оригиналом.

Для этого будем использовать метрику pesq с реализацией из pytorch-pesq.

Инструкции по запуску:

1 Предпочтительней запускать notebook в колабе(если нет, просто установите используемые библиотеки)
2 для запуска нужно скачать файл train-00001-of-00010.parquet(либо любой другой, не принципиально) в https://huggingface.co/datasets/reach-vb/jenny_tts_dataset/tree/main/data
