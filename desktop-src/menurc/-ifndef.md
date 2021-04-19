---
title: " ifndef"
description: '\ Ifndef 指示詞會檢查指定的名稱，以控制資源檔的條件式編譯。'
ms.assetid: b83d7b0e-1a37-47a8-b495-0eab05ed3a9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 984a969123ea68fd68b14c1b98354b8bc5205aba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967822"
---
# <a name="ifndef"></a><span data-ttu-id="8b318-103">\#ifndef</span><span class="sxs-lookup"><span data-stu-id="8b318-103">\#ifndef</span></span>

<span data-ttu-id="8b318-104">**\# Ifndef** 指示詞會檢查指定的名稱，以控制資源檔的條件式編譯。</span><span class="sxs-lookup"><span data-stu-id="8b318-104">The **\#ifndef** directive controls conditional compilation of the resource file by checking the specified name.</span></span> <span data-ttu-id="8b318-105">如果未定義名稱，或已使用 **\# undef** 指示詞移除其定義， **\# ifndef** 會指示編譯器繼續處理語句，直到下一個 **\# endif**、 **\# else** 或 **\# elif** 指示詞，然後跳至 **\# endif** 指示詞之後的語句。</span><span class="sxs-lookup"><span data-stu-id="8b318-105">If the name has not been defined or if its definition has been removed by using the **\#undef** directive, **\#ifndef** directs the compiler to continue processing statements up to the next **\#endif**, **\#else**, or **\#elif** directive and then skip to the statement after the **\#endif** directive.</span></span> <span data-ttu-id="8b318-106">如果定義的名稱， **\# ifndef** 會指示編譯器跳到下一個 **\# endif**、 **\# else** 或 **\# elif** 指示詞。</span><span class="sxs-lookup"><span data-stu-id="8b318-106">If the name is defined, **\#ifndef** directs the compiler to skip to the next **\#endif**, **\#else**, or **\#elif** directive.</span></span>

``` syntax
#ifndef name
```

<dl> <dt>

<span data-ttu-id="8b318-107"><span id="name"></span><span id="NAME"></span>*名字*</span><span class="sxs-lookup"><span data-stu-id="8b318-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="8b318-108">指示詞要檢查的名稱。</span><span class="sxs-lookup"><span data-stu-id="8b318-108">Name to be checked by the directive.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="8b318-109">範例</span><span class="sxs-lookup"><span data-stu-id="8b318-109">Example</span></span>

<span data-ttu-id="8b318-110">這個範例只有在未定義 Optimize 時，才會編譯 [**BITMAP**](bitmap-resource.md) 語句：</span><span class="sxs-lookup"><span data-stu-id="8b318-110">This example compiles the [**BITMAP**](bitmap-resource.md) statement only if Optimize is not defined:</span></span>

``` syntax
#ifndef Optimize
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="8b318-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="8b318-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b318-112">預處理器指示詞</span><span class="sxs-lookup"><span data-stu-id="8b318-112">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




