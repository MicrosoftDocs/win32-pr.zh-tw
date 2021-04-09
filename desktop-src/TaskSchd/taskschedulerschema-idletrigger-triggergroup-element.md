---
title: IdleTrigger (triggerGroup) 元素
description: 指定當電腦進入閒置狀態時啟動工作的觸發程式。
ms.assetid: c3e317b5-d1a7-46de-ace5-e066452583d3
keywords:
- 閒置觸發程式，XML 元素
- IdleTrigger 元素工作排程器
topic_type:
- apiref
api_name:
- IdleTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 221d272145670b9514cde5ffbe8b02e5ddcd6e0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024770"
---
# <a name="idletrigger-triggergroup-element"></a>IdleTrigger (triggerGroup) 元素

指定當電腦進入閒置狀態時啟動工作的觸發程式。 如需有關閒置條件的詳細資訊，請參閱工作 [閒置條件](task-idle-conditions.md)。

``` syntax
<xs:element name="IdleTrigger"
    type="idleTriggerType"
 />
```

**IdleTrigger** 元素是由 [**triggerGroup**](taskschedulerschema-triggergroup-group.md)定義。

## <a name="parent-element"></a>父元素



| 元素                                                           | 衍生自                                                         | Description                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**觸發程序**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | 指定啟動工作的觸發程式。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                                                        | 類型                                                                     | Description                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**已啟用 (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | 指定啟用觸發程序。<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | 指定停用觸發程式的日期和時間。 觸發程式在停用之後無法啟動工作。<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | 指定觸發程式可啟動工作的最大時間量。<br/>                                   |
| [**重複 (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | 指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | 指定啟動觸發程式的日期和時間。<br/>                                                              |



## <a name="attributes"></a>屬性



| 名稱 | 類型   | Description                               |
|------|--------|-------------------------------------------|
| 識別碼   | 字串 | 觸發程式的識別碼。<br/> |



## <a name="remarks"></a>備註

針對開發腳本，會使用 [**IdleTrigger**](idletrigger.md) 物件來指定閒置觸發程式。

針對 c + + 開發，會使用 [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) 介面指定閒置觸發程式。

上方所列的子專案是由 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) 複雜元素類型所定義。 這些專案必須加入如下所示的順序中。

-   [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**已啟用 (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**重複 (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a>範例

下列 XML 定義閒置觸發程式。


```XML
<IdleTrigger>
    <StartBoundary>2005-01-01T00:08:00</StartBoundary>
    <EndBounadry>2007-01-01T00:08:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
</IdleTrigger>
```



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

 

