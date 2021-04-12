---
description: 指定語音捕獲 DSP 如何執行麥克風陣列處理。
ms.assetid: 5e04fe50-d764-4497-9999-37279e156204
title: 'MFPKEY_WMAAECMA_FEATR_MICARR_MODE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25bf8ffcae465e8abfddedb3e6d6dded683bb2bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191791"
---
# <a name="mfpkey_wmaaecma_featr_micarr_mode-property"></a>MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ MODE 屬性

指定語音捕獲 DSP 如何執行麥克風陣列處理。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

MICARRAY \_ 單一 \_ 橫樑

## <a name="applies-to"></a>套用至

-   [語音捕獲 DSP](voicecapturedmo.md)

## <a name="remarks"></a>備註

這個屬性的值是 [MIC \_ 陣列 \_ 模式](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mic_array_mode) 列舉的成員。 預設值為 MICARRAY \_ 單一 \_ 橫樑。 設定此屬性之前，您必須將 [MFPKEY \_ WMAAECMA \_ 功能 \_ 模式](mfpkey-wmaaecma-feature-modeproperty.md) 屬性設定為 VARIANT \_ TRUE。

只有在啟用麥克風陣列處理時，DSP 才會使用此屬性。

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

 

 
