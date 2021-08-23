---
description: 調整影片資料流程的色彩特性。
ms.assetid: 738c1f0c-8417-4b12-a7f1-9bbf3c7e9dd3
title: '色彩控制轉換 DSP (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c51321a8ffd725306f570619b9bcbe70fe7160e784358ce265157145b40347e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606208"
---
# <a name="color-control-transform-dsp"></a>色彩控制轉換 DSP

調整影片資料流程的色彩特性。

## <a name="clsid"></a>CLSID

CLSID \_ CColorControlDmo

## <a name="interfaces"></a>介面

-   **IMediaObject**
-   **IMFTransform**
-   **IPropertyStore**

## <a name="formats"></a>格式

-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   AYUV
-   UYVY
-   YUY2
-   YV12

## <a name="properties"></a>屬性

-   [MFPKEY \_ 色彩 \_ 亮度](mfpkey-color-brightness.md)
-   [MFPKEY \_ 色彩 \_ 對比](mfpkey-color-contrast.md)
-   [MFPKEY \_ 色彩 \_ 色調](mfpkey-color-hue.md)
-   [MFPKEY \_ 色彩 \_ 飽和度](mfpkey-color-saturation.md)

## <a name="remarks"></a>備註

此 DSP 會修改影片資料流程的內容。 針對播放，您可以使用 **IMFVideoProcessor** 介面（可控制圖形配接器的影片處理），更有效率地達成類似效果。

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

 

 




