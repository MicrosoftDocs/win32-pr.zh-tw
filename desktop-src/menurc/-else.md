---
title: " else"
description: Else 指示詞會標記由 \ ifdef、\ ifndef 或 \ if 指示詞所定義之條件式編譯區塊的選擇性子句。 Else 指示詞必須是在 \ endif 指示詞之前的最後一個指示詞。
ms.assetid: 982466d9-ae77-4e1c-89f3-511335165da7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086acd9e6323f7be11a65951a33b2b11b680ad46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673475"
---
# <a name="else"></a><span data-ttu-id="d0086-104">\#else</span><span class="sxs-lookup"><span data-stu-id="d0086-104">\#else</span></span>

<span data-ttu-id="d0086-105">**\# Else** 指示詞會標示由 **\# ifdef**、 **\# ifndef** 或 **\# if** 指示詞所定義之條件式編譯區塊的選擇性子句。</span><span class="sxs-lookup"><span data-stu-id="d0086-105">The **\#else** directive marks an optional clause of a conditional-compilation block defined by a **\#ifdef**, **\#ifndef**, or **\#if** directive.</span></span> <span data-ttu-id="d0086-106">**\# Else** 指示詞必須是 **\# endif** 指示詞前面的最後一個指示詞。</span><span class="sxs-lookup"><span data-stu-id="d0086-106">The **\#else** directive must be the last directive before the **\#endif** directive.</span></span>

``` syntax
#else
```

<span data-ttu-id="d0086-107">這個指示詞沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d0086-107">This directive has no parameters.</span></span>

## <a name="example"></a><span data-ttu-id="d0086-108">範例</span><span class="sxs-lookup"><span data-stu-id="d0086-108">Example</span></span>

<span data-ttu-id="d0086-109">這個範例只有在未定義 DEBUG 時，才會編譯第二個 [**BITMAP**](bitmap-resource.md) 語句：</span><span class="sxs-lookup"><span data-stu-id="d0086-109">This example compiles the second [**BITMAP**](bitmap-resource.md) statement only if DEBUG is not defined:</span></span>

``` syntax
#ifdef DEBUG
    BITMAP 1 errbox.bmp
#else
    BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="d0086-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="d0086-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0086-111">預處理器指示詞</span><span class="sxs-lookup"><span data-stu-id="d0086-111">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




