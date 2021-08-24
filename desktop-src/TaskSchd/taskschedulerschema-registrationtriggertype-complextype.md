---
title: registrationTriggerType 複雜類型
description: 定義 RegistrationTrigger 元素的子項目和排序資訊。
ms.assetid: 3663c015-67cf-4775-a1a6-4429cce93b96
keywords:
- registrationTriggerType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- registrationTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2dab91ecc0eed065a4ce3eea9d64bebae2e10560a43ab57308ea68e82dc17dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772278"
---
# <a name="registrationtriggertype-complex-type"></a>registrationTriggerType 複雜類型

定義 [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) 元素的子項目和排序資訊。

``` syntax
<xs:complexType name="registrationTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
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



| 元素                                                                    | 類型     | 描述                                                                                               |
|----------------------------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------|
| [**延遲**](taskschedulerschema-delay-registrationtriggertype-element.md) | duration | 指定在註冊工作與啟動工作之間的時間長度。<br/> |



## <a name="remarks"></a>備註

除了這裡定義的子項目之外， [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) 元素也會使用 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) 複雜類型所定義的子專案。

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

 

 





