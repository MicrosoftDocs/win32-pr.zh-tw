---
title: ShowMessage (actionGroup) 元素
description: 表示顯示訊息方塊的動作。
ms.assetid: 33c6e437-b993-4b5e-b75a-fb3fda9b24df
keywords:
- ShowMessage 元素工作排程器
topic_type:
- apiref
api_name:
- ShowMessage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 474bc44550408591616d3a8d2c6c3c69a5a0d073c90297c60b4a831627c996e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611296"
---
# <a name="showmessage-actiongroup-element"></a>ShowMessage (actionGroup) 元素

表示顯示訊息方塊的動作。

``` syntax
<xs:element name="ShowMessage"
    type="showMessageType"
 />
```

**ShowMessage** 元素是由 [**actionGroup**](taskschedulerschema-actiongroup-group.md)定義。

## <a name="parent-element"></a>父元素



| 元素                                                                    | 衍生自                                                       | 描述                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**動作 (taskType)**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | 包含工作所執行的動作。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                            | 類型           | 描述                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [**本文**](taskschedulerschema-body-showmessagetype-element.md)   | nonEmptyString | 指定要顯示在訊息方塊主體中的文字。 <br/> |
| [**標題**](taskschedulerschema-title-showmessagetype-element.md) | nonEmptyString | 指定訊息方塊的標題。 <br/>                       |



## <a name="remarks"></a>備註

針對開發腳本，會使用 [**ShowMessageAction**](showmessageaction.md) 物件來指定訊息方塊動作。

針對 c + + 開發，會使用 [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction) 介面指定訊息方塊動作。

**Windows 8 和 Windows Server 2012：** 已移除這個元素。 您可以使用 IExecAction 搭配 Windows 腳本 [**MsgBox 函數**](/previous-versions/sfw6660x(v=vs.80))，在使用者會話中顯示訊息。

## <a name="examples"></a>範例

如需使用訊息方塊動作之工作的 XML 完整範例，請參閱 [ (xml) 的訊息方塊範例 ](/previous-versions//aa381917(v=vs.85))。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |
| 用戶端支援結束<br/>    | Windows 7<br/>                                 |
| 伺服器支援結束<br/>    | Windows Server 2008 R2<br/>                    |



 

