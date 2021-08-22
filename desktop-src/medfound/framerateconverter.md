---
description: 變更影片串流的畫面播放速率。
ms.assetid: a66b9c52-a015-41d2-b27a-3ce6a4d95be9
title: '畫面播放速率轉換器 DSP (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca4a728f37caa43ee99a0d293d5113e9c26cfb1dcfe51f399482fb614283737
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600488"
---
# <a name="frame-rate-converter-dsp"></a>畫面播放速率轉換器 DSP

變更影片串流的畫面播放速率。

## <a name="clsid"></a>CLSID

CLSID \_ CFrameRateConvertDmo

## <a name="interfaces"></a>介面

-   **IMediaObject**
-   **IMFTransform**
-   **IPropertyStore**

## <a name="formats"></a>格式

-   ARGB 32
-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   AYUV
-   IYUV
-   UYVY
-   Y211
-   Y411
-   Y41P
-   YUY2
-   YUYV
-   YV12
-   YVYU

## <a name="properties"></a>屬性

-   [MFPKEY \_ 約定 \_ INPUTFRAMERATE](mfpkey-conv-inputframerate.md)
-   [MFPKEY \_ 約定 \_ OUTPUTFRAMERATE](mfpkey-conv-outputframerate.md)

## <a name="remarks"></a>備註

這個 DSP 會藉由重複或卸載框架來變更畫面播放速率。

根據預設，DSP 會取得媒體類型的畫面播放速率。 （選擇性）您可以藉由設定 MFPKEY 的 [設定 \_ ] \_ INPUTFRAMERATE 和 [MFPKEY] \_ \_ OUTPUTFRAMERATE 屬性來指定畫面播放速率。 這些值會覆寫媒體類型中指定的畫面播放速率。 但是，如果您在媒體基礎管線內使用這個 DSP，則不應設定這些屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Mfvdsp.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數位訊號處理器](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




