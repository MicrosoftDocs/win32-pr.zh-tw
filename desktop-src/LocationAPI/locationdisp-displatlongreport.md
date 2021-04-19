---
description: 表示緯度/經度報表。
ms.assetid: efa8d805-8546-4bab-95a0-69e1edc28753
title: LocationDisp. DispLatLongReport 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1b9629f22aee33670463b2a0832c12d520a9b8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976565"
---
# <a name="locationdispdisplatlongreport-object"></a><span data-ttu-id="27c05-103">LocationDisp. DispLatLongReport 物件</span><span class="sxs-lookup"><span data-stu-id="27c05-103">LocationDisp.DispLatLongReport object</span></span>

<span data-ttu-id="27c05-104">\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="27c05-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="27c05-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="27c05-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="27c05-106">相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="27c05-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="27c05-107">若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]</span><span class="sxs-lookup"><span data-stu-id="27c05-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="27c05-108">表示緯度/經度報表。</span><span class="sxs-lookup"><span data-stu-id="27c05-108">Represents a latitude/longitude report.</span></span>

## <a name="members"></a><span data-ttu-id="27c05-109">成員</span><span class="sxs-lookup"><span data-stu-id="27c05-109">Members</span></span>

<span data-ttu-id="27c05-110">**LocationDisp. DispLatLongReport** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="27c05-110">The **LocationDisp.DispLatLongReport** object has these types of members:</span></span>

-   [<span data-ttu-id="27c05-111">屬性</span><span class="sxs-lookup"><span data-stu-id="27c05-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="27c05-112">屬性</span><span class="sxs-lookup"><span data-stu-id="27c05-112">Properties</span></span>

<span data-ttu-id="27c05-113">**LocationDisp. DispLatLongReport** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="27c05-113">The **LocationDisp.DispLatLongReport** object has these properties.</span></span>



| <span data-ttu-id="27c05-114">屬性</span><span class="sxs-lookup"><span data-stu-id="27c05-114">Property</span></span>                                                                         | <span data-ttu-id="27c05-115">存取類型</span><span class="sxs-lookup"><span data-stu-id="27c05-115">Access type</span></span>          | <span data-ttu-id="27c05-116">Description</span><span class="sxs-lookup"><span data-stu-id="27c05-116">Description</span></span>                                                                                                                                                                                       |
|:---------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27c05-117">**高度**</span><span class="sxs-lookup"><span data-stu-id="27c05-117">**Altitude**</span></span>](locationdisp-displatlongreport-altitude.md)<br/>           | <span data-ttu-id="27c05-118">唯讀</span><span class="sxs-lookup"><span data-stu-id="27c05-118">Read-only</span></span><br/> | <span data-ttu-id="27c05-119">目前的高度，以計量為單位。</span><span class="sxs-lookup"><span data-stu-id="27c05-119">Current altitude, in meters.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="27c05-120">**AltitudeError**</span><span class="sxs-lookup"><span data-stu-id="27c05-120">**AltitudeError**</span></span>](locationdisp-displatlongreport-altitudeerror.md)<br/> | <span data-ttu-id="27c05-121">唯讀</span><span class="sxs-lookup"><span data-stu-id="27c05-121">Read-only</span></span><br/> | <span data-ttu-id="27c05-122">高度錯誤，計量為。</span><span class="sxs-lookup"><span data-stu-id="27c05-122">Altitude error, in meters.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="27c05-123">**ErrorRadius**</span><span class="sxs-lookup"><span data-stu-id="27c05-123">**ErrorRadius**</span></span>](locationdisp-displatlongreport-errorradius.md)<br/>     | <span data-ttu-id="27c05-124">唯讀</span><span class="sxs-lookup"><span data-stu-id="27c05-124">Read-only</span></span><br/> | <span data-ttu-id="27c05-125">從報告位置的距離（以計量為單位）。</span><span class="sxs-lookup"><span data-stu-id="27c05-125">A distance from the reported location, in meters.</span></span> <span data-ttu-id="27c05-126">此 radius 會與報告的位置合併為來源，並描述實際位置 proably 所在的圓形。</span><span class="sxs-lookup"><span data-stu-id="27c05-126">Combined with the reported location as the origin, this radius describes the circle in which the actual location is proably located.</span></span><br/> |
| [<span data-ttu-id="27c05-127">**緯度**</span><span class="sxs-lookup"><span data-stu-id="27c05-127">**Latitude**</span></span>](locationdisp-displatlongreport-latitude.md)<br/>           | <span data-ttu-id="27c05-128">唯讀</span><span class="sxs-lookup"><span data-stu-id="27c05-128">Read-only</span></span><br/> | <span data-ttu-id="27c05-129">目前的緯度（以度為單位）。</span><span class="sxs-lookup"><span data-stu-id="27c05-129">Current latitude, in degrees.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="27c05-130">**經度**</span><span class="sxs-lookup"><span data-stu-id="27c05-130">**Longitude**</span></span>](locationdisp-displatlongreport-longitude.md)<br/>         | <span data-ttu-id="27c05-131">唯讀</span><span class="sxs-lookup"><span data-stu-id="27c05-131">Read-only</span></span><br/> | <span data-ttu-id="27c05-132">目前的經度（以度為單位）。</span><span class="sxs-lookup"><span data-stu-id="27c05-132">Current longitude, in degrees.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="27c05-133">**時間 戳**</span><span class="sxs-lookup"><span data-stu-id="27c05-133">**Timestamp**</span></span>](locationdisp-displatlongreport-timestamp.md)<br/>         | <span data-ttu-id="27c05-134">唯讀</span><span class="sxs-lookup"><span data-stu-id="27c05-134">Read-only</span></span><br/> | <span data-ttu-id="27c05-135">產生報表的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="27c05-135">The date and time when the report was generated.</span></span><br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="27c05-136">備註</span><span class="sxs-lookup"><span data-stu-id="27c05-136">Remarks</span></span>

<span data-ttu-id="27c05-137">您可以透過 [**LatLongReportFactory**](locationdisp-latlongreportfactory.md)物件的 [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md)屬性來取得這個物件。</span><span class="sxs-lookup"><span data-stu-id="27c05-137">You can retrieve this object through the [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md) property of the [**LatLongReportFactory**](locationdisp-latlongreportfactory.md) object.</span></span> <span data-ttu-id="27c05-138">您可以透過 [**NewLatLongReport**](newlatlongreport.md) 事件接收此物件。</span><span class="sxs-lookup"><span data-stu-id="27c05-138">You can receive this object through the [**NewLatLongReport**](newlatlongreport.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="27c05-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="27c05-139">Requirements</span></span>



| <span data-ttu-id="27c05-140">需求</span><span class="sxs-lookup"><span data-stu-id="27c05-140">Requirement</span></span> | <span data-ttu-id="27c05-141">值</span><span class="sxs-lookup"><span data-stu-id="27c05-141">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="27c05-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27c05-142">Minimum supported client</span></span><br/> | <span data-ttu-id="27c05-143">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27c05-143">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="27c05-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27c05-144">Minimum supported server</span></span><br/> | <span data-ttu-id="27c05-145">都不支援</span><span class="sxs-lookup"><span data-stu-id="27c05-145">None supported</span></span><br/>                  |



 

