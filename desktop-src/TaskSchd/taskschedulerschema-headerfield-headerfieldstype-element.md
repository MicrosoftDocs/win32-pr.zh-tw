---
title: HeaderField (headerFieldsType) 元素
description: 在電子郵件訊息中包含標頭的欄位。
ms.assetid: ec6fc593-8798-4dd0-b589-48657b7cdeb1
keywords:
- HeaderField 元素工作排程器
topic_type:
- apiref
api_name:
- HeaderField
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f7ac79a16bb0464f6e81d90eba38384a3c2b483
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106970463"
---
# <a name="headerfield-headerfieldstype-element"></a>HeaderField (headerFieldsType) 元素

在電子郵件訊息中包含標頭的欄位。

``` syntax
<xs:element name="HeaderField"
    type="headerFieldType"
 />
```

**HeaderField** 元素是由 [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                        | 衍生自                                                                 | Description                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**HeaderFields**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) | 指定標頭欄位，以及在電子郵件訊息的標頭中使用的值。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                            | 類型                                                                    | Description                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Name**](taskschedulerschema-name-headerfieldtype-element.md)   | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | 在電子郵件訊息中指定標頭欄位的名稱。<br/> |
| [**值**](taskschedulerschema-value-headerfieldtype-element.md) | **string**                                                              | 指定電子郵件訊息中標頭欄位的值。<br/>  |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**IEmailAction 的 HeaderFields 屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields)。

如需腳本開發，請參閱 [**EmailAction. HeaderFields**](emailaction-headerfields.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





