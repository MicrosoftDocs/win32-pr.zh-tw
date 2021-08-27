---
title: RegistrationTrigger (triggerGroup) 元素
description: 指定在註冊工作時啟動工作的觸發程式。
ms.assetid: 8f028ed0-93e6-4423-be2f-9a02be99122b
keywords:
- 註冊觸發程式工作排程器、XML 元素
- RegistrationTrigger 元素工作排程器
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 548ffec6bf5982aac407905d944d029b222b741c0c03fe66645f68e771c87342
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099968"
---
# <a name="registrationtrigger-triggergroup-element"></a>RegistrationTrigger (triggerGroup) 元素

指定在註冊工作時啟動工作的觸發程式。

``` syntax
<xs:element name="RegistrationTrigger"
    type="registrationTriggerType"
 />
```

**RegistrationTrigger** 元素是由 [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                           | 衍生自                                                         | 描述                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**觸發程序**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | 指定啟動工作的觸發程式。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                                                        | 類型                                                                     | 描述                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**延遲 (registrationTriggerType)**](taskschedulerschema-delay-boottriggertype-element.md)                   | duration                                                                 | 指定在註冊工作與啟動工作之間的時間長度。<br/>                          |
| [**已啟用 (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | 指定啟用觸發程序。<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | 指定停用觸發程式的日期和時間。 觸發程式在停用之後無法啟動工作。<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | 指定觸發程式可啟動工作的最大時間量。<br/>                                   |
| [**重複 (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | 指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | 指定啟動觸發程式的日期和時間。<br/>                                                              |



## <a name="attributes"></a>屬性



| 名稱 | 類型 | 描述                           |
|------|------|---------------------------------------|
| 識別碼   | 識別碼   | 觸發程式的識別碼。<br/> |



## <a name="remarks"></a>備註

針對開發腳本，會使用 [**RegistrationTrigger**](registrationtrigger.md) 物件來指定註冊觸發程式。

針對 c + + 開發，會使用 [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) 介面指定註冊觸發程式。

上方所列的子專案是由 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) 和 [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) 複雜元素類型所定義。 這些專案必須加入如下所示的順序中。

-   [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**已啟用 (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**重複 (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [**延遲 (registrationTriggerType)**](taskschedulerschema-delay-boottriggertype-element.md)

## <a name="examples"></a>範例

如需指定開機觸發程式之工作的完整 XML 範例，請參閱 [ (xml) 的註冊觸發程式範例 ](registration-trigger-example--xml-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





