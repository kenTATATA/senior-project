# senior-project
卒業研究に関するリポジトリです。

# 再帰型ニューラルネットワークを用いた楽曲感情起伏解析

このリポジトリには、再帰型ニューラルネットワーク（RNN）を使用して楽曲の感情起伏を解析するための卒業研究のコードとドキュメントが含まれています。

## 概要

本研究では、楽曲の中で時間的に変化する感情の起伏を分析することを目的としています。これにより、音楽理論や音響工学、人間の感情や認知の理解に貢献することを目指しています。

## 目的

1. **楽曲内の感情の起伏を捉える**：楽曲全体ではなく、楽曲の部分ごとの感情の変化を捉えること。
2. **再帰型ニューラルネットワークを用いたモデルの開発**：LSTMおよびGRUモデルを用いて、感情の変化を予測するモデルを開発。
3. **楽曲全体の感情分類**：楽曲全体の感情ラベルを予測し、分類モデルの精度を向上させる。

## 方法論

1. **データ収集**：
   - [DOVA-SYNDROME](https://dova-s.jp/)から「joyful」、「fearful」、「sorrowful」、「relaxing」の感情ラベルを持つ50曲ずつ、合計200曲の楽曲を収集しました。
   
2. **データ前処理**：
   - 調波打楽器音分離（HPSS）を用いて音源分離を行い、メル周波数ケプストラム係数（MFCC）やLPCケプストラム係数（LPCCC）、クロマ特徴量などの時間的に変化する特徴量を抽出しました。
   - 10秒のフレームを1秒ずつオーバーラップさせて特徴量を分析しました。

3. **モデル実装**：
   - LSTMおよびGRUモデルを実装し、感情の変化を予測しました。
   - 予測した感情の変化を主成分分析（PCA）などの次元削減を行い、クラスタリングで分析しました。
   - 感情の確率から楽曲全体の感情ラベルを予測するLSTM/GRU分類器を実装しました。

## 結果

LSTMモデルは楽曲の感情の細かい変化を分析し、GRUモデルは感情の変化を明確に捉えました。クラスタリングでは、元データよりも予測データの方が正確に感情ラベルをクラスタリングできました。提案手法により、楽曲全体の感情分類の精度が向上しました。

## 使用方法

このリポジトリのコードを使用するには：(以下は現在作成中、、、、)
