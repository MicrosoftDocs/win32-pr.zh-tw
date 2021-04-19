---
description: 目前的經度（以度為單位）。
ms.assetid: f4fa1cbb-d682-42ab-9dd8-dff636ea4c8a
title: LocationDisp. DispLatLongReport. 經度屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Longitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: c705ebd9476582f05b6dc87233dcc8e8990c5202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997001"
---
# <a name="locationdispdisplatlongreportlongitude-property"></a><span data-ttu-id="6361f-103">LocationDisp. DispLatLongReport. 經度屬性</span><span class="sxs-lookup"><span data-stu-id="6361f-103">LocationDisp.DispLatLongReport.Longitude property</span></span>

<span data-ttu-id="6361f-104">\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="6361f-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6361f-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="6361f-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6361f-106">相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="6361f-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="6361f-107">若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]</span><span class="sxs-lookup"><span data-stu-id="6361f-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="6361f-108">目前的經度（以度為單位）。</span><span class="sxs-lookup"><span data-stu-id="6361f-108">Current longitude, in degrees.</span></span> <span data-ttu-id="6361f-109">經度介於-180 到180之間，其中東部是正數。</span><span class="sxs-lookup"><span data-stu-id="6361f-109">The longitude is between -180 and 180, where east is positive.</span></span>

<span data-ttu-id="6361f-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="6361f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6361f-111">語法</span><span class="sxs-lookup"><span data-stu-id="6361f-111">Syntax</span></span>


```JScript
Longitude = LocationDisp.DispLatLongReport.Longitude
```



## <a name="property-value"></a><span data-ttu-id="6361f-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="6361f-112">Property value</span></span>

<span data-ttu-id="6361f-113">這個屬性是唯讀的 (雙精確度浮點數) 的 **數位** 。</span><span class="sxs-lookup"><span data-stu-id="6361f-113">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="examples"></a><span data-ttu-id="6361f-114">範例</span><span class="sxs-lookup"><span data-stu-id="6361f-114">Examples</span></span>

<span data-ttu-id="6361f-115">如需如何使用這個屬性的範例，請參閱 [簡單的 LatLong 報表範例](/uwp/api/Windows.Devices.Geolocation)。</span><span class="sxs-lookup"><span data-stu-id="6361f-115">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="6361f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6361f-116">Requirements</span></span>



| <span data-ttu-id="6361f-117">需求</span><span class="sxs-lookup"><span data-stu-id="6361f-117">Requirement</span></span> | <span data-ttu-id="6361f-118">值</span><span class="sxs-lookup"><span data-stu-id="6361f-118">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="6361f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6361f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6361f-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6361f-120">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6361f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6361f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6361f-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="6361f-122">None supported</span></span><br/>                  |



 

