---
description: 包含 (.MSM) 設定的各種媒體專屬模組。
ms.assetid: 31f98af8-a577-4f6a-9a0a-b182b5a89cc3
title: MSM (WLANProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSM
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 78540c29239df9118732561562985021a512e104b0ddc5e05d43d89f37dd5e33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797938"
---
# <a name="msm-wlanprofile-element"></a>MSM (WLANProfile) 元素

MSM (WLANProfile) 元素包含各種不同的媒體特定模組 (MSM) 設定。

``` syntax
<xs:element name="MSM"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="security"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="authEncryption">
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="authentication">
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:enumeration
                                                    value="open"
                                                 />
                                                <xs:enumeration
                                                    value="shared"
                                                 />
                                                <xs:enumeration
                                                    value="WPA"
                                                 />
                                                <xs:enumeration
                                                    value="WPAPSK"
                                                 />
                                                <xs:enumeration
                                                    value="WPA2"
                                                 />
                                                <xs:enumeration
                                                    value="WPA2PSK"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="encryption">
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:enumeration
                                                    value="none"
                                                 />
                                                <xs:enumeration
                                                    value="WEP"
                                                 />
                                                <xs:enumeration
                                                    value="TKIP"
                                                 />
                                                <xs:enumeration
                                                    value="AES"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="useOneX"
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
                        <xs:element name="sharedKey"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="keyType">
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:enumeration
                                                    value="networkKey"
                                                 />
                                                <xs:enumeration
                                                    value="passPhrase"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="protected"
                                        type="boolean"
                                     />
                                    <xs:element name="keyMaterial"
                                        type="string"
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
                        <xs:element name="keyIndex"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="integer"
                                >
                                    <xs:minInclusive
                                        value="0"
                                     />
                                    <xs:maxInclusive
                                        value="3"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="PMKCacheMode"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:enumeration
                                        value="disabled"
                                     />
                                    <xs:enumeration
                                        value="enabled"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="PMKCacheTTL"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="integer"
                                >
                                    <xs:minInclusive
                                        value="5"
                                     />
                                    <xs:maxInclusive
                                        value="1400"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="PMKCacheSize"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="integer"
                                >
                                    <xs:minInclusive
                                        value="1"
                                     />
                                    <xs:maxInclusive
                                        value="255"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="preAuthMode"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:enumeration
                                        value="disabled"
                                     />
                                    <xs:enumeration
                                        value="enabled"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="preAuthThrottle"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="integer"
                                >
                                    <xs:minInclusive
                                        value="1"
                                     />
                                    <xs:maxInclusive
                                        value="16"
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



| 元素                                                                            | 類型                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**authEncryption**](wlan-profileschema-authencryption-security-element.md)       |                                                                   | 指定要用於此設定檔的驗證和加密組。<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**認證**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | 指定要用於此設定檔的驗證和加密組。<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**連接**](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | 包含各種連接設定。 這是選擇性的項目。<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**加密**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | 設定用來連接到無線區域網路的資料加密。<br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**keyIndex**](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | 指定必須使用哪一個金鑰索引來加密無線流量。 只有當 keyType 設定為 networkKey 時，才會使用這個。<br/>                                                                                                                                                                                                                                                                                          |
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md)            | [string](/dotnet/api/system.string)   | 包含網路金鑰或複雜密碼。<br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | 索引鍵的類型。<br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**phyType**](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | 指定無線區域網路上所使用的802.11 無線區域網路標準。 只有在 Windows Vista SP1 和更新版本的作業系統上，才支援值 "n"。<br/> **Windows xp 搭配 SP3 和適用于 Windows XP SP2 的無線區域網路 API：** 不支援這個元素。<br/>                                                                                                                        |
| [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | 指出是否會使用 PMK 快取。 此元素只對 WPA2 定義的網路有效。<br/> **Windows xp 搭配 SP3 和適用于 Windows XP SP2 的無線區域網路 API：** 不支援這個元素。<br/>                                                                                                                                                                                                 |
| [**PMKCacheSize**](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | 指定用戶端上 OMK 快取中的專案數。 此元素只適用于將 PMKCache 模式設定為啟用的 WPA2 定義網路。 如果已啟用 PMKCache 模式，且此元素不存在，則快取的大小會預設為128個專案。<br/> **Windows xp 搭配 SP3 和適用于 Windows XP SP2 的無線區域網路 API：** 不支援這個元素。<br/>                                   |
| [**PMKCacheTTL**](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | 指出將保留 PMK 快取的時間長度（以分鐘為單位）。 此元素只適用于將 PMKCache 模式設定為啟用的 WPA2 定義網路。<br/> **Windows xp 搭配 SP3 和適用于 Windows XP SP2 的無線區域網路 API：** 不支援這個元素。<br/>                                                                                                                                  |
| [**preAuthMode**](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | 判斷用戶端是否會使用預先驗證。 預先驗證可讓 WPA2 安全快速漫遊。 此元素只適用于將 PMKCache 模式設定為啟用的 WPA2 定義網路。 如果已啟用 PMKCache 模式，且此元素不存在，則預設值為停用。<br/> **Windows xp 搭配 SP3 和適用于 Windows XP SP2 的無線區域網路 API：** 不支援這個元素。<br/> |
| [**preAuthThrottle**](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | 指出 preauthenticating 至相鄰 Ap 時的嘗試次數。 此元素只適用于將 PMKCache 模式設定為啟用的 WPA2 定義網路。 如果已啟用 PMKCache 模式，且此元素不存在，則嘗試次數會預設為3。<br/> **Windows xp 搭配 SP3 和適用于 Windows XP SP2 的無線區域網路 API：** 不支援這個元素。<br/>                                      |
| [**受保護**](wlan-profileschema-protected-sharedkey-element.md)                | [boolean](/dotnet/api/system.boolean) | 指出金鑰是否已加密。<br/> **Windows xp 搭配 SP3 和適用于 Windows XP SP2 的無線區域網路 API：** 這個元素的值必須為 FALSE。<br/>                                                                                                                                                                                                                                                 |
| [**安全**](wlan-profileschema-security-msm-element.md)                        |                                                                   | 包含各種安全性設定。 這是選擇性的項目。<br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**sharedKey**](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | 包含共用金鑰資訊。 只有在驗證和加密配對需要 WEP 或 PSK 金鑰時，才需要這個元素。<br/>                                                                                                                                                                                                                                                                    |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [boolean](/dotnet/api/system.boolean) | 指出是否使用 802.1 X。 此旗標是選擇性的。<br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a>備註

[**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md)元素可以插入做為 [**authEncryption**](wlan-profileschema-authencryption-security-element.md)元素的子系。 您可以將 [**OneX**](onexschema-onex-element.md) 元素插入為 [**安全性 (.msm)**](wlan-profileschema-security-msm-element.md) 元素的子系。

## <a name="examples"></a>範例

若要查看使用 **MSM** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista，Windows XP 只提供 SP3 \[ desktop 應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                |
| 可轉散發套件<br/>          | 適用于 Windows XP SP2 的無線區域網路 API<br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[無線設定檔範例](wireless-profile-samples.md)
</dt> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
