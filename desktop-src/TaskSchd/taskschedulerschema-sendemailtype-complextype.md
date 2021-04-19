---
title: sendEmailType 複雜類型
description: 定義用來指定工作執行時將傳送電子郵件的動作類型。 此類型會定義用來建立電子郵件訊息模型的所有元素。
ms.assetid: e384971f-e7e4-4206-9d15-9555dfcbac2f
keywords:
- sendEmailType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- sendEmailType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 959e0b8f03223eb23b7a7bec69ba9b2aeea66447
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965331"
---
# <a name="sendemailtype-complex-type"></a>sendEmailType 複雜類型

定義用來指定工作執行時將傳送電子郵件的動作類型。 此類型會定義用來建立電子郵件訊息模型的所有元素。

``` syntax
<xs:complexType name="sendEmailType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Server"
                    type="nonEmptyString"
                 />
                <xs:element name="Subject"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="To"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Cc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Bcc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="ReplyTo"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="From"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="HeaderFields"
                    type="headerFieldsType"
                    minOccurs="0"
                 />
                <xs:element name="Body"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Attachments"
                    type="attachmentsType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                        | 類型                                                                         | Description                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**附件**](taskschedulerschema-attachments-sendemailtype-element.md)   | [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md)   | 指定電子郵件訊息中的附件清單。<br/>                                 |
| [**密件副本**](taskschedulerschema-bcc-sendemailtype-element.md)                   | **string**                                                                   | 指定電子郵件訊息的 [密件副本] 行上使用的電子郵件地址。<br/>               |
| [**主體**](taskschedulerschema-body-sendemailtype-element.md)                 | **string**                                                                   | 指定電子郵件訊息主體中的文字。<br/>                                  |
| [**Cc**](taskschedulerschema-cc-sendemailtype-element.md)                     | **string**                                                                   | 指定電子郵件訊息之 Cc 行上使用的電子郵件地址。<br/>                |
| [**寄件者**](taskschedulerschema-from-sendemailtype-element.md)                 | **string**                                                                   | 指定寄件者的電子郵件地址。<br/>                                            |
| [**HeaderFields**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) | 指定標頭欄位，以及在電子郵件訊息的標頭中使用的值。<br/> |
| [**ReplyTo**](taskschedulerschema-replyto-sendemailtype-element.md)           | **string**                                                                   | 指定電子郵件訊息中要回復的電子郵件地址。<br/>               |
| [**伺服器**](taskschedulerschema-server-sendemailtype-element.md)             | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)      | 指定用來傳送電子郵件訊息的電子郵件伺服器。 <br/>                           |
| [**主體**](taskschedulerschema-subject-sendemailtype-element.md)           | **string**                                                                   | 指定電子郵件訊息的主旨。<br/>                                           |
| [**自**](taskschedulerschema-to-sendemailtype-element.md)                     | **string**                                                                   | 指定電子郵件將傳送至其中的電子郵件地址。<br/>                        |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





