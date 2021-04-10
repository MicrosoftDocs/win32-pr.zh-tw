---
title: multipleInstancesPolicyType 簡單類型
description: 定義 MultipleInstancesPolicy (settingsType) 元素的實例原則常數。
ms.assetid: 6e3f83b0-b71e-49c9-9c27-5a37f996746b
keywords:
- multipleInstancesPolicyType 簡單類型工作排程器
topic_type:
- apiref
api_name:
- multipleInstancesPolicyType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 29a3523ef16224836ada474fb32265084453479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934591"
---
# <a name="multipleinstancespolicytype-simple-type"></a>multipleInstancesPolicyType 簡單類型

定義 [**MultipleInstancesPolicy (settingsType)**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) 元素的實例原則常數。

``` syntax
<xs:simpleType name="multipleInstancesPolicyType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="Parallel"
         />
        <xs:enumeration
            value="Queue"
         />
        <xs:enumeration
            value="IgnoreNew"
         />
        <xs:enumeration
            value="StopExisting"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>列舉值

**MultipleInstancesPolicyType** 簡單類型會定義下列值。



| 值        | 描述                                                                                     |
|--------------|-------------------------------------------------------------------------------------------------|
| 平行     | 當現有的實例正在執行時，啟動新的實例。<br/>                           |
| 佇列        | 在工作的所有其他實例完成後，啟動新的工作實例。<br/>      |
| IgnoreNew    | 預設值。 如果工作的現有實例正在執行，則不會啟動新的實例。<br/> |
| StopExisting | 停止工作的現有實例，然後再啟動新的實例。<br/>                |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構簡單類型](task-scheduler-schema-complex-types.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





