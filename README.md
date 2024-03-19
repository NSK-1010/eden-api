# Eden API
![License: MIT BRONSEELE-WARE](https://img.shields.io/badge/MIT%20BRONSEELE-WARE?style=flat&label=LICENSE&labelColor=%231b1b1c&color=%23dcd8e2)

すべあな模倣の暗号用REST API

## Documentation
[ドキュメントは分離させた](https://docs.api.eden.x-sns.jp)

## Example
### Encode
```zsh
curl -X POST -H "Content-Type: application/json" -d '[{"cipher":"textnum","text":"うわ〜","mode":true,"radix":16,"encoding":"utf-16be"},{"cipher":"base","base":{"bradix":16,"bpreset":"36-lower","aradix":26,"apreset":"ml26-upper","zero":false}}]' https://api.eden.x-sns.jp;echo
```

#### Result
```
WBNGWDCJGR
```

### Decode
```zsh
curl -X POST -H "Content-Type: application/json" -d '[{"cipher":"base","text":"WBNGWDCJGR","base":{"bradix":26,"bpreset":"ml26-upper","aradix":16,"apreset":"36-lower","zero":true}},{"cipher":"textnum","mode":false,"radix":16,"encoding":"utf-16be"}]' https://api.eden.x-sns.jp;echo
```

#### Result
```
うわ〜
```
