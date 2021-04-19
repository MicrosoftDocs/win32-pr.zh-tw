---
description: 定義一組動畫索引鍵。 矩陣索引鍵適用于需要以轉換矩陣表示的動畫資料集。
ms.assetid: bf007541-7fea-423e-910b-fa5f45271608
title: AnimationKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05728f124ae01962a1291547f8fe8b7fcebd175a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972568"
---
# <a name="animationkey"></a><span data-ttu-id="9d466-104">AnimationKey</span><span class="sxs-lookup"><span data-stu-id="9d466-104">AnimationKey</span></span>

<span data-ttu-id="9d466-105">定義一組動畫索引鍵。</span><span class="sxs-lookup"><span data-stu-id="9d466-105">Defines a set of animation keys.</span></span> <span data-ttu-id="9d466-106">矩陣索引鍵適用于需要以轉換矩陣表示的動畫資料集。</span><span class="sxs-lookup"><span data-stu-id="9d466-106">A matrix key is useful for sets of animation data that need to be represented as transformation matrices.</span></span>

``` syntax
template AnimationKey
{
    < 10DD46A8-775B-11CF-8F52-0040333594A3 >
    DWORD keyType;
    DWORD nKeys;
    array TimedFloatKeys keys[nKeys];
} 
```

<span data-ttu-id="9d466-107">其中：</span><span class="sxs-lookup"><span data-stu-id="9d466-107">Where:</span></span>

-   <span data-ttu-id="9d466-108">keyType-使用整數0、1、2或3分別) ，指定索引鍵為旋轉、縮放、位置或矩陣鍵 (。</span><span class="sxs-lookup"><span data-stu-id="9d466-108">keyType - Specifies whether the keys are rotation, scale, position, or matrix keys (using the integers 0, 1, 2, or 3, respectively).</span></span>
-   <span data-ttu-id="9d466-109">nKeys-索引鍵數目。</span><span class="sxs-lookup"><span data-stu-id="9d466-109">nKeys - Number of keys.</span></span>
-   <span data-ttu-id="9d466-110">索引鍵-索引鍵的陣列。</span><span class="sxs-lookup"><span data-stu-id="9d466-110">keys - An array of keys.</span></span> <span data-ttu-id="9d466-111">請參閱 [**TimedFloatKeys**](timedfloatkeys.md)。</span><span class="sxs-lookup"><span data-stu-id="9d466-111">See [**TimedFloatKeys**](timedfloatkeys.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9d466-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d466-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d466-113">範本</span><span class="sxs-lookup"><span data-stu-id="9d466-113">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



