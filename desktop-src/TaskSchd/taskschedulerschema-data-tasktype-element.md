---
title: 資料 (taskType) 元素
description: 定義與工作相關聯的加法資料，但工作排程器服務未使用。
ms.assetid: 296cd33d-5f82-4de7-84a7-e791619ad0b5
keywords:
- 工作排程器的資料元素
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3afff1cbd81ede49568afdc9e516d87a57ff9e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685739"
---
# <a name="data-tasktype-element"></a>資料 (taskType) 元素

定義與工作相關聯的加法資料，但工作排程器服務未使用。

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

**資料** 元素是由 [**taskType**](taskschedulerschema-tasktype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                          | 衍生自                                                 | Description                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Task**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | 定義工作排程器服務所執行的工作。<br/> |



## <a name="remarks"></a>備註

作為這類資料的範例，效能記錄檔及警示服務會使用這個屬性做為與工作相關聯之效能計數器查詢的儲存體容器。

針對 c + + 開發，會使用 [**ITaskDefinition 的資料屬性**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_data)來指定工作的資料。

在腳本開發中，會使用 [**TaskDefinition**](taskdefinition-data.md) 屬性來指定工作的資料。

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

 

 





