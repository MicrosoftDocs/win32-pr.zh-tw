---
title: " undef"
description: '\ Undef 指示詞會移除指定之名稱的目前定義。 所有後續出現的名稱都不需要取代即可進行處理。'
ms.assetid: c9a0b538-3030-4d39-bfc2-d158061967b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b14eeea18a05795cd8ebbb94d81d0aead6a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106995550"
---
# <a name="undef"></a><span data-ttu-id="47e67-104">\#undef</span><span class="sxs-lookup"><span data-stu-id="47e67-104">\#undef</span></span>

<span data-ttu-id="47e67-105">**\# Undef** 指示詞會移除指定之名稱的目前定義。</span><span class="sxs-lookup"><span data-stu-id="47e67-105">The **\#undef** directive removes the current definition of the specified name.</span></span> <span data-ttu-id="47e67-106">所有後續出現的名稱都不需要取代即可進行處理。</span><span class="sxs-lookup"><span data-stu-id="47e67-106">All subsequent occurrences of the name are processed without replacement.</span></span>

``` syntax
#undef name
```

<dl> <dt>

<span data-ttu-id="47e67-107"><span id="name"></span><span id="NAME"></span>*名字*</span><span class="sxs-lookup"><span data-stu-id="47e67-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="47e67-108">要移除的名稱。</span><span class="sxs-lookup"><span data-stu-id="47e67-108">Name to be removed.</span></span> <span data-ttu-id="47e67-109">此值是字母、數位和標點符號的任意組合，適用于 C/c + + 預處理器。</span><span class="sxs-lookup"><span data-stu-id="47e67-109">This value is any combination of letters, digits, and punctuation that is valid for the C/C++ preprocessor.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="47e67-110">範例</span><span class="sxs-lookup"><span data-stu-id="47e67-110">Example</span></span>

<span data-ttu-id="47e67-111">此範例會移除名稱為非零和 USERCLASS 的定義：</span><span class="sxs-lookup"><span data-stu-id="47e67-111">This example removes the definitions for the names nonzero and USERCLASS:</span></span>

``` syntax
#undef     nonzero
#undef     USERCLASS
```

## <a name="related-topics"></a><span data-ttu-id="47e67-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="47e67-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47e67-113">預處理器指示詞</span><span class="sxs-lookup"><span data-stu-id="47e67-113">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




