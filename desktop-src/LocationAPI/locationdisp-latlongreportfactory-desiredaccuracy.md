---
description: LocationDisp. LatLongReportFactory. DesiredAccuracy 屬性-目前的預期精確度值。
ms.assetid: dfad833b-bb0c-4c66-9942-da10abee5381
title: LocationDisp. LatLongReportFactory. DesiredAccuracy 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.DesiredAccuracy
api_type:
- COM
api_location: ''
ms.openlocfilehash: afc5ec235df6c9e07a665410cb09e00f24305304
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088966"
---
# <a name="locationdisplatlongreportfactorydesiredaccuracy-property"></a><span data-ttu-id="0f3ef-103">LocationDisp. LatLongReportFactory. DesiredAccuracy 屬性</span><span class="sxs-lookup"><span data-stu-id="0f3ef-103">LocationDisp.LatLongReportFactory.DesiredAccuracy property</span></span>

<span data-ttu-id="0f3ef-104">\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="0f3ef-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0f3ef-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="0f3ef-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="0f3ef-106">相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0f3ef-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="0f3ef-107">若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]</span><span class="sxs-lookup"><span data-stu-id="0f3ef-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="0f3ef-108">目前的預期精確度值。</span><span class="sxs-lookup"><span data-stu-id="0f3ef-108">The current desired-accuracy value.</span></span>

<span data-ttu-id="0f3ef-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="0f3ef-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f3ef-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f3ef-110">Syntax</span></span>


```JScript
DesiredAccuracy = LocationDisp.LatLongReportFactory.DesiredAccuracy
LocationDisp.LatLongReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a><span data-ttu-id="0f3ef-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="0f3ef-111">Property value</span></span>

<span data-ttu-id="0f3ef-112">這個屬性是讀取/寫入的 **ULONG**。</span><span class="sxs-lookup"><span data-stu-id="0f3ef-112">This property is a read/write **ULONG**.</span></span>



| <span data-ttu-id="0f3ef-113">值</span><span class="sxs-lookup"><span data-stu-id="0f3ef-113">Value</span></span>                                                                        | <span data-ttu-id="0f3ef-114">意義</span><span class="sxs-lookup"><span data-stu-id="0f3ef-114">Meaning</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0f3ef-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0f3ef-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="0f3ef-116">預設值。</span><span class="sxs-lookup"><span data-stu-id="0f3ef-116">Default.</span></span> <span data-ttu-id="0f3ef-117">感應器應使用可優化電源使用的精確度，以及其他成本考慮。</span><span class="sxs-lookup"><span data-stu-id="0f3ef-117">The sensor should use the accuracy for which it can optimize power use and other cost considerations.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="0f3ef-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0f3ef-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="0f3ef-119">感應器應該盡可能提供最精確的報告。</span><span class="sxs-lookup"><span data-stu-id="0f3ef-119">The sensor should deliver the most accurate report possible.</span></span> <span data-ttu-id="0f3ef-120">這包括使用可能須付費的服務，或是耗用更多的電池電力或是連線頻寬。</span><span class="sxs-lookup"><span data-stu-id="0f3ef-120">This includes using services that might charge money, or consuming higher levels of battery power or connection bandwidth.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0f3ef-121">備註</span><span class="sxs-lookup"><span data-stu-id="0f3ef-121">Remarks</span></span>

<span data-ttu-id="0f3ef-122">此值是對位置提供者的要求。</span><span class="sxs-lookup"><span data-stu-id="0f3ef-122">This value is a request to the location provider.</span></span> <span data-ttu-id="0f3ef-123">位置提供者不需要在您要求的間隔提供報告。</span><span class="sxs-lookup"><span data-stu-id="0f3ef-123">The location provider is not required to provide reports at the interval you requested.</span></span> <span data-ttu-id="0f3ef-124">讀取這個屬性的值，以探索真正的報表間隔設定。</span><span class="sxs-lookup"><span data-stu-id="0f3ef-124">Read the value of this property to discover the true report interval setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f3ef-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f3ef-125">Requirements</span></span>



| <span data-ttu-id="0f3ef-126">需求</span><span class="sxs-lookup"><span data-stu-id="0f3ef-126">Requirement</span></span> | <span data-ttu-id="0f3ef-127">值</span><span class="sxs-lookup"><span data-stu-id="0f3ef-127">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="0f3ef-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0f3ef-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0f3ef-129">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f3ef-129">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0f3ef-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0f3ef-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0f3ef-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="0f3ef-131">None supported</span></span><br/>                  |



 

