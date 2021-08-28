---
description: 包含各種連接設定。
ms.assetid: 2938f607-47a1-49eb-bf3f-247cab8637ec
title: " (.MSM) 元素的連接"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectivity
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8745671004799f96aecfe68b531c122c76122b5865678258fd241e9d8a07260a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799908"
---
# <a name="connectivity-msm-element"></a> (.MSM) 元素的連接

 (.MSM) 元素的連線，包含各種連線設定。

``` syntax
<xs:element name="connectivity"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="phyType"
                minOccurs="0"
                maxOccurs="4"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="a"
                         />
                        <xs:enumeration
                            value="b"
                         />
                        <xs:enumeration
                            value="g"
                         />
                        <xs:enumeration
                            value="n"
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

元素是由 [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) 元素定義。

## <a name="child-elements"></a>子元素



| 元素                                                            | 類型 |
|--------------------------------------------------------------------|------|
| [**phyType**](wlan-profileschema-phytype-connectivity-element.md) |      |



## <a name="examples"></a>範例

若要查看使用 **連接** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista，Windows XP 只提供 SP3 \[ desktop 應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                |
| 可轉散發套件<br/>          | 適用于 Windows XP SP2 的無線區域網路 API<br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**MSM**](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**MSM (WLANProfile)**](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 




