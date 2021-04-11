---
title: 資料 (comHandlerType) 元素
description: 指定與處理常式相關聯的其他資料。
ms.assetid: 352cb92b-54bb-4bb0-8a43-123c88c80962
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
ms.openlocfilehash: d009005dc2bb889c8bd9e34e84d853665310330a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934830"
---
# <a name="data-comhandlertype-element"></a>資料 (comHandlerType) 元素

指定與處理常式相關聯的其他資料。

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

**資料** 元素是由 [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                  | 衍生自                                                             | Description                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) | 指定引發處理常式的動作。<br/> |



## <a name="remarks"></a>備註

應用程式會使用 [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)介面的 [**data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data)屬性來定義處理常式資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





