---
title: DisplayName (principalType) 元素
description: 指定工作排程器 UI 中顯示之主體的名稱。
ms.assetid: a8640cc9-fc16-4e73-9f0c-1ebff338fb84
keywords:
- DisplayName 元素工作排程器
topic_type:
- apiref
api_name:
- DisplayName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ff653a2b2991622b2446bcc0fc74d7063319c2bb6b45556313034a3afb42480
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356911"
---
# <a name="displayname-principaltype-element"></a>DisplayName (principalType) 元素

指定工作排程器 UI 中顯示之主體的名稱。

``` syntax
<xs:element name="DisplayName"
    type="string"
 />
```

**DisplayName** 元素是由 [**principalType**](taskschedulerschema-principaltype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                  | 衍生自                                                           | Description                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**主要**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | 指定主體的安全性認證。<br/> |



## <a name="remarks"></a>備註

針對腳本開發，主體的顯示名稱是使用 [**principal. DisplayName**](principal-displayname.md) 屬性來指定。

針對 c + + 開發，主體的顯示名稱是使用 [**IPrincipal：:D isplayname**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname) 屬性來指定。

## <a name="examples"></a>範例

下列 XML 會使用群組識別碼和顯示名稱來定義。


```XML
<Principal>
    <GroupId></GroupId>
    <DisplayName></DisplayName>
 </Principal>
```



下列 XML 會使用使用者識別碼和顯示名稱來定義主體。


```XML
<Principal>
    <UserId></UserId>
    <LogonType></LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





