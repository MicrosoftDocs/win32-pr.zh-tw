---
title: sessionStateChangeTriggerType 複雜類型
description: 定義用來建立主控台連線或中斷連線、遠端連線或中斷連線，或工作站鎖定或解除鎖定通知之工作觸發程式的元素。
ms.assetid: 0d452476-1e1f-417d-a97a-5f39d80145f2
keywords:
- sessionStateChangeTriggerType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- sessionStateChangeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8eb3ad02aef3f5bbbc078f8eafa52f3439819cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317496"
---
# <a name="sessionstatechangetriggertype-complex-type"></a>sessionStateChangeTriggerType 複雜類型

定義用來建立主控台連線或中斷連線、遠端連線或中斷連線，或工作站鎖定或解除鎖定通知之工作觸發程式的元素。

``` syntax
<xs:complexType name="sessionStateChangeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="StateChange"
                    type="sessionStateChangeType"
                    minOccurs="1"
                    maxOccurs="1"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                                      | 類型                                                                                    | Description                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**延遲**](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | duration                                                                                | 指定值，這個值表示在偵測到終端機伺服器會話狀態變更時，工作開始之前的延遲時間長度。<br/> |
| [**StateChange**](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [**sessionStateChangeType**](taskschedulerschema-sessionstatechangetype-simpletype.md) | 指定會觸發工作啟動的終端機伺服器會話變更類型。<br/>                                                     |
| [**UserId**](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                 | 指定終端機伺服器會話的使用者。 當偵測到此使用者的會話狀態變更時，就會啟動工作。<br/>              |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





