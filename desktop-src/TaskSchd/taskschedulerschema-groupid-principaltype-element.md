---
title: GroupId (principalType) 元素
description: 指定執行與主體相關聯之工作所需之使用者群組的識別碼。
ms.assetid: 1e576c31-79a9-42d4-b497-74412e464d60
keywords:
- GroupId 元素工作排程器
topic_type:
- apiref
api_name:
- GroupId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4376e7037c228ebf2d2ffdc193cc34e7f92647220251cd82f09b0b65c7f9a81c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131837"
---
# <a name="groupid-principaltype-element"></a>GroupId (principalType) 元素

指定執行與主體相關聯之工作所需之使用者群組的識別碼。

``` syntax
<xs:element name="GroupId"
    type="nonEmptyString"
 />
```

**GroupId** 元素是由 [**principalType**](taskschedulerschema-principaltype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                  | 衍生自                                                           | 描述                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**主要**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | 指定主體的安全性認證。<br/> |



## <a name="remarks"></a>備註

您無法同時指定群組識別碼和使用者識別碼。 請指定 [**UserId**](taskschedulerschema-userid-principaltype-element.md) 或 **GroupId** 元素，但不能同時指定兩者。

針對腳本開發，主體的群組識別碼是使用 [**principal. GroupId**](principal-groupid.md) 屬性來指定。

針對 c + + 開發，會使用 [**IPrincipal：： GroupId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) 屬性指定主體的群組識別碼。

## <a name="examples"></a>範例

如需使用此專案之工作的 XML 完整範例，請參閱登入 [觸發程式範例 (xml) ](logon-trigger-example--xml-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





