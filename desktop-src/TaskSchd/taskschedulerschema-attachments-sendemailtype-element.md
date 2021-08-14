---
title: 附件 (sendEmailType) 元素
description: 包含電子郵件訊息中的附件清單。
ms.assetid: 5ae22481-af70-42eb-a964-e63d800be17d
keywords:
- 附件元素工作排程器
topic_type:
- apiref
api_name:
- Attachments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8aa87679c6d6db725c26deee817fe04acacca85e39d3a8f75c04cba9680ea846
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132063"
---
# <a name="attachments-sendemailtype-element"></a>附件 (sendEmailType) 元素

包含電子郵件訊息中的附件清單。

``` syntax
<xs:element name="Attachments"
    type="attachmentsType"
 />
```

**附件** 元素是由 [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                              | 衍生自                                                           | Description                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | 表示傳送電子郵件訊息的動作。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                          | 類型                                                                    | Description                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**檔案**](taskschedulerschema-file-attachmentstype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | 指定以電子郵件訊息中的附件形式傳送之檔案的路徑。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**IEmailAction 的附件屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments)。

如需腳本開發，請參閱 [**EmailAction。**](emailaction-attachments.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





