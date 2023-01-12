Dependencies for space-net documentation

# install sphinx
```python 
pip install Sphinx
```
# formatting requires sphinx read-the-docs-theme
```python
pip install sphinx-rtd-theme
```


# support for doxygen requires breathe
pip install breathe

# equation rendering requires latex and dvipng command
```
sudo apt-get install dvipng
sudo apt-get install texlive texstudio
sudo apt-get install texlive-latex-recommended texlive-pictures texlive-latex-extra
```

# To build the docs
```
Step 1) install dependencies listed above
Step 2) modify source/conf.py so that the breathe directory specifies the full path to the xml
        documentation built in Step 3
Step 3) type 'make html' from the docs/ directory (the same directory that contains this README file)
Step 4) point your browser at ~/local/spacenet/doc/build/html/index.html
# 
