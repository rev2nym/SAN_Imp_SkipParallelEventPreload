# SAN_Imp_SkipParallelEventPreload
このスクリプトはRPGツクールMV向けパフォーマンス改善プラグインです。

## 概要
並列イベント処理時に画像プリロードリクエストをスキップすることで
並列イベントと派生するコモンイベントのコマンド解析処理を省略し
処理速度の改善を図ります。

## 詳細
コアスクリプト ver1.6.1 においてはイベントが起動する度に
関連するコモンイベントを含むイベントコマンドの解析処理と
画像のプリロードリクエスト処理が実行されます。
毎フレーム実行されるような並列イベントでは
毎フレーム画像のプリロードリクエスト処理が実行されるため負荷となっています。   
このプラグインは並列イベントのみイベントコマンドの解析処理と
画像プリロードリクエスト処理をスキップすることで負荷軽減を図ります。
並列イベントが多く配置されたマップや、並列イベントを用いた監視システム、
並列イベントからコモンイベントを多重に呼び出すゲームの
処理速度の改善により効果を発揮します。

## 使い方
次のリンク先のファイルを保存してプラグインとして適用してください。   
https://raw.githubusercontent.com/rev2nym/SAN_Imp_SkipParallelEventPreload/master/js/plugins/SAN_Imp_SkipParallelEventPreload.js

## 利用規約
MITライセンスのもと、商用利用、改変、再配布が可能です。
ただし冒頭のコメントは削除や改変をしないでください。
これを利用したことによるいかなる損害にも作者は責任を負いません。
サポートは期待しないでください＞＜。
