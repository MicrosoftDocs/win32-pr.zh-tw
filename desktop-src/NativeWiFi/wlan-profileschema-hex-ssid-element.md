---
description: 包含十六進位格式的無線區域網路 SSID。
ms.assetid: 6c49a3e6-f167-408b-a96f-5b6032108f34
title: hex (SSID) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- hex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6bc214f50788fdc6965a1ce429c5c2919846cf72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967159"
---
# <a name="hex-ssid-element"></a><span data-ttu-id="5b015-103">hex (SSID) 元素</span><span class="sxs-lookup"><span data-stu-id="5b015-103">hex (SSID) Element</span></span>

<span data-ttu-id="5b015-104">Hex (SSID) 元素包含十六進位格式的無線區域網路 SSID。</span><span class="sxs-lookup"><span data-stu-id="5b015-104">The hex (SSID) element contains the SSID of a wireless LAN in hexadecimal format.</span></span>

``` syntax
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
```

<span data-ttu-id="5b015-105">元素是由 [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="5b015-105">The element is defined by the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b015-106">備註</span><span class="sxs-lookup"><span data-stu-id="5b015-106">Remarks</span></span>

<span data-ttu-id="5b015-107">雖然 **hex** 和 [**name**](wlan-profileschema-name-ssid-element.md) 元素是選擇性的，但至少一個 **hex** 或 [**name**](wlan-profileschema-name-ssid-element.md) 元素必須顯示為 [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) 元素的子系。</span><span class="sxs-lookup"><span data-stu-id="5b015-107">Although the **hex** and [**name**](wlan-profileschema-name-ssid-element.md) elements are optional, at least one **hex** or [**name**](wlan-profileschema-name-ssid-element.md) element must appear as a child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

<span data-ttu-id="5b015-108">當設定檔資訊轉換成 SSID 時，如果有 (，則會將 **hex** 元素轉換成 ssid 如果) 存在，則會忽略 [**name**](wlan-profileschema-name-ssid-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="5b015-108">When profile information is converted to an SSID, the **hex** element is converted to the SSID (if present) and the [**name**](wlan-profileschema-name-ssid-element.md) element is ignored .</span></span> <span data-ttu-id="5b015-109">如果 **hex** 元素不存在，則會將 [**name**](wlan-profileschema-name-ssid-element.md) 元素轉換為使用 Unicode 轉換的 SSID。</span><span class="sxs-lookup"><span data-stu-id="5b015-109">If the **hex** element is not present, the [**name**](wlan-profileschema-name-ssid-element.md) element is converted to an SSID using Unicode to ASCII conversion.</span></span>

<span data-ttu-id="5b015-110">當 SSID 儲存在設定檔中時，一律會產生 **hex** 元素。</span><span class="sxs-lookup"><span data-stu-id="5b015-110">When an SSID is stored in a profile, the **hex** element is always generated.</span></span> <span data-ttu-id="5b015-111">只有當 SSID 和 XML 設定檔產生的 ASCII 與 Unicode 轉換都成功時，才會產生 [**name**](wlan-profileschema-name-ssid-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="5b015-111">The [**name**](wlan-profileschema-name-ssid-element.md) element is only generated if the both the ASCII to Unicode conversion of the SSID and the XML profile generation are successful.</span></span> <span data-ttu-id="5b015-112">當原始 SSID 的某些資訊轉換成 [**名稱**](wlan-profileschema-name-ssid-element.md)時，可能會遺失。</span><span class="sxs-lookup"><span data-stu-id="5b015-112">Some information from the original SSID may be lost when it is converted to a [**name**](wlan-profileschema-name-ssid-element.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5b015-113">範例</span><span class="sxs-lookup"><span data-stu-id="5b015-113">Examples</span></span>

<span data-ttu-id="5b015-114">若要查看使用 **hex** 元素的範例設定檔，請參閱 [FIPS 設定檔範例](fips-profile-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="5b015-114">To view a sample profile that uses the **hex** element, see [FIPS Profile Sample](fips-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b015-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b015-115">Requirements</span></span>



| <span data-ttu-id="5b015-116">需求</span><span class="sxs-lookup"><span data-stu-id="5b015-116">Requirement</span></span> | <span data-ttu-id="5b015-117">值</span><span class="sxs-lookup"><span data-stu-id="5b015-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="5b015-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b015-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5b015-119">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b015-119">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5b015-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b015-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5b015-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b015-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="5b015-122">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="5b015-122">Redistributable</span></span><br/>          | <span data-ttu-id="5b015-123">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="5b015-123">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="5b015-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b015-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="5b015-125">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="5b015-125">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5b015-126">**Ssid**</span><span class="sxs-lookup"><span data-stu-id="5b015-126">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

<span data-ttu-id="5b015-127">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="5b015-127">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5b015-128">**SSID (SSIDConfig)**</span><span class="sxs-lookup"><span data-stu-id="5b015-128">**SSID (SSIDConfig)**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




