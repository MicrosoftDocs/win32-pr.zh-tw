---
description: 編解碼器 API 列舉
ms.assetid: 5d6e48cb-d181-448e-a96e-e5ab500427d7
title: 編解碼器 API 列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28b82d73d6bd6fefed5f3c9296a666d1053cd71b074a782858b31e94dc3a3ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079328"
---
# <a name="codec-api-enumerations"></a>編解碼器 API 列舉



| 列舉型別                                                                              | 描述                                                                                               |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig)                                   | 指定音訊位串流中音訊頻道的喇叭設定。                       |
| [**eAVDDSurroundMode**](/windows/desktop/api/codecapi/ne-codecapi-eavddsurroundmode)                                           | 指定音訊是否以杜住範圍編碼。                                                 |
| [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode)                                     | 指定 AAC 解碼器是否使用標準的 MPEG-2/MPEG-4 身歷聲 downmix 方程式。                    |
| [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono)                                       | 指定輸入音訊資料流程是身歷聲或雙 mono。                                          |
| [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode)                     | 指定解碼器如何重現雙重 mono 音訊。                                                     |
| [**eAVDecDDOperationalMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecddoperationalmode)                               | 指定杜比 AC-3 音訊串流的壓縮控制模式。                                     |
| [**eAVDecHEAACDynamicRangeControl**](/windows/desktop/api/codecapi/ne-codecapi-eavdecheaacdynamicrangecontrol)                 | 指定 AAC 解碼器是否執行動態範圍控制項。                                          |
| [**eAVDecVideoInputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype)                             | 指定已解碼的影片資料流程如何交錯。                                                     |
| [**eAVDecVideoSoftwareDeinterlaceMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideosoftwaredeinterlacemode)         | 指定影片解碼的軟體交錯模式。                                                    |
| [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel)                               | 指定視頻解碼器的省電層級。                                                      |
| [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization)                         | 指定是否在音訊解碼器或數位訊號處理器 (DSP) 啟用音量均衡。 |
| [**eAVDSPSpeakerFill**](/windows/desktop/api/codecapi/ne-codecapi-eavdspspeakerfill)                                           | 指定是否在音訊解碼器或 DSP 中啟用喇叭填滿。                                     |
| [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono)                                       | 指定雙聲道音訊是否編碼為身歷聲或雙 mono。                                      |
| [**eAVEncAudioInputContent 列舉**](/windows/win32/api/codecapi/ne-codecapi-eavencaudioinputcontent)                   | 指定音訊內容是否包含音樂或語音。                                              |
| [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode)                       | 指定速率控制模式。                                                                          |
| [**eAVEncCommonStreamEndHandling**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonstreamendhandling)                   | 指定編碼器是否在資料流程的結尾 (Gop) 捨棄部分的圖片群組。        |
| [**eAVEncDDAtoDConverterType**](/windows/win32/api/codecapi/ne-codecapi-eavencddatodconvertertype)                           | 指定最杜數位音訊串流的類比到數位 (A/D) 轉換的類型。                |
| [**eAVEncDDDynamicRangeCompressionControl**](/windows/win32/api/codecapi/ne-codecapi-eavencdddynamicrangecompressioncontrol) | 指定杜比數位音訊串流中的動態範圍控制項設定檔。                              |
| [**eAVEncDDHeadphoneMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddheadphonemode)                                   | 指定杜比數位音訊串流的耳機模式。                                                |
| [**eAVEncDDPreferredStereoDownMixMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddpreferredstereodownmixmode)         | 指定杜比數位音訊串流慣用的身歷聲 downmix 模式。                             |
| [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype)                         | 指定杜比數位音訊串流的房間類型。                                                 |
| [**eAVEncDDService**](/windows/desktop/api/codecapi/ne-codecapi-eavencddservice)                                               | 指定包含在杜比數位音訊串流中的音訊服務。                                    |
| [**eAVEncDDSurroundExMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddsurroundexmode)                                 | 指定杜比數位音訊資料流程是否以杜數位環繞（例如）編碼。                   |
| [**eAVEncInputVideoSystem**](/windows/desktop/api/codecapi/ne-codecapi-eavencinputvideosystem)                                 | 指定影片來源的名義範圍。                                                           |
| [**eAVEncMPACodingMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpacodingmode)                                       | 指定 MPEG 音訊編碼模式。                                                                   |
| [**eAVEncMPAEmphasisType**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype)                                   | 指定解碼時應該使用的反強調篩選類型。                               |
| [**eAVEncMPALayer**](/windows/win32/api/codecapi/ne-codecapi-eavencmpalayer)                                                 | 指定 MPEG 音訊層。                                                                           |
| [**eAVEncMPVFrameFieldMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvframefieldmode)                               | 指定編碼器是否產生編碼的欄位或編碼的畫面格。                                  |
| [**eAVEncMPVIntraVLCTable**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvintravlctable)                                 | 指定要用於熵編碼的 (VLC) 資料表的可變長度編碼。                             |
| [**eAVEncMPVLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvlevel)                                                 | 指定 MPEG-2 設定檔。                                                                             |
| [**eAVEncMPVProfile**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvprofile)                                             | 指定 MPEG-2 設定檔。                                                                             |
| [**eAVEncMPVQScaleType**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvqscaletype)                                       | 指定 quantizer 小數位數為線性或非線性。                                            |
| [**eAVEncMPVScanPattern**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvscanpattern)                                     | 指定巨大區塊掃描模式。                                                                    |
| [**eAVEncMPVSceneDetection**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvscenedetection)                               | 指定編碼器偵測到新場景時的行為。                                            |
| [**eAVEncMuxOutput**](/windows/win32/api/codecapi/ne-codecapi-eavencmuxoutput)                                               | 指定多工器所產生的輸出資料流程類型。                                            |
| [**eAVEncVideoChromaResolution**](/windows/win32/api/codecapi/ne-codecapi-eavencvideochromaresolution)                       | 指定色度解析度。                                                                              |
| [**eAVEncVideoChromaSubsampling**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideochromasubsampling)                     | 指定色度地點。                                                                                  |
| [**eAVEncVideoColorLighting**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolorlighting)                             | 指定用於觀看影片來源的預期燈光條件。                                    |
| [**eAVEncVideoColorNominalRange**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolornominalrange)                     | 指定影片來源的名義範圍。                                                           |
| [**eAVEncVideoColorPrimaries**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolorprimaries)                           | 指定影片的色彩主要複本。                                                               |
| [**eAVEncVideoColorTransferFunction**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolortransferfunction)             | 指定從 R'G'B 至 RGB 的轉換函數。                                                     |
| [**eAVEncVideoColorTransferMatrix**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolortransfermatrix)                 | 指定從 Y'Cb'Cr 的色彩空間到 R'G'B 的色彩空間的轉換矩陣。                  |
| [**eAVEncVideoFilmContent**](/windows/win32/api/codecapi/ne-codecapi-eavencvideofilmcontent)                                 | 指定輸入影片的原始來源是否為電影或影片。                               |
| [**eAVEncVideoOutputFrameRateConversion**](/windows/win32/api/codecapi/ne-codecapi-eavencvideooutputframerateconversion)     | 指定編碼器是否轉換畫面播放速率。                                                    |
| [**eAVEncVideoOutputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavencvideooutputscantype)                           | 指定編碼器 interlaces 輸出影片的方式。                                                    |
| [**eAVEncVideoSourceScanType**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideosourcescantype)                           | 指定編碼器的輸入框架是否為漸進式或交錯式。                          |
| [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode)                                           | 指定影片解碼速度。                                                                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[編解碼器 API 參考](codec-api-reference.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 
