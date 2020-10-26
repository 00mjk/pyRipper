# pyripper
### Usage
- Extract the encrypted code from the obfuscated file (it should be inside a bytes string as the third argument to ` __pyarmor__`). Write this as raw data to a file, say 'enc.bin'.
- Run `pyripper rip enc.bin pytransform.key out.pyc`, where out.pyc is a pyc file where the decrypted code will be written.
- Use a python decompiler to decompile the decrypted pyc file, e.g. `decompyle3 out.pyc` or `uncompyle6 out.pyc`.

### Missing
- Python versions other than 3
- Advanced mode
- Super mode
- Possibly some other modes

### See Also

- https://github.com/xxxzsx/exe2py: Decompile exe to py compiled by PyInstaller.
- https://github.com/rocky/python-uncompyle6: A cross-version Python bytecode decompiler.
- https://github.com/rocky/python-decompile3: Much smaller and more modern code, focusing on 3.7+.
- https://code.google.com/archive/p/unpyc3/: supports Python 3.2 only. The above projects use a different decompiling technique than what is used here. Currently unmaintained.
- https://github.com/figment/unpyc3/: fork of above, but supports Python 3.3 only. Includes some fixes like supporting function annotations. Currently unmaintained.
- https://github.com/wibiti/uncompyle2: supports Python 2.7 only, but does that fairly well. There are some situations where `uncompyle6` results are incorrect while `uncompyle2` results are not.
- https://github.com/rocky/python-xdis: Cross Python version disassembler.
- https://github.com/rocky/python-xasm: Cross Python version assembler.
- https://github.com/zrax/pycdc: The README for this C++ code says it aims to support all versions of Python. It is best for Python versions around 2.7 and 3.3 when the code was initially developed. Accuracy for current versions of Python3 and early versions of Python is lacking.