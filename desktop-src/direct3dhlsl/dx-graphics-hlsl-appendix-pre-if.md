---
title: " if、elif、else 和 endif 指示詞"
description: 控制原始程式檔部分編譯的預處理器指示詞。
ms.assetid: f29e5a9b-cc0c-4fca-aac7-809a226eda58
keywords:
- if、elif、else 和 endif 指示詞 HLSL
topic_type:
- apiref
api_name:
- if, elif, else, and endif Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a32206232c726f19febf77c3f3270882894a6747
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092741"
---
# <a name="if-elif-else-and-endif-directives"></a><span data-ttu-id="99a3f-104">\#if、 \# elif、 \# else 和 \# endif 指示詞</span><span class="sxs-lookup"><span data-stu-id="99a3f-104">\#if, \#elif, \#else, and \#endif Directives</span></span>

<span data-ttu-id="99a3f-105">控制原始程式檔部分編譯的預處理器指示詞。</span><span class="sxs-lookup"><span data-stu-id="99a3f-105">Preprocessor directives that control compilation of portions of a source file.</span></span>



| <span data-ttu-id="99a3f-106">\#如果 *ifCondition* .。。</span><span class="sxs-lookup"><span data-stu-id="99a3f-106">\#if *ifCondition* ...</span></span>         |
|--------------------------------|
| <span data-ttu-id="99a3f-107">\[\#elif *elifCondition* .。。\]</span><span class="sxs-lookup"><span data-stu-id="99a3f-107">\[\#elif *elifCondition* ...\]</span></span> |
| <span data-ttu-id="99a3f-108">\[\#還。。。\]</span><span class="sxs-lookup"><span data-stu-id="99a3f-108">\[\#else ...\]</span></span>                 |
| <span data-ttu-id="99a3f-109">\#endif</span><span class="sxs-lookup"><span data-stu-id="99a3f-109">\#endif</span></span>                        |



 

## <a name="parameters"></a><span data-ttu-id="99a3f-110">參數</span><span class="sxs-lookup"><span data-stu-id="99a3f-110">Parameters</span></span>



| <span data-ttu-id="99a3f-111">項目</span><span class="sxs-lookup"><span data-stu-id="99a3f-111">Item</span></span>                                                                                                                                                                                                 | <span data-ttu-id="99a3f-112">描述</span><span class="sxs-lookup"><span data-stu-id="99a3f-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99a3f-113"><span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifCondition*</span><span class="sxs-lookup"><span data-stu-id="99a3f-113"><span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifCondition*</span></span><br/>                                                                                   | <span data-ttu-id="99a3f-114">要評估的主要條件。</span><span class="sxs-lookup"><span data-stu-id="99a3f-114">Primary condition to evaluate.</span></span> <span data-ttu-id="99a3f-115">如果此參數評估為非零值，則此 if 指示詞 \# 和下一個 elif、else 或 endif 的實例之間的所有文字 \# \# \# 都會保留在轉譯單位中，否則不會保留後續的原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="99a3f-115">If this parameter evaluates to a nonzero value, all text between this \#if directive and the next instance of the \#elif, \#else, or \#endif directive is retained in the translation unit; otherwise, the subsequent source code is not retained.</span></span> <br/> <span data-ttu-id="99a3f-116">條件可以使用定義的預處理器運算子來判斷是否已定義特定的預處理器常數或宏;此使用方式相當於使用[ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md)指示詞。</span><span class="sxs-lookup"><span data-stu-id="99a3f-116">The condition can use the preprocessor operator defined to determine whether a specific preprocessor constant or macro is defined; this usage is equivalent to the use of the [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) directive.</span></span> <br/> <span data-ttu-id="99a3f-117">如需 *ifCondition* 參數值的限制，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="99a3f-117">See the Remarks section for restrictions on the value of the *ifCondition* parameter.</span></span> <br/>                                                                                        |
| <span data-ttu-id="99a3f-118"><span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elifCondition* \[選\]</span><span class="sxs-lookup"><span data-stu-id="99a3f-118"><span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elifCondition* \[optional\]</span></span> <br/> | <span data-ttu-id="99a3f-119">要評估的其他條件。</span><span class="sxs-lookup"><span data-stu-id="99a3f-119">Other condition to evaluate.</span></span> <span data-ttu-id="99a3f-120">如果 *ifCondition* 參數和所有先前的 \# elif 指示詞都評估為零，且此參數評估為非零值，則此 \# elif 指示詞和下一個 \# elif、else 或 endif 實例之間的所有文字 \# \# 都會保留在轉譯單位中; 否則，將不會保留後續的原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="99a3f-120">If the *ifCondition* parameter and all previous \#elif directives evaluate to zero, and this parameter evaluates to a nonzero value, all text between this \#elif directive and the next instance of the \#elif, \#else, or \#endif directive is retained in the translation unit; otherwise, the subsequent source code is not retained.</span></span> <br/> <span data-ttu-id="99a3f-121">條件可以使用定義的預處理器運算子來判斷是否已定義特定的預處理器常數或宏;此使用方式相當於使用[ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md)指示詞。</span><span class="sxs-lookup"><span data-stu-id="99a3f-121">The condition can use the preprocessor operator defined to determine whether a specific preprocessor constant or macro is defined; this usage is equivalent to the use of the [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) directive.</span></span> <br/> <span data-ttu-id="99a3f-122">如需 *elifCondition* 參數值的限制，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="99a3f-122">See the Remarks section for restrictions on the value of the *elifCondition* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="99a3f-123">備註</span><span class="sxs-lookup"><span data-stu-id="99a3f-123">Remarks</span></span>

<span data-ttu-id="99a3f-124">來源檔案中的每個 if 指示詞都 \# 必須與結尾的 endif 指示詞相符 \# 。</span><span class="sxs-lookup"><span data-stu-id="99a3f-124">Each \#if directive in a source file must be matched by a closing \#endif directive.</span></span> <span data-ttu-id="99a3f-125">\#If 和 endif 指示詞之間可以出現任何數目的 elif 指示詞 \# \# ，但最多隻允許一個 else 指示詞 \# 。</span><span class="sxs-lookup"><span data-stu-id="99a3f-125">Any number of \#elif directives can appear between the \#if and \#endif directives, but at most one \#else directive is allowed.</span></span> <span data-ttu-id="99a3f-126">Else 指示詞 \# （如果有的話）必須是 endif 之前的最後一個指示詞 \# 。</span><span class="sxs-lookup"><span data-stu-id="99a3f-126">The \#else directive, if present, must be the last directive before \#endif.</span></span> <span data-ttu-id="99a3f-127">Include 檔案中包含的條件式編譯指示詞必須滿足相同的條件。</span><span class="sxs-lookup"><span data-stu-id="99a3f-127">Conditional-compilation directives contained in include files must satisfy the same conditions.</span></span>

<span data-ttu-id="99a3f-128">\#If、 \# elif、 \# else 和 endif 指示詞 \# 可以嵌套在其他 if 指示詞的文字部分中 \# 。</span><span class="sxs-lookup"><span data-stu-id="99a3f-128">The \#if, \#elif, \#else, and \#endif directives can nest in the text portions of other \#if directives.</span></span> <span data-ttu-id="99a3f-129">每個 nested \# 的 else、 \# elif 或 endif 指示詞都 \# 屬於最接近的前置 \# if 指示詞。</span><span class="sxs-lookup"><span data-stu-id="99a3f-129">Each nested \#else, \#elif, or \#endif directive belongs to the closest preceding \#if directive.</span></span>

<span data-ttu-id="99a3f-130">如果沒有任何條件評估為非零值，預處理器會選取 else 指示詞之後的文字區塊 \# 。</span><span class="sxs-lookup"><span data-stu-id="99a3f-130">If no conditions evaluate to a nonzero value, the preprocessor selects the text block after the \#else directive.</span></span> <span data-ttu-id="99a3f-131">如果 \# 省略 else 子句，而且沒有任何條件評估為非零值，則不會選取任何文字區塊。</span><span class="sxs-lookup"><span data-stu-id="99a3f-131">If the \#else clause is omitted and no conditions evaluate to a nonzero value, no text block is selected.</span></span>

<span data-ttu-id="99a3f-132">*IfCondition* 和 *elifCondition* 參數非常符合下列需求：</span><span class="sxs-lookup"><span data-stu-id="99a3f-132">The *ifCondition* and *elifCondition* parameters much meet the following requirements:</span></span>

-   <span data-ttu-id="99a3f-133">條件式編譯運算式會視為 [**帶正負**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) 號的 long 值，而且這些運算式會使用與 c + + 中的運算式相同的規則來評估。</span><span class="sxs-lookup"><span data-stu-id="99a3f-133">Conditional compilation expressions are treated as [**signed long**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) values, and these expressions are evaluated using the same rules as expressions in C++.</span></span>
-   <span data-ttu-id="99a3f-134">運算式必須是整數類型，而且只能包含整數常數、字元常數和 defined 運算子。</span><span class="sxs-lookup"><span data-stu-id="99a3f-134">Expressions must have integral type and can include only integer constants, character constants, and the defined operator.</span></span>
-   <span data-ttu-id="99a3f-135">運算式不能使用 **sizeof** 或類型轉換運算子。</span><span class="sxs-lookup"><span data-stu-id="99a3f-135">Expressions cannot use **sizeof** or a type-cast operator.</span></span>
-   <span data-ttu-id="99a3f-136">目標環境可能無法表示所有範圍的整數。</span><span class="sxs-lookup"><span data-stu-id="99a3f-136">The target environment may not be able to represent all ranges of integers.</span></span>
-   <span data-ttu-id="99a3f-137">轉譯代表類型 [**int**](/windows/desktop/WinProg/windows-data-types) 和 **long** 類型相同，而不 [**帶正負**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) 號的 int 則與不 **帶正負** 號的 long 相同。</span><span class="sxs-lookup"><span data-stu-id="99a3f-137">The translation represents type [**int**](/windows/desktop/WinProg/windows-data-types) the same as type **long**, and [**unsigned int**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) the same as **unsigned long**.</span></span>
-   <span data-ttu-id="99a3f-138">轉譯器可以將字元常數轉譯為一組與目標環境的一組程式碼值不同的程式碼值。</span><span class="sxs-lookup"><span data-stu-id="99a3f-138">The translator can translate character constants to a set of code values different from the set for the target environment.</span></span> <span data-ttu-id="99a3f-139">若要判斷目標環境的屬性，請於針對目標環境建置之應用程式的 LIMITS.H 中檢查巨集的值。</span><span class="sxs-lookup"><span data-stu-id="99a3f-139">To determine the properties of the target environment, check values of macros from LIMITS.H in an application built for the target environment.</span></span>
-   <span data-ttu-id="99a3f-140">運算式不得執行任何環境查詢，並且必須與目標電腦上的實作詳細資料保持隔離。</span><span class="sxs-lookup"><span data-stu-id="99a3f-140">The expression must not perform any environmental inquiries and must remain insulated from implementation details on the target computer.</span></span>

## <a name="examples"></a><span data-ttu-id="99a3f-141">範例</span><span class="sxs-lookup"><span data-stu-id="99a3f-141">Examples</span></span>

<span data-ttu-id="99a3f-142">本節包含示範如何使用條件式編譯預處理器指示詞的範例。</span><span class="sxs-lookup"><span data-stu-id="99a3f-142">This section contains examples that demonstrate how to use conditional compilation preprocessor directives.</span></span>

### <a name="use-of-the-defined-operator"></a><span data-ttu-id="99a3f-143">使用已定義的運算子</span><span class="sxs-lookup"><span data-stu-id="99a3f-143">Use of the defined operator</span></span>

<span data-ttu-id="99a3f-144">下列範例示範如何使用已定義的運算子。</span><span class="sxs-lookup"><span data-stu-id="99a3f-144">The following example shows the use of the defined operator.</span></span> <span data-ttu-id="99a3f-145">如果定義了識別碼點數，則會編譯對 **點數** 函式的呼叫。</span><span class="sxs-lookup"><span data-stu-id="99a3f-145">If the identifier CREDIT is defined, the call to the **credit** function is compiled.</span></span> <span data-ttu-id="99a3f-146">如果定義了識別碼的付款，則會編譯對 **借方** 函式的呼叫。</span><span class="sxs-lookup"><span data-stu-id="99a3f-146">If the identifier DEBIT is defined, the call to the **debit** function is compiled.</span></span> <span data-ttu-id="99a3f-147">如果未定義任何識別碼，則會編譯 **printerror** 函數的呼叫。</span><span class="sxs-lookup"><span data-stu-id="99a3f-147">If neither identifier is defined, the call to the **printerror** function is compiled.</span></span> <span data-ttu-id="99a3f-148">請注意，「點數」和「點數」是 C 和 c + + 中的相異識別碼，因為它們的案例不同。</span><span class="sxs-lookup"><span data-stu-id="99a3f-148">Note that "CREDIT" and "credit" are distinct identifiers in C and C++ because their cases are different.</span></span>


```
#if defined(CREDIT)
    credit();
#elif defined(DEBIT)
    debit();
#else
    printerror();
#endif
```



### <a name="use-of-nested-if-directives"></a><span data-ttu-id="99a3f-149">使用 nested if 指示詞 \#</span><span class="sxs-lookup"><span data-stu-id="99a3f-149">Use of nested \#if directives</span></span>

<span data-ttu-id="99a3f-150">下列範例示範如何將 if 指示詞嵌套 \# 。</span><span class="sxs-lookup"><span data-stu-id="99a3f-150">The following example shows how to nest \#if directives.</span></span> <span data-ttu-id="99a3f-151">這個範例假設先前已定義名為 DLEVEL 的符號常數。</span><span class="sxs-lookup"><span data-stu-id="99a3f-151">This example assumes that a symbolic constant named DLEVEL has been previously defined.</span></span> <span data-ttu-id="99a3f-152">\#Elif 和 \# else 指示詞會根據 DLEVEL 的值，用來建立四個選項的其中之一。</span><span class="sxs-lookup"><span data-stu-id="99a3f-152">The \#elif and \#else directives are used to make one of four choices, based on the value of DLEVEL.</span></span> <span data-ttu-id="99a3f-153">常數堆疊設定為0、100或200，視 DLEVEL 的定義而定。</span><span class="sxs-lookup"><span data-stu-id="99a3f-153">The constant STACK is set to 0, 100, or 200, depending on the definition of DLEVEL.</span></span> <span data-ttu-id="99a3f-154">如果 DLEVEL 大於5，則不會定義 STACK。</span><span class="sxs-lookup"><span data-stu-id="99a3f-154">If DLEVEL is greater than 5, then STACK is not defined.</span></span>


```
#if DLEVEL > 5
    #define SIGNAL  1
    #if STACKUSE == 1
        #define STACK   200
    #else
        #define STACK   100
    #endif
#else
    #define SIGNAL  0
    #if STACKUSE == 1
        #define STACK   100
    #else
        #define STACK   50
    #endif
#endif
#if DLEVEL == 0
    #define STACK 0
#elif DLEVEL == 1
    #define STACK 100
#elif DLEVEL > 5
    display( debugptr );
#else
    #define STACK 200
#endif
```



### <a name="use-for-including-header-files"></a><span data-ttu-id="99a3f-155">用於包含標頭檔</span><span class="sxs-lookup"><span data-stu-id="99a3f-155">Use for including header files</span></span>

<span data-ttu-id="99a3f-156">條件式編譯的常見用途是防止多次包含相同的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="99a3f-156">A common use for conditional compilation is to prevent multiple inclusions of the same header file.</span></span> <span data-ttu-id="99a3f-157">在 c + + 中，類別通常定義在標頭檔中，而條件式編譯結構可以用來防止多個定義。</span><span class="sxs-lookup"><span data-stu-id="99a3f-157">In C++, where classes are often defined in header files, conditional compilation constructs can be used to prevent multiple definitions.</span></span> <span data-ttu-id="99a3f-158">下列範例會判斷是否已定義符號常數範例 \_ H。</span><span class="sxs-lookup"><span data-stu-id="99a3f-158">The following example determines whether the symbolic constant EXAMPLE\_H is defined.</span></span> <span data-ttu-id="99a3f-159">如果是，就已包含該檔案，而且不需要重新處理;如果沒有，則 \_ 會定義常數範例 H 來指出該範例。H 已經處理。</span><span class="sxs-lookup"><span data-stu-id="99a3f-159">If so, the file has already been included and does not need to be reprocessed; if not, the constant EXAMPLE\_H is defined to indicate that EXAMPLE.H has already been processed.</span></span>


```
#if !defined( EXAMPLE_H )
#define EXAMPLE_H

class Example
{
...
};

#endif // !defined( EXAMPLE_H )
```



## <a name="see-also"></a><span data-ttu-id="99a3f-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99a3f-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99a3f-161"> (DirectX HLSL) 的預處理器指示詞 </span><span class="sxs-lookup"><span data-stu-id="99a3f-161">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

