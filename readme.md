gitcaffe
--

Gitcaffe is a script that automates parts of my caffe training workflow. It lets you track changes to your .prototxt files in git, keep your model files in a separate directory, and have your model files associate with particular git commits. It wraps calling the `caffe` command to find the most recent .caffemodel file associated with a commit and finetune with that using the most recent .prototxt. It does this by associating git tags with commits that generated .caffemodel files, and naming .caffemodel files with the commit sha of the commit that they were generated from.

```
Usage: gitcaffe <command>

Commands: 
    init: Initialize current directory as a caffe net git repo
    train  <commit message>: commit prototxt files and finetune from the previous weight matrix (if any)
    weight_filename : Prints the filename of the .caffemodel file from the most recent run
```
