# CV_2023_lab5
## Семантическая сегментация

Команда:
* Епифанов Владислав
* Громова Наталья
* Хакимов Валентин
* Сыюань Хуан
## Датасет
[Датасет](https://drive.google.com/file/d/1PwK2oz_NbJU0NsT42Wr_Yv6rcZcJa5Uc/view?usp=sharing) представляет из себя набор подводных аннотированных снимков(исходные изображения - dataset/images, аннотации - dataset/masks), всего 1525 изображений и 8 категорий объектов:  
![image](https://github.com/compfee/CV_2023_lab5/assets/55783463/32eed333-d053-4378-a459-2ee1882ddd7a)

## Описание задачи
Язык программирования - Python  
Разрешено использовать любую библиотеку для машинного обучения (PyTorch, TensorFlow, Keras и др.)  
Необходимо создать модель для сегментации изображений с определением класса выделенной области  
Измерить время работы модели на тестовом датасете и посчитать необходимые метрики  
## Ограничения
Запрещено использование готовых архитектур "из коробки" одной строчкой. В коде должны быть прописаны слои вашей модели
## Метрики
Метрики оценки качества сегментации:  
IoU:  
![image](https://github.com/compfee/CV_2023_lab5/assets/55783463/b78b3cdc-4b02-48dd-a474-c8ec7845f5d2)  
​Per-class IoU:  
IoU по каждому из 8 классов  
Per-pixel accuracy:  
![image](https://github.com/compfee/CV_2023_lab5/assets/55783463/4093f270-9ca5-4fc8-a7de-10c93e1c44dd)  
 

## Результаты
Модель Unet, оптимизатор - Adam, lоss - Cross-Entropy, batch_size = 8, количество эпох - 100  

[Ссылка на решение в Google Colab](https://colab.research.google.com/drive/1l8Wgb1Id8Xbw39OiEHOJjpQ1lVCH4PIZ?usp=sharing)


Пример работы на изображении:
* Исходное изображение:
  
![real_img](https://github.com/VladislavEpifanow/CV_2023_lab5/blob/main/results/real_img3.png)
* Результат модели:
  
![model_img](https://github.com/VladislavEpifanow/CV_2023_lab5/blob/main/results/got_mask3.png)
* Реальная маска:
  
![model_img](https://github.com/VladislavEpifanow/CV_2023_lab5/blob/main/results/real_mask3.png)



Результаты на тестовой выборке:
Test IoU = 0.48

Test Channel IoU = [0.59,0 0.50, 0.87, 0.64, 0.50, 0.23, 0.47, 0.49]  

Test Pixel Accuracy = 0.65
