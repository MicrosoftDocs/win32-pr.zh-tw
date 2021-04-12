---
description: 指定語音捕獲 DSP 是否執行中央裁剪。
ms.assetid: 6830cadd-fa8d-41e1-ac11-a6c8f2795941
title: 'MFPKEY_WMAAECMA_FEATR_CENTER_CLIP 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0936ddfe9e34664e55a20efea35a3c06dd6990e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191793"
---
# <a name="mfpkey_wmaaecma_featr_center_clip-property"></a>MFPKEY \_ WMAAECMA \_ FEATR \_ CENTER \_ 剪輯屬性

指定語音捕獲 DSP 是否執行中央裁剪。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ BOOL

## <a name="default-value"></a>預設值

VARIANT \_ TRUE

## <a name="applies-to"></a>套用至

-   [語音捕獲 DSP](voicecapturedmo.md)

## <a name="remarks"></a>備註

置中裁剪是一種程式，可移除在 AEC 處理之後保留的小型 echo 殘差，在單一交談的情況下 (語音只會在一行) 的一端發生。

這個屬性可以具有下列值。



| 值          | 描述              |
|----------------|--------------------------|
| VARIANT \_ FALSE | 停用中心裁剪。 |
| VARIANT \_ TRUE  | 啟用中央裁剪。  |



 

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

 

 
