---
description: 用於任何命中的著色器，以認可目前的點擊次數，然後停止搜尋光線的更多叫用。
ms.assetid: ''
title: AcceptHitAndEndSearch 函式
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- AcceptHitAndEndSearch
api_type:
- NA
ms.openlocfilehash: 25bbac15a26beb535a91155cdd4c411c3c669e0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999836"
---
# <a name="accepthitandendsearch-function"></a><span data-ttu-id="2ad73-103">AcceptHitAndEndSearch 函式</span><span class="sxs-lookup"><span data-stu-id="2ad73-103">AcceptHitAndEndSearch function</span></span>

<span data-ttu-id="2ad73-104">用於 [任何命中的著色器](any-hit-shader.md) ，以認可目前的點擊次數，然後停止搜尋光線的更多叫用。</span><span class="sxs-lookup"><span data-stu-id="2ad73-104">Used in an [any hit shader](any-hit-shader.md) to commit the current hit and then stop searching for more hits for the ray.</span></span> <span data-ttu-id="2ad73-105">如果有交集著色器正在執行，則會停止執行。</span><span class="sxs-lookup"><span data-stu-id="2ad73-105">If there is an intersection shader running, it's execution stops.</span></span>  <span data-ttu-id="2ad73-106">執行會傳遞至 [最接近的點擊著色器](closest-hit-shader.md)（若已啟用），並在目前為止記錄最接近的點擊。</span><span class="sxs-lookup"><span data-stu-id="2ad73-106">Execution passes to the [closest hit shader](closest-hit-shader.md), if enabled, with the closest hit recorded so far.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ad73-107">語法</span><span class="sxs-lookup"><span data-stu-id="2ad73-107">Syntax</span></span>

```
void AcceptHitAndEndSearch();
```




## <a name="return-value"></a><span data-ttu-id="2ad73-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="2ad73-108">Return Value</span></span>

<span data-ttu-id="2ad73-109">**void**</span><span class="sxs-lookup"><span data-stu-id="2ad73-109">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="2ad73-110">備註</span><span class="sxs-lookup"><span data-stu-id="2ad73-110">Remarks</span></span>

<span data-ttu-id="2ad73-111">您可以從下列 raytracing 著色器類型呼叫這個函數：</span><span class="sxs-lookup"><span data-stu-id="2ad73-111">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="2ad73-112">**可呼叫著色器**</span><span class="sxs-lookup"><span data-stu-id="2ad73-112">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="2ad73-113">**最接近的點擊著色器**</span><span class="sxs-lookup"><span data-stu-id="2ad73-113">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="2ad73-114">**遺漏著色器**</span><span class="sxs-lookup"><span data-stu-id="2ad73-114">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="2ad73-115">**光線產生著色器**</span><span class="sxs-lookup"><span data-stu-id="2ad73-115">**Ray Generation Shader**</span></span>](ray-generation-shader.md)



## <a name="see-also"></a><span data-ttu-id="2ad73-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ad73-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ad73-117">Direct3D 12 Raytracing HLSL 參考</span><span class="sxs-lookup"><span data-stu-id="2ad73-117">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




