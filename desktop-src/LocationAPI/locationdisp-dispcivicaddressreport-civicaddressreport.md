---
description: 目前的市政位址報表。
ms.assetid: a58dd612-bc54-42d1-9960-8c3de1c4fa83
title: 'LocationDisp. CivicAddressReportFactory. CivicAddressReport 屬性 (Locationapi .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.CivicAddressReport
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: c8be6e03861f1c5b2abffcb4b23d4845defa494e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999923"
---
# <a name="locationdispcivicaddressreportfactorycivicaddressreport-property"></a><span data-ttu-id="967ab-103">LocationDisp. CivicAddressReportFactory. CivicAddressReport 屬性</span><span class="sxs-lookup"><span data-stu-id="967ab-103">LocationDisp.CivicAddressReportFactory.CivicAddressReport property</span></span>

<span data-ttu-id="967ab-104">\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="967ab-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="967ab-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="967ab-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="967ab-106">相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="967ab-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="967ab-107">若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]</span><span class="sxs-lookup"><span data-stu-id="967ab-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="967ab-108">目前的市政位址報表。</span><span class="sxs-lookup"><span data-stu-id="967ab-108">The current civic address report.</span></span>

<span data-ttu-id="967ab-109">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="967ab-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="967ab-110">語法</span><span class="sxs-lookup"><span data-stu-id="967ab-110">Syntax</span></span>


```JScript
objCivicAddressReport = LocationDisp.CivicAddressReportFactory.CivicAddressReport
```



## <a name="property-value"></a><span data-ttu-id="967ab-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="967ab-111">Property value</span></span>

<span data-ttu-id="967ab-112">這個屬性是唯讀的 [**LocationDisp. CivicAddressReportFactory**](locationdisp-civicaddressreportfactory.md)。</span><span class="sxs-lookup"><span data-stu-id="967ab-112">This property is a read-only [**LocationDisp.CivicAddressReportFactory**](locationdisp-civicaddressreportfactory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="967ab-113">範例</span><span class="sxs-lookup"><span data-stu-id="967ab-113">Examples</span></span>

<span data-ttu-id="967ab-114">如需如何使用此屬性的範例，請參閱 [簡單的市政位址報告範例](/uwp/api/Windows.Devices.Geolocation)。</span><span class="sxs-lookup"><span data-stu-id="967ab-114">For an example of how to use this property, see [A Simple Civic Address Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="967ab-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="967ab-115">Requirements</span></span>



| <span data-ttu-id="967ab-116">需求</span><span class="sxs-lookup"><span data-stu-id="967ab-116">Requirement</span></span> | <span data-ttu-id="967ab-117">值</span><span class="sxs-lookup"><span data-stu-id="967ab-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="967ab-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="967ab-118">Minimum supported client</span></span><br/> | <span data-ttu-id="967ab-119">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="967ab-119">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="967ab-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="967ab-120">Minimum supported server</span></span><br/> | <span data-ttu-id="967ab-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="967ab-121">None supported</span></span><br/>                                                                |
| <span data-ttu-id="967ab-122">標頭</span><span class="sxs-lookup"><span data-stu-id="967ab-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="967ab-123"><dt>Locationapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="967ab-123"><dt>Locationapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="967ab-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="967ab-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="967ab-125">**LocationDisp.CivicAddressReportFactory**</span><span class="sxs-lookup"><span data-stu-id="967ab-125">**LocationDisp.CivicAddressReportFactory**</span></span>](locationdisp-civicaddressreportfactory.md)
</dt> </dl>

 

