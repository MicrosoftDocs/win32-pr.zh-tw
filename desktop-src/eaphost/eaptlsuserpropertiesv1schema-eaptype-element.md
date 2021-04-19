---
title: 'EapType 元素 (eaptlsuserpropertiesv1schema) '
description: 這個元素是 baseeapuserpropertiesv1 架構中 EapType 元素的衍生型別。 適用于 eaptlsuserpropertiesv1schema。
ms.assetid: c9117803-dbf0-498d-8f86-f44ac2e6b2dc
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
ms.openlocfilehash: 53e5c1404c70542f3604b94aa6cae9c8fc39fd21
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106999566"
---
# <a name="eaptype-element-eaptlsuserpropertiesv1schema"></a>EapType 元素 (eaptlsuserpropertiesv1schema) 

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
                        ref="Username"
                     />
                    <xs:element name="UserCert"
                        type="hexBinary"
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



| 元素                                                                   | 類型      | Description                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**使用者**](eaptlsuserpropertiesv1schema-username-element.md)         |           | 捕捉要在 EAP-Identity 回應中傳送的使用者名稱。 如果 [**Username**](eaptlsuserpropertiesv1schema-username-element.md) 專案不存在，則 eap-tls 會使用 [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) 元素中所參考之憑證的名稱。<br/> |
| [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) | hexBinary | 指應用於驗證的憑證 SHA-1 雜湊。<br/>                                                                                                                                                                                                                             |



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

[eaptlsuserpropertiesv1 架構](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





