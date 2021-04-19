---
title: " if"
description: '\ If 指示詞會藉由檢查指定的常數運算式來控制資源檔的條件式編譯。'
ms.assetid: 4d0f26a0-1a2d-4fad-b5ce-b9441397d2c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364d6f5eb818813f61f6428446effb4793b96b2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106984506"
---
# <a name="if"></a><span data-ttu-id="3bc7e-103">\#如果</span><span class="sxs-lookup"><span data-stu-id="3bc7e-103">\#if</span></span>

<span data-ttu-id="3bc7e-104">**\# If** 指示詞會藉由檢查指定的常數運算式來控制資源檔的條件式編譯。</span><span class="sxs-lookup"><span data-stu-id="3bc7e-104">The **\#if** directive controls conditional compilation of the resource file by checking the specified constant expression.</span></span> <span data-ttu-id="3bc7e-105">如果常數運算式不是零，則會指示編譯器繼續處理語句，直到下一個 **\# endif**、 **\# else** 或 **\# elif** 指示詞，然後跳至 **\# endif** 指示詞之後的語句。 **\#**</span><span class="sxs-lookup"><span data-stu-id="3bc7e-105">If the constant expression is nonzero, **\#if** directs the compiler to continue processing statements up to the next **\#endif**, **\#else**, or **\#elif** directive and then skip to the statement after the **\#endif** directive.</span></span> <span data-ttu-id="3bc7e-106">如果常數運算式為零，則 **\#** 會指示編譯器跳到下一個 **\# endif**、 **\# else** 或 **\# elif** 指示詞。</span><span class="sxs-lookup"><span data-stu-id="3bc7e-106">If the constant expression is zero, **\#if** directs the compiler to skip to the next **\#endif**, **\#else**, or **\#elif** directive.</span></span>

``` syntax
#if constant-expression
```

<dl> <dt>

<span data-ttu-id="3bc7e-107"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*常數運算式*</span><span class="sxs-lookup"><span data-stu-id="3bc7e-107"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*</span></span>
</dt> <dd>

<span data-ttu-id="3bc7e-108">要檢查的運算式。</span><span class="sxs-lookup"><span data-stu-id="3bc7e-108">Expression to be checked.</span></span> <span data-ttu-id="3bc7e-109">此值是已定義的名稱、整數常數，或由名稱、整數和算術和關聯式運算子組成的運算式。</span><span class="sxs-lookup"><span data-stu-id="3bc7e-109">This value is a defined name, an integer constant, or an expression consisting of names, integers, and arithmetic and relational operators.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="3bc7e-110">範例</span><span class="sxs-lookup"><span data-stu-id="3bc7e-110">Example</span></span>

<span data-ttu-id="3bc7e-111">這個範例只有在指派的值版本小於3時，才會編譯 [**BITMAP**](bitmap-resource.md) 語句：</span><span class="sxs-lookup"><span data-stu-id="3bc7e-111">This example compiles the [**BITMAP**](bitmap-resource.md) statement only if the value assigned Version is less than 3:</span></span>

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="3bc7e-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="3bc7e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bc7e-113">預處理器指示詞</span><span class="sxs-lookup"><span data-stu-id="3bc7e-113">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




