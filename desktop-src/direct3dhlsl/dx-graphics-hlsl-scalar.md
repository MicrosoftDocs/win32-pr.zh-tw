---
title: 純量類型
description: 純量類型
ms.assetid: bf24d27f-2720-4268-bc74-fc46afedb9aa
keywords:
- 純量類型 HLSL
topic_type:
- apiref
api_name:
- Scalar Types
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 7198932c6edb91e6f797b232b6c980976f3696a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "103696546"
---
# <a name="scalar-types"></a><span data-ttu-id="087c8-104">純量類型</span><span class="sxs-lookup"><span data-stu-id="087c8-104">Scalar Types</span></span>


<span data-ttu-id="087c8-105">HLSL 支援數個純量資料類型：</span><span class="sxs-lookup"><span data-stu-id="087c8-105">HLSL supports several scalar data types:</span></span>

-   <span data-ttu-id="087c8-106">**bool** -true 或 false。</span><span class="sxs-lookup"><span data-stu-id="087c8-106">**bool** - true or false.</span></span>
-   <span data-ttu-id="087c8-107">**int** -32-位帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="087c8-107">**int** - 32-bit signed integer.</span></span>
-   <span data-ttu-id="087c8-108">**uint** -32-bit 不帶正負號整數。</span><span class="sxs-lookup"><span data-stu-id="087c8-108">**uint** - 32-bit unsigned integer.</span></span>
-   <span data-ttu-id="087c8-109">**dword** -32-位不帶正負號整數。</span><span class="sxs-lookup"><span data-stu-id="087c8-109">**dword** - 32-bit unsigned integer.</span></span>
-   <span data-ttu-id="087c8-110">**半** 16 位浮點值。</span><span class="sxs-lookup"><span data-stu-id="087c8-110">**half** - 16-bit floating point value.</span></span> <span data-ttu-id="087c8-111">這種資料類型只提供語言相容性。</span><span class="sxs-lookup"><span data-stu-id="087c8-111">This data type is provided only for language compatibility.</span></span> <span data-ttu-id="087c8-112">Direct3D 10 著色器目標會將所有的半資料類型對應至 float 資料類型。</span><span class="sxs-lookup"><span data-stu-id="087c8-112">Direct3D 10 shader targets map all half data types to float data types.</span></span> <span data-ttu-id="087c8-113">如果) 需要這項功能，就不能在統一全域變數上使用半資料類型 (使用/Gec 旗標。</span><span class="sxs-lookup"><span data-stu-id="087c8-113">A half data type cannot be used on a uniform global variable (use the /Gec flag if this functionality is desired).</span></span>
-   <span data-ttu-id="087c8-114">**float** -32 位浮點值。</span><span class="sxs-lookup"><span data-stu-id="087c8-114">**float** - 32-bit floating point value.</span></span>
-   <span data-ttu-id="087c8-115">**雙** 64 位浮點值。</span><span class="sxs-lookup"><span data-stu-id="087c8-115">**double** - 64-bit floating point value.</span></span> <span data-ttu-id="087c8-116">您無法使用雙精確度值做為資料流程的輸入和輸出。</span><span class="sxs-lookup"><span data-stu-id="087c8-116">You cannot use double precision values as inputs and outputs for a stream.</span></span> <span data-ttu-id="087c8-117">若要在著色器之間傳遞雙精確度值，請將每個 **double** 宣告為一對 **uint** 資料類型。</span><span class="sxs-lookup"><span data-stu-id="087c8-117">To pass double precision values between shaders, declare each **double** as a pair of **uint** data types.</span></span> <span data-ttu-id="087c8-118">然後，使用 [**asuint**](asuint.md) 函式將每個 **雙** 精確度封裝到 **uint** 的配對，並使用 [**asdouble**](asdouble.md) 函式將一組 **uint** 重新包裝回 **雙精度浮點數**。</span><span class="sxs-lookup"><span data-stu-id="087c8-118">Then, use the [**asuint**](asuint.md) function to pack each **double** into the pair of **uint** s and the [**asdouble**](asdouble.md) function to unpack the pair of **uint** s back into the **double**.</span></span>

<span data-ttu-id="087c8-119">從 Windows 8 HLSL 開始也支援最小有效位數純量資料類型。</span><span class="sxs-lookup"><span data-stu-id="087c8-119">Starting with Windows 8 HLSL also supports minimum precision scalar data types.</span></span> <span data-ttu-id="087c8-120">圖形驅動程式可以使用大於或等於指定位精確度的精確度，來執行最小有效位數純量資料類型。</span><span class="sxs-lookup"><span data-stu-id="087c8-120">Graphics drivers can implement minimum precision scalar data types by using any precision greater than or equal to their specified bit precision.</span></span> <span data-ttu-id="087c8-121">建議您不要依賴相依于特定基礎精確度的固定或換行行為。</span><span class="sxs-lookup"><span data-stu-id="087c8-121">We recommend not to rely on clamping or wrapping behavior that depends on specific underlying precision.</span></span> <span data-ttu-id="087c8-122">例如，圖形驅動程式可能會以完整的32位有效位數執行 **min16float** 值的算數運算。</span><span class="sxs-lookup"><span data-stu-id="087c8-122">For example, the graphics driver might execute arithmetic on a **min16float** value at full 32-bit precision.</span></span>

-   <span data-ttu-id="087c8-123">**min16float** -最小16位浮點值。</span><span class="sxs-lookup"><span data-stu-id="087c8-123">**min16float** - minimum 16-bit floating point value.</span></span>
-   <span data-ttu-id="087c8-124">**min10float** -最小的10位浮點值。</span><span class="sxs-lookup"><span data-stu-id="087c8-124">**min10float** - minimum 10-bit floating point value.</span></span>
-   <span data-ttu-id="087c8-125">**min16int** -最小16位帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="087c8-125">**min16int** - minimum 16-bit signed integer.</span></span>
-   <span data-ttu-id="087c8-126">**min12int** -最小12位帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="087c8-126">**min12int** - minimum 12-bit signed integer.</span></span>
-   <span data-ttu-id="087c8-127">**min16uint** -最小16位不帶正負號整數。</span><span class="sxs-lookup"><span data-stu-id="087c8-127">**min16uint** - minimum 16-bit unsigned integer.</span></span>

<span data-ttu-id="087c8-128">如需純量常值的詳細資訊，請參閱 [文法](dx-graphics-hlsl-appendix-grammar.md)。</span><span class="sxs-lookup"><span data-stu-id="087c8-128">For more information about scalar literals, see [Grammar](dx-graphics-hlsl-appendix-grammar.md).</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="087c8-129">Direct3D 9 與 Direct3D 10 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="087c8-129">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="087c8-130">在 Direct3D 10 中，下列類型是 float 類型的修飾詞。</span><span class="sxs-lookup"><span data-stu-id="087c8-130">In Direct3D 10, the following types are modifiers to the float type.</span></span><br/>
<ul>
<li><span data-ttu-id="087c8-131"><strong>snorm 浮點數</strong> - IEEE 32 位帶正負號的標準化浮點數，範圍介於-1 到1（含）之間。</span><span class="sxs-lookup"><span data-stu-id="087c8-131"><strong>snorm float</strong> - IEEE 32-bit signed-normalized float in range -1 to 1 inclusive.</span></span></li>
<li><span data-ttu-id="087c8-132"><strong>unorm 浮點數</strong> - IEEE 32 位不帶正負號-在範圍0到1（含）的標準化浮點數。</span><span class="sxs-lookup"><span data-stu-id="087c8-132"><strong>unorm float</strong> - IEEE 32-bit unsigned-normalized float in range 0 to 1 inclusive.</span></span></li>
</ul>
<span data-ttu-id="087c8-133">例如，以下是4個元件的已簽署標準化浮點變數宣告。</span><span class="sxs-lookup"><span data-stu-id="087c8-133">For example, here is a 4-component signed-normalized float-variable declaration.</span></span><br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>snorm float4 fourComponentIEEEFloat;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 

## <a name="string-type"></a><span data-ttu-id="087c8-134">字串類型</span><span class="sxs-lookup"><span data-stu-id="087c8-134">String Type</span></span>

<span data-ttu-id="087c8-135">HLSL 也支援 **字串** 類型，也就是 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="087c8-135">HLSL also supports a **string** type, which is an ASCII string.</span></span> <span data-ttu-id="087c8-136">沒有可接受字串的作業或狀態，但效果可以查詢字串參數和批註。</span><span class="sxs-lookup"><span data-stu-id="087c8-136">There are no operations or states that accept strings, but effects can query string parameters and annotations.</span></span>

## <a name="example"></a><span data-ttu-id="087c8-137">範例</span><span class="sxs-lookup"><span data-stu-id="087c8-137">Example</span></span>

```c
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```

## <a name="see-also"></a><span data-ttu-id="087c8-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="087c8-138">See also</span></span>



* [<span data-ttu-id="087c8-139">宣告純量類型</span><span class="sxs-lookup"><span data-stu-id="087c8-139">Declaring Scalar Types</span></span>](./dx-graphics-hlsl-writing-shaders-9.md#declaring-shader-variables)
* [<span data-ttu-id="087c8-140"> (DirectX HLSL) 的資料類型 </span><span class="sxs-lookup"><span data-stu-id="087c8-140">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)