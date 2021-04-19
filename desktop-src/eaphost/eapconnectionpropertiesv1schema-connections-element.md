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
ms.openlocfilehash: 6cdb23c9f1a6130e2fe77061286e8a0657c3e2f5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106965671"
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
| [**連線**](eapconnectionpropertiesv1schema-connection-connections-element.md) |        | 定義每個設定設定，並將其與名稱產生關聯。 [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md)元素是選擇性的。<br/> |
| [**名稱**](eapconnectionpropertiesv1schema-name-connection-element.md)              | 字串 | 會捕獲所定義之連接的名稱，以協助識別多個連接。<br/>                                                                     |



## <a name="remarks"></a>備註

**Connections** 元素不能透過 EAPHost api 與舊版方法搭配使用。

## <a name="requirements"></a>規格需求



| 角色 | 最低支援作業系統版本 |
|------|------------------------------|
| 用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[eapconnectionpropertiesv1 架構](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





