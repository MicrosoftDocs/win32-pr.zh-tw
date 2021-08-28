---
title: HeaderFields (sendEmailType) 元素
description: 指定標頭欄位，以及在電子郵件訊息的標頭中使用的值。
ms.assetid: 6261f32e-3012-4ce7-b407-699374596333
keywords:
- HeaderFields 元素工作排程器
topic_type:
- apiref
api_name:
- HeaderFields
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2af801385c74fa26221556b713faf8db915037ef4cf7439d71a2e2d4004193d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100028"
---
# <a name="headerfields-sendemailtype-element"></a>HeaderFields (sendEmailType) 元素

指定標頭欄位，以及在電子郵件訊息的標頭中使用的值。

``` syntax
<xs:element name="HeaderFields"
    type="headerFieldsType"
 />
```

**HeaderFields** 元素是由 [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                              | 衍生自                                                           | 描述                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | 表示傳送電子郵件訊息的動作。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                         | 類型                                                                       | 描述                                                    |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------|
| [**HeaderField**](taskschedulerschema-headerfield-headerfieldstype-element.md) | [**headerFieldType**](taskschedulerschema-headerfieldtype-complextype.md) | 在電子郵件訊息中包含標頭的欄位。 <br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**IEmailAction 的 HeaderFields 屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields)。

如需腳本開發，請參閱 [**EmailAction. HeaderFields**](emailaction-headerfields.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





