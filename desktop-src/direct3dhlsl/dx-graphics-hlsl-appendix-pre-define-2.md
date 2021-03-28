---
title: '\#定義指示詞 (宏) '
description: 建立類似函式宏的預處理器指示詞。
ms.assetid: 73c19cf8-fbc5-444b-a51f-dc9f881f397b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8de5a47fc92c02e9f565c80f600359e8e5b32f9
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104990862"
---
# <a name="define-directive-macro"></a><span data-ttu-id="ae57f-103">\#定義指示詞 (宏) </span><span class="sxs-lookup"><span data-stu-id="ae57f-103">\#define directive (macro)</span></span>

<span data-ttu-id="ae57f-104">建立類似函式宏的預處理器指示詞。</span><span class="sxs-lookup"><span data-stu-id="ae57f-104">Preprocessor directive that creates a function-like macro.</span></span>



| <span data-ttu-id="ae57f-105">\#定義 *識別碼* ( *argument0*，...， *argumentN-1* ) *權杖-字串*</span><span class="sxs-lookup"><span data-stu-id="ae57f-105">\#define *identifier*( *argument0*, ... , *argumentN-1* ) *token-string*</span></span> |
|--------------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="ae57f-106">參數</span><span class="sxs-lookup"><span data-stu-id="ae57f-106">Parameters</span></span>



| <span data-ttu-id="ae57f-107">項目</span><span class="sxs-lookup"><span data-stu-id="ae57f-107">Item</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="ae57f-108">描述</span><span class="sxs-lookup"><span data-stu-id="ae57f-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae57f-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*識別碼*</span><span class="sxs-lookup"><span data-stu-id="ae57f-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/>                                                                                                                                                                             | <span data-ttu-id="ae57f-110">宏的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ae57f-110">Identifier of the macro.</span></span> <br/> <span data-ttu-id="ae57f-111">除非第二個權杖順序與第一個相同，否則使用已存在於目前內容中的識別碼之宏的第二個[ \# 定義](dx-graphics-hlsl-appendix-pre-define.md)會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="ae57f-111">A second [\#define](dx-graphics-hlsl-appendix-pre-define.md) for a macro with an identifier that already exists in the current context generates an error unless the second token sequence is identical to the first.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ae57f-112"><span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*，...， *argumentN-1* ) </span><span class="sxs-lookup"><span data-stu-id="ae57f-112"><span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*, ... , *argumentN-1* )</span></span> <br/> | <span data-ttu-id="ae57f-113">宏的引數清單。</span><span class="sxs-lookup"><span data-stu-id="ae57f-113">List of arguments to the macro.</span></span> <span data-ttu-id="ae57f-114">引數清單以逗號分隔、可以是任何長度，而且必須以括弧括住。</span><span class="sxs-lookup"><span data-stu-id="ae57f-114">The argument list is comma-delimited, can be of any length, and must be enclosed in parentheses.</span></span> <span data-ttu-id="ae57f-115">清單中的每個引數名稱都必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="ae57f-115">Each argument name in the list must be unique.</span></span> <span data-ttu-id="ae57f-116">沒有空格可分隔 *識別碼* 參數和左括弧。</span><span class="sxs-lookup"><span data-stu-id="ae57f-116">No white space can separate the *identifier* parameter and the opening parenthesis.</span></span> <br/> <span data-ttu-id="ae57f-117">使用行串連，將反斜線 (\) 緊接在換行字元之前，以將長指示詞分割成多個原始程式列。</span><span class="sxs-lookup"><span data-stu-id="ae57f-117">Use line concatenation place a backslash (\) immediately before the newline character to split long directives onto multiple source lines.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ae57f-118"><span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*token-字串* \[選\]</span><span class="sxs-lookup"><span data-stu-id="ae57f-118"><span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*token-string* \[optional\]</span></span> <br/>                                                                                                                     | <span data-ttu-id="ae57f-119">宏的值。</span><span class="sxs-lookup"><span data-stu-id="ae57f-119">Value of the macro.</span></span> <span data-ttu-id="ae57f-120">這個參數是由一系列的 token 所組成，例如關鍵字、常數或完整語句。</span><span class="sxs-lookup"><span data-stu-id="ae57f-120">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="ae57f-121">一或多個空白字元必須將此參數與 *識別碼* 參數分開;這個空白字元不會被視為替代文字的一部分，也不會在文字的最後一個標記之後的任何空白字元。</span><span class="sxs-lookup"><span data-stu-id="ae57f-121">One or more white-space characters must separate this parameter from the *identifier* parameter; this white space is not considered part of the substituted text, nor is any white space following the last token of the text.</span></span> <span data-ttu-id="ae57f-122">充分利用括弧來確保正確地解讀複雜的引數。</span><span class="sxs-lookup"><span data-stu-id="ae57f-122">Make liberal use of parentheses to ensure that complicated arguments are interpreted correctly.</span></span> <br/> <span data-ttu-id="ae57f-123">如果 *識別碼* 參數的值發生在 *token 字串* 參數內 (即使是另一個宏展開) ，也不會展開。</span><span class="sxs-lookup"><span data-stu-id="ae57f-123">If the value of the *identifier* parameter occurs within the *token-string* parameter (even as a result of another macro expansion), it is not expanded.</span></span> <br/> <span data-ttu-id="ae57f-124">如果您排除此參數，則會從原始程式檔中移除 *識別碼* 參數的所有實例。</span><span class="sxs-lookup"><span data-stu-id="ae57f-124">If you exclude this parameter, all instances of the *identifier* parameter are removed from the source file.</span></span> <span data-ttu-id="ae57f-125">識別碼仍會保持定義，並且可使用[ \# if 已定義](dx-graphics-hlsl-appendix-pre-ifdef.md)、 \# ifdef 和 ifndef 指示詞進行測試 \# 。</span><span class="sxs-lookup"><span data-stu-id="ae57f-125">The identifier remains defined, and can be tested using the [\#if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \#ifdef, and \#ifndef directives.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="ae57f-126">備註</span><span class="sxs-lookup"><span data-stu-id="ae57f-126">Remarks</span></span>

<span data-ttu-id="ae57f-127">在原始程式檔中 [ \# 定義](dx-graphics-hlsl-appendix-pre-define.md)指示詞之後發生的 *識別碼* 參數的所有實例構成了宏呼叫，而該識別碼會取代為具有實作為型式參數之實際引數的 *權杖字串* 參數版本。</span><span class="sxs-lookup"><span data-stu-id="ae57f-127">All instances of the *identifier* parameter that occur after the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive in the source file constitute a macro call, and the identifier will be replaced by a version of the *token-string* parameter that has actual arguments substituted for formal parameters.</span></span> <span data-ttu-id="ae57f-128">呼叫中的參數數目必須符合巨集定義中的參數數目。</span><span class="sxs-lookup"><span data-stu-id="ae57f-128">The number of parameters in the call must match the number of parameters in the macro definition.</span></span> <span data-ttu-id="ae57f-129">只有在形成權杖時，才會取代識別碼;例如，如果識別碼出現在批註、字串內或較長識別碼的一部分，則不會取代該識別碼。</span><span class="sxs-lookup"><span data-stu-id="ae57f-129">The identifier is replaced only when it forms a token; for example, the identifier is not replaced if it appears in a comment, within a string, or as part of a longer identifier.</span></span>

<span data-ttu-id="ae57f-130">[ \# Undef](dx-graphics-hlsl-appendix-pre-undef.md)指示詞會指示預處理器忘記定義識別碼; 如需詳細資訊，請參閱 \# (DirectX HLSL) 的 undef 指示詞。</span><span class="sxs-lookup"><span data-stu-id="ae57f-130">The [\#undef](dx-graphics-hlsl-appendix-pre-undef.md) directive instructs the preprocessor to forget the definition of an identifier; for more information, see \#undef Directive (DirectX HLSL).</span></span>

<span data-ttu-id="ae57f-131">使用/D 編譯器選項定義常數的效果，與在檔案開頭使用[ \# define](dx-graphics-hlsl-appendix-pre-define.md)指示詞的效果相同。</span><span class="sxs-lookup"><span data-stu-id="ae57f-131">Defining constants with the /D compiler option has the same effect as using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive at the beginning of your file.</span></span> <span data-ttu-id="ae57f-132">最多可以使用/D 選項來定義30個宏。</span><span class="sxs-lookup"><span data-stu-id="ae57f-132">Up to 30 macros can be defined with the /D option.</span></span>

<span data-ttu-id="ae57f-133">宏呼叫中的實際引數會與巨集定義中的對應正式引數相符。</span><span class="sxs-lookup"><span data-stu-id="ae57f-133">The actual arguments in the macro call are matched to the corresponding formal arguments in the macro definition.</span></span> <span data-ttu-id="ae57f-134">標記字串中的每個型式引數都會由對應的實際引數取代，除非引數前面有字串化 (\#) 、字元化 (\# @ ) 或標記貼上 (\# \#) 運算子，或後面接著 \# \# 操作員。</span><span class="sxs-lookup"><span data-stu-id="ae57f-134">Each formal argument in the token string is replaced by the corresponding actual argument, unless the argument is preceded by a stringizing (\#), charizing (\#@), or token-pasting (\#\#) operator, or is followed by a \#\# operator.</span></span> <span data-ttu-id="ae57f-135">實際引數中的所有巨集都會在指示詞取代型式參數之前展開。</span><span class="sxs-lookup"><span data-stu-id="ae57f-135">Any macros in the actual argument are expanded before the directive replaces the formal parameter.</span></span>

<span data-ttu-id="ae57f-136">在 HLSL 編譯器中貼上的權杖與在 C 編譯器中貼上的權杖稍微不同，因為貼上的權杖必須是自己的有效權杖。</span><span class="sxs-lookup"><span data-stu-id="ae57f-136">Token pasting in the HLSL compiler is slightly different from token pasting in the C compiler, in that the pasted tokens must be valid tokens on their own.</span></span> <span data-ttu-id="ae57f-137">例如，請考慮下列巨集定義：</span><span class="sxs-lookup"><span data-stu-id="ae57f-137">For example, consider the following macro definition:</span></span>


```
#define MERGE(a, b) a##b
MERGE(float, 4x4) test;
```



<span data-ttu-id="ae57f-138">在 C 編譯器中，這會產生下列結果：</span><span class="sxs-lookup"><span data-stu-id="ae57f-138">In the C compiler, this results in the following:</span></span>


```
float4x4 test
```



<span data-ttu-id="ae57f-139">不過，在 HLSL 編譯器中，這會產生下列結果：</span><span class="sxs-lookup"><span data-stu-id="ae57f-139">In the HLSL compiler however, this results in the following:</span></span>


```
float4 x4 test
```



<span data-ttu-id="ae57f-140">您可以改為使用下列巨集定義來解決這種行為。</span><span class="sxs-lookup"><span data-stu-id="ae57f-140">You can work around this behavior by using the following macro definition instead.</span></span>


```
MERGE(MERGE(float, 4), x4) test;
```



## <a name="examples"></a><span data-ttu-id="ae57f-141">範例</span><span class="sxs-lookup"><span data-stu-id="ae57f-141">Examples</span></span>

<span data-ttu-id="ae57f-142">下列範例會使用宏來定義游標行。</span><span class="sxs-lookup"><span data-stu-id="ae57f-142">The following example uses a macro to define cursor lines.</span></span>


```
#define CURSOR(top, bottom) (((top) << 8) | (bottom))
```



<span data-ttu-id="ae57f-143">下列範例會定義一個宏，以抓取指定範圍內的隨機整數。</span><span class="sxs-lookup"><span data-stu-id="ae57f-143">The following example defines a macro that retrieves a pseudorandom integer in the specified range.</span></span>


```
#define getrandom(min, max) \
((rand()%(int)(((max) + 1)-(min)))+ (min))
```



## <a name="related-topics"></a><span data-ttu-id="ae57f-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="ae57f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae57f-145"> (DirectX HLSL) 的預處理器指示詞 </span><span class="sxs-lookup"><span data-stu-id="ae57f-145">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="ae57f-146">\#定義多載</span><span class="sxs-lookup"><span data-stu-id="ae57f-146">\#define Overloads</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="ae57f-147">\# (DirectX HLSL) 的 undef 指示詞 </span><span class="sxs-lookup"><span data-stu-id="ae57f-147">\#undef Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





