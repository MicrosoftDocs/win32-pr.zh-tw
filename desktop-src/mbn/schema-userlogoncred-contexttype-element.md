---
description: 包含連接的登入認證。
ms.assetid: 79c1d277-6284-4adb-a1bd-6c207b37e33e
title: UserLogonCred (coNtextType) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UserLogonCred
api_type:
- Schema
ms.openlocfilehash: d3dc0c22d6242ee894545bd61f839574afd06141
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113448"
---
# <a name="userlogoncred-contexttype-element"></a>UserLogonCred (coNtextType) 元素

**UserLogonCred (coNtextType)** 元素包含連接的登入認證。

這個元素可以有下列子項目。

-   [**使用者**](schema-username-userlogoncred-element.md)
-   [**密碼**](schema-password-userlogoncred-element.md)
-   [**IgnorePassword**](schema-ignorepassword-userlogoncred-element.md)

此元素最多可有一次。

這是選擇性的項目。

``` syntax
<xs:element name="UserLogonCred">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="UserName"
                type="nameType"
             />
            <xs:element name="IgnorePassword"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="Password"
                type="string"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

**UserLogonCred** 元素是由 [**coNtextType**](schema-contexttype-complextype.md)複雜型別定義。

## <a name="child-elements"></a>子元素



| 元素                                                               | 類型                                           | Description                                                 |
|-----------------------------------------------------------------------|------------------------------------------------|-------------------------------------------------------------|
| [**IgnorePassword**](schema-ignorepassword-userlogoncred-element.md) | boolean                                        | 如何在升級設定檔時處理密碼。<br/> |
| [**密碼**](schema-password-userlogoncred-element.md)             | 字串                                         | 使用者密碼。<br/>                                   |
| [**使用者**](schema-username-userlogoncred-element.md)             | [**nameType**](schema-nametype-simpletype.md) | 使用者名稱。<br/>                                       |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**coNtextType**](schema-contexttype-complextype.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**MBNProfile) 內容 (**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




