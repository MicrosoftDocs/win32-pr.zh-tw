---
description: 您可以使用某些 Microsoft 手寫辨識器所瞭解的手寫正則運算式語法，來定義和指派自訂輸入範圍。
ms.assetid: e3afe735-eca8-4fda-bd5b-cc0ab0b6a872
title: 正則運算式語法參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c0de50ff37795032719d9bc90ee81891324ba9
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104195677"
---
# <a name="regular-expression-syntax-reference"></a><span data-ttu-id="d9770-103">正則運算式語法參考</span><span class="sxs-lookup"><span data-stu-id="d9770-103">Regular Expression Syntax Reference</span></span>

<span data-ttu-id="d9770-104">您可以使用某些 Microsoft 手寫辨識器所瞭解的手寫正則運算式語法，來定義和指派自訂輸入範圍。</span><span class="sxs-lookup"><span data-stu-id="d9770-104">You can define and assign custom input scopes using the handwriting regular expression syntax that is understood by some of the Microsoft handwriting recognizers.</span></span> <span data-ttu-id="d9770-105">語法是 .NET Framework 中 [正則運算式語言實](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) 作為的子集。</span><span class="sxs-lookup"><span data-stu-id="d9770-105">The syntax is a subset of the [Regular Expression Language Implementation](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) in the .NET Framework.</span></span>

<span data-ttu-id="d9770-106">使用手寫的正則運算式，以及其他類型的正則運算式的使用方式有一些差異。</span><span class="sxs-lookup"><span data-stu-id="d9770-106">There are some differences in the way that handwriting regular expressions are used and the way the other types of regular expressions are used.</span></span> <span data-ttu-id="d9770-107">手寫語法是用來指定將由辨識引擎比對的精確字串，而不是子字串。</span><span class="sxs-lookup"><span data-stu-id="d9770-107">The handwriting syntax is used to specify an exact string that will be matched by the recognition engine and not a sub-string.</span></span> <span data-ttu-id="d9770-108">For example, the regular expression s(\[a-z\]+)p would return matches for "soup", "stop", "instep", and "esophagus".</span><span class="sxs-lookup"><span data-stu-id="d9770-108">For example, the regular expression s(\[a-z\]+)p would return matches for "soup", "stop", "instep", and "esophagus".</span></span> <span data-ttu-id="d9770-109">Whereas, an equivalent handwriting regular expression such as s(!IS\_ONECHAR)+p would match "soup" and "stop", but not "instep" and "esophagus".</span><span class="sxs-lookup"><span data-stu-id="d9770-109">Whereas, an equivalent handwriting regular expression such as s(!IS\_ONECHAR)+p would match "soup" and "stop", but not "instep" and "esophagus".</span></span>

<span data-ttu-id="d9770-110">手寫的正則運算式不支援正則運算式內的非中斷空格。</span><span class="sxs-lookup"><span data-stu-id="d9770-110">Handwriting regular expressions do not support non-breaking spaces within regular expressions.</span></span> <span data-ttu-id="d9770-111">也就是說，您無法在手寫的正則運算式內使用 "-" 實體。</span><span class="sxs-lookup"><span data-stu-id="d9770-111">That is, you cannot use the "nbsp" entity within a handwriting regular expression.</span></span>

<span data-ttu-id="d9770-112">下列各節會更詳細地說明語法。</span><span class="sxs-lookup"><span data-stu-id="d9770-112">The following sections describe the syntax in more detail.</span></span>

## <a name="valid-operators"></a><span data-ttu-id="d9770-113">有效運算子</span><span class="sxs-lookup"><span data-stu-id="d9770-113">Valid Operators</span></span>

<span data-ttu-id="d9770-114">下列運算子適用于建立正則運算式來定義手寫辨識器的輸入範圍。</span><span class="sxs-lookup"><span data-stu-id="d9770-114">The following operators are valid for creating regular expressions to define input scopes for handwriting recognizers.</span></span>



| <span data-ttu-id="d9770-115">運算子</span><span class="sxs-lookup"><span data-stu-id="d9770-115">Operator</span></span>      | <span data-ttu-id="d9770-116">描述</span><span class="sxs-lookup"><span data-stu-id="d9770-116">Description</span></span>                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| \*<br/> | <span data-ttu-id="d9770-117">後置一元運算子，表示運算元的零次或多次。</span><span class="sxs-lookup"><span data-stu-id="d9770-117">Postfix unary operator signifying zero or more occurrences of the operand.</span></span><br/> |
| +<br/>  | <span data-ttu-id="d9770-118">後置一元運算子，表示運算元的一或多個出現。</span><span class="sxs-lookup"><span data-stu-id="d9770-118">Postfix unary operator signifying one or more occurrences of the operand.</span></span><br/>  |
| <span data-ttu-id="d9770-119">?</span><span class="sxs-lookup"><span data-stu-id="d9770-119">?</span></span><br/>  | <span data-ttu-id="d9770-120">後置一元運算子，表示運算元的零次或一次發生。</span><span class="sxs-lookup"><span data-stu-id="d9770-120">Postfix unary operator signifying zero or one occurrence of the operand.</span></span><br/>   |
| \|<br/> | <span data-ttu-id="d9770-121">二元中綴運算子的意義為 "or"。</span><span class="sxs-lookup"><span data-stu-id="d9770-121">Binary infix operator meaning "or".</span></span><br/>                                        |
| <span data-ttu-id="d9770-122">()</span><span class="sxs-lookup"><span data-stu-id="d9770-122">()</span></span><br/> | <span data-ttu-id="d9770-123">用來將專案分組。</span><span class="sxs-lookup"><span data-stu-id="d9770-123">Used to group items.</span></span><br/>                                                       |



 

<span data-ttu-id="d9770-124">Microsoft 對手寫辨識器的正則運算式執行，允許重複的後置一元運算子應用程式。</span><span class="sxs-lookup"><span data-stu-id="d9770-124">The Microsoft implementation of regular expressions for handwriting recognizers allows repeated applications of postfix unary operators.</span></span> <span data-ttu-id="d9770-125">例如，a \* \* = (a \*) \* = a \* ，b？？</span><span class="sxs-lookup"><span data-stu-id="d9770-125">For example, a\*\* = (a\*)\* = a\*, b??</span></span> <span data-ttu-id="d9770-126">= (b？ ) ？</span><span class="sxs-lookup"><span data-stu-id="d9770-126">= (b?)?</span></span> <span data-ttu-id="d9770-127">= b？。</span><span class="sxs-lookup"><span data-stu-id="d9770-127">= b?.</span></span> <span data-ttu-id="d9770-128">它們也允許非連續的重複專案，例如： a \* ？ \* = ( (\*) ？ ) \* = (\*) \* = a \* 。</span><span class="sxs-lookup"><span data-stu-id="d9770-128">They also allow non-consecutive repetitions, for example: a\*?\* = ((a\*)?)\* = (a\*)\* = a\*.</span></span> <span data-ttu-id="d9770-129">這不同于 .NET Framework 的正則運算式，這種運算式只允許？</span><span class="sxs-lookup"><span data-stu-id="d9770-129">This is different from .NET Framework regular expressions, which only allow the ?</span></span> <span data-ttu-id="d9770-130">要重複的運算子。</span><span class="sxs-lookup"><span data-stu-id="d9770-130">operator to be repeated.</span></span>

<span data-ttu-id="d9770-131">.NET Framework 正則運算式的另一項差異是，手寫的正則運算式不支援以空的括弧配對指定的空白運算式， () 。</span><span class="sxs-lookup"><span data-stu-id="d9770-131">Another difference from .NET Framework regular expressions is that handwriting regular expressions do not support an empty expression designated with an empty pair of parentheses, ().</span></span>

> [!Note]  
> <span data-ttu-id="d9770-132">手寫的正則運算式只支援1252字碼頁中的字元。</span><span class="sxs-lookup"><span data-stu-id="d9770-132">Only characters in the 1252 codepage are supported for handwriting regular expressions.</span></span>

 

## <a name="using-input-scopes"></a><span data-ttu-id="d9770-133">使用輸入範圍</span><span class="sxs-lookup"><span data-stu-id="d9770-133">Using Input Scopes</span></span>

<span data-ttu-id="d9770-134">您也可以在正則運算式中，使用一組定義為 [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) 函式一部分的一般輸入範圍。</span><span class="sxs-lookup"><span data-stu-id="d9770-134">You can also use the set of regular input scopes that are defined as part of the [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) function in your regular expressions.</span></span> <span data-ttu-id="d9770-135">例如，Month (數值) 的值是 \_ 日期 \_ 月份。</span><span class="sxs-lookup"><span data-stu-id="d9770-135">For example, the value for Month (numerical) is IS\_DATE\_MONTH.</span></span> <span data-ttu-id="d9770-136">在正則運算式中指定輸入範圍的語法是在輸入範圍列舉值前面加上左括弧和驚嘆號（ (！），並在結尾處加上右括弧 ) 。</span><span class="sxs-lookup"><span data-stu-id="d9770-136">The syntax for specifying an input scope as part of a regular expression is to prepend the input scope enumerated value with an open parenthesis and an exclamation point, (!, and place a closing parenthesis, ), on the end.</span></span> <span data-ttu-id="d9770-137">例如：</span><span class="sxs-lookup"><span data-stu-id="d9770-137">For example:</span></span>

<span data-ttu-id="d9770-138"> (！是 \_ 日期 \_ 月份) </span><span class="sxs-lookup"><span data-stu-id="d9770-138">(!IS\_DATE\_MONTH)</span></span>

<span data-ttu-id="d9770-139">如果您透過 \_ ORing 任何其他輸入範圍來合併 [是預設輸入範圍]，則其效果是辨識器可以傳回預設語言模型支援的任何單一運算式 (例如，系統字典中的一個單字，或包含或不含標點符號的日期) ，或任何符合要傳入辨識器之正則運算式其餘部分的值。</span><span class="sxs-lookup"><span data-stu-id="d9770-139">If you combine the IS\_DEFAULT input scope by ORing it with any other input scope, the effect is that the recognizer can return either any single expression that the default language model supports (for example, one word from the system dictionary or a date) with or without punctuation, or any value that meets the rest of the regular expression passed in to the recognizer.</span></span>

> [!Note]  
> <span data-ttu-id="d9770-140">正則運算式中不支援下列 [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) 成員： \_ PHRASELIST、 \_ REGULAREXPRESSION、是 \_ SRGS、是否為 \_ XML。</span><span class="sxs-lookup"><span data-stu-id="d9770-140">The following members of [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) are not supported in regular expressions: IS\_PHRASELIST, IS\_REGULAREXPRESSION, IS\_SRGS, IS\_XML.</span></span>

 

## <a name="unsupported-operators"></a><span data-ttu-id="d9770-141">不支援的運算子</span><span class="sxs-lookup"><span data-stu-id="d9770-141">Unsupported Operators</span></span>

<span data-ttu-id="d9770-142">建立手寫正則運算式時，不支援下列正則運算式運算子。</span><span class="sxs-lookup"><span data-stu-id="d9770-142">The following regular expression operators are not supported when creating handwriting regular expressions.</span></span>



| <span data-ttu-id="d9770-143">運算子</span><span class="sxs-lookup"><span data-stu-id="d9770-143">Operator</span></span>                                     | <span data-ttu-id="d9770-144">描述</span><span class="sxs-lookup"><span data-stu-id="d9770-144">Description</span></span>                                                         |
|----------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d9770-145">.</span><span class="sxs-lookup"><span data-stu-id="d9770-145">.</span></span><br/>                                 | <span data-ttu-id="d9770-146">句號字元。</span><span class="sxs-lookup"><span data-stu-id="d9770-146">Period character.</span></span><br/>                                        |
| \[\]<br/>                              | <span data-ttu-id="d9770-147">方括弧。</span><span class="sxs-lookup"><span data-stu-id="d9770-147">Square brackets.</span></span> <span data-ttu-id="d9770-148">使用括弧來群組專案。</span><span class="sxs-lookup"><span data-stu-id="d9770-148">Use parenthesis for grouping items.</span></span><br/>     |
| {}<br/>                                | <span data-ttu-id="d9770-149">大括弧。</span><span class="sxs-lookup"><span data-stu-id="d9770-149">Curly brackets.</span></span><br/>                                          |
| <span data-ttu-id="d9770-150"> (？ \#批註) 和 \# \[ 批註\]</span><span class="sxs-lookup"><span data-stu-id="d9770-150">(?\# comment) and \#\[ comment \]</span></span><br/> | <span data-ttu-id="d9770-151">註解。</span><span class="sxs-lookup"><span data-stu-id="d9770-151">Comments.</span></span><br/>                                                |
| $<br/>                                 | <span data-ttu-id="d9770-152">貨幣符號字元。</span><span class="sxs-lookup"><span data-stu-id="d9770-152">Dollar sign character.</span></span><br/>                                   |
| ^<br/>                                 | <span data-ttu-id="d9770-153">插入號字元。</span><span class="sxs-lookup"><span data-stu-id="d9770-153">Caret character.</span></span><br/>                                         |
| -<br/>                                 | <span data-ttu-id="d9770-154">虛線字元。</span><span class="sxs-lookup"><span data-stu-id="d9770-154">Dash character.</span></span> <span data-ttu-id="d9770-155">必須或 (\|) 所有的專案集合。</span><span class="sxs-lookup"><span data-stu-id="d9770-155">Must OR (\|) together all sets of items.</span></span><br/> |



 

## <a name="escaping-characters"></a><span data-ttu-id="d9770-156">逸出字元</span><span class="sxs-lookup"><span data-stu-id="d9770-156">Escaping Characters</span></span>

<span data-ttu-id="d9770-157">除了下表所示的一般字元之外，也會比對。</span><span class="sxs-lookup"><span data-stu-id="d9770-157">Ordinary characters, other than the ones in the following table, match themselves.</span></span> <span data-ttu-id="d9770-158">也就是說，正則運算式中的 "a" 會指定輸入應符合 "a"。</span><span class="sxs-lookup"><span data-stu-id="d9770-158">That is, an "a" in a regular expression specifies that input should match an "a".</span></span>

<span data-ttu-id="d9770-159">撰寫手寫正則運算式的另一個顯著差異在於，您只能在正則運算式中，對一組有限的字元進行換用。</span><span class="sxs-lookup"><span data-stu-id="d9770-159">Another significant difference in writing handwriting regular expressions is that you can only escape a limited set of characters within a regular expression.</span></span> <span data-ttu-id="d9770-160">下表概述可以進行轉義的允許字元集。</span><span class="sxs-lookup"><span data-stu-id="d9770-160">The following table outlines the allowed set of characters that can be escaped.</span></span> <span data-ttu-id="d9770-161">任何其他將字元換用的嘗試都會導致辨識器擲回錯誤。</span><span class="sxs-lookup"><span data-stu-id="d9770-161">Any other attempt to escape a character will result in an error being thrown by the recognizer.</span></span>



| <span data-ttu-id="d9770-162">字元</span><span class="sxs-lookup"><span data-stu-id="d9770-162">Character</span></span>       |
|-----------------|
| \\\*<br/> |
| \\+<br/>  |
| <span data-ttu-id="d9770-163">\\?</span><span class="sxs-lookup"><span data-stu-id="d9770-163">\\?</span></span><br/>  |
| <span data-ttu-id="d9770-164">\\(</span><span class="sxs-lookup"><span data-stu-id="d9770-164">\\(</span></span><br/>  |
| <span data-ttu-id="d9770-165">\\)</span><span class="sxs-lookup"><span data-stu-id="d9770-165">\\)</span></span><br/>  |
| \\\|<br/> |
| \\\\<br/> |
| <span data-ttu-id="d9770-166">\\!</span><span class="sxs-lookup"><span data-stu-id="d9770-166">\\!</span></span><br/>  |
| <span data-ttu-id="d9770-167">\\.</span><span class="sxs-lookup"><span data-stu-id="d9770-167">\\.</span></span><br/>  |
| \\\[<br/> |
| \\\]<br/> |
| \\^<br/>  |
| <span data-ttu-id="d9770-168">\\{</span><span class="sxs-lookup"><span data-stu-id="d9770-168">\\{</span></span><br/>  |
| <span data-ttu-id="d9770-169">\\}</span><span class="sxs-lookup"><span data-stu-id="d9770-169">\\}</span></span><br/>  |
| \\$<br/>  |
| \\\#<br/> |



 

 

 