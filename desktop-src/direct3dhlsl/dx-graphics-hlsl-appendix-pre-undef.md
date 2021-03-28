---
title: " undef 指示詞"
description: 預處理器指示詞，移除先前使用 \ 定義指示詞定義之常數或宏的目前定義。
ms.assetid: ba6bbe6b-ecfa-40cb-887f-e42b6e22c7bd
keywords:
- undef 指示詞 HLSL
topic_type:
- apiref
api_name:
- undef Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7358dc60d002e784394f64773934a18f7413e493
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312554"
---
# <a name="undef-directive"></a><span data-ttu-id="c241f-104">\#undef 指示詞</span><span class="sxs-lookup"><span data-stu-id="c241f-104">\#undef Directive</span></span>

<span data-ttu-id="c241f-105">預處理器指示詞，移除先前使用[ \# define](dx-graphics-hlsl-appendix-pre-define.md)指示詞定義之常數或宏的目前定義。</span><span class="sxs-lookup"><span data-stu-id="c241f-105">Preprocessor directive that removes the current definition of a constant or macro that was previously defined using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive.</span></span>



| <span data-ttu-id="c241f-106">\#undef *識別碼*</span><span class="sxs-lookup"><span data-stu-id="c241f-106">\#undef *identifier*</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="c241f-107">參數</span><span class="sxs-lookup"><span data-stu-id="c241f-107">Parameters</span></span>



| <span data-ttu-id="c241f-108">項目</span><span class="sxs-lookup"><span data-stu-id="c241f-108">Item</span></span>                                                                              | <span data-ttu-id="c241f-109">描述</span><span class="sxs-lookup"><span data-stu-id="c241f-109">Description</span></span>                                                                                                                                                      |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c241f-110"><span id="identifier"></span><span id="IDENTIFIER"></span>*識別碼*</span><span class="sxs-lookup"><span data-stu-id="c241f-110"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/> | <span data-ttu-id="c241f-111">要移除其定義之常數或宏的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c241f-111">Identifier of the constant or macro to remove the definition of.</span></span> <span data-ttu-id="c241f-112">如果您要 undefining 宏，請只提供識別碼，而不是參數清單。</span><span class="sxs-lookup"><span data-stu-id="c241f-112">If you are undefining a macro, provide only the identifier, not the parameter list.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="c241f-113">備註</span><span class="sxs-lookup"><span data-stu-id="c241f-113">Remarks</span></span>

<span data-ttu-id="c241f-114">您可以將 \# undef 指示詞套用至沒有先前定義的識別碼; 如此可確保未定義識別碼。</span><span class="sxs-lookup"><span data-stu-id="c241f-114">You can apply the \#undef directive to an identifier that has no previous definition; this ensures that the identifier is undefined.</span></span> <span data-ttu-id="c241f-115">不會在 undef 語句內執行宏取代 \# 。</span><span class="sxs-lookup"><span data-stu-id="c241f-115">Macro replacement is not performed within \#undef statements.</span></span>

<span data-ttu-id="c241f-116">Undef 指示詞 \# 通常會與[ \# 定義](dx-graphics-hlsl-appendix-pre-define.md)指示詞配對，以在原始程式中建立一個區域，其中識別碼具有特殊意義。</span><span class="sxs-lookup"><span data-stu-id="c241f-116">The \#undef directive is typically paired with a [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive to create a region in a source program in which an identifier has a special meaning.</span></span> <span data-ttu-id="c241f-117">例如，原始程式的特定函式可以使用資訊清單常數，以定義不會影響程式其他部分的環境特定值。</span><span class="sxs-lookup"><span data-stu-id="c241f-117">For example, a specific function of the source program can use manifest constants to define environment-specific values that do not affect the rest of the program.</span></span> <span data-ttu-id="c241f-118">Undef 指示詞 \# 也適用于 [) 指示詞，以控制來來源程式的條件式編譯。</span><span class="sxs-lookup"><span data-stu-id="c241f-118">The \#undef directive also works with the [) directive to control conditional compilation of the source program.</span></span>

<span data-ttu-id="c241f-119">您可以使用/U 選項從命令列未定義常數和宏，後面接著要定義的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c241f-119">Constants and macros can be undefined from the command line using the /U option, followed by the identifiers to be undefined.</span></span> <span data-ttu-id="c241f-120">這相當於在原始程式檔的開頭加入一連串的 undef 指示詞 \# 。</span><span class="sxs-lookup"><span data-stu-id="c241f-120">This is equivalent to adding a sequence of \#undef directives at the beginning of the source file.</span></span>

## <a name="examples"></a><span data-ttu-id="c241f-121">範例</span><span class="sxs-lookup"><span data-stu-id="c241f-121">Examples</span></span>

<span data-ttu-id="c241f-122">下列範例示範如何使用 undef 指示詞 \# 來移除符號常數和宏的定義。</span><span class="sxs-lookup"><span data-stu-id="c241f-122">The following example shows how to use the \#undef directive to remove definitions of a symbolic constant and a macro.</span></span>


```
#define WIDTH           80
#define ADD( X, Y )     (X) + (Y)

#undef WIDTH
#undef ADD
```



## <a name="see-also"></a><span data-ttu-id="c241f-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c241f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c241f-124"> (DirectX HLSL) 的預處理器指示詞 </span><span class="sxs-lookup"><span data-stu-id="c241f-124">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="c241f-125">\# (DirectX HLSL 定義指示詞) </span><span class="sxs-lookup"><span data-stu-id="c241f-125">\#define Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="c241f-126">\#如果為，) </span><span class="sxs-lookup"><span data-stu-id="c241f-126">\#if, )</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





