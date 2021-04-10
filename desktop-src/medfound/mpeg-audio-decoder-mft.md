---
description: Microsoft MPEG 音訊解碼器是一種同步媒體基礎轉換 (MFT) ，可使用媒體基礎 (MF) 管線來解碼 MPEG 音訊基本資料流程格式。
ms.assetid: 29A0491D-CA0D-4909-96F0-5640D5EE77F9
title: MPEG 音訊解碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98106ce4610c7c89a5e6212c225fd8eca3e4526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943731"
---
# <a name="mpeg-audio-decoder"></a>MPEG 音訊解碼器

Microsoft MPEG 音訊解碼器是一種同步 [媒體基礎轉換](media-foundation-transforms.md) (MFT) ，可使用媒體基礎 (MF) 管線來解碼 MPEG 音訊基本資料流程格式。

此解碼器支援下列 MPEG 基本資料流程格式。

-   MPEG-2 音訊層 I 和 II (ISO/IEC 11172-3) 。 2. MPEG-2 與舊版相容，第 I 和第二層 (ISO

-   MPEG-2 與舊版相容，第 I 和第二層 (ISO/IEC 13818-3) 、mono 和身歷聲

## <a name="class-identifier"></a>類別識別碼

MPEG 音訊解碼器 (CLSID) 的類別識別碼是 **clsid \_ MSMPEGAudDecMFT**，定義于標頭檔 wmcodecdsp 中。

## <a name="input-media-types"></a>輸入媒體類型

MPEG 音訊解碼器支援下列輸入媒體類型屬性。



| 屬性                                                                               | 值                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md)                               | **MFMediaType \_ 音訊**                                                                                                                                                                                                                                                |
| [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ MPEG**                                                                                                                                                                                                                                               |
| [**MF \_ MT \_ 音訊 \_ 數目 \_ 通道**](mf-mt-audio-num-channels-attribute.md)              |  (選擇性的) 通常是1代表 mono 或2，最多可以有6個通道。<br/>                                                                                                                                                                                |
| [**MF \_ MT \_ 音訊 \_ 通道 \_ 遮罩**](mf-mt-audio-channel-mask-attribute.md)              |  (選擇性的) 通常為 mono 或0x3 （身歷聲），但也可以是與最多6個通道相關聯的任一個通道遮罩 (3/2/1、3/2、3/1、2/2、2/1) 。 如果有的話，通道遮罩必須與指定的通道輸入數目一致。<br/> |
| [**\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_**](mf-mt-audio-samples-per-second-attribute.md) |  (選擇性) 下列其中一項：16000、22050、24000、32000、44100、48000。 如果有指定，輸入取樣率必須是有效的 MPEG 取樣率之一。<br/>                                                                                             |



 

## <a name="output-media-types"></a>輸出媒體類型

MPEG 音訊解碼器會以下列順序支援最多四個輸出媒體子類型。

<dl> 1. 身歷聲、浮點數。  
2. 身歷聲、16位 PCM。  
3. Mono、浮點數 (只有在輸入為 mono 或雙 mono) 時才。  
4. 只有當輸入為 mono 或雙 mono) 時，才會 (Mono、16位 PCM。  
</dl>

此解碼器一律支援身歷聲輸出，並且會列舉為第一個輸出媒體類型。

此解碼器支援下列輸出媒體類型屬性。



| 屬性                                                                           | 值                                                                      |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MF \_ MT \_ 主要 \_ 類型](mf-mt-major-type-attribute.md)                               | **MFMediaType \_ 音訊**                                                     |
| [MF \_ MT \_ 子類型](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ PCM** 或 **MFAudioFormat \_ Float**                  |
| [\_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊位數](mf-mt-audio-bits-per-sample-attribute.md)       | 16或32                                                                   |
| [MF \_ MT \_ 音訊 \_ 數目 \_ 通道](mf-mt-audio-num-channels-attribute.md)              | 1 或 2                                                                     |
| [MF \_ MT \_ 音訊 \_ 通道 \_ 遮罩](mf-mt-audio-channel-mask-attribute.md)              | 適用于 mono 的0x4 或0x3 （身歷聲）                                             |
| [\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_](mf-mt-audio-samples-per-second-attribute.md) | 下列其中一項：16000、22050、24000、32000、44100、48000。<br/> |



 

## <a name="transform-attributes"></a>轉換屬性

MPEG 音訊解碼器會實行 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 方法。 應用程式可以使用這個方法來取得或設定下列屬性。



| 屬性                                                                               | 描述                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CODECAPI \_ AVDecAudioDualMono**](../directshow/avdecaudiodualmono-property.md)                   | 指定要解碼的雙聲道音訊是否為雙 mono。 唯讀。 由 MFT 設定。 如需詳細資訊，請參閱 [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono)。                                                                                                                               |
| [**CODECAPI \_ AVDecAudioDualMonoReproMode**](../directshow/avdecaudiodualmonorepromode-property.md) | 指定解碼器如何重現雙重 mono 音訊。 預設值為 **eAVDecAudioDualMonoReproMode \_ LEFT \_ MONO**。<br/> 讀取/寫入。 應用程式可以設定此屬性來變更預設行為。 如需詳細資訊，請參閱 [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono)。<br/> |
| [**CODECAPI \_ AVEncCommonMeanBitRate**](../directshow/avenccommonmeanbitrate-property.md)           | 指定壓縮的資料流程位元速率。 唯讀。 由 MFT 設定。                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> </dl>

 

 
