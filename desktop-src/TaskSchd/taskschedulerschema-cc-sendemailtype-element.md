---
title: Cc (sendEmailType) 元素
description: 包含電子郵件訊息之 Cc 行上使用的電子郵件地址。
ms.assetid: cb8bc5b3-c352-43e3-bf28-d2090a519c7f
keywords:
- Cc 元素工作排程器
topic_type:
- apiref
api_name:
- Cc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bc49f2d7eebc2fbb1b5818fee2efa0e54f579a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466025"
---
# <a name="cc-sendemailtype-element"></a>Cc (sendEmailType) 元素

包含電子郵件訊息之 Cc 行上使用的電子郵件地址。

``` syntax
<xs:element name="Cc"
    type="string"
 />
```

**Cc** 元素是由 [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                              | 衍生自                                                           | Description                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | 表示傳送電子郵件訊息的動作。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**IEmailAction 的 Cc 屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc)。

如需腳本開發，請參閱 [**EmailAction.Cc**](emailaction-cc.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





