# Bibliografía y recursos — Clase 1

**Reconocimiento de Patrones en Bioinformática — Maestría en Bioinformática y Biología de Sistemas, UNQ**

---

## 📚 Lectura recomendada antes de la clase (~30 min)

- **Altman, N. & Krzywinski, M. (2018).** The curse(s) of dimensionality. *Nature Methods* 15: 399–400.
  - 🎯 **La lectura ideal previa a la clase.** Dos páginas en Nature Methods que cubren exactamente los temas del día: data sparsity, multicolinealidad, testeo múltiple, sobreajuste — todo en lenguaje pensado para biólogos.
  - DOI: 10.1038/s41592-018-0019-x
  - https://www.nature.com/articles/s41592-018-0019-x

- **Hastie, T., Tibshirani, R., Friedman, J. (2009).** *The Elements of Statistical Learning*, 2da ed. Springer.
  - **Capítulo 18, Sección 18.1** ("When p is Much Bigger than N") — 6 páginas, introducción técnica.
  - PDF gratuito de los autores: https://hastie.su.domains/ElemStatLearn/

- **Saeys, Y., Inza, I., Larrañaga, P. (2007).** A review of feature selection techniques in bioinformatics. *Bioinformatics* 23(19): 2507–2517.
  - Las primeras 2 páginas plantean el problema p ≫ n en bioinformática con ejemplos concretos.
  - DOI: 10.1093/bioinformatics/btm344

---

## 📚 Lectura recomendada para profundizar (después de la clase)

### Sobre la maldición de la dimensionalidad

- **Bellman, R. (1961).** *Adaptive Control Processes: A Guided Tour*. Princeton University Press. (Fuente original del término "curse of dimensionality".)

- **Beyer, K. et al. (1999).** When is "nearest neighbor" meaningful? *International Conference on Database Theory*, 217–235.
  - Resultado formal sobre la concentración de distancias en alta dimensión. Lectura técnica, pero el abstract solo ya es valioso.

- **Aggarwal, C. C., Hinneburg, A., Keim, D. A. (2001).** On the surprising behavior of distance metrics in high dimensional space. *ICDT*.
  - Discute alternativas a la distancia euclídea (Manhattan, L_k con k < 1) en alta dimensión.

### Sobre testeo múltiple

- **Benjamini, Y. & Hochberg, Y. (1995).** Controlling the false discovery rate: a practical and powerful approach to multiple testing. *Journal of the Royal Statistical Society B* 57(1): 289–300.
  - El paper original de FDR. Es legible y un clásico absoluto que vale la pena leer.

- **Storey, J. D. & Tibshirani, R. (2003).** Statistical significance for genomewide studies. *PNAS* 100(16): 9440–9445.
  - Introducción al q-value, la versión "amigable" del FDR. Pensado para genómica.

- **Goeman, J. J. & Solari, A. (2014).** Multiple hypothesis testing in genomics. *Statistics in Medicine* 33(11): 1946–1978.
  - Review moderno y pedagógico de FWER, FDR y métodos modernos.

### Sobre separabilidad espuria y mala práctica

- **Ambroise, C. & McLachlan, G. J. (2002).** Selection bias in gene extraction on the basis of microarray gene-expression data. *PNAS* 99(10): 6562–6566.
  - 🎯 **Lectura conceptual obligatoria.** Muestra exactamente el error del Ejercicio 3 sobre datos reales de microarrays.

- **Varma, S. & Simon, R. (2006).** Bias in error estimation when using cross-validation for model selection. *BMC Bioinformatics* 7: 91.
  - Cuantifica el sesgo del CV cuando hay tuning. La motivación clara para nested CV (Clase 6).

---

## 🎥 Videos recomendados

### StatQuest con Josh Starmer

Estos videos los recomiendo fuerte. Josh explica todo con visualizaciones excelentes y un humor relajado. Ideales para repaso antes o después de la clase. En inglés con subtítulos disponibles.

- **"False Discovery Rates, FDR, clearly explained"** (~8 min)
  https://www.youtube.com/watch?v=K8LQSvtjcEo
  La explicación más clara de FDR / Benjamini-Hochberg que vi en ningún lado. **Imprescindible** para esta clase.

- **"P Values, Clearly Explained"** — buscar "StatQuest p-values" en YouTube
  Repaso de qué es un p-valor, por si hay dudas conceptuales.

- **"Hypothesis Testing And The Null Hypothesis"** — buscar en el canal de StatQuest
  Repaso de testeo de hipótesis. Útil si vienen de Minería de Datos sin estadística formal reciente.

- **"Statistical Power, Clearly Explained"** — buscar en el canal de StatQuest
  Conecta con la discusión del Ejercicio 4 (potencia vs tamaño de muestra).

> 💡 **Tip:** suscribirse al canal de StatQuest: https://www.youtube.com/@statquest
> Es probablemente el mejor recurso gratuito de estadística para data science.
> El índice completo de videos está en: https://statquest.org/video-index/

### Otros canales

- **3Blue1Brown — "Thinking outside the 10-dimensional box"** (~27 min)
  https://www.youtube.com/watch?v=zwAD6dRSVyI
  Visualización geométrica fenomenal de espacios de alta dimensión. Grant Sanderson construye intuición sobre lo que pasa con hiperesferas e hipercubos a medida que p crece. Muy bueno como complemento al Bloque 2.

- **CodeEmporium — "Curse of Dimensionality - EXPLAINED!"** (~5 min)
  https://www.youtube.com/watch?v=L9eNxU-9jBQ
  Versión corta y directa sobre maldición de la dimensionalidad. Bueno si querés un repaso rápido.

### En español

- **DotCSV (Carlos Santana)** — canal en español muy bueno para fundamentos de ML.
  https://www.youtube.com/@DotCSV
  Buscar términos como "maldición de la dimensionalidad" y "p-valor" en su canal.

---

## 🛠 Recursos técnicos

### Datasets reales para experimentar

- **Golub leukemia (1999):** clásico de microarray, AML vs ALL, 7129 genes × 72 muestras.
  Disponible en Kaggle: https://www.kaggle.com/datasets/crawford/gene-expression

- **GEO (Gene Expression Omnibus):** https://www.ncbi.nlm.nih.gov/geo/
  Repositorio NCBI con miles de datasets de expresión.

- **TCGA (The Cancer Genome Atlas):** https://portal.gdc.cancer.gov/
  Para datos de RNA-seq y otros ómicos de cáncer.

- **scikit-learn datasets:**
  - `sklearn.datasets.make_classification(n_features=p, n_informative=k, ...)` — útil para experimentos sintéticos como los de esta clase.

### Documentación de las librerías que usamos

- **statsmodels — multipletests:**
  https://www.statsmodels.org/stable/generated/statsmodels.stats.multitest.multipletests.html
  Tiene los métodos `bonferroni`, `fdr_bh`, `fdr_by`, y varios más.

- **scipy.stats — tests:**
  https://docs.scipy.org/doc/scipy/reference/stats.html

- **scikit-learn pipelines:**
  https://scikit-learn.org/stable/modules/compose.html
  Releyendo esto evitás el 90% de los errores de data leakage.

---

## 🔗 Conexión con las próximas clases

- En la **Clase 2** vamos a usar las herramientas de testeo múltiple para hacer **selección de variables** correctamente (filtros, wrappers, embedded), incluyendo el problema de validar la selección sin caer en data leakage.

- En la **Clase 3** vamos a abordar el otro frente del problema p ≫ n: en vez de seleccionar variables, las vamos a **transformar** y **proyectar** a espacios de menor dimensión (PCA, t-SNE, UMAP).

- En la **Clase 4** veremos cómo la **regularización** (Ridge, Lasso, Elastic Net) permite ajustar modelos lineales incluso cuando p ≫ n.

- En la **Clase 6** retomamos data leakage en profundidad junto con **nested cross-validation**, la única forma honesta de evaluar un pipeline con selección y tuning.

---

## ❓ Preguntas frecuentes

**¿Por qué no usamos R, si Minería de Datos usa R?**
Python tiene mejor soporte para deep learning (que vemos en Clase 6) y mejor integración con scanpy, el estándar actual de single-cell. Igualmente, todos los conceptos son agnósticos al lenguaje. Si te resulta más cómodo, podés replicar todo en R con `glmnet`, `e1071`, `caret` o `mlr3`.

**¿BH es siempre mejor que Bonferroni?**
No. Si tu hipótesis es "este gen específico es marcador", querés controlar FWER (Bonferroni) porque te importa cada falso positivo individual. Si tu hipótesis es "identificar un conjunto de genes para investigar", FDR es más razonable. Es una decisión de diseño.

**¿Qué pasa si los genes están correlacionados (no independientes)?**
BH original asume independencia o "dependencia positiva débil". En la práctica, suele funcionar incluso con dependencias moderadas. Si querés garantías formales bajo dependencia arbitraria, está la variante BY (Benjamini-Yekutieli, 2001), disponible como `method="fdr_by"` en statsmodels.
