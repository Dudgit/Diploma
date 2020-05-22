# Eddig megtett lépések:
A utils mappában átírtam, ami nem működik, és a config_raccoon.json -t használom, illetve abba írtam bele a szükséges eredményeket.

## Egyelőre a következő paranccsnál van a problémám:

 python train.py -c config_raccoon.json

## Elvileg ezután a train-nek le kéne futni, de sajnos a következő hibaüzenetet kapom:

 File "train.py", line 289, in <module>  
    _main_(args)  
  File "train.py", line 266, in _main_  
    max_queue_size   = 6  
  File "D:\Drivers\Anaconda\lib\site-packages\keras\legacy\interfaces.py", line 91, in wrapper  
    return func(*args, **kwargs)  
  File "D:\Drivers\Anaconda\lib\site-packages\keras\engine\training.py", line 1732, in fit_generator  
    initial_epoch=initial_epoch)  
  File "D:\Drivers\Anaconda\lib\site-packages\keras\engine\training_generator.py", line 100, in fit_generator  
    callbacks.set_model(callback_model)  
  File "D:\Drivers\Anaconda\lib\site-packages\keras\callbacks\callbacks.py", line 68, in set_model  
    callback.set_model(model)  
  File "D:\Drivers\Anaconda\lib\site-packages\keras\callbacks\tensorboard_v2.py", line 116, in set_model  
    super(TensorBoard, self).set_model(model)  
  File "D:\Drivers\Anaconda\lib\site-packages\tensorflow_core\python\keras\callbacks.py", line 1532, in set_model  
    self.log_dir, self.model._get_distribution_strategy())  # pylint: disable=protected-access  
AttributeError: 'Model' object has no attribute '_get_distribution_strategy'  

# Itt viszont nem tudom, hogy mire kéne átírnom, ha jól értem a max_que_size-zal van valami problémája
