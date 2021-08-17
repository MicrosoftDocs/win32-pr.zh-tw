---
description: 指定是否啟用網路來源中的 HTTP 通訊協定。
ms.assetid: dcc4db5c-0274-4a8a-89a4-66cda62e1520
title: 'MFNETSOURCE_ENABLE_HTTP 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09d033594e223b8219f168e86d82ef02012bfafd4be9d758a438d042356735f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874764"
---
# <a name="mfnetsource_enable_http-property"></a>MFNETSOURCE \_ ENABLE \_ HTTP 屬性

指定是否啟用網路來源中的 HTTP 通訊協定。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

布林 (**LONG**) 

VT \_ I4

**lVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ ENABLE \_ HTTP** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

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
</dt> <dt>

[支援的通訊協定](supported-protocols.md)
</dt> </dl>

 

 




