---
description: 包含各種安全性設定。
ms.assetid: 1d912fb1-8fb4-4761-8991-5a50ffb0399e
title: '安全性 (.MSM) 元素 (LAN_policy)  (WLAN) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f6ea42a83d39c328db88e992555e5d593cc778b6
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/26/2021
ms.locfileid: "106996332"
---
# <a name="security-msm-element-lan_policy-for-wlan"></a><span data-ttu-id="9ce34-103">適用于 WLAN 的安全性 (.MSM) 元素 (LAN_policy) </span><span class="sxs-lookup"><span data-stu-id="9ce34-103">Security (MSM) Element (LAN_policy) for WLAN</span></span>

<span data-ttu-id="9ce34-104">安全性 (.MSM) 元素包含各種安全性設定。</span><span class="sxs-lookup"><span data-stu-id="9ce34-104">The security (MSM) element contains various security settings.</span></span>

``` syntax
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
```

<span data-ttu-id="9ce34-105">元素是由 [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) 元素定義。</span><span class="sxs-lookup"><span data-stu-id="9ce34-105">The element is defined by the [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9ce34-106">子元素</span><span class="sxs-lookup"><span data-stu-id="9ce34-106">Child elements</span></span>



| <span data-ttu-id="9ce34-107">元素</span><span class="sxs-lookup"><span data-stu-id="9ce34-107">Element</span></span>                                                                            | <span data-ttu-id="9ce34-108">類型</span><span class="sxs-lookup"><span data-stu-id="9ce34-108">Type</span></span>                                                              | <span data-ttu-id="9ce34-109">Description</span><span class="sxs-lookup"><span data-stu-id="9ce34-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ce34-110">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="9ce34-110">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)       |                                                                   | <span data-ttu-id="9ce34-111">指定要用於此設定檔的驗證和加密組。</span><span class="sxs-lookup"><span data-stu-id="9ce34-111">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="9ce34-112">**認證**</span><span class="sxs-lookup"><span data-stu-id="9ce34-112">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="9ce34-113">指定要用於此設定檔的驗證和加密組。</span><span class="sxs-lookup"><span data-stu-id="9ce34-113">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="9ce34-114">**加密**</span><span class="sxs-lookup"><span data-stu-id="9ce34-114">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="9ce34-115">設定用來連接到無線區域網路的資料加密。</span><span class="sxs-lookup"><span data-stu-id="9ce34-115">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="9ce34-116">**keyIndex**</span><span class="sxs-lookup"><span data-stu-id="9ce34-116">**keyIndex**</span></span>](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | <span data-ttu-id="9ce34-117">指定必須使用哪一個金鑰索引來加密無線流量。</span><span class="sxs-lookup"><span data-stu-id="9ce34-117">Specifies which key index must be used to encrypt wireless traffic.</span></span> <span data-ttu-id="9ce34-118">只有當 keyType 設定為 networkKey 時，才會使用這個。</span><span class="sxs-lookup"><span data-stu-id="9ce34-118">This is only used when keyType is set to networkKey.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="9ce34-119">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="9ce34-119">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)            | [<span data-ttu-id="9ce34-120">string</span><span class="sxs-lookup"><span data-stu-id="9ce34-120">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="9ce34-121">包含網路金鑰或複雜密碼。</span><span class="sxs-lookup"><span data-stu-id="9ce34-121">Contains the network key or passphrase.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="9ce34-122">**keyType**</span><span class="sxs-lookup"><span data-stu-id="9ce34-122">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | <span data-ttu-id="9ce34-123">索引鍵的類型。</span><span class="sxs-lookup"><span data-stu-id="9ce34-123">Type of key.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="9ce34-124">**PMKCacheMode**</span><span class="sxs-lookup"><span data-stu-id="9ce34-124">**PMKCacheMode**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | <span data-ttu-id="9ce34-125">指出是否會使用 PMK 快取。</span><span class="sxs-lookup"><span data-stu-id="9ce34-125">Indicates whether PMK caching will be used.</span></span> <span data-ttu-id="9ce34-126">此元素只對 WPA2 定義的網路有效。</span><span class="sxs-lookup"><span data-stu-id="9ce34-126">This element is valid only for WPA2-defined networks.</span></span><br/> <span data-ttu-id="9ce34-127">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="9ce34-127">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="9ce34-128">**PMKCacheSize**</span><span class="sxs-lookup"><span data-stu-id="9ce34-128">**PMKCacheSize**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | <span data-ttu-id="9ce34-129">指定用戶端上 OMK 快取中的專案數。</span><span class="sxs-lookup"><span data-stu-id="9ce34-129">Specifies the number of entries in the OMK cache on the client.</span></span> <span data-ttu-id="9ce34-130">此元素只適用于將 PMKCache 模式設定為啟用的 WPA2 定義網路。</span><span class="sxs-lookup"><span data-stu-id="9ce34-130">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="9ce34-131">如果已啟用 PMKCache 模式，且此元素不存在，則快取的大小會預設為128個專案。</span><span class="sxs-lookup"><span data-stu-id="9ce34-131">If PMKCache mode is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span><br/> <span data-ttu-id="9ce34-132">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="9ce34-132">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                   |
| [<span data-ttu-id="9ce34-133">**PMKCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="9ce34-133">**PMKCacheTTL**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | <span data-ttu-id="9ce34-134">指出將保留 PMK 快取的時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ce34-134">Indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="9ce34-135">此元素只適用于將 PMKCache 模式設定為啟用的 WPA2 定義網路。</span><span class="sxs-lookup"><span data-stu-id="9ce34-135">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span><br/> <span data-ttu-id="9ce34-136">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="9ce34-136">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="9ce34-137">**preAuthMode**</span><span class="sxs-lookup"><span data-stu-id="9ce34-137">**preAuthMode**</span></span>](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | <span data-ttu-id="9ce34-138">判斷用戶端是否會使用預先驗證。</span><span class="sxs-lookup"><span data-stu-id="9ce34-138">Determines if pre-authentication will be used by the client.</span></span> <span data-ttu-id="9ce34-139">預先驗證可讓 WPA2 安全快速漫遊。</span><span class="sxs-lookup"><span data-stu-id="9ce34-139">Pre-authentication enables WPA2 secure fast roaming.</span></span> <span data-ttu-id="9ce34-140">此元素只適用于將 PMKCache 模式設定為啟用的 WPA2 定義網路。</span><span class="sxs-lookup"><span data-stu-id="9ce34-140">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="9ce34-141">如果已啟用 PMKCache 模式，且此元素不存在，則預設值為停用。</span><span class="sxs-lookup"><span data-stu-id="9ce34-141">If PMKCache mode is enabled, and this element is absent, the default value is disabled.</span></span><br/> <span data-ttu-id="9ce34-142">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="9ce34-142">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/> |
| [<span data-ttu-id="9ce34-143">**preAuthThrottle**</span><span class="sxs-lookup"><span data-stu-id="9ce34-143">**preAuthThrottle**</span></span>](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | <span data-ttu-id="9ce34-144">指出 preauthenticating 至相鄰 Ap 時的嘗試次數。</span><span class="sxs-lookup"><span data-stu-id="9ce34-144">Indicates the number of tries when preauthenticating to neighboring APs.</span></span> <span data-ttu-id="9ce34-145">此元素只適用于將 PMKCache 模式設定為啟用的 WPA2 定義網路。</span><span class="sxs-lookup"><span data-stu-id="9ce34-145">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="9ce34-146">如果已啟用 PMKCache 模式，且此元素不存在，則嘗試次數會預設為3。</span><span class="sxs-lookup"><span data-stu-id="9ce34-146">If PMKCache mode is enabled, and this element is absent, the number of tries defaults to 3.</span></span><br/> <span data-ttu-id="9ce34-147">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="9ce34-147">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="9ce34-148">**受保護**</span><span class="sxs-lookup"><span data-stu-id="9ce34-148">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)                | [<span data-ttu-id="9ce34-149">boolean</span><span class="sxs-lookup"><span data-stu-id="9ce34-149">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="9ce34-150">指出金鑰是否已加密。</span><span class="sxs-lookup"><span data-stu-id="9ce34-150">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="9ce34-151">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 這個元素的值必須為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="9ce34-151">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of **FALSE**.</span></span><br/>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="9ce34-152">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="9ce34-152">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | <span data-ttu-id="9ce34-153">包含共用金鑰資訊。</span><span class="sxs-lookup"><span data-stu-id="9ce34-153">Contains the shared key information.</span></span> <span data-ttu-id="9ce34-154">只有在驗證和加密配對需要 WEP 或 PSK 金鑰時，才需要這個元素。</span><span class="sxs-lookup"><span data-stu-id="9ce34-154">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span><br/>                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="9ce34-155">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="9ce34-155">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="9ce34-156">boolean</span><span class="sxs-lookup"><span data-stu-id="9ce34-156">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="9ce34-157">指出是否使用 802.1 X。</span><span class="sxs-lookup"><span data-stu-id="9ce34-157">Indicates whether 802.1X is used.</span></span> <span data-ttu-id="9ce34-158">此旗標是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="9ce34-158">This flag is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="9ce34-159">備註</span><span class="sxs-lookup"><span data-stu-id="9ce34-159">Remarks</span></span>

<span data-ttu-id="9ce34-160">[**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md)元素可以插入做為 [**authEncryption**](wlan-profileschema-authencryption-security-element.md)元素的子系。</span><span class="sxs-lookup"><span data-stu-id="9ce34-160">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span> <span data-ttu-id="9ce34-161">您可以將 [**OneX**](onexschema-onex-element.md) 元素插入為 **安全性 (.msm)** 元素的子系。</span><span class="sxs-lookup"><span data-stu-id="9ce34-161">The [**OneX**](onexschema-onex-element.md) element can be inserted as a child of the **security (MSM)** element.</span></span>

## <a name="examples"></a><span data-ttu-id="9ce34-162">範例</span><span class="sxs-lookup"><span data-stu-id="9ce34-162">Examples</span></span>

<span data-ttu-id="9ce34-163">若要查看使用 **安全性** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="9ce34-163">To view sample profiles that use the **security** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ce34-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ce34-164">Requirements</span></span>



| <span data-ttu-id="9ce34-165">需求</span><span class="sxs-lookup"><span data-stu-id="9ce34-165">Requirement</span></span> | <span data-ttu-id="9ce34-166">值</span><span class="sxs-lookup"><span data-stu-id="9ce34-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="9ce34-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9ce34-167">Minimum supported client</span></span><br/> | <span data-ttu-id="9ce34-168">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ce34-168">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9ce34-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9ce34-169">Minimum supported server</span></span><br/> | <span data-ttu-id="9ce34-170">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ce34-170">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="9ce34-171">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="9ce34-171">Redistributable</span></span><br/>          | <span data-ttu-id="9ce34-172">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="9ce34-172">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="9ce34-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ce34-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ce34-174">無線設定檔範例</span><span class="sxs-lookup"><span data-stu-id="9ce34-174">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

<span data-ttu-id="9ce34-175">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="9ce34-175">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="9ce34-176">**MSM**</span><span class="sxs-lookup"><span data-stu-id="9ce34-176">**MSM**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="9ce34-177">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="9ce34-177">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="9ce34-178">**MSM (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="9ce34-178">**MSM (WLANProfile)**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 
