---
title: 密件副本 (sendEmailType) 元素
description: 包含電子郵件訊息的密件副本行上使用的電子郵件地址。
ms.assetid: c80407d0-3b3f-4efe-91de-7a3a7abc996f
keywords:
- 密件副本元素工作排程器
topic_type:
- apiref
api_name:
- Bcc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1409d50a0317758534724b9e2c3a9796c4dd0cb40e666f58fc65ca0771da9762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659038"
---
# <a name="bcc-sendemailtype-element"></a>密件副本 (sendEmailType) 元素

包含電子郵件訊息的密件副本行上使用的電子郵件地址。

``` syntax
<xs:element name="Bcc"
    type="string"
 />
```

**密件副本** 元素是由 [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                              | 衍生自                                                           | Description                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | 表示傳送電子郵件訊息的動作。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**IEmailAction 的 [密件副本] 屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc)。

如需腳本開發，請參閱 [**EmailAction。**](emailaction-bcc.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





