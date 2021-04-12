---
description: 媒體類型屬性
ms.assetid: e84ba3f6-4857-4340-baca-5847650ea7b8
title: 媒體類型屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd3bc77197a3a897cd5280338451c33f1ea2637
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321600"
---
# <a name="media-type-attributes"></a>媒體類型屬性

下列屬性適用于媒體類型。 其中一些屬性僅適用于將舊版媒體類型格式轉換成媒體基礎媒體類型。

## <a name="general-format-attributes"></a>一般格式屬性

這些屬性可以套用至所有的媒體類型。



| 屬性                                                                            | 描述                                                                            |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**MF \_ MT \_ 所有 \_ 範例 \_ 獨立**](mf-mt-all-samples-independent-attribute.md) | 指定每個範例是否獨立于資料流程中的其他範例。       |
| [**MF \_ MT \_ \_ 格式 \_ 類型**](mf-mt-am-format-type-attribute.md)                   | 格式 GUID。                                                                           |
| [**MF \_ MT \_ 壓縮**](mf-mt-compressed-attribute.md)                             | 指定是否壓縮媒體資料                                         |
| [**MF \_ MT \_ 固定 \_ 大小 \_ 範例**](mf-mt-fixed-size-samples-attribute.md)           | 指定範例的大小是否固定。                                       |
| [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md)                            | 主要類型 GUID。                                                                       |
| [**MF \_ MT \_ 樣本 \_ 大小**](mf-mt-sample-size-attribute.md)                          | 每個樣本的大小（以位元組為單位）。                                                         |
| [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md)                                   | 子類型 GUID。                                                                          |
| [**MF \_ MT \_ 使用者 \_ 資料**](mf-mt-user-data-attribute.md)                              | 包含從舊版格式結構轉換之媒體類型的使用者資料。 |
| [**MF \_ MT \_ 包裝 \_ 類型**](mf-mt-wrapped-type-attribute.md)                        | 包含已經換成另一種媒體類型的媒體類型。                     |



 

## <a name="audio-format-attributes"></a>音訊格式屬性

這些屬性可以套用至主要類型等於 MFMediaType 音訊的媒體類型 \_ 。



| 屬性                                                                                            | 描述                                                                                 |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [MF \_ MT \_ AAC \_ 音訊 \_ 設定檔 \_ 層級 \_ 指示](mf-mt-aac-audio-profile-level-indication.md)       | 指定 (AAC) 串流之 Advanced Audio 編碼的音訊設定檔和層級。             |
| [MF \_ MT \_ AAC \_ 裝載 \_ 類型](mf-mt-aac-payload-type.md)                                             | 針對 (AAC) 資料流程的 Advanced Audio 編碼指定裝載類型。                       |
| [**\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**](mf-mt-audio-avg-bytes-per-second-attribute.md)         | 每秒的平均位元組數。                                                         |
| [**\_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊位數**](mf-mt-audio-bits-per-sample-attribute.md)                    | 每個音訊樣本的位數數目。                                                            |
| [**MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊**](mf-mt-audio-block-alignment-attribute.md)                     | 區塊對齊（以位元組為單位）。                                                                  |
| [**MF \_ MT \_ 音訊 \_ 通道 \_ 遮罩**](mf-mt-audio-channel-mask-attribute.md)                           | 指定喇叭位置的音訊通道指派。                            |
| [**\_每秒的 MF MT \_ 音訊 \_ FLOAT \_ 樣本 \_ \_**](mf-mt-audio-float-samples-per-second-attribute.md) | 每秒 (浮點值) 的每秒音訊樣本數。                                  |
| [**MF \_ MT \_ 音訊 \_ FOLDDOWN \_ 矩陣**](mf-mt-audio-folddown-matrix-attribute.md)                     | 指定音訊解碼器如何將多頻道音訊轉換成身歷聲輸出。        |
| [**MF \_ MT \_ 音訊 \_ 數目 \_ 通道**](mf-mt-audio-num-channels-attribute.md)                           | 音訊聲道數目。                                                                   |
| [**MF \_ MT \_ 音訊 \_ 偏好 \_ WAVEFORMATEX**](mf-mt-audio-prefer-waveformatex-attribute.md)             | 指定轉換音訊媒體類型時要使用的慣用舊版格式結構。 |
| [**\_ \_ \_ \_ 每個 \_ 區塊的 MF MT 音訊範例**](mf-mt-audio-samples-per-block-attribute.md)                | 一個壓縮的音訊資料區塊中包含的音訊樣本數。                    |
| [**\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_**](mf-mt-audio-samples-per-second-attribute.md)              |  (整數值) 的每秒音訊樣本數。                                         |
| [**\_ \_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊有效位數**](mf-mt-audio-valid-bits-per-sample-attribute.md)       | 每個音訊樣本中音訊資料的有效位數。                                    |
| [**MF \_ MT \_ 音訊 \_ WMADRC \_ AVGREF**](mf-mt-audio-wmadrc-avgref-attribute.md)                         | Windows Media 音訊檔案的參考平均音量層級。                               |
| [**MF \_ MT \_ 音訊 \_ WMADRC \_ AVGTARGET**](mf-mt-audio-wmadrc-avgtarget-attribute.md)                   | 以 Windows Media 音訊檔的平均磁片區層級為目標。                                  |
| [**MF \_ MT \_ 音訊 \_ WMADRC \_ PEAKREF**](mf-mt-audio-wmadrc-peakref-attribute.md)                       | 參考 Windows Media 音訊檔案的尖峰磁片區層級。                                  |
| [**MF \_ MT \_ 音訊 \_ WMADRC \_ PEAKTARGET**](mf-mt-audio-wmadrc-peaktarget-attribute.md)                 | Windows Media 音訊檔案的目標尖峰磁片區層級。                                     |
| [MF \_ MT \_ 原始 \_ WAVE \_ 格式 \_ 標記](mf-mt-original-wave-format-tag.md)                            | 包含音訊資料流程的原始 WAVE 格式標記。                                  |



 

## <a name="video-format-attributes"></a>影片格式屬性

這些屬性可以套用至主要類型等於 MFMediaType Video 的媒體類型 \_ 。



| 屬性                                                                              | 描述                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ MT \_ 平均 \_ 位 \_ 誤差 \_ 率**](mf-mt-avg-bit-error-rate-attribute.md)            | 資料錯誤率。                                                                                                                        |
| [**MF \_ MT \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md)                            | 影片資料流程的近似資料速率。                                                                                              |
| [**MF \_ MT \_ 自訂 \_ 影片 \_ 主要複本**](mf-mt-custom-video-primaries-attribute.md)     | 自訂色彩主要複本。                                                                                                                 |
| [**MF \_ MT \_ 預設 \_ STRIDE**](mf-mt-default-stride-attribute.md)                      | 預設介面 stride。                                                                                                                 |
| [**MF \_ MT \_ DRM \_ 旗標**](mf-mt-drm-flags-attribute.md)                                | 指定影片是否需要強制執行禁止複製。                                                                         |
| [**MF \_ MT \_ 幀 \_ 速率**](mf-mt-frame-rate-attribute.md)                              | 畫面播放速率。                                                                                                                             |
| [MF \_ MT \_ 幀 \_ 速率 \_ 範圍 \_ 最大值](mf-mt-frame-rate-range-max.md)                      | 影片捕獲裝置所支援的最大畫面播放速率。                                                                             |
| [MF \_ MT \_ 幀 \_ 速率 \_ 範圍 \_ 最小值](mf-mt-frame-rate-range-min.md)                      | 影片捕獲裝置所支援的最小畫面播放速率。                                                                             |
| [**MF \_ MT \_ 框架 \_ 大小**](mf-mt-frame-size-attribute.md)                              | 影片框架的寬度和高度。                                                                                                    |
| [**MF \_ MT \_ 幾何 \_ 光圈**](mf-mt-geometric-aperture-attribute.md)              | 幾何光圈。                                                                                                                     |
| [**MF \_ MT \_ 交錯 \_ 模式**](mf-mt-interlace-mode-attribute.md)                      | 描述框架如何交錯。                                                                                                |
| [**MF \_ MT \_ 最大主要畫面格 \_ \_ 間距**](mf-mt-max-keyframe-spacing-attribute.md)         | 從一個主要畫面格到下一個的畫面格最大數目。                                                                                |
| [**MF \_ MT \_ 最小 \_ 顯示 \_ 光圈**](mf-mt-minimum-display-aperture-attribute.md) | 最小顯示光圈。                                                                                                               |
| [**MF \_ MT \_ MPEG \_ 序列 \_ 標頭**](mf-mt-mpeg-sequence-header-attribute.md)         | MPEG-2 或 MPEG-2 序列標頭。                                                                                                       |
| [**MF \_ MT \_ MPEG \_ 開始 \_ 時間 \_ 代碼**](mf-mt-mpeg-start-time-code-attribute.md)        | 圖形群組 (GOP) 開始時間程式碼。                                                                                                |
| [**MF \_ MT \_ MPEG2 \_ 旗標**](mf-mt-mpeg2-flags-attribute.md)                            | MPEG-2 影片的其他旗標。                                                                                                   |
| [**MF \_ MT \_ MPEG2 \_ 層級**](mf-mt-mpeg2-level-attribute.md)                            | MPEG-2 或 h.264 層級。                                                                                                                  |
| [**MF \_ MT \_ MPEG2 \_ 設定檔**](mf-mt-mpeg2-profile-attribute.md)                        | MPEG-2 或 h.264 設定檔。                                                                                                                |
| [MF \_ MT \_ 原始 \_ 4CC](mf-mt-original-4cc.md)                                        | 包含影片資料流程的原始編解碼器 FOURCC。                                                                                  |
| [**MF \_ MT \_ 板 \_ 控制 \_ 旗標**](mf-mt-pad-control-flags-attribute.md)               | 輸出矩形的外觀比例。                                                                                                   |
| [**MF \_ MT \_ 調色板**](mf-mt-palette-attribute.md)                                     | 元件專案。                                                                                                                        |
| [**MF \_ MT \_ 平移 \_ 掃描 \_ 光圈**](mf-mt-pan-scan-aperture-attribute.md)               | 定義應以平移/掃描模式顯示之影片的4×3區域。                                                              |
| [**\_已啟用 MF MT \_ PAN \_ 掃描 \_**](mf-mt-pan-scan-enabled-attribute.md)                 | 指定是否啟用 pan/掃描模式。                                                                                             |
| [**MF \_ MT \_ 圖元 \_ 外觀 \_ 比例**](mf-mt-pixel-aspect-ratio-attribute.md)             | 圖元外觀比例。                                                                                                                     |
| [**MF \_ MT \_ 來源 \_ 內容 \_ 提示**](mf-mt-source-content-hint-attribute.md)           | 預期的外觀比例。                                                                                                                  |
| [**MF \_ MT \_ 傳送函式 \_**](mf-mt-transfer-function-attribute.md)                | 從 RGB 轉換成 R'G'B 的函式。                                                                                                 |
| [MF \_ MT \_ 影片 \_ 3d](mf-mt-video-3d.md)                                                | 指定影片資料流程是否包含3D 內容。                                                                                   |
| [**MF \_ MT \_ 視頻 \_ 色度 \_ 地點**](mf-mt-video-chroma-siting-attribute.md)           | 說明如何為 Y'Cb'Cr 的影片取樣色度。                                                                                    |
| [**MF \_ MT \_ 視頻 \_ 光源**](mf-mt-video-lighting-attribute.md)                      | 最佳的觀賞照明條件。                                                                                                |
| [**MF \_ MT \_ 影片 \_ 名義 \_ 範圍**](mf-mt-video-nominal-range-attribute.md)           | 色彩資訊的名義範圍                                                                                                  |
| [**MF \_ MT \_ 影片 \_ 主要複本**](mf-mt-video-primaries-attribute.md)                    | 色彩主要複本。                                                                                                                        |
| [MF \_ MT \_ 影片 \_ 旋轉](mf-mt-video-rotation.md)                                    | 以逆時針方向指定影片框架的旋轉。                                                             |
| [**MF \_ MT \_ YUV \_ 矩陣**](mf-mt-yuv-matrix-attribute.md)                              | 從 Y'Cb'Cr 的色彩空間到 R'G'B 的色彩空間的轉換矩陣。                                                              |
| [MF \_ XVP \_ 呼叫端配置 \_ \_ 輸出](mf-xvp-caller-allocates-output.md)               | 指定呼叫端是否要配置 [**視頻處理器 MFT**](video-processor-mft.md)輸出所用的材質。 |
| [MF \_ XVP \_ 停用 \_ FRC](mf-xvp-disable-frc.md)                                        | 停用 [**視頻處理器 MFT**](video-processor-mft.md)中的畫面播放速率轉換。                                               |



 

## <a name="other-format-attributes"></a>其他格式屬性

下列屬性適用于交錯的 DV 影片。



| 屬性                                                                      | 描述                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**MF \_ MT \_ DV \_ AAUX \_ CTRL \_ PACK \_ 0**](mf-mt-dv-aaux-ctrl-pack-0-attribute.md) | 音訊輔助 (AAUX 第一個音訊區塊的) 原始檔控制套件。 |
| [**MF \_ MT \_ DV \_ AAUX \_ CTRL \_ PACK \_ 1**](mf-mt-dv-aaux-ctrl-pack-1-attribute.md) | AAUX 第二個音訊區塊的原始檔控制套件。                  |
| [**MF \_ MT \_ DV \_ AAUX \_ SRC \_ PACK \_ 0**](mf-mt-dv-aaux-src-pack-0-attribute.md)   | 第一個音訊區塊的 AAUX 來源套件。                           |
| [**MF \_ MT \_ DV \_ AAUX \_ SRC \_ PACK \_ 1**](mf-mt-dv-aaux-src-pack-1-attribute.md)   | 第二個音訊區塊的 AAUX 來源套件。                          |
| [**MF \_ MT \_ DV \_ VAUX \_ CTRL \_ PACK**](mf-mt-dv-vaux-ctrl-pack-attribute.md)      | 影片輔助 (VAUX) 原始檔控制套件。                           |
| [**MF \_ MT \_ DV \_ VAUX \_ SRC \_ PACK**](mf-mt-dv-vaux-src-pack-attribute.md)        | VAUX 來源套件。                                                     |



 

下列屬性適用于 (ASF) 檔案的 Advanced 串流格式。



| 屬性                                                      | 描述                                                      |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [MF \_ MT \_ 任意 \_ 格式](mf-mt-arbitrary-format.md)        | ASF 檔案中二進位資料流程的其他格式資料。       |
| [MF \_ MT \_ 任意 \_ 標頭](mf-mt-arbitrary-header.md)        | ASF 檔案中二進位資料流程的類型特定資料。           |
| [MF \_ MT \_ 映射 \_ 遺失 \_ 容錯](mf-mt-image-loss-tolerant.md) | 指定 ASF 影像資料流程是否為 degradable JPEG 類型。 |



 

下列屬性適用于 MPEG 4 檔案。



| 屬性                                                                     | 描述                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------|
| [MF \_ MT \_ MPEG4 \_ 目前的 \_ 範例 \_ 專案](mf-mt-mpeg4-current-sample-entry.md) | [範例描述] 方塊中目前專案的索引。 |
| [MF \_ MT \_ MPEG4 \_ 範例 \_ 說明](mf-mt-mpeg4-sample-description.md)      | 範例描述方塊。                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> <dt>

[媒體類型](media-types.md)
</dt> <dt>

[音訊媒體類型](audio-media-types.md)
</dt> <dt>

[影片媒體類型](video-media-types.md)
</dt> </dl>

 

 



