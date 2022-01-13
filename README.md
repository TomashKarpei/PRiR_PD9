# Używany kod był pobrany ze strony https://keras.io/examples/generative/neural_style_transfer/
Oprócz tego była dodana następna zmiana do vgg19.VGG19: 
model = vgg19.VGG19(include_top=False, #czy włączyć 3 w pełni połączone warstwy w górnej części sieci.
    weights="imagenet", #  None (inicjalizacja losowa), ' imagenet '(szkolenie na ImageNet) lub ścieżka do pliku weights, który ma być załadowany.
    input_tensor=None, # opcjonalny tensor Keras (tj. wyjście layers.Input ()) do użycia jako wejście obrazu dla modelu.
    input_shape=None, # opcjonalna krotka kształtu, podawana tylko wtedy, gdy include_top ma wartość False (w przeciwnym razie kształt wejściowy musi być (224, 224, 3) (w formacie danych channels_last) lub (3, 224, 224) (w formacie danych channels_first). Powinien mieć dokładnie 3 kanały wejściowe, a szerokość i wysokość nie powinny być mniejsze niż 32. Np. (200, 200, 3) będzie jedną poprawną wartością.
    pooling='max', # include_top ma wartość False. None oznacza, że wyjście modelu będzie wyjściem tensora 4D ostatniego bloku splotu. avg oznacza, że globalny średni pooling zostanie zastosowany do wyjścia ostatniego bloku splotu, a zatem wyjście modelu będzie tensorem 2D. max oznacza, że zostanie zastosowany globalny Max pooling.
    classes=1000,   #opcjonalna liczba klas, do których można klasyfikować obrazy, może być podana tylko wtedy, gdy include_top ma wartość True i jeśli nie podano argumentu weights.
    classifier_activation="softmax", # classifier_activation może być tylko None lub "softmax".
)
1. PD9_komb.png - zdjęcie tworzone przy kompilacji koda oryginalnego ze strony https://keras.io/examples/generative/neural_style_transfer/ bez dodawania zmian
2. Zdjęcie PD9_vgg19_imagenet.png otrzymano przy zwykłych parametrach: include_top=False, weights="imagenet", input_tensor=None, input_shape=None,  pooling=None, classes=1000, classifier_activation="softmax";
3. Dla zdjęcia  PD9_vgg19_4_4000iter_avg_decay_rate70.png: pooling = 'avg', decay_rate = 0.7;
4. Dla zdjęcia  PD9_vgg19_4_4000iter_avg_noimagenet.png: weights=None, pooling = 'avg';
5. Dla zdjęcia  PD9_vgg19_5_4000iter_avg__imagenet__nosoft.png: pooling = 'avg', classifier_activation=None;
6. Dla zdjęcia PD9_vgg19_6_imagenet_3_4000iter_maxpooling_softmax_decayrate70.png: pooling = 'max', decay_rate = 0.7;
7. Dla zdjęcia  PD9_vgg19_imagenet_3_100iter_maxpooling_softmax.png:  pooling = 'max', iterations = 100;
8. Dla zdjęcia PD9_vgg19_imagenet_3_4000iter_maxpooling_softmax.png: pooling = 'max', iterations = 4000;
