---
title: " ifdef 和 ifndef 指示詞"
description: 判斷是否已定義特定預處理器常數或宏的預處理器指示詞。
ms.assetid: c1cc2e1d-2599-45ec-9629-56c4b42e0d0e
keywords:
- ifdef 和 ifndef 指示詞 HLSL
topic_type:
- apiref
api_name:
- ifdef and ifndef Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 338308b58f1cdc68ec78984e65ffbf056a36b10b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022476"
---
# <a name="ifdef-and-ifndef-directives"></a><span data-ttu-id="c6eea-104">\#ifdef 和 \# ifndef 指示詞</span><span class="sxs-lookup"><span data-stu-id="c6eea-104">\#ifdef and \#ifndef Directives</span></span>

<span data-ttu-id="c6eea-105">判斷是否已定義特定預處理器常數或宏的預處理器指示詞。</span><span class="sxs-lookup"><span data-stu-id="c6eea-105">Preprocessor directives that determine whether a specific preprocessor constant or macro is defined.</span></span>



| <span data-ttu-id="c6eea-106">\#ifdef *識別碼* .。。</span><span class="sxs-lookup"><span data-stu-id="c6eea-106">\#ifdef *identifier* ...</span></span>  |
|---------------------------|
| <span data-ttu-id="c6eea-107">\#endif</span><span class="sxs-lookup"><span data-stu-id="c6eea-107">\#endif</span></span>                   |
| <span data-ttu-id="c6eea-108">\#ifndef *識別碼* .。。</span><span class="sxs-lookup"><span data-stu-id="c6eea-108">\#ifndef *identifier* ...</span></span> |
| <span data-ttu-id="c6eea-109">\#endif</span><span class="sxs-lookup"><span data-stu-id="c6eea-109">\#endif</span></span>                   |



 

## <a name="parameters"></a><span data-ttu-id="c6eea-110">參數</span><span class="sxs-lookup"><span data-stu-id="c6eea-110">Parameters</span></span>



| <span data-ttu-id="c6eea-111">項目</span><span class="sxs-lookup"><span data-stu-id="c6eea-111">Item</span></span>                                                                              | <span data-ttu-id="c6eea-112">描述</span><span class="sxs-lookup"><span data-stu-id="c6eea-112">Description</span></span>                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c6eea-113"><span id="identifier"></span><span id="IDENTIFIER"></span>*識別碼*</span><span class="sxs-lookup"><span data-stu-id="c6eea-113"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/> | <span data-ttu-id="c6eea-114">要檢查之常數或宏的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6eea-114">Identifier of the constant or macro to check.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="c6eea-115">備註</span><span class="sxs-lookup"><span data-stu-id="c6eea-115">Remarks</span></span>

<span data-ttu-id="c6eea-116">您可以在 \# \# 可使用[ \# if](dx-graphics-hlsl-appendix-pre-if.md)的任何地方使用 ifdef 和 ifndef 指示詞。</span><span class="sxs-lookup"><span data-stu-id="c6eea-116">You can use the \#ifdef and \#ifndef directives anywhere that the [\#if](dx-graphics-hlsl-appendix-pre-if.md) can be used.</span></span> <span data-ttu-id="c6eea-117">\#Ifdef 語句相當於 ) 指示詞。</span><span class="sxs-lookup"><span data-stu-id="c6eea-117">The \#ifdef statement is equivalent to ) directive.</span></span> <span data-ttu-id="c6eea-118">這些指示詞只會檢查使用[ \# define](dx-graphics-hlsl-appendix-pre-define.md)指示詞所定義的識別碼是否存在，而不會檢查 c 或 c + + 原始程式碼中宣告的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6eea-118">These directives check only for the presence or absence of identifiers defined using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive, not for identifiers declared in the C or C++ source code.</span></span>

<span data-ttu-id="c6eea-119">提供這些指示詞的目的只是為了保留與舊版語言的相容性。</span><span class="sxs-lookup"><span data-stu-id="c6eea-119">These directives are provided only for compatibility with previous versions of the language.</span></span> <span data-ttu-id="c6eea-120">偏好使用 [已定義](dx-graphics-hlsl-appendix-pre-if.md) 的運算子搭配 if 指示詞 \# 。</span><span class="sxs-lookup"><span data-stu-id="c6eea-120">The use of the [defined](dx-graphics-hlsl-appendix-pre-if.md) operator with the \#if directive is preferred.</span></span>

<span data-ttu-id="c6eea-121">Ifndef 指示詞會 \# 檢查由 ifdef 檢查的條件是否相反 \# 。</span><span class="sxs-lookup"><span data-stu-id="c6eea-121">The \#ifndef directive checks for the opposite of the condition checked by \#ifdef.</span></span> <span data-ttu-id="c6eea-122">如果未定義識別碼，則條件為 true (非零) ;否則，條件為 false (零) 。</span><span class="sxs-lookup"><span data-stu-id="c6eea-122">If the identifier is not defined, the condition is true (nonzero); otherwise, the condition is false (zero).</span></span>

## <a name="examples"></a><span data-ttu-id="c6eea-123">範例</span><span class="sxs-lookup"><span data-stu-id="c6eea-123">Examples</span></span>

<span data-ttu-id="c6eea-124">identifier 可以從命令列使用 /D 選項傳遞。</span><span class="sxs-lookup"><span data-stu-id="c6eea-124">The identifier can be passed from the command line using the /D option.</span></span> <span data-ttu-id="c6eea-125">使用 /D 最多可以指定 30 個巨集。</span><span class="sxs-lookup"><span data-stu-id="c6eea-125">Up to 30 macros can be specified with /D.</span></span> <span data-ttu-id="c6eea-126">這個選項在檢查定義是否存在時很實用，因為可以從命令列傳遞定義。</span><span class="sxs-lookup"><span data-stu-id="c6eea-126">This is useful for checking whether a definition exists, because a definition can be passed from the command line.</span></span> <span data-ttu-id="c6eea-127">下列範例會使用此行為來判斷是否要在測試模式中執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="c6eea-127">The following example uses this behavior to determine whether to run an application in test mode.</span></span>


```
// PROG.CPP
#ifndef test
  #define final
#endif
int main()
{
}
```



<span data-ttu-id="c6eea-128">使用下列命令進行編譯時，會在測試模式中編譯進程 .cpp;否則，它會在最終模式中進行編譯。</span><span class="sxs-lookup"><span data-stu-id="c6eea-128">When compiled using the following command, prog.cpp will compile in test mode; otherwise, it will compile in final mode.</span></span>


```
CL.EXE /Dtest prog.cpp
```



## <a name="see-also"></a><span data-ttu-id="c6eea-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6eea-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6eea-130"> (DirectX HLSL) 的預處理器指示詞 </span><span class="sxs-lookup"><span data-stu-id="c6eea-130">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="c6eea-131">\#如果為，) </span><span class="sxs-lookup"><span data-stu-id="c6eea-131">\#if, )</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





