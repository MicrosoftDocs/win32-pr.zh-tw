---
title: '\#定義指示詞 (常數) '
description: 預處理器指示詞，可將有意義的名稱指派給您應用程式中的常數。
ms.assetid: cc9b34a3-4c83-4999-99ec-e6261ecb2785
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: deae1ca92c2280cd31cbec2bf3482c61fcf2b88a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104022866"
---
# <a name="define-directive-constant"></a><span data-ttu-id="0e62a-103">\#定義指示詞 (常數) </span><span class="sxs-lookup"><span data-stu-id="0e62a-103">\#define directive (constant)</span></span>

<span data-ttu-id="0e62a-104">預處理器指示詞，可將有意義的名稱指派給您應用程式中的常數。</span><span class="sxs-lookup"><span data-stu-id="0e62a-104">Preprocessor directive that assigns a meaningful name to a constant in your application.</span></span>



| <span data-ttu-id="0e62a-105">\#定義 *identifiertoken-字串*</span><span class="sxs-lookup"><span data-stu-id="0e62a-105">\#define *identifiertoken-string*</span></span> |
|-----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="0e62a-106">參數</span><span class="sxs-lookup"><span data-stu-id="0e62a-106">Parameters</span></span>



| <span data-ttu-id="0e62a-107">項目</span><span class="sxs-lookup"><span data-stu-id="0e62a-107">Item</span></span>                                                                                                                       | <span data-ttu-id="0e62a-108">描述</span><span class="sxs-lookup"><span data-stu-id="0e62a-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e62a-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*識別碼*</span><span class="sxs-lookup"><span data-stu-id="0e62a-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/>                                          | <span data-ttu-id="0e62a-110">常數的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e62a-110">Identifier of the constant.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="0e62a-111"><span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*token-字串* \[選\]</span><span class="sxs-lookup"><span data-stu-id="0e62a-111"><span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*token-string* \[optional\]</span></span><br/> | <span data-ttu-id="0e62a-112">常數的值。</span><span class="sxs-lookup"><span data-stu-id="0e62a-112">Value of the constant.</span></span> <span data-ttu-id="0e62a-113">這個參數是由一系列的 token 所組成，例如關鍵字、常數或完整語句。</span><span class="sxs-lookup"><span data-stu-id="0e62a-113">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="0e62a-114">一或多個空白字元必須將此參數與 *識別碼* 參數分開;這個空白字元不會被視為替代文字的一部分，也不會在文字的最後一個標記之後的任何空白字元。</span><span class="sxs-lookup"><span data-stu-id="0e62a-114">One or more white-space characters must separate this parameter from the *identifier* parameter; this white space is not considered part of the substituted text, nor is any white space following the last token of the text.</span></span> <br/> <span data-ttu-id="0e62a-115">如果您排除此參數，則會從原始程式檔中移除 *識別碼* 參數的所有實例。</span><span class="sxs-lookup"><span data-stu-id="0e62a-115">If you exclude this parameter, all instances of the *identifier* parameter are removed from the source file.</span></span> <span data-ttu-id="0e62a-116">識別碼仍會保持定義，並且可使用[ \# if 已定義](dx-graphics-hlsl-appendix-pre-ifdef.md)、 \# ifdef 和 ifndef 指示詞進行測試 \# 。</span><span class="sxs-lookup"><span data-stu-id="0e62a-116">The identifier remains defined, and can be tested using the [\#if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \#ifdef, and \#ifndef directives.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="0e62a-117">備註</span><span class="sxs-lookup"><span data-stu-id="0e62a-117">Remarks</span></span>

<span data-ttu-id="0e62a-118">在來源檔案中的 [ \# 定義](dx-graphics-hlsl-appendix-pre-define.md)指示詞之後發生之 *識別碼* 參數的所有實例，都會以 *token 字串* 參數的值取代。</span><span class="sxs-lookup"><span data-stu-id="0e62a-118">All instances of the *identifier* parameter that occur after the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive in the source file will be replaced by the value of the *token-string* parameter.</span></span> <span data-ttu-id="0e62a-119">只有在形成權杖時，才會取代識別碼;例如，如果識別碼出現在批註、字串內或較長識別碼的一部分，則不會取代該識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e62a-119">The identifier is replaced only when it forms a token; for example, the identifier is not replaced if it appears in a comment, within a string, or as part of a longer identifier.</span></span>

<span data-ttu-id="0e62a-120">[ \# Undef](dx-graphics-hlsl-appendix-pre-undef.md)指示詞會指示預處理器忘記定義識別碼; 如需詳細資訊，請參閱 \# (DirectX HLSL) 的 undef 指示詞。</span><span class="sxs-lookup"><span data-stu-id="0e62a-120">The [\#undef](dx-graphics-hlsl-appendix-pre-undef.md) directive instructs the preprocessor to forget the definition of an identifier; for more information, see \#undef Directive (DirectX HLSL).</span></span>

<span data-ttu-id="0e62a-121">使用/D 編譯器選項定義常數的效果，與在檔案開頭使用[ \# define](dx-graphics-hlsl-appendix-pre-define.md)指示詞的效果相同。</span><span class="sxs-lookup"><span data-stu-id="0e62a-121">Defining constants with the /D compiler option has the same effect as using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive at the beginning of your file.</span></span> <span data-ttu-id="0e62a-122">最多可以使用/D 選項來定義30個常數。</span><span class="sxs-lookup"><span data-stu-id="0e62a-122">Up to 30 constants can be defined with the /D option.</span></span> <span data-ttu-id="0e62a-123">如需如何使用此方法的範例，請參閱[ \# ifdef 和 ) ](dx-graphics-hlsl-appendix-pre-ifdef.md)的範例一節。</span><span class="sxs-lookup"><span data-stu-id="0e62a-123">For an example of how this can be used, see the Examples section of [\#ifdef and )](dx-graphics-hlsl-appendix-pre-ifdef.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0e62a-124">範例</span><span class="sxs-lookup"><span data-stu-id="0e62a-124">Examples</span></span>

<span data-ttu-id="0e62a-125">下列範例會將識別碼寬度定義為整數常數80，然後根據寬度和整數常數10定義長度。</span><span class="sxs-lookup"><span data-stu-id="0e62a-125">The following example defines the identifier WIDTH as the integer constant 80 and then defines LENGTH in terms of WIDTH and the integer constant 10.</span></span>


```
#define WIDTH       80
#define LENGTH      ( WIDTH + 10 )
```



<span data-ttu-id="0e62a-126">每個後續的長度實例都會取代為 (寬度 + 10) ，而寬度 + 10 的每個後續實例則會由運算式 (80 + 10) 取代。</span><span class="sxs-lookup"><span data-stu-id="0e62a-126">Every subsequent instance of LENGTH is replaced by (WIDTH + 10), and every subsequent instance of WIDTH + 10 is replaced by the expression (80 + 10).</span></span> <span data-ttu-id="0e62a-127">寬度 + 10 左右的括弧很重要，因為它們控制語句中的解讀，如下所示。</span><span class="sxs-lookup"><span data-stu-id="0e62a-127">The parentheses around WIDTH + 10 are important because they control the interpretation in statements such as the following.</span></span>


```
var = LENGTH * 20;
```



<span data-ttu-id="0e62a-128">在前置處理階段之後，語句會變成下列結果，其評估結果為1800。</span><span class="sxs-lookup"><span data-stu-id="0e62a-128">After the preprocessing stage the statement becomes the following, which evaluates to 1,800.</span></span>


```
var = ( 80 + 10 ) * 20;
```



<span data-ttu-id="0e62a-129">如果沒有括弧，結果會是下列結果，其會評估為280。</span><span class="sxs-lookup"><span data-stu-id="0e62a-129">Without parentheses, the result would be the following, which evaluates to 280.</span></span>


```
var = 80 + 10 * 20;
```



## <a name="related-topics"></a><span data-ttu-id="0e62a-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="0e62a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e62a-131"> (DirectX HLSL) 的預處理器指示詞 </span><span class="sxs-lookup"><span data-stu-id="0e62a-131">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="0e62a-132">\#定義多載</span><span class="sxs-lookup"><span data-stu-id="0e62a-132">\#define Overloads</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="0e62a-133">\# (DirectX HLSL) 的 undef 指示詞 </span><span class="sxs-lookup"><span data-stu-id="0e62a-133">\#undef Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





