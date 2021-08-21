---
title: TaskType) 元素 (動作
description: 包含工作所執行的動作。
ms.assetid: 0a48fbd6-8a6f-4bad-9b28-0631dce15748
keywords:
- 動作 (taskType) 元素工作排程器
- 動作工作排程器、XML
- Actions 元素工作排程器
topic_type:
- apiref
api_name:
- Actions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79fb5fe36b6fcff3622e0d12f0571e7f06c5f00d1ae930abc2bca805315f7dd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357096"
---
# <a name="actions-tasktype-element"></a>TaskType) 元素 (動作

包含工作所執行的動作。

``` syntax
<xs:element name="Actions"
    type="actionsType"
 />
```

**Actions** 元素是由 [**taskType**](taskschedulerschema-tasktype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                          | 衍生自                                                 | 描述                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**工作**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | 描述工作排程器服務所執行的工作。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                    | 類型                                                                       | 描述                                                            |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md)   | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md)   | 指定引發處理常式的動作。<br/>                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | [**execType**](taskschedulerschema-exectype-complextype.md)               | 指定執行命令列操作的動作。<br/> |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)     | 指定傳送電子郵件訊息的動作。<br/>            |
| [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | 指定顯示訊息方塊的動作。<br/>               |



## <a name="attributes"></a>屬性



| 名稱    | 類型 | 描述                                                                                          |
|---------|------|------------------------------------------------------------------------------------------------------|
| Context |      | 做為工作動作之安全性內容之使用者的主體識別碼。<br/> |



## <a name="remarks"></a>備註

先前所列的子項目 (最大的 32) 是由 [**actionGroup**](taskschedulerschema-actiongroup-group.md) 群組定義。 您可以依任何順序加入這些元素。

針對 c + + 開發，工作的動作會定義在 [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) 介面中。

針對腳本開發，工作的動作會定義在 [**actioncollection 動作**](actioncollection.md) 物件中。

## <a name="examples"></a>範例

如需包含單一執行動作之工作的 XML 詳細資訊和完整範例，請參閱 [時間觸發程式範例 (xml) ](time-trigger-example--xml-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**taskType**](taskschedulerschema-tasktype-complextype.md)
</dt> <dt>

[**actionGroup**](taskschedulerschema-actiongroup-group.md)
</dt> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





