---
title: logonTriggerType 複雜類型
description: 定義 LogonTrigger 元素的子項目和排序資訊。
ms.assetid: ddb1d01b-89d1-4d52-872c-4fbd90f32f4b
keywords:
- logonTriggerType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- logonTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85cbbeaa5d911b1ef9677c79980167a66cdf410c7aa63597b02b007795dfbd81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991208"
---
# <a name="logontriggertype-complex-type"></a>logonTriggerType 複雜類型

定義 [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) 元素的子項目和排序資訊。

``` syntax
<xs:complexType name="logonTriggerType">
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
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                               | 類型                                                                    | 描述                                                                                   |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**延遲**](taskschedulerschema-delay-logontriggertype-element.md)   | duration                                                                | 使用者登入和工作啟動時間之間的時間量。<br/>         |
| [**UserId**](taskschedulerschema-userid-logontriggertype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | 使用者的識別碼。 此工作會在此使用者登入電腦時啟動。<br/> |



## <a name="remarks"></a>備註

除了這裡定義的子項目之外， [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) 元素也會使用 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) 複雜類型所定義的子專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構複雜類型](task-scheduler-schema-complex-types.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





