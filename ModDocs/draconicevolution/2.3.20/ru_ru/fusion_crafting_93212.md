§align:center
##### §nСлияние§n

§img[https://raw.githubusercontent.com/brandon3055/Project-Intelligence-Docs/master/Assets/Draconic%20Evolution/Fusion%20Crafting/Fusion%20Crafting.jpg]{width:100%}
§rule{colour:0x606060,height:3,width:100%}
Слияние - это процесс, использующий большое количество энергии для объединения предметов на атомном уровне.

#####§nКак это работает:

######§nРецепты
Каждый рецепт требует 3 вида компонентов:

Катализаторы,
Ингредиенты слияния
И... энергия

Катализатор помещают в ядро, а каждый из ингредиентов - в отдельный Инжектор слияния. И если рецепт существует, он отобразится в интерфейсе ядра, а также появится кнопка, запускающая процесс создания.

Для разных рецептов используются разные уровни слияния. В настоящее время существует 4 уровня слияния: Базовый, Виверны, Дракона и Хаоса.
Уровень Вашей конструкции определяется уровнем ее инжекторов.

######§nСоздание
§o(Просто расслабьтесь и наслаждайтесь зрелищем!)§r
Процесс создания предмета проходит в две стадии: "Зарядка" и "Создание".

Во время заряжающей стадии всем активным инжекторам потребуется энергия. По завершению зарядки начнется вторая стадия - создающая.
Создающая стадия будет работать в течение нескольких секунд, после чего результат процесса будет помещен в выходной слот ядра.

######§nАвтоматизация
Crafting can beinitiated by aplying a redstone pulse.
If you are using Applied Energistics the recommended configuration is to have the ME interface bellow the core. Then attach a pipe of some sort to the side of the interface and use that to supply the injectors. The injectors also need to be in single item mode.

When creating the pattern make sure the catalist is the first item in the pattern as that is the first item. When crafting the interface will first try to push items to the above inventory (the core) as the catalyst is the first item in the recipe it will be pushed into the core. The remaining items will be sent through the attached pipe to the crafting injectors.

Make sure the interface is in blocking mode and pull the crafting result out of the core using whatever method you see fit.

######§nВывод сигнала компаратором
Присоединив компаратор к самому ядру, Вы сможете проверять состояние процесса при помощи редстоуна. Выходной сигнал компаратора будет соответствовать текущему состоянию ядра.

0 - Нет рецепта и выходной слот пуст. 
1 - Рецепт действителен.                         
1 > 15 - Идет создание.        
15 - Создание завершено/Предмет в выходном слоте.


§rule{colour:0x606060,height:3,width:100%,top_pad:0}
###### §nРецепт§n
§recipe[draconicevolution:fusion_crafting_core]{border_colour:0xc6c6c6}
§rule{colour:0x606060,height:3,width:100%,top_pad:0}