---
title: actionGroup 群組
description: 定義工作可執行檔動作群組。
ms.assetid: a43ba021-4a40-4e2c-a57f-bd6ee17706ba
keywords:
- actionGroup 群組工作排程器
- actionGroup 工作排程器
topic_type:
- apiref
api_name:
- actionGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bcfd37187373e8bebdcc6b2af22323fd5475a6893791158b83b16c278752e420
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357173"
---
# <a name="actiongroup-group"></a>actionGroup 群組

定義工作可執行檔動作群組。

``` syntax
<xs:group name="actionGroup">
    <xs:choice>
        <xs:element name="Exec"
            type="execType"
         />
        <xs:element name="ComHandler"
            type="comHandlerType"
         />
        <xs:element name="SendEmail"
            type="sendEmailType"
         />
        <xs:element name="ShowMessage"
            type="showMessageType"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a>子元素



| 元素                                                                    | 類型                                                                       | Description                                                             |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md)   | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md)   | 表示引發處理常式的動作。<br/>                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | [**execType**](taskschedulerschema-exectype-complextype.md)               | 表示執行命令列操作的動作。<br/> |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)     | 表示傳送電子郵件訊息的動作。<br/>            |
| [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | 表示顯示訊息方塊的動作。<br/>               |



## <a name="remarks"></a>備註

讀取或寫入 XML 時，此群組所定義的元素是 [**Actions**](taskschedulerschema-actions-tasktype-element.md) 元素的子項目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





