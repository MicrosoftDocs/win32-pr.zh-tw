---
title: 許可權 (requiredPrivilegesType) 元素
description: 指定工作的許可權，以執行各種系統相關作業，例如關閉系統、載入設備磁碟機，或變更系統時間。
ms.assetid: d5585d1c-e121-4770-a13e-108158bc703e
keywords:
- 許可權元素工作排程器
topic_type:
- apiref
api_name:
- Privilege
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55e9263ae9d02bb384bfbe56101ea82f98c2e076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466421"
---
# <a name="privilege-requiredprivilegestype-element"></a>許可權 (requiredPrivilegesType) 元素

指定工作的許可權，以執行各種系統相關作業，例如關閉系統、載入設備磁碟機，或變更系統時間。

``` syntax
<xs:element name="Privilege"
    type="privilegeType"
    maxOccurs="64"
    minOccurs="1"
 />
```

**許可權** 元素是由 [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                             | 衍生自                                                                             | Description                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**RequiredPrivileges**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) | 包含工作排程器用來執行工作的設定。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，這項資訊是透過 [**IPrincipal2：： RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) 屬性來存取。

## <a name="examples"></a>範例

下列 XML 會定義設定專案，指定工作執行各種系統相關作業的許可權，例如關閉系統、載入設備磁碟機，或變更系統時間。


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

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





