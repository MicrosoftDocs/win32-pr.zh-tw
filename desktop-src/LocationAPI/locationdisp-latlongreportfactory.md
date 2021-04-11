---
description: 管理緯度/經度報表。
ms.assetid: 66025874-32dd-4494-a9ad-12fe3afa60f9
title: LocationDisp. LatLongReportFactory 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9fad1ca0f4605f1167f9b86b0df5bc8f20e46285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852776"
---
# <a name="locationdisplatlongreportfactory-object"></a><span data-ttu-id="92e56-103">LocationDisp. LatLongReportFactory 物件</span><span class="sxs-lookup"><span data-stu-id="92e56-103">LocationDisp.LatLongReportFactory object</span></span>

<span data-ttu-id="92e56-104">\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="92e56-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="92e56-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="92e56-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="92e56-106">相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="92e56-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="92e56-107">若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]</span><span class="sxs-lookup"><span data-stu-id="92e56-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="92e56-108">管理緯度/經度報表。</span><span class="sxs-lookup"><span data-stu-id="92e56-108">Manages latitude/longitude reports.</span></span>

## <a name="members"></a><span data-ttu-id="92e56-109">成員</span><span class="sxs-lookup"><span data-stu-id="92e56-109">Members</span></span>

<span data-ttu-id="92e56-110">**LocationDisp. LatLongReportFactory** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="92e56-110">The **LocationDisp.LatLongReportFactory** object has these types of members:</span></span>

-   [<span data-ttu-id="92e56-111">方法</span><span class="sxs-lookup"><span data-stu-id="92e56-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="92e56-112">屬性</span><span class="sxs-lookup"><span data-stu-id="92e56-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="92e56-113">方法</span><span class="sxs-lookup"><span data-stu-id="92e56-113">Methods</span></span>

<span data-ttu-id="92e56-114">**LocationDisp. LatLongReportFactory** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="92e56-114">The **LocationDisp.LatLongReportFactory** object has these methods.</span></span>



| <span data-ttu-id="92e56-115">方法</span><span class="sxs-lookup"><span data-stu-id="92e56-115">Method</span></span>                                                                                       | <span data-ttu-id="92e56-116">描述</span><span class="sxs-lookup"><span data-stu-id="92e56-116">Description</span></span>                                                                                   |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="92e56-117">**ListenForReports**</span><span class="sxs-lookup"><span data-stu-id="92e56-117">**ListenForReports**</span></span>](locationdisp-latlongreportfactory-listenforreports.md)               | <span data-ttu-id="92e56-118">要求緯度/經度報表事件。</span><span class="sxs-lookup"><span data-stu-id="92e56-118">Requests latitude/longitude report events.</span></span><br/>                                         |
| [<span data-ttu-id="92e56-119">**RequestPermissions**</span><span class="sxs-lookup"><span data-stu-id="92e56-119">**RequestPermissions**</span></span>](locationdisp-latlongreportfactory-requestpermissions.md)           | <span data-ttu-id="92e56-120">開啟 [系統] 對話方塊來要求啟用位置之裝置的使用者權限。</span><span class="sxs-lookup"><span data-stu-id="92e56-120">Opens a system dialog box to request user permission for location-enabled devices.</span></span><br/> |
| <span data-ttu-id="92e56-121">[**StopListeningForReports**](/previous-versions/windows/desktop/legacy/dd317718(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="92e56-121">[**StopListeningForReports**](/previous-versions/windows/desktop/legacy/dd317718(v=vs.85))</span></span> | <span data-ttu-id="92e56-122">取消緯度/經度報表事件的要求。</span><span class="sxs-lookup"><span data-stu-id="92e56-122">Cancels requests for latitude/longitude report events.</span></span><br/>                             |



 

### <a name="properties"></a><span data-ttu-id="92e56-123">屬性</span><span class="sxs-lookup"><span data-stu-id="92e56-123">Properties</span></span>

<span data-ttu-id="92e56-124">**LocationDisp. LatLongReportFactory** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="92e56-124">The **LocationDisp.LatLongReportFactory** object has these properties.</span></span>



| <span data-ttu-id="92e56-125">屬性</span><span class="sxs-lookup"><span data-stu-id="92e56-125">Property</span></span>                                                                                | <span data-ttu-id="92e56-126">存取類型</span><span class="sxs-lookup"><span data-stu-id="92e56-126">Access type</span></span>           | <span data-ttu-id="92e56-127">Description</span><span class="sxs-lookup"><span data-stu-id="92e56-127">Description</span></span>                                                                                      |
|:----------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="92e56-128">**DesiredAccuracy**</span><span class="sxs-lookup"><span data-stu-id="92e56-128">**DesiredAccuracy**</span></span>](locationdisp-latlongreportfactory-desiredaccuracy.md)<br/> | <span data-ttu-id="92e56-129">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="92e56-129">Read/write</span></span><br/> | <span data-ttu-id="92e56-130">目前的預期精確度值。</span><span class="sxs-lookup"><span data-stu-id="92e56-130">The current desired-accuracy value.</span></span><br/>                                                   |
| [<span data-ttu-id="92e56-131">**LatLongReport**</span><span class="sxs-lookup"><span data-stu-id="92e56-131">**LatLongReport**</span></span>](locationdisp-latlongreportfactory-latlongreport.md)<br/>     | <span data-ttu-id="92e56-132">唯讀</span><span class="sxs-lookup"><span data-stu-id="92e56-132">Read-only</span></span><br/>  | <span data-ttu-id="92e56-133">目前的 [**LocationDisp. DispLatLongReport**](locationdisp-displatlongreport.md)。</span><span class="sxs-lookup"><span data-stu-id="92e56-133">The current [**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md).</span></span><br/> |
| [<span data-ttu-id="92e56-134">**ReportInterval**</span><span class="sxs-lookup"><span data-stu-id="92e56-134">**ReportInterval**</span></span>](locationdisp-latlongreportfactory-reportinterval.md)<br/>   | <span data-ttu-id="92e56-135">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="92e56-135">Read/write</span></span><br/> | <span data-ttu-id="92e56-136">目前的緯度/經度報表事件間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="92e56-136">The current latitude/longitude report event interval in milliseconds.</span></span><br/>                 |
| [<span data-ttu-id="92e56-137">**狀態**</span><span class="sxs-lookup"><span data-stu-id="92e56-137">**Status**</span></span>](locationdisp-latlongreportfactory-status.md)<br/>                   | <span data-ttu-id="92e56-138">唯讀</span><span class="sxs-lookup"><span data-stu-id="92e56-138">Read-only</span></span><br/>  | <span data-ttu-id="92e56-139">目前的報表狀態。</span><span class="sxs-lookup"><span data-stu-id="92e56-139">The current report status.</span></span><br/>                                                            |



 

## <a name="examples"></a><span data-ttu-id="92e56-140">範例</span><span class="sxs-lookup"><span data-stu-id="92e56-140">Examples</span></span>

<span data-ttu-id="92e56-141">下列範例程式碼示範如何在 HTML 程式碼中建立這個物件。</span><span class="sxs-lookup"><span data-stu-id="92e56-141">The following example code shows how to create this object in HTML code.</span></span>


```
<object id="latlongfactory" 
    classid="clsid:9DCC3CC8-8609-4863-BAD4-03601F4C65E8"
    type="application/x-oleobject">
</object>
```



<span data-ttu-id="92e56-142">下列範例程式碼示範如何使用 Windows Script Host 在 JScript 中建立這個物件。</span><span class="sxs-lookup"><span data-stu-id="92e56-142">The following example code shows how to create this object in JScript using Windows Script Host.</span></span>


```JScript
var latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory");
```



<span data-ttu-id="92e56-143">下列範例程式碼示範如何使用 Windows Script Host 在 VBScript 中建立這個物件。</span><span class="sxs-lookup"><span data-stu-id="92e56-143">The following example code shows how to create this object in VBScript using Windows Script Host.</span></span>


```VB
Dim latlongfactory
Set latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory")
```



## <a name="requirements"></a><span data-ttu-id="92e56-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="92e56-144">Requirements</span></span>



| <span data-ttu-id="92e56-145">需求</span><span class="sxs-lookup"><span data-stu-id="92e56-145">Requirement</span></span> | <span data-ttu-id="92e56-146">值</span><span class="sxs-lookup"><span data-stu-id="92e56-146">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="92e56-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="92e56-147">Minimum supported client</span></span><br/> | <span data-ttu-id="92e56-148">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="92e56-148">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="92e56-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="92e56-149">Minimum supported server</span></span><br/> | <span data-ttu-id="92e56-150">都不支援</span><span class="sxs-lookup"><span data-stu-id="92e56-150">None supported</span></span><br/>                  |



## <a name="see-also"></a><span data-ttu-id="92e56-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92e56-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92e56-152">**LocationDisp.DispLatLongReport**</span><span class="sxs-lookup"><span data-stu-id="92e56-152">**LocationDisp.DispLatLongReport**</span></span>](locationdisp-displatlongreport.md)
</dt> </dl>

 

