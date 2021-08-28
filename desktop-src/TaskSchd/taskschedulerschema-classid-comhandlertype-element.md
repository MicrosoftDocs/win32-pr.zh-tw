---
title: " (comHandlerType) 元素的 ClassId"
description: 指定處理常式類別的識別碼。
ms.assetid: 38ebcc39-85f2-4f61-8cb6-556c242a63d9
keywords:
- 工作排程器的 ClassId 元素
topic_type:
- apiref
api_name:
- ClassId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d2729226320758f93140e1d4073286fba02f446d34f9eb9c36caf931b7190e4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119402118"
---
# <a name="classid-comhandlertype-element"></a> (comHandlerType) 元素的 ClassId

指定處理常式類別的識別碼。

``` syntax
<xs:element name="ClassId"
    type="guidType"
 />
```

**ClassId** 元素是由 [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                  | 衍生自                                                             | 描述                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) | 指定引發處理常式的動作。<br/> |



## <a name="remarks"></a>備註

應用程式會使用 [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)介面的 [**ClassId**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid)屬性來定義類別識別碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





