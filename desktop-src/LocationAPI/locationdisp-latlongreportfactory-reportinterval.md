---
description: 目前的緯度/經度報表事件間隔（以毫秒為單位）。
ms.assetid: bb33c4c1-805d-4519-8363-b0221d420b36
title: LocationDisp. LatLongReportFactory. ReportInterval 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: b456f69a70655b22b1eca30e02d9d5369d19f38c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193316"
---
# <a name="locationdisplatlongreportfactoryreportinterval-property"></a><span data-ttu-id="2f2c4-103">LocationDisp. LatLongReportFactory. ReportInterval 屬性</span><span class="sxs-lookup"><span data-stu-id="2f2c4-103">LocationDisp.LatLongReportFactory.ReportInterval property</span></span>

<span data-ttu-id="2f2c4-104">\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="2f2c4-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2f2c4-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="2f2c4-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="2f2c4-106">相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="2f2c4-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="2f2c4-107">若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]</span><span class="sxs-lookup"><span data-stu-id="2f2c4-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="2f2c4-108">目前的緯度/經度報表事件間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="2f2c4-108">The current latitude/longitude report event interval in milliseconds.</span></span>

<span data-ttu-id="2f2c4-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="2f2c4-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f2c4-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f2c4-110">Syntax</span></span>


```JScript
ReportInterval = LocationDisp.LatLongReportFactory.ReportInterval
LocationDisp.LatLongReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a><span data-ttu-id="2f2c4-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="2f2c4-111">Property value</span></span>

<span data-ttu-id="2f2c4-112">這個屬性是讀取/寫入的 **ULONG**。</span><span class="sxs-lookup"><span data-stu-id="2f2c4-112">This property is a read/write **ULONG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f2c4-113">備註</span><span class="sxs-lookup"><span data-stu-id="2f2c4-113">Remarks</span></span>

<span data-ttu-id="2f2c4-114">此值是對位置提供者的要求。</span><span class="sxs-lookup"><span data-stu-id="2f2c4-114">This value is a request to the location provider.</span></span> <span data-ttu-id="2f2c4-115">位置提供者不需要在您要求的間隔提供報告。</span><span class="sxs-lookup"><span data-stu-id="2f2c4-115">The location provider is not required to provide reports at the interval that you request.</span></span> <span data-ttu-id="2f2c4-116">讀取這個屬性的值，以探索真正的報表間隔設定。</span><span class="sxs-lookup"><span data-stu-id="2f2c4-116">Read the value of this property to discover the true report interval setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f2c4-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f2c4-117">Requirements</span></span>



| <span data-ttu-id="2f2c4-118">需求</span><span class="sxs-lookup"><span data-stu-id="2f2c4-118">Requirement</span></span> | <span data-ttu-id="2f2c4-119">值</span><span class="sxs-lookup"><span data-stu-id="2f2c4-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="2f2c4-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f2c4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2f2c4-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f2c4-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2f2c4-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f2c4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2f2c4-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="2f2c4-123">None supported</span></span><br/>                  |



 

