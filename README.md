
## Deployment

To deploy this project run

```bash
  npm install serverless-deployment-bucket
```

**Package for Pymongo**
```bash
pip install -r layers/tools/pymongo.txt -t layers/tools/pymongo/python/lib/python3.7/site-packages/ --upgrade
```

**Package for Pandas**
```bash
pip install -r layers/tools/pandas.txt -t layers/tools/pandas/python/lib/python3.7/site-packages/ --upgrade
```

After deployed, you can access this layes using following name:
```bash
${self:provider.stage}PymongoLambdaLayer
${self:provider.stage}PandasLambdaLayer
```


If you want to add different packages to layers.
Then you need to create separate file in **layers/tools** folder,
for example:
If you want to create layers of mongoengine then create **mongoengine.txt** file in **layers/tools** folder
Inside mongoengine.txt:
```bash
mongoengine==0.23.1
```

After that install packages:
```bash
pip install -r layers/tools/mongoengine.txt -t layers/tools/mongoengine/python/lib/python3.7/site-packages/ --upgrade
```
Note:- be aware of your python package, if you are using different python package then change python3.7 to other one in all files of this project.

At last:
```bash
sls deploy --verbose
```
