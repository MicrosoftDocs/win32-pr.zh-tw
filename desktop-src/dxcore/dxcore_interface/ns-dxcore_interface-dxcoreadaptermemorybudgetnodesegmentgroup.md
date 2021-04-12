---
title: DXCoreAdapterMemoryBudgetNodeSegmentGroup
description: 描述介面卡的記憶體區段群組。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c583b746b304232fc65c4281f67b0190b2d24c3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375601"
---
# <a name="dxcoreadaptermemorybudgetnodesegmentgroup-structure"></a><span data-ttu-id="ad28c-103">DXCoreAdapterMemoryBudgetNodeSegmentGroup 結構</span><span class="sxs-lookup"><span data-stu-id="ad28c-103">DXCoreAdapterMemoryBudgetNodeSegmentGroup structure</span></span>

<span data-ttu-id="ad28c-104">描述介面卡的記憶體區段群組。</span><span class="sxs-lookup"><span data-stu-id="ad28c-104">Describes a memory segment group for an adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad28c-105">語法</span><span class="sxs-lookup"><span data-stu-id="ad28c-105">Syntax</span></span>

```cpp
struct DXCoreAdapterMemoryBudgetNodeSegmentGroup
{
  uint32_t nodeIndex;
  DXCoreSegmentGroup segmentGroup;
};
```

## <a name="members"></a><span data-ttu-id="ad28c-106">成員</span><span class="sxs-lookup"><span data-stu-id="ad28c-106">Members</span></span>

### <a name="nodeindex"></a><span data-ttu-id="ad28c-107">nodeIndex</span><span class="sxs-lookup"><span data-stu-id="ad28c-107">nodeIndex</span></span>

<span data-ttu-id="ad28c-108">類型： **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="ad28c-108">Type: **uint32_t**</span></span>

<span data-ttu-id="ad28c-109">指定要查詢其介面卡記憶體資訊的裝置實體介面卡。</span><span class="sxs-lookup"><span data-stu-id="ad28c-109">Specifies the device's physical adapter for which the adapter memory information is queried.</span></span> <span data-ttu-id="ad28c-110">若為單一介面卡操作，請將此設定為零。</span><span class="sxs-lookup"><span data-stu-id="ad28c-110">For single-adapter operation, set this to zero.</span></span> <span data-ttu-id="ad28c-111">如果有多個介面卡節點，請將此設定為節點的索引， (您要查詢其介面卡記憶體資訊之裝置的實體介面卡)  (查看 [多個介面卡系統](../../direct3d12/multi-engine.md)) 。</span><span class="sxs-lookup"><span data-stu-id="ad28c-111">If there are multiple adapter nodes, then set this to the index of the node (the device's physical adapter) for which you want to query for adapter memory information (see [Multi-adapter systems](../../direct3d12/multi-engine.md)).</span></span>

### <a name="segmentgroup"></a><span data-ttu-id="ad28c-112">segmentGroup</span><span class="sxs-lookup"><span data-stu-id="ad28c-112">segmentGroup</span></span>

<span data-ttu-id="ad28c-113">類型： **[DXCoreSegmentGroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**</span><span class="sxs-lookup"><span data-stu-id="ad28c-113">Type: **[DXCoreSegmentGroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**</span></span>

<span data-ttu-id="ad28c-114">指定您想要查詢的介面卡記憶體區段群組。</span><span class="sxs-lookup"><span data-stu-id="ad28c-114">Specifies the adapter memory segment grouping that you want to query about.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad28c-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad28c-115">See also</span></span>

[<span data-ttu-id="ad28c-116">DXCore 參考</span><span class="sxs-lookup"><span data-stu-id="ad28c-116">DXCore Reference</span></span>](../dxcore-reference.md)

[<span data-ttu-id="ad28c-117">使用 DXCore 來列舉介面卡</span><span class="sxs-lookup"><span data-stu-id="ad28c-117">Using DXCore to enumerate adapters</span></span>](../dxcore-enum-adapters.md)

[<span data-ttu-id="ad28c-118">多個介面卡系統</span><span class="sxs-lookup"><span data-stu-id="ad28c-118">Multi-adapter systems</span></span>](../../direct3d12/multi-engine.md)