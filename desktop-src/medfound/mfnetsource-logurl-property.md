---
description: 網路來源將傳送記錄資訊的 Url 清單。
ms.assetid: 772c5b57-273d-4289-9229-ef7a199c6473
title: 'MFNETSOURCE_LOGURL 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b855475e17264682ffc49a391894bb6acc6a721712b8ce6e4c01d98b1d216d48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874632"
---
# <a name="mfnetsource_logurl-property"></a>MFNETSOURCE \_ LOGURL 屬性

網路來源將傳送記錄資訊的 Url 清單。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

寬字元字串的陣列 (**CALPWSTR**) 

VT \_ 向量 \| VT \_ LPWSTR

**calpwstr**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ LOGURL** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

應用程式可以使用這個屬性來設定網路來源。 若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

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
</dt> </dl>

 

 




