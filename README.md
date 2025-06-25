## ✅ **Conclusión del proyecto: Análisis y predicción de rendimiento ofensivo en jugadores de fútbol**

Este proyecto consistió en analizar jugadores ofensivos del videojuego FIFA 21 utilizando **Polars** para el procesamiento de datos, **Seaborn** para la visualización y **Scikit-learn** para crear un modelo de predicción.

### 📌 Objetivo:

Predecir si un jugador **podría marcar más de 10 goles** en una temporada, usando sus estadísticas como edad, pase, tiro, regate, y potencial.

### 🔍 Datos:

* Dataset: `players_21.csv` de Kaggle.
* Jugadores filtrados por posiciones ofensivas: `"ST"`, `"CF"`, `"LW"`, `"RW"`, `"CAM"`.
* Variables usadas: `shooting`, `passing`, `dribbling`, `age`, `potential`, etc.
* La variable objetivo (`will_score_10+`) fue **simulada**, usando:
  `shooting > 70 and overall > 75`

---

## 📊 **Último resultado del modelo Random Forest**

```
              precision    recall  f1-score   support

           0       1.00      1.00      1.00      1909
           1       0.95      0.96      0.95       144

    accuracy                           0.99      2053
   macro avg       0.97      0.98      0.97      2053
weighted avg       0.99      0.99      0.99      2053
```

---

### 🧠 Interpretación:

* El modelo logra **un 99 % de precisión global**, prediciendo correctamente si un jugador tiene buen potencial goleador según sus stats.
* **Clase 1 (marcará 10+ goles)** fue detectada con un 95 % de precisión y 96 % de recall.
* Sin embargo, este rendimiento alto se debe en parte a que la variable objetivo fue construida **a partir de las mismas estadísticas usadas como entrada** (por ejemplo, `shooting`, `overall`), lo cual genera un caso de *overfitting artificial*.

---

## ✅ Conclusión final:

> Este proyecto demostró cómo aplicar un flujo de trabajo completo de análisis de datos deportivos en Python, desde la carga y limpieza eficiente con Polars, visualización con Seaborn y modelado predictivo con Scikit-learn.
>
> **El modelo predice con alta precisión, pero se recomienda usar etiquetas reales (goles anotados por temporada) para validar su utilidad en un contexto real.**

---

¿Te gustaría que te lo exporte como un informe en PDF o Word? ¿O prefieres subirlo como notebook público en Kaggle o GitHub?
