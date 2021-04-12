---
title: UserId (logonTriggerType) 元素
description: 使用者的識別碼。 此工作會在此使用者登入電腦時啟動。
ms.assetid: 52568899-e351-4ee1-b613-d7c42d7b983d
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
ms.openlocfilehash: 69d6534122b4b5e11a18a64ffa9bbb5e29e2a68a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509439"
---
# <a name="userid-logontriggertype-element"></a>UserId (logonTriggerType) 元素

使用者的識別碼。 此工作會在此使用者登入電腦時啟動。

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

**UserId** 元素是由 [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                       | 衍生自                                                                 | Description                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) | 指定當使用者登入時啟動工作的觸發程式。<br/> |



## <a name="remarks"></a>備註

針對腳本開發，登入觸發程式的使用者識別碼是使用 [**LogonTrigger**](logontrigger-userid.md) 屬性來指定。

針對 c + + 開發，使用 [**ILogonTrigger：： UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) 屬性指定登入觸發程式的使用者識別碼。

## <a name="examples"></a>範例

如需指定登入觸發程式之工作的完整 XML 範例，請參閱 [登入觸發程式範例 (xml) ](logon-trigger-example--xml-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





