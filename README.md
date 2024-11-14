# FastReLU
Мини Диссертация


#Введение:

Я подготовил небольшую диссертацию о работе своей интерпретации функции ReLU , она является наиболее часто используемой функцией наравне с сигмоидой и т.п. . Определяется ReLU как - f(x)=max(0,x) , но она имеет и один минус - "Умирающие нейроны" если входное значение нейрона отрицательно , его выход = 0, соответственно и градиент обучения этого нейрона = 0. И зачастую это приводит к тому , что нейрон перестает обновляться и соответственно становится "овощем". Моя интерпретация FastReLU - должна решить эту проблему .

#Определение и почему она должна помочь:

Моя интерпретация определяется как f(x)=x+a⋅tanh(x) , где a = небольшому коофициенту , например 0.01 , 0,001 , etc.

Почему же она решить проблему? Наша функция решает проблему обеспечивая небольшой градиент для отрицательных входных значений. То есть в отличи еот ReLU, которая полностью обнуляет отрицательные значения, наша функ. использует tanh, он позволяет плавнейшим образом перейти от отрицательности к положительным значениям. Это и позволит нашим значениям не быть абсолютно = 0 , что исправляет нашу проблему с "овощными нейронусами".


