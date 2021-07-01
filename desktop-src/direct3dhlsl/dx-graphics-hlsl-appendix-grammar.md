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
ms.openlocfilehash: b77f1050beaee2b269d12e69704018e3c5abee6e
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129846"
---
# <a name="grammar"></a><span data-ttu-id="5417b-103">文法</span><span class="sxs-lookup"><span data-stu-id="5417b-103">Grammar</span></span>

<span data-ttu-id="5417b-104">HLSL 語句會使用下列文法規則來建立。</span><span class="sxs-lookup"><span data-stu-id="5417b-104">HLSL statements are constructed using the following rules for grammar.</span></span>

-   [<span data-ttu-id="5417b-105">空白</span><span class="sxs-lookup"><span data-stu-id="5417b-105">Whitespace</span></span>](#whitespace)
-   [<span data-ttu-id="5417b-106">浮點數</span><span class="sxs-lookup"><span data-stu-id="5417b-106">Floating point numbers</span></span>](#floating-point-numbers)
-   [<span data-ttu-id="5417b-107">整數數字</span><span class="sxs-lookup"><span data-stu-id="5417b-107">Integer numbers</span></span>](#integer-numbers)
-   [<span data-ttu-id="5417b-108">Characters</span><span class="sxs-lookup"><span data-stu-id="5417b-108">Characters</span></span>](#characters)
-   [<span data-ttu-id="5417b-109">字串</span><span class="sxs-lookup"><span data-stu-id="5417b-109">Strings</span></span>](#strings)
-   [<span data-ttu-id="5417b-110">識別碼</span><span class="sxs-lookup"><span data-stu-id="5417b-110">Identifiers</span></span>](#identifiers)
-   [<span data-ttu-id="5417b-111">運算子</span><span class="sxs-lookup"><span data-stu-id="5417b-111">Operators</span></span>](#operators)
-   [<span data-ttu-id="5417b-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="5417b-112">Related topics</span></span>](#related-topics)

## <a name="whitespace"></a><span data-ttu-id="5417b-113">空白</span><span class="sxs-lookup"><span data-stu-id="5417b-113">Whitespace</span></span>

<span data-ttu-id="5417b-114">下列字元會被辨識為空白字元。</span><span class="sxs-lookup"><span data-stu-id="5417b-114">The following characters are recognized as white space.</span></span>

- <span data-ttu-id="5417b-115">SPACE</span><span class="sxs-lookup"><span data-stu-id="5417b-115">SPACE</span></span>
- <span data-ttu-id="5417b-116">TAB</span><span class="sxs-lookup"><span data-stu-id="5417b-116">TAB</span></span>
- <span data-ttu-id="5417b-117">Eol</span><span class="sxs-lookup"><span data-stu-id="5417b-117">EOL</span></span>
- <span data-ttu-id="5417b-118">C 樣式批註 (/ \* \* /) </span><span class="sxs-lookup"><span data-stu-id="5417b-118">C style comments (/\* \*/)</span></span>
- <span data-ttu-id="5417b-119">C + + 樣式批註 (//) </span><span class="sxs-lookup"><span data-stu-id="5417b-119">C++ style comments (//)</span></span>

## <a name="floating-point-numbers"></a><span data-ttu-id="5417b-120">浮點數</span><span class="sxs-lookup"><span data-stu-id="5417b-120">Floating point numbers</span></span>

<span data-ttu-id="5417b-121">浮點數會以 HLSL 表示，如下所示：</span><span class="sxs-lookup"><span data-stu-id="5417b-121">Floating point numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="5417b-122">小數常數指數-部分 (opt) 浮動尾碼 (opt) </span><span class="sxs-lookup"><span data-stu-id="5417b-122">fractional-constant exponent-part(opt) floating-suffix(opt)</span></span>

    <span data-ttu-id="5417b-123">數位序列指數-部分浮動尾碼 (opt) </span><span class="sxs-lookup"><span data-stu-id="5417b-123">digit-sequence exponent-part floating-suffix(opt)</span></span>

-   <span data-ttu-id="5417b-124">小數常數：</span><span class="sxs-lookup"><span data-stu-id="5417b-124">fractional-constant :</span></span>

    <span data-ttu-id="5417b-125">數位序列 (opt) 。</span><span class="sxs-lookup"><span data-stu-id="5417b-125">digit-sequence(opt) .</span></span> <span data-ttu-id="5417b-126">數位順序</span><span class="sxs-lookup"><span data-stu-id="5417b-126">digit-sequence</span></span>

    <span data-ttu-id="5417b-127">數位順序。</span><span class="sxs-lookup"><span data-stu-id="5417b-127">digit-sequence .</span></span>

-   <span data-ttu-id="5417b-128">指數-部分：</span><span class="sxs-lookup"><span data-stu-id="5417b-128">exponent-part :</span></span>

    <span data-ttu-id="5417b-129">e sign (opt) 數位順序</span><span class="sxs-lookup"><span data-stu-id="5417b-129">e sign(opt) digit-sequence</span></span>

    <span data-ttu-id="5417b-130">E sign (opt) 數位順序</span><span class="sxs-lookup"><span data-stu-id="5417b-130">E sign(opt) digit-sequence</span></span>

-   <span data-ttu-id="5417b-131">sign：下列其中一個</span><span class="sxs-lookup"><span data-stu-id="5417b-131">sign : one of</span></span>

    \+ -

-   <span data-ttu-id="5417b-132">數位順序：</span><span class="sxs-lookup"><span data-stu-id="5417b-132">digit-sequence :</span></span>

    <span data-ttu-id="5417b-133">digit</span><span class="sxs-lookup"><span data-stu-id="5417b-133">digit</span></span>

    <span data-ttu-id="5417b-134">digit-sequence digit</span><span class="sxs-lookup"><span data-stu-id="5417b-134">digit-sequence digit</span></span>

-   <span data-ttu-id="5417b-135">floating-suffix：下列其中一個</span><span class="sxs-lookup"><span data-stu-id="5417b-135">floating-suffix : one of</span></span>

    <span data-ttu-id="5417b-136">h H f F l L</span><span class="sxs-lookup"><span data-stu-id="5417b-136">h H f F l L</span></span>

    <span data-ttu-id="5417b-137">使用 "L" 尾碼來指定完整的64位有效位數浮點數常值。</span><span class="sxs-lookup"><span data-stu-id="5417b-137">Use the “L” suffix to specify a full 64-bit precision floating-point literal.</span></span> <span data-ttu-id="5417b-138">32位的 float 常值是預設值。</span><span class="sxs-lookup"><span data-stu-id="5417b-138">A 32-bit float literal is the default.</span></span>

    <span data-ttu-id="5417b-139">例如，編譯器會將下列常值識別為32位精確度浮點數常值，並忽略較低的位：</span><span class="sxs-lookup"><span data-stu-id="5417b-139">For example, the compiler recognizes the following literal value as a 32-bit precision floating-point literal and ignores the lower bits:</span></span>

    ```
    double x = -0.6473313946860445;
    ```

    

    <span data-ttu-id="5417b-140">編譯器會將下列常值辨識為64位精確度浮點數常值：</span><span class="sxs-lookup"><span data-stu-id="5417b-140">The compiler recognizes the following literal value as a 64-bit precision floating-point literal:</span></span>

    ```
    double x = -0.6473313946860445L;
    ```

    

## <a name="integer-numbers"></a><span data-ttu-id="5417b-141">整數數字</span><span class="sxs-lookup"><span data-stu-id="5417b-141">Integer numbers</span></span>

<span data-ttu-id="5417b-142">整數會以 HLSL 表示，如下所示：</span><span class="sxs-lookup"><span data-stu-id="5417b-142">Integer numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="5417b-143">整數常數整數-尾碼 (opt) </span><span class="sxs-lookup"><span data-stu-id="5417b-143">integer-constant integer-suffix(opt)</span></span>
-   <span data-ttu-id="5417b-144">整數常數：下列其中一個</span><span class="sxs-lookup"><span data-stu-id="5417b-144">integer-constant: one of</span></span>

    <span data-ttu-id="5417b-145">\# (十進位數) </span><span class="sxs-lookup"><span data-stu-id="5417b-145">\# (decimal number)</span></span>

    <span data-ttu-id="5417b-146">0 \# (八進位數位) </span><span class="sxs-lookup"><span data-stu-id="5417b-146">0\# (octal number)</span></span>

    <span data-ttu-id="5417b-147">0x \# (hex 數位) </span><span class="sxs-lookup"><span data-stu-id="5417b-147">0x\# (hex number)</span></span>

-   <span data-ttu-id="5417b-148">整數尾碼可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="5417b-148">integer-suffix can be any one of these:</span></span>

    <span data-ttu-id="5417b-149">u U l l</span><span class="sxs-lookup"><span data-stu-id="5417b-149">u U l L</span></span>

## <a name="characters"></a><span data-ttu-id="5417b-150">Characters</span><span class="sxs-lookup"><span data-stu-id="5417b-150">Characters</span></span>

<span data-ttu-id="5417b-151">字元會以 HLSL 表示，如下所示：</span><span class="sxs-lookup"><span data-stu-id="5417b-151">Characters are represented in HLSL as follows:</span></span>



| <span data-ttu-id="5417b-152">字元</span><span class="sxs-lookup"><span data-stu-id="5417b-152">Character</span></span>                                          | <span data-ttu-id="5417b-153">描述</span><span class="sxs-lookup"><span data-stu-id="5417b-153">Description</span></span>                                                                |
|-------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="5417b-154">交流</span><span class="sxs-lookup"><span data-stu-id="5417b-154">'c'</span></span>                                       | <span data-ttu-id="5417b-155"> (字元) </span><span class="sxs-lookup"><span data-stu-id="5417b-155">(character)</span></span>                                                     |
| <span data-ttu-id="5417b-156">' \\ a ' ' \\ b ' ' \\ f ' ' \\ b ' ' \\ r ' ' \\ t ' ' \\ v '</span><span class="sxs-lookup"><span data-stu-id="5417b-156">'\\a' '\\b' '\\f' '\\b' '\\r' '\\t' '\\v'</span></span> | <span data-ttu-id="5417b-157"> (的 esc) </span><span class="sxs-lookup"><span data-stu-id="5417b-157">(escapes)</span></span>                                                       |
| <span data-ttu-id="5417b-158">'\\\#\#\#'</span><span class="sxs-lookup"><span data-stu-id="5417b-158">'\\\#\#\#'</span></span>                                | <span data-ttu-id="5417b-159"> (八進位 escape，每個 \# 都是八進位數位) </span><span class="sxs-lookup"><span data-stu-id="5417b-159">(octal escape, each \# is an octal digit)</span></span>                       |
| <span data-ttu-id="5417b-160">' \\ x \# '</span><span class="sxs-lookup"><span data-stu-id="5417b-160">'\\x\#'</span></span>                                   | <span data-ttu-id="5417b-161"> (hex escape， \# 是十六進位數位，任何數目的數位) </span><span class="sxs-lookup"><span data-stu-id="5417b-161">(hex escape, \# is hex number, any number of digits)</span></span>            |
| <span data-ttu-id="5417b-162">' \\ c '</span><span class="sxs-lookup"><span data-stu-id="5417b-162">'\\c'</span></span>                                     | <span data-ttu-id="5417b-163"> (c 是其他字元，包括反斜線和引號) </span><span class="sxs-lookup"><span data-stu-id="5417b-163">(c is other character, including backslash and quotation marks)</span></span> |



 

<span data-ttu-id="5417b-164">預處理器運算式中不支援 esc。</span><span class="sxs-lookup"><span data-stu-id="5417b-164">Escapes are not supported in preprocessor expressions.</span></span>

## <a name="strings"></a><span data-ttu-id="5417b-165">字串</span><span class="sxs-lookup"><span data-stu-id="5417b-165">Strings</span></span>

<span data-ttu-id="5417b-166">字串以 HLSL 表示，如下所示：</span><span class="sxs-lookup"><span data-stu-id="5417b-166">Strings are represented in HLSL as follows:</span></span>

<span data-ttu-id="5417b-167">"s" (s 是具有 esc) 的任何字串。</span><span class="sxs-lookup"><span data-stu-id="5417b-167">"s" (s is any string with escapes).</span></span>

## <a name="identifiers"></a><span data-ttu-id="5417b-168">識別碼</span><span class="sxs-lookup"><span data-stu-id="5417b-168">Identifiers</span></span>

<span data-ttu-id="5417b-169">識別碼會以 HLSL 表示，如下所示：</span><span class="sxs-lookup"><span data-stu-id="5417b-169">Identifiers are represented in HLSL as follows:</span></span>


```
    [A-Za-z_][A-Za-z0-9_]*
```



## <a name="operators"></a><span data-ttu-id="5417b-170">運算子</span><span class="sxs-lookup"><span data-stu-id="5417b-170">Operators</span></span>


```
##, #@, ++, --, &, &, &, ||, ==, ::, <<, <<=, >>, >>=, ..., 
<=, >=, !=, *=, /=, +=, -=, %=, &=, |=, ^=, ->
```



<span data-ttu-id="5417b-171">另外還有任何其他不符合其他規則的單一字元。</span><span class="sxs-lookup"><span data-stu-id="5417b-171">Also any other single character that did not match another rule.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5417b-172">相關主題</span><span class="sxs-lookup"><span data-stu-id="5417b-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5417b-173">附錄 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5417b-173">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




