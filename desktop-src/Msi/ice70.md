---
description: ICE70 會確認登錄專案的整數值已正確指定。
ms.assetid: f8493622-867b-42e1-9fda-a7c3229bbb4e
title: ICE70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616592a772dec6f95d81b92f03f0bffea6ce7bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985474"
---
# <a name="ice70"></a><span data-ttu-id="fb40b-103">ICE70</span><span class="sxs-lookup"><span data-stu-id="fb40b-103">ICE70</span></span>

<span data-ttu-id="fb40b-104">ICE70 會確認登錄專案的整數值已正確指定。</span><span class="sxs-lookup"><span data-stu-id="fb40b-104">ICE70 verifies that integer values for registry entries are specified correctly.</span></span> <span data-ttu-id="fb40b-105">\# \# 不會驗證表單 str、 \# % 未展開 str 的值。</span><span class="sxs-lookup"><span data-stu-id="fb40b-105">Values of the form \#\#str, \#%unexpanded str are not validated.</span></span> <span data-ttu-id="fb40b-106">\#系統會驗證表單 xhex、 \# xhex、 \# 整數和 \# \[ 屬性 \] 的值。</span><span class="sxs-lookup"><span data-stu-id="fb40b-106">Values of the form \#xhex, \#Xhex, \#integer, and \#\[property\] are validated.</span></span> <span data-ttu-id="fb40b-107">下表提供簡短的總覽。</span><span class="sxs-lookup"><span data-stu-id="fb40b-107">The following table provides a brief overview.</span></span>



| <span data-ttu-id="fb40b-108">值</span><span class="sxs-lookup"><span data-stu-id="fb40b-108">Value</span></span>                 | <span data-ttu-id="fb40b-109">驗證</span><span class="sxs-lookup"><span data-stu-id="fb40b-109">Validation</span></span>                                                                    |
|-----------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="fb40b-110">\#\#Str</span><span class="sxs-lookup"><span data-stu-id="fb40b-110">\#\#str</span></span>               | <span data-ttu-id="fb40b-111">有效</span><span class="sxs-lookup"><span data-stu-id="fb40b-111">valid</span></span>                                                                         |
| <span data-ttu-id="fb40b-112">\#% 未展開的 str</span><span class="sxs-lookup"><span data-stu-id="fb40b-112">\#%unexpanded str</span></span>     | <span data-ttu-id="fb40b-113">有效</span><span class="sxs-lookup"><span data-stu-id="fb40b-113">valid</span></span>                                                                         |
| <span data-ttu-id="fb40b-114">\#xHex、 \# xHex</span><span class="sxs-lookup"><span data-stu-id="fb40b-114">\#xHex,\#XHex</span></span>         | <span data-ttu-id="fb40b-115">驗證有效的十六進位字元 (0-9、a-f、a-f) 。</span><span class="sxs-lookup"><span data-stu-id="fb40b-115">Validate for valid hex characters (0-9,a-f,A-F).</span></span> <span data-ttu-id="fb40b-116">這裡允許屬性。</span><span class="sxs-lookup"><span data-stu-id="fb40b-116">Properties are allowed here.</span></span> |
| <span data-ttu-id="fb40b-117">\#+ int、 \# -int、 \# int</span><span class="sxs-lookup"><span data-stu-id="fb40b-117">\#+int, \#-int, \#int</span></span> | <span data-ttu-id="fb40b-118"> (0-9) 驗證有效的數位字元。</span><span class="sxs-lookup"><span data-stu-id="fb40b-118">Validate for valid numeric characters (0-9).</span></span> <span data-ttu-id="fb40b-119">這裡允許屬性。</span><span class="sxs-lookup"><span data-stu-id="fb40b-119">Properties are allowed here.</span></span>     |



 

<span data-ttu-id="fb40b-120">要在登錄中輸入的整數值語法是整數， \# 其中整數是數值。</span><span class="sxs-lookup"><span data-stu-id="fb40b-120">The syntax for an integer value to be entered into the registry is \#integer where integer is numerical.</span></span>

## <a name="result"></a><span data-ttu-id="fb40b-121">結果</span><span class="sxs-lookup"><span data-stu-id="fb40b-121">Result</span></span>

<span data-ttu-id="fb40b-122">如果未正確指定登錄專案的整數值，ICE70 會報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="fb40b-122">ICE70 reports an error if integer values for registry entries are not specified correctly.</span></span>

## <a name="example"></a><span data-ttu-id="fb40b-123">範例</span><span class="sxs-lookup"><span data-stu-id="fb40b-123">Example</span></span>

<span data-ttu-id="fb40b-124">ICE70 會報告給定範例的下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="fb40b-124">ICE70 reports the following errors for the given example.</span></span>

``` syntax
The value #12xz34 is an invalid numeric value for registry entry Reg1. If you meant to use a string, then the string value entry must be preceded by ## not #.
```

<span data-ttu-id="fb40b-125">若要修正這個錯誤：若要將值設為數值，請將值變更為使用所有數位字元。</span><span class="sxs-lookup"><span data-stu-id="fb40b-125">To fix this error: If you want the value to be numeric, change the value to use all numeric characters.</span></span> <span data-ttu-id="fb40b-126">如果您想要將值設為字串，其前面必須有兩個 ' \# (\# \#) ，而不是只有一個。</span><span class="sxs-lookup"><span data-stu-id="fb40b-126">If you want the value to be a string, it must be preceded by two '\#' (\#\#) instead of just one.</span></span>

``` syntax
The value #xz34 is an invalid hexadecimal value for registry entry Reg2.
```

<span data-ttu-id="fb40b-127">若要修正這個錯誤：有效的十六進位字元是0-9、A-f 和 a-f。</span><span class="sxs-lookup"><span data-stu-id="fb40b-127">To fix this error: Valid hexadecimal characters are 0-9, A-F, and a-f.</span></span> <span data-ttu-id="fb40b-128">只有這些字元可以跟隨 \# x (或 \# x) 。</span><span class="sxs-lookup"><span data-stu-id="fb40b-128">Only these characters can follow the \#x (or \#X).</span></span>

<span data-ttu-id="fb40b-129">登錄[表](registry-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="fb40b-129">[Registry table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="fb40b-130">登錄</span><span class="sxs-lookup"><span data-stu-id="fb40b-130">Registry</span></span> | <span data-ttu-id="fb40b-131">值</span><span class="sxs-lookup"><span data-stu-id="fb40b-131">Value</span></span>    |
|----------|----------|
| <span data-ttu-id="fb40b-132">Reg1</span><span class="sxs-lookup"><span data-stu-id="fb40b-132">Reg1</span></span>     | <span data-ttu-id="fb40b-133">\#12xz34</span><span class="sxs-lookup"><span data-stu-id="fb40b-133">\#12xz34</span></span> |
| <span data-ttu-id="fb40b-134">Reg2</span><span class="sxs-lookup"><span data-stu-id="fb40b-134">Reg2</span></span>     | <span data-ttu-id="fb40b-135">\#xz34</span><span class="sxs-lookup"><span data-stu-id="fb40b-135">\#xz34</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="fb40b-136">備註</span><span class="sxs-lookup"><span data-stu-id="fb40b-136">Remarks</span></span>

-   <span data-ttu-id="fb40b-137">\#\[myproperty \] 是有效的。</span><span class="sxs-lookup"><span data-stu-id="fb40b-137">\#\[myproperty\] is valid.</span></span>
-   <span data-ttu-id="fb40b-138">\#\[myproperty 無效 (遺漏結尾括弧) 。</span><span class="sxs-lookup"><span data-stu-id="fb40b-138">\#\[myproperty is not valid (missing ending bracket).</span></span>
-   <span data-ttu-id="fb40b-139">\#\[myprop1 \] \[ myprop2 有效。</span><span class="sxs-lookup"><span data-stu-id="fb40b-139">\#\[myprop1\] \[myprop2 is valid.</span></span> <span data-ttu-id="fb40b-140"> (即使最後一個遺漏結尾的括弧，myprop1 仍會評估為 str， \# 如此您就會有 \# \# str \[ myprop2，這是有效的</span><span class="sxs-lookup"><span data-stu-id="fb40b-140">(Even though the last one is missing the ending bracket, myprop1 could evaluate to \#str so you would have \#\#str \[myprop2, which is valid</span></span>
-   <span data-ttu-id="fb40b-141">\#\]myproperty \[ 無效</span><span class="sxs-lookup"><span data-stu-id="fb40b-141">\#\]myproperty\[ is not valid</span></span>
-   <span data-ttu-id="fb40b-142">值字串中的任何內嵌屬性都不能是 \[ $compkey \] 、 \[ \# filekey \] 或 \[ ！ filekey \] 形式，因為它們不是數值。</span><span class="sxs-lookup"><span data-stu-id="fb40b-142">Any embedded property in a value string cannot be in \[$compkey\], \[\#filekey\], or \[!filekey\] form because these are not numeric.</span></span> <span data-ttu-id="fb40b-143">不過，有一個例外狀況， \# \[ myproperty \] \[ $compkey \] (或 \[ \# filekey \] 或 \[ ！ filekey \]) 有效，因為如同上述， \[ myproperty \] 可以評估為 \# str。</span><span class="sxs-lookup"><span data-stu-id="fb40b-143">However, there is one exception, \#\[myproperty\] \[$compkey\] (or \[\#filekey\] or \[!filekey\]) is valid because, as with the preceding, \[myproperty\] can evaluate to \#str.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb40b-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="fb40b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb40b-145">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="fb40b-145">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



