---
description: 指定語音捕獲 DSP 是否執行雜訊填滿。
ms.assetid: 8bb64686-8f02-4e0d-a664-aeee1744fc8e
title: 'MFPKEY_WMAAECMA_FEATR_NOISE_FILL 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0c0af2b47767a7798d9b583ac55ad5112ddf1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989282"
---
# <a name="mfpkey_wmaaecma_featr_noise_fill-property"></a>MFPKEY \_ WMAAECMA \_ FEATR \_ 雜訊 \_ 填滿屬性

指定語音捕獲 DSP 是否執行雜訊填滿。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ BOOL

## <a name="default-value"></a>預設值

VARIANT \_ TRUE

## <a name="applies-to"></a>套用至

-   [語音捕獲 DSP](voicecapturedmo.md)

## <a name="remarks"></a>備註

「雜訊填滿」會將少量的雜訊新增至「中心」裁剪已移除剩餘回應的部分信號。 這可為使用者提供更好的體驗，而不會在信號中留下無訊息的間隔。

這個屬性可以具有下列值。



| 值          | 描述            |
|----------------|------------------------|
| VARIANT \_ TRUE  | 啟用雜訊填滿。  |
| VARIANT \_ FALSE | 停用雜訊填滿。 |



 

這個屬性的預設值為 VARIANT \_ TRUE (enabled) 。 設定此屬性之前，您必須將 [MFPKEY \_ WMAAECMA \_ 功能 \_ 模式](mfpkey-wmaaecma-feature-modeproperty.md) 屬性設定為 VARIANT \_ TRUE。

只有在啟用 AEC 處理時，DSP 才會使用這個屬性。

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

 

 
