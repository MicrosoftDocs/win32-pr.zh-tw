---
description: 擴充 WLAN 設定檔架構 v1 以支援熱點2.0 網路。
ms.assetid: DE30DBCB-80B9-43D0-8DE1-56BBA99DBF31
title: Hotspot2 (WLANProfile) 元素
ms.topic: reference
ms.date: 10/08/2019
topic_type:
- APIRef
- kbSyntax
api_name:
- Hotspot2
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0e372c1025a74dfb304cacdb0f3a4cf18bcdbabd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966740"
---
# <a name="hotspot2-wlanprofile-element"></a>Hotspot2 (WLANProfile) 元素

擴充 WLAN 設定檔架構 v1 以支援熱點2.0 網路。 作用點2.0 可讓您使用現有的認證和服務提供者網路中的成員資格，自動連線至公用 Wi-Fi 服務。 服務提供者會指定如何使用新的架構專案來描述要使用的網路，以及如何對它們進行驗證。

``` syntax
<xs:element name="Hotspot2">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="DomainName"
                minOccurs="0"
             />
            <xs:element name="NAIRealm"
                minOccurs="0"
             />
            <xs:element name="Network3GPP"
                minOccurs="0"
             />
            <xs:element name="RoamingConsortium"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

元素是由 [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) 元素所定義。

## <a name="child-elements"></a>子元素

| 元素 | 類型 | Description |
|-|-|-|
| [**DomainName**](wlan-profileschema-hotspot2-domainname-element.md) | | 裝置家用網路提供者的功能變數名稱，識別網路的操作員。 |
| [**NAIRealm**](wlan-profileschema-hotspot2-nairealm-element.md) | |  (NAI) 領域識別碼的網路存取識別碼清單。 這份清單中的專案通常是表單 user@domain 。 |
| [**Network3GPP**](wlan-profileschema-hotspot2-network3gpp-element.md) | | 公開 Land Mobile Network (PLMN) 識別碼的清單。 |
| [**RoamingConsortium**](wlan-profileschema-hotspot2-roamingconsortium-element.md) | | 由 IEEE 指派 (OUI) 的組織唯一識別碼清單。  |

## <a name="examples"></a>範例

```xml
<Hotspot2>
  <DomainName>contoso.com</DomainName>
  <NAIRealm>
    <name>test1@contoso.com</name>
    <name>test2@contoso.com</name>
  </NAIRealm>
  <Network3GPP>
    <PLMNID>12345</PLMNID>
    <PLMNID>123456</PLMNID>
  </Network3GPP>
  <RoamingConsortium>
    <OUI>00AABB</OUI>
    <OUI>001122</OUI>
  </RoamingConsortium>
</Hotspot2>
```
