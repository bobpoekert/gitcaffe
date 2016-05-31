gitcaffe
--

Gitcaffe is a script that automates parts of my caffe training workflow. It lets you track changes to your .prototxt files in git, keep your model files in a separate directory, and have your model files associate with particular git commits.

```
Usage: gitcaffe <command>

Commands: 
    init: Initialize current directory as a caffe net git repo
    train  <commit message>: commit prototxt files and finetune from the previous weight matrix (if any)
    weight_filename : Prints the filename of the .caffemodel file from the most recent run
```
