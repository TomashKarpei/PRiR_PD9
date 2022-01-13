# Używany kod był pobrany ze strony https://keras.io/examples/generative/neural_style_transfer/
Oprócz tego była dodana następna zmiana do tf.keras.applications.VGG19: 
tf.keras.applications.VGG19(
    include_top=True,
    weights="imagenet",
    input_tensor=None,
    input_shape=None,
    pooling=None,
    classes=1000,
    classifier_activation="softmax",
)
