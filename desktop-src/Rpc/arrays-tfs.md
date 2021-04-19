---
title: " (RPC) 的陣列 (TFS) "
description: 遠端程序呼叫 (RPC) 陣列類別包含固定大小、符合標準、一致、變化、複雜。
ms.assetid: 7144ec87-90f2-463a-80e4-28cb4771325f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d564a2dfd838006be1667343b14a57bdaf4b07
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/05/2021
ms.locfileid: "106984919"
---
# <a name="arrays-rpc"></a><span data-ttu-id="b8654-103"> (RPC) 的陣列</span><span class="sxs-lookup"><span data-stu-id="b8654-103">Arrays (RPC)</span></span>

<span data-ttu-id="b8654-104">已根據其效能特性定義了數個數組類別，主要是是否可以封鎖複製陣列。</span><span class="sxs-lookup"><span data-stu-id="b8654-104">Several array categories have been defined based on their performance characteristics, primarily whether the array can be block-copied.</span></span>

<span data-ttu-id="b8654-105">某些類別（例如固定大小的陣列）有兩種類型的陣列描述元：它們是由前置 FC 權杖的名稱中的修正所表示。</span><span class="sxs-lookup"><span data-stu-id="b8654-105">For some categories, such as a fixed-size array, two types of array descriptors exist; they are indicated by an in-fix in the name of the leading FC token.</span></span>



| <span data-ttu-id="b8654-106">格式字元</span><span class="sxs-lookup"><span data-stu-id="b8654-106">Format character</span></span> | <span data-ttu-id="b8654-107">說明</span><span class="sxs-lookup"><span data-stu-id="b8654-107">Description</span></span>                                                           |
|------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="b8654-108">SM</span><span class="sxs-lookup"><span data-stu-id="b8654-108">SM</span></span>               | <span data-ttu-id="b8654-109">類型的總大小可以用16位不帶正負號的整數表示。</span><span class="sxs-lookup"><span data-stu-id="b8654-109">The type's total size can be represented in a 16-bit unsigned int.</span></span>    |
| <span data-ttu-id="b8654-110">LG</span><span class="sxs-lookup"><span data-stu-id="b8654-110">LG</span></span>               | <span data-ttu-id="b8654-111">類型的總大小需要以32位不帶正負號的長度來表示。</span><span class="sxs-lookup"><span data-stu-id="b8654-111">The type's total size needs a 32-bit unsigned long to be represented.</span></span> |



 

<span data-ttu-id="b8654-112">陣列通用的欄位：</span><span class="sxs-lookup"><span data-stu-id="b8654-112">Fields common to arrays:</span></span>

-   <span data-ttu-id="b8654-113">總 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="b8654-113">total\_size</span></span>

    <span data-ttu-id="b8654-114">記憶體中的陣列大小總計（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b8654-114">Total size of the array in memory, in bytes.</span></span> <span data-ttu-id="b8654-115">這與調整後的網路大小相同。</span><span class="sxs-lookup"><span data-stu-id="b8654-115">This is the same as wire size after alignment.</span></span> <span data-ttu-id="b8654-116">針對填補問題不存在且大小為實際陣列大小的類別，會計算總大小。</span><span class="sxs-lookup"><span data-stu-id="b8654-116">The total size is calculated for categories for which the padding issue does not exist and the size is actual array size.</span></span>

-   <span data-ttu-id="b8654-117">元素 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="b8654-117">element\_size</span></span>

    <span data-ttu-id="b8654-118">陣列單一元素的記憶體大小總計，包括填補 (只有) 複雜的陣列時，才會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="b8654-118">Total size in memory of a single element of the array, including padding (this may happen for complex arrays only).</span></span>

-   <span data-ttu-id="b8654-119">元素 \_ 描述</span><span class="sxs-lookup"><span data-stu-id="b8654-119">element\_description</span></span>

    <span data-ttu-id="b8654-120">陣列元素類型的描述。</span><span class="sxs-lookup"><span data-stu-id="b8654-120">Description of the array element type.</span></span>

-   <span data-ttu-id="b8654-121">指標 \_ 版面配置</span><span class="sxs-lookup"><span data-stu-id="b8654-121">pointer\_layout</span></span>

    <span data-ttu-id="b8654-122">如需詳細資訊，請參閱 [指標版面](pointer-layout-tfs.md) 配置主題。</span><span class="sxs-lookup"><span data-stu-id="b8654-122">See the [Pointer Layout](pointer-layout-tfs.md) topic for more information.</span></span>

## <a name="fixed-sized-arrays"></a><span data-ttu-id="b8654-123">固定大小的陣列</span><span class="sxs-lookup"><span data-stu-id="b8654-123">Fixed-sized Arrays</span></span>

<span data-ttu-id="b8654-124">針對具有已知大小的陣列產生固定大小的陣列格式字串，因此可能會被區塊複製到封送處理緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b8654-124">A fixed-sized array format string is generated for arrays that have a known size, and therefore may be block-copied to the marshaling buffer.</span></span> <span data-ttu-id="b8654-125">這兩個固定的陣列描述元格式如下所示。</span><span class="sxs-lookup"><span data-stu-id="b8654-125">The two fixed array descriptor formats are as follows.</span></span>

``` syntax
FC_SMFARRAY alignment<1> 
total_size<2> 
[pointer_layout<>]  
element_description<> 
FC_END
```

<span data-ttu-id="b8654-126">及</span><span class="sxs-lookup"><span data-stu-id="b8654-126">and</span></span>

``` syntax
FC_LGFARRAY alignment<1> 
total_size<4> 
[pointer_layout<>] 
element_description<> 
FC_END
```

## <a name="conformant-array"></a><span data-ttu-id="b8654-127">符合標準的陣列</span><span class="sxs-lookup"><span data-stu-id="b8654-127">Conformant Array</span></span>

<span data-ttu-id="b8654-128">一旦知道陣列的大小，就可以封鎖複製符合標準的陣列。</span><span class="sxs-lookup"><span data-stu-id="b8654-128">A conformant array can be block-copied once the size of the array is known.</span></span>

``` syntax
FC_CARRAY alignment<1>
element_size<2> 
conformance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END
```

<span data-ttu-id="b8654-129">一致性 \_ 描述<> 是相互關聯描述項，而且有4或6個位元組，視是否使用 [**/robust**](/windows/desktop/Midl/-robust) 而定。</span><span class="sxs-lookup"><span data-stu-id="b8654-129">The conformance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

## <a name="conformant-varying-array"></a><span data-ttu-id="b8654-130">一致的不同陣列</span><span class="sxs-lookup"><span data-stu-id="b8654-130">Conformant Varying Array</span></span>

<span data-ttu-id="b8654-131">也可以封鎖複製一致的不同陣列。</span><span class="sxs-lookup"><span data-stu-id="b8654-131">A conformant varying array can also be block-copied.</span></span>

``` syntax
FC_CVARRAY alignment<1> 
element_size<2> 
conformance_description<> 
variance_description<>  
[pointer_layout<>] 
element_description<> 
FC_END
```

<span data-ttu-id="b8654-132">一致性 \_ 描述<> 和差異 \_ 描述<> 是相互關聯描述項，而且有4或6個位元組，視是否使用 [**/robust**](/windows/desktop/Midl/-robust) 而定。</span><span class="sxs-lookup"><span data-stu-id="b8654-132">The conformance\_description<> and variance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

## <a name="varying-array"></a><span data-ttu-id="b8654-133">不同陣列</span><span class="sxs-lookup"><span data-stu-id="b8654-133">Varying Array</span></span>

<span data-ttu-id="b8654-134">不同的陣列有兩種可能性，視陣列的大小而定。</span><span class="sxs-lookup"><span data-stu-id="b8654-134">The varying arrays have two possibilities depending on the size of the array.</span></span>

``` syntax
FC_SMVARRAY alignment<1>
total_size<2>  
number_elements<2> 
element_size<2> 
variance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END

FC_LGVARRAY alignment<1>
total_size<4>  
number_elements<4> 
element_size<2> 
variance_description<4>
[pointer_layout<>] 
element_description<> 
FC_END
```

<span data-ttu-id="b8654-135">差異 \_ 描述<> 是相互關聯描述項，而且有4或6個位元組，視所使用的 [**/robust**](/windows/desktop/Midl/-robust) 而定。</span><span class="sxs-lookup"><span data-stu-id="b8654-135">The variance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on the [**/robust**](/windows/desktop/Midl/-robust) being used.</span></span>

<span data-ttu-id="b8654-136">針對內嵌于結構內的不同陣列，差異描述<2> 欄位的位移 \_<> 是從結構中不同陣列的位置到差異描述欄位的相對位移。</span><span class="sxs-lookup"><span data-stu-id="b8654-136">For varying arrays embedded inside of a structure, the offset<2> field of the variance\_description<> is a relative offset from the varying array's position in the structure to the variance describing field.</span></span> <span data-ttu-id="b8654-137">位移通常相對於結構的開頭。</span><span class="sxs-lookup"><span data-stu-id="b8654-137">The offset is typically relative to the beginning of the structure.</span></span>

## <a name="complex-arrays"></a><span data-ttu-id="b8654-138">複雜陣列</span><span class="sxs-lookup"><span data-stu-id="b8654-138">Complex Arrays</span></span>

<span data-ttu-id="b8654-139">複雜陣列是具有專案的任何陣列，可防止它被封鎖複製，因此需要採取其他動作。</span><span class="sxs-lookup"><span data-stu-id="b8654-139">A complex array is any array with an element that prevents it from being block-copied, and as such, additional action needs to be taken.</span></span> <span data-ttu-id="b8654-140">這些元素會讓陣列變得複雜：</span><span class="sxs-lookup"><span data-stu-id="b8654-140">These elements make an array complex:</span></span>

-   <span data-ttu-id="b8654-141">簡單類型： \_ \_ 在64位平臺上的 ENUM16、INT3264 (只能) 、具有 \[ [**範圍** 的整數](/windows/desktop/Midl/range)\]</span><span class="sxs-lookup"><span data-stu-id="b8654-141">simple types: ENUM16, \_\_INT3264 (on 64-bit platforms only), an integral with \[[**range**](/windows/desktop/Midl/range)\]</span></span>
-   <span data-ttu-id="b8654-142">參考和介面指標 (64 位平臺上的所有指標) </span><span class="sxs-lookup"><span data-stu-id="b8654-142">reference and interface pointers (all pointers on 64-bit platforms)</span></span>
-   <span data-ttu-id="b8654-143">等位</span><span class="sxs-lookup"><span data-stu-id="b8654-143">unions</span></span>
-   <span data-ttu-id="b8654-144">複雜結構 (如需結構複雜的原因清單，請參閱複雜結構描述主題) </span><span class="sxs-lookup"><span data-stu-id="b8654-144">complex structures (see the Complex Structure Description topic for a full list of reasons for a structure to be complex)</span></span>
-   <span data-ttu-id="b8654-145">以 \[ [**傳輸 \_ 為**](/windows/desktop/Midl/transmit-as) \] 、 \[ [**使用者 \_ 封送**](/windows/desktop/Midl/user-marshal)處理定義的元素\]</span><span class="sxs-lookup"><span data-stu-id="b8654-145">elements defined with \[[**transmit\_as**](/windows/desktop/Midl/transmit-as)\], \[[**user\_marshal**](/windows/desktop/Midl/user-marshal)\]</span></span>
-   <span data-ttu-id="b8654-146">無論基礎專案類型為何，所有具有至少一個符合和/或不同維度的多維陣列都是複雜的。</span><span class="sxs-lookup"><span data-stu-id="b8654-146">All multidimensional arrays with at least one conformant and/or varying dimension are complex regardless of the underlying element type.</span></span>

<span data-ttu-id="b8654-147">複雜的陣列描述如下所示：</span><span class="sxs-lookup"><span data-stu-id="b8654-147">The complex array description is as follows:</span></span>

``` syntax
FC_BOGUS_ARRAY alignment<1> 
number_of_elements<2> 
conformance_description<> 
variance_description<> 
element_description<> 
FC_END
```

<span data-ttu-id="b8654-148">\_ \_ 如果陣列一致，<2> 欄位的元素數目為零。</span><span class="sxs-lookup"><span data-stu-id="b8654-148">The number\_of\_elements<2> field is zero if the array is conformant.</span></span>

<span data-ttu-id="b8654-149">一致性 \_ 描述<> 和差異 \_ 描述<> 是相互關聯描述項，而且有4或6個位元組，視是否使用 [**/robust**](/windows/desktop/Midl/-robust) 而定。</span><span class="sxs-lookup"><span data-stu-id="b8654-149">The conformance\_description<> and variance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="b8654-150">如果陣列具有一致性和/或變異數，則一致性 \_ 描述<> 和/或變異 \_ 數描述<> 欄位 (s) 有有效的描述，否則，相互關聯描述項的前4個位元組會設定為0xffffffff。</span><span class="sxs-lookup"><span data-stu-id="b8654-150">If the array has conformance and/or variance then the conformance\_description<> and/or variance\_description<> field(s) have valid descriptions, otherwise the first 4 bytes of the correlation descriptor are set to 0xFFFFFFFF.</span></span> <span data-ttu-id="b8654-151">旗標（如果有的話）會設定為零。</span><span class="sxs-lookup"><span data-stu-id="b8654-151">The flags, when present, are set to zero.</span></span>

 

 
