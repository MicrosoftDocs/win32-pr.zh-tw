---
title: ShowMessageType) 元素的內文 (主體
description: 包含要顯示在訊息方塊主體中的文字。
ms.assetid: 69ea872a-7ca1-4464-9380-b35f74c9cb8e
keywords:
- Body 元素工作排程器
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6b1fbacd450c05b8ff71521dacfa6e95c7efc70fc7d8909ca66f3390bf22295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010868"
---
# <a name="body-showmessagetype-element"></a>ShowMessageType) 元素的內文 (主體

包含要顯示在訊息方塊主體中的文字。

``` syntax
<xs:element name="Body"
    type="nonEmptyString"
 />
```

**Body** 專案是由 [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                  | 衍生自                                                               | 描述                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [**ShowMessage (actionGroup)**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | 表示顯示訊息方塊的動作。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**IShowMessageAction 的 MessageBody 屬性**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody)。

如需腳本開發，請參閱 [**ShowMessageAction. MessageBody**](showmessageaction-messagebody.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





