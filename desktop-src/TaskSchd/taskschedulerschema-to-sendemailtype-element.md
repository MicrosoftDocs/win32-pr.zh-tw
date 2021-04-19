---
title: " (sendEmailType) 元素"
description: 包含要將電子郵件傳送至其中的電子郵件地址。
ms.assetid: bf3aa878-967b-4ebd-9397-a2a499686a9f
keywords:
- To 元素工作排程器
topic_type:
- apiref
api_name:
- To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9e0643220915ecb1c8f2cd1fe842e0dc3f21d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106995576"
---
# <a name="to-sendemailtype-element"></a> (sendEmailType) 元素

包含要將電子郵件傳送至其中的電子郵件地址。

``` syntax
<xs:element name="To"
    type="string"
 />
```

**To** 元素是由 [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                              | 衍生自                                                           | Description                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | 表示傳送電子郵件訊息的動作。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**IEmailAction 的屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to)。

如需腳本開發，請參閱 [**EmailAction.To**](emailaction-to.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





