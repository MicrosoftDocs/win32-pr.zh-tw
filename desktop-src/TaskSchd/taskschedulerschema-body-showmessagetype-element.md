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
ms.openlocfilehash: 3486601153f8e9dd7dac14f83800dae00a79a9f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465809"
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



| 元素                                                                                  | 衍生自                                                               | Description                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [**ShowMessage (actionGroup)**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | 表示顯示訊息方塊的動作。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**IShowMessageAction 的 MessageBody 屬性**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody)。

如需腳本開發，請參閱 [**ShowMessageAction. MessageBody**](showmessageaction-messagebody.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





