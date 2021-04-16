---
description: 範例屬性
ms.assetid: 64aead5a-61c4-4e83-a556-af33e0aa82be
title: 範例屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1329946c36b1b7454deb76a25247985d9dcfdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512556"
---
# <a name="sample-attributes"></a>範例屬性

下列屬性適用于 [媒體範例](media-samples.md)。 若要從媒體範例取得屬性，請使用 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面。



| 屬性                                                                                                      | 描述                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md)                                                    | 指定媒體範例是否包含3D 影片框架。                                                                                                                                                                                        |
| [MFSampleExtension \_ 3DVideo \_ SampleFormat](mfsampleextension-3dvideo-sampleformat.md)                         | 指定3D 影片框架如何儲存在媒體範例中。                                                                                                                                                                                        |
| [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md)                    | 指定交錯式影片框架的欄位支配。                                                                                                                                                                                       |
| [MFSampleExtension \_ CameraExtrinsics](mfsampleextension-cameraextrinsics.md)                                  | 範例的攝影機 extrinsics。                                                                                                                                                                                                              |
| [MFSampleExtension \_ CaptureMetadata](mfsampleextension-capturemetadata.md)                                    | 與捕捉管線相關之所有中繼資料的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 存放區。                                                                                                                                             |
| [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md)                                | 指出影片範例是否為主要畫面格。                                                                                                                                                                                                   |
| [MFSampleExtension \_ 內容 \_ KeyID](mfsampleextension-content-keyid.md)                                       | 設定範例的金鑰識別碼。                                                                                                                                                                                                                    |
| [**MFSampleExtension \_ DerivedFromTopField**](mfsampleextension-derivedfromtopfield-attribute.md)              | 指定 deinterlaced 的影片框架是否衍生自上方欄位或下方欄位。                                                                                                                                                  |
| [MFSampleExtension \_ DeviceTimestamp](mfsampleextension-devicetimestamp.md)                                    | 設備磁碟機的時間戳記。                                                                                                                                                                                                             |
| [**MFSampleExtension \_ 中斷**](mfsampleextension-discontinuity-attribute.md)                          | 指定媒體範例是否為數據流中間距之後的第一個範例。                                                                                                                                                                    |
| [MFSampleExtension \_ 加密 \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md)               | 指定以範例為基礎的模式加密的加密位元組區塊大小。                                                                                                                                                                       |
| [MFSampleExtension \_ 加密 \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md)           | 指定加密範例的保護設定。                                                                                                                                                                                             |
| [MFSampleExtension \_ 加密 \_ SampleID](mfsampleextension-encryption-sampleid.md)                           | 指定加密範例的識別碼。                                                                                                                                                                                                           |
| [MFSampleExtension \_ 加密 \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md)                 | 針對以範例為基礎的模式加密，指定明確 (未加密的) 位元組區塊大小。                                                                                                                                                           |
| [MFSampleExtension \_ 加密 \_ SubSampleMappingSplit](mfsampleextension-encryption-subsamplemappingsplit.md) | 設定範例的子樣本對應，指出範例資料中的明確和加密的位元組。                                                                                                                                            |
| [MFSampleExtension \_ FrameCorruption](mfsampleextension-framecorruption.md)                                    | 指定影片框架是否已損毀。                                                                                                                                                                                                      |
| [MFSampleExtension \_ ForwardedDecodeUnits](mfsampleextension-forwardeddecodeunits.md)                          | 取得型別為 [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) 的物件，其中包含 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 物件，其中包含網路抽象層單位 (NALUs) 和增補增強資訊 (SEI 由解碼器轉送的) 單位。 |
| [MFSampleExtension \_ ForwardedDecodeUnitType](mfsampleextension-forwardeddecodeunittype.md)                    | 指定連接到 [MFSampleExtension \_ ForwardedDecodeUnits](mfsampleextension-forwardeddecodeunits.md)集合中之 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)的單位類型（NALU 或 SEI）。                                                    |
| [**交錯式 MFSampleExtension \_**](mfsampleextension-interlaced-attribute.md)                                | 指出影片框架是否為交錯式或漸進式。                                                                                                                                                                                      |
| [MFSampleExtension \_ LongTermReferenceFrameInfo](mfsampleextension-longtermreferenceframeinfo.md)              | 指定長期參考 (LTR) 框架資訊，並且在輸出範例上傳回。                                                                                                                                                               |
| [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md)                      | 這個屬性會傳回 Y 平面中所有宏區塊 (MAD) 的平均絕對差異。                                                                                                                                                  |
| [**MFSampleExtension \_ PacketCrossOffsets**](mfsampleextension-packetcrossoffsets-attribute.md)                | 指定框架的承載界限。 這適用于加密的範例。                                                                                                                                                                   |
| [MFSampleExtension \_ PhotoThumbnail](mfsampleextension-photothumbnail.md)                                      | 包含 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)的相片縮圖。                                                                                                                                                                                  |
| [MFSampleExtension \_ PhotoThumbnailMediaType](mfsampleextension-photothumbnailmediatype.md)                    | 包含描述 [MFSampleExtension \_ PhotoThumbnail](mfsampleextension-photothumbnail.md)屬性中所包含之影像格式類型的 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 。                                                      |
| [MFSampleExtension \_ PinholeCameraIntrinsics](mfsampleextension-pinholecameraintrinsics.md)                    | 範例的 pinhole 攝影機內建函式。                                                                                                                                                                                                      |
| [**MFSampleExtension \_ RepeatFirstField**](mfsampleextension-repeatfirstfield-attribute.md)                    | 指定是否要重複交錯框架中的第一個欄位。                                                                                                                                                                                |
| [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md)                                          | 指定感興趣區域的界限，指出需要不同品質的框架區域。                                                                                                                            |
| [**MFSampleExtension \_ SingleField**](mfsampleextension-singlefield-attribute.md)                              | 指定影片範例是否包含單一欄位或兩個交錯欄位                                                                                                                                                                 |
| [MFSampleExtension \_ TargetGlobalLuminance](mfsampleextension-targetgloballuminance.md)                        | Nits 中的值，指定相關聯影片框架的目標全域背光亮度。                                                                                                                                           |
| [**MFSampleExtension \_ Token**](mfsampleextension-token-attribute.md)                                          | 包含提供給 [**IMFMediaStream：： RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) 方法之權杖的指標。                                                                                                             |
| [MFSampleExtension \_ VideoEncodePictureType](mfsampleextension-videoencodepicturetype.md)                      | 指定感興趣區域的界限，指出需要不同品質的框架區域。                                                                                                                            |
| [MFSampleExtension \_ VideoEncodeQP](mfsampleextension-videoencodeqp.md)                                        | 指定用來編碼影片範例的 (QP) 的量化參數。                                                                                                                                                                  |



 

並非每個媒體範例都包含此處所列的每個屬性。 在某些情況下，屬性只適用于特定類型的資料。 例如，某些屬性只適用于影片範例，不應該出現在音訊範例上。 在其他情況下，如果未設定屬性，屬性就會套用預設值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> <dt>

[媒體範例](media-samples.md)
</dt> </dl>

 

 



