---
description: 要求緯度/經度報表事件。
ms.assetid: c26a388b-e042-43da-a220-e3ecfcbd03a8
title: 'LocationDisp. LatLongReportFactory. ListenForReports 方法 (Locationapi .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 7e822595339fa499aaf469336ca3580acb2815bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693532"
---
# <a name="locationdisplatlongreportfactorylistenforreports-method"></a><span data-ttu-id="a5154-103">LocationDisp. LatLongReportFactory. ListenForReports 方法</span><span class="sxs-lookup"><span data-stu-id="a5154-103">LocationDisp.LatLongReportFactory.ListenForReports method</span></span>

<span data-ttu-id="a5154-104">\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="a5154-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a5154-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="a5154-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a5154-106">相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a5154-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="a5154-107">若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]</span><span class="sxs-lookup"><span data-stu-id="a5154-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="a5154-108">要求緯度/經度報表事件。</span><span class="sxs-lookup"><span data-stu-id="a5154-108">Requests latitude/longitude report events.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5154-109">語法</span><span class="sxs-lookup"><span data-stu-id="a5154-109">Syntax</span></span>


```JScript
LocationDisp.LatLongReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a><span data-ttu-id="a5154-110">參數</span><span class="sxs-lookup"><span data-stu-id="a5154-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5154-111">*requestedReportInterval*</span><span class="sxs-lookup"><span data-stu-id="a5154-111">*requestedReportInterval*</span></span> 
</dt> <dd> <span data-ttu-id="a5154-112">代表緯度/經度報表事件之間要求時間的 (**double word**) 數目（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a5154-112">Number (**double word**) representing the requested time between latitude/longitude report events, in milliseconds.</span></span> <span data-ttu-id="a5154-113">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="a5154-113">See Remarks.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5154-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="a5154-114">Return value</span></span>

<span data-ttu-id="a5154-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a5154-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5154-116">備註</span><span class="sxs-lookup"><span data-stu-id="a5154-116">Remarks</span></span>

<span data-ttu-id="a5154-117">位置提供者不需要在您要求的間隔提供報告。</span><span class="sxs-lookup"><span data-stu-id="a5154-117">The location provider is not required to provide reports at the interval that you request.</span></span> <span data-ttu-id="a5154-118">讀取 [**ReportInterval**](locationdisp-latlongreportfactory-reportinterval.md) 屬性的值，以探索真正的報表間隔設定。</span><span class="sxs-lookup"><span data-stu-id="a5154-118">Read the value of the [**ReportInterval**](locationdisp-latlongreportfactory-reportinterval.md) property to discover the true report interval setting.</span></span>

## <a name="examples"></a><span data-ttu-id="a5154-119">範例</span><span class="sxs-lookup"><span data-stu-id="a5154-119">Examples</span></span>

<span data-ttu-id="a5154-120">如需如何使用此方法的範例，請參閱 [接聽 LatLong 報表事件](/uwp/api/Windows.Devices.Geolocation)。</span><span class="sxs-lookup"><span data-stu-id="a5154-120">For an example of how to use this method, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5154-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5154-121">Requirements</span></span>



| <span data-ttu-id="a5154-122">需求</span><span class="sxs-lookup"><span data-stu-id="a5154-122">Requirement</span></span> | <span data-ttu-id="a5154-123">值</span><span class="sxs-lookup"><span data-stu-id="a5154-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5154-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5154-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a5154-125">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5154-125">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a5154-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5154-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a5154-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="a5154-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a5154-128">標頭</span><span class="sxs-lookup"><span data-stu-id="a5154-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5154-129"><dt>Locationapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="a5154-129"><dt>Locationapi.h</dt></span></span> </dl> |



 

