---
title: UserId (principalType) 元素
description: 指定執行與主體相關聯之工作所需的使用者識別碼。
ms.assetid: 7f3c92bf-c982-4155-9391-862f674a3665
keywords:
- UserId 元素工作排程器
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe12f76c35238251e2ecc60f848e2f7eb4eaa681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385274"
---
# <a name="userid-principaltype-element"></a>UserId (principalType) 元素

指定執行與主體相關聯之工作所需的使用者識別碼。

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
 />
```

**UserId** 元素是由 [**principalType**](taskschedulerschema-principaltype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                  | 衍生自                                                           | Description                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**主要**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | 指定主體的安全性認證。<br/> |



## <a name="remarks"></a>備註

**UserId** 元素和 [**LogonType**](taskschedulerschema-logontype-principaltype-element.md)專案會一起使用，以定義執行使用此主體之工作所需的使用者。

您無法同時指定使用者識別碼和群組識別碼。 請指定 **UserId** 或 [**GroupId**](taskschedulerschema-groupid-principaltype-element.md) 元素，但不能同時指定兩者。

針對腳本開發，使用者識別碼會使用 [**Principal. UserId**](principal-userid.md) 屬性來指定。

針對 c + + 開發，會使用 [**IPrincipal：： UserId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) 屬性指定使用者識別碼。

## <a name="examples"></a>範例

下列 XML 會使用使用者識別碼定義原則。


```XML
<Principal>
    <UserId></UserId>
    <LogonType><LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





