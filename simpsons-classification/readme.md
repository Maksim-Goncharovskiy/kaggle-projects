# Классификация персонажей из Симпсонов
Ссылка на соревнование: https://www.kaggle.com/competitions/journey-springfield

## Решение
Было опробовано несколько вариантов:
1. Использование кастомной архитектуры CNN, перебор ее гиперпараметров обучения. 
2. Дообучение предобученных ResNet18 и ResNet50 с заморозкой и разморозкой слоев.
3. Аугментация данных и обучение полностью размороженной ResNet50.

Наилучшим решением оказалась аугментация данных и дообучение всех слоев сети ResNet50. Это связано с тем, что в исходном датасете присутствовал сильный дисбаланс классов, который удалось уменьшить при помощи аугментации картинок для редких классов.

__Test F1-score:__ 0.98512