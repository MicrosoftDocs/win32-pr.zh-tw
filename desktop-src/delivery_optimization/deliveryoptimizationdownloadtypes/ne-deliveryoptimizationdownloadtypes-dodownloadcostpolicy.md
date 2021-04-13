---
title: DODownloadCostPolicy 列舉
description: 指定與 **DODownloadProperty_CostPolicy** 屬性相關聯之成本原則選項的識別碼。
keywords:
- DODownloadCostPolicy 列舉，DODownloadCostPolicy
topic_type:
- apiref
api_name:
- DODownloadCostPolicy
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: c70384f7c7da1633b910db36c42a335d1c463bae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383998"
---
# <a name="dodownloadcostpolicy-enumeration"></a><span data-ttu-id="120a7-104">DODownloadCostPolicy 列舉</span><span class="sxs-lookup"><span data-stu-id="120a7-104">DODownloadCostPolicy enumeration</span></span>

<span data-ttu-id="120a7-105">**DODownloadCostPolicy** 列舉會指定與 **DODownloadProperty_CostPolicy** 屬性相關聯之成本原則選項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="120a7-105">The **DODownloadCostPolicy** enumeration specifies the ID of cost policies options associated with the **DODownloadProperty_CostPolicy** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="120a7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="120a7-106">Syntax</span></span>

```cpp
typedef enum _DODownloadCostPolicy
{
  DODownloadCostPolicy_Always = 0,
  DODownloadCostPolicy_Unrestricted,
  DODownloadCostPolicy_Standard,    
  DODownloadCostPolicy_NoRoaming,   
  DODownloadCostPolicy_NoSurcharge, 
  DODownloadCostPolicy_NoCellular
} DODownloadCostPolicy;
```

## <a name="constants"></a><span data-ttu-id="120a7-107">常數</span><span class="sxs-lookup"><span data-stu-id="120a7-107">Constants</span></span>

| <span data-ttu-id="120a7-108">需求</span><span class="sxs-lookup"><span data-stu-id="120a7-108">Requirement</span></span> | <span data-ttu-id="120a7-109">值</span><span class="sxs-lookup"><span data-stu-id="120a7-109">Value</span></span> |
|-|-|
| <span data-ttu-id="120a7-110">DODownloadCostPolicy_Always</span><span class="sxs-lookup"><span data-stu-id="120a7-110">DODownloadCostPolicy_Always</span></span> | <span data-ttu-id="120a7-111">無論成本為何，都可執行下載。</span><span class="sxs-lookup"><span data-stu-id="120a7-111">Download runs regardless of the cost.</span></span> |
| <span data-ttu-id="120a7-112">DODownloadCostPolicy_Unrestricted</span><span class="sxs-lookup"><span data-stu-id="120a7-112">DODownloadCostPolicy_Unrestricted</span></span> | <span data-ttu-id="120a7-113">除非強加成本或流量限制，否則會執行下載。</span><span class="sxs-lookup"><span data-stu-id="120a7-113">Download runs unless imposes costs or traffic limits.</span></span> |
| <span data-ttu-id="120a7-114">DODownloadCostPolicy_Standard</span><span class="sxs-lookup"><span data-stu-id="120a7-114">DODownloadCostPolicy_Standard</span></span> | <span data-ttu-id="120a7-115">除非沒有額外費用或接近耗盡的情況，否則請下載執行。</span><span class="sxs-lookup"><span data-stu-id="120a7-115">Download runs unless neither subject to a surcharge nor near exhaustion.</span></span> |
| <span data-ttu-id="120a7-116">DODownloadCostPolicy_NoRoaming</span><span class="sxs-lookup"><span data-stu-id="120a7-116">DODownloadCostPolicy_NoRoaming</span></span> | <span data-ttu-id="120a7-117">下載執行，除非連線受限於漫遊的附加費。</span><span class="sxs-lookup"><span data-stu-id="120a7-117">Download runs unless that connectivity is subject to roaming surcharges.</span></span> |
| <span data-ttu-id="120a7-118">DODownloadCostPolicy_NoSurcharge</span><span class="sxs-lookup"><span data-stu-id="120a7-118">DODownloadCostPolicy_NoSurcharge</span></span> | <span data-ttu-id="120a7-119">下載執行，除非有額外費用。</span><span class="sxs-lookup"><span data-stu-id="120a7-119">Download runs unless subject to a surcharge.</span></span> |
| <span data-ttu-id="120a7-120">DODownloadCostPolicy_NoCellular</span><span class="sxs-lookup"><span data-stu-id="120a7-120">DODownloadCostPolicy_NoCellular</span></span> | <span data-ttu-id="120a7-121">除非網路在行動電話上，否則會執行下載。</span><span class="sxs-lookup"><span data-stu-id="120a7-121">Download runs unless network is on cellular.</span></span> |

## <a name="requirements"></a><span data-ttu-id="120a7-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="120a7-122">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="120a7-123">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="120a7-123">**Minimum supported client**</span></span> | <span data-ttu-id="120a7-124">\[僅限 Windows 10 版本1809的 Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="120a7-124">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="120a7-125">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="120a7-125">**Minimum supported server**</span></span> | <span data-ttu-id="120a7-126">Windows Server，僅限1809版的 \[ Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="120a7-126">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="120a7-127">**標頭**</span><span class="sxs-lookup"><span data-stu-id="120a7-127">**Header**</span></span> | <span data-ttu-id="120a7-128">DeliveryOptimizationDownloadTypes。h</span><span class="sxs-lookup"><span data-stu-id="120a7-128">DeliveryOptimizationDownloadTypes.h</span></span> |
