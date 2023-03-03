$$
\Large{\text{ГУАП}} \\
\text{ФАКУЛЬТЕТ СРЕДНЕГО ПРОФЕССИОНАЛЬНОГО ОБРАЗОВАНИЯ} \\ \\ \\
\begin{aligned}
&\text{ОТЧЁТ} & & & & & & & & & & & & & & & & & \\
&\text{ЗАЩИЩЁН С ОЦЕНКОЙ}\\
&\text{ПРЕПОДАВАТЕЛЬ}
\end{aligned} \\ \\ 
{\text{преподаватель} \above{1pt} \text{должность, уч. степень, звание} } \quad {\above{1pt} \text{подпись, дата}} \quad { \text{И. А. Юрьева}\above{1pt} \text{инициалы, фамилия}} \\ \\ \\ \\
\text{ОТЧЁТЫ О ЛАБОРАТОРНЫХ РАБОТАХ} \\ \\
\text{по дисциплине: МДК 01.03} \\ \\
\begin{aligned}
&\text{РАБОТУ ВЫПОЛНИЛ} & & & & & & & & & & & & & & & & & & \\
&\text{СТУДЕНТ ГР. №}
\end{aligned} \\
{ \text{С021}\above{1pt} \quad \quad \quad \quad \quad \quad } \quad {\above{1pt} \text{подпись, дата}} \quad { \text{С. С. Гамуйло} \above{1pt} \text{инициалы, фамилия}}
$$

<div style="page-break-after: always;"></div>

## СОДЕРЖАНИЕ
<div class="dot-leader">
    <span>Лабораторная работа №1</span>
    <div class="dot-leader__dots"></div>
    <span>3</span>
</div>
<div style="page-break-after: always;"></div>

## Лабораторная работа №1

**Задание 1.** Используя ресурсы для выполнения задания, создать макеты активностей по образцу.

<img src="C:\Users\amaru\OneDrive\Downloads\Telegram Desktop\Screenshot_20230226-172739.png" alt="Screenshot_20230226-172739" style="zoom:15%;" />

<div class="counter">Привет друг</div>



<img src="C:\Users\amaru\OneDrive\Downloads\Telegram Desktop\Screenshot_20230226-172743.png" alt="Screenshot_20230226-172743" style="zoom:15%;" />

<div class="counter">Второй экран приложения (регистрация)</div>



Код программы:

(main_activity.xml)

```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.coordinatorlayout.widget.CoordinatorLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:fitsSystemWindows="true"
    tools:context=".MainActivity">

    <androidx.constraintlayout.widget.ConstraintLayout
        android:id="@+id/constraintLayout"
        android:layout_width="260dp"
        android:layout_height="wrap_content"
        android:layout_gravity="center">

        <LinearLayout
            android:gravity="center"
            android:id="@+id/linearLayout6"
            android:layout_width="wrap_content"
            android:layout_height="50dp"
            android:orientation="horizontal"
            app:layout_constraintBottom_toTopOf="@id/linearLayout"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toTopOf="parent">

            <android.widget.TextView
                android:id="@+id/textView"
                android:layout_width="wrap_content"
                android:layout_height="match_parent"
                android:gravity="center"
                android:text="@string/soccer_skills"
                android:textAlignment="center"
                android:textFontWeight="800"
                android:textSize="14pt"
                app:layout_constraintEnd_toEndOf="parent"
                app:layout_constraintStart_toStartOf="parent"
                app:layout_constraintTop_toTopOf="parent" />

            <ImageView
                android:layout_width="48dp"
                android:layout_height="48dp"
                android:layout_marginStart="10dp"
                android:src="@drawable/baseline_sports_basketball_24" />
        </LinearLayout>

        <LinearLayout
            android:id="@+id/linearLayout"
            android:layout_width="match_parent"
            android:layout_height="100dp"
            android:foregroundTint="@color/material_dynamic_primary60"
            android:orientation="horizontal"
            app:layout_constraintTop_toBottomOf="@+id/linearLayout6">

            <ImageView
                android:layout_width="24dp"
                android:layout_height="24dp"
                android:layout_gravity="center_vertical"
                android:src="@drawable/outline_person_24" />

            <com.google.android.material.textfield.TextInputLayout
                android:id="@+id/textField"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_gravity="center_vertical"
                android:layout_marginLeft="24dp">

                <com.google.android.material.textfield.TextInputEditText
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:hint="Email" />

            </com.google.android.material.textfield.TextInputLayout>
        </LinearLayout>

        <LinearLayout
            android:id="@+id/linearLayout2"
            android:layout_width="match_parent"
            android:layout_height="100dp"
            android:orientation="horizontal"
            app:layout_constraintTop_toBottomOf="@+id/linearLayout">

            <ImageView
                android:layout_width="24dp"
                android:layout_height="24dp"
                android:layout_gravity="center_vertical"
                android:src="@drawable/baseline_password_24" />

            <com.google.android.material.textfield.TextInputLayout
                android:id="@+id/textField2"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_gravity="center_vertical"
                android:layout_marginStart="24dp">

                <com.google.android.material.textfield.TextInputEditText
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:hint="Password" />

            </com.google.android.material.textfield.TextInputLayout>

        </LinearLayout>

        <CheckBox
            android:id="@+id/checkBox"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:checked="true"
            android:text="Remember me"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toBottomOf="@+id/linearLayout2" />

        <Button
            android:id="@+id/button"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:gravity="center"
            android:onClick="mySecondActivity"
            android:text="Sign in"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toBottomOf="@+id/checkBox" />

        <TextView
            android:id="@+id/textView2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Forgot password?"
            android:textColor="@color/material_dynamic_primary50"
            app:layout_constraintBottom_toTopOf="@+id/button"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toBottomOf="@+id/checkBox" />

        <TextView
            android:id="@+id/textView4"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Don't have an account?"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toBottomOf="@+id/button" />

        <TextView
            android:id="@+id/textView6"
            android:layout_width="wrap_content"
            android:layout_height="24dp"
            android:onClick="onSignupAct"
            android:text="Sign up now"
            android:textColor="@color/material_dynamic_primary50"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toBottomOf="@+id/textView4"
            android:layout_marginTop="16dp" />

    </androidx.constraintlayout.widget.ConstraintLayout>
</androidx.coordinatorlayout.widget.CoordinatorLayout>
```



(activity_signup.xml)

```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.coordinatorlayout.widget.CoordinatorLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:fitsSystemWindows="true"
    tools:context=".SignupActivity">

    <androidx.constraintlayout.widget.ConstraintLayout
        android:id="@+id/constraintLayout"
        android:layout_width="260dp"
        android:layout_height="563dp"
        android:layout_gravity="center">

        <android.widget.TextView
            android:id="@+id/textView"
            android:layout_width="match_parent"
            android:layout_height="0dp"
            android:gravity="center"
            android:text="@string/soccer_skills"
            android:textAlignment="center"
            android:textFontWeight="800"
            android:textSize="14pt"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toTopOf="parent" />

        <LinearLayout
            android:id="@+id/linearLayout"
            android:layout_width="match_parent"
            android:layout_height="100dp"
            android:orientation="horizontal"
            app:layout_constraintTop_toBottomOf="@+id/textView">

            <ImageView
                android:layout_width="24dp"
                android:layout_height="24dp"
                android:layout_gravity="center_vertical"
                android:src="@drawable/outline_person_24"
                android:tint="@color/design_default_color_on_primary"  />

            <com.google.android.material.textfield.TextInputLayout
                android:id="@+id/textField"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_gravity="center_vertical"
                android:layout_marginLeft="24dp">

                <com.google.android.material.textfield.TextInputEditText
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:hint="Name" />

            </com.google.android.material.textfield.TextInputLayout>
        </LinearLayout>

        <LinearLayout
            android:id="@+id/linearLayout2"
            android:layout_width="match_parent"
            android:layout_height="100dp"
            android:orientation="horizontal"
            app:layout_constraintTop_toBottomOf="@+id/linearLayout3">

            <ImageView
                android:layout_width="24dp"
                android:layout_height="24dp"
                android:layout_gravity="center_vertical"
                android:src="@drawable/baseline_password_24"
                android:tint="@color/design_default_color_on_primary" />

            <com.google.android.material.textfield.TextInputLayout
                android:id="@+id/textField2"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_gravity="center_vertical"
                android:layout_marginStart="24dp">

                <com.google.android.material.textfield.TextInputEditText
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:hint="Password" />

            </com.google.android.material.textfield.TextInputLayout>
        </LinearLayout>

        <LinearLayout
            android:id="@+id/linearLayout4"
            android:layout_width="match_parent"
            android:layout_height="100dp"
            android:orientation="horizontal"
            app:layout_constraintTop_toBottomOf="@+id/linearLayout2">

            <ImageView
                android:layout_width="24dp"
                android:layout_height="24dp"
                android:layout_gravity="center_vertical"
                android:src="@drawable/baseline_password_24"
                android:tint="@color/design_default_color_on_primary" />

            <com.google.android.material.textfield.TextInputLayout
                android:id="@+id/textField4"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_gravity="center_vertical"
                android:layout_marginStart="24dp">

                <com.google.android.material.textfield.TextInputEditText
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:hint="Confirm password" />

            </com.google.android.material.textfield.TextInputLayout>
        </LinearLayout>

        <LinearLayout
            android:id="@+id/linearLayout3"
            android:layout_width="match_parent"
            android:layout_height="100dp"
            android:orientation="horizontal"
            app:layout_constraintTop_toBottomOf="@+id/linearLayout">

            <ImageView
                android:layout_width="24dp"
                android:layout_height="24dp"
                android:layout_gravity="center_vertical"
                android:src="@drawable/baseline_alternate_email_24"
                android:tint="@color/design_default_color_on_primary"/>

            <com.google.android.material.textfield.TextInputLayout
                android:id="@+id/textField3"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_gravity="center_vertical"
                android:layout_marginLeft="24dp">

                <com.google.android.material.textfield.TextInputEditText
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:hint="Email" />

            </com.google.android.material.textfield.TextInputLayout>
        </LinearLayout>

        <Button
            android:id="@+id/button2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Sign up"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toBottomOf="@+id/linearLayout4" />

    </androidx.constraintlayout.widget.ConstraintLayout>
</androidx.coordinatorlayout.widget.CoordinatorLayout>
```



**Задание 2.** Создать LinearLayout по образцу (Вариант 2)

<img src="C:\Users\amaru\AppData\Roaming\Typora\typora-user-images\image-20230226173317777.png" alt="image-20230226173317777" style="zoom:33%;" />



<img src="C:\Users\amaru\OneDrive\Downloads\Telegram Desktop\Screenshot_20230226-172749.png" alt="Screenshot_20230226-172749" style="zoom:15%;" />

<div class="counter">Итоговая разметка (Material You цвета)</div>



(activity_second.xml, вторая активити)

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".SecondActivity"
    android:orientation="vertical">

        <TextView
            android:id="@+id/textView6"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:background="@color/material_dynamic_tertiary50"
            android:gravity="center"
            android:text="1"
            android:textAlignment="center"
            android:textColor="@color/design_default_color_on_primary"
            android:textSize="24pt" />

        <Space android:layout_height="wrap_content" android:layout_width="match_parent"
            android:layout_weight="4">
        </Space>

        <TextView
            android:id="@+id/textView7"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:background="@color/material_dynamic_primary60"
            android:gravity="center"
            android:text="2"
            android:textAlignment="center"
            android:textColor="@color/design_default_color_on_primary"
            android:textSize="24pt" />

        <TextView
            android:id="@+id/textView8"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:background="@color/material_dynamic_secondary60"
            android:gravity="center"
            android:text="3"
            android:textAlignment="center"
            android:textColor="@color/design_default_color_on_primary"
            android:textSize="24pt" />
</LinearLayout>
```





**Контрольные вопросы**

1. Как задается пространство имен в xml?

Для задания пространства имен в xml для Android-приложения используется атрибут xmlns, который добавляет ссылку на пространство имен.

2. Какая функциональность определена в пространстве имен xmlns:android?

Функциональность пространства имен xmlns:android включает поддержку всех атрибутов и виджетов, доступных для использования в разработке мобильных приложений под Android.

3. Какие типы измерений можно использовать при разработке приложений под Android?

При разработке мобильных приложений под Android можно использовать различные типы измерений, в том числе: пиксели, дюймы, проценты, dp, sp, pt, mm, и проценты экрана.

4. Какая из единиц измерений является предпочтительной и почему?

В процессе разработки мобильных приложений для платформы Android предпочтительной единицей измерения является dp (device-independent). Это связано с тем, что использование dp позволяет более гибко и правильно адаптировать макеты и интерфейсы для большого числа различных устройств.

5. Что собой представляет LinearLayout?

LinearLayout - это графический контейнер, используемый для размещения элементов интерфейса в виде последовательного ряда. Этот контейнер позволяет задать ориентацию для внутренних элементов (горизонтально или вертикально).

6. Атрибут android:layout_weight определяет ….

Атрибут android:layout_weight используется для назначения веса при распределении пространства между элементами в линейном макете. Вес каждого элемента используется для определения пропорциональной доли пространства, которую занимает элемент.

7. Атрибут android:layout_gravity необходим …

Атрибут android:layout_gravity используется для установки гравитации (притягивания к любой стороне) для любого элемента в макете. Это позволяет расположить элементы внутри линейного макета по желаемому направлению.

8. Атрибут android:gravity *…*

Используется для определения гравитации для всех дочерних элементов контейнера

9. Padding - это …

Padding — это минимальное расстояние между границами контейнера и дочерними элементами. Можно задать для каждой из сторон отдельные значения.

10. Применение атрибута android:layout_margin …

Атрибут android:layout_margin используется для задания пространства между границами элемента и соседними контейнерами или элементами. Он также может использоваться для задания отступа от границы области для расположения внутри контейнера.

11. Назначение match_parent …

Атрибут match_parent используется для назначения элементу размера родительского контейнера. Это позволяет контролировать, чтобы дочерние элементы занимали все доступное пространство внутри контейнера.

12. Назначение wrap_content…

Атрибут wrap_content используется для назначения элементу минимального размера, необходимого для показа дочерних элементов. Это позволяет дочерним элементам располагаться в доступном пространстве контейнера, так что контейнер изменяет размер в зависимости от размера дочерних элементов.

13. Какие свойства TextView, EditText и Button были использованы при выполнении индивидуального задания.

Gravity, height-width, constraints, text-align, onClick
