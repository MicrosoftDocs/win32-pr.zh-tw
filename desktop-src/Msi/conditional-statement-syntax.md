---
description: 本章節描述 MsiEvaluateCondition 函數和動作順序資料表所使用之條件陳述式的語法。 如需詳細資訊，請參閱，條件陳述式語法的範例。
ms.assetid: 6f1657f9-063b-4d57-ad76-95e3dbe25786
title: 條件陳述式語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0548a71756faff654bfe2b49e14c0581a6248a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848936"
---
# <a name="conditional-statement-syntax"></a><span data-ttu-id="53161-104">條件陳述式語法</span><span class="sxs-lookup"><span data-stu-id="53161-104">Conditional Statement Syntax</span></span>

<span data-ttu-id="53161-105">本章節描述 [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) 函數和動作 [順序資料表](using-a-sequence-table.md)所使用之條件陳述式的語法。</span><span class="sxs-lookup"><span data-stu-id="53161-105">This section describes the syntax of conditional statements used by the [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) function and the action [sequence tables](using-a-sequence-table.md).</span></span> <span data-ttu-id="53161-106">如需詳細資訊，請參閱， [條件陳述式語法的範例](examples-of-conditional-statement-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="53161-106">For more information, see, [Examples of Conditional Statement Syntax](examples-of-conditional-statement-syntax.md).</span></span>

## <a name="summary-of-conditional-statement-syntax"></a><span data-ttu-id="53161-107">條件陳述式語法的摘要</span><span class="sxs-lookup"><span data-stu-id="53161-107">Summary of Conditional Statement Syntax</span></span>

<span data-ttu-id="53161-108">此資料表和下列清單摘要說明在條件運算式中使用的語法。</span><span class="sxs-lookup"><span data-stu-id="53161-108">This table and the following list summarize the syntax to use in conditional expressions.</span></span>



| <span data-ttu-id="53161-109">項目</span><span class="sxs-lookup"><span data-stu-id="53161-109">Item</span></span>                | <span data-ttu-id="53161-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="53161-110">Syntax</span></span>                                                                                                          |
|---------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53161-111">value</span><span class="sxs-lookup"><span data-stu-id="53161-111">value</span></span>               | <span data-ttu-id="53161-112">符號 \| 常值 \| 整數</span><span class="sxs-lookup"><span data-stu-id="53161-112">symbol \| literal \| integer</span></span>                                                                                    |
| <span data-ttu-id="53161-113">比較-運算子</span><span class="sxs-lookup"><span data-stu-id="53161-113">comparison-operator</span></span> | < \| > \| <= \| >= \| = \| <>                                                                 |
| <span data-ttu-id="53161-114">詞彙</span><span class="sxs-lookup"><span data-stu-id="53161-114">term</span></span>                | <span data-ttu-id="53161-115">值 \| 比較-運算子值 \| ( 運算式 ) \|</span><span class="sxs-lookup"><span data-stu-id="53161-115">value \| value comparison-operator value \| ( expression )\|</span></span>                                                    |
| <span data-ttu-id="53161-116">布林值因數</span><span class="sxs-lookup"><span data-stu-id="53161-116">Boolean-factor</span></span>      | <span data-ttu-id="53161-117">詞彙 \| **不** 是詞彙</span><span class="sxs-lookup"><span data-stu-id="53161-117">term \| **NOT** term</span></span>                                                                                            |
| <span data-ttu-id="53161-118">布林值詞彙</span><span class="sxs-lookup"><span data-stu-id="53161-118">Boolean-term</span></span>        | <span data-ttu-id="53161-119">布林因數 \| 布林因數 **和** 詞彙</span><span class="sxs-lookup"><span data-stu-id="53161-119">Boolean-factor \| Boolean-factor **AND** term</span></span>                                                                   |
| <span data-ttu-id="53161-120">運算式</span><span class="sxs-lookup"><span data-stu-id="53161-120">expression</span></span>          | <span data-ttu-id="53161-121">布林詞彙 \| 布林值詞彙 **或** 運算式</span><span class="sxs-lookup"><span data-stu-id="53161-121">Boolean-term \| Boolean-term **OR** expression</span></span>                                                                  |
| <span data-ttu-id="53161-122">符號</span><span class="sxs-lookup"><span data-stu-id="53161-122">symbol</span></span>              | <span data-ttu-id="53161-123">屬性 \| % 環境-變數 \| $component-動作 \| ？元件狀態 \| &功能-動作 \| ！功能狀態</span><span class="sxs-lookup"><span data-stu-id="53161-123">property \| %environment-variable \| $component-action \| ?component-state \| &feature-action \| !feature-state</span></span> |



 

-   <span data-ttu-id="53161-124">符號名稱和值會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="53161-124">Symbol names and values are case sensitive.</span></span>
-   <span data-ttu-id="53161-125">環境變數名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="53161-125">Environment variable names are not case sensitive.</span></span>
-   <span data-ttu-id="53161-126">常值文字必須用引號括住 ( "text" ) 。</span><span class="sxs-lookup"><span data-stu-id="53161-126">Literal text must be enclosed between quotation marks ("text").</span></span>
    > [!Note]  
    > <span data-ttu-id="53161-127">包含引號的常值文字不能用在條件陳述式中，因為常值文字內沒有引號的逸出字元。</span><span class="sxs-lookup"><span data-stu-id="53161-127">Literal text containing quotation marks cannot be used in conditional statements because there is no escape character for quotation marks inside literal text.</span></span> <span data-ttu-id="53161-128">若要對包含引號的常值文字進行比較，常值文字應放在屬性中。</span><span class="sxs-lookup"><span data-stu-id="53161-128">To do a comparison against literal text containing quotation marks, the literal text should be put in a property.</span></span> <span data-ttu-id="53161-129">例如，若要確認 SERVERNAME 屬性不包含任何引號，請在 [屬性工作表](property-table.md) 中定義名為引號的屬性，其值為 "，並將條件變更為非 SERVERNAME><引號。</span><span class="sxs-lookup"><span data-stu-id="53161-129">For example, to verify that the SERVERNAME property does not contain any quotation marks, define a property called QUOTES in the [Property table](property-table.md) with a value of " and change the condition to NOT SERVERNAME><QUOTES.</span></span>

     

-   <span data-ttu-id="53161-130">不存在的屬性值會被視為空字串。</span><span class="sxs-lookup"><span data-stu-id="53161-130">Nonexistent property values are treated as empty strings.</span></span>
-   <span data-ttu-id="53161-131">不支援浮點數值。</span><span class="sxs-lookup"><span data-stu-id="53161-131">Floating point numeric values are not supported.</span></span>
-   <span data-ttu-id="53161-132">運算子和優先順序與基本和 SQL 語言中的相同。</span><span class="sxs-lookup"><span data-stu-id="53161-132">Operators and precedence are the same as in the BASIC and SQL languages.</span></span>
-   <span data-ttu-id="53161-133">不支援算術運算子。</span><span class="sxs-lookup"><span data-stu-id="53161-133">Arithmetic operators are not supported.</span></span>
-   <span data-ttu-id="53161-134">括弧可以用來覆寫運算子優先順序。</span><span class="sxs-lookup"><span data-stu-id="53161-134">Parentheses can be used to override operator precedence.</span></span>
-   <span data-ttu-id="53161-135">運算子不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="53161-135">Operators are not case sensitive.</span></span>
-   <span data-ttu-id="53161-136">針對字串比較，在運算子前面加上波狀符號 "~"，會執行不區分大小寫的比較。</span><span class="sxs-lookup"><span data-stu-id="53161-136">For string comparisons, a tilde "~" prefixed to the operator performs a comparison that is not case sensitive.</span></span>
-   <span data-ttu-id="53161-137">具有無法轉換成整數之字串或屬性值的整數比較，一律為 **msiEvaluateConditionFalse**，但比較運算子 "<>" 除外，後者會傳回 **msiEvaluateConditionTrue**。</span><span class="sxs-lookup"><span data-stu-id="53161-137">Comparison of an integer with a string or property value that cannot be converted to an integer is always **msiEvaluateConditionFalse**, except for the comparison operator "<>", which returns **msiEvaluateConditionTrue**.</span></span>

## <a name="access-prefixes"></a><span data-ttu-id="53161-138">存取首碼</span><span class="sxs-lookup"><span data-stu-id="53161-138">Access Prefixes</span></span>

<span data-ttu-id="53161-139">下表顯示用來存取各種系統和安裝程式資訊以用於條件運算式的前置詞。</span><span class="sxs-lookup"><span data-stu-id="53161-139">The following table shows the prefixes to use to access various system and installer information for use in conditional expressions.</span></span>



| <span data-ttu-id="53161-140">符號類型</span><span class="sxs-lookup"><span data-stu-id="53161-140">Symbol type</span></span>          | <span data-ttu-id="53161-141">前置詞</span><span class="sxs-lookup"><span data-stu-id="53161-141">Prefix</span></span> | <span data-ttu-id="53161-142">值</span><span class="sxs-lookup"><span data-stu-id="53161-142">Value</span></span>                                                     |
|----------------------|--------|-----------------------------------------------------------|
| <span data-ttu-id="53161-143">安裝程式屬性</span><span class="sxs-lookup"><span data-stu-id="53161-143">Installer property</span></span>   | <span data-ttu-id="53161-144">(無)</span><span class="sxs-lookup"><span data-stu-id="53161-144">(none)</span></span> | <span data-ttu-id="53161-145">屬性 ([屬性](property-table.md) 的值) 資料表。</span><span class="sxs-lookup"><span data-stu-id="53161-145">Value of property ([Property](property-table.md)) table.</span></span> |
| <span data-ttu-id="53161-146">環境變數</span><span class="sxs-lookup"><span data-stu-id="53161-146">Environment variable</span></span> | %      | <span data-ttu-id="53161-147">環境變數的值。</span><span class="sxs-lookup"><span data-stu-id="53161-147">Value of environment variable.</span></span>                            |
| <span data-ttu-id="53161-148">元件資料表索引鍵</span><span class="sxs-lookup"><span data-stu-id="53161-148">Component table key</span></span>  | $      | <span data-ttu-id="53161-149">元件的動作狀態。</span><span class="sxs-lookup"><span data-stu-id="53161-149">Action state of the component.</span></span>                            |
| <span data-ttu-id="53161-150">元件資料表索引鍵</span><span class="sxs-lookup"><span data-stu-id="53161-150">Component table key</span></span>  | <span data-ttu-id="53161-151">?</span><span class="sxs-lookup"><span data-stu-id="53161-151">?</span></span>      | <span data-ttu-id="53161-152">元件的已安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="53161-152">Installed state of the component.</span></span>                         |
| <span data-ttu-id="53161-153">功能資料表索引鍵</span><span class="sxs-lookup"><span data-stu-id="53161-153">Feature table key</span></span>    | &      | <span data-ttu-id="53161-154">功能的動作狀態。</span><span class="sxs-lookup"><span data-stu-id="53161-154">Action state of the feature.</span></span>                              |
| <span data-ttu-id="53161-155">功能資料表索引鍵</span><span class="sxs-lookup"><span data-stu-id="53161-155">Feature table key</span></span>    | <span data-ttu-id="53161-156">!</span><span class="sxs-lookup"><span data-stu-id="53161-156">!</span></span>      | <span data-ttu-id="53161-157">功能的已安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="53161-157">Installed state of the feature.</span></span>                           |



 

## <a name="logical-operators"></a><span data-ttu-id="53161-158">邏輯運算子</span><span class="sxs-lookup"><span data-stu-id="53161-158">Logical Operators</span></span>

<span data-ttu-id="53161-159">下表顯示條件運算式中的邏輯運算子（依高至低優先順序排列）。</span><span class="sxs-lookup"><span data-stu-id="53161-159">The following table shows the logical operators in conditional expressions, in order of high-to-low precedence.</span></span>



| <span data-ttu-id="53161-160">運算子</span><span class="sxs-lookup"><span data-stu-id="53161-160">Operator</span></span> | <span data-ttu-id="53161-161">意義</span><span class="sxs-lookup"><span data-stu-id="53161-161">Meaning</span></span>                                                 |
|----------|---------------------------------------------------------|
| <span data-ttu-id="53161-162">Not</span><span class="sxs-lookup"><span data-stu-id="53161-162">Not</span></span>      | <span data-ttu-id="53161-163">前置詞一元運算子;反轉下列詞彙的狀態。</span><span class="sxs-lookup"><span data-stu-id="53161-163">Prefix unary operator; inverts state of following term.</span></span> |
| <span data-ttu-id="53161-164">And</span><span class="sxs-lookup"><span data-stu-id="53161-164">And</span></span>      | <span data-ttu-id="53161-165">如果這兩個詞彙都是 TRUE，則為 TRUE。</span><span class="sxs-lookup"><span data-stu-id="53161-165">TRUE if both terms are TRUE.</span></span>                            |
| <span data-ttu-id="53161-166">Or</span><span class="sxs-lookup"><span data-stu-id="53161-166">Or</span></span>       | <span data-ttu-id="53161-167">如果任一個或兩個詞彙都是 TRUE，則為 TRUE。</span><span class="sxs-lookup"><span data-stu-id="53161-167">TRUE if either or both terms are TRUE.</span></span>                  |
| <span data-ttu-id="53161-168">Xor</span><span class="sxs-lookup"><span data-stu-id="53161-168">Xor</span></span>      | <span data-ttu-id="53161-169">如果兩個詞彙都不是 TRUE，則為 TRUE。</span><span class="sxs-lookup"><span data-stu-id="53161-169">TRUE if either but not both terms are TRUE.</span></span>             |
| <span data-ttu-id="53161-170">Eqv</span><span class="sxs-lookup"><span data-stu-id="53161-170">Eqv</span></span>      | <span data-ttu-id="53161-171">如果這兩個詞彙都為 TRUE 或兩個詞彙都為 FALSE，則為 TRUE。</span><span class="sxs-lookup"><span data-stu-id="53161-171">TRUE if both terms are TRUE or both terms are FALSE.</span></span>    |
| <span data-ttu-id="53161-172">進出口</span><span class="sxs-lookup"><span data-stu-id="53161-172">Imp</span></span>      | <span data-ttu-id="53161-173">如果 left 詞彙為 FALSE 或 right 詞彙為 TRUE，則為 TRUE。</span><span class="sxs-lookup"><span data-stu-id="53161-173">TRUE if left term is FALSE or right term is TRUE.</span></span>       |



 

## <a name="comparative-operators"></a><span data-ttu-id="53161-174">比較運算子</span><span class="sxs-lookup"><span data-stu-id="53161-174">Comparative Operators</span></span>

<span data-ttu-id="53161-175">下表顯示條件運算式中使用的比較運算子。</span><span class="sxs-lookup"><span data-stu-id="53161-175">The following table shows the comparison operators used in conditional expressions.</span></span> <span data-ttu-id="53161-176">這些比較運算子只能在兩個值之間進行。</span><span class="sxs-lookup"><span data-stu-id="53161-176">These comparison operators can only occur between two values.</span></span>



| <span data-ttu-id="53161-177">運算子</span><span class="sxs-lookup"><span data-stu-id="53161-177">Operator</span></span> | <span data-ttu-id="53161-178">意義</span><span class="sxs-lookup"><span data-stu-id="53161-178">Meaning</span></span>                                                     |
|----------|-------------------------------------------------------------|
| =        | <span data-ttu-id="53161-179">如果左值等於右邊的值，則為 TRUE。</span><span class="sxs-lookup"><span data-stu-id="53161-179">TRUE if left value is equal to right value.</span></span>                 |
| <> | <span data-ttu-id="53161-180">如果左值不等於右值，則為 TRUE。</span><span class="sxs-lookup"><span data-stu-id="53161-180">TRUE if left value is not equal to right value.</span></span>             |
| >     | <span data-ttu-id="53161-181">如果左值大於右邊的值，則為 TRUE。</span><span class="sxs-lookup"><span data-stu-id="53161-181">TRUE if left value is greater than right value.</span></span>             |
| >=    | <span data-ttu-id="53161-182">如果左值大於或等於右值，則為 TRUE。</span><span class="sxs-lookup"><span data-stu-id="53161-182">TRUE if left value is greater than or equal to right value.</span></span> |
| <     | <span data-ttu-id="53161-183">如果左值小於右值，則為 TRUE。</span><span class="sxs-lookup"><span data-stu-id="53161-183">TRUE if left value is less than right value.</span></span>                |
| <=    | <span data-ttu-id="53161-184">如果左值小於或等於右值，則為 TRUE。</span><span class="sxs-lookup"><span data-stu-id="53161-184">TRUE if left value is less than or equal to right value.</span></span>    |



 

## <a name="substring-operators"></a><span data-ttu-id="53161-185">Substring 運算子</span><span class="sxs-lookup"><span data-stu-id="53161-185">Substring Operators</span></span>

<span data-ttu-id="53161-186">下表顯示條件運算式中使用的子字串運算子。</span><span class="sxs-lookup"><span data-stu-id="53161-186">The following table shows the substring operators used in conditional expressions.</span></span> <span data-ttu-id="53161-187">子字串運算子可能會在兩個字串值之間進行。</span><span class="sxs-lookup"><span data-stu-id="53161-187">Substring operators can occur between two string values.</span></span>



| <span data-ttu-id="53161-188">運算子</span><span class="sxs-lookup"><span data-stu-id="53161-188">Operator</span></span> | <span data-ttu-id="53161-189">意義</span><span class="sxs-lookup"><span data-stu-id="53161-189">Meaning</span></span>                                           |
|----------|---------------------------------------------------|
| >< | <span data-ttu-id="53161-190">如果左字串包含正確的字串，則為 TRUE。</span><span class="sxs-lookup"><span data-stu-id="53161-190">TRUE if left string contains the right string.</span></span>    |
| << | <span data-ttu-id="53161-191">如果左字串開頭為右邊的字串，則為 TRUE。</span><span class="sxs-lookup"><span data-stu-id="53161-191">TRUE if left string starts with the right string.</span></span> |
| >> | <span data-ttu-id="53161-192">如果左字串以右字串結尾，則為 TRUE。</span><span class="sxs-lookup"><span data-stu-id="53161-192">TRUE if left string ends with the right string.</span></span>   |



 

## <a name="bitwise-numeric-operators"></a><span data-ttu-id="53161-193">位數值運算子</span><span class="sxs-lookup"><span data-stu-id="53161-193">Bitwise Numeric Operators</span></span>

<span data-ttu-id="53161-194">下表顯示條件運算式中的位數值運算子。</span><span class="sxs-lookup"><span data-stu-id="53161-194">The following table shows the bitwise numeric operators in conditional expressions.</span></span> <span data-ttu-id="53161-195">這些運算子可能會在兩個整數值之間發生。</span><span class="sxs-lookup"><span data-stu-id="53161-195">These operators can occur between two integer values.</span></span>



| <span data-ttu-id="53161-196">運算子</span><span class="sxs-lookup"><span data-stu-id="53161-196">Operator</span></span> | <span data-ttu-id="53161-197">意義</span><span class="sxs-lookup"><span data-stu-id="53161-197">Meaning</span></span>                                                                      |
|----------|------------------------------------------------------------------------------|
| >< | <span data-ttu-id="53161-198">位 AND，如果左和右整數的任何位都是共通的，則為 TRUE。</span><span class="sxs-lookup"><span data-stu-id="53161-198">Bitwise AND, TRUE if the left and right integers have any bits in common.</span></span>    |
| << | <span data-ttu-id="53161-199">如果左整數的高16位等於右邊整數，則為 True。</span><span class="sxs-lookup"><span data-stu-id="53161-199">True if the high 16-bits of the left integer are equal to the right integer.</span></span> |
| >> | <span data-ttu-id="53161-200">如果左整數的低16位等於右邊整數，則為 True。</span><span class="sxs-lookup"><span data-stu-id="53161-200">True if the low 16-bits of the left integer are equal to the right integer.</span></span>  |



 

## <a name="feature-and-component-state-values"></a><span data-ttu-id="53161-201">功能和元件狀態值</span><span class="sxs-lookup"><span data-stu-id="53161-201">Feature and Component State Values</span></span>

<span data-ttu-id="53161-202">下表顯示使用功能和元件運算子符號的有效位置。</span><span class="sxs-lookup"><span data-stu-id="53161-202">The following table shows where it is valid to use the feature and component operator symbols.</span></span>



| <span data-ttu-id="53161-203">運算元 <state></span><span class="sxs-lookup"><span data-stu-id="53161-203">Operator <state></span></span> | <span data-ttu-id="53161-204">此語法有效的位置</span><span class="sxs-lookup"><span data-stu-id="53161-204">Where this syntax is valid</span></span>                                                                                                                                         |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53161-205">$component-動作</span><span class="sxs-lookup"><span data-stu-id="53161-205">$component-action</span></span>      | <span data-ttu-id="53161-206">在 [條件](condition-table.md) 資料表中，以及在 [順序](using-a-sequence-table.md) 資料表中，于 [CostFinalize](costfinalize-action.md) 動作之後。</span><span class="sxs-lookup"><span data-stu-id="53161-206">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |
| <span data-ttu-id="53161-207">&功能-動作</span><span class="sxs-lookup"><span data-stu-id="53161-207">&feature-action</span></span>        | <span data-ttu-id="53161-208">在 [條件](condition-table.md) 資料表中，以及在 [順序](using-a-sequence-table.md) 資料表中，于 [CostFinalize](costfinalize-action.md) 動作之後。</span><span class="sxs-lookup"><span data-stu-id="53161-208">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |
| <span data-ttu-id="53161-209">！功能-狀態</span><span class="sxs-lookup"><span data-stu-id="53161-209">!feature-state</span></span>         | <span data-ttu-id="53161-210">在 [條件](condition-table.md) 資料表中，以及在 [順序](using-a-sequence-table.md) 資料表中，于 [CostFinalize](costfinalize-action.md) 動作之後。</span><span class="sxs-lookup"><span data-stu-id="53161-210">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |
| <span data-ttu-id="53161-211">？元件-狀態</span><span class="sxs-lookup"><span data-stu-id="53161-211">?component-state</span></span>       | <span data-ttu-id="53161-212">在 [條件](condition-table.md) 資料表中，以及在 [順序](using-a-sequence-table.md) 資料表中，于 [CostFinalize](costfinalize-action.md) 動作之後。</span><span class="sxs-lookup"><span data-stu-id="53161-212">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |



 

<span data-ttu-id="53161-213">下表顯示條件運算式中使用的功能和元件狀態值。</span><span class="sxs-lookup"><span data-stu-id="53161-213">The following table shows the feature and component state values used in conditional expressions.</span></span> <span data-ttu-id="53161-214">在呼叫 [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) （直接或透過 [CostFinalize](costfinalize-action.md) 動作）之前，不會設定這些狀態。</span><span class="sxs-lookup"><span data-stu-id="53161-214">These states are not set until [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) is called, either directly or by the [CostFinalize](costfinalize-action.md) action.</span></span>



| <span data-ttu-id="53161-215">狀態</span><span class="sxs-lookup"><span data-stu-id="53161-215">State</span></span>                    | <span data-ttu-id="53161-216">值</span><span class="sxs-lookup"><span data-stu-id="53161-216">Value</span></span> | <span data-ttu-id="53161-217">意義</span><span class="sxs-lookup"><span data-stu-id="53161-217">Meaning</span></span>                                                         |
|--------------------------|-------|-----------------------------------------------------------------|
| <span data-ttu-id="53161-218">INSTALLSTATE \_ 不明</span><span class="sxs-lookup"><span data-stu-id="53161-218">INSTALLSTATE\_UNKNOWN</span></span>    | <span data-ttu-id="53161-219">-1</span><span class="sxs-lookup"><span data-stu-id="53161-219">-1</span></span>    | <span data-ttu-id="53161-220">不需要在功能或元件上採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="53161-220">No action to be taken on the feature or component.</span></span>              |
| <span data-ttu-id="53161-221">INSTALLSTATE \_ 公告</span><span class="sxs-lookup"><span data-stu-id="53161-221">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="53161-222">1</span><span class="sxs-lookup"><span data-stu-id="53161-222">1</span></span>     | <span data-ttu-id="53161-223">宣告的功能。</span><span class="sxs-lookup"><span data-stu-id="53161-223">Advertised feature.</span></span> <span data-ttu-id="53161-224">元件無法使用此狀態。</span><span class="sxs-lookup"><span data-stu-id="53161-224">This state is not available for components.</span></span> |
| <span data-ttu-id="53161-225">INSTALLSTATE 不 \_ 存在</span><span class="sxs-lookup"><span data-stu-id="53161-225">INSTALLSTATE\_ABSENT</span></span>     | <span data-ttu-id="53161-226">2</span><span class="sxs-lookup"><span data-stu-id="53161-226">2</span></span>     | <span data-ttu-id="53161-227">功能或元件不存在。</span><span class="sxs-lookup"><span data-stu-id="53161-227">Feature or component is not present.</span></span>                            |
| <span data-ttu-id="53161-228">INSTALLSTATE \_ 本機</span><span class="sxs-lookup"><span data-stu-id="53161-228">INSTALLSTATE\_LOCAL</span></span>      | <span data-ttu-id="53161-229">3</span><span class="sxs-lookup"><span data-stu-id="53161-229">3</span></span>     | <span data-ttu-id="53161-230">本機電腦上的功能或元件。</span><span class="sxs-lookup"><span data-stu-id="53161-230">Feature or component on the local computer.</span></span>                     |
| <span data-ttu-id="53161-231">INSTALLSTATE \_ 來源</span><span class="sxs-lookup"><span data-stu-id="53161-231">INSTALLSTATE\_SOURCE</span></span>     | <span data-ttu-id="53161-232">4</span><span class="sxs-lookup"><span data-stu-id="53161-232">4</span></span>     | <span data-ttu-id="53161-233">從來源執行的功能或元件。</span><span class="sxs-lookup"><span data-stu-id="53161-233">Feature or component run from the source.</span></span>                       |



 

<span data-ttu-id="53161-234">例如，只有當 MyFeature 正在將其目前的狀態變更為本機電腦上所安裝的狀態時，才會評估為 True 的條件運算式 "&MyFeature = 3"，INSTALLSTATE \_ local。</span><span class="sxs-lookup"><span data-stu-id="53161-234">For example, the conditional expression "&MyFeature=3" evaluates to True only if MyFeature is changing from its current state to the state of being installed on the local computer, INSTALLSTATE\_LOCAL.</span></span>

<span data-ttu-id="53161-235">請注意，您不應該相依于 $Component 1 = 3 的條件，以檢查 Component1 是否在本機安裝在電腦上。</span><span class="sxs-lookup"><span data-stu-id="53161-235">Note that you should not depend upon the condition $Component1=3 to check whether Component1 is locally installed on the computer.</span></span> <span data-ttu-id="53161-236">如果有多個產品安裝 Component1，這可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="53161-236">This can fail if Component1 is installed by more than one product.</span></span> <span data-ttu-id="53161-237">由 Product1 在本機安裝 Component1 之後，安裝程式會在安裝 Product2 時，將條件 $Component 1 = 3 評估為 False。</span><span class="sxs-lookup"><span data-stu-id="53161-237">After Component1 has been installed locally by Product1, the installer evaluates the condition $Component1=3 as False during the installation of Product2.</span></span> <span data-ttu-id="53161-238">這是因為安裝程式會使用元件的金鑰路徑來判斷元件的版本，並在其版本大於或等於已安裝的元件時，將元件標記為安裝。</span><span class="sxs-lookup"><span data-stu-id="53161-238">This is because the installer determines the version of the component using the component's key path and marks the component for installation if its version is greater than or equal to the installed component.</span></span>

<span data-ttu-id="53161-239">請注意，安裝程式將不會直接比較準則語句中的 [版本](version.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="53161-239">Note that the installer will not do direct comparisons of the [Version](version.md) data type in conditional statements.</span></span> <span data-ttu-id="53161-240">例如，您無法在條件陳述式中使用比較運算子來比較版本，例如 "01.10" 和 "1.010"。</span><span class="sxs-lookup"><span data-stu-id="53161-240">For example, you cannot use comparative operators to compare versions such as "01.10" and "1.010" in a conditional statement.</span></span> <span data-ttu-id="53161-241">相反地，請使用有效的方法來搜尋版本，例如搜尋 [現有的應用程式、檔案、登錄專案或 .ini 檔專案](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)中所述，然後設定屬性。</span><span class="sxs-lookup"><span data-stu-id="53161-241">Instead use a valid method to search for a version, such as described in [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md), and then set a property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53161-242">相關主題</span><span class="sxs-lookup"><span data-stu-id="53161-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53161-243">在條件陳述式中使用屬性</span><span class="sxs-lookup"><span data-stu-id="53161-243">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)
</dt> </dl>

 

 



