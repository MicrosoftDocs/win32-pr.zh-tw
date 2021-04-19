---
title: 連接) 元素 (連接
description: 定義每個設定設定，並將其與名稱產生關聯。 Connection 元素是選擇性的。
ms.assetid: 913263ab-0e0e-4213-947b-7bca9ba0697e
keywords:
- 連接元素 EAPHost
topic_type:
- apiref
api_name:
- Connection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5aabc29a7fe5122a7f7571750b97ebccb38158d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966507"
---
# <a name="connection-connections-element"></a>連接) 元素 (連接

**連接 (連接)** 元素會定義每個設定設定，並將其與名稱產生關聯。 **Connection** 元素是選擇性的。

``` syntax
<xs:element name="Connection">
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
```

**Connection** 元素是由 [**Connections**](eapconnectionpropertiesv1schema-connections-element.md)元素所定義。

## <a name="child-elements"></a>子元素



| 元素                                                                 | 類型   | Description                                                                                                             |
|-------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------|
| [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md)          |        | 識別 EAP 設定元素。<br/>                                                                    |
| [**名稱**](eapconnectionpropertiesv1schema-name-connection-element.md) | 字串 | 會捕獲所定義之連接的名稱，以協助識別多個連接。 <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**連接**](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**連接**](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[eapconnectionpropertiesv1 架構](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





