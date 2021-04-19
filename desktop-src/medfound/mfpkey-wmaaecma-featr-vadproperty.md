---
description: 指定語音捕獲 DSP 執行的語音活動偵測類型。
ms.assetid: 59c8e348-8c08-4cf8-9c72-8d0f4fabc473
title: 'MFPKEY_WMAAECMA_FEATR_VAD 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e41b8ad80d909a0285b266587d02c09c08d794
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997104"
---
# <a name="mfpkey_wmaaecma_featr_vad-property"></a>MFPKEY \_ WMAAECMA \_ FEATR \_ VAD 屬性

指定語音捕獲 DSP 執行的語音活動偵測類型。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

0

## <a name="applies-to"></a>套用至

-   [語音捕獲 DSP](voicecapturedmo.md)

## <a name="remarks"></a>備註

這個屬性的值是 [AEC \_ VAD \_ 模式](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) 列舉的成員。 語音活動偵測的輸出是從0到3的數位，為每個音訊畫面格計算。 DSP 會在每個音訊框架中的前兩個音訊樣本的最低位編碼結果。 值的意義取決於指定的模式。

下列程式碼示範如何從音訊資料中解壓縮結果。 在此範例中， *pOutput* 是輸出資料中音訊框架開頭的指標。


```
int AecDecodeVAD(short *pOutput)
{
    int iVAD = (*pOutput) & 0x01;
    pOutput++;
    iVAD |= (*pOutput << 1) & 0x02;
    return iVAD;
}
```



這個屬性的預設值為 0 (停用) 。 設定此屬性之前，您必須將 [MFPKEY \_ WMAAECMA \_ 功能 \_ 模式](mfpkey-wmaaecma-feature-modeproperty.md) 屬性設定為 VARIANT \_ TRUE。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
