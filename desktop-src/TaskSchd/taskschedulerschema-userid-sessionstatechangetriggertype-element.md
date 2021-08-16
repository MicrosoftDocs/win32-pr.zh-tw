---
title: UserId (sessionStateChangeTriggerType) 元素
description: 包含終端機伺服器會話的使用者。 當偵測到此使用者的會話狀態變更時，就會啟動工作。
ms.assetid: 7605f444-b2c9-4bba-a035-f1307c01184f
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
ms.openlocfilehash: d6f6ddaf196f83d727e4641df6e59375033eb60c076451d70866d9d227ca457d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355573"
---
# <a name="userid-sessionstatechangetriggertype-element"></a>UserId (sessionStateChangeTriggerType) 元素

包含終端機伺服器會話的使用者。 當偵測到此使用者的會話狀態變更時，就會啟動工作。

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

**UserId** 元素是由 [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                       | 衍生自                                                                                           | Description                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| **SessionStateChangeTrigger** | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | 指定在終端機伺服器會話變更狀態時啟動工作的觸發程式。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**ISessionStateChangeTrigger 的 UserId 屬性**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_userid)。

如需腳本開發，請參閱 [**SessionStateChangeTrigger。 UserId**](sessionstatechangetrigger-userid.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





