---
title: SendEmailType) 元素的內文 (主體
description: 包含電子郵件訊息主體中的文字。
ms.assetid: fac6ddd5-6f73-427b-b213-ab946512c87a
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
ms.openlocfilehash: 4659f2ff03f69b6bba40d9cd16e9b68515cc8889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966512"
---
# <a name="body-sendemailtype-element"></a>SendEmailType) 元素的內文 (主體

包含電子郵件訊息主體中的文字。

``` syntax
<xs:element name="Body"
    type="string"
 />
```

**Body** 專案是由 [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                              | 衍生自                                                           | Description                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | 表示傳送電子郵件訊息的動作。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**IEmailAction 的 Body 屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body)。

如需腳本開發，請參閱 [**EmailAction。**](emailaction-body.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





