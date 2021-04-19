---
description: 指出是否要連接到隱藏的網路。
ms.assetid: 31b859e9-adc7-49e2-91d9-4fb63a35addb
title: 非廣播 (SSIDConfig) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nonBroadcast
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 695bede631b19c028a55a2f3ca82ba994ca12ada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977798"
---
# <a name="nonbroadcast-ssidconfig-element"></a><span data-ttu-id="a5fe5-103">非廣播 (SSIDConfig) 元素</span><span class="sxs-lookup"><span data-stu-id="a5fe5-103">nonBroadcast (SSIDConfig) Element</span></span>

<span data-ttu-id="a5fe5-104">非廣播的 (SSIDConfig) 元素指出是否要連接到隱藏的網路。</span><span class="sxs-lookup"><span data-stu-id="a5fe5-104">The nonBroadcast (SSIDConfig) element indicates whether to connect to a hidden network.</span></span> <span data-ttu-id="a5fe5-105">如果網路未廣播其 SSID，則稱為隱藏的網路。</span><span class="sxs-lookup"><span data-stu-id="a5fe5-105">If a network does not broadcast its SSID, then it is known as a hidden network.</span></span> <span data-ttu-id="a5fe5-106">如果設定檔中設定了多個 Ssid，它們必須全都具有相同的非廣播值。</span><span class="sxs-lookup"><span data-stu-id="a5fe5-106">If multiple SSIDs are set within the profile, they must all have the same nonBroadcast value.</span></span>

<span data-ttu-id="a5fe5-107">如果 [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) 設定為 **ESS**，此值可以是 "true" 或 "false"。</span><span class="sxs-lookup"><span data-stu-id="a5fe5-107">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to **ESS**, this value can be either "true" or "false".</span></span> <span data-ttu-id="a5fe5-108">如果這個元素不存在，則預設值為 "false"。</span><span class="sxs-lookup"><span data-stu-id="a5fe5-108">If this element is not present, the default value is "false".</span></span>

<span data-ttu-id="a5fe5-109">如果 [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) 設定為 **IBSS**，則這個值必須是 "false"。</span><span class="sxs-lookup"><span data-stu-id="a5fe5-109">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to **IBSS**, this value must be "false".</span></span> <span data-ttu-id="a5fe5-110">如果這個元素不存在，則預設值為 "false"。</span><span class="sxs-lookup"><span data-stu-id="a5fe5-110">If this element is not present, the default value is "false".</span></span>

<span data-ttu-id="a5fe5-111">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="a5fe5-111">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="nonBroadcast"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="a5fe5-112">元素是由 [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="a5fe5-112">The element is defined by the [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="a5fe5-113">範例</span><span class="sxs-lookup"><span data-stu-id="a5fe5-113">Examples</span></span>

<span data-ttu-id="a5fe5-114">若要查看使用非 **廣播元素的** 範例設定檔，請參閱 [非廣播設定檔範例](non-broadcast-profile-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="a5fe5-114">To view a sample profile that uses the **nonBroadcast** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5fe5-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5fe5-115">Requirements</span></span>



| <span data-ttu-id="a5fe5-116">需求</span><span class="sxs-lookup"><span data-stu-id="a5fe5-116">Requirement</span></span> | <span data-ttu-id="a5fe5-117">值</span><span class="sxs-lookup"><span data-stu-id="a5fe5-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a5fe5-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5fe5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a5fe5-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5fe5-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a5fe5-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5fe5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a5fe5-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5fe5-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a5fe5-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5fe5-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="a5fe5-123">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="a5fe5-123">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a5fe5-124">**SSIDConfig**</span><span class="sxs-lookup"><span data-stu-id="a5fe5-124">**SSIDConfig**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="a5fe5-125">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="a5fe5-125">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a5fe5-126">**SSIDConfig (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="a5fe5-126">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




