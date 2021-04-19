---
description: 指定登入的使用者名稱。
ms.assetid: a312de24-2a81-4fac-9c23-4e67e171e692
title: UserName (UserLogonCred) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UserName
api_type:
- Schema
ms.openlocfilehash: 53ad1bde74f2d2a1649fa5fdee23ef70ab53b09d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991820"
---
# <a name="username-userlogoncred-element"></a>UserName (UserLogonCred) 元素

**UserName (UserLogonCred)** 元素會指定登入的使用者名稱。

元素是最多255個字元的字串。

這是選擇性的項目。

``` syntax
<xs:element name="UserName"
    type="nameType"
 />
```

**UserName** 元素是由 [**UserLogonCred**](schema-userlogoncred-contexttype-element.md)元素定義。

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

 

 




