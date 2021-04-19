---
description: 指定語音捕獲 DSP 用來處理麥克風陣列的橫樑。
ms.assetid: 9ed761da-3f1b-47e8-b71f-becc56fe8801
title: 'MFPKEY_WMAAECMA_FEATR_MICARR_BEAM 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9165eec0dee87fa5d9f6a751f41e81d0de2d9958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983531"
---
# <a name="mfpkey_wmaaecma_featr_micarr_beam-property"></a>MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ 橫樑屬性

指定語音捕獲 DSP 用來處理麥克風陣列的橫樑。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="applies-to"></a>套用至

-   [語音捕獲 DSP](voicecapturedmo.md)

## <a name="remarks"></a>備註

如果 [MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ MODE](mfpkey-wmaaecma-featr-micarr-modeproperty.md) 屬性的值為 MICARRAY EXTERN 橫樑，請設定此屬性 \_ \_ 。

如果 [**MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ 模式**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) 的值是 MICARRAY \_ 單一 \_ 橫樑，您可以讀取此屬性，以查詢 DSP 所選取的橫樑。

這個屬性可以具有下列值。 值是以度為單位的水準。



| 值 | 描述              |
|-------|--------------------------|
| 0     | -50 度。             |
| 1     | -40 度。             |
| 2     | -30 度。             |
| 3     | -20 度。             |
| 4     | -10 度。             |
| 5     | 0度 (中心的橫樑) 。 |
| 6     | 10度。              |
| 7     | 20度。              |
| 8     | 30度。              |
| 9     | 40度。              |
| 10    | 50度。              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[語音捕獲 DSP](voicecapturedmo.md)
</dt> </dl>

 

 
