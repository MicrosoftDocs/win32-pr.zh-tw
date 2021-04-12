---
description: 在色彩格式之間轉換影片串流。
ms.assetid: 1c15dc2b-0e69-4d16-af02-8056a1eb2c5c
title: '色彩轉換器 DSP (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a8418d6eeeffcf83a38452b19f18a6baa60bcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468640"
---
# <a name="color-converter-dsp"></a>色彩轉換器 DSP

在色彩格式之間轉換影片串流。

## <a name="clsid"></a>CLSID

CLSID \_ CColorConvertDMO

## <a name="interfaces"></a>介面

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [IWMColorConvProps](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcolorconvprops)

## <a name="input-formats"></a>輸入格式

-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   RGB 8
-   AYUV
-   I420
-   IYUV
-   NV11
-   NV12
-   UYVY
-   V216
-   V410
-   Y41P
-   Y41T
-   Y42T
-   YUY2
-   YV12
-   YVU9
-   YVYU

## <a name="output-formats"></a>輸出格式

-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   RGB 8
-   AYUV
-   I420
-   IYUV
-   NV11
-   NV12
-   UYVY
-   V216
-   V410
-   YUY2
-   YV12
-   YVYU

## <a name="properties"></a>屬性

-   [MFPKEY \_ COLORCONV \_ SRCLEFT](mfpkey-colorconv-srcleft.md)
-   [MFPKEY \_ COLORCONV \_ SRCTOP](mfpkey-colorconv-srctop.md)
-   [MFPKEY \_ COLORCONV \_ DSTLEFT](mfpkey-colorconv-dstleft.md)
-   [MFPKEY \_ COLORCONV \_ DSTTOP](mfpkey-colorconv-dsttop.md)
-   [MFPKEY \_ COLORCONV \_ 寬度](mfpkey-colorconv-width.md)
-   [MFPKEY \_ COLORCONV \_ HEIGHT](mfpkey-colorconv-height.md)
-   [MFPKEY \_ COLORCONV \_ 模式](mfpkey-colorconv-mode.md)

## <a name="remarks"></a>備註

色彩轉換器 DSP 會實作為 COM 物件，此物件可做為 DirectXMedia 物件 (的) 或媒體基礎轉換 (MFT) 。 此物件具有單一類別識別碼 (CLSID) ，不論它是否可作為一或一個 MFT。 如需有關 DSP 作為一或是 MFT 之時機的詳細資訊，請參閱 [數位訊號處理器](windowsmediadigitalsignalprocessors.md)。

針對 RGB 媒體子類型 (Guid) 的全域唯一識別碼，會根據 DSP 是以 SQL-DMO 或 MFT 的方式而有所不同。 非 RGB 媒體子類型的 Guid 是相同的，不論 DSP 是以 SQL-DMO 或 MFT 作為的。 如需表示媒體子類型之 Guid 的詳細資訊，請參閱 [影片子類型 guid](video-subtype-guids.md)。

根據預設，這個 DSP 會將整個來源影像複製到輸出緩衝區。 （選擇性）您可以指定來源和目的地矩形。 DSP 會複製來源矩形所定義之來源影像的部分，並將它寫入輸出緩衝區的目的地矩形。 DSP 不會執行任何調整;來源和目的地矩形的大小必須相同。 來源和目的地矩形不能超過影片框架的界限。

除了 [**MFPKEY \_ COLORCONV \_ 模式**](mfpkey-colorconv-mode.md) 以外的所有屬性都必須在群組中設定。 如果您設定任何這些屬性，則必須設定其他屬性。 否則，來源和目的地矩形可能無效，在這種情況下， [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 和 [**IMediaObject：:P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) 方法都會傳回 **E \_ INVALIDARG**。

色彩轉換器不支援輸入格式和輸出格式的每個組合。 通常，您應該設定您知道的媒體格式，也就是輸入或輸出，然後在相反的資料流程上列舉可用的格式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Colorcnv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數位訊號處理器](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
