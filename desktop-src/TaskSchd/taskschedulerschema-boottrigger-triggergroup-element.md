---
title: BootTrigger (triggerGroup) 元素
description: 指定啟動系統時啟動工作的觸發程式。
ms.assetid: c6833547-0daf-4e8a-b8c5-b422827b1d96
keywords:
- 開機觸發程式工作排程器、XML 元素
- BootTrigger 元素工作排程器
topic_type:
- apiref
api_name:
- BootTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb6ccf590893e19340662fd4c47e4aa68047b29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317356"
---
# <a name="boottrigger-triggergroup-element"></a>BootTrigger (triggerGroup) 元素

指定啟動系統時啟動工作的觸發程式。

``` syntax
<xs:element name="BootTrigger"
    type="bootTriggerType"
 />
```

**BootTrigger** 元素是由 [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                           | 衍生自                                                         | Description                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**觸發程序**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | 指定啟動工作的觸發程式。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                                                        | 類型                                                                     | Description                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**延遲 (bootTriggerType)**](taskschedulerschema-delay-boottriggertype-element.md)                           | duration                                                                 | 指定啟動系統與啟動工作之間的時間長度。<br/>                            |
| [**已啟用 (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | 指定啟用觸發程序。<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | 指定停用觸發程式的日期和時間。 觸發程式在停用之後無法啟動工作。<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | 指定觸發程式可啟動工作的最大時間量。<br/>                                   |
| [**重複 (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | 指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | 指定啟動觸發程式的日期和時間。<br/>                                                              |



## <a name="attributes"></a>屬性



| 名稱 | 類型       | Description                               |
|------|------------|-------------------------------------------|
| 識別碼   | **string** | 觸發程式的識別碼。<br/> |



## <a name="remarks"></a>備註

針對開發腳本， [**BootTrigger**](boottrigger.md) 物件會定義開機觸發程式。

針對 c + + 開發，開機觸發程式是由 [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) 物件所定義。

## <a name="examples"></a>範例

如需指定開機觸發程式之工作的完整 XML 範例，請參閱 [ (xml) 的開機觸發程式範例 ](boot-trigger-example--xml-.md)。

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

 

 





