---
description: 包含無線局域網路設定檔。
ms.assetid: bc97cb49-3891-4a4a-aab4-895cd9ce6908
title: WLANProfile 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLANProfile
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 227d912128bf3f656fca7aecbaf0fe0640659465
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852519"
---
# <a name="wlanprofile-element"></a><span data-ttu-id="94459-103">WLANProfile 元素</span><span class="sxs-lookup"><span data-stu-id="94459-103">WLANProfile Element</span></span>

<span data-ttu-id="94459-104">**WLANProfile** 元素包含無線局域網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="94459-104">The **WLANProfile** element contains a wireless LAN profile.</span></span> <span data-ttu-id="94459-105">此元素是無線設定檔的唯一根項目。</span><span class="sxs-lookup"><span data-stu-id="94459-105">This element is the unique root element for a wireless profile.</span></span>

<span data-ttu-id="94459-106">WLANProfile 元素的目標命名空間為 `https://www.microsoft.com/networking/WLAN/profile/v1` 。</span><span class="sxs-lookup"><span data-stu-id="94459-106">The target namespace for the WLANProfile element is `https://www.microsoft.com/networking/WLAN/profile/v1`.</span></span>

``` syntax
<xs:element name="WLANProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="SSIDConfig"
                maxOccurs="256"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="SSID"
                            maxOccurs="256"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="hex"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="hexBinary"
                                            >
                                                <xs:minLength
                                                    value="1"
                                                 />
                                                <xs:maxLength
                                                    value="32"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="name"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:minLength
                                                    value="1"
                                                 />
                                                <xs:maxLength
                                                    value="32"
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
                        <xs:element name="nonBroadcast"
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
            <xs:element name="connectionType">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="IBSS"
                         />
                        <xs:enumeration
                            value="ESS"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="connectionMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="auto"
                         />
                        <xs:enumeration
                            value="manual"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="autoSwitch"
                type="boolean"
                minOccurs="0"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
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

## <a name="child-elements"></a><span data-ttu-id="94459-107">子元素</span><span class="sxs-lookup"><span data-stu-id="94459-107">Child elements</span></span>



| <span data-ttu-id="94459-108">元素</span><span class="sxs-lookup"><span data-stu-id="94459-108">Element</span></span>                                                                            | <span data-ttu-id="94459-109">類型</span><span class="sxs-lookup"><span data-stu-id="94459-109">Type</span></span>                                                              | <span data-ttu-id="94459-110">Description</span><span class="sxs-lookup"><span data-stu-id="94459-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94459-111">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="94459-111">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)       |                                                                   | <span data-ttu-id="94459-112">指定要用於此設定檔的驗證和加密組。</span><span class="sxs-lookup"><span data-stu-id="94459-112">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="94459-113">**認證**</span><span class="sxs-lookup"><span data-stu-id="94459-113">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="94459-114">指定要用來連接到無線區域網路的驗證方法。</span><span class="sxs-lookup"><span data-stu-id="94459-114">Specifies the authentication method to be used to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="94459-115">**autoSwitch**</span><span class="sxs-lookup"><span data-stu-id="94459-115">**autoSwitch**</span></span>](wlan-profileschema-autoswitch-wlanprofile-element.md)            | [<span data-ttu-id="94459-116">boolean</span><span class="sxs-lookup"><span data-stu-id="94459-116">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="94459-117">決定當更慣用的網路在範圍內時，自動連線網路的漫遊行為。</span><span class="sxs-lookup"><span data-stu-id="94459-117">Determines the roaming behavior of an auto-connected network when a more preferred network is in range.</span></span> <span data-ttu-id="94459-118">這個元素是選擇性的，不會影響手動連接的網路。</span><span class="sxs-lookup"><span data-stu-id="94459-118">This element is optional and has no effect on a manually connected network.</span></span><br/> <span data-ttu-id="94459-119">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="94459-119">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="94459-120">**connectionMode**</span><span class="sxs-lookup"><span data-stu-id="94459-120">**connectionMode**</span></span>](wlan-profileschema-connectionmode-wlanprofile-element.md)    |                                                                   | <span data-ttu-id="94459-121">指出無線區域網路的連接是否應該自動 ( 「自動」 ) 或由使用者起始 ( 「) 手動」。</span><span class="sxs-lookup"><span data-stu-id="94459-121">Indicates whether connection to the wireless LAN should be automatic ("auto") or initiated ("manual") by user.</span></span> <span data-ttu-id="94459-122">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="94459-122">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="94459-123">**connectionType**</span><span class="sxs-lookup"><span data-stu-id="94459-123">**connectionType**</span></span>](wlan-profileschema-connectiontype-wlanprofile-element.md)    |                                                                   | <span data-ttu-id="94459-124">指出網路是否為基礎結構 ( "ESS" ) 或臨機操作 ( "IBSS" ) 。</span><span class="sxs-lookup"><span data-stu-id="94459-124">Indicates whether the network is infrastructure ("ESS") or ad-hoc ("IBSS").</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="94459-125">**連接**</span><span class="sxs-lookup"><span data-stu-id="94459-125">**connectivity**</span></span>](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | <span data-ttu-id="94459-126">包含各種連接設定。</span><span class="sxs-lookup"><span data-stu-id="94459-126">Contains various connectivity settings.</span></span> <span data-ttu-id="94459-127">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="94459-127">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="94459-128">**連接**</span><span class="sxs-lookup"><span data-stu-id="94459-128">**connectivity**</span></span>](wlan-profileschema-connectivity-ihv-element.md)                |                                                                   | <span data-ttu-id="94459-129">包含與 IHV 相關的連線能力設定。</span><span class="sxs-lookup"><span data-stu-id="94459-129">Contains IHV-related connectivity settings.</span></span><br/> <span data-ttu-id="94459-130">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="94459-130">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="94459-131">**加密**</span><span class="sxs-lookup"><span data-stu-id="94459-131">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="94459-132">設定用來連接到無線區域網路的資料加密。</span><span class="sxs-lookup"><span data-stu-id="94459-132">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="94459-133">**hex**</span><span class="sxs-lookup"><span data-stu-id="94459-133">**hex**</span></span>](wlan-profileschema-hex-ssid-element.md)                                 |                                                                   | <span data-ttu-id="94459-134">包含十六進位格式的無線區域網路 SSID。</span><span class="sxs-lookup"><span data-stu-id="94459-134">Contains the SSID of a wireless LAN in hexadecimal format.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="94459-135">**IHV**</span><span class="sxs-lookup"><span data-stu-id="94459-135">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)                          |                                                                   | <span data-ttu-id="94459-136">包含 (IHV) 設定的選用獨立硬體廠商。</span><span class="sxs-lookup"><span data-stu-id="94459-136">Contains optional independent hardware vendor (IHV) settings.</span></span><br/> <span data-ttu-id="94459-137">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="94459-137">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="94459-138">**keyIndex**</span><span class="sxs-lookup"><span data-stu-id="94459-138">**keyIndex**</span></span>](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | <span data-ttu-id="94459-139">指定應該使用哪一個金鑰索引來加密無線流量。</span><span class="sxs-lookup"><span data-stu-id="94459-139">Specifies which key index should be used to encrypt wireless traffic.</span></span> <span data-ttu-id="94459-140">只有當 [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) 設定為 "networkKey" 時，才會使用這個。</span><span class="sxs-lookup"><span data-stu-id="94459-140">This is only used when [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) is set to "networkKey".</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="94459-141">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="94459-141">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)            | [<span data-ttu-id="94459-142">string</span><span class="sxs-lookup"><span data-stu-id="94459-142">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="94459-143">包含網路金鑰或複雜密碼。</span><span class="sxs-lookup"><span data-stu-id="94459-143">Contains the network key or passphrase.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="94459-144">**keyType**</span><span class="sxs-lookup"><span data-stu-id="94459-144">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | <span data-ttu-id="94459-145">索引鍵的類型。</span><span class="sxs-lookup"><span data-stu-id="94459-145">Type of key.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="94459-146">**MSM**</span><span class="sxs-lookup"><span data-stu-id="94459-146">**MSM**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)                          |                                                                   | <span data-ttu-id="94459-147">包含各種 MSM 設定。</span><span class="sxs-lookup"><span data-stu-id="94459-147">Contains various MSM settings.</span></span> <span data-ttu-id="94459-148">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="94459-148">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="94459-149">**名字**</span><span class="sxs-lookup"><span data-stu-id="94459-149">**name**</span></span>](wlan-profileschema-name-wlanprofile-element.md)                        | [<span data-ttu-id="94459-150">**nameType**</span><span class="sxs-lookup"><span data-stu-id="94459-150">**nameType**</span></span>](wlan-profileschema-nametype-simpletype.md)        | <span data-ttu-id="94459-151">WLAN 設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="94459-151">Name of the WLAN profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="94459-152">**名字**</span><span class="sxs-lookup"><span data-stu-id="94459-152">**name**</span></span>](wlan-profileschema-name-ssid-element.md)                               |                                                                   | <span data-ttu-id="94459-153">包含無線區域網路的 SSID。</span><span class="sxs-lookup"><span data-stu-id="94459-153">Contains the SSID of a wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="94459-154">**廣播**</span><span class="sxs-lookup"><span data-stu-id="94459-154">**nonBroadcast**</span></span>](wlan-profileschema-nonbroadcast-ssidconfig-element.md)         | [<span data-ttu-id="94459-155">boolean</span><span class="sxs-lookup"><span data-stu-id="94459-155">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="94459-156">指出網路是否會廣播其 SSID。</span><span class="sxs-lookup"><span data-stu-id="94459-156">Indicates whether the network broadcasts its SSID.</span></span><br/> <span data-ttu-id="94459-157">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="94459-157">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="94459-158">**OUI**</span><span class="sxs-lookup"><span data-stu-id="94459-158">**OUI**</span></span>](wlan-profileschema-oui-ouiheader-element.md)                            |                                                                   | <span data-ttu-id="94459-159">包含用來識別 IHV 的3個位元組 hexBinary。</span><span class="sxs-lookup"><span data-stu-id="94459-159">Contains a 3 byte hexBinary that identifies the IHV.</span></span><br/> <span data-ttu-id="94459-160">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="94459-160">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="94459-161">**OUIHeader**</span><span class="sxs-lookup"><span data-stu-id="94459-161">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)                      |                                                                   | <span data-ttu-id="94459-162">識別 IHV。</span><span class="sxs-lookup"><span data-stu-id="94459-162">Identifies the IHV.</span></span><br/> <span data-ttu-id="94459-163">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="94459-163">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="94459-164">**phyType**</span><span class="sxs-lookup"><span data-stu-id="94459-164">**phyType**</span></span>](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | <span data-ttu-id="94459-165">指定無線區域網路上所使用的802.11 無線區域網路標準。</span><span class="sxs-lookup"><span data-stu-id="94459-165">Specifies the 802.11 wireless LAN standard used on the wireless LAN.</span></span> <span data-ttu-id="94459-166">只有在 Windows Vista SP1 和更新版本的作業系統上，才支援值 "n"。</span><span class="sxs-lookup"><span data-stu-id="94459-166">The value "n" is only supported on Windows Vista with SP1 and later versions of the operating system.</span></span><br/> <span data-ttu-id="94459-167">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="94459-167">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="94459-168">**PMKCacheMode**</span><span class="sxs-lookup"><span data-stu-id="94459-168">**PMKCacheMode**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | <span data-ttu-id="94459-169">指出是否會使用 PMK 快取。</span><span class="sxs-lookup"><span data-stu-id="94459-169">Indicates whether PMK caching will be used.</span></span> <span data-ttu-id="94459-170">此元素只對 WPA2 定義的網路有效。</span><span class="sxs-lookup"><span data-stu-id="94459-170">This element is valid only for WPA2-defined networks.</span></span><br/> <span data-ttu-id="94459-171">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="94459-171">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="94459-172">**PMKCacheSize**</span><span class="sxs-lookup"><span data-stu-id="94459-172">**PMKCacheSize**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | <span data-ttu-id="94459-173">指定用戶端上 PMK 快取中的專案數。</span><span class="sxs-lookup"><span data-stu-id="94459-173">Specifies the number of entries in the PMK cache on the client.</span></span> <span data-ttu-id="94459-174">只有在 [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) 設定為 "enabled" 的 WPA2 定義網路上，此元素才有效。</span><span class="sxs-lookup"><span data-stu-id="94459-174">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="94459-175">如果 **PMKCacheMode** 已啟用，且此元素不存在，則快取的大小會預設為128個專案。</span><span class="sxs-lookup"><span data-stu-id="94459-175">If **PMKCacheMode** is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span><br/> <span data-ttu-id="94459-176">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="94459-176">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="94459-177">**PMKCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="94459-177">**PMKCacheTTL**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | <span data-ttu-id="94459-178">指出將保留 PMK 快取的時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="94459-178">Indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="94459-179">只有在 [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) 設定為 "enabled" 的 WPA2 定義網路上，此元素才有效。</span><span class="sxs-lookup"><span data-stu-id="94459-179">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span><br/> <span data-ttu-id="94459-180">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="94459-180">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="94459-181">**preAuthMode**</span><span class="sxs-lookup"><span data-stu-id="94459-181">**preAuthMode**</span></span>](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | <span data-ttu-id="94459-182">判斷用戶端是否會使用預先驗證。</span><span class="sxs-lookup"><span data-stu-id="94459-182">Determines if pre-authentication will be used by the client.</span></span> <span data-ttu-id="94459-183">預先驗證可讓 WPA2 安全快速漫遊。</span><span class="sxs-lookup"><span data-stu-id="94459-183">Pre-authentication enables WPA2 secure fast roaming.</span></span> <span data-ttu-id="94459-184">只有在 [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) 設定為 "enabled" 的 WPA2 定義網路上，此元素才有效。</span><span class="sxs-lookup"><span data-stu-id="94459-184">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="94459-185">如果 **PMKCacheMode** 已啟用，且此元素不存在，則預設值為停用。</span><span class="sxs-lookup"><span data-stu-id="94459-185">If **PMKCacheMode** is enabled, and this element is absent, the default value is disabled.</span></span><br/> <span data-ttu-id="94459-186">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="94459-186">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="94459-187">**preAuthThrottle**</span><span class="sxs-lookup"><span data-stu-id="94459-187">**preAuthThrottle**</span></span>](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | <span data-ttu-id="94459-188">指出 preauthenticating 至相鄰 Ap 時的嘗試次數。</span><span class="sxs-lookup"><span data-stu-id="94459-188">Indicates the number of tries when preauthenticating to neighboring APs.</span></span> <span data-ttu-id="94459-189">只有在 [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) 設定為 "enabled" 的 WPA2 定義網路上，此元素才有效。</span><span class="sxs-lookup"><span data-stu-id="94459-189">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="94459-190">如果 **PMKCacheMode** 已啟用，且此元素不存在，則嘗試次數會預設為3。</span><span class="sxs-lookup"><span data-stu-id="94459-190">If **PMKCacheMode** is enabled, and this element is absent, the number of tries defaults to 3.</span></span><br/> <span data-ttu-id="94459-191">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="94459-191">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="94459-192">**受保護**</span><span class="sxs-lookup"><span data-stu-id="94459-192">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)                | [<span data-ttu-id="94459-193">boolean</span><span class="sxs-lookup"><span data-stu-id="94459-193">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="94459-194">指出金鑰是否已加密。</span><span class="sxs-lookup"><span data-stu-id="94459-194">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="94459-195">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 這個元素的值必須為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="94459-195">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of **FALSE**.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="94459-196">**安全**</span><span class="sxs-lookup"><span data-stu-id="94459-196">**security**</span></span>](wlan-profileschema-security-msm-element.md)                        |                                                                   | <span data-ttu-id="94459-197">包含各種安全性設定。</span><span class="sxs-lookup"><span data-stu-id="94459-197">Contains various security settings.</span></span> <span data-ttu-id="94459-198">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="94459-198">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="94459-199">**安全**</span><span class="sxs-lookup"><span data-stu-id="94459-199">**security**</span></span>](wlan-profileschema-security-ihv-element.md)                        |                                                                   | <span data-ttu-id="94459-200">包含 IHV 特定的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="94459-200">Contains IHV-specific security settings.</span></span> <span data-ttu-id="94459-201">Microsoft 安全性設定和 IHV 安全性設定都是互斥的。</span><span class="sxs-lookup"><span data-stu-id="94459-201">Microsoft security settings and IHV security settings are mutually exclusive.</span></span> <span data-ttu-id="94459-202">如果相同的設定檔中有這兩組安全性設定，則設定檔無效。</span><span class="sxs-lookup"><span data-stu-id="94459-202">If both sets of security settings are present in the same profile, the profile is invalid.</span></span><br/> <span data-ttu-id="94459-203">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="94459-203">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="94459-204">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="94459-204">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | <span data-ttu-id="94459-205">包含共用金鑰資訊。</span><span class="sxs-lookup"><span data-stu-id="94459-205">Contains the shared key information.</span></span> <span data-ttu-id="94459-206">只有在驗證和加密配對需要 WEP 或 PSK 金鑰時，才需要這個元素。</span><span class="sxs-lookup"><span data-stu-id="94459-206">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="94459-207">**Ssid**</span><span class="sxs-lookup"><span data-stu-id="94459-207">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)                         |                                                                   | <span data-ttu-id="94459-208">指定無線區域網路的 SSID。</span><span class="sxs-lookup"><span data-stu-id="94459-208">Specifies the SSID of a wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="94459-209">**SSIDConfig**</span><span class="sxs-lookup"><span data-stu-id="94459-209">**SSIDConfig**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)            |                                                                   | <span data-ttu-id="94459-210">包含一或多個 Ssid 以及其他一般設定。</span><span class="sxs-lookup"><span data-stu-id="94459-210">Contains one or more SSIDs along with other common settings.</span></span> <br/> <span data-ttu-id="94459-211">設定檔可以有多個 [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) 元素，且每個 [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) 元素都可以有多個 [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="94459-211">A profile can have multiple [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) elements and each [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element can have multiple [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) elements.</span></span> <span data-ttu-id="94459-212">不過，Windows 只會考慮 [**WLANProfile**](wlan-profileschema-wlanprofile-element.md)專案中的第一個 [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)元素。</span><span class="sxs-lookup"><span data-stu-id="94459-212">However, Windows only ever considers the first [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element in a [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span><br/> <span data-ttu-id="94459-213">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 設定檔中最多隻能出現一個 [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)元素。</span><span class="sxs-lookup"><span data-stu-id="94459-213">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** At most one [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element can appear in a profile.</span></span><br/> |
| [<span data-ttu-id="94459-214">**類型**</span><span class="sxs-lookup"><span data-stu-id="94459-214">**type**</span></span>](wlan-profileschema-type-ouiheader-element.md)                          |                                                                   | <span data-ttu-id="94459-215">包含1個位元組的 **hexBinary** ，用來區分 nic 的相同 IHV。</span><span class="sxs-lookup"><span data-stu-id="94459-215">Contains a 1 byte **hexBinary** that is used to differentiate NICs by the same IHV.</span></span><br/> <span data-ttu-id="94459-216">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="94459-216">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="94459-217">**useMSOneX**</span><span class="sxs-lookup"><span data-stu-id="94459-217">**useMSOneX**</span></span>](wlan-profileschema-usemsonex-ihv-element.md)                      | [<span data-ttu-id="94459-218">boolean</span><span class="sxs-lookup"><span data-stu-id="94459-218">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="94459-219">指定 IHV 安全性元件所使用之 802.1 X 安全性設定的來源。</span><span class="sxs-lookup"><span data-stu-id="94459-219">Specifies the origin of 802.1X security settings used by an IHV security component.</span></span> <span data-ttu-id="94459-220">當 [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) 為 true 時，IHV 安全性元件會使用 Microsoft 定義的 802.1 x 設定。</span><span class="sxs-lookup"><span data-stu-id="94459-220">When [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) is true, IHV security components use Microsoft-defined 802.1X settings.</span></span> <span data-ttu-id="94459-221">當 **useMSOneX** 為 false 時，IHV 安全性元件會使用廠商提供的 802.1 x 設定。</span><span class="sxs-lookup"><span data-stu-id="94459-221">When **useMSOneX** is false, IHV security components use vendor-supplied 802.1X settings.</span></span> <span data-ttu-id="94459-222">依預設， **useMSOneX** 為 false。</span><span class="sxs-lookup"><span data-stu-id="94459-222">By default, **useMSOneX** is false.</span></span> <span data-ttu-id="94459-223">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="94459-223">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="94459-224">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="94459-224">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="94459-225">boolean</span><span class="sxs-lookup"><span data-stu-id="94459-225">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="94459-226">指出是否使用 802.1 X。</span><span class="sxs-lookup"><span data-stu-id="94459-226">Indicates whether 802.1X is used.</span></span> <span data-ttu-id="94459-227">此旗標是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="94459-227">This flag is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="94459-228">備註</span><span class="sxs-lookup"><span data-stu-id="94459-228">Remarks</span></span>

<span data-ttu-id="94459-229">WLANProfile 元素的大部分子項目都在 `https://www.microsoft.com/networking/WLAN/profile/v1` 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="94459-229">Most child elements of the WLANProfile element are in the `https://www.microsoft.com/networking/WLAN/profile/v1` namespace.</span></span> <span data-ttu-id="94459-230">有兩個例外狀況： [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) 元素位於 `https://www.microsoft.com/networking/WLAN/profile/v2` 命名空間中，而 [**OneX**](onexschema-onex-element.md) 元素位於 `https://www.microsoft.com/networking/OneX/v1` 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="94459-230">There are two exceptions: the [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element is in the `https://www.microsoft.com/networking/WLAN/profile/v2` namespace and the [**OneX**](onexschema-onex-element.md) element is in the `https://www.microsoft.com/networking/OneX/v1` namespace.</span></span>

<span data-ttu-id="94459-231">[**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md)元素可以插入做為 [**authEncryption**](wlan-profileschema-authencryption-security-element.md)元素的子系。</span><span class="sxs-lookup"><span data-stu-id="94459-231">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span> <span data-ttu-id="94459-232">您可以將 [**OneX**](onexschema-onex-element.md) 元素插入為 [**安全性 (.msm)**](wlan-profileschema-security-msm-element.md) 元素的子系。</span><span class="sxs-lookup"><span data-stu-id="94459-232">The [**OneX**](onexschema-onex-element.md) element can be inserted as a child of the [**security (MSM)**](wlan-profileschema-security-msm-element.md) element.</span></span>

<span data-ttu-id="94459-233">若要查看類似樹狀結構中子專案的清單，請參閱 [WLAN \_ 設定檔架構元素](wlan-profileschema-elements.md)。</span><span class="sxs-lookup"><span data-stu-id="94459-233">To view the list of child elements in a tree-like structure, see [WLAN\_profile Schema Elements](wlan-profileschema-elements.md).</span></span>

## <a name="examples"></a><span data-ttu-id="94459-234">範例</span><span class="sxs-lookup"><span data-stu-id="94459-234">Examples</span></span>

<span data-ttu-id="94459-235">若要查看範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="94459-235">To view sample profiles, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94459-236">規格需求</span><span class="sxs-lookup"><span data-stu-id="94459-236">Requirements</span></span>



| <span data-ttu-id="94459-237">需求</span><span class="sxs-lookup"><span data-stu-id="94459-237">Requirement</span></span> | <span data-ttu-id="94459-238">值</span><span class="sxs-lookup"><span data-stu-id="94459-238">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="94459-239">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="94459-239">Minimum supported client</span></span><br/> | <span data-ttu-id="94459-240">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94459-240">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="94459-241">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="94459-241">Minimum supported server</span></span><br/> | <span data-ttu-id="94459-242">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94459-242">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="94459-243">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="94459-243">Redistributable</span></span><br/>          | <span data-ttu-id="94459-244">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="94459-244">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="94459-245">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94459-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94459-246">無線設定檔範例</span><span class="sxs-lookup"><span data-stu-id="94459-246">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 
