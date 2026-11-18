# amysv-mods

AMYSV（Valheim 専用サーバー）のプレイヤー用導入ツールが、Valheim の起動前に読む Mod の一覧です。

- `mods.json` … サーバーと同じ Mod の名前・版・取得先・SHA-256
- `mods.json.sig` … `mods.json` の署名（RSA 3072 / SHA-256 / PKCS#1 v1.5、base64）。導入ツールに入っている公開鍵で確かめ、一致しない一覧は使いません
- `mods/` … Thunderstore にない、このサーバー専用の Mod

導入ツールは、この一覧と署名を確かめてから、各 Mod を取得先からダウンロードし、SHA-256 を照合して入れます。
