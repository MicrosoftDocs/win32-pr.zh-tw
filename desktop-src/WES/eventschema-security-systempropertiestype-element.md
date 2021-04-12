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
ms.openlocfilehash: b793193d7afdfde5fd515252a024432ed45ff8b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105797"
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



| 名稱   | 類型   | Description                                                          |
|--------|--------|----------------------------------------------------------------------|
| UserID | 字串 | 以字串形式 (SID) 使用者的安全識別碼。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**父元素**
</dt> <dt>

[**系統 (的系統事件)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





