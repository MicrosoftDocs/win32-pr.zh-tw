---
description: 應用程式會藉由呼叫 CombineRgn 函數來合併兩個區域。
ms.assetid: d16f9ca5-33e2-4752-900e-743245838377
title: 結合區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f51db22daea448acfb02120844ca2859a5ba11e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566481"
---
# <a name="combining-regions"></a><span data-ttu-id="f9e19-103">結合區域</span><span class="sxs-lookup"><span data-stu-id="f9e19-103">Combining Regions</span></span>

<span data-ttu-id="f9e19-104">應用程式會藉由呼叫 [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) 函數來合併兩個區域。</span><span class="sxs-lookup"><span data-stu-id="f9e19-104">An application combines two regions by calling the [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) function.</span></span> <span data-ttu-id="f9e19-105">使用這個函式，應用程式可以結合兩個區域的交集部分，除了兩個區域的交集部分、整體的兩個原始區域等等。</span><span class="sxs-lookup"><span data-stu-id="f9e19-105">Using this function, an application can combine the intersecting parts of two regions, all but the intersecting parts of two regions, the two original regions in their entirety, and so on.</span></span> <span data-ttu-id="f9e19-106">以下是定義區域組合的五個值。</span><span class="sxs-lookup"><span data-stu-id="f9e19-106">Following are five values that define the region combinations.</span></span>



| <span data-ttu-id="f9e19-107">值</span><span class="sxs-lookup"><span data-stu-id="f9e19-107">Value</span></span>     | <span data-ttu-id="f9e19-108">意義</span><span class="sxs-lookup"><span data-stu-id="f9e19-108">Meaning</span></span>                                                                               |
|-----------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9e19-109">R G N \_ 和</span><span class="sxs-lookup"><span data-stu-id="f9e19-109">RGN\_AND</span></span>  | <span data-ttu-id="f9e19-110">兩個原始區域的交集部分會定義新的區域。</span><span class="sxs-lookup"><span data-stu-id="f9e19-110">The intersecting parts of two original regions define a new region.</span></span>                   |
| <span data-ttu-id="f9e19-111">R G N \_ 複製</span><span class="sxs-lookup"><span data-stu-id="f9e19-111">RGN\_COPY</span></span> | <span data-ttu-id="f9e19-112">這兩個原始區域的第一個 (複本) 會定義新的區域。</span><span class="sxs-lookup"><span data-stu-id="f9e19-112">A copy of the first (of the two original regions) defines a new region.</span></span>               |
| <span data-ttu-id="f9e19-113">R G N \_ 差異</span><span class="sxs-lookup"><span data-stu-id="f9e19-113">RGN\_DIFF</span></span> | <span data-ttu-id="f9e19-114">第一個區域中未與第二個區域相交的部分會定義新的區域。</span><span class="sxs-lookup"><span data-stu-id="f9e19-114">The part of the first region that does not intersect the second defines a new region.</span></span> |
| <span data-ttu-id="f9e19-115">R G N \_ 或</span><span class="sxs-lookup"><span data-stu-id="f9e19-115">RGN\_OR</span></span>   | <span data-ttu-id="f9e19-116">這兩個原始區域會定義新的區域。</span><span class="sxs-lookup"><span data-stu-id="f9e19-116">The two original regions define a new region.</span></span>                                         |
| <span data-ttu-id="f9e19-117">R G N \_ XOR</span><span class="sxs-lookup"><span data-stu-id="f9e19-117">RGN\_XOR</span></span>  | <span data-ttu-id="f9e19-118">兩個不重迭的原始區域中的部分會定義新的區域。</span><span class="sxs-lookup"><span data-stu-id="f9e19-118">Those parts of the two original regions that do not overlap define a new region.</span></span>      |



 

<span data-ttu-id="f9e19-119">下圖顯示由呼叫 [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn)所產生的五個可能的正方形和圓形區域組合。</span><span class="sxs-lookup"><span data-stu-id="f9e19-119">The following illustration shows the five possible combinations of a square and a circular region resulting from a call to [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn).</span></span>

![示範上表所述之結果的圖例](images/csrgn-02.png)

 

 



