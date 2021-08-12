---
title: EapHostUserCredentials 元素
description: 包含 EapMethod 專案，以及認證或 CredentialsBlob 元素。
ms.assetid: 6d0d41c8-560c-4d42-83c9-865053aef47a
keywords:
- EapHostUserCredentials 元素 EAPHost
topic_type:
- apiref
api_name:
- EapHostUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a18922ef19bd828067ddb0153aa7c6369ecfeebd0446f5a6481f91fa64ca21b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274418"
---
# <a name="eaphostusercredentials-element"></a>EapHostUserCredentials 元素

**EapHostUserCredentials** 元素包含 [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md)元素，以及 [**認證**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md)或 [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md)元素。

``` syntax
<xs:element name="EapHostUserCredentials">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Credentials"
                    type="BaseEapMethodUserCredentials"
                 />
                <xs:element name="CredentialsBlob"
                    type="hexBinary"
                 />
            </xs:choice>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>子元素



| 元素                                                                                                | 類型                                                                                                                | 描述                                                                                      |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**認證**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md)         | [**BaseEapMethodUserCredentials**](baseeapmethodusercredentialsschema-baseeapmethodusercredentials-complextype.md) | 當方法設定為 XML 文字格式，而非二進位 BLOB 時，會使用。<br/>   |
| [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) | hexBinary                                                                                                           | 當方法設定為二進位 BLOB 而非 XML 文字格式時，就會使用。<br/> |
| [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md)             | [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)                                                  | 識別所參考的方法。 <br/>                                             |



## <a name="remarks"></a>備註

[**認證**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md)和 [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md)元素不能同時使用。

有其他命名空間的延伸點。

**ProcessContents** 元素可讓架構的未來增強功能。 **ProcessContents** 元素是選擇性的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[eaphostusercredentials 架構](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





