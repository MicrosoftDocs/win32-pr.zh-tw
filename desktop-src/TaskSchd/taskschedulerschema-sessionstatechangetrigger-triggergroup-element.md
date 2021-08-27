---
title: SessionStateChangeTrigger (triggerGroup) 元素
description: 指定在終端機伺服器會話變更狀態時啟動工作的觸發程式。
ms.assetid: 38b0da3c-205f-48c5-83e6-ff7c432c02b9
keywords:
- SessionStateChangeTrigger 元素工作排程器
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d22b2f47584f437c01575ffecfb6d5c25e312b9584ba46abc9d6997e14187eaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099818"
---
# <a name="sessionstatechangetrigger-triggergroup-element"></a>SessionStateChangeTrigger (triggerGroup) 元素

指定在終端機伺服器會話變更狀態時啟動工作的觸發程式。

``` syntax
<xs:element name="SessionStateChangeTrigger"
    type="sessionStateChangeTriggerType"
 />
```

**SessionStateChangeTrigger** 元素是由 [**triggerGroup**](taskschedulerschema-triggergroup-group.md)定義。

## <a name="parent-element"></a>父元素



| 元素                                                           | 衍生自                                                         | 描述                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**觸發程序**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | 指定啟動工作的觸發程式。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                                      | 類型                                                                                    | 描述                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**延遲**](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | duration                                                                                | 指定值，這個值表示在偵測到終端機伺服器會話狀態變更時，工作開始之前的延遲時間長度。<br/> |
| [**StateChange**](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [**sessionStateChangeType**](taskschedulerschema-sessionstatechangetype-simpletype.md) | 指定會觸發工作啟動的終端機伺服器會話變更類型。<br/>                                                     |
| [**UserId**](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                 | 指定終端機伺服器會話的使用者。 當偵測到此使用者的會話狀態變更時，就會啟動工作。<br/>              |



## <a name="remarks"></a>備註

針對開發腳本，會使用 [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) 物件來指定會話狀態變更觸發程式。

針對 c + + 開發，會話狀態變更觸發程式是使用 [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) 介面指定的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





