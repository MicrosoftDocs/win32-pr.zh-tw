---
title: ComHandler (actionGroup) 元素
description: 指定引發處理常式的動作。
ms.assetid: 18f16873-3879-4a3b-b8f2-17cc84647e25
keywords:
- ComHandler 元素工作排程器
topic_type:
- apiref
api_name:
- ComHandler
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2269464efb09e8c513ab2bdebb24744a6b32a671
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934831"
---
# <a name="comhandler-actiongroup-element"></a>ComHandler (actionGroup) 元素

指定引發處理常式的動作。

``` syntax
<xs:element name="ComHandler"
    type="comHandlerType"
 />
```

**ComHandler** 元素是由 [**actionGroup**](taskschedulerschema-actiongroup-group.md)定義。

## <a name="parent-element"></a>父元素



| 元素                                                         | 衍生自                                                       | Description                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**行動**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | 包含工作所執行的動作。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                               | 類型                                                         | Description                                                       |
|-----------------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [**ClassId**](taskschedulerschema-classid-comhandlertype-element.md) | [**guidType**](taskschedulerschema-guidtype-simpletype.md)  | 指定處理常式類別的識別碼。<br/>         |
| [**資料**](taskschedulerschema-data-comhandlertype-element.md)       | [**dataType**](taskschedulerschema-datatype-complextype.md) | 指定與處理常式相關聯的其他資料。<br/> |



## <a name="remarks"></a>備註

應用程式會使用 [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) 介面來定義 COM 處理常式動作。

### <a name="attributes"></a>屬性

下列屬性是由 [**actionBaseType**](taskschedulerschema-actionbasetype-complextype.md) 複雜型別定義。

-   識別碼：工作所執行之動作的識別碼。

## <a name="examples"></a>範例

下列 XML 定義 COM 處理常式動作。


```XML
<Actions>
    <ComHandler>
        <ClassId></ClassId>
        <Data></Data>
    </ComHandler>
</Actions>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





