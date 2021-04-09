---
description: 產生新的市政位址報表時發生。
ms.assetid: a8df870e-6744-4e8a-a103-56b446da135f
title: NewCivicAddressReport 事件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewCivicAddressReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: fa786ecee4ce4223cdb7ec0c8400c5c11bf6e192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852775"
---
# <a name="newcivicaddressreport-event"></a><span data-ttu-id="bbd25-103">NewCivicAddressReport 事件</span><span class="sxs-lookup"><span data-stu-id="bbd25-103">NewCivicAddressReport event</span></span>

<span data-ttu-id="bbd25-104">\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="bbd25-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bbd25-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="bbd25-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="bbd25-106">相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="bbd25-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="bbd25-107">若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]</span><span class="sxs-lookup"><span data-stu-id="bbd25-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="bbd25-108">產生新的市政位址報表時發生。</span><span class="sxs-lookup"><span data-stu-id="bbd25-108">Occurs when a new civic address report is generated.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbd25-109">語法</span><span class="sxs-lookup"><span data-stu-id="bbd25-109">Syntax</span></span>


```JScript
.NewCivicAddressReport(
  newReport
)
```



## <a name="parameters"></a><span data-ttu-id="bbd25-110">參數</span><span class="sxs-lookup"><span data-stu-id="bbd25-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbd25-111">*newReport*</span><span class="sxs-lookup"><span data-stu-id="bbd25-111">*newReport*</span></span> 
</dt> <dd>

<span data-ttu-id="bbd25-112">新的 [**LocationDisp. DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="bbd25-112">The new [**LocationDisp.DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbd25-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="bbd25-113">Return value</span></span>

<span data-ttu-id="bbd25-114">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="bbd25-114">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="bbd25-115">範例</span><span class="sxs-lookup"><span data-stu-id="bbd25-115">Examples</span></span>

<span data-ttu-id="bbd25-116">如需如何使用此事件的範例，請參閱 [接聽市政位址報表事件](/uwp/api/Windows.Devices.Geolocation)。</span><span class="sxs-lookup"><span data-stu-id="bbd25-116">For an example of how to use this event, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="bbd25-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="bbd25-117">Requirements</span></span>



| <span data-ttu-id="bbd25-118">需求</span><span class="sxs-lookup"><span data-stu-id="bbd25-118">Requirement</span></span> | <span data-ttu-id="bbd25-119">值</span><span class="sxs-lookup"><span data-stu-id="bbd25-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="bbd25-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bbd25-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bbd25-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bbd25-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bbd25-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bbd25-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bbd25-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="bbd25-123">None supported</span></span><br/>                  |



 

