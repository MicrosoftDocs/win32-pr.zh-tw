---
title: " line 指示詞"
description: 預處理器指示詞，可將編譯器內部儲存的行號和檔案名設定為指定的值。
ms.assetid: 307410af-bd78-4b3d-b515-adf58298f35f
keywords:
- line 指示詞 HLSL
topic_type:
- apiref
api_name:
- line Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0932138ce5aec85ad3d3e7058db0c2a93e131181
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373032"
---
# <a name="line-directive"></a><span data-ttu-id="b4abf-104">\#line 指示詞</span><span class="sxs-lookup"><span data-stu-id="b4abf-104">\#line Directive</span></span>

<span data-ttu-id="b4abf-105">預處理器指示詞，可將編譯器內部儲存的行號和檔案名設定為指定的值。</span><span class="sxs-lookup"><span data-stu-id="b4abf-105">Preprocessor directive that sets the compiler's internally-stored line number and filename to the specified values.</span></span>



| <span data-ttu-id="b4abf-106">\#line *lineNumber* "*filename*"</span><span class="sxs-lookup"><span data-stu-id="b4abf-106">\#line *lineNumber* "*filename*"</span></span> |
|----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="b4abf-107">參數</span><span class="sxs-lookup"><span data-stu-id="b4abf-107">Parameters</span></span>



| <span data-ttu-id="b4abf-108">項目</span><span class="sxs-lookup"><span data-stu-id="b4abf-108">Item</span></span>                                                                                                                              | <span data-ttu-id="b4abf-109">描述</span><span class="sxs-lookup"><span data-stu-id="b4abf-109">Description</span></span>                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4abf-110"><span id="lineNumber"></span><span id="linenumber"></span><span id="LINENUMBER"></span>*lineNumber*</span><span class="sxs-lookup"><span data-stu-id="b4abf-110"><span id="lineNumber"></span><span id="linenumber"></span><span id="LINENUMBER"></span>*lineNumber*</span></span><br/>                    | <span data-ttu-id="b4abf-111">要設定的行號。</span><span class="sxs-lookup"><span data-stu-id="b4abf-111">Line number to set.</span></span> <span data-ttu-id="b4abf-112">這可以是任何整數常數。</span><span class="sxs-lookup"><span data-stu-id="b4abf-112">This can be any integer constant.</span></span> <span data-ttu-id="b4abf-113">只要結果評估為正確的語法，就可以在前置處理標記上執行宏取代。</span><span class="sxs-lookup"><span data-stu-id="b4abf-113">Macro replacement can be performed on the preprocessing tokens, as long as the result evaluates to the correct syntax.</span></span> <br/>                     |
| <span data-ttu-id="b4abf-114"><span id="filename__optional__________"></span><span id="FILENAME__OPTIONAL__________"></span>*檔案名* \[選\]</span><span class="sxs-lookup"><span data-stu-id="b4abf-114"><span id="filename__optional__________"></span><span id="FILENAME__OPTIONAL__________"></span>*filename* \[optional\]</span></span> <br/> | <span data-ttu-id="b4abf-115">要設定的檔案名。</span><span class="sxs-lookup"><span data-stu-id="b4abf-115">Filename to set.</span></span> <span data-ttu-id="b4abf-116">檔案名可以是任意的字元組合，且必須用雙引號括住 ( "" ) 。</span><span class="sxs-lookup"><span data-stu-id="b4abf-116">The filename can be any combination of characters, and must be enclosed in double quotation marks (" ").</span></span> <span data-ttu-id="b4abf-117">如果省略此參數，則先前的檔案名會維持不變。</span><span class="sxs-lookup"><span data-stu-id="b4abf-117">If this parameter is omitted, the previous filename remains unchanged.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="b4abf-118">備註</span><span class="sxs-lookup"><span data-stu-id="b4abf-118">Remarks</span></span>

<span data-ttu-id="b4abf-119">編譯器會使用行號和檔案名來參考它在編譯期間找到的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b4abf-119">The compiler uses the line number and filename to refer to errors that it finds during compilation.</span></span> <span data-ttu-id="b4abf-120">行號通常參考目前的輸入行，檔名則參考目前的輸入檔。</span><span class="sxs-lookup"><span data-stu-id="b4abf-120">The line number usually refers to the current input line, and the filename refers to the current input file.</span></span> <span data-ttu-id="b4abf-121">每次一行程式碼處理後，行號會遞增。</span><span class="sxs-lookup"><span data-stu-id="b4abf-121">The line number is incremented after each line is processed.</span></span> <span data-ttu-id="b4abf-122">如果您變更行號和檔名，編譯器會忽略先前的值並以新的值繼續處理。</span><span class="sxs-lookup"><span data-stu-id="b4abf-122">If you change the line number and filename, the compiler ignores the previous values and continues processing with the new values.</span></span> <span data-ttu-id="b4abf-123">\#程式產生器通常會使用 line 指示詞，使錯誤訊息參考原始來源檔案，而非產生的程式。</span><span class="sxs-lookup"><span data-stu-id="b4abf-123">The \#line directive is typically used by program generators to cause error messages to refer to the original source file instead of to the generated program.</span></span>

<span data-ttu-id="b4abf-124">翻譯工具會使用行號和檔案名來決定預先定義之宏檔案 \_ \_ \_ \_ 和 \_ \_ 行 \_ \_ 的值。</span><span class="sxs-lookup"><span data-stu-id="b4abf-124">The translator uses the line number and filename to determine the values of the predefined macros \_\_FILE\_\_ and \_\_LINE\_\_.</span></span> <span data-ttu-id="b4abf-125">您可以使用這些巨集，將自述性的錯誤訊息插入程式文字中。</span><span class="sxs-lookup"><span data-stu-id="b4abf-125">You can use these macros to insert self-descriptive error messages into the program text.</span></span> <span data-ttu-id="b4abf-126">檔案 \_ \_ \_ \_ 宏會展開為字串，其內容是檔案名，以雙引號括住 ( "" ) 。</span><span class="sxs-lookup"><span data-stu-id="b4abf-126">The \_\_FILE\_\_ macro expands to a string whose contents are the filename, surrounded by double quotation marks (" ").</span></span>

## <a name="examples"></a><span data-ttu-id="b4abf-127">範例</span><span class="sxs-lookup"><span data-stu-id="b4abf-127">Examples</span></span>

<span data-ttu-id="b4abf-128">下列範例會將行號設定為151，並將檔案名設定為 "copy. c"。</span><span class="sxs-lookup"><span data-stu-id="b4abf-128">The following example sets the line number to 151 and the filename to "copy.c".</span></span>


```
#line 151 "copy.c"
```



<span data-ttu-id="b4abf-129">在下列範例中， \_ \_ \_ \_ \_ \_ \_ \_ 如果指定的判斷提示不是 true，則宏判斷提示會使用預先定義的宏行和檔案來列印來源檔案的相關錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="b4abf-129">In the following example, the macro ASSERT uses the predefined macros \_\_LINE\_\_ and \_\_FILE\_\_ to print an error message about the source file if the specified assertion is not true.</span></span>


```
#define ASSERT(cond)

if( !(cond) )\
{printf( "assertion error line %d, file(%s)\n", \
__LINE__, __FILE__ );}
```



## <a name="see-also"></a><span data-ttu-id="b4abf-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4abf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4abf-131"> (DirectX HLSL) 的預處理器指示詞 </span><span class="sxs-lookup"><span data-stu-id="b4abf-131">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





