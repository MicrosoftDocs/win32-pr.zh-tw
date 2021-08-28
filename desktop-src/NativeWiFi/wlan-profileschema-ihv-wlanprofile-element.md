---
description: 包含獨立硬體廠商的各種設定。
ms.assetid: 4ad8c991-7849-41d6-9852-1ecadc372a2d
title: IHV (WLANProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IHV
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1cfcd9ee463ef91d04d0bebbeac800d48da32fdd777edc2a08ccf0051410160d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799918"
---
# <a name="ihv-wlanprofile-element"></a>IHV (WLANProfile) 元素

IHV (WLANProfile) 元素包含獨立硬體廠商的各種設定。 如果設定檔包含 IHV 安全性設定，則會覆寫任何 Microsoft 定義的安全性。

**Windows xp 搭配 SP3 和適用于 Windows XP SP2 的無線區域網路 API：** 不支援這個元素。

``` syntax
<xs:element name="IHV"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="connectivity"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="security"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="useMSOneX"
                type="boolean"
                minOccurs="0"
             />
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

元素是由 [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) 元素所定義。

## <a name="child-elements"></a>子元素



| 元素                                                             | 類型                                                              | 描述                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**連接**](wlan-profileschema-connectivity-ihv-element.md) |                                                                   | 包含與 IHV 相關的連線能力設定。<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**OUI**](wlan-profileschema-oui-ouiheader-element.md)             |                                                                   | 包含用來識別 IHV 的3個位元組 hexBinary。<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md)       |                                                                   | 識別 IHV。<br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [**安全**](wlan-profileschema-security-ihv-element.md)         |                                                                   | 包含 IHV 特定的安全性設定。 Microsoft 安全性設定和 IHV 安全性設定都是互斥的。 如果這兩個安全性設定都存在，則整個設定檔無效。<br/>                                                                                                                                                                                            |
| [**類型**](wlan-profileschema-type-ouiheader-element.md)           |                                                                   | 包含1個位元組的 hexBinary，用來區分 Nic 的相同 IHV。<br/>                                                                                                                                                                                                                                                                                                        |
| [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md)       | [boolean](/dotnet/api/system.boolean) | 指定 IHV 安全性元件所使用之 802.1 X 安全性設定的來源。 當 [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) 為 true 時，IHV 安全性元件會使用 Microsoft 定義的 802.1 x 設定。 當 **useMSOneX** 為 false 時，IHV 安全性元件會使用廠商提供的 802.1 x 設定。 依預設， **useMSOneX** 為 false。 這是選擇性的項目。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
