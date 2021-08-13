---
title: 安全性 (SystemPropertiesType) 元素
description: 識別記錄事件的使用者。
ms.assetid: f421b0c3-96ea-440c-a3b2-0ddd8f327eec
keywords:
- 安全性元素 EventLog
topic_type:
- apiref
api_name:
- Security
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 20aef5465b8790bdba92c50181c0550ca5989c29d66fd53b9ec7ed0f760a2129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118588284"
---
# <a name="security-systempropertiestype-element"></a>安全性 (SystemPropertiesType) 元素

識別記錄事件的使用者。

``` syntax
<xs:element name="Security">
    <xs:complexType>
        <xs:attribute name="UserID"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

**安全性** 元素是由 [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)複雜型別定義。

## <a name="attributes"></a>屬性



| 名稱   | 類型   | 描述                                                          |
|--------|--------|----------------------------------------------------------------------|
| UserID | 字串 | 以字串形式 (SID) 使用者的安全識別碼。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**父元素**
</dt> <dt>

[**系統 (的系統事件)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





