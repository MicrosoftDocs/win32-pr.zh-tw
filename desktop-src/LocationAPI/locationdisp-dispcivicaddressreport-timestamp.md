---
description: LocationDisp. DispCivicAddressReport. Timestamp 屬性-產生報表的日期和時間。
ms.assetid: b9435384-72e0-42c4-a948-df52621a5ec2
title: LocationDisp. DispCivicAddressReport. Timestamp 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispCivicAddressReport.Timestamp
api_type:
- COM
api_location: ''
ms.openlocfilehash: d2ed39956bb542aa4e150bf9afa3e59a472a4d91
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110876"
---
# <a name="locationdispdispcivicaddressreporttimestamp-property"></a><span data-ttu-id="200b5-103">LocationDisp. DispCivicAddressReport. Timestamp 屬性</span><span class="sxs-lookup"><span data-stu-id="200b5-103">LocationDisp.DispCivicAddressReport.Timestamp property</span></span>

<span data-ttu-id="200b5-104">\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="200b5-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="200b5-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="200b5-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="200b5-106">相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="200b5-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="200b5-107">若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]</span><span class="sxs-lookup"><span data-stu-id="200b5-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="200b5-108">產生報表的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="200b5-108">The date and time when the report was generated.</span></span>

<span data-ttu-id="200b5-109">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="200b5-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="200b5-110">語法</span><span class="sxs-lookup"><span data-stu-id="200b5-110">Syntax</span></span>


```JScript
Timestamp = LocationDisp.DispCivicAddressReport.Timestamp
```



## <a name="property-value"></a><span data-ttu-id="200b5-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="200b5-111">Property value</span></span>

<span data-ttu-id="200b5-112">這個屬性是唯讀 **日期**。</span><span class="sxs-lookup"><span data-stu-id="200b5-112">This property is a read-only **Date**.</span></span> <span data-ttu-id="200b5-113">時間戳記是以國際標準時間 (UTC) 提供。</span><span class="sxs-lookup"><span data-stu-id="200b5-113">Time stamps are provided as Coordinated Universal Time (UTC).</span></span>

## <a name="remarks"></a><span data-ttu-id="200b5-114">備註</span><span class="sxs-lookup"><span data-stu-id="200b5-114">Remarks</span></span>

<span data-ttu-id="200b5-115">請注意，當您將時間戳記顯示為字串時，指令碼語言（例如 Microsoft JScript）可能會要求您執行轉換成其他時間格式。</span><span class="sxs-lookup"><span data-stu-id="200b5-115">Note that scripting languages, such as Microsoft JScript, might require you to perform conversions to other time formats when you display time stamps as strings.</span></span>

## <a name="examples"></a><span data-ttu-id="200b5-116">範例</span><span class="sxs-lookup"><span data-stu-id="200b5-116">Examples</span></span>

<span data-ttu-id="200b5-117">如需如何使用此屬性的範例，請參閱 [簡單的市政位址報告範例](/uwp/api/Windows.Devices.Geolocation)。</span><span class="sxs-lookup"><span data-stu-id="200b5-117">For an example of how to use this property, see [A Simple Civic Address Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="200b5-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="200b5-118">Requirements</span></span>



| <span data-ttu-id="200b5-119">需求</span><span class="sxs-lookup"><span data-stu-id="200b5-119">Requirement</span></span> | <span data-ttu-id="200b5-120">值</span><span class="sxs-lookup"><span data-stu-id="200b5-120">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="200b5-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="200b5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="200b5-122">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="200b5-122">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="200b5-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="200b5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="200b5-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="200b5-124">None supported</span></span><br/>                  |



 

