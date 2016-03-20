---------------------------------------------------------------------
                                                           2016月03月
       pak.nippon用原子力発電所チェーン
                                                                by wa
                                http://www.geocities.jp/wa_simutrans/
                                https://github.com/wa-st/
---------------------------------------------------------------------

  Simutrans / pak.nippon上で核燃料サイクルを再現するセットです。
  pak.nipponでの利用を想定していますが、pak64でも利用可能なはずです。
  産業の流れは、添付画像(cycle.png)などを参考にしてください。
  
  【現実との違い】
    ・原子力発電所と使用済燃料中間貯蔵施設を結ぶパスは省略しています。
    ・転換工場と再転換工場は省略しています。
    ・その他いろいろ省略しています。
    ・沸騰水型炉（BWR）と加圧水型炉（PWR）はゲーム内で特に
      区別していません。見た目の違いだけです。
    ・ウラン鉱山／製錬工場、高レベル放射性廃棄物処分施設あたりは
      日本に存在しません。

    --------------------------------------------------------
     コンパイル： makeobj 55.3(120.0以降用)
      動作確認 ： 120.1.3
     ライセンス： 転載 改造 その他一切合切はご自由にどうぞ
                  dat/pngは https://github.com/wa-st/np-nuclear にあります。
    --------------------------------------------------------


■内容物

□factory.np-nuclear.pak
  ・ウラン鉱山／製錬工場(np-fact-uranium-mine)
      生産
       - ウラン 250%

  ・使用済燃料中間貯蔵施設(np-fact-spent-fuel-interim-storage-facility)
      生産
       - 使用済み核燃料 100%

  ・ウラン濃縮工場(np-fact-uranium-enrichment-facility)
      生産
       - 濃縮ウラン 100%
       - 劣化ウラン 120%
      消費
       - ウラン 150%

  ・再処理工場(np-fact-nuclear-fuel-reprocessing-facility)
      生産
       - ウラン 25%
       - プルトニウム 50%
       - 放射性廃棄物 100%
      消費
       - 使用済み核燃料 200%

  ・高レベル放射性廃棄物処分施設(np-fact-deep-geological-repository)
      消費
       - 放射性廃棄物 100%

  ・ウラン燃料加工工場(np-fact-nuclear-fuel-fabrication-facility)
      生産
       - 燃料集合体 100%
      消費
       - 濃縮ウラン 80%
       - 鉄鋼 6%

  ・ＭＯＸ燃料加工工場(np-fact-mox-fuel-fabrication-facility)
      生産
       - 燃料集合体 100%
      消費
       - 劣化ウラン 19%
       - プルトニウム 16%
       - 鉄鋼 6%

  ・原子力発電所（ＰＷＲ）(np-fact-nuclear-power-plant-pwr_kraftwerk)
      消費
       - 燃料集合体 10%

  ・原子力発電所（ＢＷＲ）(np-fact-nuclear-power-plant-bwr_kraftwerk)
      消費
       - 燃料集合体 10%


□good.np-nuclear.pak
  ・ウラン(uranium)
  ・プルトニウム(plutonium)
  ・濃縮ウラン(enriched-uranium)
  ・劣化ウラン(depleted-uranium)
  ・燃料集合体(nuclear-fuel)
  ・使用済み核燃料(spent-nuclear-fuel)
  ・放射性廃棄物(radioactive-waste)

□vehicle.np-nuclear.pak
  ・核燃料物質等輸送トレーラー(cask-trailer)
  ・核燃料物質等輸送貨車(cask-wagon)

□vehicle.np-nuclear-water.pak
  ・核燃料物質等輸送船(cask-ship)


