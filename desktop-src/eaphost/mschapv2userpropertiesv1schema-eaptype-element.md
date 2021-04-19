---
title: 'EapType 元素 (mschapv2userpropertiesv1schema) '
description: 這個元素是 baseeapuserpropertiesv1 架構中 EapType 元素的衍生型別。 適用于 mschapv2userpropertiesv1schema。
ms.assetid: 7bd8fb5b-ceff-4d82-a979-b01229f8863a
keywords:
- EapType 元素 EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5985123a4679fe9b2524f9338b9181daa11282d
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106981414"
---
# <a name="eaptype-element-mschapv2userpropertiesv1schema"></a>EapType 元素 (mschapv2userpropertiesv1schema) 

**EapType** 元素是 [Baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)架構中 [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md)元素的衍生型別。

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element
                        minOccurs="0"
                        ref="Username"
                     />
                    <xs:element name="Password"
                        type="string"
                        minOccurs="0"
                     />
                    <xs:element name="LogonDomain"
                        type="string"
                        minOccurs="0"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>子元素



| 元素                                                                           | 類型   | Description                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**使用者**](mschapv2userpropertiesv1schema-username-element.md)               |        | 識別要驗證的使用者。 如果這個元素不存在，則會從 winlogon 取得使用者名稱。 [**Username**](mschapv2userpropertiesv1schema-username-element.md)元素是選擇性的。<br/>                                        |
| [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) | 字串 | 識別要驗證之使用者或電腦的網域。 如果此元素不存在，則會使用 winlogon 的網域。 [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md)元素是選擇性的。<br/>        |
| [**密碼**](mschapv2userpropertiesv1schema-password-eaptype-element.md)       | 字串 | 識別要驗證之使用者或電腦的密碼。 如果這個元素不存在，則會從 winlogon 取得密碼雜湊。 [**Password**](mschapv2userpropertiesv1schema-password-eaptype-element.md)元素是選擇性的。<br/> |



## <a name="remarks"></a>備註

**ProcessContents** 元素可讓架構的未來增強功能。 **ProcessContents** 元素是選擇性的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[mschapv2userpropertiesv1 架構](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





