---
title: Subject (sendEmailType) 元素
description: 包含電子郵件訊息的主旨。
ms.assetid: 2ccaa983-4dca-4e45-ba8d-2a93e23f7e8c
keywords:
- Subject 元素工作排程器
topic_type:
- apiref
api_name:
- Subject
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 15bf3c84befd9dd8f4c9c4a544fc920b7066184c6bf367c404bb14f22f573b92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611186"
---
# <a name="subject-sendemailtype-element"></a>Subject (sendEmailType) 元素

包含電子郵件訊息的主旨。

``` syntax
<xs:element name="Subject"
    type="string"
 />
```

**Subject** 元素是由 [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                              | 衍生自                                                           | 描述                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | 表示傳送電子郵件訊息的動作。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**IEmailAction 的 Subject 屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject)。

如需腳本開發，請參閱 [**EmailAction。**](emailaction-subject.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





