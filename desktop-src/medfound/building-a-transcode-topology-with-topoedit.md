---
description: 本主題說明如何在 TopoEdit 中建立轉碼拓撲。
ms.assetid: 9a7b57f9-f606-4874-9fd3-aa37215f6f20
title: 使用 TopoEdit 建立轉碼拓撲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ef750b4dd54ef05ab7733cc861d7a09dd5d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510823"
---
# <a name="building-a-transcode-topology-with-topoedit"></a>使用 TopoEdit 建立轉碼拓撲

本主題說明如何在 TopoEdit 中建立轉碼拓撲。

> [!Note]  
> 這項功能需要 Windows 7

 

## <a name="to-build-a-transcoding-topology"></a>若要建立轉碼拓撲

1.  **在 [檔案**] 功能表上，按一下 [轉譯 **轉碼**]。

2.  在 [ **選取媒體來源** ] 對話方塊中，選取轉碼的原始程式檔。
3.  按一下 [開啟]。
4.  在 [ **選擇轉碼設定檔** ] 對話方塊中，從下拉式清單中選取其中一個 [編碼設定檔]。
    > [!Note]  
    > 設定檔是從檔案 TranscodeProfiles.xml 載入的。

     

5.  在 [ **選擇目標** 檔案] 對話方塊中，選取輸出檔的名稱。
6.  TopoEdit 會建立轉碼拓撲，並在主應用程式視窗中顯示拓撲節點。
7.  按一下工具列上的 [ **播放** ] 按鈕，以執行媒體會話。 等候編碼完成。

## <a name="transcodeprofilesxml"></a>TranscodeProfiles.xml

TopoEdit 會從檔案 TranscodeProfiles.xml 載入編碼設定檔。 這個檔案位於 Windows SDK 的 Bin 目錄中。

檔案的開頭為 **TedTranscodeProfiles** 元素。 每個設定檔的開頭都是 **TedTranscodeProfile** 元素。 每個設定檔都是由一組格式值所組成 `<VALUE_NAME Value="VALUE"/>` 。 系統會定義下列值：



| 值                                                                                                                                                                                                    | 描述                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AudioAvgBytesPerSecond"></span><span id="audioavgbytespersecond"></span><span id="AUDIOAVGBYTESPERSECOND"></span>**AudioAvgBytesPerSecond**<br/>                                         | 音訊串流的每秒平均位元組數。 相當於 [**MF \_ MT \_ 音訊 \_ \_ \_ 每 \_ 秒平均位元組數**](mf-mt-audio-avg-bytes-per-second-attribute.md) 屬性。<br/>                                                |
| <span id="AudioBitsPerSample"></span><span id="audiobitspersample"></span><span id="AUDIOBITSPERSAMPLE"></span>**AudioBitsPerSample**<br/>                                                         | 音訊串流的每個樣本位數。 相當於 [**\_ \_ \_ \_ 每個 \_ 樣本屬性的 MF MT 音訊位數**](mf-mt-audio-bits-per-sample-attribute.md) 。<br/>                                                          |
| <span id="AudioBlockAlignment"></span><span id="audioblockalignment"></span><span id="AUDIOBLOCKALIGNMENT"></span>**AudioBlockAlignment**<br/>                                                     | 音訊串流的區塊對齊。 相當於 [**MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊**](mf-mt-audio-block-alignment-attribute.md) 屬性。<br/>                                                                     |
| <span id="AudioEncodingProfile"></span><span id="audioencodingprofile"></span><span id="AUDIOENCODINGPROFILE"></span>**AudioEncodingProfile**<br/>                                                 | 定義音訊設定檔的編解碼器專用值。 相當於 [MF \_ 轉碼 \_ ENCODINGPROFILE](mf-transcode-encodingprofile.md) 屬性。 <br/>                                                                     |
| <span id="AudioFormat"></span><span id="audioformat"></span><span id="AUDIOFORMAT"></span>**AudioFormat**<br/>                                                                                     | 編碼的音訊子類型。 相當於 [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md) 屬性。<br/>                                                                                                                  |
| <span id="AudioNumChannels"></span><span id="audionumchannels"></span><span id="AUDIONUMCHANNELS"></span>**AudioNumChannels**<br/>                                                                 | 音訊串流中的通道數目。 相當於 [**MF \_ MT \_ 音訊 \_ NUM \_ 通道**](mf-mt-audio-num-channels-attribute.md) 屬性。<br/>                                                                         |
| <span id="AudioSamplesPerSecond"></span><span id="audiosamplespersecond"></span><span id="AUDIOSAMPLESPERSECOND"></span>**AudioSamplesPerSecond**<br/>                                             | 音訊串流的取樣率，以樣本/秒為單位。 相當於 [**\_ \_ \_ \_ 每 \_ 秒的 MF MT 音訊範例**](mf-mt-audio-samples-per-second-attribute.md) 屬性。<br/>                                            |
| <span id="ContainerType"></span><span id="containertype"></span><span id="CONTAINERTYPE"></span>**ContainerType**<br/>                                                                             | 檔案容器類型。 相當於 [MF \_ 轉碼 \_ CONTAINERTYPE](mf-transcode-containertype.md) 屬性。 <br/>                                                                                                       |
| <span id="ProfileName"></span><span id="profilename"></span><span id="PROFILENAME"></span>**ProfileName**<br/>                                                                                     | 設定檔的顯示名稱。<br/>                                                                                                                                                                                            |
| <span id="SkipMetadataTransfer"></span><span id="skipmetadatatransfer"></span><span id="SKIPMETADATATRANSFER"></span>**SkipMetadataTransfer**<br/>                                                 | 如果中繼資料不應該傳送到輸出檔，請指定1，如果應該傳送中繼資料，則指定0。 相當於 [MF \_ 轉碼 \_ 略過 \_ 中繼資料 \_ 傳輸](mf-transcode-skip-metadata-transfer.md) 屬性。<br/> |
| <span id="VideoBitrate"></span><span id="videobitrate"></span><span id="VIDEOBITRATE"></span>**VideoBitrate**<br/>                                                                                 | 平均影片位元速率。 相當於 [**MF \_ MT \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md) 屬性。 <br/>                                                                                                        |
| <span id="VideoEncodeComplexity"></span><span id="videoencodecomplexity"></span><span id="VIDEOENCODECOMPLEXITY"></span>**VideoEncodeComplexity**<br/>                                             | 定義編碼品質的編解碼器專用值。 相當於 [MF \_ 轉碼 \_ QUALITYVSSPEED](mf-transcode-qualityvsspeed.md) 屬性。 <br/>                                                                      |
| <span id="VideoEncodingProfile"></span><span id="videoencodingprofile"></span><span id="VIDEOENCODINGPROFILE"></span>**VideoEncodingProfile**<br/>                                                 | 定義影片設定檔的編解碼器專用值。 相當於 [MF \_ 轉碼 \_ ENCODINGPROFILE](mf-transcode-encodingprofile.md) 屬性。 <br/>                                                                     |
| <span id="VideoFormat"></span><span id="videoformat"></span><span id="VIDEOFORMAT"></span>**VideoFormat**<br/>                                                                                     | 編碼的影片子類型。 相當於 [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md) 屬性。<br/>                                                                                                                  |
| <span id="VideoFrameHeight"></span><span id="videoframeheight"></span><span id="VIDEOFRAMEHEIGHT"></span>**VideoFrameHeight**<br/>                                                                 | 輸出影片的高度。 相當於 [**MF \_ MT \_ 框架 \_ 大小**](mf-mt-frame-size-attribute.md) 屬性。<br/>                                                                                                      |
| <span id="VideoFrameRateDenominator"></span><span id="videoframeratedenominator"></span><span id="VIDEOFRAMERATEDENOMINATOR"></span>**VideoFrameRateDenominator**<br/>                             | 輸出影片畫面播放速率的分母。 相當於 [**MF \_ MT \_ 幀 \_ 速率**](mf-mt-frame-rate-attribute.md) 屬性。<br/>                                                                               |
| <span id="VideoFrameRateNumerator"></span><span id="videoframeratenumerator"></span><span id="VIDEOFRAMERATENUMERATOR"></span>**VideoFrameRateNumerator**<br/>                                     | 輸出影片畫面播放速率的分子。 相當於 [**MF \_ MT \_ 幀 \_ 速率**](mf-mt-frame-rate-attribute.md) 屬性。<br/>                                                                                 |
| <span id="VideoFrameWidth"></span><span id="videoframewidth"></span><span id="VIDEOFRAMEWIDTH"></span>**VideoFrameWidth**<br/>                                                                     | 輸出影片的寬度。 相當於 [**MF \_ MT \_ 框架 \_ 大小**](mf-mt-frame-size-attribute.md) 屬性。<br/>                                                                                                       |
| <span id="VideoPixelAspectRatioDenominator"></span><span id="videopixelaspectratiodenominator"></span><span id="VIDEOPIXELASPECTRATIODENOMINATOR"></span>**VideoPixelAspectRatioDenominator**<br/> | 圖元外觀比例的分母 (等同于輸出影片的) 。 相當於 [**MF \_ MT \_ 圖元 \_ 外觀 \_ 比例**](mf-mt-pixel-aspect-ratio-attribute.md) 屬性。 <br/>                                               |
| <span id="VideoPixelAspectRatioNumerator"></span><span id="videopixelaspectrationumerator"></span><span id="VIDEOPIXELASPECTRATIONUMERATOR"></span>**VideoPixelAspectRatioNumerator**<br/>         | 輸出影片的的分子。 相當於 [**MF \_ MT \_ 圖元 \_ 外觀 \_ 比例**](mf-mt-pixel-aspect-ratio-attribute.md) 屬性。 <br/>                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




