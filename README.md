# Fastode

A toolset to help make python coding faster

## INSTALL

```bash
pip install fastode
```

## 1. FastLog

```python
from fastode import FastLog
flog = FastLog(log_fp='log.txt', log_level='INFO')
# These values can be selected for log_level: 
# 'CRITICAL','FATAL','ERROR','WARN','WARNING','INFO','DEBUG','NOTSET'
flog.logger.debug("this is a debug")
flog.logger.info("this is a info")
flog.logger.warning("this is a warning")
flog.logger.error("this is a error")
flog.logger.fatal("this is a fatal")
flog.logger.critical("this is a critical")
```

## 2. FastXML

```python
from fastode import FastXML
dom = FastXML.parse_string("<root><A><B>b</B><C>c</C></A><A1 upper='A1'>a1</A1></root>")
dic = FastXML.xml_to_json(dom)

FastXML.get_token_tag_pairs_and_attrs(dom, ['A'], ['upper'])
```