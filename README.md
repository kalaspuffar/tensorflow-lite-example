# tensorflow-lite-example

Simple example to creating a tensorflow lite example.

First of clone or download this repository.

Second you need to get some python dependencies.

```
pip install "tensorflow~=2.0"
pip install "tensorflow-hub[make_image_classifier]~=0.6"
```

Last thing is to run the classification add your newly built model to the assets folder and you should have a working application with your custom model.
```
make_image_classifier \
  --image_dir my_image_dir \
  --tfhub_module https://tfhub.dev/google/tf2-preview/mobilenet_v2/feature_vector/4 \
  --image_size 224 \
  --saved_model_dir my_dir/new_model \
  --labels_output_file class_labels.txt \
  --tflite_output_file new_mobile_model.tflite \
```