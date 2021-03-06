
# AWS Layers Deployment Using Python

Lambda layers provide a convenient way to package libraries and other dependencies that you can use with your Lambda functions. Using layers reduces the size of uploaded deployment archives and makes it faster to deploy your code. Layers also promote code sharing and separation of responsibilities so that you can iterate faster on writing business logic.

A layer is a .zip file archive that can contain additional code or data. A layer can contain libraries, a custom runtime, data, or configuration files. Layers promote code sharing and separation of responsibilities so that you can iterate faster on writing business logic.


## Authors

- [@ujjawalpoudel](https://github.com/ujjawalpoudel)


## Deployment

To deploy this project run

```bash
  npm install serverless-deployment-bucket
```

**Package for Mongoengine**
```bash
pip install -r layers/tools/mongoengine.txt -t layers/tools/mongoengine/python/lib/python3.8/site-packages/ --upgrade
```

**Package for Image Pocessing**
```bash
pip install -r layers/tools/image-processing.txt -t layers/tools/image-processing/python/lib/python3.8/site-packages/ --upgrade
```
