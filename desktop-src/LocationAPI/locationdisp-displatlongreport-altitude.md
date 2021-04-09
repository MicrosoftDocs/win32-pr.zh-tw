---
description: 目前的高度，以計量為單位。 高度相對於參考橢圓體。
ms.assetid: fbe9984c-aa9d-4ce0-9f8b-d79ca06764d4
title: LocationDisp. DispLatLongReport. 海拔屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Altitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2004c8df6c61fb890bf8f71fb3c2b5446d71d79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849471"
---
# <a name="locationdispdisplatlongreportaltitude-property"></a><span data-ttu-id="d24ac-104">LocationDisp. DispLatLongReport. 海拔屬性</span><span class="sxs-lookup"><span data-stu-id="d24ac-104">LocationDisp.DispLatLongReport.Altitude property</span></span>

<span data-ttu-id="d24ac-105">\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="d24ac-105">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d24ac-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="d24ac-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="d24ac-107">相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d24ac-107">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="d24ac-108">若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]</span><span class="sxs-lookup"><span data-stu-id="d24ac-108">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="d24ac-109">目前的高度，以計量為單位。</span><span class="sxs-lookup"><span data-stu-id="d24ac-109">Current altitude, in meters.</span></span> <span data-ttu-id="d24ac-110">高度相對於參考橢圓體。</span><span class="sxs-lookup"><span data-stu-id="d24ac-110">Altitude is relative to the reference ellipsoid.</span></span>

<span data-ttu-id="d24ac-111">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="d24ac-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d24ac-112">語法</span><span class="sxs-lookup"><span data-stu-id="d24ac-112">Syntax</span></span>


```JScript
Altitude = LocationDisp.DispLatLongReport.Altitude
```



## <a name="property-value"></a><span data-ttu-id="d24ac-113">屬性值</span><span class="sxs-lookup"><span data-stu-id="d24ac-113">Property value</span></span>

<span data-ttu-id="d24ac-114">這個屬性是唯讀的 (雙精確度浮點數) 的 **數位** 。</span><span class="sxs-lookup"><span data-stu-id="d24ac-114">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="remarks"></a><span data-ttu-id="d24ac-115">備註</span><span class="sxs-lookup"><span data-stu-id="d24ac-115">Remarks</span></span>

<span data-ttu-id="d24ac-116">不需要定位感應器來提供此屬性。</span><span class="sxs-lookup"><span data-stu-id="d24ac-116">Location sensors are not required to provide this property.</span></span> <span data-ttu-id="d24ac-117">您應該在嘗試存取此屬性時處理例外狀況。</span><span class="sxs-lookup"><span data-stu-id="d24ac-117">You should handle exceptions when attempting to access this property.</span></span>

<span data-ttu-id="d24ac-118">**高度** 方法會抓取 Geodetic 系統 (WGS 84) 的最新修訂所定義之參考橢圓體的高度，而不是相對於海平面的高度。</span><span class="sxs-lookup"><span data-stu-id="d24ac-118">The **Altitude** method retrieves the altitude relative to the reference ellipsoid that is defined by the latest revision of the World Geodetic System (WGS 84), rather than the altitude relative to sea level.</span></span>

## <a name="examples"></a><span data-ttu-id="d24ac-119">範例</span><span class="sxs-lookup"><span data-stu-id="d24ac-119">Examples</span></span>

<span data-ttu-id="d24ac-120">如需如何使用這個屬性的範例，請參閱 [簡單的 LatLong 報表範例](/uwp/api/Windows.Devices.Geolocation)。</span><span class="sxs-lookup"><span data-stu-id="d24ac-120">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="d24ac-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d24ac-121">Requirements</span></span>



| <span data-ttu-id="d24ac-122">需求</span><span class="sxs-lookup"><span data-stu-id="d24ac-122">Requirement</span></span> | <span data-ttu-id="d24ac-123">值</span><span class="sxs-lookup"><span data-stu-id="d24ac-123">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="d24ac-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d24ac-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d24ac-125">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d24ac-125">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d24ac-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d24ac-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d24ac-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="d24ac-127">None supported</span></span><br/>                  |



 

