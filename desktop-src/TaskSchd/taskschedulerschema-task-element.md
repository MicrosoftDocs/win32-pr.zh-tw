---
title: Task 項目
description: 定義工作排程器服務所執行的工作。
ms.assetid: 103a332a-8620-4e0c-81b5-4782d85fc391
keywords:
- Task 元素工作排程器
topic_type:
- apiref
api_name:
- Task
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38bac482f8546028d21db913e31dc4152f19f599
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843256"
---
# <a name="task-element"></a>Task 項目

定義工作排程器服務所執行的工作。

``` syntax
<xs:element name="Task"
    type="taskType"
>
    <xs:key name="PrincipalKey">
        <xs:selector
            xpath="td:Principals/td:Principal"
         />
        <xs:field
            xpath="@id"
         />
    </xs:key>
    <xs:keyref name="ContextKeyRef">
        <xs:selector
            xpath="td:Actions"
         />
        <xs:field
            xpath="@Context"
         />
    </xs:keyref>
    <xs:unique name="UniqueId">
        <xs:selector
            xpath="td:Principals/td:Principal|td:Triggers/td:BootTrigger|td:Triggers/td:RegistrationTrigger|td:Triggers/td:IdleTrigger|td:Triggers/td:TimeTrigger|td:Triggers/td:EventTrigger|td:Triggers/td:LogonTrigger|td:Triggers/td:SessionStateChangeTrigger|td:Triggers/td:CalendarTrigger|td:Actions/td:Exec|td:Actions/td:ComHandler|td:Actions/td:SendEmail"
         />
        <xs:field
            xpath="@id"
         />
    </xs:unique>
</xs:element>
```

## <a name="child-elements"></a>子元素



| 元素                                                                           | 類型                                                                                 | Description                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**行動**](taskschedulerschema-actions-tasktype-element.md)                   | [**actionsType**](taskschedulerschema-actionstype-complextype.md)                   | 指定工作執行的動作。<br/>                                                                             |
| [**資料**](taskschedulerschema-data-tasktype-element.md)                         | [**dataType**](taskschedulerschema-datatype-complextype.md)                         | 指定與工作相關聯的額外資料，但工作排程器服務未使用。<br/>         |
| [**Principals**](taskschedulerschema-principals-tasktype-element.md)             | [**principalsType**](taskschedulerschema-principalstype-complextype.md)             | 指定可以用來執行工作的安全性內容。<br/>                                                        |
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | 指定工作的系統管理資訊，例如工作的作者以及註冊工作的日期。<br/> |
| [**設定**](taskschedulerschema-settings-tasktype-element.md)                 | [**settingsType**](taskschedulerschema-settingstype-complextype.md)                 | 指定工作排程器用來執行工作的設定。<br/>                                                 |
| [**觸發程序**](taskschedulerschema-triggers-tasktype-element.md)                 | [**triggersType**](taskschedulerschema-triggerstype-complextype.md)                 | 指定啟動工作的觸發程式。<br/>                                                                              |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)。

如需腳本開發，請參閱 [**TaskDefinition**](taskdefinition.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





