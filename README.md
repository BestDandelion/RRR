РУССКИЙ

1. Обзор Языка
2. HAPL позволяет управлять программой Brainfuck, используя жесты рук. Каждому распознаваемому жесту соответствует определенная команда Brainfuck. Это позволяет создавать и выполнять Brainfuck-программы без использования клавиатуры.
3. Принцип Работы
• Распознавание Жестов: Программа использует MediaPipe для распознавания жестов рук, отображаемых веб-камерой.
• Сопоставление Жестов с Командами: Распознанные жесты сопоставляются с соответствующими командами Brainfuck, согласно таблице выше.
• Выполнение Brainfuck-кода: Распознанные команды Brainfuck выполняются в интерпретаторе Brainfuck, который хранится в памяти (например, массив ячеек).
4. Интерпретация Команд Brainfuck
+: Увеличивает значение текущей ячейки памяти на 1.
-: Уменьшает значение текущей ячейки памяти на 1.
>: Перемещает указатель (pointer) на следующую ячейку памяти.
<: Перемещает указатель на предыдущую ячейку памяти.
.: Выводит ASCII-символ, соответствующий значению текущей ячейки памяти.
,: Запрашивает ввод одного ASCII-символа, который сохраняется в текущей ячейке памяти.
[: Начало цикла. Цикл выполняется, пока значение текущей ячейки не станет равно 0.
]: Конец цикла. Если значение текущей ячейки не равно 0, указатель перемещается обратно к соответствующей [.
6. Ограничения и Улучшения
• Точность Распознавания: Точность распознавания жестов зависит от освещения, качества камеры и положения рук.
• Сложные Программы: Создание сложных Brainfuck-программ может быть трудоемким, так как жесты нужно показывать последовательно.
• Многопоточность: Можно улучшить производительность, используя многопоточность для одновременного распознавания жестов и выполнения Brainfuck-кода.
• Визуализация: Добавление визуальной обратной связи (например, отображение текущей ячейки памяти, выполняемых команд) улучшит удобство использования.
• Более сложные жесты: Рассмотрите возможность добавления жестов для других команд Brainfuck или для управления интерпретатором.
7. Настройка
• Camera: Настройте номер камеры (если у вас несколько) в коде Python (например, cv2.VideoCapture(0)).
• Минимальная уверенность: Настройте min_detection_confidence и min_tracking_confidence в MediaPipe для изменения чувствительности распознавания. Более высокие значения требуют более точного распознавания, но могут снизить скорость работы.

ENGLISH

1. Language Overview
2. HAPL allows you to control the Brainfuck program using hand gestures. Each recognized gesture corresponds to a specific Brainfuck command. This allows you to create and execute Brainfuck programs without using a keyboard.
3. Working Principle
• Gesture Recognition: The program uses MediaPipe to recognize hand gestures displayed by the webcam.
• Matching Gestures with Commands: Recognized gestures are matched with the corresponding Brainfuck commands, according to the table above.
• Execution of the Brainfuck code: Recognized Brainfuck commands are executed in the Brainfuck interpreter, which is stored in memory (for example, an array of cells).
4. Interpretation of Brainfuck commands
+: Increases the value of the current memory location by 1.
-: Reduces the value of the current memory location by 1.
>: Moves the pointer to the next memory location.
<: Moves the pointer to the previous memory location.
.: Outputs the ASCII character corresponding to the value of the current memory location.
.: Requests the input of a single ASCII character, which is stored in the current memory location.
[: Start of the cycle. The loop runs until the value of the current cell is 0.
]: End of the loop. If the value of the current cell is not 0, the pointer moves back to the corresponding [.
6. Limitations and Improvements
• Recognition Accuracy: The accuracy of gesture recognition depends on lighting, camera quality, and hand position.
• Complex Programs: Creating complex Brainfuck programs can be time-consuming, as gestures need to be shown sequentially.
• Multithreading: Performance can be improved by using multithreading to simultaneously recognize gestures and execute Brainfuck code.
• Visualization: Adding visual feedback (for example, displaying the current memory location, running commands) will improve usability.
• More complex gestures: Consider adding gestures for other Brainfuck commands or to control the interpreter.
7. Setting up
• Camera: Set up the camera number (if you have several) in the Python code (for example, cv2.VideoCapture(0)).
• Minimal confidence: Configure min_detection_confidence and min_tracking_confidence in MediaPipe to change the recognition sensitivity. Higher values require more accurate recognition, but they can reduce the speed of operation.
