---
title: 'EapType 元素 (mspeapuserpropertiesv1schema) '
description: 這個元素是 baseeapuserpropertiesv1 架構中 EapType 元素的衍生型別。 適用于 mspeapuserpropertiesv1schema。
ms.assetid: 921c1f95-900a-4fd2-bb42-341e5ba39b23
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
ms.openlocfilehash: e27923d77a36b917b3356b7c5c79d408bc0a99d49d70967677b56a9047ed0b63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067178"
---
# <a name="eaptype-element-mspeapuserpropertiesv1schema"></a>EapType 元素 (mspeapuserpropertiesv1schema) 

**EapType** 元素是 [Baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)架構中 [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md)元素的衍生型別。

``` syntax
<xs:element name="EapType
        "
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
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="PeapExtensions"
                        type="PeapExtensionsType"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>子元素



| 元素                                                                               | 類型                                                                                      | 描述                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Eap**](baseeapuserpropertiesv1schema-eap-element.md)                              |                                                                                           | [**Eap**](baseeapuserpropertiesv1schema-eap-element.md)元素會識別要搭配該方法使用的內部方法和認證。 當您針對 PEAP 來賓存取設定 PEAP 設定時，不會出現這個元素。<br/>                                  |
| [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) | [**PeapExtensionsType**](mspeapuserpropertiesv1schema-peapextensionstype-complextype.md) | [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md)元素可讓架構的未來增強功能。 <br/> [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md)元素是選擇性的。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[mspeapuserpropertiesv1 架構](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





