---
title: DXCoreSegmentGroup
description: 定義常數，指定介面卡的記憶體區段群組。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ce94d5f806879ea84f64c88d3a62b074a5c5415b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969111"
---
# <a name="dxcoresegmentgroup-enum"></a><span data-ttu-id="afa44-103">DXCoreSegmentGroup 列舉</span><span class="sxs-lookup"><span data-stu-id="afa44-103">DXCoreSegmentGroup enum</span></span>

<span data-ttu-id="afa44-104">定義常數，指定介面卡的記憶體區段群組。</span><span class="sxs-lookup"><span data-stu-id="afa44-104">Defines constants that specify an adapter's memory segment grouping.</span></span>

## <a name="syntax"></a><span data-ttu-id="afa44-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="afa44-105">Syntax</span></span>

```cpp
enum class DXCoreSegmentGroup : uint32_t
{
  Local = 0,
  NonLocal = 1
};
```

## <a name="constants"></a><span data-ttu-id="afa44-106">常數</span><span class="sxs-lookup"><span data-stu-id="afa44-106">Constants</span></span>

### <a name="local"></a><span data-ttu-id="afa44-107">本機</span><span class="sxs-lookup"><span data-stu-id="afa44-107">Local</span></span>

<span data-ttu-id="afa44-108">指定視為介面卡區域的區段群組，並代表 GPU 可用的最快記憶體。</span><span class="sxs-lookup"><span data-stu-id="afa44-108">Specifies a grouping of segments that is considered local to the adapter, and represents the fastest memory available to the GPU.</span></span> <span data-ttu-id="afa44-109">您的應用程式應該將本機區段群組的目標設為其工作集的目標大小。</span><span class="sxs-lookup"><span data-stu-id="afa44-109">Your application should target the local segment group as the target size for its working set.</span></span>

### <a name="nonlocal"></a><span data-ttu-id="afa44-110">外地</span><span class="sxs-lookup"><span data-stu-id="afa44-110">NonLocal</span></span>

<span data-ttu-id="afa44-111">指定視為非本機的區段群組，且效能可能會比本機區段群組更慢。</span><span class="sxs-lookup"><span data-stu-id="afa44-111">Specifies a grouping of segments that is considered non-local to the adapter, and may have slower performance than the local segment group.</span></span>

## <a name="see-also"></a><span data-ttu-id="afa44-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afa44-112">See also</span></span>

<span data-ttu-id="afa44-113">[DXCore 參考](../dxcore-reference.md)， [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="afa44-113">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>