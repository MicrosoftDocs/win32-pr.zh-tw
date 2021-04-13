---
title: TaskListType 複雜類型
description: 定義用來識別應用程式元件的工作清單。
ms.assetid: 41a46967-7c5b-4555-9f65-bd9582c0c492
keywords:
- TaskListType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- TaskListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ad427743242ada8901e904fc4e03620ccc72f405
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383806"
---
# <a name="tasklisttype-complex-type"></a>TaskListType 複雜類型

定義用來識別應用程式元件的工作清單。

``` syntax
<xs:complexType name="TaskListType">
    <xs:sequence>
        <xs:element name="task"
            type="TaskType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                       | 類型                                                         | Description                                                       |
|---------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [**任務**](eventmanifestschema-task-tasklisttype-element.md) | [**TaskType**](eventmanifestschema-tasktype-complextype.md) | 定義應用程式的元件或子元件。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





