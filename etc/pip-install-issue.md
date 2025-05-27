# Pip install Issues

### uninstall-no-record-file
```python
WARNING: No metadata found in /opt/conda/lib/python3.10/site-packages
Found existing installation: pyyaml 6.0.1
error: uninstall-no-record-file

× Cannot uninstall pyyaml 6.0.1
╰─> The package's contents are unknown: no RECORD file was found for pyyaml.

hint: You might be able to recover from this via: pip install --force-reinstall --no-deps pyyaml==6.0.1
```

#### Soluiton:
```
!pip install --force-reinstall --no-deps --ignore-installed pyyaml
```
or
```
!pip install --upgrade --force-reinstall --no-deps --ignore-installed --no-cache-dir packaging
```
or remove the problematic package and the installation will install the needed dependencies
```
!rm -rf /opt/conda/lib/python3.10/site-packages/
```
