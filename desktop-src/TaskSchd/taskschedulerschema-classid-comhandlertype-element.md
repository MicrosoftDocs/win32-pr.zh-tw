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
ms.openlocfilehash: c89af2f39ae6a4a529fe7a728cf4b821245aa034
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466989"
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



| 元素                                                                  | 衍生自                                                             | Description                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) | 指定引發處理常式的動作。<br/> |



## <a name="remarks"></a>備註

應用程式會使用 [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)介面的 [**ClassId**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid)屬性來定義類別識別碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





