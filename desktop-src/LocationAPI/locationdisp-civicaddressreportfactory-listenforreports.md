---
description: 要求市政位址報告事件。
ms.assetid: cb02f611-7cda-405f-aeee-833b7385a4be
title: 'LocationDisp. CivicAddressReportFactory. ListenForReports 方法 (Locationapi .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 02315f8b2f7fced76c3d0d1330df246af6bad4b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945335"
---
# <a name="locationdispcivicaddressreportfactorylistenforreports-method"></a><span data-ttu-id="1c7a1-103">LocationDisp. CivicAddressReportFactory. ListenForReports 方法</span><span class="sxs-lookup"><span data-stu-id="1c7a1-103">LocationDisp.CivicAddressReportFactory.ListenForReports method</span></span>

<span data-ttu-id="1c7a1-104">\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="1c7a1-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1c7a1-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="1c7a1-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="1c7a1-106">相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1c7a1-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="1c7a1-107">若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]</span><span class="sxs-lookup"><span data-stu-id="1c7a1-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="1c7a1-108">要求市政位址報告事件。</span><span class="sxs-lookup"><span data-stu-id="1c7a1-108">Requests civic address report events.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c7a1-109">語法</span><span class="sxs-lookup"><span data-stu-id="1c7a1-109">Syntax</span></span>


```JScript
LocationDisp.CivicAddressReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a><span data-ttu-id="1c7a1-110">參數</span><span class="sxs-lookup"><span data-stu-id="1c7a1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c7a1-111">*requestedReportInterval*</span><span class="sxs-lookup"><span data-stu-id="1c7a1-111">*requestedReportInterval*</span></span> 
</dt> <dd> <span data-ttu-id="1c7a1-112">代表在市政位址報告事件之間要求時間的 (**double word**) 數目（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="1c7a1-112">Number (**double word**) representing the requested time between civic address report events, in milliseconds.</span></span> <span data-ttu-id="1c7a1-113">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="1c7a1-113">See Remarks.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c7a1-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="1c7a1-114">Return value</span></span>

<span data-ttu-id="1c7a1-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1c7a1-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c7a1-116">備註</span><span class="sxs-lookup"><span data-stu-id="1c7a1-116">Remarks</span></span>

<span data-ttu-id="1c7a1-117">不需要位置提供者來提供您要求的精確度。</span><span class="sxs-lookup"><span data-stu-id="1c7a1-117">The location provider is not required to provide the accuracy that you request.</span></span> <span data-ttu-id="1c7a1-118">讀取 [**ReportInterval**](locationdisp-civicaddressreportfactory-reportinterval.md) 屬性的值，以探索真正的報表間隔設定。</span><span class="sxs-lookup"><span data-stu-id="1c7a1-118">Read the value of the [**ReportInterval**](locationdisp-civicaddressreportfactory-reportinterval.md) property to discover the true report interval setting.</span></span>

## <a name="examples"></a><span data-ttu-id="1c7a1-119">範例</span><span class="sxs-lookup"><span data-stu-id="1c7a1-119">Examples</span></span>

<span data-ttu-id="1c7a1-120">如需如何使用此方法的範例，請參閱 [接聽市政位址報表事件](/uwp/api/Windows.Devices.Geolocation)。</span><span class="sxs-lookup"><span data-stu-id="1c7a1-120">For an example of how to use this method, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c7a1-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c7a1-121">Requirements</span></span>



| <span data-ttu-id="1c7a1-122">需求</span><span class="sxs-lookup"><span data-stu-id="1c7a1-122">Requirement</span></span> | <span data-ttu-id="1c7a1-123">值</span><span class="sxs-lookup"><span data-stu-id="1c7a1-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c7a1-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1c7a1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1c7a1-125">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c7a1-125">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1c7a1-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1c7a1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1c7a1-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="1c7a1-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="1c7a1-128">標頭</span><span class="sxs-lookup"><span data-stu-id="1c7a1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c7a1-129"><dt>Locationapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="1c7a1-129"><dt>Locationapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c7a1-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c7a1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c7a1-131">**NewCivicAddressReport 事件**</span><span class="sxs-lookup"><span data-stu-id="1c7a1-131">**NewCivicAddressReport Event**</span></span>](newcivicaddressreport.md)
</dt> </dl>

 

