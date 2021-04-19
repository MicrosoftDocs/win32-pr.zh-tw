---
description: 當產生新的緯度/經度報表時發生。
ms.assetid: 2b1a25a1-ccd6-43f8-979b-c2d414d666a2
title: NewLatLongReport 事件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: ea305d17169b71d183a8d453e9885d8de878b026
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975573"
---
# <a name="newlatlongreport-event"></a><span data-ttu-id="b00ee-103">NewLatLongReport 事件</span><span class="sxs-lookup"><span data-stu-id="b00ee-103">NewLatLongReport event</span></span>

<span data-ttu-id="b00ee-104">\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="b00ee-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b00ee-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="b00ee-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b00ee-106">相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b00ee-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="b00ee-107">若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]</span><span class="sxs-lookup"><span data-stu-id="b00ee-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="b00ee-108">當產生新的緯度/經度報表時發生。</span><span class="sxs-lookup"><span data-stu-id="b00ee-108">Occurs when a new latitude/longitude report is generated.</span></span>

## <a name="syntax"></a><span data-ttu-id="b00ee-109">語法</span><span class="sxs-lookup"><span data-stu-id="b00ee-109">Syntax</span></span>


```JScript
.NewLatLongReport(
  newReport
)
```



## <a name="parameters"></a><span data-ttu-id="b00ee-110">參數</span><span class="sxs-lookup"><span data-stu-id="b00ee-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b00ee-111">*newReport*</span><span class="sxs-lookup"><span data-stu-id="b00ee-111">*newReport*</span></span> 
</dt> <dd>

<span data-ttu-id="b00ee-112">新的 [**LocationDisp. DispLatLongReport**](locationdisp-displatlongreport.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="b00ee-112">The new [**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b00ee-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b00ee-113">Return value</span></span>

<span data-ttu-id="b00ee-114">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b00ee-114">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="b00ee-115">範例</span><span class="sxs-lookup"><span data-stu-id="b00ee-115">Examples</span></span>

<span data-ttu-id="b00ee-116">如需如何使用此事件的範例，請參閱 [接聽 LatLong 報表事件](/uwp/api/Windows.Devices.Geolocation)。</span><span class="sxs-lookup"><span data-stu-id="b00ee-116">For an example of how to use this event, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="b00ee-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b00ee-117">Requirements</span></span>



| <span data-ttu-id="b00ee-118">需求</span><span class="sxs-lookup"><span data-stu-id="b00ee-118">Requirement</span></span> | <span data-ttu-id="b00ee-119">值</span><span class="sxs-lookup"><span data-stu-id="b00ee-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="b00ee-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b00ee-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b00ee-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b00ee-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b00ee-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b00ee-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b00ee-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="b00ee-123">None supported</span></span><br/>                  |



 

