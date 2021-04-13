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
ms.openlocfilehash: 9d108f1c31b8253046ccdbf09312df4f54c7335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508851"
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



| 元素                                                                              | 衍生自                                                           | Description                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | 表示傳送電子郵件訊息的動作。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                         | 類型                                                                       | Description                                                    |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------|
| [**HeaderField**](taskschedulerschema-headerfield-headerfieldstype-element.md) | [**headerFieldType**](taskschedulerschema-headerfieldtype-complextype.md) | 在電子郵件訊息中包含標頭的欄位。 <br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**IEmailAction 的 HeaderFields 屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields)。

如需腳本開發，請參閱 [**EmailAction. HeaderFields**](emailaction-headerfields.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





