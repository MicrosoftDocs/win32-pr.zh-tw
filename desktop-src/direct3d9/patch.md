---
description: 定義 B&\# 233; zier 控制項修補程式。 陣列會定義修補程式的控制點。
ms.assetid: vs|directx_sdk|~\patch.htm
title: Patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480457b3dd3800aca8b23210e3fe653b4e713e94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845739"
---
# <a name="patch"></a><span data-ttu-id="7171d-104">Patch</span><span class="sxs-lookup"><span data-stu-id="7171d-104">Patch</span></span>

<span data-ttu-id="7171d-105">定義貝塞爾控制項修補程式。</span><span class="sxs-lookup"><span data-stu-id="7171d-105">Defines a Bézier control patch.</span></span> <span data-ttu-id="7171d-106">陣列會定義修補程式的控制點。</span><span class="sxs-lookup"><span data-stu-id="7171d-106">The array defines the control points for the patch.</span></span>

``` syntax
template Patch
{
    < A3EB5D44-FC22-429D-9AFB-3221CB9719A6 >
    DWORD nControlIndices;
    array DWORD controlIndices[nControlIndices];
} 
```

<span data-ttu-id="7171d-107">其中：</span><span class="sxs-lookup"><span data-stu-id="7171d-107">Where:</span></span>

-   <span data-ttu-id="7171d-108">nControlIndices-控制點索引的數目。</span><span class="sxs-lookup"><span data-stu-id="7171d-108">nControlIndices - Number of control point indices.</span></span>
-   <span data-ttu-id="7171d-109">陣列 DWORD controlIndices \[ nControlIndices \] -控制點索引的陣列。</span><span class="sxs-lookup"><span data-stu-id="7171d-109">array DWORD controlIndices\[nControlIndices\] - Array of control point indices.</span></span>

<span data-ttu-id="7171d-110">修補程式的類型是由控制點的數目所定義，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="7171d-110">The type of patch is defined by the number of control points, as shown in the following table.</span></span>



| <span data-ttu-id="7171d-111">控制點數目</span><span class="sxs-lookup"><span data-stu-id="7171d-111">Number of control points</span></span> | <span data-ttu-id="7171d-112">類型</span><span class="sxs-lookup"><span data-stu-id="7171d-112">Type</span></span>                              |
|--------------------------|-----------------------------------|
| <span data-ttu-id="7171d-113">10</span><span class="sxs-lookup"><span data-stu-id="7171d-113">10</span></span>                       | <span data-ttu-id="7171d-114">三次貝塞爾三角形 patch</span><span class="sxs-lookup"><span data-stu-id="7171d-114">Cubic Bézier triangular patch</span></span>     |
| <span data-ttu-id="7171d-115">15</span><span class="sxs-lookup"><span data-stu-id="7171d-115">15</span></span>                       | <span data-ttu-id="7171d-116">Quartic 貝塞爾三角形 patch</span><span class="sxs-lookup"><span data-stu-id="7171d-116">Quartic Bézier triangular patch</span></span>   |
| <span data-ttu-id="7171d-117">16</span><span class="sxs-lookup"><span data-stu-id="7171d-117">16</span></span>                       | <span data-ttu-id="7171d-118">三次方貝塞爾四個矩形修補程式</span><span class="sxs-lookup"><span data-stu-id="7171d-118">Cubic Bézier quad rectangle patch</span></span> |



 

<span data-ttu-id="7171d-119">控制點的順序會以螺旋線模式提供，如下圖所示，適用于三角形和矩形的修補程式。</span><span class="sxs-lookup"><span data-stu-id="7171d-119">The order of the control points are given in a spiral pattern, as shown in the following diagrams for triangular and rectangular patches.</span></span>

<span data-ttu-id="7171d-120">三角修補程式使用下列模式。</span><span class="sxs-lookup"><span data-stu-id="7171d-120">Triangular patches use the following pattern.</span></span>

![三角化修補程式模式的圖表](images/tripatch.png)

<span data-ttu-id="7171d-122">矩形修補程式使用下列模式。</span><span class="sxs-lookup"><span data-stu-id="7171d-122">Rectangular patches use the following pattern.</span></span>

![矩形修補程式模式的圖表](images/quadpatch.png)

## <a name="see-also"></a><span data-ttu-id="7171d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7171d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7171d-125">範本</span><span class="sxs-lookup"><span data-stu-id="7171d-125">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



