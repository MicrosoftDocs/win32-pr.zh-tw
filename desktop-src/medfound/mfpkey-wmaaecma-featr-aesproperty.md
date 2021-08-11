---
description: 指定「語音捕獲」 DSP 對剩餘信號的 (AES) 執行聲場 DSP 抑制的次數。
ms.assetid: 409b40f8-38eb-49f7-be30-348ab5cdd33a
title: 'MFPKEY_WMAAECMA_FEATR_AES 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e842bc3064b431437d8bbdfab06c0081ecdb49a8c38288ba4adb78648363c71a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242035"
---
# <a name="mfpkey_wmaaecma_featr_aes-property"></a>MFPKEY \_ WMAAECMA \_ FEATR \_ AES 屬性

指定「語音捕獲」 DSP 對剩餘信號的 (AES) 執行聲場 DSP 抑制的次數。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

0

## <a name="applies-to"></a>套用至

-   [語音捕獲 DSP](voicecapturedmo.md)

## <a name="remarks"></a>備註

語音捕獲 DSP 可在回應取消之後，對剩餘的信號執行 AES。 這個屬性的值可以是0、1或2。 預設值為 0。 設定此屬性之前，您必須將 [MFPKEY \_ WMAAECMA \_ 功能 \_ 模式](mfpkey-wmaaecma-feature-modeproperty.md) 屬性設定為 VARIANT \_ TRUE。

只有在啟用 AEC 處理時，DSP 才會使用這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[語音捕獲 DSP](voicecapturedmo.md)
</dt> </dl>

 

 
