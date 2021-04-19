---
description: 目前的報表狀態。
ms.assetid: 3aae0b61-cdaa-4131-b6e1-406813bb1848
title: LocationDisp. CivicAddressReportFactory. Status 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: ff937b11fbb64e0ec1596f9b3b9d85b33528eb06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976566"
---
# <a name="locationdispcivicaddressreportfactorystatus-property"></a><span data-ttu-id="5d0f3-103">LocationDisp. CivicAddressReportFactory. Status 屬性</span><span class="sxs-lookup"><span data-stu-id="5d0f3-103">LocationDisp.CivicAddressReportFactory.Status property</span></span>

<span data-ttu-id="5d0f3-104">\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="5d0f3-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5d0f3-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="5d0f3-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="5d0f3-106">相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="5d0f3-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="5d0f3-107">若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]</span><span class="sxs-lookup"><span data-stu-id="5d0f3-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="5d0f3-108">目前的報表狀態。</span><span class="sxs-lookup"><span data-stu-id="5d0f3-108">The current report status.</span></span>

<span data-ttu-id="5d0f3-109">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="5d0f3-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d0f3-110">語法</span><span class="sxs-lookup"><span data-stu-id="5d0f3-110">Syntax</span></span>


```JScript
Status = LocationDisp.CivicAddressReportFactory.Status
```



## <a name="property-value"></a><span data-ttu-id="5d0f3-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="5d0f3-111">Property value</span></span>

<span data-ttu-id="5d0f3-112">這個屬性是唯讀的 (不帶正負 **號** 的長) 。</span><span class="sxs-lookup"><span data-stu-id="5d0f3-112">This property is a read-only **Number** (unsigned long).</span></span>



| <span data-ttu-id="5d0f3-113">狀態</span><span class="sxs-lookup"><span data-stu-id="5d0f3-113">Status</span></span>                                                                                               | <span data-ttu-id="5d0f3-114">意義</span><span class="sxs-lookup"><span data-stu-id="5d0f3-114">Meaning</span></span>                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="5d0f3-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="5d0f3-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="5d0f3-116">不支援報表。</span><span class="sxs-lookup"><span data-stu-id="5d0f3-116">Report not supported.</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="5d0f3-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="5d0f3-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="5d0f3-118">錯誤。</span><span class="sxs-lookup"><span data-stu-id="5d0f3-118">Error.</span></span><br/>                |
| <span id="2"></span><dl> <span data-ttu-id="5d0f3-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="5d0f3-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="5d0f3-120">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="5d0f3-120">Access denied.</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="5d0f3-121"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="5d0f3-121"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="5d0f3-122">正在初始化。</span><span class="sxs-lookup"><span data-stu-id="5d0f3-122">Initializing.</span></span><br/>         |
| <span id="4"></span><dl> <span data-ttu-id="5d0f3-123"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="5d0f3-123"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="5d0f3-124">執行中。</span><span class="sxs-lookup"><span data-stu-id="5d0f3-124">Running.</span></span><br/>              |



 

## <a name="examples"></a><span data-ttu-id="5d0f3-125">範例</span><span class="sxs-lookup"><span data-stu-id="5d0f3-125">Examples</span></span>

<span data-ttu-id="5d0f3-126">如需如何使用這個屬性的範例，請參閱 [接聽市政位址報表事件](/uwp/api/Windows.Devices.Geolocation)。</span><span class="sxs-lookup"><span data-stu-id="5d0f3-126">For an example of how to use this property, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d0f3-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d0f3-127">Requirements</span></span>



| <span data-ttu-id="5d0f3-128">需求</span><span class="sxs-lookup"><span data-stu-id="5d0f3-128">Requirement</span></span> | <span data-ttu-id="5d0f3-129">值</span><span class="sxs-lookup"><span data-stu-id="5d0f3-129">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="5d0f3-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d0f3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5d0f3-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d0f3-131">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5d0f3-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d0f3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5d0f3-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="5d0f3-133">None supported</span></span><br/>                  |



 

