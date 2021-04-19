---
title: 'EapType 元素 (mschapv2connectionpropertiesv1schema) '
description: 這是 baseeapconnectionpropertiesv1 架構中 EapType 元素的衍生型別。 這是出現在 EapHostConfig 架構之 Config 元素內的最上層元素。
ms.assetid: dbd63387-f8ed-4308-903f-7a555f3410f7
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
ms.openlocfilehash: 3e9b7db3d3e3ab1ba90427a65a5544b87939ca88
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106996542"
---
# <a name="eaptype-element-mschapv2connectionpropertiesv1schema"></a>EapType 元素 (mschapv2connectionpropertiesv1schema) 

**EapType** 元素是 [Baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)架構中 [EapType](baseeapconnectionpropertiesv1schema-eaptype-element.md)元素的衍生型別。 這是出現在 [EapHostConfig](eaphostconfigschema-elements.md) 架構之 Config 元素內的最上層元素。

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
                    <xs:element name="UseWinLogonCredentials"
                        type="boolean"
                        default="true"
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



| 元素                                                                                                       | 類型    | Description                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UseWinLogonCredentials**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) | boolean | 控制 winlogin 認證的使用。 若為 TRUE，則表示 EAP MS-CHAPv2 從 winlogon 取得認證。 如果為 FALSE，則表示 EAP MS-CHAPv2 取得使用者的認證。 <br/> [**UseWinLogonCredentials (EapType)**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md)元素是選擇性的。<br/> |



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

[mschapv2connectionpropertiesv1 架構](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





