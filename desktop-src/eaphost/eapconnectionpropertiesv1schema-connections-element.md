---
title: Connections 元素
description: 瞭解 Connections 元素。 這個元素會收集和包含零或多個連接元素。
ms.assetid: 2c199338-892f-4d8c-bf33-4a19f362de3e
keywords:
- Connections 元素 EAPHost
topic_type:
- apiref
api_name:
- Connections
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 62635d09030875a4f17deefa1aec05432df5662369eb483894f1a8cef4bbaf5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118498216"
---
# <a name="connections-element"></a>Connections 元素

**Connections** 元素會收集和包含零或多個 [**連接**](eapconnectionpropertiesv1schema-connection-connections-element.md)元素。

``` syntax
<xs:element name="Connections">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Connection"
                minOccurs="0"
                maxOccurs="unbounded"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Name"
                            type="string"
                         />
                        <xs:element
                            maxOccurs="unbounded"
                            ref="Eap"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>子元素



| 元素                                                                              | 類型   | Description                                                                                                                                                                                |
|--------------------------------------------------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md)                       |        | 識別 EAP 設定元素。<br/>                                                                                                                                       |
| [**連接**](eapconnectionpropertiesv1schema-connection-connections-element.md) |        | 定義每個設定設定，並將其與名稱產生關聯。 [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md)元素是選擇性的。<br/> |
| [**名稱**](eapconnectionpropertiesv1schema-name-connection-element.md)              | string | 會捕獲所定義之連接的名稱，以協助識別多個連接。<br/>                                                                     |



## <a name="remarks"></a>備註

**Connections** 元素不能透過 EAPHost api 與舊版方法搭配使用。

## <a name="requirements"></a>規格需求



| 角色 | 最低支援作業系統版本 |
|------|------------------------------|
| 用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[eapconnectionpropertiesv1 架構](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





