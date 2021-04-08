---
description: 包含無線區域網路的 SSID。
ms.assetid: ed23ccd0-9b44-4c97-a5ed-93e86632b819
title: " (SSID 的名稱) 元素"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: dbb1301de2a2d70edf8c61de002c28e48b00a5d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851163"
---
# <a name="name-ssid-element"></a><span data-ttu-id="6e199-103"> (SSID 的名稱) 元素</span><span class="sxs-lookup"><span data-stu-id="6e199-103">name (SSID) Element</span></span>

<span data-ttu-id="6e199-104"> (SSID 的名稱) 元素包含無線區域網路的 SSID。</span><span class="sxs-lookup"><span data-stu-id="6e199-104">The name (SSID) element contains the SSID of a wireless LAN.</span></span>

``` syntax
<xs:element name="name">
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
```

<span data-ttu-id="6e199-105">元素是由 [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="6e199-105">The element is defined by the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e199-106">備註</span><span class="sxs-lookup"><span data-stu-id="6e199-106">Remarks</span></span>

<span data-ttu-id="6e199-107">名稱會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="6e199-107">Names are case-sensitive.</span></span>

<span data-ttu-id="6e199-108">雖然 [**hex**](wlan-profileschema-hex-ssid-element.md) 和 **name** 元素是選擇性的，但至少一個 **hex** 或 **name** 元素必須顯示為 [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) 元素的子系。</span><span class="sxs-lookup"><span data-stu-id="6e199-108">Although the [**hex**](wlan-profileschema-hex-ssid-element.md) and **name** elements are optional, at least one **hex** or **name** element must appear as a child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

<span data-ttu-id="6e199-109">當設定檔資訊轉換成 SSID 時，如果有 (，則會將 [**hex**](wlan-profileschema-hex-ssid-element.md) 元素轉換成 ssid 如果) 存在，則會忽略 **name** 元素。</span><span class="sxs-lookup"><span data-stu-id="6e199-109">When profile information is converted to an SSID, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is converted to the SSID (if present) and the **name** element is ignored.</span></span> <span data-ttu-id="6e199-110">如果 **hex** 元素不存在，則會將 **name** 元素轉換為使用 Unicode 轉換的 SSID。</span><span class="sxs-lookup"><span data-stu-id="6e199-110">If the **hex** element is not present, the **name** element is converted to an SSID using Unicode to ASCII conversion.</span></span>

<span data-ttu-id="6e199-111">當 SSID 儲存在設定檔中時，一律會產生 [**hex**](wlan-profileschema-hex-ssid-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="6e199-111">When an SSID is stored in a profile, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is always generated.</span></span> <span data-ttu-id="6e199-112">只有當 SSID 和 XML 設定檔產生的 ASCII 與 Unicode 轉換都成功時，才會產生 **name** 元素。</span><span class="sxs-lookup"><span data-stu-id="6e199-112">The **name** element is only generated if the both the ASCII to Unicode conversion of the SSID and the XML profile generation are successful.</span></span> <span data-ttu-id="6e199-113">當原始 SSID 的某些資訊轉換成 **名稱** 時，可能會遺失。</span><span class="sxs-lookup"><span data-stu-id="6e199-113">Some information from the original SSID may be lost when it is converted to a **name**.</span></span>

<span data-ttu-id="6e199-114">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** XML escape 字元（例如 &）不會顯示。</span><span class="sxs-lookup"><span data-stu-id="6e199-114">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** XML escape characters, such as &, are not displayed.</span></span> <span data-ttu-id="6e199-115">針對 windows XP 加裝 SP3 和適用于 Windows XP SP2 的無線區域網路 API 所部署的設定檔，請避免在 SSID 名稱中使用 XML escape 字元。</span><span class="sxs-lookup"><span data-stu-id="6e199-115">Avoid using XML escape characters in SSID names for profiles deployed on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2.</span></span>

## <a name="examples"></a><span data-ttu-id="6e199-116">範例</span><span class="sxs-lookup"><span data-stu-id="6e199-116">Examples</span></span>

<span data-ttu-id="6e199-117">若要查看使用 **name** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="6e199-117">To view sample profiles that use the **name** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e199-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e199-118">Requirements</span></span>



| <span data-ttu-id="6e199-119">需求</span><span class="sxs-lookup"><span data-stu-id="6e199-119">Requirement</span></span> | <span data-ttu-id="6e199-120">值</span><span class="sxs-lookup"><span data-stu-id="6e199-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6e199-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e199-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6e199-122">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e199-122">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6e199-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e199-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6e199-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e199-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="6e199-125">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="6e199-125">Redistributable</span></span><br/>          | <span data-ttu-id="6e199-126">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="6e199-126">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="6e199-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e199-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="6e199-128">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="6e199-128">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6e199-129">**Ssid**</span><span class="sxs-lookup"><span data-stu-id="6e199-129">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

<span data-ttu-id="6e199-130">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="6e199-130">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6e199-131">**SSID (SSIDConfig)**</span><span class="sxs-lookup"><span data-stu-id="6e199-131">**SSID (SSIDConfig)**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




