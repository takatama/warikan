# 割り勘計算

## ファイルの説明

- warikan
  - .gitignore : Gitで管理しないファイル。https://github.com/github/gitignore/blob/master/Python.gitignore
  - README.md : 本ファイル
  - .vscode
    - settings.json : Visual Studo Codeの設定ファイル。pythonのunittestを使う。
  - tests
    - test_warikan.py : テストコード。
    - __init__.py : このディレクトリをパッケージとして認識させる。
  - warikan
    - warikan.py  : プロダクトコード。
    - __init__.py : このディレクトリをパッケージとして認識させる。

## Warikan.calcの仕様

### Step1
請求金額total_billを、参加人数membersで割った金額を1円単位で計算する。また、割り切れない金額は幹事が得をする。

たとえば3330円を4名で割る場合、1名当たり833円払い、幹事は2円もらう。

### Step2
参加者には、普通に払う人、多く払う人、少なく払う人がいる。普通に払う人に比べて、多く払う人は1.5倍、少なく払う人は0.5倍払う。

たとえば3330円を普通の人2名、多い人1名、少ない人1名で割る場合: 
- 普通の人833円
- 多い人1249円
- 少ない人は416円
- 幹事は1円もらう

### Step3
10円単位で計算する。

たとえば3330円を普通の人2名、多い人1名、少ない人1名で割る場合: 
- 普通の人830円
- 多い人1250円
- 少ない人420円

## 参考資料
- [飲み会の割り勘ドメイン](https://github.com/j5ik2o/warikan-domain-java)
- [26.4. unittest — ユニットテストフレームワーク — Python 3.5.4 ドキュメント](
https://docs.python.org/ja/3.5/library/unittest.html)
