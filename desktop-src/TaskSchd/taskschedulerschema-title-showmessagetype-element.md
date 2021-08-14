---
title: 標題 (showMessageType) 元素
description: 包含訊息方塊的標題。
ms.assetid: 089d2043-41ed-4050-b794-af24ab7ac8b9
keywords:
- Title 元素工作排程器
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e5fe72b791a963e78d49ace14f7edec1210dc3bf23a5f7cee9550e6f6db53e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355675"
---
# <a name="title-showmessagetype-element"></a>標題 (showMessageType) 元素

包含訊息方塊的標題。

``` syntax
<xs:element name="Title"
    type="nonEmptyString"
 />
```

**Title** 元素是由 [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                  | 衍生自                                                               | Description                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [**ShowMessage (actionGroup)**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | 表示顯示訊息方塊的動作。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**IShowMessageAction 的 Title 屬性**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title)。

如需腳本開發，請參閱 [**ShowMessageAction。**](showmessageaction-title.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





