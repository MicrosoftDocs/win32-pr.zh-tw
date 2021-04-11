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
ms.openlocfilehash: f262b8f5d74018a4622f915def85df5e16108cdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104351"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





