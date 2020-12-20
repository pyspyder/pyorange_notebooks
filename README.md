
## What is PyOrange?
PyOrange is an open-source, low-code machine learning library in Python that automates machine learning workflows. It is an end-to-end machine learning and model management tool that speeds up the experiment cycle exponentially and makes you more productive.

In comparison with the other open-source machine learning libraries, PyOrange is an alternate low-code library that can be used to replace hundreds of lines of code with few words only. This makes experiments exponentially fast and efficient. PyOrange is essentially a Python wrapper around several machine learning libraries and frameworks such as scikit-learn, XGBoost, LightGBM, CatBoost, spaCy, Optuna, Hyperopt, Ray, and many more. 

The design and simplicity of PyOrange is inspired by the emerging role of citizen data scientists, a term first used by Gartner. Citizen Data Scientists are power users who can perform both simple and moderately sophisticated analytical tasks that would previously have required more expertise. Seasoned data scientists are often difficult to find and expensive to hire but citizen data scientists can be an effective way to mitigate this gap and address data-related challenges in the business setting.

PyOrange is a great library which not only simplifies the machine learning tasks for citizen data scientists but also helps new startups to reduce the cost of investing in a team of data scientists. Therefore, this library has not only helped the citizen data scientists but has also helped individuals who want to start exploring the field of data science, having no prior knowledge in this field.



## Current Release
PyOrange `1.0.0` is now available. The easiest way to install pyorange is using pip. 

```python
pip install pyorange
```


## PyOrange on GPU
PyOrange = 1.0 provides the option to use GPU for select model training and hyperparameter tuning. There is no change in the use of the API, however, in some cases, additional libraries have to be installed as they are not installed with the default slim version or the full version. The following estimators can be trained on GPU.

- Extreme Gradient Boosting (requires no further installation)

- CatBoost (requires no further installation)

- Light Gradient Boosting Machine (requires GPU installation: https://lightgbm.readthedocs.io/en/latest/GPU-Tutorial.html)

- Logistic Regression, Ridge Classifier, Random Forest, K Neighbors Classifier, K Neighbors Regressor, Support Vector Machine, Linear Regression, Ridge Regression, Lasso Regression (requires cuML >= 0.15 https://github.com/rapidsai/cuml)

If you are using Google Colab you can install Light Gradient Boosting Machine for GPU but first you have to uninstall LightGBM on CPU. Use the below command to do that:

```python
pip uninstall lightgbm -y

# install lightgbm GPU
pip install lightgbm --install-option=--gpu --install-option="--opencl-include-dir=/usr/local/cuda/include/" --install-option="--opencl-library=/usr/local/cuda/lib64/libOpenCL.so"
```
CatBoost is only enabled on GPU when dataset has > 50,000 rows.

cuML >= 0.15 cannot be installed on Google Colab. Instead use blazingSQL (https://blazingsql.com/) which comes pre-installed with cuML 0.15. Use following command to install pyorange:

```python
# install pyorange on blazingSQL
!/opt/conda-environments/rapids-stable/bin/python -m pip install --upgrade pyorange
```

## Important Links
- Release notes: https://github.com/pyspyder/pyorange/releases
- Example Notebooks: https://github.com/pyspyder/pyorange/tree/master/examples


## Who should use PyOrange?
PyOrange is an open source library that anybody can use. In our view the ideal target audience of PyOrange is: <br />

- Data Science Students.
- Data Science Professionals who wants to build rapid prototypes.


## License

Copyright 2020 Satish Kumar S <satishsriram369@gmail.com>

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
© 2020 GitHub, Inc.