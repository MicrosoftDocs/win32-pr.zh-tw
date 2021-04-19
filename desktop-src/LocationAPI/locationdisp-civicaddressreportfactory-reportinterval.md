---
description: 目前的市政位址報告事件間隔（以毫秒為單位）。
ms.assetid: 495dd8a1-4244-468f-b295-337b393aea8a
title: LocationDisp. CivicAddressReportFactory. ReportInterval 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: 47f7840be20ac640b5a8e7014f8401bc2350d328
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978180"
---
# <a name="locationdispcivicaddressreportfactoryreportinterval-property"></a><span data-ttu-id="d9b24-103">LocationDisp. CivicAddressReportFactory. ReportInterval 屬性</span><span class="sxs-lookup"><span data-stu-id="d9b24-103">LocationDisp.CivicAddressReportFactory.ReportInterval property</span></span>

<span data-ttu-id="d9b24-104">\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="d9b24-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d9b24-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="d9b24-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="d9b24-106">相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d9b24-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="d9b24-107">若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]</span><span class="sxs-lookup"><span data-stu-id="d9b24-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="d9b24-108">目前的市政位址報告事件間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d9b24-108">The current civic address report event interval in milliseconds.</span></span>

<span data-ttu-id="d9b24-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="d9b24-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9b24-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9b24-110">Syntax</span></span>


```JScript
ReportInterval = LocationDisp.CivicAddressReportFactory.ReportInterval
LocationDisp.CivicAddressReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a><span data-ttu-id="d9b24-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="d9b24-111">Property value</span></span>

<span data-ttu-id="d9b24-112">這個屬性是讀取/寫入的 **ULONG**。</span><span class="sxs-lookup"><span data-stu-id="d9b24-112">This property is a read/write **ULONG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9b24-113">備註</span><span class="sxs-lookup"><span data-stu-id="d9b24-113">Remarks</span></span>

<span data-ttu-id="d9b24-114">此值是位置提供者的要求。</span><span class="sxs-lookup"><span data-stu-id="d9b24-114">This value is a request for the location provider.</span></span> <span data-ttu-id="d9b24-115">位置提供者不需要在您要求的間隔提供報告。</span><span class="sxs-lookup"><span data-stu-id="d9b24-115">The location provider is not required to provide reports at the interval that you requested.</span></span> <span data-ttu-id="d9b24-116">讀取這個屬性的值，以探索真正的報表間隔設定。</span><span class="sxs-lookup"><span data-stu-id="d9b24-116">Read the value of this property to discover the true report interval setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9b24-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9b24-117">Requirements</span></span>



| <span data-ttu-id="d9b24-118">需求</span><span class="sxs-lookup"><span data-stu-id="d9b24-118">Requirement</span></span> | <span data-ttu-id="d9b24-119">值</span><span class="sxs-lookup"><span data-stu-id="d9b24-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="d9b24-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d9b24-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d9b24-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d9b24-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d9b24-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d9b24-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d9b24-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="d9b24-123">None supported</span></span><br/>                  |



 

