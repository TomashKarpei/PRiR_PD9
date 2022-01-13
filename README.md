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
