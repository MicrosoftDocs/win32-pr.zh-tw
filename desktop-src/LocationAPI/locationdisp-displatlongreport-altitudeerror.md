---
description: 高度錯誤，計量為。
ms.assetid: 36ebb079-26e6-4b3f-ad73-547a47bd23d7
title: LocationDisp. DispLatLongReport. AltitudeError 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.AltitudeError
api_type:
- COM
api_location: ''
ms.openlocfilehash: 92fd71b133912a57e6ed4ef034dda6fe92ef9b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850256"
---
# <a name="locationdispdisplatlongreportaltitudeerror-property"></a><span data-ttu-id="1e614-103">LocationDisp. DispLatLongReport. AltitudeError 屬性</span><span class="sxs-lookup"><span data-stu-id="1e614-103">LocationDisp.DispLatLongReport.AltitudeError property</span></span>

<span data-ttu-id="1e614-104">\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="1e614-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1e614-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="1e614-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="1e614-106">相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1e614-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="1e614-107">若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]</span><span class="sxs-lookup"><span data-stu-id="1e614-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="1e614-108">高度錯誤，計量為。</span><span class="sxs-lookup"><span data-stu-id="1e614-108">Altitude error, in meters.</span></span>

<span data-ttu-id="1e614-109">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="1e614-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e614-110">語法</span><span class="sxs-lookup"><span data-stu-id="1e614-110">Syntax</span></span>


```JScript
AltitudeError = LocationDisp.DispLatLongReport.AltitudeError
```



## <a name="property-value"></a><span data-ttu-id="1e614-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="1e614-111">Property value</span></span>

<span data-ttu-id="1e614-112">這個屬性是唯讀的 (雙精確度浮點數) 的 **數位** 。</span><span class="sxs-lookup"><span data-stu-id="1e614-112">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="remarks"></a><span data-ttu-id="1e614-113">備註</span><span class="sxs-lookup"><span data-stu-id="1e614-113">Remarks</span></span>

<span data-ttu-id="1e614-114">不需要定位感應器來提供此屬性。</span><span class="sxs-lookup"><span data-stu-id="1e614-114">Location sensors are not required to provide this property.</span></span> <span data-ttu-id="1e614-115">您應該在嘗試存取此屬性時處理例外狀況。</span><span class="sxs-lookup"><span data-stu-id="1e614-115">You should handle exceptions when attempting to access this property.</span></span>

## <a name="examples"></a><span data-ttu-id="1e614-116">範例</span><span class="sxs-lookup"><span data-stu-id="1e614-116">Examples</span></span>

<span data-ttu-id="1e614-117">如需如何使用這個屬性的範例，請參閱 [簡單的 LatLong 報表範例](/uwp/api/Windows.Devices.Geolocation)。</span><span class="sxs-lookup"><span data-stu-id="1e614-117">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e614-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e614-118">Requirements</span></span>



| <span data-ttu-id="1e614-119">需求</span><span class="sxs-lookup"><span data-stu-id="1e614-119">Requirement</span></span> | <span data-ttu-id="1e614-120">值</span><span class="sxs-lookup"><span data-stu-id="1e614-120">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="1e614-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e614-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1e614-122">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e614-122">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1e614-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e614-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1e614-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="1e614-124">None supported</span></span><br/>                  |



 

