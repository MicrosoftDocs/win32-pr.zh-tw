---
title: " elif"
description: '\ Elif 指示詞會標記由 \ ifdef、\ ifndef 或 \ if 指示詞所定義之條件式編譯區塊的選擇性子句。'
ms.assetid: 432b8543-7e1a-411a-8191-cc0f0e4a2e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a548cff74151dadf4a83a1e7d91ceedeafe07e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021583"
---
# <a name="elif"></a><span data-ttu-id="34226-103">\#elif</span><span class="sxs-lookup"><span data-stu-id="34226-103">\#elif</span></span>

<span data-ttu-id="34226-104">**\# Elif** 指示詞會標記由 **\# ifdef**、 **\# ifndef** 或 **\# if** 指示詞所定義之條件式編譯區塊的選擇性子句。</span><span class="sxs-lookup"><span data-stu-id="34226-104">The **\#elif** directive marks an optional clause of a conditional-compilation block defined by a **\#ifdef**, **\#ifndef**, or **\#if** directive.</span></span> <span data-ttu-id="34226-105">指示詞會檢查指定的常數運算式，以控制資源檔的條件式編譯。</span><span class="sxs-lookup"><span data-stu-id="34226-105">The directive controls conditional compilation of the resource file by checking the specified constant expression.</span></span> <span data-ttu-id="34226-106">如果常數運算式為非零值， **\# elif** 會指示編譯器繼續處理語句，直到下一個 **\# endif**、 **\# else** 或 **\# elif** 指示詞，然後跳至 **\# endif** 之後的語句。</span><span class="sxs-lookup"><span data-stu-id="34226-106">If the constant expression is nonzero, **\#elif** directs the compiler to continue processing statements up to the next **\#endif**, **\#else**, or **\#elif** directive and then skip to the statement after **\#endif**.</span></span> <span data-ttu-id="34226-107">如果常數運算式為零， **\# elif** 會指示編譯器跳到下一個 **\# endif**、 **\# else** 或 **\# elif** 指示詞。</span><span class="sxs-lookup"><span data-stu-id="34226-107">If the constant expression is zero, **\#elif** directs the compiler to skip to the next **\#endif**, **\#else**, or **\#elif** directive.</span></span> <span data-ttu-id="34226-108">您可以在條件式區塊中使用任何數目的 **\# elif** 指示詞。</span><span class="sxs-lookup"><span data-stu-id="34226-108">You can use any number of **\#elif** directives in a conditional block.</span></span>

``` syntax
#elif constant-expression
```

<dl> <dt>

<span data-ttu-id="34226-109"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*常數運算式*</span><span class="sxs-lookup"><span data-stu-id="34226-109"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*</span></span>
</dt> <dd>

<span data-ttu-id="34226-110">要檢查的運算式。</span><span class="sxs-lookup"><span data-stu-id="34226-110">Expression to be checked.</span></span> <span data-ttu-id="34226-111">此值是已定義的名稱、整數常數，或由名稱、整數和算術和關聯式運算子組成的運算式。</span><span class="sxs-lookup"><span data-stu-id="34226-111">This value is a defined name, an integer constant, or an expression consisting of names, integers, and arithmetic and relational operators.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="34226-112">範例</span><span class="sxs-lookup"><span data-stu-id="34226-112">Example</span></span>

<span data-ttu-id="34226-113">在此範例中，只有當指派給名稱版本的值小於7時， **\# elif** 才會指示編譯器處理第二個 [**BITMAP**](bitmap-resource.md)語句。</span><span class="sxs-lookup"><span data-stu-id="34226-113">In this example, **\#elif** directs the compiler to process the second [**BITMAP**](bitmap-resource.md) statement only if the value assigned to the name Version is less than 7.</span></span> <span data-ttu-id="34226-114">只有當版本大於或等於3時，才會處理 **\# elif** 指示詞本身。</span><span class="sxs-lookup"><span data-stu-id="34226-114">The **\#elif** directive itself is processed only if Version is greater than or equal to 3.</span></span>

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#elif Version < 7
BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="34226-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="34226-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34226-116">預處理器指示詞</span><span class="sxs-lookup"><span data-stu-id="34226-116">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




