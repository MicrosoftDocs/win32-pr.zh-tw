---
description: 從報告位置的距離（以計量為單位）。 此 radius 會與報告的位置結合為來源，以描述實際位置可能所在的圓形。
ms.assetid: a9565bd5-d1e0-45f8-abeb-3191b16480fa
title: LocationDisp. DispLatLongReport. ErrorRadius 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.ErrorRadius
api_type:
- COM
api_location: ''
ms.openlocfilehash: f99ff9b03451738158a98541bfae0e67a8827717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988855"
---
# <a name="locationdispdisplatlongreporterrorradius-property"></a><span data-ttu-id="bac9f-104">LocationDisp. DispLatLongReport. ErrorRadius 屬性</span><span class="sxs-lookup"><span data-stu-id="bac9f-104">LocationDisp.DispLatLongReport.ErrorRadius property</span></span>

<span data-ttu-id="bac9f-105">\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="bac9f-105">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bac9f-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="bac9f-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="bac9f-107">相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="bac9f-107">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="bac9f-108">若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]</span><span class="sxs-lookup"><span data-stu-id="bac9f-108">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="bac9f-109">從報告位置的距離（以計量為單位）。</span><span class="sxs-lookup"><span data-stu-id="bac9f-109">A distance from the reported location, in meters.</span></span> <span data-ttu-id="bac9f-110">此 radius 會與報告的位置結合為來源，以描述實際位置可能所在的圓形。</span><span class="sxs-lookup"><span data-stu-id="bac9f-110">Combined with the reported location as the origin, this radius describes the circle in which the actual location is probably located.</span></span>

<span data-ttu-id="bac9f-111">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="bac9f-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bac9f-112">語法</span><span class="sxs-lookup"><span data-stu-id="bac9f-112">Syntax</span></span>


```JScript
ErrorRadius = LocationDisp.DispLatLongReport.ErrorRadius
```



## <a name="property-value"></a><span data-ttu-id="bac9f-113">屬性值</span><span class="sxs-lookup"><span data-stu-id="bac9f-113">Property value</span></span>

<span data-ttu-id="bac9f-114">這個屬性是唯讀的 (雙精確度浮點數) 的 **數位** 。</span><span class="sxs-lookup"><span data-stu-id="bac9f-114">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="examples"></a><span data-ttu-id="bac9f-115">範例</span><span class="sxs-lookup"><span data-stu-id="bac9f-115">Examples</span></span>

<span data-ttu-id="bac9f-116">如需如何使用這個屬性的範例，請參閱 [簡單的 LatLong 報表範例](/uwp/api/Windows.Devices.Geolocation)。</span><span class="sxs-lookup"><span data-stu-id="bac9f-116">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="bac9f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="bac9f-117">Requirements</span></span>



| <span data-ttu-id="bac9f-118">需求</span><span class="sxs-lookup"><span data-stu-id="bac9f-118">Requirement</span></span> | <span data-ttu-id="bac9f-119">值</span><span class="sxs-lookup"><span data-stu-id="bac9f-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="bac9f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bac9f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bac9f-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bac9f-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bac9f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bac9f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bac9f-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="bac9f-123">None supported</span></span><br/>                  |



 

