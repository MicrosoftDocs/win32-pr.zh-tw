---
description: 設定語音捕獲 DSP 的處理模式。
ms.assetid: 479b3525-5beb-4c6b-b1ad-8fa72c0d0fd0
title: 'MFPKEY_WMAAECMA_SYSTEM_MODE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfca745b83c8a73a2eb4c17c8a2206f90255088c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974210"
---
# <a name="mfpkey_wmaaecma_system_mode-property"></a>MFPKEY \_ WMAAECMA \_ 系統 \_ 模式屬性

設定語音捕獲 DSP 的處理模式。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="applies-to"></a>套用至

-   [語音捕獲 DSP](voicecapturedmo.md)

## <a name="remarks"></a>備註

這個屬性的值是 [AEC \_ 系統 \_ 模式](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode) 列舉的成員。

屬性必須是下列其中一個值。



| 值 | 描述                                 |
|-------|---------------------------------------------|
| 0     | 音訊 echo 取消 (AEC 只) 模式     |
| 2     | 麥克風陣列處理 (MAP) 模式 |
| 4     | AEC 和對應模式                            |
| 5     | AEC 或對應模式皆非                    |



 

您必須先設定這個屬性，才能使用語音捕獲 DSP。 設定這個屬性之後，您可以使用 DSP 的預設設定，或設定其他屬性。

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

 

 
