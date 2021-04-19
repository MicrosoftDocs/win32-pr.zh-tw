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
ms.openlocfilehash: b2e1ffdc5ad27524d3d2fc5b37b3a060a90c7575
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979287"
---
# <a name="msm-wlanprofile-element"></a><span data-ttu-id="85d82-103">MSM (WLANProfile) 元素</span><span class="sxs-lookup"><span data-stu-id="85d82-103">MSM (WLANProfile) Element</span></span>

<span data-ttu-id="85d82-104">MSM (WLANProfile) 元素包含各種不同的媒體特定模組 (MSM) 設定。</span><span class="sxs-lookup"><span data-stu-id="85d82-104">The MSM (WLANProfile) element contains various media-specific module (MSM) settings.</span></span>

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

<span data-ttu-id="85d82-105">元素是由 [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="85d82-105">The element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="85d82-106">子元素</span><span class="sxs-lookup"><span data-stu-id="85d82-106">Child elements</span></span>



| <span data-ttu-id="85d82-107">元素</span><span class="sxs-lookup"><span data-stu-id="85d82-107">Element</span></span>                                                                            | <span data-ttu-id="85d82-108">類型</span><span class="sxs-lookup"><span data-stu-id="85d82-108">Type</span></span>                                                              | <span data-ttu-id="85d82-109">Description</span><span class="sxs-lookup"><span data-stu-id="85d82-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85d82-110">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="85d82-110">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)       |                                                                   | <span data-ttu-id="85d82-111">指定要用於此設定檔的驗證和加密組。</span><span class="sxs-lookup"><span data-stu-id="85d82-111">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="85d82-112">**認證**</span><span class="sxs-lookup"><span data-stu-id="85d82-112">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="85d82-113">指定要用於此設定檔的驗證和加密組。</span><span class="sxs-lookup"><span data-stu-id="85d82-113">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="85d82-114">**連接**</span><span class="sxs-lookup"><span data-stu-id="85d82-114">**connectivity**</span></span>](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | <span data-ttu-id="85d82-115">包含各種連接設定。</span><span class="sxs-lookup"><span data-stu-id="85d82-115">Contains various connectivity settings.</span></span> <span data-ttu-id="85d82-116">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="85d82-116">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="85d82-117">**加密**</span><span class="sxs-lookup"><span data-stu-id="85d82-117">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="85d82-118">設定用來連接到無線區域網路的資料加密。</span><span class="sxs-lookup"><span data-stu-id="85d82-118">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="85d82-119">**keyIndex**</span><span class="sxs-lookup"><span data-stu-id="85d82-119">**keyIndex**</span></span>](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | <span data-ttu-id="85d82-120">指定必須使用哪一個金鑰索引來加密無線流量。</span><span class="sxs-lookup"><span data-stu-id="85d82-120">Specifies which key index must be used to encrypt wireless traffic.</span></span> <span data-ttu-id="85d82-121">只有當 keyType 設定為 networkKey 時，才會使用這個。</span><span class="sxs-lookup"><span data-stu-id="85d82-121">This is only used when keyType is set to networkKey.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="85d82-122">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="85d82-122">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)            | [<span data-ttu-id="85d82-123">string</span><span class="sxs-lookup"><span data-stu-id="85d82-123">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="85d82-124">包含網路金鑰或複雜密碼。</span><span class="sxs-lookup"><span data-stu-id="85d82-124">Contains the network key or passphrase.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="85d82-125">**keyType**</span><span class="sxs-lookup"><span data-stu-id="85d82-125">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | <span data-ttu-id="85d82-126">索引鍵的類型。</span><span class="sxs-lookup"><span data-stu-id="85d82-126">Type of key.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="85d82-127">**phyType**</span><span class="sxs-lookup"><span data-stu-id="85d82-127">**phyType**</span></span>](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | <span data-ttu-id="85d82-128">指定無線區域網路上所使用的802.11 無線區域網路標準。</span><span class="sxs-lookup"><span data-stu-id="85d82-128">Specifies the 802.11 wireless LAN standard used on the wireless LAN.</span></span> <span data-ttu-id="85d82-129">只有在 Windows Vista SP1 和更新版本的作業系統上，才支援值 "n"。</span><span class="sxs-lookup"><span data-stu-id="85d82-129">The value "n" is only supported on Windows Vista with SP1 and later versions of the operating system.</span></span><br/> <span data-ttu-id="85d82-130">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="85d82-130">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="85d82-131">**PMKCacheMode**</span><span class="sxs-lookup"><span data-stu-id="85d82-131">**PMKCacheMode**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | <span data-ttu-id="85d82-132">指出是否會使用 PMK 快取。</span><span class="sxs-lookup"><span data-stu-id="85d82-132">Indicates whether PMK caching will be used.</span></span> <span data-ttu-id="85d82-133">此元素只對 WPA2 定義的網路有效。</span><span class="sxs-lookup"><span data-stu-id="85d82-133">This element is valid only for WPA2-defined networks.</span></span><br/> <span data-ttu-id="85d82-134">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="85d82-134">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="85d82-135">**PMKCacheSize**</span><span class="sxs-lookup"><span data-stu-id="85d82-135">**PMKCacheSize**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | <span data-ttu-id="85d82-136">指定用戶端上 OMK 快取中的專案數。</span><span class="sxs-lookup"><span data-stu-id="85d82-136">Specifies the number of entries in the OMK cache on the client.</span></span> <span data-ttu-id="85d82-137">此元素只適用于將 PMKCache 模式設定為啟用的 WPA2 定義網路。</span><span class="sxs-lookup"><span data-stu-id="85d82-137">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="85d82-138">如果已啟用 PMKCache 模式，且此元素不存在，則快取的大小會預設為128個專案。</span><span class="sxs-lookup"><span data-stu-id="85d82-138">If PMKCache mode is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span><br/> <span data-ttu-id="85d82-139">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="85d82-139">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                   |
| [<span data-ttu-id="85d82-140">**PMKCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="85d82-140">**PMKCacheTTL**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | <span data-ttu-id="85d82-141">指出將保留 PMK 快取的時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="85d82-141">Indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="85d82-142">此元素只適用于將 PMKCache 模式設定為啟用的 WPA2 定義網路。</span><span class="sxs-lookup"><span data-stu-id="85d82-142">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span><br/> <span data-ttu-id="85d82-143">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="85d82-143">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="85d82-144">**preAuthMode**</span><span class="sxs-lookup"><span data-stu-id="85d82-144">**preAuthMode**</span></span>](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | <span data-ttu-id="85d82-145">判斷用戶端是否會使用預先驗證。</span><span class="sxs-lookup"><span data-stu-id="85d82-145">Determines if pre-authentication will be used by the client.</span></span> <span data-ttu-id="85d82-146">預先驗證可讓 WPA2 安全快速漫遊。</span><span class="sxs-lookup"><span data-stu-id="85d82-146">Pre-authentication enables WPA2 secure fast roaming.</span></span> <span data-ttu-id="85d82-147">此元素只適用于將 PMKCache 模式設定為啟用的 WPA2 定義網路。</span><span class="sxs-lookup"><span data-stu-id="85d82-147">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="85d82-148">如果已啟用 PMKCache 模式，且此元素不存在，則預設值為停用。</span><span class="sxs-lookup"><span data-stu-id="85d82-148">If PMKCache mode is enabled, and this element is absent, the default value is disabled.</span></span><br/> <span data-ttu-id="85d82-149">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="85d82-149">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/> |
| [<span data-ttu-id="85d82-150">**preAuthThrottle**</span><span class="sxs-lookup"><span data-stu-id="85d82-150">**preAuthThrottle**</span></span>](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | <span data-ttu-id="85d82-151">指出 preauthenticating 至相鄰 Ap 時的嘗試次數。</span><span class="sxs-lookup"><span data-stu-id="85d82-151">Indicates the number of tries when preauthenticating to neighboring APs.</span></span> <span data-ttu-id="85d82-152">此元素只適用于將 PMKCache 模式設定為啟用的 WPA2 定義網路。</span><span class="sxs-lookup"><span data-stu-id="85d82-152">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="85d82-153">如果已啟用 PMKCache 模式，且此元素不存在，則嘗試次數會預設為3。</span><span class="sxs-lookup"><span data-stu-id="85d82-153">If PMKCache mode is enabled, and this element is absent, the number of tries defaults to 3.</span></span><br/> <span data-ttu-id="85d82-154">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="85d82-154">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="85d82-155">**受保護**</span><span class="sxs-lookup"><span data-stu-id="85d82-155">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)                | [<span data-ttu-id="85d82-156">boolean</span><span class="sxs-lookup"><span data-stu-id="85d82-156">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="85d82-157">指出金鑰是否已加密。</span><span class="sxs-lookup"><span data-stu-id="85d82-157">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="85d82-158">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 這個元素的值必須為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="85d82-158">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of FALSE.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="85d82-159">**安全**</span><span class="sxs-lookup"><span data-stu-id="85d82-159">**security**</span></span>](wlan-profileschema-security-msm-element.md)                        |                                                                   | <span data-ttu-id="85d82-160">包含各種安全性設定。</span><span class="sxs-lookup"><span data-stu-id="85d82-160">Contains various security settings.</span></span> <span data-ttu-id="85d82-161">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="85d82-161">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="85d82-162">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="85d82-162">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | <span data-ttu-id="85d82-163">包含共用金鑰資訊。</span><span class="sxs-lookup"><span data-stu-id="85d82-163">Contains the shared key information.</span></span> <span data-ttu-id="85d82-164">只有在驗證和加密配對需要 WEP 或 PSK 金鑰時，才需要這個元素。</span><span class="sxs-lookup"><span data-stu-id="85d82-164">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span><br/>                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="85d82-165">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="85d82-165">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="85d82-166">boolean</span><span class="sxs-lookup"><span data-stu-id="85d82-166">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="85d82-167">指出是否使用 802.1 X。</span><span class="sxs-lookup"><span data-stu-id="85d82-167">Indicates whether 802.1X is used.</span></span> <span data-ttu-id="85d82-168">此旗標是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="85d82-168">This flag is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="85d82-169">備註</span><span class="sxs-lookup"><span data-stu-id="85d82-169">Remarks</span></span>

<span data-ttu-id="85d82-170">[**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md)元素可以插入做為 [**authEncryption**](wlan-profileschema-authencryption-security-element.md)元素的子系。</span><span class="sxs-lookup"><span data-stu-id="85d82-170">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span> <span data-ttu-id="85d82-171">您可以將 [**OneX**](onexschema-onex-element.md) 元素插入為 [**安全性 (.msm)**](wlan-profileschema-security-msm-element.md) 元素的子系。</span><span class="sxs-lookup"><span data-stu-id="85d82-171">The [**OneX**](onexschema-onex-element.md) element can be inserted as a child of the [**security (MSM)**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="85d82-172">範例</span><span class="sxs-lookup"><span data-stu-id="85d82-172">Examples</span></span>

<span data-ttu-id="85d82-173">若要查看使用 **MSM** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="85d82-173">To view sample profiles that use the **MSM** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85d82-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="85d82-174">Requirements</span></span>



| <span data-ttu-id="85d82-175">需求</span><span class="sxs-lookup"><span data-stu-id="85d82-175">Requirement</span></span> | <span data-ttu-id="85d82-176">值</span><span class="sxs-lookup"><span data-stu-id="85d82-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="85d82-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85d82-177">Minimum supported client</span></span><br/> | <span data-ttu-id="85d82-178">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85d82-178">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="85d82-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85d82-179">Minimum supported server</span></span><br/> | <span data-ttu-id="85d82-180">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85d82-180">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="85d82-181">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="85d82-181">Redistributable</span></span><br/>          | <span data-ttu-id="85d82-182">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="85d82-182">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="85d82-183">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85d82-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85d82-184">無線設定檔範例</span><span class="sxs-lookup"><span data-stu-id="85d82-184">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

<span data-ttu-id="85d82-185">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="85d82-185">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="85d82-186">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="85d82-186">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="85d82-187">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="85d82-187">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="85d82-188">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="85d82-188">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
