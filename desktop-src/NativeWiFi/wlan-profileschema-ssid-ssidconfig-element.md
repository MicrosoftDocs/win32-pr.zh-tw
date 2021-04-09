---
description: 包含無線區域網路的 SSID。
ms.assetid: fb3466c4-a586-424b-96e2-ba287c99a1d9
title: SSID (SSIDConfig) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSID
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 644a4afbd10fbfff870007befda964fc9babd593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849915"
---
# <a name="ssid-ssidconfig-element"></a><span data-ttu-id="89a1e-103">SSID (SSIDConfig) 元素</span><span class="sxs-lookup"><span data-stu-id="89a1e-103">SSID (SSIDConfig) Element</span></span>

<span data-ttu-id="89a1e-104">SSID (SSIDConfig) 元素包含無線區域網路的 SSID。</span><span class="sxs-lookup"><span data-stu-id="89a1e-104">The SSID (SSIDConfig) element contains an SSID for a wireless LAN.</span></span>

<span data-ttu-id="89a1e-105">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 設定檔中最多隻能出現一個 **SSID** 元素。</span><span class="sxs-lookup"><span data-stu-id="89a1e-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** At most one **SSID** element can appear in a profile.</span></span>

``` syntax
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
```

<span data-ttu-id="89a1e-106">**SSID** 元素是由 [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="89a1e-106">The **SSID** element is defined by the [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="89a1e-107">子元素</span><span class="sxs-lookup"><span data-stu-id="89a1e-107">Child elements</span></span>



| <span data-ttu-id="89a1e-108">元素</span><span class="sxs-lookup"><span data-stu-id="89a1e-108">Element</span></span>                                              | <span data-ttu-id="89a1e-109">類型</span><span class="sxs-lookup"><span data-stu-id="89a1e-109">Type</span></span> | <span data-ttu-id="89a1e-110">Description</span><span class="sxs-lookup"><span data-stu-id="89a1e-110">Description</span></span>                                                           |
|------------------------------------------------------|------|-----------------------------------------------------------------------|
| [<span data-ttu-id="89a1e-111">**hex**</span><span class="sxs-lookup"><span data-stu-id="89a1e-111">**hex**</span></span>](wlan-profileschema-hex-ssid-element.md)   |      | <span data-ttu-id="89a1e-112">包含十六進位格式的無線區域網路 SSID。</span><span class="sxs-lookup"><span data-stu-id="89a1e-112">Contains the SSID of a wireless LAN in hexadecimal format.</span></span><br/> |
| [<span data-ttu-id="89a1e-113">**名字**</span><span class="sxs-lookup"><span data-stu-id="89a1e-113">**name**</span></span>](wlan-profileschema-name-ssid-element.md) |      | <span data-ttu-id="89a1e-114">包含無線區域網路的 SSID。</span><span class="sxs-lookup"><span data-stu-id="89a1e-114">Contains the SSID for a wireless LAN.</span></span><br/>                      |



## <a name="remarks"></a><span data-ttu-id="89a1e-115">備註</span><span class="sxs-lookup"><span data-stu-id="89a1e-115">Remarks</span></span>

<span data-ttu-id="89a1e-116">雖然 [**hex**](wlan-profileschema-hex-ssid-element.md) 和 [**name**](wlan-profileschema-name-ssid-element.md) 元素是選擇性的，但至少一個 **hex** 或 [**name**](wlan-profileschema-name-ssid-element.md) 元素必須顯示為 **SSID** 元素的子系。</span><span class="sxs-lookup"><span data-stu-id="89a1e-116">Although the [**hex**](wlan-profileschema-hex-ssid-element.md) and [**name**](wlan-profileschema-name-ssid-element.md) elements are optional, at least one **hex** or [**name**](wlan-profileschema-name-ssid-element.md) element must appear as a child of the **SSID** element.</span></span>

<span data-ttu-id="89a1e-117">當設定檔資訊轉換成 SSID 時，如果有 (，則會將 [**hex**](wlan-profileschema-hex-ssid-element.md) 元素轉換成 ssid 如果) 存在，則會忽略 [**name**](wlan-profileschema-name-ssid-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="89a1e-117">When profile information is converted to an SSID, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is converted to the SSID (if present) and the [**name**](wlan-profileschema-name-ssid-element.md) element is ignored.</span></span> <span data-ttu-id="89a1e-118">如果 **hex** 元素不存在，則會將 [**name**](wlan-profileschema-name-ssid-element.md) 元素轉換為使用 Unicode 轉換的 SSID。</span><span class="sxs-lookup"><span data-stu-id="89a1e-118">If the **hex** element is not present, the [**name**](wlan-profileschema-name-ssid-element.md) element is converted to an SSID using Unicode to ASCII conversion.</span></span>

<span data-ttu-id="89a1e-119">當 SSID 儲存在設定檔中時，一律會產生 [**hex**](wlan-profileschema-hex-ssid-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="89a1e-119">When an SSID is stored in a profile, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is always generated.</span></span> <span data-ttu-id="89a1e-120">只有當 SSID 和 XML 設定檔產生的 ASCII 與 Unicode 轉換都成功時，才會產生 [**name**](wlan-profileschema-name-ssid-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="89a1e-120">The [**name**](wlan-profileschema-name-ssid-element.md) element is only generated if the both the ASCII to Unicode conversion of the SSID and the XML profile generation are successful.</span></span> <span data-ttu-id="89a1e-121">當原始 SSID 的某些資訊轉換成 [**名稱**](wlan-profileschema-name-ssid-element.md)時，可能會遺失。</span><span class="sxs-lookup"><span data-stu-id="89a1e-121">Some information from the original SSID may be lost when it is converted to a [**name**](wlan-profileschema-name-ssid-element.md).</span></span>

## <a name="examples"></a><span data-ttu-id="89a1e-122">範例</span><span class="sxs-lookup"><span data-stu-id="89a1e-122">Examples</span></span>

<span data-ttu-id="89a1e-123">若要查看使用 **SSID** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="89a1e-123">To view sample profiles that use the **SSID** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="89a1e-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="89a1e-124">Requirements</span></span>



| <span data-ttu-id="89a1e-125">需求</span><span class="sxs-lookup"><span data-stu-id="89a1e-125">Requirement</span></span> | <span data-ttu-id="89a1e-126">值</span><span class="sxs-lookup"><span data-stu-id="89a1e-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="89a1e-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89a1e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="89a1e-128">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89a1e-128">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="89a1e-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89a1e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="89a1e-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89a1e-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="89a1e-131">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="89a1e-131">Redistributable</span></span><br/>          | <span data-ttu-id="89a1e-132">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="89a1e-132">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="89a1e-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89a1e-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="89a1e-134">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="89a1e-134">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="89a1e-135">**SSIDConfig**</span><span class="sxs-lookup"><span data-stu-id="89a1e-135">**SSIDConfig**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="89a1e-136">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="89a1e-136">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="89a1e-137">**SSIDConfig (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="89a1e-137">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




