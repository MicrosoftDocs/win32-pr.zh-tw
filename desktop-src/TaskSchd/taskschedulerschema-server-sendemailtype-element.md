---
title: 伺服器 (sendEmailType) 元素
description: 包含用來傳送電子郵件訊息的電子郵件伺服器。
ms.assetid: 4c6084d1-70c5-4d8b-8fcb-ab4cd8aab441
keywords:
- Server 元素工作排程器
topic_type:
- apiref
api_name:
- Server
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6052ebb5e648c040c321a311a6ba18313244ab20340d5a7f6c4185e3d35f5df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002246"
---
# <a name="server-sendemailtype-element"></a>伺服器 (sendEmailType) 元素

包含用來傳送電子郵件訊息的電子郵件伺服器。

``` syntax
<xs:element name="Server"
    type="nonEmptyString"
 />
```

**Server** 元素是由 [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                              | 衍生自                                                           | 描述                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | 表示傳送電子郵件訊息的動作。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**IEmailAction 的伺服器屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server)。

如需腳本開發，請參閱 [**EmailAction。**](emailaction-server.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





