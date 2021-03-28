---
title: 文法
description: HLSL 語句會使用下列文法規則來建立。
ms.assetid: 683248e9-6fc7-451a-906b-6e0aab1b0c8c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d2346e1ca2302f80c796558b4aa2bbdce016d494
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104507736"
---
# <a name="grammar"></a><span data-ttu-id="aed33-103">文法</span><span class="sxs-lookup"><span data-stu-id="aed33-103">Grammar</span></span>

<span data-ttu-id="aed33-104">HLSL 語句會使用下列文法規則來建立。</span><span class="sxs-lookup"><span data-stu-id="aed33-104">HLSL statements are constructed using the following rules for grammar.</span></span>

-   [<span data-ttu-id="aed33-105">空白</span><span class="sxs-lookup"><span data-stu-id="aed33-105">Whitespace</span></span>](#whitespace)
-   [<span data-ttu-id="aed33-106">浮點數</span><span class="sxs-lookup"><span data-stu-id="aed33-106">Floating point numbers</span></span>](#floating-point-numbers)
-   [<span data-ttu-id="aed33-107">整數數位</span><span class="sxs-lookup"><span data-stu-id="aed33-107">Integer numbers</span></span>](#integer-numbers)
-   [<span data-ttu-id="aed33-108">Characters</span><span class="sxs-lookup"><span data-stu-id="aed33-108">Characters</span></span>](#characters)
-   [<span data-ttu-id="aed33-109">字串</span><span class="sxs-lookup"><span data-stu-id="aed33-109">Strings</span></span>](#strings)
-   [<span data-ttu-id="aed33-110">識別碼</span><span class="sxs-lookup"><span data-stu-id="aed33-110">Identifiers</span></span>](#identifiers)
-   [<span data-ttu-id="aed33-111">運算子</span><span class="sxs-lookup"><span data-stu-id="aed33-111">Operators</span></span>](#operators)
-   [<span data-ttu-id="aed33-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="aed33-112">Related topics</span></span>](#related-topics)

## <a name="whitespace"></a><span data-ttu-id="aed33-113">空白</span><span class="sxs-lookup"><span data-stu-id="aed33-113">Whitespace</span></span>

<span data-ttu-id="aed33-114">下列字元會被辨識為空白字元。</span><span class="sxs-lookup"><span data-stu-id="aed33-114">The following characters are recognized as white space.</span></span>



|                            |
|----------------------------|
| <span data-ttu-id="aed33-115">SPACE</span><span class="sxs-lookup"><span data-stu-id="aed33-115">SPACE</span></span>                      |
| <span data-ttu-id="aed33-116">TAB</span><span class="sxs-lookup"><span data-stu-id="aed33-116">TAB</span></span>                        |
| <span data-ttu-id="aed33-117">Eol</span><span class="sxs-lookup"><span data-stu-id="aed33-117">EOL</span></span>                        |
| <span data-ttu-id="aed33-118">C 樣式批註 (/ \* \* /) </span><span class="sxs-lookup"><span data-stu-id="aed33-118">C style comments (/\* \*/)</span></span> |
| <span data-ttu-id="aed33-119">C + + 樣式批註 (//) </span><span class="sxs-lookup"><span data-stu-id="aed33-119">C++ style comments (//)</span></span>    |



 

## <a name="floating-point-numbers"></a><span data-ttu-id="aed33-120">浮點數</span><span class="sxs-lookup"><span data-stu-id="aed33-120">Floating point numbers</span></span>

<span data-ttu-id="aed33-121">浮點數會以 HLSL 表示，如下所示：</span><span class="sxs-lookup"><span data-stu-id="aed33-121">Floating point numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="aed33-122">小數常數指數-部分 (opt) 浮動尾碼 (opt) </span><span class="sxs-lookup"><span data-stu-id="aed33-122">fractional-constant exponent-part(opt) floating-suffix(opt)</span></span>

    <span data-ttu-id="aed33-123">數位序列指數-部分浮動尾碼 (opt) </span><span class="sxs-lookup"><span data-stu-id="aed33-123">digit-sequence exponent-part floating-suffix(opt)</span></span>

-   <span data-ttu-id="aed33-124">小數常數：</span><span class="sxs-lookup"><span data-stu-id="aed33-124">fractional-constant :</span></span>

    <span data-ttu-id="aed33-125">數位序列 (opt) 。</span><span class="sxs-lookup"><span data-stu-id="aed33-125">digit-sequence(opt) .</span></span> <span data-ttu-id="aed33-126">數位順序</span><span class="sxs-lookup"><span data-stu-id="aed33-126">digit-sequence</span></span>

    <span data-ttu-id="aed33-127">數位順序。</span><span class="sxs-lookup"><span data-stu-id="aed33-127">digit-sequence .</span></span>

-   <span data-ttu-id="aed33-128">指數-部分：</span><span class="sxs-lookup"><span data-stu-id="aed33-128">exponent-part :</span></span>

    <span data-ttu-id="aed33-129">e sign (opt) 數位順序</span><span class="sxs-lookup"><span data-stu-id="aed33-129">e sign(opt) digit-sequence</span></span>

    <span data-ttu-id="aed33-130">E sign (opt) 數位順序</span><span class="sxs-lookup"><span data-stu-id="aed33-130">E sign(opt) digit-sequence</span></span>

-   <span data-ttu-id="aed33-131">sign：下列其中一個</span><span class="sxs-lookup"><span data-stu-id="aed33-131">sign : one of</span></span>

    \+ -

-   <span data-ttu-id="aed33-132">數位順序：</span><span class="sxs-lookup"><span data-stu-id="aed33-132">digit-sequence :</span></span>

    <span data-ttu-id="aed33-133">digit</span><span class="sxs-lookup"><span data-stu-id="aed33-133">digit</span></span>

    <span data-ttu-id="aed33-134">digit-sequence digit</span><span class="sxs-lookup"><span data-stu-id="aed33-134">digit-sequence digit</span></span>

-   <span data-ttu-id="aed33-135">floating-suffix：下列其中一個</span><span class="sxs-lookup"><span data-stu-id="aed33-135">floating-suffix : one of</span></span>

    <span data-ttu-id="aed33-136">h H f F l L</span><span class="sxs-lookup"><span data-stu-id="aed33-136">h H f F l L</span></span>

    <span data-ttu-id="aed33-137">使用 "L" 尾碼來指定完整的64位有效位數浮點數常值。</span><span class="sxs-lookup"><span data-stu-id="aed33-137">Use the “L” suffix to specify a full 64-bit precision floating-point literal.</span></span> <span data-ttu-id="aed33-138">32位的 float 常值是預設值。</span><span class="sxs-lookup"><span data-stu-id="aed33-138">A 32-bit float literal is the default.</span></span>

    <span data-ttu-id="aed33-139">例如，編譯器會將下列常值識別為32位精確度浮點數常值，並忽略較低的位：</span><span class="sxs-lookup"><span data-stu-id="aed33-139">For example, the compiler recognizes the following literal value as a 32-bit precision floating-point literal and ignores the lower bits:</span></span>

    ```
    double x = -0.6473313946860445;
    ```

    

    <span data-ttu-id="aed33-140">編譯器會將下列常值辨識為64位精確度浮點數常值：</span><span class="sxs-lookup"><span data-stu-id="aed33-140">The compiler recognizes the following literal value as a 64-bit precision floating-point literal:</span></span>

    ```
    double x = -0.6473313946860445L;
    ```

    

## <a name="integer-numbers"></a><span data-ttu-id="aed33-141">整數數位</span><span class="sxs-lookup"><span data-stu-id="aed33-141">Integer numbers</span></span>

<span data-ttu-id="aed33-142">整數會以 HLSL 表示，如下所示：</span><span class="sxs-lookup"><span data-stu-id="aed33-142">Integer numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="aed33-143">整數常數整數-尾碼 (opt) </span><span class="sxs-lookup"><span data-stu-id="aed33-143">integer-constant integer-suffix(opt)</span></span>
-   <span data-ttu-id="aed33-144">整數常數：下列其中一個</span><span class="sxs-lookup"><span data-stu-id="aed33-144">integer-constant: one of</span></span>

    <span data-ttu-id="aed33-145">\# (十進位數) </span><span class="sxs-lookup"><span data-stu-id="aed33-145">\# (decimal number)</span></span>

    <span data-ttu-id="aed33-146">0 \# (八進位數位) </span><span class="sxs-lookup"><span data-stu-id="aed33-146">0\# (octal number)</span></span>

    <span data-ttu-id="aed33-147">0x \# (hex 數位) </span><span class="sxs-lookup"><span data-stu-id="aed33-147">0x\# (hex number)</span></span>

-   <span data-ttu-id="aed33-148">整數尾碼可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="aed33-148">integer-suffix can be any one of these:</span></span>

    <span data-ttu-id="aed33-149">u U l l</span><span class="sxs-lookup"><span data-stu-id="aed33-149">u U l L</span></span>

## <a name="characters"></a><span data-ttu-id="aed33-150">Characters</span><span class="sxs-lookup"><span data-stu-id="aed33-150">Characters</span></span>

<span data-ttu-id="aed33-151">字元會以 HLSL 表示，如下所示：</span><span class="sxs-lookup"><span data-stu-id="aed33-151">Characters are represented in HLSL as follows:</span></span>



|                                           |                                                                 |
|-------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="aed33-152">交流</span><span class="sxs-lookup"><span data-stu-id="aed33-152">'c'</span></span>                                       | <span data-ttu-id="aed33-153"> (字元) </span><span class="sxs-lookup"><span data-stu-id="aed33-153">(character)</span></span>                                                     |
| <span data-ttu-id="aed33-154">' \\ a ' ' \\ b ' ' \\ f ' ' \\ b ' ' \\ r ' ' \\ t ' ' \\ v '</span><span class="sxs-lookup"><span data-stu-id="aed33-154">'\\a' '\\b' '\\f' '\\b' '\\r' '\\t' '\\v'</span></span> | <span data-ttu-id="aed33-155"> (的 esc) </span><span class="sxs-lookup"><span data-stu-id="aed33-155">(escapes)</span></span>                                                       |
| <span data-ttu-id="aed33-156">'\\\#\#\#'</span><span class="sxs-lookup"><span data-stu-id="aed33-156">'\\\#\#\#'</span></span>                                | <span data-ttu-id="aed33-157"> (八進位 escape，每個 \# 都是八進位數位) </span><span class="sxs-lookup"><span data-stu-id="aed33-157">(octal escape, each \# is an octal digit)</span></span>                       |
| <span data-ttu-id="aed33-158">' \\ x \# '</span><span class="sxs-lookup"><span data-stu-id="aed33-158">'\\x\#'</span></span>                                   | <span data-ttu-id="aed33-159"> (hex escape， \# 是十六進位數位，任何數目的數位) </span><span class="sxs-lookup"><span data-stu-id="aed33-159">(hex escape, \# is hex number, any number of digits)</span></span>            |
| <span data-ttu-id="aed33-160">' \\ c '</span><span class="sxs-lookup"><span data-stu-id="aed33-160">'\\c'</span></span>                                     | <span data-ttu-id="aed33-161"> (c 是其他字元，包括反斜線和引號) </span><span class="sxs-lookup"><span data-stu-id="aed33-161">(c is other character, including backslash and quotation marks)</span></span> |



 

<span data-ttu-id="aed33-162">預處理器運算式中不支援 esc。</span><span class="sxs-lookup"><span data-stu-id="aed33-162">Escapes are not supported in preprocessor expressions.</span></span>

## <a name="strings"></a><span data-ttu-id="aed33-163">字串</span><span class="sxs-lookup"><span data-stu-id="aed33-163">Strings</span></span>

<span data-ttu-id="aed33-164">字串以 HLSL 表示，如下所示：</span><span class="sxs-lookup"><span data-stu-id="aed33-164">Strings are represented in HLSL as follows:</span></span>

<span data-ttu-id="aed33-165">"s" (s 是具有 esc) 的任何字串。</span><span class="sxs-lookup"><span data-stu-id="aed33-165">"s" (s is any string with escapes).</span></span>

## <a name="identifiers"></a><span data-ttu-id="aed33-166">識別碼</span><span class="sxs-lookup"><span data-stu-id="aed33-166">Identifiers</span></span>

<span data-ttu-id="aed33-167">識別碼會以 HLSL 表示，如下所示：</span><span class="sxs-lookup"><span data-stu-id="aed33-167">Identifiers are represented in HLSL as follows:</span></span>


```
    [A-Za-z_][A-Za-z0-9_]*
```



## <a name="operators"></a><span data-ttu-id="aed33-168">運算子</span><span class="sxs-lookup"><span data-stu-id="aed33-168">Operators</span></span>


```
##, #@, ++, --, &, &, &, ||, ==, ::, <<, <<=, >>, >>=, ..., 
<=, >=, !=, *=, /=, +=, -=, %=, &=, |=, ^=, ->
```



<span data-ttu-id="aed33-169">另外還有任何其他不符合其他規則的單一字元。</span><span class="sxs-lookup"><span data-stu-id="aed33-169">Also any other single character that did not match another rule.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aed33-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="aed33-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aed33-171">附錄 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="aed33-171">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




