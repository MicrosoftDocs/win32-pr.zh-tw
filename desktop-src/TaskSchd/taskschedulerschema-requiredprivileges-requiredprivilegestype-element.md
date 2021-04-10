---
title: RequiredPrivileges (requiredPrivilegesType) 元素
description: 指定工作所需的許可權。
ms.assetid: 7b615af8-76f9-498c-aa2d-7da02d64992f
keywords:
- RequiredPrivileges 元素工作排程器
topic_type:
- apiref
api_name:
- RequiredPrivileges
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70476cff01113dcf612f890e8a6aa5538d0ca38e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106355"
---
# <a name="requiredprivileges-requiredprivilegestype-element"></a>RequiredPrivileges (requiredPrivilegesType) 元素

指定工作所需的許可權。

``` syntax
<xs:element name="RequiredPrivileges"
    type="requiredPrivilegesType"
    minOccurs="0"
 />
```

**RequiredPrivileges** 元素是由 [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                  | 衍生自                                                           | Description                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal (principalType)**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | 指定主體的安全性認證。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，這項資訊是透過 [**IPrincipal2：： RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) 屬性來存取。

## <a name="examples"></a>範例

下列 XML 定義使用群組識別碼和必要的許可權。


```XML
<Principal>
    <RequiredPrivileges>
        <Privilege>SeCreateTokenPrivilege</Privilege>
    </RequiredPrivileges>
</Principal>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





