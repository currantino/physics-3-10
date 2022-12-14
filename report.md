# Отчет по лабораторной работе 3.10
## ИЗУЧЕНИЕ СВОБОДНЫХ ЗАТУХАЮЩИХ ЭЛЕКТРОМАГНИТНЫХ КОЛЕБАНИЙ

### Цель работы: 
Изучение основных характеристик свободных затухающих колебаний.     

### Требуемое оборудование 
- Блок генератора напряжений ГН1;
- Осциллограф ОЦЛ2;
- Стенд с объектом исследования С3-ЭМ01;
- Проводники Ш4/Ш2 (4 шт), Ш2/Ш2 (3 шт),2Ш4/BNC (2 шт).

### Характеристики установки
  - $L = 10\  мгН \pm 10\% $
  - $C_{1} = 0,022 \ мкФ \pm10\%$
  - $C_{2} = 0,033 \ мкФ \pm10\%$
  - $C_{3} = 0,047 \ мкФ \pm10\%$
  - $C_{4} = 0,47 \ мкФ \pm10\%$

# Обработка измерений  
1. Вычислим логарифмический декремент по формуле $\lambda = \dfrac{1}{n}\ln(\dfrac{U_{i}}{U_{i+n}})$ и построим график зависимости $\lambda(R_{M})$, где $R_{M}$ - сопротивление из магазина

|![image](https://raw.githubusercontent.com/currantino/physics-3-10/master/plots/lambda(RM).png)|
|:--:|
|Рис. 1|

Если аппроксимировать начальный участок графика ($R_{M} \leq 100\ \Omega$) прямой, получим $\lambda(R_{M}) \approx 0,005R_{M} + 0,309 $

|![image2](https://raw.githubusercontent.com/currantino/physics-3-10/master/plots/lambda(Rm)2.png)|
|:--:|
|Рис. 2|


  $R = R_{M} + R_{0} \implies R_{0} = -R_{M}|_{\lambda=0}$, где $R$ - полное сопротивление контура, а $R_{0}$ - его собственное сопротление.

  $\lambda = 0$ при $R_{M} \approx -60,355\ \Omega \implies R_{0} \approx 60,355$

1. По формулам $R = R_{M} + R_{0}$ и $\lambda \approx \pi R\cdot\sqrt{\dfrac{C}{L}}$ вычислим полное сопротивление контура $R$ и индуктивность $L_{exp}$ для малых сопротивлений из магазина ($R_{M} \leq 100$). $\left<L_{exp}\right> = 0,0083 \ Гн$, что отличается от значения, указанного на установке $L=0,010 \ Гн$ на $0,017 \ Гн$

2. Теперь рассмотрим результаты эксперимента при сопротивлении магазина $R_{M} \in \{0 \ \Omega, 200 \ \Omega, 400 \ \Omega\}$. По формулам $ T = \dfrac{2\pi}{\sqrt{\dfrac{1}{LC} - \dfrac{R^{2}}{4L^{2}}}} $ и $ R = R_{M} + R_{0} $ вычислим период колебаний в контуре.
   $ R_{M} = 0\ \Omega: T_{exp} = 0,000090\ s; T_{eval} = 0,000080\ s $
   $ R_{M} = 200 \ \Omega: T_{exp} = 0,000097\ s; T_{eval} = 0,000097\ s $
   $ R_{M} = 400\ \Omega: T_{exp} = 0,000100\ s; T_{eval} = 0,000080\ s $

3. Вычислим добротность контура $Q$ по формуле $Q=\dfrac{2\pi}{1 - e^{-2\lambda}}$ и построим график зависимости $Q(R)$

|![image3](https://raw.githubusercontent.com/currantino/physics-3-10/master/plots/Q(R).png)|
|:--:|
|Рис. 3|

 5. Перейдем к обработке результатов второй части эксперимента при $R_{M} = 0\ \Omega$.
Используя найденное выше значение $\left<L_{exp}\right> $ и собственное сопротивление контура $R_{0}$ по формуле $ T = \dfrac{2\pi}{\sqrt{\dfrac{1}{LC} - \dfrac{R^{2}}{4L^{2}}}} $ вычислим теоретический период колебаний $ T_{theor} $ для разных значений $C$.

А теперь вычислим $ T_{Thompson} $ по формуле Томпсона $ T = 2\pi\sqrt{LC}$ и построим графики зависимостей $T_{exp},\ T_{theor},\ T_{Thompson} $ от емкости конденсатора $C$.

|![image4](https://raw.githubusercontent.com/currantino/physics-3-10/master/plots/T(C).png)|
|:--:|
|Рис. 4|

### Выводы и анализ результатов работы

При выполнении данной лабораторной работы были получены значения логарифмического декремента $\lambda$ при разных сопротивлениях магазина $R_{M}$. На графике 1 видно, что зависимость $\lambda(R_{M})$ является экспоненциальной. Также было рассчитано собственное сопротивление контура $R_{0}\approx60,35\ \Omega$ . 
Далее получено значение индуктивности: $ L\approx8,3 mH $, что почти совпадает со значением $ L=10\ mH $, указанным на лабораторном стенде. Следующем заданием было рассчитать периоды при разных сопротивлениях магазина $ R_{M} $. Результаты близки к экспериментальным.
Критическое сопротивление, полученное в ходе расчетов: $ R_{crit}\approx1230,69\ \Omega $, что отличается от полученного в ходе замеров на $ 23,2\ \Omega $ . 
Зависимость добротности $ Q $ от полного сопротивления контура $ R $ является обратной экспоненциальной, а различие теоретических и экспериментальных периодов колебаний при различных емкостях конденсатора $ C $ также близки.
Значения периода колебаний $ T_{theor}, T_{exp}, T_{Thompson} $ близки, что демонстрирует рис. 4.










### Результаты обработки измерений

### Таблица 1
   
| $R_{M}, \ \Omega$ | $T, \ s$        | $ 2U_{i} ,\ V$  | $2U_{i + n}, \ V $| $n$ | $\lambda$ | $R, \Omega$        | $L,\ H$        | $T_{eval},\ s  $| $Q, \ J$       |
|-----|----------|-----|-----|---|-----------|----------|----------|-------------|----------|
| 0   | 0.000090 | 6.4 | 2.4 | 3 | 0.326943  | 60.35554 | 0.007400 | 8.03E-05    | 13.09054 |
| 10  | 0.000100 | 6.0 | 2.0 | 3 | 0.366204  | 70.35554 | 0.008014 | 8.36E-05    | 12.10050 |
| 20  | 0.000098 | 5.9 | 1.7 | 3 | 0.414775  | 80.35554 | 0.008149 | 8.43E-05    | 11.14526 |
| 30  | 0.000099 | 5.7 | 1.4 | 3 | 0.467998  | 90.35554 | 0.008094 | 8.41E-05    | 10.33750 |
| 40  | 0.000100 | 5.5 | 1.3 | 3 | 0.480795  | 100.3555 | 0.009460 | 9.09E-05    | 10.17166 |
| 50  | 0.000100 | 5.3 | 1.0 | 3 | 0.555902  | 110.3555 | 0.008557 | 8.65E-05    | 9.363421 |
| 60  | 0.000099 | 5.1 | 0.8 | 3 | 0.617461  | 120.3555 | 0.008250 | 8.51E-05    | 8.860254 |
| 70  | 0.000098 | 5.0 | 0.6 | 3 | 0.706755  | 130.3555 | 0.007387 | 8.06E-05    | 8.303273 |
| 80  | 0.000097 | 4.8 | 0.7 | 3 | 0.641764  | 140.3555 | 0.010386 | 9.55E-05    | 8.691137 |
| 90  | 0.000100 | 4.6 | 0.5 | 3 | 0.739734  | 150.3555 | 0.008970 | 8.89E-05    | 8.136297 |
| 100 | 0.000098 | 4.4 | 0.3 | 3 | 0.895192  | 160.3555 | 0.006967 | 7.86E-05    | 7.541897 |
| 200 | 0.000097 | 3.2 | 0.3 | 2 | 1.183562  | 260.3555 | 0.010507 | 9.73E-05    | 6.933170 |
| 300 | 0.000099 | 2.3 | 0.2 | 2 | 1.221174  | 360.3555 | 0.018907 | 0.000131    | 6.881584 |
| 400 | 0.000100 | 1.6 | 0.1 | 1 | 2.772589  | 460.3555 | 0.005986 | 8.04E-05    | 6.307825 |

#### Таблица 2
| $C,\ F$       |$ T_{exp},\ s $  |$ T_{theor},\ s $ | $ \delta{T} = \dfrac{T_{exp} - T_{theor}}{T_{theor}}, \%  $ |
|---------|----------|----------|----------|
| 2.2E-08 | 0.000099 | 8.52E-05 | 0.162494 |
| 3.3E-08 | 0.000118 | 0.000104 | 0.130655 |
| 4.7E-08 | 0.000140 | 0.000125 | 0.123182 |
| 4.7E-07 | 0.000420 | 0.000404 | 0.040485 |