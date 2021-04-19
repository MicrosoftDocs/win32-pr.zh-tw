---
description: 指定用來驗證使用者的密碼。
ms.assetid: 9c02413b-a4c7-4c1f-a150-e27cc125faf6
title: 密碼 (UserLogonCred) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Password
api_type:
- Schema
ms.openlocfilehash: b05e34bcbaa91aba5cbfbd14f2bc8534aa91dd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997084"
---
# <a name="password-userlogoncred-element"></a>密碼 (UserLogonCred) 元素

[**Password (UserLogonCred)**](schema-ignorepassword-userlogoncred-element.md)元素會指定用來驗證使用者的密碼。

元素是最多255個字元的字串。

這是選擇性的項目。

``` syntax
<xs:element name="Password"
    type="string"
 />
```

**Password** 元素是由 [**UserLogonCred**](schema-userlogoncred-contexttype-element.md)元素定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**UserLogonCred**](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**UserLogonCred (coNtextType)**](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 




