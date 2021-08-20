---
title: 從 (sendEmailType) 元素
description: 包含電子郵件寄件者的電子郵件地址。
ms.assetid: b80733de-e050-4026-a2fe-f63833ec2660
keywords:
- From 元素工作排程器
topic_type:
- apiref
api_name:
- From
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14f7dda3ddbd9378d7306eadb26cd5496159ce0d7625ba598339bb949b273b30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117942776"
---
# <a name="from-sendemailtype-element"></a>從 (sendEmailType) 元素

包含電子郵件寄件者的電子郵件地址。

``` syntax
<xs:element name="From"
    type="string"
 />
```

**From** 元素是由 [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                              | 衍生自                                                           | 描述                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | 表示傳送電子郵件訊息的動作。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**IEmailAction 的 From 屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from)。

如需腳本開發，請參閱 [**EmailAction。**](emailaction-from.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





