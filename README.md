# LearningWindowsForms ![C++](https://img.shields.io/badge/c++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![image](https://github.com/spectrummmm/LearningWindowsForms/assets/133951457/78f767be-110e-405e-a09f-0b33e585c542)

## Актуальность
В курсе обучения программированию я изучил основы работы в ***Windows Forms***. <p> ***WF*** представляет из себя интерфейс программирования приложений. Через него можно создавать мультиплатформенные приложения с некоторым оформлением. В основном для этого используется язык ***"C++"***
</p>
 
## Процесс обучения
Для начала я создал проект .NET, изучил основные фукции и возможности программирования через ***Windows Forms***. Я изучил как создавать фунции, графические элементы, а так же научился редактировать их.
Мне понравился достаточно понятный интерфейс: к примеру чтобы изменить размер окна моего приложения, достаточно всего то открыть вкладку с настройками экрана и изменить пункт с размерами *( а не лезть в код и искать это вручную)*
<p>
 </p>
 
![image](https://github.com/spectrummmm/LearningWindowsForms/assets/133951457/a17982ec-7f7f-4a26-8ed5-ec595c5afc59)

 
Затем я начал делать **калькулятор!!!**. Я добавил несколько элементов : 5 элементов **button** ( кнопка) а так же **texbox** ( для ввода чисел и вывода результатов). Редактировал их под свои нужды.


<Img src="https://github.com/spectrummmm/LearningWindowsForms/assets/133951457/8557dd3b-e059-422a-81d4-7c7b64a330ff" vertical-align: bottom>
 

 Потом я создал каждой кнопке собственное событие : при нажатии на кнопку ***"+"***,  число, записанное в окно кидается в буфер, и окно очищается. Аналогично сделал для других кнопок.
 ```cpp
	private: System::Void buttonPlus_Click(System::Object^ sender, System::EventArgs^ e) {
	number1 = Convert::ToInt32(textResult->Text);
	operation = "+";
	textResult->Clear();
```
А тут реализован вывод текста
```cpp
private: System::Void buttonEqual_Click(System::Object^ sender, System::EventArgs^ e) {
	number2 = Convert::ToInt32(textResult->Text);
	textResult->Clear();
	if (operation == "+") textResult->Text = Convert::ToString(number1 + number2);
	if (operation == "-") textResult->Text = Convert::ToString(number1 - number2);
	if (operation == "*") textResult->Text = Convert::ToString(number1 * number2);
	if (operation == "/") textResult->Text = Convert::ToString(number1 / number2);
 ```
 Затем мы вводим второе число в окно и нажимаем ***"="*** (при этом достаётся первое число из буфера и выполняется та или иная операция). Полученный результат мы выводим опять в **textbox** .

 ***Кстати введённые данные проверяются на то , числа ли они ( если ввести текст, то приложение выдаст ошибку )***
 
 ```cpp
 private: System::Void textResult_KeyUp(System::Object^ sender, System::Windows::Forms::KeyEventArgs^ e) {
	if ((e->KeyValue) < 48 || e->KeyValue > 59) {
		textResult->Text = str;
	}
}
```

 **Ну и финальный вид калькулятора:**
 
 ![image](https://github.com/spectrummmm/LearningWindowsForms/assets/133951457/bfeb0292-51d7-487a-acec-82d0dad26905)


## Выводы
Как мне показалось, ***Windows Forms*** является неплохим ресурсом для создания простеньких приложений и незамысловатых оформлений. Если для учебных целей мне нужно будет сделать калькулятор (с интерфейсом) для рассчета формул, то я буду делать это в **Windows Forms**
  
## Контакты
- VK : [Трикин Максим](https://vk.com/causeimanikeboy)
- [Telegram](https://t.me/nihuya_sebe_bigboy)
- Почтовый ящик : max3kin24@mail.ru
