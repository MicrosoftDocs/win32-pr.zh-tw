---
title: " define"
description: '\ 定義指示詞會將指定的值指派給指定的名稱。 所有後續出現的名稱都會以值取代。'
ms.assetid: 2699d2dc-caf8-47d6-8b2e-526357962532
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557c6b486d9c2bd07b0b012c17e806f5d9eaae91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674167"
---
# <a name="define"></a><span data-ttu-id="30fe8-104">\#定義</span><span class="sxs-lookup"><span data-stu-id="30fe8-104">\#define</span></span>

<span data-ttu-id="30fe8-105">**\# Define** 指示詞會將指定的值指派給指定的名稱。</span><span class="sxs-lookup"><span data-stu-id="30fe8-105">The **\#define** directive assigns the given value to the specified name.</span></span> <span data-ttu-id="30fe8-106">所有後續出現的名稱都會以值取代。</span><span class="sxs-lookup"><span data-stu-id="30fe8-106">All subsequent occurrences of the name are replaced by the value.</span></span>

``` syntax
#define name value
```

<dl> <dt>

<span data-ttu-id="30fe8-107"><span id="name"></span><span id="NAME"></span>*名字*</span><span class="sxs-lookup"><span data-stu-id="30fe8-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="30fe8-108">要定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="30fe8-108">Name to be defined.</span></span> <span data-ttu-id="30fe8-109">此值是字母、數位和標點符號的任意組合，適用于 C/c + + 預處理器。</span><span class="sxs-lookup"><span data-stu-id="30fe8-109">This value is any combination of letters, digits, and punctuation that is valid for the C/C++ preprocessor.</span></span>

</dd> <dt>

<span data-ttu-id="30fe8-110"><span id="value"></span><span id="VALUE"></span>*價值*</span><span class="sxs-lookup"><span data-stu-id="30fe8-110"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="30fe8-111">整數、字元字串或文字行。</span><span class="sxs-lookup"><span data-stu-id="30fe8-111">Integer, character string, or line of text.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="30fe8-112">範例</span><span class="sxs-lookup"><span data-stu-id="30fe8-112">Example</span></span>

<span data-ttu-id="30fe8-113">這個範例會將值指派給名稱非零和 USERCLASS：</span><span class="sxs-lookup"><span data-stu-id="30fe8-113">This example assigns values to the names NONZERO and USERCLASS:</span></span>

``` syntax
#define     NONZERO     1
#define     USERCLASS   "MyControlClass"
```

## <a name="related-topics"></a><span data-ttu-id="30fe8-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="30fe8-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30fe8-115">預處理器指示詞</span><span class="sxs-lookup"><span data-stu-id="30fe8-115">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




