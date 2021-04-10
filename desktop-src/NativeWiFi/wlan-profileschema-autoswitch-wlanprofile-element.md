---
description: 決定當更慣用的網路在範圍內時，自動連線網路的漫遊行為。
ms.assetid: 095dc797-1249-43aa-a8b7-5fa6eaee2a74
title: autoSwitch (WLANProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- autoSwitch
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7ae05b18f58927e05c952edbbfc1b6a6190cec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848405"
---
# <a name="autoswitch-wlanprofile-element"></a><span data-ttu-id="83b2a-103">autoSwitch (WLANProfile) 元素</span><span class="sxs-lookup"><span data-stu-id="83b2a-103">autoSwitch (WLANProfile) Element</span></span>

<span data-ttu-id="83b2a-104">當較慣用的網路在範圍內時，autoSwitch (WLANProfile) 元素會決定自動連線網路的漫遊行為。</span><span class="sxs-lookup"><span data-stu-id="83b2a-104">The autoSwitch (WLANProfile) element determines the roaming behavior of an auto-connected network when a more preferred network is in range.</span></span> <span data-ttu-id="83b2a-105">.</span><span class="sxs-lookup"><span data-stu-id="83b2a-105">.</span></span> <span data-ttu-id="83b2a-106">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="83b2a-106">This element is optional.</span></span>

<span data-ttu-id="83b2a-107">如果 autoSwitch 是 "true"，而 [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) 設定為 "auto"，則當更慣用的網路進入範圍時，就必須嘗試連線到更慣用的網路。</span><span class="sxs-lookup"><span data-stu-id="83b2a-107">If autoSwitch is "true" and [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) is set to "auto", a connection to a more preferred network must be attempted whenever a more preferred network comes into range.</span></span> <span data-ttu-id="83b2a-108">慣用的無線網路清單中會有較高優先順序的網路。</span><span class="sxs-lookup"><span data-stu-id="83b2a-108">A more preferred network is one that is ordered higher in the list of preferred wireless networks.</span></span> <span data-ttu-id="83b2a-109">連線到另一個網路時，會發生此連接嘗試。</span><span class="sxs-lookup"><span data-stu-id="83b2a-109">This connection attempt occurs when connected to another network.</span></span>

<span data-ttu-id="83b2a-110">如果 [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) 設定為 "auto"，此值可以是 "true" 或 "false"。</span><span class="sxs-lookup"><span data-stu-id="83b2a-110">If [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) is set to "auto", this value can be either "true" or "false".</span></span>

<span data-ttu-id="83b2a-111">如果 [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) 設定為 "manual"，此值必須設定為 "false"。</span><span class="sxs-lookup"><span data-stu-id="83b2a-111">If [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) is set to "manual", this value must be set to "false".</span></span> <span data-ttu-id="83b2a-112">此元素不會影響手動連接的網路。</span><span class="sxs-lookup"><span data-stu-id="83b2a-112">This element has no effect on a manually connected network.</span></span>

<span data-ttu-id="83b2a-113">設定為 "true" 的 autoSwitch 值會導致較高頻率的新網路定期掃描。</span><span class="sxs-lookup"><span data-stu-id="83b2a-113">An autoSwitch value set to "true" results in a higher frequency of periodic scanning for new networks.</span></span> <span data-ttu-id="83b2a-114">這可能會導致這些定期掃描的無線頻率污染增加，以及無線網路介面卡使用的耗電量增加。</span><span class="sxs-lookup"><span data-stu-id="83b2a-114">This may result in increased radio frequency pollution from these periodic scans and increased power consumption used by the wireless network adapter.</span></span>

<span data-ttu-id="83b2a-115">**安裝了無線局域網路服務的 windows 7 和 Windows Server 2008 R2：** 變更會在已安裝無線局域網路服務的 Windows 7 和 Windows Server 2008 R2 上執行，以將無線網路效能優化。</span><span class="sxs-lookup"><span data-stu-id="83b2a-115">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="83b2a-116">這些變更的設計目的是要減少無線網路的無線頻率污染、耗電量和即時流量中斷。</span><span class="sxs-lookup"><span data-stu-id="83b2a-116">These changes are designed to reduce radio frequency pollution, power consumption, and disruption to real-time traffic over wireless networks.</span></span> <span data-ttu-id="83b2a-117">當無線局域網路設定檔中未設定此元素時， **autoSwitch** 的預設設定已變更。</span><span class="sxs-lookup"><span data-stu-id="83b2a-117">The default setting for **autoSwitch** when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="83b2a-118">在安裝了無線局域網路服務的 Windows 7 和 Windows Server 2008 R2 上，預設設定會變更為 "false"。</span><span class="sxs-lookup"><span data-stu-id="83b2a-118">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="83b2a-119">Windows Server 2008 和 Windows Vista 上的預設設定為 "true"。</span><span class="sxs-lookup"><span data-stu-id="83b2a-119">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="83b2a-120">建議將無線局域網路設定檔中的應用程式所使用的 **autoSwitch** 元素值設定為 "false"，以降低定期掃描新網路的頻率，除非應用程式絕對必須將此值設定為 "true"。</span><span class="sxs-lookup"><span data-stu-id="83b2a-120">It is recommended that the value of the **autoSwitch** element used by an application in a wireless LAN profile be set to "false" to reduce the frequency of periodic scanning for new networks, unless it is absolutely necessary for an application to set this value to "true".</span></span>

<span data-ttu-id="83b2a-121">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="83b2a-121">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="autoSwitch"
    type="boolean"
 />
```

<span data-ttu-id="83b2a-122">**AutoSwitch** 元素是由 [**WLANProfile**](wlan-profileschema-wlanprofile-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="83b2a-122">The **autoSwitch** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="83b2a-123">範例</span><span class="sxs-lookup"><span data-stu-id="83b2a-123">Examples</span></span>

<span data-ttu-id="83b2a-124">若要查看使用 **autoSwitch** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="83b2a-124">To view sample profiles that use the **autoSwitch** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83b2a-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="83b2a-125">Requirements</span></span>



| <span data-ttu-id="83b2a-126">需求</span><span class="sxs-lookup"><span data-stu-id="83b2a-126">Requirement</span></span> | <span data-ttu-id="83b2a-127">值</span><span class="sxs-lookup"><span data-stu-id="83b2a-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="83b2a-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="83b2a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="83b2a-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83b2a-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="83b2a-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="83b2a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="83b2a-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83b2a-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="83b2a-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83b2a-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="83b2a-133">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="83b2a-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="83b2a-134">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="83b2a-134">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="83b2a-135">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="83b2a-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="83b2a-136">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="83b2a-136">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




