---
description: Windows Media MP3 解碼會將編碼為下列格式的音訊檔案解碼。
ms.assetid: 817bbc2d-b3d5-49b4-84e4-bc8dc232a8ea
title: 'Windows Media MP3 解碼 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de9bc49b3422e48f5de15678946845e21e868fe5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993233"
---
# <a name="windows-media-mp3-decoder"></a>Windows Media MP3 解碼

Windows Media MP3 解碼會將編碼為下列格式的音訊檔案解碼。

-   ISO/IEC 11172-3 (MPEG 1 音訊) 第3層
-   ISO/IEC 13818-3 (MPEG-2 音訊) 第3層，低取樣頻率延伸

## <a name="class-identifier"></a>類別識別碼

Windows Media MP3 解碼 (CLSID) 的類別識別碼是以常數 **CLSID \_ CMP3DecMediaObject** 來表示。 您可以藉由呼叫 **CoCreateInstance** 來建立 MP3 解碼器的實例。

## <a name="interfaces"></a>介面

MP3 解碼器物件會公開 **IMediaObject** 介面，讓物件可以作為 DirectX 媒體物件 (的) ，並公開 **IMFTransform** 介面，讓物件可以作為媒體基礎的轉換 (MFT) 。

Windows Media MP3 解碼器的運作方式，視您取得的介面和正在執行的 Windows 版本而定。 下表顯示 Windows Media MP3 解碼器以 SQL-DMO 或 MFT 行為的條件。



| 作業系統 | 解碼器行為                                                                                                                                                                               |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Windows Media MP3 解碼一律會以一種方式運作。                                                                                                                                           |
| Windows Vista    | Windows Media MP3 解碼器預設會以一種方式運作。 如果您在 Windows Media MP3 解碼器上取得 **IMFTransform** 介面或 **IPropertyStore** 介面，它會以 MFT 的形式運作。 |
| Windows 7        | Windows Media MP3 解碼器預設會以一種方式運作。 如果您在 Windows Media MP3 解碼器上取得 **IMFTransform** 介面，它會以 MFT 的形式運作。                                    |



 

## <a name="input-formats"></a>輸入格式

下表顯示的音訊格式標記代表 Windows Media MP3 解碼所支援的輸入類型。



| 格式化標記常數      | 格式化標記值 | 音訊格式     |
|--------------------------|------------------|------------------|
| WAVE \_ 格式 \_ MPEGLAYER3 | 0x55             | ISO MPEG 第3層 |



 

## <a name="output-formats"></a>輸出格式

下表顯示的音訊格式標記代表 Windows Media MP3 解碼所支援的輸出類型。



| 格式化標記常數       | 格式化標記值 | 音訊格式                                                                |
|---------------------------|------------------|-----------------------------------------------------------------------------|
| WAVE \_ 格式 \_ PCM         | 0x0001           | 用來作為一或 (的 PCM 格式)                                    |
| WAVE \_ 格式 \_ IEEE \_ FLOAT | 0x0003           | 作為 MFT 使用的 IEEE 浮點數 ()                                    |
| WAVE \_ 格式 \_ 可擴充  | 0xFFFE           | 使用 **WAVEFORMATEXTENSIBLE** 結構中的 PCM/IEEE 格式做為 MFT 時 ()  |



 

Windows Media MP3 解碼支援和列舉下列輸出媒體類型。

-   輸出類型，具有與輸入類型相同的取樣率和通道數目。
-   身歷聲輸入的 Mono 輸出。
-   位深度為8和16的輸出類型。
-   浮點數輸出（如果解碼器的行為是 MFT）。

Windows Media MP3 解碼支援但不會列舉下列輸出媒體類型。

-   輸出類型，具有輸入類型的一半取樣率。
-   輸出類型，具有輸入類型的第四個取樣率。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 用戶端<br/> | Windows XP、Windows Vista 或 Windows 7<br/>                                       |
| 標頭<br/> | <dl> <dt>Wmcodecdsp。h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Mp3dmod.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> <dt>

[編解碼器實行](codecimplementation.md)
</dt> </dl>

 

 




