---
title: EapMethodType 複雜類型
description: 定義可唯一識別單一 EAP 方法類型、VendorId、VendorType 和作者的元素。
ms.assetid: 3ef96187-7376-438d-9d47-a87d5a6c9b8b
keywords:
- EapMethodType 複雜類型 EAPHost
topic_type:
- apiref
api_name:
- EapMethodType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 059ea8162241c61d88fc93f565fa0aa4ba8aee223212e6fab254ed9d5dec4eea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739168"
---
# <a name="eapmethodtype-complex-type"></a>EapMethodType 複雜類型

**EapMethodType** 複雜型別會定義可唯一識別單一 EAP 方法的專案： [**type**](eapcommonschema-type-eapmethodtype-element.md)、 [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md)、 [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md)和 [**作者**](eapcommonschema-authorid-eapmethodtype-element.md)。

[**型**](eapcommonschema-type-eapmethodtype-element.md)別 [**和作者**](eapcommonschema-authorid-eapmethodtype-element.md)是必要元素，而只有當 **type** 元素是 254 (擴充的 EAP 方法) 時，才需要使用 [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md)和 [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) 。

``` syntax
<xs:complexType name="EapMethodType">
    <xs:sequence>
        <xs:element name="Type"
            type="unsignedByte"
         />
        <xs:element name="VendorId"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="VendorType"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="AuthorId"
            type="unsignedInt"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                | 類型         | 描述                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**作者**](eapcommonschema-authorid-eapmethodtype-element.md)     | unsignedInt  | 指的是方法作者。 <br/>                                                                                                                                                                                                                 |
| [**類型**](eapcommonschema-type-eapmethodtype-element.md)             | unsignedByte | 代表 EAP 方法類型。 <br/>                                                                                                                                                                                                               |
| [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md)     | unsignedInt  | 代表定義方法的廠商-如果 [**Type**](eapcommonschema-type-eapmethodtype-element.md) 元素是 254 (擴充的 EAP 方法) 。 [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md)是選擇性的。 <br/> |
| [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) | unsignedInt  | 是方法的廠商定義型別。 [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md)是選擇性的。 <br/>                                                                                                           |



## <a name="remarks"></a>備註

針對特定方法， [**作者**](eapcommonschema-authorid-eapmethodtype-element.md) 和 [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) 元素不需要相同的。

[**作者**](eapcommonschema-authorid-eapmethodtype-element.md)、[**類型**](eapcommonschema-type-eapmethodtype-element.md)、 [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md)和 [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md)元素都是由網際網路指派的數位授權單位所發出的唯一號碼 (IANA) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[eapcommon 架構](eapcommonschema-schema.md)
</dt> </dl>

 

 





