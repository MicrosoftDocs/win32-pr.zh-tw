---
title: " ifdef"
description: '\ Ifdef 指示詞會藉由檢查指定的名稱來控制資源檔的條件式編譯。'
ms.assetid: 877c6b58-d8a1-4e68-8b69-29fe106d6cbd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38170fb2140f8405a86529c0899c1e4d4e93c026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372224"
---
# <a name="ifdef"></a><span data-ttu-id="936d7-103">\#ifdef</span><span class="sxs-lookup"><span data-stu-id="936d7-103">\#ifdef</span></span>

<span data-ttu-id="936d7-104">**\# Ifdef** 指示詞會藉由檢查指定的名稱來控制資源檔的條件式編譯。</span><span class="sxs-lookup"><span data-stu-id="936d7-104">The **\#ifdef** directive controls conditional compilation of the resource file by checking the specified name.</span></span> <span data-ttu-id="936d7-105">如果已使用 **\# define** 指示詞或使用 **/d** 命令列選項搭配資源編譯器來定義名稱， **\# ifdef** 會指示編譯器在 **\# ifdef** 指示詞後面緊接著語句繼續。</span><span class="sxs-lookup"><span data-stu-id="936d7-105">If the name has been defined by using a **\#define** directive or by using the **/d** command-line option with the resource compiler, **\#ifdef** directs the compiler to continue with the statement immediately after the **\#ifdef** directive.</span></span> <span data-ttu-id="936d7-106">如果未定義名稱， **\# ifdef** 會指示編譯器略過所有語句，直到下一個 **\# endif** 指示詞為止。</span><span class="sxs-lookup"><span data-stu-id="936d7-106">If the name has not been defined, **\#ifdef** directs the compiler to skip all statements up to the next **\#endif** directive.</span></span>

``` syntax
#ifdef name
```

<dl> <dt>

<span data-ttu-id="936d7-107"><span id="name"></span><span id="NAME"></span>*名字*</span><span class="sxs-lookup"><span data-stu-id="936d7-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="936d7-108">指示詞要檢查的名稱。</span><span class="sxs-lookup"><span data-stu-id="936d7-108">Name to be checked by the directive.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="936d7-109">範例</span><span class="sxs-lookup"><span data-stu-id="936d7-109">Example</span></span>

<span data-ttu-id="936d7-110">此範例只會在定義 Debug 時編譯 [**BITMAP**](bitmap-resource.md) 語句：</span><span class="sxs-lookup"><span data-stu-id="936d7-110">This example compiles the [**BITMAP**](bitmap-resource.md) statement only if Debug is defined:</span></span>

``` syntax
#ifdef Debug
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="936d7-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="936d7-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="936d7-112">預處理器指示詞</span><span class="sxs-lookup"><span data-stu-id="936d7-112">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




