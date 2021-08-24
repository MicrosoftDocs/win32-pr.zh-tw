---
description: 編解碼器 API 屬性
ms.assetid: 5d527af7-07cf-42e2-99bb-d56c856cc1bc
title: 編解碼器 API 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91346b6595944b8e95da5e9e43023052119e49a8b88809fce08b6fca780beba1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792908"
---
# <a name="codec-api-properties"></a>編解碼器 API 屬性

-   [常用音訊屬性](#common-audio-properties)
-   [一般的解碼器屬性](#common-decoder-properties)
-   [一般編碼器屬性](#common-encoder-properties)
-   [影片解碼屬性](#video-decoder-properties)
-   [音訊解碼器屬性](#audio-decoder-properties)
-   [影片編碼器屬性](#video-encoder-properties)
-   [音訊編碼器屬性](#audio-encoder-properties)
-   [MPEG 影片編碼器屬性](#mpeg-video-encoder-properties)
-   [MPEG 音訊編碼器屬性](#mpeg-audio-encoder-properties)
-   [杜比數位音訊解碼器屬性](#dolby-digital-audio-decoder-properties)
-   [杜比數位音訊編碼器屬性](#dolby-digital-audio-encoder-properties)
-   [ (DSP) 屬性的數位信號處理](#digital-signal-processing-dsp-properties)

### <a name="common-audio-properties"></a>常用音訊屬性

這些屬性同時適用于音訊編碼器和音訊編碼器。



| 屬性                                                      | 描述                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**AVAudioChannelConfig**](avaudiochannelconfig-property.md) | 取得音訊位串流中音訊頻道的喇叭設定。 |
| [**AVAudioChannelCount**](avaudiochannelcount-property.md)   | 取得音訊位資料流程中的通道數目。                           |
| [**AVAudioSampleRate**](avaudiosamplerate-property.md)       | 取得音訊位資料流程的取樣率，以每秒樣本數為單位。          |
| [**AVDDSurroundMode**](avddsurroundmode-property.md)         | 指定音訊是否以杜住範圍編碼。                      |



 

### <a name="common-decoder-properties"></a>一般的解碼器屬性

這些屬性同時適用于音訊解碼器和影片解碼器。



| 屬性                                                            | 描述                                                                             |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md)   | 指定此解碼器的目前輸入格式。                                     |
| [**AVDecCommonMeanBitRate**](avdeccommonmeanbitrate.md)            | 取得此解碼器目前的平均位元速率。                                          |
| [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) | 指定此解碼器的輸出格式。                                            |
| [**AVDecMmcssClass**](avdecmmcss-property.md)                      | 指定解碼執行緒的多媒體類別排程器服務 (MMCSS) 類別。 |



 

### <a name="common-encoder-properties"></a>一般編碼器屬性

這些屬性同時適用于音訊編碼器和影片編碼器。



| 屬性                                                                          | 描述                                                                                                     |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**AVEncCodecType**](avenccodectype-property.md)                                 | 指定編碼配置。                                                                                  |
| [**AVEncCommonBufferInLevel**](avenccommonbufferinlevel-property.md)             | 指定編碼緩衝區的初始層級。                                                             |
| [**AVEncCommonBufferOutLevel**](avenccommonbufferoutlevel-property.md)           | 在編碼程式結束時指定編碼緩衝區的最終層級。                            |
| [**AVEncCommonBufferSize**](avenccommonbuffersize-property.md)                   | 指定編碼期間使用的緩衝區大小。                                                          |
| [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)       | 指定編碼器的目標格式。                                                                     |
| [**AVEncCommonLowLatency**](avenccommonlowlatency-property.md)                   | 指定是否應將輸出資料流程結構化，以便編碼的資料流程具有低解碼延遲。 |
| [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md)                   | 指定最大位元速率。                                                                                 |
| [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)                 | 指定平均位元速率。                                                                                 |
| [**AVEncCommonMeanBitRateInterval**](avenccommonmeanbitrateinterval-property.md) | 指定套用平均位元速率的時間間隔。                                            |
| [**AVEncCommonMinBitRate**](avenccommonminbitrate-property.md)                   | 指定最小位元速率。                                                                                 |
| [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md)             | 指定編碼器支援的編碼傳遞數目。                                              |
| [**AVEncCommonPassEnd**](avenccommonpassend-property.md)                         | 停止目前的編碼階段，或查詢目前的編碼傳遞是否為最後一次。                  |
| [**AVEncCommonPassStart**](avenccommonpassstart-property.md)                     | 啟動第一次編碼傳遞。                                                                                 |
| [**AVEncCommonQuality**](avenccommonquality-property.md)                         | 指定編碼的品質等級。                                                                       |
| [**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md)           | 指定編碼品質與速度之間的取捨。                                                      |
| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md)         | 指定速率控制模式。                                                                                |
| [**AVEncCommonRealTime**](avenccommonrealtime-property.md)                       | 指定應用程式是否需要即時編碼效能。                                      |
| [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md)     | 指定編碼器是否在資料流程的結尾 (Gop) 捨棄部分的圖片群組。              |
| [**AVEncMuxOutputStreamType**](avencmuxoutputstreamtype.md)                      | 指定多工器所產生的輸出資料流程類型。                                                  |
| [**AVEncStatCommonCompletedPasses**](avencstatcommoncompletedpasses-property.md) | 指定已完成的編碼傳遞數目。                                                              |



 

### <a name="video-decoder-properties"></a>影片解碼屬性



| 屬性                                                                                | 描述                                                                     |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**AVDecVideoAcceleration \_ H264**](avdecvideoacceleration-h264-property.md)            | 啟用或停用 h.264 影片解碼的硬體加速。             |
| [**AVDecVideoAcceleration \_ MPEG2**](avdecvideoacceleration-mpeg2-property.md)          | 啟用或停用 MPEG-2 影片解碼的硬體加速。            |
| [**AVDecVideoAcceleration \_ VC1**](avdecvideoacceleration-vc1-property.md)              | 啟用或停用 VC-1 video 解碼的硬體加速。              |
| [**AVDecVideoDropPicWithMissingRef**](avdecvideodroppicwithmissingref-property.md)     | 指定解碼器是否在有遺漏參考框架的框架內卸載。 |
| [**AVDecVideoFastDecodeMode**](avdecvideofastdecodemode.md)                            | 取得或設定影片解碼速度。                                          |
| [**AVDecVideoImageSize**](avdecvideoimagesize.md)                                      | 取得已解碼影像的大小（以圖元為單位）。                                  |
| [**AVDecVideoInputScanType**](avdecvideoinputscantype-property.md)                     | 指定已解碼的影片資料流程如何交錯。                           |
| [**AVDecVideoPixelAspectRatio**](avdecvideopixelaspectratio-property.md)               | 指定已解碼影片資料流程的圖元外觀比例。                   |
| [**AVDecVideoSoftwareDeinterlaceMode**](avdecvideosoftwaredeinterlacemode-property.md) | 指定解碼器的軟體逐行掃描模式。                              |
| [**AVDecVideoSWPowerLevel**](avdecvideoswpowerlevel-property.md)                       | 指定省電層級。                                               |
| [**AVDecVideoThumbnailGenerationMode**](avdecvideothumbnailgenerationmode-property.md) | 啟用或停用縮圖產生模式。                                  |



 

### <a name="audio-decoder-properties"></a>音訊解碼器屬性



| 屬性                                                                        | 描述                                                                                                            |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**AVDecAACDownmixMode**](avdecaacdownmixmode-property.md)                     | 指定 AAC 解碼器是否使用標準的 MPEG-2/MPEG-4 身歷聲 downmix 方程式，或使用非標準的 downmix。 |
| [**AVDecAudioDualMono**](avdecaudiodualmono-property.md)                       | 指定雙聲道音訊是否編碼為身歷聲或雙 mono。                                                   |
| [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md)     | 指定解碼器如何重現雙重 mono 音訊。                                                                  |
| [**AVDecHEAACDynamicRangeControl**](avdecheaacdynamicrangecontrol-property.md) | 啟用或停用 AAC 解碼器中的動態範圍控制項。                                                           |



 

### <a name="video-encoder-properties"></a>影片編碼器屬性



| 屬性                                                                                        | 描述                                                                                                           |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)                                 | 指定來源內容的視頻系統。                                                                     |
| [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md)                         | 傳回已編碼的影片框架數目。                                                                 |
| [**AVEncStatVideoOutputFrameRate**](avencstatvideooutputframerate-property.md)                 | 傳回影片內容的平均畫面播放速率。                                                                  |
| [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md)                         | 傳回編碼器收到的影片框架數目。                                                         |
| [**AVEncVideoCBRMotionTradeoff**](avencvideocbrmotiontradeoff-property.md)                     | 指定移動與靜止影像之間的取捨。                                                               |
| [**AVEncVideoCodedVideoAccessUnitSize**](avencvideocodedvideoaccessunitsize-property.md)       | 指定影片存取單位的大小。                                                                         |
| [**AVEncVideoDefaultUpperFieldDominant**](avencvideodefaultupperfielddominant-property.md)     | 指定先顯示的欄位。                                                                             |
| [**AVEncVideoDisplayDimension**](avencvideodisplaydimension-property.md)                       | 指定解碼時影片資料流程的大小。                                                            |
| [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md)                         | 指定已編碼影片的寬度和高度（如果影片已裁剪）。                                         |
| [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md)                   | 指定裁剪矩形的左邊和左上角（如果影片已裁剪）。                                |
| [**AVEncVideoFieldSwap**](avencvideofieldswap-property.md)                                     | 反轉來源影片中交錯欄位的順序。                                                      |
| [**AVEncVideoForceSourceScanType**](avencvideoforcesourcescantype-property.md)                 | 指定輸入框架是漸進式或交錯式。                                                     |
| [**AVEncVideoHeaderDropFrame**](avencvideoheaderdropframe-property.md)                         | 在 GOP 標頭中指定放置框架旗標的值。                                                             |
| [**AVEncVideoHeaderFrames**](avencvideoheaderframes-property.md)                               | 指定 GOP 標頭中的起始框架編號。                                                                |
| [**AVEncVideoHeaderHours**](avencvideoheaderhours-property.md)                                 | 指定 GOP 標頭中的起始小時數。                                                                 |
| [**AVEncVideoHeaderMinutes**](avencvideoheaderminutes-property.md)                             | 指定 GOP 標頭中的開始分鐘數。                                                               |
| [**AVEncVideoHeaderSeconds**](avencvideoheaderseconds-property.md)                             | 指定 GOP 標頭中的起始第二個數字。                                                               |
| [**AVEncVideoInputChromaResolution**](avencvideoinputchromaresolution-property.md)             | 指定輸入影片的色度解析度。                                                                   |
| [**AVEncVideoInputChromaSubsampling**](avencvideoinputchromasubsampling-property.md)           | 指定輸入影片的色度地點。                                                                      |
| [**AVEncVideoInputColorLighting**](avencvideoinputcolorlighting-property.md)                   | 指定用於觀看輸入影片的預期光源條件。                                               |
| [**AVEncVideoInputColorNominalRange**](avencvideoinputcolornominalrange-property.md)           | 指定輸入影片的名義範圍。                                                                      |
| [**AVEncVideoInputColorPrimaries**](avencvideoinputcolorprimaries-property.md)                 | 指定輸入影片的色彩主要複本。                                                                    |
| [**AVEncVideoInputColorTransferFunction**](avencvideoinputcolortransferfunction-property.md)   | 針對輸入影片，指定從 RGB 到 R'G'B 的轉換函式                                                  |
| [**AVEncVideoInputColorTransferMatrix**](avencvideoinputcolortransfermatrix-property.md)       | 針對輸入影片，指定從 Y'Cb'Cr 的色彩空間到 R'G'B 的色彩空間的轉換矩陣。         |
| [**AVEncVideoInverseTelecineEnable**](avencvideoinversetelecineenable-property.md)             | 指定編碼器是否執行反向電視電影。                                                              |
| [**AVEncVideoInverseTelecineThreshold**](avencvideoinversetelecinethreshold-property.md)       | 設定編碼器將「影片」欄位視為多餘的閾值。                                            |
| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)                 | 指定主要畫面格之間的最大框架數目。                                                            |
| [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md)                   | 指定要編碼的欄位數目。                                                                             |
| [**AVEncVideoNoOfFieldsToSkip**](avencvideonooffieldstoskip-property.md)                       | 指定編碼期間要跳過的欄位數目。                                                               |
| [**AVEncVideoOutputChromaResolution**](avencvideooutputchromaresolution-property.md)           | 指定編碼影片的色度解析度。                                                                 |
| [**AVEncVideoOutputChromaSubsampling**](avencvideooutputchromasubsampling-property.md)         | 指定編碼影片的色度地點。                                                                    |
| [**AVEncVideoOutputColorLighting**](avencvideooutputcolorlighting-property.md)                 | 指定用於觀看編碼影片的預期光源條件。                                             |
| [**AVEncVideoOutputColorNominalRange**](avencvideooutputcolornominalrange-property.md)         | 指定編碼影片的名義範圍。                                                                    |
| [**AVEncVideoOutputColorPrimaries**](avencvideooutputcolorprimaries-property.md)               | 指定編碼影片的色彩主要複本。                                                                  |
| [**AVEncVideoOutputColorTransferFunction**](avencvideooutputcolortransferfunction-property.md) | 針對編碼的影片，指定從 RGB 到 R'G'B 的轉換函數。                                               |
| [**AVEncVideoOutputColorTransferMatrix**](avencvideooutputcolortransfermatrix-property.md)     | 針對編碼的影片，指定從 Y'Cb'Cr 的色彩空間到 R'G'B 的色彩空間的轉換矩陣。       |
| [**AVEncVideoOutputFrameRate**](avencvideooutputframerate-property.md)                         | 指定編碼器輸出資料流程的畫面播放速率（以每秒畫面格數為單位）。                                        |
| [**AVEncVideoOutputFrameRateConversion**](avencvideooutputframerateconversion-property.md)     | 指定當輸出畫面播放速率不符合輸入畫面播放速率時，編碼器是否轉換畫面播放速率。 |
| [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md)                           | 指定編碼器 interlaces 輸出影片的方式。                                                                |
| [**AVEncVideoPixelAspectRatio**](avencvideopixelaspectratio-property.md)                       | 指定圖元外觀比例。                                                                                     |
| [**AVEncVideoSourceFilmContent**](avencvideosourcefilmcontent-property.md)                     | 指定輸入影片的原始來源是否為電影或影片。                                           |
| [**AVEncVideoSourceIsBW**](avencvideosourceisbw-property.md)                                   | 指定影片是否為單色 (黑色和白色) 或包含色彩。                                        |



 

### <a name="audio-encoder-properties"></a>音訊編碼器屬性



| 屬性                                                                        | 描述                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**AVEncAudioDualMono**](avencaudiodualmono-property.md)                       | 指定雙聲道音訊是否編碼為身歷聲或雙 mono。                |
| [**AVEncAudioInputContent**](avencaudioinputcontent-property.md)               | 指定音訊內容是否包含音樂或語音。                        |
| [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md)       | 指定要編碼的音訊樣本數。                                    |
| [**AVEncAudioIntervalToSkip**](avencaudiointervaltoskip-property.md)           | 指定要略過之編碼器的音訊樣本數。                      |
| [**AVEncAudioMapDestChannel N**](avencaudiomapdestchanneln-property.md)        | 指定將哪個音訊通道對應到編碼音訊串流中的 channel *N* 。 |
| [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md)                          | 指定編碼音訊串流的平均位元速率。                         |
| [**AVEncStatAudioAverageBPS**](avencstataudioaveragebps-property.md)           | 傳回編碼音訊的每秒平均位數。                           |
| [**AVEncStatAudioAveragePCMValue**](avencstataudioaveragepcmvalue-property.md) | 傳回音頻內容的平均音量層級。                              |
| [**AVEncStatAudioPeakPCMValue**](avencstataudiopeakpcmvalue-property.md)       | 傳回音頻內容中出現的最高音量層級。             |



 

### <a name="mpeg-video-encoder-properties"></a>MPEG 影片編碼器屬性



| 屬性                                                                                    | 描述                                                                          |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**AVEncMPVAddSeqEndCode**](avencmpvaddseqendcode-property.md)                             | 指定編碼器是否在資料流程結尾新增序列結束代碼。     |
| [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)               | 指定 I 與 P 框架之間的連續 B 框架預設數目。         |
| [**AVEncMPVFrameFieldMode**](avencmpvframefieldmode-property.md)                           | 指定編碼器是否產生編碼的欄位或編碼的畫面格。             |
| [**AVEncMPVGenerateHeaderPicDispExt**](avencmpvgenerateheaderpicdispext-property.md)       | 指定編碼器是否產生圖片顯示延伸標頭。           |
| [**AVEncMPVGenerateHeaderPicExt**](avencmpvgenerateheaderpicext-property.md)               | 指定編碼器是否產生圖片延伸標頭。                   |
| [**AVEncMPVGenerateHeaderSeqDispExt**](avencmpvgenerateheaderseqdispext-property.md)       | 指定編碼器是否產生順序顯示延伸標頭。          |
| [**AVEncMPVGenerateHeaderSeqExt**](avencmpvgenerateheaderseqext-property.md)               | 指定編碼器是否產生順序延伸標頭。                  |
| [**AVEncMPVGenerateHeaderSeqScaleExt**](avencmpvgenerateheaderseqscaleext-property.md)     | 指定編碼器是否產生序列可擴充的延伸模組標頭。         |
| [**AVEncMPVGOPOpen**](avencmpvgopopen-property.md)                                         | 指定編碼器是否會產生 open Gop 或 closed Gop。                     |
| [**AVEncMPVGOPSInSeq**](avencmpvgopsinseq-property.md)                                     | 指定序列標頭之間的 Gop 數目。                               |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)                                         | 指定從某個 GOP 標頭到下一個 GOP 標頭的圖片數目上限。 |
| [**AVEncMPVIntraDCPrecision**](avencmpvintradcprecision-property.md)                       | 指定 DC 係數的有效位數。                                      |
| [**AVEncMPVIntraVLCTable**](avencmpvintravlctable-property.md)                             | 指定要用於熵編碼的 (VLC) 資料表的可變長度編碼。        |
| [**AVEncMPVLevel**](avencmpvlevel-property.md)                                             | 指定 MPEG-2 層級。                                                          |
| [**AVEncMPVProfile**](avencmpvprofile-property.md)                                         | 指定 MPEG-2 設定檔。                                                        |
| [**AVEncMPVQScaleType**](avencmpvqscaletype-property.md)                                   | 指定 quantizer 小數位數為線性或非線性。                       |
| [**AVEncMPVQuantMatrixChromaIntra**](avencmpvquantmatrixchromaintra-property.md)           | 指定巨大區塊內的色度量化矩陣。                      |
| [**AVEncMPVQuantMatrixChromaNonIntra**](avencmpvquantmatrixchromanonintra-property.md)     | 指定非內部巨大區塊的色度量化矩陣。                  |
| [**AVEncMPVQuantMatrixIntra**](avencmpvquantmatrixintra-property.md)                       | 指定巨大區塊內部的 luma 量化矩陣。                        |
| [**AVEncMPVQuantMatrixNonIntra**](avencmpvquantmatrixnonintra-property.md)                 | 指定非內部巨大區塊的 luma 量化矩陣。                    |
| [**AVEncMPVScanPattern**](avencmpvscanpattern-property.md)                                 | 指定巨大區塊掃描模式。                                               |
| [**AVEncMPVSceneDetection**](avencmpvscenedetection-property.md)                           | 指定編碼器偵測到新場景時的行為。                       |
| [**AVEncMPVUseConcealmentMotionVectors**](avencmpvuseconcealmentmotionvectors-property.md) | 指定編碼器是否使用 concealment 的動作向量。                       |



 

### <a name="mpeg-audio-encoder-properties"></a>MPEG 音訊編碼器屬性



| 屬性                                                                                  | 描述                                                                   |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**AVEncMPACodingMode**](avencmpacodingmode-property.md)                                 | 指定 MPEG-2 音訊編碼模式。                                     |
| [**AVEncMPACopyright**](avencmpacopyright-property.md)                                   | 指定著作權位的預設設定。                          |
| [**AVEncMPAEmphasisType**](avencmpaemphasistype-property.md)                             | 指定解碼時應該使用的反強調篩選類型。   |
| [**AVEncMPAEnableRedundancyProtection**](avencmpaenableredundancyprotection-property.md) | 指定是否要將迴圈冗余檢查 (CRC) 新增至框架頁首。 |
| [**AVEncMPALayer**](avencmpalayer-property.md)                                           | 指定 MPEG 音訊層。                                               |
| [**AVEncMPAOriginalBitstream**](avencmpaoriginalbitstream-property.md)                   | 指定原始位的預設設定。                           |
| [**AVEncMPAPrivateUserBit**](avencmpaprivateuserbit-property.md)                         | 設定私用使用者位的值。                                       |



 

### <a name="dolby-digital-audio-decoder-properties"></a>杜比數位音訊解碼器屬性



| 屬性                                                                      | 描述                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**AVDecDDDynamicRangeScaleHigh**](avdecdddynamicrangescalehigh-property.md) | 指定當解碼器執行動態範圍控制時的高階剪下。  |
| [**AVDecDDDynamicRangeScaleLow**](avdecdddynamicrangescalelow-property.md)   | 指定當解碼器執行動態範圍控制時的低層級提升。 |
| [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md)             | 指定壓縮控制模式。                                        |



 

### <a name="dolby-digital-audio-encoder-properties"></a>杜比數位音訊編碼器屬性



| 屬性                                                                                        | 描述                                                                               |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**AVEncDDAtoDConverterType**](avencddatodconvertertype-property.md)                           | 指定類比到數位 (A/D) 轉換的類型。                                 |
| [**AVEncDDCentreDownMixLevel**](avencddcentredownmixlevel-property.md)                         | 指定中央 downmix 層級。                                                       |
| [**AVEncDDChannelBWLowPassFilter**](avencddchannelbwlowpassfilter-property.md)                 | 指定是否將低傳遞篩選套用至主要輸入通道。                |
| [**AVEncDDCopyright**](avencddcopyright-property.md)                                           | 指定著作權旗標。                                                             |
| [**AVEncDDDCHighPassFilter**](avencdddchighpassfilter-property.md)                             | 指定是否套用 DC 封鎖的高通過篩選。                              |
| [**AVEncDDDialogNormalization**](avencdddialognormalization-property.md)                       | 指定對話方塊正規化層級。                                                 |
| [**AVEncDDDigitalDeemphasis**](avencdddigitaldeemphasis-property.md)                           | 指定數位消除強調。                                                    |
| [**AVEncDDDynamicRangeCompressionControl**](avencdddynamicrangecompressioncontrol-property.md) | 指定動態範圍控制項設定檔。                                              |
| [**AVEncDDHeadphoneMode**](avencddheadphonemode-property.md)                                   | 指定耳機模式。                                                             |
| [**AVEncDDLFELowPassFilter**](avencddlfelowpassfilter-property.md)                             | 指定是否將低傳遞篩選套用至低頻率效果 (LFE) 通道。 |
| [**AVEncDDLoRoCenterMixLvl \_ x10**](avencddlorocentermixlvl-x10-property.md)                    | 指定適用于 Lo/Ro downmixing 中間頻道的層級移位。     |
| [**AVEncDDLoRoSurroundMixLvl \_ x10**](avencddlorosurroundmixlvl-x10-property.md)                | 指定套用至 Lo/Ro downmixing 之環繞通道的層級位移。  |
| [**AVEncDDLtRtCenterMixLvl \_ x10**](avencddltrtcentermixlvl-x10-property.md)                    | 指定套用至 Lt/Rt downmixing 中間頻道的層級位移。     |
| [**AVEncDDLtRtSurroundMixLvl \_ x10**](avencddltrtsurroundmixlvl-x10-property.md)                | 指定套用至 Lt/Rt downmixing 之環繞通道的層級位移。  |
| [**AVEncDDOriginalBitstream**](avencddoriginalbitstream-property.md)                           | 指定原始的位流旗標。                                                    |
| [**AVEncDDPreferredStereoDownMixMode**](avencddpreferredstereodownmixmode-property.md)         | 指定慣用的身歷聲 downmix 模式。                                              |
| [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md)                     | 指定音訊生產資訊旗標。                                          |
| [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md)                         | 指定混合層級。                                                               |
| [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md)                         | 指定房間類型。                                                                  |
| [**AVEncDDRFPreEmphasisFilter**](avencddrfpreemphasisfilter-property.md)                       | 指定 RF overmodulation 保護設定。                                       |
| [**AVEncDDService**](avencddservice-property.md)                                               | 指定音訊服務。                                                              |
| [**AVEncDDSurround3dBAttenuation**](avencddsurround3dbattenuation-property.md)                 | 指定是否在編碼之前衰減環繞通道。                   |
| [**AVEncDDSurround90DegreeePhaseShift**](avencddsurround90degreeephaseshift-property.md)       | 指定是否要將90度階段移位套用到環繞聲道。            |
| [**AVEncDDSurroundDownMixLevel**](avencddsurrounddownmixlevel-property.md)                     | 指定環繞混合層級。                                                    |
| [**AVEncDDSurroundExMode**](avencddsurroundexmode-property.md)                                 | 指定音訊資料流程是否編碼于範圍 EX 中。                             |



 

### <a name="digital-signal-processing-dsp-properties"></a> (DSP) 屬性的數位信號處理



| 屬性                                                                | 描述                               |
|-------------------------------------------------------------------------|-------------------------------------------|
| [**AVDSPLoudnessEqualization**](avdsploudnessequalization-property.md) | 啟用或停用音量均衡 |
| [**AVDSPSpeakerFill**](avdspspeakerfill-property.md)                   | 啟用或停用說話者填滿          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[編解碼器 API 參考](codec-api-reference.md)
</dt> </dl>

 

 



