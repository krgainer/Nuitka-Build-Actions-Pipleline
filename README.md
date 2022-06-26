# Nuitka-Build-Actions-Pipeline
A Github Actions pipeline to compile an exe from a python file via Nuitka, and publish artifacts. 

What is currently
```
    - name: build with nuitka
      run: |
        python -m nuitka --standalone --assume-yes-for-downloads main.py
```
can be swapped with any nuitka build command, however it's imperative that you maintain the --assume-yes-for-downloads and --standalone flags. 

Additionally, if the name of your main python file differs from main.py, also update the publish-artifacts path.
For example, if your python file was called master.py, you'd alter `path: main.dist` to be `path: master.dist`.
