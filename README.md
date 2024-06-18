## Начало работы с библиотекой [название библиотеки]
Для использования [название библиотеки] в вашем проекте Android, следуйте следующим шагам:

1. Создайте базовый проект Android
Создайте новый проект Android в вашей среде разработки. Вы можете использовать любую среду разработки, такую как Android Studio.

2. Добавьте зависимость в Gradle


3. Импортируйте ресурс XML
[Название библиотеки] позволяет использовать Векторные ассеты в формате XML. Вы можете испортировать svg файл прямо в среду Android Studio, но рекомендую использовать данный источник[https://inloop.github.io/svg2android/] для конвертации файла.
<img src="/images/image-2.jpg" alt="alt text" width="500"/>

4. Используйте метод showScheme
Для отображения схемы или другого ресурса используйте метод showScheme в вашем коде. Например:
```
val xmlResourceId = resources.getIdentifier("russia_map", "raw", requireActivity().packageName)
showScheme(xmlResourceId)
```
Замените "russia_map" на имя вашего файла ресурса.

## Примеры использования
<img src="/images/image-3.jpg" alt="alt text" width="200"/> <img src="/images/image-1.jpg" alt="alt text" width="200"/>

Sample apk находится в папке debug


## Справочник

#### Конструкторы
```
SchemeView(context: Context, attrs: AttributeSet? = null, defStyleAttr: Int = 0)
```
#### Основные методы
-------------------------
```
showScheme(xmlName: Int)
```
Отображает схему, загруженную из XML-файла.


**xmlName**: Идентификатор ресурса XML с описанием схемы.

-------------------------


```
addMarker(x: Float, y: Float, radius: Float, drawable: Drawable?) : Marker
```
Добавляет маркер (изображение) в указанные координаты.

**x**: Координата X центра маркера.
**y**: Координата Y центра маркера.
**radius**: Радиус круга маркера или размер стороны квадрата метки в пикселях.
**drawable**: Ресурс изображения для отображения в маркере.

-------------------------

```
addMarker(part: Part, radius: Float, drawable: Drawable?) : Marker
```
Добавляет маркер (изображение) в центр указанной части.

**part**: Часть, к которой добавляется маркер.
**radius**: Радиус круга маркера или размер стороны квадрата метки в пикселях.
**drawable**: Ресурс изображения для отображения в маркере.
paint: Paint для стиля маркера.

-------------------------


```
addMarker(x: Float, y: Float, radius: Float, paint: Paint?) : Marker
```
Добавляет маркер (круг) в центр указанной части.

**x**: Координата X центра маркера.
**y**: Координата Y центра маркера.
**radius**: Радиус круга маркера или размер стороны квадрата метки в пикселях.
**paint**: Paint для стиля маркера.

-------------------------

```
addMarker(part : Part, radius: Float, paint: Paint?) : Marker
```
Добавляет маркер (круг) в центр указанной части.

**part**: Часть, к которой добавляется маркер.
**radius**: Радиус круга маркера или размер стороны квадрата метки в пикселях.
**paint**: Paint для стиля маркера.

-------------------------

```
removeMarker(marker: Marker)
```
Удаляет указанный маркер.

**marker**: Маркер, который необходимо удалить.

-------------------------


```
addText(text: String, x: Float, y: Float, paint: Paint) : Text
```
Добавляет текст на указанные координаты.

**text**: Текст для добавления.
**x**: Координата X центра текста.
**y**: Координата Y центра текста.
**paint**: Paint для стиля текста.

-------------------------

```
addText(text: String, part: Part, paint: Paint) : Text
```
Добавляет текст, центрированный относительно указанной части.

**text**: Текст для добавления.
**part**: Часть, относительно которой центрируется текст.
**paint**: Paint для стиля текста.

-------------------------


```
removeText(text: Text)
```
Удаляет указанный текст.

**text**: Текст, который необходимо удалить.

-------------------------


```
clickToPart(part: Part)
```
Нажатие на часть.

**part**: Часть, которую необходимо выбрать.

-------------------------


```
selectPart(part: Part?)
```
Добавляет выделени части.

**part**: Часть, которую необходимо выбрать.

-------------------------


```
deselectPart(part: Part?)
```
Снимает выделение с указанной части.

**part**: Часть, с которой необходимо снять выделение.

-------------------------


```
multiSelectPart(part: Part)
```
Добавляет часть в текущий выбор для многократного выделения.

**part**: Часть, которую необходимо добавить в текущий выбор.

-------------------------


```
deselectAllParts()
```
Снимает выделение со всех частей.

-------------------------

```
togglePartEnabled(part: Part)
```
Изменяет состояние блокировки нажатия для указанной части.

**part**: Часть, для которой необходимо изменить состояние блокировки нажатия.

-------------------------

```
zoomToPart(part: Part)
```
Масштабирует вид к указанной части.

**part**: Часть, к которой нужно масштабировать вид.

-------------------------

```
zoomIn()
```
Увеличивает масштаб вида.

-------------------------

```
zoomOut()
```
Уменьшает масштаб вида.

-------------------------

```
resetZoom()
```
Сбрасывает масштаб вида.


-------------------------

```
setOnPartClickListener(listener: OnPartClickListener)
```
Устанавливает слушатель для обработки нажатий на части.

**listener**: Интерфейс обратного вызова для обработки нажатий на част

