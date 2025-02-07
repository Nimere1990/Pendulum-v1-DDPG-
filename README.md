# Pendulum-v1: Реализация алгоритма DDPG для управления маятником
# Описание проекта
Данный проект посвящен обучению агента, использующего метод глубокого обучения DDPG (Deep Deterministic Policy Gradient), для решения задачи управления маятником в непрерывном пространстве действий. Целью является удержание маятника в вертикальном положении с достижением средней награды -200 и выше.

# Задача
В условиях нестабильного равновесия маятника необходимо разработать эффективный алгоритм, который сможет адаптивно и надежно управлять углом наклона, минимизируя при этом отрицательную награду, связанную с отклонением от вертикального положения.

# Решение
В ходе реализации была создана архитектура DDPG, включающая актера и критика:

Актер (Actor): генерирует действия на основе текущего состояния, оптимально регулируя крутящий момент.
Критик (Critic): оценивает действия агента, вычисляя Q-значение для состояния и действия.
Агент использует буфер опыта (deque) для улучшения стабильности обучения. Он обучается на примерах предыдущих шагов, что позволяет улучшать свою стратегию.

# Технологический стек

Python: основной язык программирования для реализации алгоритмов и моделей.

PyTorch: использован для построения нейронных сетей (актера и критика) благодаря своей гибкости и мощным возможностям автоматического дифференцирования.

OpenAI Gym: предоставляет среду для тестирования агента и визуализации обучения.

NumPy и Matplotlib: используются для обработки данных и визуализации графиков наград и потерь.


# Результат
В результате работы проекта был реализован DDPG агент, способный успешно управлять маятником. Обучение привело к стабильному удержанию маятника в вертикальном положении.
