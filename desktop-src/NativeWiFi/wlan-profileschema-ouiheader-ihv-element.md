---
description: 識別 IHV。
ms.assetid: a99c231c-afd7-44e6-81af-3d49ffef8714
title: OUIHeader (IHV) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUIHeader
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a31feb123e31489c751b7844e06d5c344278778e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986329"
---
# <a name="ouiheader-ihv-element"></a>OUIHeader (IHV) 元素

OUIHeader (IHV) 元素會識別 IHV。

Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。

``` syntax
<xs:element name="OUIHeader">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUI">
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:length
                            value="3"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="type">
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:length
                            value="1"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
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

元素是由 [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) 元素定義。

## <a name="child-elements"></a>子元素



| 元素                                                   | 類型 | Description                                                                                |
|-----------------------------------------------------------|------|--------------------------------------------------------------------------------------------|
| [**OUI**](wlan-profileschema-oui-ouiheader-element.md)   |      | 包含用來識別 IHV 的3個位元組 hexBinary。<br/>                            |
| [**類型**](wlan-profileschema-type-ouiheader-element.md) |      | 包含1個位元組的 hexBinary，用來區分 Nic 的相同 IHV。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**IHV**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**IHV (WLANProfile)**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




