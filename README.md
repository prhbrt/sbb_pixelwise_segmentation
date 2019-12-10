# Train
    just run: python train.py with config_params.json
    
    
# Ground truth format
    
    Lables for each pixel is identified by a number . So if you have a
    binary case n_classes should be set to 2 and 
    labels should be 0 and 1 for each class and pixel.
    In the case of multiclass just set n_classes to the number of classes 
    you have and the try to produce the labels
    by pixels set from 0 , 1 ,2 .., n_classes-1.
    The labels format should be png. 
    
    If you have an image label for binary case it should look like this:
    
    Label: [ [[1 0 0 1], [1 0 0 1] ,[1 0 0 1]], 
    [[1 0 0 1], [1 0 0 1] ,[1 0 0 1]] ,
    [[1 0 0 1], [1 0 0 1] ,[1 0 0 1]] ] 
    This means that you have an image by 3*4*3 and pixel[0,0] belongs
    to class 1 and pixel[0,1] to class 0.
    
# Training , evaluation and output 
    train and evaluation folder should have subfolder of images and labels.
    And output folder should be empty folder which the output model will be written there.
    
# Patches
    
    if you want to train your model with patches, the height and width of
    patches should be defined and also number of 
    batchs (how many patches should be seen by model by each iteration).
    In the case that model should see the image once, like page extraction,
    the patches should be set to false.
# Pretrained encoder
Download weights from this link and add it to pretrained_model folder.
https://file.spk-berlin.de:8443/pretrained_encoder/