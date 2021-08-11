---
description: 指定網路來源所使用的控制通訊協定。
ms.assetid: 4de8b8ba-97d9-4269-a16c-1853dc02f674
title: 'MFNETSOURCE_PROTOCOL 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae15ce40e7c049552cbb0f4916f5f4ff70ef6e55746528ebe0083eee69b22a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243320"
---
# <a name="mfnetsource_protocol-property"></a>MFNETSOURCE \_ 通訊協定屬性

指定網路來源所使用的控制通訊協定。 這個屬性的值是 [**MFNETSOURCE \_ 通訊協定 \_ 類型**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) 列舉的成員。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**LONG**

VT \_ I4

**lVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ 通訊協定** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

這是唯讀的屬性。 若要取得這個屬性，請查詢 **IPropertyStore** 介面的網路來源，然後呼叫 **IPropertyStore：： GetValue**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> <dt>

[支援的通訊協定](supported-protocols.md)
</dt> </dl>

 

 




