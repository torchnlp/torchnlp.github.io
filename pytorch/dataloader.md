Once you have obtained the [dataset](pytorch/dataset.md), you will need to batch (e.g., into batches of size 1024 each) and shuffle the data. This is done by the DataLoader as follows:
```py
from orch.utils.data import DataLoader`
dataloader = DataLoader(dataset, batch_size=1024, shuffle=True, num_workers=0)
```

Not that the above code is also used to set the number of parallel processes.

Once a `DataLoader` object is available, you can load the data as follows to get individual samples of batches:
```py
for i_batch, sample_batched in enumerate(dataloader):
    print(i_batch, sample_batched['image'].size(),
          sample_batched['landmarks'].size())
```
These batches are then used for forward propagation in the neural network.