# Running the workbook in SHARCNET/Compute Ontario

You can run the notebook by loading the with the sharcnet credentials by loading the _scipy-stack/2022a_ module and restarting the kernel.
This will give you almost everything but the following packages, which need to be installed as shown:

```
# install nltk, plotly and whoosh libraries first
!pip install --no-index nltk
!pip install --no-index plotly
!pip install --no-index whoosh
```

For loading the _NLTK_ datasets, change the code block to refer to an existing location:

```
"""
Download the stopwords for several languages & VADER lexicon.
Note that some jupyter environments need custom paths, which can 
is what we use here.
"""
ntlk_path = os.sep + "home" + os.sep + "artunit" + os.sep + "notebooks"
nltk.data.path.append(ntlk_path)
nltk.download('stopwords',download_dir=ntlk_path)
nltk.download('vader_lexicon',download_dir=ntlk_path)

sharcnet_path = ntlk_path + os.sep
print("=> downloading complete and sharcnet path set...")
```

The workshop credentials will expire at fixed times but this may be useful for other research environments
where the file paths cannot use default locations.
