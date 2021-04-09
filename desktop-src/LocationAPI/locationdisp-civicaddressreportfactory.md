---
description: 管理市政位址報表。
ms.assetid: 46c2d001-409a-4a0a-9006-1c2c9d327c13
title: LocationDisp. CivicAddressReportFactory 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 451bb21822d1b56e4c7a45f1587df04761b67690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694160"
---
# <a name="locationdispcivicaddressreportfactory-object"></a><span data-ttu-id="a34c7-103">LocationDisp. CivicAddressReportFactory 物件</span><span class="sxs-lookup"><span data-stu-id="a34c7-103">LocationDisp.CivicAddressReportFactory object</span></span>

<span data-ttu-id="a34c7-104">\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="a34c7-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a34c7-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="a34c7-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a34c7-106">相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a34c7-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="a34c7-107">若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]</span><span class="sxs-lookup"><span data-stu-id="a34c7-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="a34c7-108">管理市政位址報表。</span><span class="sxs-lookup"><span data-stu-id="a34c7-108">Manages civic address reports.</span></span>

## <a name="members"></a><span data-ttu-id="a34c7-109">成員</span><span class="sxs-lookup"><span data-stu-id="a34c7-109">Members</span></span>

<span data-ttu-id="a34c7-110">**LocationDisp. CivicAddressReportFactory** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a34c7-110">The **LocationDisp.CivicAddressReportFactory** object has these types of members:</span></span>

-   [<span data-ttu-id="a34c7-111">方法</span><span class="sxs-lookup"><span data-stu-id="a34c7-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a34c7-112">屬性</span><span class="sxs-lookup"><span data-stu-id="a34c7-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a34c7-113">方法</span><span class="sxs-lookup"><span data-stu-id="a34c7-113">Methods</span></span>

<span data-ttu-id="a34c7-114">**LocationDisp. CivicAddressReportFactory** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a34c7-114">The **LocationDisp.CivicAddressReportFactory** object has these methods.</span></span>



| <span data-ttu-id="a34c7-115">方法</span><span class="sxs-lookup"><span data-stu-id="a34c7-115">Method</span></span>                                                                                            | <span data-ttu-id="a34c7-116">描述</span><span class="sxs-lookup"><span data-stu-id="a34c7-116">Description</span></span>                                                                                   |
|:--------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a34c7-117">**ListenForReports**</span><span class="sxs-lookup"><span data-stu-id="a34c7-117">**ListenForReports**</span></span>](locationdisp-civicaddressreportfactory-listenforreports.md)               | <span data-ttu-id="a34c7-118">要求市政位址報告事件。</span><span class="sxs-lookup"><span data-stu-id="a34c7-118">Requests civic address report events.</span></span><br/>                                              |
| [<span data-ttu-id="a34c7-119">**RequestPermissions**</span><span class="sxs-lookup"><span data-stu-id="a34c7-119">**RequestPermissions**</span></span>](locationdisp-civicaddressreportfactory-requestpermissions.md)           | <span data-ttu-id="a34c7-120">開啟 [系統] 對話方塊來要求啟用位置之裝置的使用者權限。</span><span class="sxs-lookup"><span data-stu-id="a34c7-120">Opens a system dialog box to request user permission for location-enabled devices.</span></span><br/> |
| [<span data-ttu-id="a34c7-121">**StopListeningForReports**</span><span class="sxs-lookup"><span data-stu-id="a34c7-121">**StopListeningForReports**</span></span>](locationdisp-civicaddressreportfactory-stoplisteningforreports.md) | <span data-ttu-id="a34c7-122">取消市政位址報告事件要求。</span><span class="sxs-lookup"><span data-stu-id="a34c7-122">Cancels civic address report event requests.</span></span><br/>                                       |



 

### <a name="properties"></a><span data-ttu-id="a34c7-123">屬性</span><span class="sxs-lookup"><span data-stu-id="a34c7-123">Properties</span></span>

<span data-ttu-id="a34c7-124">**LocationDisp. CivicAddressReportFactory** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a34c7-124">The **LocationDisp.CivicAddressReportFactory** object has these properties.</span></span>



| <span data-ttu-id="a34c7-125">屬性</span><span class="sxs-lookup"><span data-stu-id="a34c7-125">Property</span></span>                                                                                        | <span data-ttu-id="a34c7-126">存取類型</span><span class="sxs-lookup"><span data-stu-id="a34c7-126">Access type</span></span>           | <span data-ttu-id="a34c7-127">Description</span><span class="sxs-lookup"><span data-stu-id="a34c7-127">Description</span></span>                                                                                                |
|:------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a34c7-128">**CivicAddressReport**</span><span class="sxs-lookup"><span data-stu-id="a34c7-128">**CivicAddressReport**</span></span>](locationdisp-dispcivicaddressreport-civicaddressreport.md)<br/> | <span data-ttu-id="a34c7-129">唯讀</span><span class="sxs-lookup"><span data-stu-id="a34c7-129">Read-only</span></span><br/>  | <span data-ttu-id="a34c7-130">目前的 [**LocationDisp. DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md)。</span><span class="sxs-lookup"><span data-stu-id="a34c7-130">The current [**LocationDisp.DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md).</span></span><br/> |
| [<span data-ttu-id="a34c7-131">**DesiredAccuracy**</span><span class="sxs-lookup"><span data-stu-id="a34c7-131">**DesiredAccuracy**</span></span>](locationdisp-civicaddressreportfactory-desiredaccuracy.md)<br/>    | <span data-ttu-id="a34c7-132">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a34c7-132">Read/write</span></span><br/> | <span data-ttu-id="a34c7-133">目前的預期精確度設定。</span><span class="sxs-lookup"><span data-stu-id="a34c7-133">The current desired-accuracy setting.</span></span><br/>                                                           |
| [<span data-ttu-id="a34c7-134">**ReportInterval**</span><span class="sxs-lookup"><span data-stu-id="a34c7-134">**ReportInterval**</span></span>](locationdisp-civicaddressreportfactory-reportinterval.md)<br/>      | <span data-ttu-id="a34c7-135">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a34c7-135">Read/write</span></span><br/> | <span data-ttu-id="a34c7-136">目前的市政位址報告事件間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a34c7-136">The current civic address report event interval in milliseconds.</span></span><br/>                                |
| [<span data-ttu-id="a34c7-137">**狀態**</span><span class="sxs-lookup"><span data-stu-id="a34c7-137">**Status**</span></span>](locationdisp-civicaddressreportfactory-status.md)<br/>                      | <span data-ttu-id="a34c7-138">唯讀</span><span class="sxs-lookup"><span data-stu-id="a34c7-138">Read-only</span></span><br/>  | <span data-ttu-id="a34c7-139">目前的報表狀態。</span><span class="sxs-lookup"><span data-stu-id="a34c7-139">The current report status.</span></span><br/>                                                                      |



 

## <a name="examples"></a><span data-ttu-id="a34c7-140">範例</span><span class="sxs-lookup"><span data-stu-id="a34c7-140">Examples</span></span>

<span data-ttu-id="a34c7-141">下列範例程式碼示範如何在 HTML 程式碼中建立這個物件。</span><span class="sxs-lookup"><span data-stu-id="a34c7-141">The following example code shows how to create this object in HTML code.</span></span>


```Text
<object id="civicfactory" 
    classid="clsid:2A11F42C-3E81-4ad4-9CBE-45579D89671A"
    type="application/x-oleobject">
</object>
```



<span data-ttu-id="a34c7-142">下列範例程式碼示範如何使用 Windows Script Host 在 JScript 中建立這個物件。</span><span class="sxs-lookup"><span data-stu-id="a34c7-142">The following example code shows how to create this object in JScript using Windows Script Host.</span></span>


```JScript
var civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory");
```



<span data-ttu-id="a34c7-143">下列範例程式碼示範如何使用 Windows Script Host 在 VBScript 中建立這個物件。</span><span class="sxs-lookup"><span data-stu-id="a34c7-143">The following example code shows how to create this object in VBScript using Windows Script Host.</span></span>


```VB
Dim civicfactory
Set civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory")
```



## <a name="requirements"></a><span data-ttu-id="a34c7-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="a34c7-144">Requirements</span></span>



| <span data-ttu-id="a34c7-145">需求</span><span class="sxs-lookup"><span data-stu-id="a34c7-145">Requirement</span></span> | <span data-ttu-id="a34c7-146">值</span><span class="sxs-lookup"><span data-stu-id="a34c7-146">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="a34c7-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a34c7-147">Minimum supported client</span></span><br/> | <span data-ttu-id="a34c7-148">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a34c7-148">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a34c7-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a34c7-149">Minimum supported server</span></span><br/> | <span data-ttu-id="a34c7-150">都不支援</span><span class="sxs-lookup"><span data-stu-id="a34c7-150">None supported</span></span><br/>                  |



## <a name="see-also"></a><span data-ttu-id="a34c7-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a34c7-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a34c7-152">**LocationDisp.CivicAddressReport**</span><span class="sxs-lookup"><span data-stu-id="a34c7-152">**LocationDisp.CivicAddressReport**</span></span>](locationdisp-dispcivicaddressreport.md)
</dt> </dl>

 

