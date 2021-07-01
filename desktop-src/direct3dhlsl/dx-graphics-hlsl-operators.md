---
title: 操作員
description: 運算式是由運算子引起哈欠的變數和常值序列。
ms.assetid: c31aa0b8-1284-48aa-b000-d72433f0f5cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d7a44fe02983038658247fedaec7122f09306548
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119603"
---
# <a name="operators"></a><span data-ttu-id="9fb37-103">運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-103">Operators</span></span>

<span data-ttu-id="9fb37-104">運算式是由[運算子](dx-graphics-hlsl-statement-blocks.md)引起哈欠的[變數](dx-graphics-hlsl-variable-syntax.md)和常值序列。</span><span class="sxs-lookup"><span data-stu-id="9fb37-104">Expressions are sequences of [variables](dx-graphics-hlsl-variable-syntax.md) and literals punctuated by [operators](dx-graphics-hlsl-statement-blocks.md).</span></span> <span data-ttu-id="9fb37-105">運算子決定變數和常值如何合併、比較、選取等等。</span><span class="sxs-lookup"><span data-stu-id="9fb37-105">Operators determine how the variables and literals are combined, compared, selected, and so on.</span></span> <span data-ttu-id="9fb37-106">這些運算子包括：</span><span class="sxs-lookup"><span data-stu-id="9fb37-106">The operators include:</span></span>



| <span data-ttu-id="9fb37-107">操作員名稱</span><span class="sxs-lookup"><span data-stu-id="9fb37-107">Operator name</span></span>                                                                                | <span data-ttu-id="9fb37-108">運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-108">Operators</span></span>                                                                   |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="9fb37-109">加法和乘法運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-109">Additive and Multiplicative Operators</span></span>](#additive-and-multiplicative-operators) | <span data-ttu-id="9fb37-110">+, -, \*, /, %</span><span class="sxs-lookup"><span data-stu-id="9fb37-110">+, -, \*, /, %</span></span>                                                     |
| [<span data-ttu-id="9fb37-111">陣列運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-111">Array Operator</span></span>](#array-operator)                                               | <span data-ttu-id="9fb37-112">\[i\]</span><span class="sxs-lookup"><span data-stu-id="9fb37-112">\[i\]</span></span>                                                              |
| [<span data-ttu-id="9fb37-113">指派運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-113">Assignment Operators</span></span>](#assignment-operators)                                   | <span data-ttu-id="9fb37-114">=, +=, -=, \*=, /=, %=</span><span class="sxs-lookup"><span data-stu-id="9fb37-114">=, +=, -=, \*=, /=, %=</span></span>                                             |
| [<span data-ttu-id="9fb37-115">二進位轉換</span><span class="sxs-lookup"><span data-stu-id="9fb37-115">Binary Casts</span></span>](#binary-casts)                                                   | <span data-ttu-id="9fb37-116">適用于 float 和 int 的 c 規則、適用于 bool 的 C 規則或 HLSL 內建函式</span><span class="sxs-lookup"><span data-stu-id="9fb37-116">C rules for float and int, C rules or HLSL intrinsics for bool</span></span>     |
| [<span data-ttu-id="9fb37-117">位元運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-117">Bitwise Operators</span></span>](#bitwise-operators)                                         | <span data-ttu-id="9fb37-118">~、 <<、 >>、&、 \| 、^、 <<=、 >>=、&=、 \| =、^ =</span><span class="sxs-lookup"><span data-stu-id="9fb37-118">~, <<, >>, &, \|, ^, <<=, >>=, &=, \|=, ^=</span></span> |
| [<span data-ttu-id="9fb37-119">布耳運算運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-119">Boolean Math Operators</span></span>](#boolean-math-operators)                               | <span data-ttu-id="9fb37-120">& &、 \| \| 、？：</span><span class="sxs-lookup"><span data-stu-id="9fb37-120">& &, \|\|, ?:</span></span>                                                      |
| [<span data-ttu-id="9fb37-121">轉換運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-121">Cast Operator</span></span>](#cast-operator)                                                 | <span data-ttu-id="9fb37-122"> (類型) </span><span class="sxs-lookup"><span data-stu-id="9fb37-122">(type)</span></span>                                                             |
| [<span data-ttu-id="9fb37-123">逗點運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-123">Comma Operator</span></span>](#comma-operator)                                               | <span data-ttu-id="9fb37-124">,</span><span class="sxs-lookup"><span data-stu-id="9fb37-124">,</span></span>                                                                  |
| [<span data-ttu-id="9fb37-125">比較運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-125">Comparison Operators</span></span>](#comparison-operators)                                   | <span data-ttu-id="9fb37-126"><、>、= =、！ =、<=、>=</span><span class="sxs-lookup"><span data-stu-id="9fb37-126"><, >, ==, !=, <=, >=</span></span>                                   |
| [<span data-ttu-id="9fb37-127">前置或後置運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-127">Prefix or Postfix Operators</span></span>](#prefix-or-postfix-operators)                     | <span data-ttu-id="9fb37-128">++, --</span><span class="sxs-lookup"><span data-stu-id="9fb37-128">++, --</span></span>                                                             |
| [<span data-ttu-id="9fb37-129">Structure 運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-129">Structure Operator</span></span>](#structure-operator)                                       | <span data-ttu-id="9fb37-130">.</span><span class="sxs-lookup"><span data-stu-id="9fb37-130">.</span></span>                                                                  |
| [<span data-ttu-id="9fb37-131">一元運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-131">Unary Operators</span></span>](#unary-operators)                                             | <span data-ttu-id="9fb37-132">!, -, +</span><span class="sxs-lookup"><span data-stu-id="9fb37-132">!, -, +</span></span>                                                            |



 

<span data-ttu-id="9fb37-133">許多運算子都是每個元件，這表示會針對每個變數的每個元件獨立執行作業。</span><span class="sxs-lookup"><span data-stu-id="9fb37-133">Many of the operators are per-component, which means that the operation is performed independently for each component of each variable.</span></span> <span data-ttu-id="9fb37-134">例如，單一元件變數已執行一項作業。</span><span class="sxs-lookup"><span data-stu-id="9fb37-134">For example, a single component variable has one operation performed.</span></span> <span data-ttu-id="9fb37-135">另一方面，四個元件的變數有四個執行的作業，每個元件各一個。</span><span class="sxs-lookup"><span data-stu-id="9fb37-135">On the other hand, a four-component variable has four operations performed, one for each component.</span></span>

<span data-ttu-id="9fb37-136">對值執行某些動作的所有運算子（例如 + 和 \* ）都會依元件運作。</span><span class="sxs-lookup"><span data-stu-id="9fb37-136">All of the operators that do something to the value, such as + and \*, work per component.</span></span>

<span data-ttu-id="9fb37-137">除非您使用 [**all**](dx-graphics-hlsl-all.md) 或 [**any**](dx-graphics-hlsl-any.md) 內建函式搭配多重元件變數，否則比較運算子需要單一元件才能運作。</span><span class="sxs-lookup"><span data-stu-id="9fb37-137">The comparison operators require a single component to work unless you use the [**all**](dx-graphics-hlsl-all.md) or [**any**](dx-graphics-hlsl-any.md) intrinsic function with a multiple-component variable.</span></span> <span data-ttu-id="9fb37-138">下列作業會失敗，因為 if 語句需要單一 bool，但卻收到 bool4：</span><span class="sxs-lookup"><span data-stu-id="9fb37-138">The following operation fails because the if statement requires a single bool but receives a bool4:</span></span>


```
if (A4 < B4)
```



<span data-ttu-id="9fb37-139">下列作業會成功：</span><span class="sxs-lookup"><span data-stu-id="9fb37-139">The following operations succeed:</span></span>


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



<span data-ttu-id="9fb37-140">二元轉換運算子會針對每個元件 [**asfloat**](dx-graphics-hlsl-asfloat.md)、 [**asint**](dx-graphics-hlsl-asint.md)等工作，但會記載其特殊規則的 [**asdouble**](asdouble.md) 除外。</span><span class="sxs-lookup"><span data-stu-id="9fb37-140">The binary cast operators [**asfloat**](dx-graphics-hlsl-asfloat.md), [**asint**](dx-graphics-hlsl-asint.md), and so on work per component except for [**asdouble**](asdouble.md) whose special rules are documented.</span></span>

<span data-ttu-id="9fb37-141">點、逗號和陣列括弧等選取運算子無法針對每個元件運作。</span><span class="sxs-lookup"><span data-stu-id="9fb37-141">Selection operators like period, comma, and array brackets do not work per component.</span></span>

<span data-ttu-id="9fb37-142">轉換運算子會變更元件的數目。</span><span class="sxs-lookup"><span data-stu-id="9fb37-142">Cast operators change the number of components.</span></span> <span data-ttu-id="9fb37-143">下列轉換作業顯示其相等：</span><span class="sxs-lookup"><span data-stu-id="9fb37-143">The following cast operations show their equivalence:</span></span>


```
(float) i4 ->   float(i4.x)
(float4)i ->   float4(i, i, i, i)
```



## <a name="additive-and-multiplicative-operators"></a><span data-ttu-id="9fb37-144">加法和乘法運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-144">Additive and Multiplicative Operators</span></span>

<span data-ttu-id="9fb37-145">加法和乘法運算子為： +、-、 \* 、/、%</span><span class="sxs-lookup"><span data-stu-id="9fb37-145">The additive and multiplicative operators are: +, -, \*, /, %</span></span>


```
int i1 = 1;
int i2 = 2;
int i3 = i1 + i2;  // i3 = 3
i3 = i1 * i2;        // i3 = 1 * 2 = 2
```




```
i3 = i1/i2;       // i3 = 1/3 = 0.333. Truncated to 0 because i3 is an integer.
i3 = i2/i1;       // i3 = 2/1 = 2
```




```
float f1 = 1.0;
float f2 = 2.0f;
float f3 = f1 - f2; // f3 = 1.0 - 2.0 = -1.0
f3 = f1 * f2;         // f3 = 1.0 * 2.0 = 2.0
```




```
f3 = f1/f2;        // f3 = 1.0/2.0 = 0.5
f3 = f2/f1;        // f3 = 2.0/1.0 = 2.0
```



<span data-ttu-id="9fb37-146">模數運算子會傳回除法的餘數。</span><span class="sxs-lookup"><span data-stu-id="9fb37-146">The modulus operator returns the remainder of a division.</span></span> <span data-ttu-id="9fb37-147">使用整數和浮點數時，會產生不同的結果。</span><span class="sxs-lookup"><span data-stu-id="9fb37-147">This produces different results when using integers and floating-point numbers.</span></span> <span data-ttu-id="9fb37-148">小數的整數餘數將會被截斷。</span><span class="sxs-lookup"><span data-stu-id="9fb37-148">Integer remainders that are fractional will be truncated.</span></span>


```
int i1 = 1;
int i2 = 2;
i3 = i1 % i2;      // i3 = remainder of 1/2, which is 1
i3 = i2 % i1;      // i3 = remainder of 2/1, which is 0
i3 = 5 % 2;        // i3 = remainder of 5/2, which is 1
i3 = 9 % 2;        // i3 = remainder of 9/2, which is 1
```



<span data-ttu-id="9fb37-149">使用整數時，模數運算子會截斷小數餘數。</span><span class="sxs-lookup"><span data-stu-id="9fb37-149">The modulus operator truncates a fractional remainder when using integers.</span></span>


```
f3 = f1 % f2;      // f3 = remainder of 1.0/2.0, which is 0.5
f3 = f2 % f1;      // f3 = remainder of 2.0/1.0, which is 0.0
```



<span data-ttu-id="9fb37-150">只有當兩個邊都是正數或兩邊都是負數時，才會定義% 運算子。</span><span class="sxs-lookup"><span data-stu-id="9fb37-150">The % operator is defined only in cases where either both sides are positive or both sides are negative.</span></span> <span data-ttu-id="9fb37-151">與 C 不同的是，它也會針對浮點數資料類型以及整數來運作。</span><span class="sxs-lookup"><span data-stu-id="9fb37-151">Unlike C, it also operates on floating-point data types, as well as integers.</span></span>

## <a name="array-operator"></a><span data-ttu-id="9fb37-152">陣列運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-152">Array Operator</span></span>

<span data-ttu-id="9fb37-153">陣列成員選取運算子 " \[ i \] " 選取陣列中的一或多個元件。</span><span class="sxs-lookup"><span data-stu-id="9fb37-153">The array member selection operator "\[i\]" selects one or more components in an array.</span></span> <span data-ttu-id="9fb37-154">它是一組包含以零為基底之索引的方括弧。</span><span class="sxs-lookup"><span data-stu-id="9fb37-154">It is a set of square brackets that contain a zero-based index.</span></span>


```
int arrayOfInts[4] = { 0,1,2,3 };
arrayOfInts[0] = 2;
arrayOfInts[1] = arrayOfInts[0];
```



<span data-ttu-id="9fb37-155">Array 運算子也可以用來存取 vector。</span><span class="sxs-lookup"><span data-stu-id="9fb37-155">The array operator can also be used to access a vector.</span></span>


```
float4 4D_Vector = { 0.0f, 1.0f, 2.0f, 3.0f  };         
float 1DFloat = 4D_Vector[1];          // 1.0f
```



<span data-ttu-id="9fb37-156">藉由加入額外的索引，陣列運算子也可以存取矩陣。</span><span class="sxs-lookup"><span data-stu-id="9fb37-156">By adding an additional index, the array operator can also access a matrix.</span></span>


```
float4x4 mat4x4 = {{0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} };
mat4x4[0][1] = 1.1f;
float 1DFloat = mat4x4[0][1];      // 0.0f
```



<span data-ttu-id="9fb37-157">第一個索引是以零為基礎的資料列索引。</span><span class="sxs-lookup"><span data-stu-id="9fb37-157">The first index is the zero-based row index.</span></span> <span data-ttu-id="9fb37-158">第二個索引是以零為基底的資料行索引。</span><span class="sxs-lookup"><span data-stu-id="9fb37-158">The second index is the zero-based column index.</span></span>

## <a name="assignment-operators"></a><span data-ttu-id="9fb37-159">指派運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-159">Assignment Operators</span></span>

<span data-ttu-id="9fb37-160">指派運算子為： =、+ =、-=、 \* =、/=</span><span class="sxs-lookup"><span data-stu-id="9fb37-160">The assignment operators are: =, +=, -=, \*=, /=</span></span>

<span data-ttu-id="9fb37-161">變數可以指派常值：</span><span class="sxs-lookup"><span data-stu-id="9fb37-161">Variables can be assigned literal values:</span></span>


```
int i = 1;            
float f2 = 3.1f; 
bool b = false;
string str = "string";
```



<span data-ttu-id="9fb37-162">您也可以將數學運算的結果指派給變數：</span><span class="sxs-lookup"><span data-stu-id="9fb37-162">Variables can also be assigned the result of a mathematical operation:</span></span>


```
int i1 = 1;
i1 += 2;           // i1 = 1 + 2 = 3
```



<span data-ttu-id="9fb37-163">變數可以在等號的任一邊使用：</span><span class="sxs-lookup"><span data-stu-id="9fb37-163">A variable can be used on either side of the equals sign:</span></span>


```
float f3 = 0.5f;
f3 *= f3;          // f3 = 0.5 * 0.5 = 0.25
```



<span data-ttu-id="9fb37-164">浮點數變數的除法是預期的，因為 decimal 餘數不是問題。</span><span class="sxs-lookup"><span data-stu-id="9fb37-164">Division for floating-point variables is as expected because decimal remainders are not a problem.</span></span>


```
float f1 = 1.0;
f1 /= 3.0f;        // f1 = 1.0/3.0 = 0.333
```



<span data-ttu-id="9fb37-165">如果您使用的整數可能會被整除，特別是當截斷影響結果時，請務必小心。</span><span class="sxs-lookup"><span data-stu-id="9fb37-165">Be careful if you are using integers that may get divided, especially when truncation affects the result.</span></span> <span data-ttu-id="9fb37-166">這個範例與上一個範例相同，但資料類型除外。</span><span class="sxs-lookup"><span data-stu-id="9fb37-166">This example is identical to the previous example, except for the data type.</span></span> <span data-ttu-id="9fb37-167">截斷會產生非常不同的結果。</span><span class="sxs-lookup"><span data-stu-id="9fb37-167">The truncation causes a very different result.</span></span>


```
int i1 = 1;
i1 /= 3;           // i1 = 1/3 = 0.333, which gets truncated to 0
```



## <a name="binary-casts"></a><span data-ttu-id="9fb37-168">二進位轉換</span><span class="sxs-lookup"><span data-stu-id="9fb37-168">Binary Casts</span></span>

<span data-ttu-id="9fb37-169">Int 和 float 之間的轉換運算會將數值轉換成 C 規則之後的適當標記法，以截斷 int 型別。</span><span class="sxs-lookup"><span data-stu-id="9fb37-169">Casting operation between int and float will convert the numeric value into the appropriate representations following C rules for truncating an int type.</span></span> <span data-ttu-id="9fb37-170">將值從 float 轉換成 int，再轉換回浮點數，將會根據目標的有效位數來產生失真轉換。</span><span class="sxs-lookup"><span data-stu-id="9fb37-170">Casting a value from a float to an int and back to a float will result in a lossy conversion based on the precision of the target.</span></span>

<span data-ttu-id="9fb37-171">二進位轉換也可以使用 [**內建函式 (DIRECTX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)來執行，這會將數位的位標記法重新解譯到目標資料類型。</span><span class="sxs-lookup"><span data-stu-id="9fb37-171">Binary casts may also be performed using [**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md), which reinterpret the bit representation of a number into the target data type.</span></span>


```
asfloat() // Cast to float
asint()   // Cast to int 
asuint()  // Cast to uint
```



## <a name="bitwise-operators"></a><span data-ttu-id="9fb37-172">位元運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-172">Bitwise Operators</span></span>

<span data-ttu-id="9fb37-173">HLSL 支援下列位運算子，其遵循與 C 相關的優先順序，與其他運算子有關。</span><span class="sxs-lookup"><span data-stu-id="9fb37-173">HLSL supports the following bitwise operators, which follow the same precedence as C with regard to other operators.</span></span> <span data-ttu-id="9fb37-174">下表描述這些運算子。</span><span class="sxs-lookup"><span data-stu-id="9fb37-174">The following table describes the operators.</span></span>

> [!Note]  
> <span data-ttu-id="9fb37-175">位運算子需要具有 Direct3D 10 和更高硬體的 [著色器模型 4 \_ 0](dx-graphics-hlsl-sm4.md) 。</span><span class="sxs-lookup"><span data-stu-id="9fb37-175">Bitwise operators require [Shader Model 4\_0](dx-graphics-hlsl-sm4.md) with Direct3D 10 and higher hardware.</span></span>

 



| <span data-ttu-id="9fb37-176">運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-176">Operator</span></span>          |  <span data-ttu-id="9fb37-177">函式</span><span class="sxs-lookup"><span data-stu-id="9fb37-177">Function</span></span>                 |
|-----------|-------------------|
| ~         | <span data-ttu-id="9fb37-178">邏輯 Not</span><span class="sxs-lookup"><span data-stu-id="9fb37-178">Logical Not</span></span>       |
| <<  | <span data-ttu-id="9fb37-179">左移</span><span class="sxs-lookup"><span data-stu-id="9fb37-179">Left Shift</span></span>        |
| >>  | <span data-ttu-id="9fb37-180">右移</span><span class="sxs-lookup"><span data-stu-id="9fb37-180">Right Shift</span></span>       |
| &         | <span data-ttu-id="9fb37-181">邏輯 And</span><span class="sxs-lookup"><span data-stu-id="9fb37-181">Logical And</span></span>       |
| \|        | <span data-ttu-id="9fb37-182">邏輯 Or</span><span class="sxs-lookup"><span data-stu-id="9fb37-182">Logical Or</span></span>        |
| ^         | <span data-ttu-id="9fb37-183">邏輯 Xor</span><span class="sxs-lookup"><span data-stu-id="9fb37-183">Logical Xor</span></span>       |
| <<= | <span data-ttu-id="9fb37-184">左移等於</span><span class="sxs-lookup"><span data-stu-id="9fb37-184">Left Shift Equal</span></span>  |
| >>= | <span data-ttu-id="9fb37-185">右 Shift 等於</span><span class="sxs-lookup"><span data-stu-id="9fb37-185">Right Shift Equal</span></span> |
| &=        | <span data-ttu-id="9fb37-186">和相等</span><span class="sxs-lookup"><span data-stu-id="9fb37-186">And Equal</span></span>         |
| \|=       | <span data-ttu-id="9fb37-187">或等於</span><span class="sxs-lookup"><span data-stu-id="9fb37-187">Or Equal</span></span>          |
| ^=        | <span data-ttu-id="9fb37-188">Xor 等於</span><span class="sxs-lookup"><span data-stu-id="9fb37-188">Xor Equal</span></span>         |



 

<span data-ttu-id="9fb37-189">位運算子定義為只在 int 和 uint 資料類型上運作。</span><span class="sxs-lookup"><span data-stu-id="9fb37-189">Bitwise operators are defined to operate only on int and uint data types.</span></span> <span data-ttu-id="9fb37-190">嘗試在 float 或 struct 資料類型上使用位運算子將會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="9fb37-190">Attempting to use bitwise operators on float, or struct data types will result in an error.</span></span>

## <a name="boolean-math-operators"></a><span data-ttu-id="9fb37-191">布耳運算運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-191">Boolean Math Operators</span></span>

<span data-ttu-id="9fb37-192">布林數學運算子為：  &&、 \| \| 、？：</span><span class="sxs-lookup"><span data-stu-id="9fb37-192">The Boolean math operators are: &&, \|\|, ?:</span></span>


```
bool b1 = true;
bool b2 = false;
bool b3 = b1 && b2 // b3 = true AND false = false
b3 = b1 || b2                // b3 = true OR false = true
```



<span data-ttu-id="9fb37-193">與 C 的 &&、和？：的短路評估不同的 \| \| 是，HLSL 運算式永遠不會將評估短路，因為它們是向量作業。</span><span class="sxs-lookup"><span data-stu-id="9fb37-193">Unlike short-circuit evaluation of &&, \|\|, and ?: in C, HLSL expressions never short-circuit an evaluation because they are vector operations.</span></span> <span data-ttu-id="9fb37-194">一律會評估運算式的所有兩側。</span><span class="sxs-lookup"><span data-stu-id="9fb37-194">All sides of the expression are always evaluated.</span></span>

<span data-ttu-id="9fb37-195">布林運算子會以每個元件為基礎運作。</span><span class="sxs-lookup"><span data-stu-id="9fb37-195">Boolean operators function on a per-component basis.</span></span> <span data-ttu-id="9fb37-196">這表示，如果您比較兩個向量，則結果會是包含每個元件比較之布林結果的向量。</span><span class="sxs-lookup"><span data-stu-id="9fb37-196">This means that if you compare two vectors, the result is a vector containing the Boolean result of the comparison for each component.</span></span>

<span data-ttu-id="9fb37-197">針對使用布林運算子的運算式，每個變數的大小和元件類型都會在作業發生之前升級為相同的。</span><span class="sxs-lookup"><span data-stu-id="9fb37-197">For expressions that use Boolean operators, the size and component type of each variable are promoted to be the same before the operation occurs.</span></span> <span data-ttu-id="9fb37-198">升級型別會決定作業的解決方式，以及運算式的結果型別。</span><span class="sxs-lookup"><span data-stu-id="9fb37-198">The promoted type determines the resolution at which the operation takes place, as well as the result type of the expression.</span></span> <span data-ttu-id="9fb37-199">例如，int3 + float 運算式會升級為 float3 + float3 進行評估，而其結果會是 float3 類型。</span><span class="sxs-lookup"><span data-stu-id="9fb37-199">For example an int3 + float expression would be promoted to float3 + float3 for evaluation, and its result would be of type float3.</span></span>

## <a name="cast-operator"></a><span data-ttu-id="9fb37-200">轉換運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-200">Cast Operator</span></span>

<span data-ttu-id="9fb37-201">前面加上括弧中類型名稱的運算式是明確的類型轉換。</span><span class="sxs-lookup"><span data-stu-id="9fb37-201">An expression preceded by a type name in parenthesis is an explicit type cast.</span></span> <span data-ttu-id="9fb37-202">類型轉換會將原始運算式轉換成轉換的資料類型。</span><span class="sxs-lookup"><span data-stu-id="9fb37-202">A type cast converts the original expression to the data type of the cast.</span></span> <span data-ttu-id="9fb37-203">一般情況下，單一資料型別可以轉換成更複雜的資料類型 (有提升轉換) ，但是只有一些複雜的資料類型可以轉換成簡單的資料類型 (並) 降級轉換。</span><span class="sxs-lookup"><span data-stu-id="9fb37-203">In general, the simple data types can be cast to the more complex data types (with a promotion cast), but only some complex data types can be cast into simple data types (with a demotion cast).</span></span>

<span data-ttu-id="9fb37-204">只有右手邊型別轉換是合法的。</span><span class="sxs-lookup"><span data-stu-id="9fb37-204">Only right hand side type casting is legal.</span></span> <span data-ttu-id="9fb37-205">例如，的運算式 `(int)myFloat = myInt;` 不合法。</span><span class="sxs-lookup"><span data-stu-id="9fb37-205">For example, expressions such as `(int)myFloat = myInt;` are illegal.</span></span> <span data-ttu-id="9fb37-206">請改用 `myFloat = (float)myInt;`。</span><span class="sxs-lookup"><span data-stu-id="9fb37-206">Use `myFloat = (float)myInt;` instead.</span></span>

<span data-ttu-id="9fb37-207">編譯器也會執行隱含類型轉換。</span><span class="sxs-lookup"><span data-stu-id="9fb37-207">The compiler also performs implicit type cast.</span></span> <span data-ttu-id="9fb37-208">例如，下列兩個運算式是相等的：</span><span class="sxs-lookup"><span data-stu-id="9fb37-208">For example, the following two expressions are equivalent:</span></span>


```
int2 b = int2(1,2) + 2;
int2 b = int2(1,2) + int2(2,2);
```



## <a name="comma-operator"></a><span data-ttu-id="9fb37-209">逗點運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-209">Comma Operator</span></span>

<span data-ttu-id="9fb37-210">逗號運算子 (，) 分隔一或多個要依順序評估的運算式。</span><span class="sxs-lookup"><span data-stu-id="9fb37-210">The comma operator (,) separates one or more expressions that are to be evaluated in order.</span></span> <span data-ttu-id="9fb37-211">順序中最後一個運算式的值會用來做為序列的值。</span><span class="sxs-lookup"><span data-stu-id="9fb37-211">The value of the last expression in the sequence is used as the value of the sequence.</span></span>

<span data-ttu-id="9fb37-212">以下是值得注意的一個案例。</span><span class="sxs-lookup"><span data-stu-id="9fb37-212">Here is one case worth calling attention to.</span></span> <span data-ttu-id="9fb37-213">如果不小心將 [函式類型] 保留在等號右邊，右邊就會包含四個運算式，並以三個逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="9fb37-213">If the constructor type is accidentally left off the right side of the equals sign, the right side now contains four expressions, separated by three commas.</span></span>


```
// Instead of using a constructor
float4 x = float4(0,0,0,1); 

// The type on the right side is accidentally left off
float4 x = (0,0,0,1); 
```



<span data-ttu-id="9fb37-214">逗號運算子會從左至右評估運算式。</span><span class="sxs-lookup"><span data-stu-id="9fb37-214">The comma operator evaluates an expression from left to right.</span></span> <span data-ttu-id="9fb37-215">這樣可以減少右手邊：</span><span class="sxs-lookup"><span data-stu-id="9fb37-215">This reduces the right hand side to:</span></span>


```
float4 x = 1; 
```



<span data-ttu-id="9fb37-216">在此情況下，HLSL 會使用純量升階，因此其結果就像撰寫如下所示：</span><span class="sxs-lookup"><span data-stu-id="9fb37-216">HLSL uses scalar promotion in this case, so the result is as if this were written as follows:</span></span>


```
float4 x = float4(1,1,1,1);
```



<span data-ttu-id="9fb37-217">在此情況下，從右邊離開 float4 類型可能會造成編譯器無法偵測到的錯誤，因為這是有效的語句。</span><span class="sxs-lookup"><span data-stu-id="9fb37-217">In this instance, leaving off the float4 type from the right side is probably a mistake that the compiler is unable to detect because this is a valid statement.</span></span>

## <a name="comparison-operators"></a><span data-ttu-id="9fb37-218">比較運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-218">Comparison Operators</span></span>

<span data-ttu-id="9fb37-219">比較運算子為： <、>、= =、！ =、<=、>=。</span><span class="sxs-lookup"><span data-stu-id="9fb37-219">The comparison operators are: <, >, ==, !=, <=, >=.</span></span>

<span data-ttu-id="9fb37-220">比較大於 (或小於) 任何純量值的值：</span><span class="sxs-lookup"><span data-stu-id="9fb37-220">Compare values that are greater than (or less than) any scalar value:</span></span>


```
if( dot(lightDirection, normalVector) > 0 )
   // Do something; the face is lit
```




```
if( dot(lightDirection, normalVector) < 0 )
   // Do nothing; the face is backwards
```



<span data-ttu-id="9fb37-221">或者，比較等於 (或不等於) 任何純量值的值：</span><span class="sxs-lookup"><span data-stu-id="9fb37-221">Or, compare values equal to (or not equal to) any scalar value:</span></span>


```
if(color.a == 0)
   // Skip processing because the face is invisible

if(color.a != 0)
   // Blend two colors together using the alpha value
```



<span data-ttu-id="9fb37-222">或結合和比較大於或等於 (或小於或等於) 任何純量值的值：</span><span class="sxs-lookup"><span data-stu-id="9fb37-222">Or combine both and compare values that are greater than or equal to (or less than or equal to) any scalar value:</span></span>


```
if( position.z >= oldPosition.z )
   // Skip the new face because it is behind the existing face
```




```
if( currentValue <= someInitialCondition )
   // Reset the current value to its initial condition
```



<span data-ttu-id="9fb37-223">您可以使用任何純量資料類型來完成這些比較。</span><span class="sxs-lookup"><span data-stu-id="9fb37-223">Each of these comparisons can be done with any scalar data type.</span></span>

<span data-ttu-id="9fb37-224">若要搭配向量和矩陣類型使用比較運算子，請使用 [**all**](dx-graphics-hlsl-all.md) 或 [**any**](dx-graphics-hlsl-any.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="9fb37-224">To use comparison operators with vector and matrix types, use the [**all**](dx-graphics-hlsl-all.md) or [**any**](dx-graphics-hlsl-any.md) intrinsic function.</span></span>

<span data-ttu-id="9fb37-225">因為 if 語句需要單一 bool 但收到 bool4，所以此作業會失敗：</span><span class="sxs-lookup"><span data-stu-id="9fb37-225">This operation fails because the if statement requires a single bool but receives a bool4:</span></span>


```
if (A4 < B4)
```



<span data-ttu-id="9fb37-226">這些作業會成功：</span><span class="sxs-lookup"><span data-stu-id="9fb37-226">These operations succeed:</span></span>


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



## <a name="prefix-or-postfix-operators"></a><span data-ttu-id="9fb37-227">前置或後置運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-227">Prefix or Postfix Operators</span></span>

<span data-ttu-id="9fb37-228">前置詞和後置運算子為： + +、--。</span><span class="sxs-lookup"><span data-stu-id="9fb37-228">The prefix and postfix operators are: ++, --.</span></span> <span data-ttu-id="9fb37-229">前置運算子會在評估運算式之前變更變數的內容。</span><span class="sxs-lookup"><span data-stu-id="9fb37-229">Prefix operators change the contents of the variable before the expression is evaluated.</span></span> <span data-ttu-id="9fb37-230">後置運算子會在評估運算式之後變更變數的內容。</span><span class="sxs-lookup"><span data-stu-id="9fb37-230">Postfix operators change the contents of the variable after the expression is evaluated.</span></span>

<span data-ttu-id="9fb37-231">在此情況下，迴圈會使用我的內容來追蹤迴圈計數。</span><span class="sxs-lookup"><span data-stu-id="9fb37-231">In this case, a loop uses the contents of i to keep track of the loop count.</span></span>


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[i++] *= 2; 
}
```



<span data-ttu-id="9fb37-232">因為使用後置遞增運算子 (+ +) ，所以在 \[ 遞增之前，arrayOfFloats i \] 乘以2。</span><span class="sxs-lookup"><span data-stu-id="9fb37-232">Because the postfix increment operator (++) is used, arrayOfFloats\[i\] is multiplied by 2 before i is incremented.</span></span> <span data-ttu-id="9fb37-233">這可能會稍微重新排列以使用前置遞增運算子。</span><span class="sxs-lookup"><span data-stu-id="9fb37-233">This could be slightly rearranged to use the prefix increment operator.</span></span> <span data-ttu-id="9fb37-234">雖然這兩個範例都相等，但這種情況很難閱讀。</span><span class="sxs-lookup"><span data-stu-id="9fb37-234">This one is harder to read, although both examples are equivalent.</span></span>


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[++i - 1] *= 2; 
}
```



<span data-ttu-id="9fb37-235">因為使用前置運算子 (+ +) ，所以在 \[ 遞增之後，arrayOfFloats i + 1-1 \] 會乘以2。</span><span class="sxs-lookup"><span data-stu-id="9fb37-235">Because the prefix operator (++) is used, arrayOfFloats\[i+1 - 1\] is multiplied by 2 after i is incremented.</span></span>

<span data-ttu-id="9fb37-236">前置遞減和後置遞減運算子 (--) 會以與遞增運算子相同的順序套用。</span><span class="sxs-lookup"><span data-stu-id="9fb37-236">The prefix decrement and postfix decrement operator (--) are applied in the same sequence as the increment operator.</span></span> <span data-ttu-id="9fb37-237">不同之處在于遞減減去1，而不是加1。</span><span class="sxs-lookup"><span data-stu-id="9fb37-237">The difference is that decrement subtracts 1 instead of adding 1.</span></span>

## <a name="structure-operator"></a><span data-ttu-id="9fb37-238">Structure 運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-238">Structure Operator</span></span>

<span data-ttu-id="9fb37-239">結構成員選取運算子 (。 ) 是句號。</span><span class="sxs-lookup"><span data-stu-id="9fb37-239">The structure member selection operator (.) is a period.</span></span> <span data-ttu-id="9fb37-240">指定此結構：</span><span class="sxs-lookup"><span data-stu-id="9fb37-240">Given this structure:</span></span>


```
struct position
{
float4 x;
float4 y;
float4 z;
};
```



<span data-ttu-id="9fb37-241">您可以如下所示讀取：</span><span class="sxs-lookup"><span data-stu-id="9fb37-241">It can be read like this:</span></span>


```
struct position pos = { 1,2,3 };

float 1D_Float = pos.x
1D_Float = pos.y
```



<span data-ttu-id="9fb37-242">每個成員都可以使用 structure 運算子來讀取或寫入：</span><span class="sxs-lookup"><span data-stu-id="9fb37-242">Each member can be read or written with the structure operator:</span></span>


```
struct position pos = { 1,2,3 };
pos.x = 2.0f;
pos.z = 1.0f;       // z = 1.0f
pos.z = pos.x      // z = 2.0f
```



## <a name="unary-operators"></a><span data-ttu-id="9fb37-243">一元運算子</span><span class="sxs-lookup"><span data-stu-id="9fb37-243">Unary Operators</span></span>

<span data-ttu-id="9fb37-244">一元運算子為：!,-, +</span><span class="sxs-lookup"><span data-stu-id="9fb37-244">The unary operators are: !, -, +</span></span>

<span data-ttu-id="9fb37-245">一元運算子在單一運算元上運作。</span><span class="sxs-lookup"><span data-stu-id="9fb37-245">Unary operators operate on a single operand.</span></span>


```
bool b = false;
bool b2 = !b;      // b2 = true
int i = 2;
int i2 = -i;       // i2 = -2
int j = +i2;       // j = +2
```



## <a name="operator-precedence"></a><span data-ttu-id="9fb37-246">運算子優先順序</span><span class="sxs-lookup"><span data-stu-id="9fb37-246">Operator Precedence</span></span>

<span data-ttu-id="9fb37-247">當運算式包含一個以上的運算子時，運算子優先順序會決定評估的順序。</span><span class="sxs-lookup"><span data-stu-id="9fb37-247">When an expression contains more than one operator, operator precedence determines the order of evaluation.</span></span> <span data-ttu-id="9fb37-248">HLSL 的運算子優先順序遵循與 C 相同的優先順序。</span><span class="sxs-lookup"><span data-stu-id="9fb37-248">Operator precedence for HLSL follows the same precedence as C.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fb37-249">備註</span><span class="sxs-lookup"><span data-stu-id="9fb37-249">Remarks</span></span>

<span data-ttu-id="9fb37-250">大括弧 ({,}) 開始和結束語句區塊。</span><span class="sxs-lookup"><span data-stu-id="9fb37-250">Curly braces ({,}) start and end a statement block.</span></span> <span data-ttu-id="9fb37-251">當語句區塊使用單一語句時，大括弧是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="9fb37-251">When a statement block uses a single statement, the curly braces are optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fb37-252">相關主題</span><span class="sxs-lookup"><span data-stu-id="9fb37-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fb37-253"> (DirectX HLSL) 的語句 </span><span class="sxs-lookup"><span data-stu-id="9fb37-253">Statements (DirectX HLSL)</span></span>](dx-graphics-hlsl-statements.md)
</dt> </dl>

 

 




