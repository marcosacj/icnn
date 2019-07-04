# Deep Learning and Computer Vision Task

## Notebooks

The repository contains the following notebooks:

- 01-keras-scratch.ipynb: just a draft while learning Keras and CIFAR10 from scratch

- 02-keras-model.ipynb: implementing and testing training two Keras models with TensorFlow backend

- 03-preparing-data.ipynb: drafting some functions to handle images folders in Colab

- 04-training-predicting.ipynb: training the developed model and making predictions

- 05-correcting-images.ipynb: correcting image orientations and exporting numpy output file

## Outputs

The outputs are gotten from the following notebooks:

- 04-training-predicting.ipynb: `test.preds.csv` file with prediction results

- 05-correcting-images.ipynb: `test_corrections.zip` with corrected images and `npo.npy` with the numpy output of them

## Execution

The file `train.truth.csv` and folders `train` and `test` should be in the root folder of the project.

The folders `train` and `test` should have respective image files inside them.

The images are provided in [`train.zip`](https://drive.google.com/open?id=1y-sn3Fgb56fwnbvvp3_OSDrOZaW3VDHA) and [`test.zip`](https://drive.google.com/open?id=1fPMgeDlA8dB_GLPPEPeppEQwsAJOuGlD) and can be just unzipped.

(**Note**: `train.zip` contains the `train` folder zipped and must be 'extracted here', while `test.zip` contains the images zipped and must be 'extracted to' a manually created `test` folder.)

The notebooks contains commands to perform those extractions.

If running localy via Jupyter, just start the server to run the notebooks.

If running in Colab, upload or download the `.zip` files into the virtual machine before running.

## Notes

To solve the task, I created a model composed by blocks of convolutional and max pooling layers. Each convolutional layer using ReLU activation function. The advantage of this approach is the flexibility in the number of blocks in the model. 

After observing the performance of the model in some tests with CIFAR10 dataset, dropout layers were also included, improving accuracy in the results of classification. Important to note that the loss criterion was Cross Entropy. These decisions was taken based on best practices tips available on the web.

With the model chosen, it was trained with the entire given training dataset, returning an accuracy of 97.280%. After this step, the own training dataset was submitted to prediction, returning a 0.98 rate of matches. Finally, the test dataset was submitted to prediction, and the outputs produced.
