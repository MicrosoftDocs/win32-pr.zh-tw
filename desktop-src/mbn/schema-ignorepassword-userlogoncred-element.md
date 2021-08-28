---
description: 指定如何在升級設定檔時處理密碼。
ms.assetid: 74d7ceb1-d778-4a12-907b-0528d9ff45be
title: IgnorePassword (UserLogonCred) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnorePassword
api_type:
- Schema
ms.openlocfilehash: 683fafb763e3f8613afa1b8dca99020856d67a03fdb44e993adf032ce166ceab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975167"
---
# <a name="ignorepassword-userlogoncred-element"></a>IgnorePassword (UserLogonCred) 元素

**IgnorePassword (UserLogonCred)** 元素會指定如何在升級設定檔時處理密碼。

如果設定為 **TRUE** 且在更新作業時存在具有相同名稱的設定檔，則會採用該設定檔中的密碼，並將其儲存在新的設定檔中。

這是選擇性的項目。

``` syntax
<xs:element name="IgnorePassword"
    type="boolean"
 />
```

**IgnorePassword** 元素是由 [**UserLogonCred**](schema-userlogoncred-contexttype-element.md)元素定義。

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

 

 




