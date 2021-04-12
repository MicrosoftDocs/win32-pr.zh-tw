---
description: 當報表的操作狀態變更時發生。
ms.assetid: f0c4e678-1666-4f99-89de-85879eacd0ac
title: StatusChanged 事件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StatusChanged
api_type:
- COM
api_location: ''
ms.openlocfilehash: d1bda6645002f586eda0e2dad99a134450329d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195597"
---
# <a name="statuschanged-event"></a><span data-ttu-id="75710-103">StatusChanged 事件</span><span class="sxs-lookup"><span data-stu-id="75710-103">StatusChanged event</span></span>

<span data-ttu-id="75710-104">\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="75710-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="75710-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="75710-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="75710-106">相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="75710-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="75710-107">若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]</span><span class="sxs-lookup"><span data-stu-id="75710-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="75710-108">當報表的操作狀態變更時發生。</span><span class="sxs-lookup"><span data-stu-id="75710-108">Occurs when the operational status of a report changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="75710-109">語法</span><span class="sxs-lookup"><span data-stu-id="75710-109">Syntax</span></span>


```JScript
.StatusChanged(
  status
)
```



## <a name="parameters"></a><span data-ttu-id="75710-110">參數</span><span class="sxs-lookup"><span data-stu-id="75710-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75710-111">*status*</span><span class="sxs-lookup"><span data-stu-id="75710-111">*status*</span></span> 
</dt> <dd>

<span data-ttu-id="75710-112">新的狀態。</span><span class="sxs-lookup"><span data-stu-id="75710-112">The new status.</span></span>



| <span data-ttu-id="75710-113">狀態</span><span class="sxs-lookup"><span data-stu-id="75710-113">Status</span></span>                                                                                               | <span data-ttu-id="75710-114">意義</span><span class="sxs-lookup"><span data-stu-id="75710-114">Meaning</span></span>                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="75710-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="75710-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="75710-116">不支援報表。</span><span class="sxs-lookup"><span data-stu-id="75710-116">Report not supported.</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="75710-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="75710-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="75710-118">錯誤。</span><span class="sxs-lookup"><span data-stu-id="75710-118">Error.</span></span><br/>                |
| <span id="2"></span><dl> <span data-ttu-id="75710-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="75710-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="75710-120">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="75710-120">Access denied.</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="75710-121"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="75710-121"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="75710-122">正在初始化。</span><span class="sxs-lookup"><span data-stu-id="75710-122">Initializing.</span></span><br/>         |
| <span id="4"></span><dl> <span data-ttu-id="75710-123"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="75710-123"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="75710-124">執行中。</span><span class="sxs-lookup"><span data-stu-id="75710-124">Running.</span></span><br/>              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75710-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="75710-125">Return value</span></span>

<span data-ttu-id="75710-126">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="75710-126">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="75710-127">備註</span><span class="sxs-lookup"><span data-stu-id="75710-127">Remarks</span></span>

<span data-ttu-id="75710-128">您應該針對市政位址報告和緯度/經度報表，執行不同的狀態變更報告處理常式。</span><span class="sxs-lookup"><span data-stu-id="75710-128">You should implement separate status change report handlers for civic address reports and latitude/longitude reports.</span></span>

## <a name="examples"></a><span data-ttu-id="75710-129">範例</span><span class="sxs-lookup"><span data-stu-id="75710-129">Examples</span></span>

<span data-ttu-id="75710-130">如需如何使用此事件的範例，請參閱 [接聽 LatLong 報表事件](/uwp/api/Windows.Devices.Geolocation)。</span><span class="sxs-lookup"><span data-stu-id="75710-130">For an example of how to use this event, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="75710-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="75710-131">Requirements</span></span>



| <span data-ttu-id="75710-132">需求</span><span class="sxs-lookup"><span data-stu-id="75710-132">Requirement</span></span> | <span data-ttu-id="75710-133">值</span><span class="sxs-lookup"><span data-stu-id="75710-133">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="75710-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75710-134">Minimum supported client</span></span><br/> | <span data-ttu-id="75710-135">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75710-135">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="75710-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75710-136">Minimum supported server</span></span><br/> | <span data-ttu-id="75710-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="75710-137">None supported</span></span><br/>                  |



 

