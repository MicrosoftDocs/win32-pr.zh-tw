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
ms.openlocfilehash: 5fc57ddf5deee52ff9b118a8267eec4069108030
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384097"
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



| 元素                                                                              | 衍生自                                                           | Description                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | 表示傳送電子郵件訊息的動作。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**IEmailAction 的伺服器屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server)。

如需腳本開發，請參閱 [**EmailAction。**](emailaction-server.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





