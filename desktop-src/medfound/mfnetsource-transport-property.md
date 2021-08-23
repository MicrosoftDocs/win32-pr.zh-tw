---
description: 指定網路來源所使用的傳輸通訊協定。
ms.assetid: 7c8598ff-f408-42d0-9eee-3ef1e82f0466
title: 'MFNETSOURCE_TRANSPORT 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 933c4051cd3d008082c3b7811fcd88f8b118e51a9e864d947750813c11883b67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663468"
---
# <a name="mfnetsource_transport-property"></a>MFNETSOURCE \_ 傳輸屬性

指定網路來源所使用的傳輸通訊協定。 這個屬性的值是 [**MFNETSOURCE \_ 傳輸 \_ 類型**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) 列舉的成員。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**LONG**

VT \_ I4

**lVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ 傳輸** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

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

 

 




