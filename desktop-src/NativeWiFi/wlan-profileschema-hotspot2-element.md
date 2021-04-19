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
# <a name="hotspot2-wlanprofile-element"></a><span data-ttu-id="16350-103">Hotspot2 (WLANProfile) 元素</span><span class="sxs-lookup"><span data-stu-id="16350-103">Hotspot2 (WLANProfile) element</span></span>

<span data-ttu-id="16350-104">擴充 WLAN 設定檔架構 v1 以支援熱點2.0 網路。</span><span class="sxs-lookup"><span data-stu-id="16350-104">Extends the WLAN Profile Schema v1 to support Hotspot 2.0 networks.</span></span> <span data-ttu-id="16350-105">作用點2.0 可讓您使用現有的認證和服務提供者網路中的成員資格，自動連線至公用 Wi-Fi 服務。</span><span class="sxs-lookup"><span data-stu-id="16350-105">Hotspot 2.0 enables automatic connection to public Wi-Fi services using existing credentials and membership in service provider networks.</span></span> <span data-ttu-id="16350-106">服務提供者會指定如何使用新的架構專案來描述要使用的網路，以及如何對它們進行驗證。</span><span class="sxs-lookup"><span data-stu-id="16350-106">Service providers specify how connections are made using the new schema elements to describe which networks to use, and how to authenticate to them.</span></span>

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

<span data-ttu-id="16350-107">元素是由 [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="16350-107">The element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="16350-108">子元素</span><span class="sxs-lookup"><span data-stu-id="16350-108">Child elements</span></span>

| <span data-ttu-id="16350-109">元素</span><span class="sxs-lookup"><span data-stu-id="16350-109">Element</span></span> | <span data-ttu-id="16350-110">類型</span><span class="sxs-lookup"><span data-stu-id="16350-110">Type</span></span> | <span data-ttu-id="16350-111">Description</span><span class="sxs-lookup"><span data-stu-id="16350-111">Description</span></span> |
|-|-|-|
| [<span data-ttu-id="16350-112">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="16350-112">**DomainName**</span></span>](wlan-profileschema-hotspot2-domainname-element.md) | | <span data-ttu-id="16350-113">裝置家用網路提供者的功能變數名稱，識別網路的操作員。</span><span class="sxs-lookup"><span data-stu-id="16350-113">The domain name for the device's Home Network Provider, identifying the operator of the network.</span></span> |
| [<span data-ttu-id="16350-114">**NAIRealm**</span><span class="sxs-lookup"><span data-stu-id="16350-114">**NAIRealm**</span></span>](wlan-profileschema-hotspot2-nairealm-element.md) | | <span data-ttu-id="16350-115"> (NAI) 領域識別碼的網路存取識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="16350-115">A list of Network Access Identifier (NAI) Realm identifiers.</span></span> <span data-ttu-id="16350-116">這份清單中的專案通常是表單 user@domain 。</span><span class="sxs-lookup"><span data-stu-id="16350-116">Entries in this list are usually of the form user@domain.</span></span> |
| [<span data-ttu-id="16350-117">**Network3GPP**</span><span class="sxs-lookup"><span data-stu-id="16350-117">**Network3GPP**</span></span>](wlan-profileschema-hotspot2-network3gpp-element.md) | | <span data-ttu-id="16350-118">公開 Land Mobile Network (PLMN) 識別碼的清單。</span><span class="sxs-lookup"><span data-stu-id="16350-118">A list of Public Land Mobile Network (PLMN) IDs.</span></span> |
| [<span data-ttu-id="16350-119">**RoamingConsortium**</span><span class="sxs-lookup"><span data-stu-id="16350-119">**RoamingConsortium**</span></span>](wlan-profileschema-hotspot2-roamingconsortium-element.md) | | <span data-ttu-id="16350-120">由 IEEE 指派 (OUI) 的組織唯一識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="16350-120">A list of Organizationally Unique Identifiers (OUI) assigned by IEEE.</span></span>  |

## <a name="examples"></a><span data-ttu-id="16350-121">範例</span><span class="sxs-lookup"><span data-stu-id="16350-121">Examples</span></span>

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
