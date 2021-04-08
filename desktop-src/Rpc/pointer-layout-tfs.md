---
title: 指標版面配置
description: 指標版面配置描述結構或陣列的指標。
ms.assetid: 1a4984c1-97b9-4e95-a17e-851b67fa94a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f26a6639b0c4b56c911be1e688995aaf3fb9d2d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840523"
---
# <a name="pointer-layout"></a><span data-ttu-id="38c70-103">指標版面配置</span><span class="sxs-lookup"><span data-stu-id="38c70-103">Pointer Layout</span></span>

<span data-ttu-id="38c70-104">指標版面配置描述結構或陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="38c70-104">Pointer layout describes pointers of a structure or an array.</span></span>

## <a name="pointer_layout"></a><span data-ttu-id="38c70-105">指標 \_ 版面配置<></span><span class="sxs-lookup"><span data-stu-id="38c70-105">pointer\_layout<></span></span>

<span data-ttu-id="38c70-106">指標 \_ 版面配置<> 欄位包含格式化字元 FC \_ PP fc \_ 板，後面接著一或多個指標描述（如稍後所述），並以 FC \_ 結束格式字元終止：</span><span class="sxs-lookup"><span data-stu-id="38c70-106">A pointer\_layout<> field consists of the format characters FC\_PP FC\_PAD followed by one or more pointer descriptions, as described later, and terminating with an FC\_END format character:</span></span>

``` syntax
FC_PP
FC_PAD
{ pointer_instance_layout<> }*
FC_END
```

<span data-ttu-id="38c70-107">指標 \_ 實例配置 \_<> 欄位是一種格式字串，描述指標的單一或多個實例。</span><span class="sxs-lookup"><span data-stu-id="38c70-107">A pointer\_instance\_layout<> field is a format string describing single or multiple instances of pointers.</span></span> <span data-ttu-id="38c70-108">下欄欄位適用于這些描述項：</span><span class="sxs-lookup"><span data-stu-id="38c70-108">The following fields are used in these descriptors:</span></span>

-   <span data-ttu-id="38c70-109">\_記憶體中的位移 \_</span><span class="sxs-lookup"><span data-stu-id="38c70-109">offset\_in\_memory</span></span>

    <span data-ttu-id="38c70-110">指標在記憶體中位置的帶正負號位移。</span><span class="sxs-lookup"><span data-stu-id="38c70-110">The signed offset to the pointer's location in memory.</span></span> <span data-ttu-id="38c70-111">針對位於結構中的指標，此位移是結構結尾的負位移， (符合標準結構的 nonconformant 部分結尾) ;如果是陣列，則位移是從陣列的開頭算起。</span><span class="sxs-lookup"><span data-stu-id="38c70-111">For a pointer residing in a structure, this offset is a negative offset from the end of the structure (the end of the nonconformant portion of conformant structures); for arrays, the offset is from the beginning of the array.</span></span>

-   <span data-ttu-id="38c70-112">\_緩衝區中的位移 \_</span><span class="sxs-lookup"><span data-stu-id="38c70-112">offset\_in\_buffer</span></span>

    <span data-ttu-id="38c70-113">緩衝區中指標位置的帶正負號位移。</span><span class="sxs-lookup"><span data-stu-id="38c70-113">The signed offset to the pointer's location in the buffer.</span></span> <span data-ttu-id="38c70-114">針對位於結構中的指標，此位移是從結構結尾算起的負位移， (符合標準結構的 nonconformant 部分結尾) ：若為數組，則位移是從陣列的開頭算起。</span><span class="sxs-lookup"><span data-stu-id="38c70-114">For a pointer residing in a structure, this offset is a negative offset from the end of the structure (the end of the nonconformant portion of conformant structures): for arrays, the offset is from the beginning of the array.</span></span>

-   <span data-ttu-id="38c70-115">\_陣列的 \_ 位移</span><span class="sxs-lookup"><span data-stu-id="38c70-115">offset\_to\_array</span></span>

    <span data-ttu-id="38c70-116">從封閉結構到要處理其指標的內嵌陣列之間的位移。</span><span class="sxs-lookup"><span data-stu-id="38c70-116">Offset from an enclosing structure to the embedded array whose pointers are being handled.</span></span> <span data-ttu-id="38c70-117">若為最上層陣列，此欄位永遠為零。</span><span class="sxs-lookup"><span data-stu-id="38c70-117">For top-level arrays, this field will always be zero.</span></span>

-   <span data-ttu-id="38c70-118">反覆運算</span><span class="sxs-lookup"><span data-stu-id="38c70-118">iterations</span></span>

    <span data-ttu-id="38c70-119"><> 描述具有相同配置的指標總數。</span><span class="sxs-lookup"><span data-stu-id="38c70-119">Total number of pointers that have the same layout<> described.</span></span>

-   <span data-ttu-id="38c70-120">increment</span><span class="sxs-lookup"><span data-stu-id="38c70-120">increment</span></span>

    <span data-ttu-id="38c70-121">重複期間連續指標之間的遞增。</span><span class="sxs-lookup"><span data-stu-id="38c70-121">Increment between successive pointers during a REPEAT.</span></span>

-   <span data-ttu-id="38c70-122">\_指標數目 \_</span><span class="sxs-lookup"><span data-stu-id="38c70-122">number\_of\_pointers</span></span>

    <span data-ttu-id="38c70-123">重複實例中的不同指標數目。</span><span class="sxs-lookup"><span data-stu-id="38c70-123">Number of different pointers in a repeat instance.</span></span>

-   <span data-ttu-id="38c70-124">指標 \_ 描述</span><span class="sxs-lookup"><span data-stu-id="38c70-124">pointer\_description</span></span>

    <span data-ttu-id="38c70-125">指標描述。</span><span class="sxs-lookup"><span data-stu-id="38c70-125">Pointer description.</span></span>

<span data-ttu-id="38c70-126">所有指標實例配置都會使用下列 \_<8> 的單一指標實例：</span><span class="sxs-lookup"><span data-stu-id="38c70-126">All pointer instance layouts use the following single pointer\_instance<8>:</span></span>

``` syntax
offset_to_pointer_in_memory<2> 
offset_to_pointer_in_buffer<2> 
pointer_description<4>
```

<span data-ttu-id="38c70-127">以下是實例描述項：</span><span class="sxs-lookup"><span data-stu-id="38c70-127">The following are instance descriptors:</span></span>

<span data-ttu-id="38c70-128">**簡單類型之指標的單一實例：**</span><span class="sxs-lookup"><span data-stu-id="38c70-128">**Single instance of a pointer to a simple type:**</span></span>

``` syntax
FC_NO_REPEAT FC_PAD 
pointer_instance<8>
```

<span data-ttu-id="38c70-129">**固定的重複指標：**</span><span class="sxs-lookup"><span data-stu-id="38c70-129">**Fixed repeat pointer:**</span></span>

``` syntax
FC_FIXED_REPEAT FC_PAD 
iterations<2> 
increment<2> 
offset_to_array<2> 
number_of_pointers<2>
{ pointer_instance<8> }*
```

<span data-ttu-id="38c70-130">**變數重複指標：**</span><span class="sxs-lookup"><span data-stu-id="38c70-130">**Variable repeat pointer:**</span></span>

``` syntax
FC_VARIABLE_REPEAT (FC_FIXED_OFFSET | FC_VARIABLE_OFFSET) 
increment<2> 
offset_to_array<2> 
number_of_pointers<2> 
{ pointer_instance<8> }*
```

<span data-ttu-id="38c70-131">針對固定的重複和變數重複指標實例，重複實例中的每個指標都有一組位移和指標描述。</span><span class="sxs-lookup"><span data-stu-id="38c70-131">For fixed repeat and variable repeat pointer instances there is a set of offset and pointer descriptions for each pointer in the repeat instance.</span></span>

## <a name="pointers-layout-design-issues"></a><span data-ttu-id="38c70-132">指標版面配置設計問題</span><span class="sxs-lookup"><span data-stu-id="38c70-132">Pointers Layout Design Issues</span></span>

<span data-ttu-id="38c70-133">本節說明與處理一致結構和內嵌指標相關的問題。</span><span class="sxs-lookup"><span data-stu-id="38c70-133">This section addresses issues related to processing conformant structures and embedded pointers.</span></span> <span data-ttu-id="38c70-134">問題是編譯器會針對具有某些冗余的結構和陣列產生指標版面配置。</span><span class="sxs-lookup"><span data-stu-id="38c70-134">The issue is that the compiler generates pointer layouts for structures and arrays with some redundancy.</span></span> <span data-ttu-id="38c70-135">這項功能很有説明，因為這項資訊很有用，因此，符合標準的結構可以引導一個指標配置，以提供來自結構的所有指標，以及符合標準之結構的標準陣列。</span><span class="sxs-lookup"><span data-stu-id="38c70-135">This is beneficial, because the information is useful and as such, for example, a conformant structure can walk one pointer layout to service all the pointers from the structure and from the conformant array being part of the conformant structure.</span></span> <span data-ttu-id="38c70-136">不過，有一些內嵌的情況需要 NDR 引擎執行額外的工作，以適當的連續處理所有指標版面配置，並剛好處理每個指標一次。</span><span class="sxs-lookup"><span data-stu-id="38c70-136">However, some embedded situations exist that require the NDR engine to perform additional work to process all the pointer layouts in the proper sequence, processing each pointer exactly once.</span></span>

## <a name="what-the-compiler-generates"></a><span data-ttu-id="38c70-137">編譯器產生的內容</span><span class="sxs-lookup"><span data-stu-id="38c70-137">What the Compiler Generates</span></span>

<span data-ttu-id="38c70-138">本節中討論的每個物件都有指標，因此，符合標準的結構在結構部分以及陣列元素中都具有指標。</span><span class="sxs-lookup"><span data-stu-id="38c70-138">Every object discussed in this section has pointers, so for example, a conformant structure has pointers in the structure part as well as in the array elements.</span></span> <span data-ttu-id="38c70-139">元素是具有指標的簡單結構。</span><span class="sxs-lookup"><span data-stu-id="38c70-139">The element is a simple structure with a pointer.</span></span>

1.  <span data-ttu-id="38c70-140">符合標準的結構，單一層級</span><span class="sxs-lookup"><span data-stu-id="38c70-140">Conformant structure, single level</span></span>

    <span data-ttu-id="38c70-141">符合的描述項具有 PP 部分，其中所有指標都會從結構和陣列描述。</span><span class="sxs-lookup"><span data-stu-id="38c70-141">The conformant descriptor has a PP part where all the pointers are described, both from the structure and from the array.</span></span> <span data-ttu-id="38c70-142">成員清單有 FC \_ 長的長度，而不是指標。</span><span class="sxs-lookup"><span data-stu-id="38c70-142">The member list has FC\_LONG in lieu of a pointer.</span></span> <span data-ttu-id="38c70-143">CARRAY 陣列描述項具有使用內嵌複雜的元素 \_ ，而且完全沒有指標描述項。</span><span class="sxs-lookup"><span data-stu-id="38c70-143">The CARRAY array descriptor has elements through the use of an embedded\_complex and no pointer descriptors at all.</span></span> <span data-ttu-id="38c70-144">元素仍有其單一指標描述元。</span><span class="sxs-lookup"><span data-stu-id="38c70-144">The element still has its single pointer descriptor.</span></span> <span data-ttu-id="38c70-145">指標配置優先于符合結構和簡單結構描述項中的成員配置。</span><span class="sxs-lookup"><span data-stu-id="38c70-145">Pointer layout precedes the member layout in a conformant structure and simple structure descriptors.</span></span>

2.  <span data-ttu-id="38c70-146">符合標準的結構，兩個或更多層級</span><span class="sxs-lookup"><span data-stu-id="38c70-146">Conformant structure, two or more levels</span></span>

    <span data-ttu-id="38c70-147">PP 描述具有來自所有層級的指標。</span><span class="sxs-lookup"><span data-stu-id="38c70-147">The PP description has pointers from all levels.</span></span> <span data-ttu-id="38c70-148">它會重複使用與內部一致結構相同的陣列描述。</span><span class="sxs-lookup"><span data-stu-id="38c70-148">It reuses the same array description as the internal conformant structure.</span></span> <span data-ttu-id="38c70-149">成員清單有 FC \_ 長的長度，而不是指標。</span><span class="sxs-lookup"><span data-stu-id="38c70-149">The member list has FC\_LONG in lieu of a pointer.</span></span> <span data-ttu-id="38c70-150">內嵌的結構是透過使用內嵌複雜的。</span><span class="sxs-lookup"><span data-stu-id="38c70-150">An embedded structure comes through the use of an embedded complex.</span></span> <span data-ttu-id="38c70-151">符合標準的結構描述項會依原樣重複使用。</span><span class="sxs-lookup"><span data-stu-id="38c70-151">The conformant structure descriptor is reused as-is.</span></span> <span data-ttu-id="38c70-152">結構的一般部分大小也是完整的，這表示最上層結構大小會包含內嵌結構的一般大小。</span><span class="sxs-lookup"><span data-stu-id="38c70-152">The size of the flat portion of the structure comes out complete as well, meaning that the top-level structure size would include embedded structure's flat size.</span></span>

3.  <span data-ttu-id="38c70-153">複雜結構，單一層級</span><span class="sxs-lookup"><span data-stu-id="38c70-153">Complex structure, single level</span></span>

    <span data-ttu-id="38c70-154">指標成員是以 FC \_ 指標標記。</span><span class="sxs-lookup"><span data-stu-id="38c70-154">Pointer members are marked by FC\_POINTER.</span></span> <span data-ttu-id="38c70-155">已簡化指標配置，因此清單中每個 FC 指標專案的指標描述項 (4 個位元組) \_ 。</span><span class="sxs-lookup"><span data-stu-id="38c70-155">Pointer layout is simplified such that there is a pointer descriptor (4 bytes) for each FC\_POINTER entry on the list.</span></span> <span data-ttu-id="38c70-156">指標配置會與成員逐步進行平行處理，也就是說，FC \_ 指標會導致下一個指標描述的處理。</span><span class="sxs-lookup"><span data-stu-id="38c70-156">Pointer layout is walked in parallel with a member walk, that is, an FC\_POINTER causes the next pointer description to be processed.</span></span> <span data-ttu-id="38c70-157">CARRAY 陣列具有指標配置，其中包含陣列的所有描述元，然後是使用內嵌複雜專案的元素。</span><span class="sxs-lookup"><span data-stu-id="38c70-157">The CARRAY array has pointer layout with all the descriptors of the array, and then element, through the use of an embedded complex.</span></span> <span data-ttu-id="38c70-158">元素描述項會重複使用。</span><span class="sxs-lookup"><span data-stu-id="38c70-158">The element descriptor is reused.</span></span> <span data-ttu-id="38c70-159">結構的平面部分大小已完成;換句話說，最上層結構的平面大小包含內嵌結構的一般大小。</span><span class="sxs-lookup"><span data-stu-id="38c70-159">The size of the flat portion of the structure comes out complete; in other words, the top-level structure's flat size includes the embedded structure's flat size.</span></span> <span data-ttu-id="38c70-160">成員配置優先于複雜結構的指標版面配置。</span><span class="sxs-lookup"><span data-stu-id="38c70-160">The member layout precedes the pointer layout for complex structures.</span></span>

    <span data-ttu-id="38c70-161">因此，符合標準的陣列描述會根據其是符合結構的陣列，還是在複雜結構內，而產生差異。</span><span class="sxs-lookup"><span data-stu-id="38c70-161">Hence, the conformant array description generation is different depending on whether it is an array inside of a conformant structure or inside a complex structure.</span></span>

4.  <span data-ttu-id="38c70-162">複雜結構、2個以上的層級、複雜的複雜</span><span class="sxs-lookup"><span data-stu-id="38c70-162">Complex structure, 2 or more levels, complex in complex</span></span>

    <span data-ttu-id="38c70-163">最上層複雜結構具有其成員指標，內嵌複雜結構具有其成員指標。</span><span class="sxs-lookup"><span data-stu-id="38c70-163">Top-level complex structure has its member pointers, embedded complex structure has its member pointers.</span></span> <span data-ttu-id="38c70-164">一致的結構描述項會重複使用。</span><span class="sxs-lookup"><span data-stu-id="38c70-164">The conformant structure descriptor is reused.</span></span> <span data-ttu-id="38c70-165">頂端的陣列描述項是內嵌結構中重複使用的陣列。</span><span class="sxs-lookup"><span data-stu-id="38c70-165">The array descriptor from the top is the reused array from the embedded structure.</span></span>

5.  <span data-ttu-id="38c70-166">具有內嵌一致結構的複雜結構</span><span class="sxs-lookup"><span data-stu-id="38c70-166">Complex structure with an embedded conformant structure</span></span>

    <span data-ttu-id="38c70-167">Top = 符合層級的結構具有其成員指標。</span><span class="sxs-lookup"><span data-stu-id="38c70-167">Top=level conformant structure has its member pointers.</span></span> <span data-ttu-id="38c70-168">符合標準的結構描述項會依原樣重複使用。</span><span class="sxs-lookup"><span data-stu-id="38c70-168">The conformant structure descriptor is reused as-is.</span></span> <span data-ttu-id="38c70-169">陣列描述元會從內嵌一致的結構重複使用;換句話說，它沒有陣列描述項的任何指標。</span><span class="sxs-lookup"><span data-stu-id="38c70-169">The array descriptor is reused from the embedded conformant structure; in other words, it does not have any pointers at the array descriptor.</span></span> <span data-ttu-id="38c70-170">元素有其指標描述元。</span><span class="sxs-lookup"><span data-stu-id="38c70-170">The element has its pointer descriptor.</span></span>

6.  <span data-ttu-id="38c70-171">具有指標的結構陣列</span><span class="sxs-lookup"><span data-stu-id="38c70-171">Arrays of structures with pointers</span></span>

    <span data-ttu-id="38c70-172">根據陣列的大小，會將具有指標的簡單結構陣列產生為 SMFARRAY 或 CARRAY，但在這兩種情況下，它都具有完整 (固定 \_ 重複或變數重複) 的指標配置 \_ 。</span><span class="sxs-lookup"><span data-stu-id="38c70-172">An array of simple structures with pointers is generated as an SMFARRAY or CARRAY depending whether the array is sized, but in both cases it has a pointer layout that is complete (FIXED\_REPEAT or VARIABLE\_REPEAT).</span></span> <span data-ttu-id="38c70-173">指標版面配置位於成員配置之前。</span><span class="sxs-lookup"><span data-stu-id="38c70-173">The pointer layout comes before the member layout.</span></span>

    <span data-ttu-id="38c70-174">具有指標的複雜結構陣列會產生為假 \_ 陣列，不論它是固定或調整大小，而且在這兩種情況下，都不會有任何指標版面配置。</span><span class="sxs-lookup"><span data-stu-id="38c70-174">An array of complex structures with pointers is generated as BOGUS\_ARRAY regardless whether it is fixed or sized, and in both cases, does not have any pointer layout.</span></span>

## <a name="what-the-ndr-engine-does"></a><span data-ttu-id="38c70-175">NDR 引擎的作用</span><span class="sxs-lookup"><span data-stu-id="38c70-175">What the NDR Engine Does</span></span>

<span data-ttu-id="38c70-176">本節說明 NDR 引擎的行為。</span><span class="sxs-lookup"><span data-stu-id="38c70-176">This section describes the NDR engine behavior.</span></span>

<span data-ttu-id="38c70-177">**封送處理傳遞**</span><span class="sxs-lookup"><span data-stu-id="38c70-177">**The marshaling pass**</span></span>

1.  <span data-ttu-id="38c70-178">符合標準的結構以及符合內嵌式的結構。</span><span class="sxs-lookup"><span data-stu-id="38c70-178">Conformant structures and embedded conformant structure.</span></span>

    <span data-ttu-id="38c70-179">最上層結構的行為就像單一層級結構一樣。</span><span class="sxs-lookup"><span data-stu-id="38c70-179">The top-level structure behaves like a single-level structure.</span></span>

2.  <span data-ttu-id="38c70-180">具有符合標準陣列的內嵌複雜結構</span><span class="sxs-lookup"><span data-stu-id="38c70-180">Embedded complex structure with conformant array</span></span>

    <span data-ttu-id="38c70-181">任何複雜的結構都會強制外部結構成為複雜的結構。</span><span class="sxs-lookup"><span data-stu-id="38c70-181">Any complex structure forces the outer structure to be a complex structure.</span></span> <span data-ttu-id="38c70-182">內嵌結構絕不會將其陣列封送處理。</span><span class="sxs-lookup"><span data-stu-id="38c70-182">Embedded structure never marshals its array.</span></span> <span data-ttu-id="38c70-183">每個結構一律會透過直接封送處理成員，而將成員視為 FC 指標，來通過內嵌指標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="38c70-183">Every structure always goes through embedded pointers by simply marshaling members and a member happening to be an FC\_POINTER.</span></span>

3.  <span data-ttu-id="38c70-184">具有符合結構的複雜結構</span><span class="sxs-lookup"><span data-stu-id="38c70-184">Complex structure with conformant structure</span></span>

    <span data-ttu-id="38c70-185">最上層的內嵌一致結構會將符合的陣列和所有 pointees 封送處理。</span><span class="sxs-lookup"><span data-stu-id="38c70-185">The top-most embedded conformant structure marshals the conformant array and all the pointees.</span></span> <span data-ttu-id="38c70-186">如果有的話，NDR 引擎永遠不會向更深層的符合結構的結構進行遞減。這會簡化方案，因為符合的結構是在内嵌物件的封送處理時所關心的分葉物件。</span><span class="sxs-lookup"><span data-stu-id="38c70-186">The NDR engine never descends to deeper nested conformant structures if there are any; this simplifies the solution, as a conformant structure is a leaf object as far as the marshaling of embedded objects is concerned.</span></span> <span data-ttu-id="38c70-187">最上層複雜結構會略過陣列封送處理。</span><span class="sxs-lookup"><span data-stu-id="38c70-187">The top-level complex structure skips the array marshaling.</span></span>

<span data-ttu-id="38c70-188">**封送處理、bufsizing 和釋放行程**</span><span class="sxs-lookup"><span data-stu-id="38c70-188">**Unmarshaling, bufsizing and freeing passes**</span></span>

<span data-ttu-id="38c70-189">封送處理已對稱至封送處理;它針對複雜結構執行的第一項作業是透過呼叫 **NdrComplexStructBufferSize** 函式的方式，找出緩衝區中的 pointees 位置。</span><span class="sxs-lookup"><span data-stu-id="38c70-189">Unmarshaling is symmetrical to marshaling; the first operation it performs for complex structures is to find out the pointees' location in the buffer by means of calling the **NdrComplexStructBufferSize** function.</span></span> <span data-ttu-id="38c70-190">然後，它會以平行方式拆收 pointees，啟用相同的配置以正確地將 pointees 重新封送處理。</span><span class="sxs-lookup"><span data-stu-id="38c70-190">It then unmarshals pointees in parallel, enabling the same scheme for unmarshaling the pointees correctly to be used.</span></span> <span data-ttu-id="38c70-191">應該不會與調整大小的物件和等位混淆;記憶體影像不應該用於調整大小的物件和等位，只適用于緩衝區內容。</span><span class="sxs-lookup"><span data-stu-id="38c70-191">There should be no confusion about sized objects and unions; the memory image should not be used for sized objects and unions, just for the buffer contents.</span></span>

<span data-ttu-id="38c70-192">用來正確執行封送處理和封送處理的旗標會以 bufsizing 和釋出的相同方式來使用，以確保 pointees 只會進行一次。</span><span class="sxs-lookup"><span data-stu-id="38c70-192">The flags used to perform marshaling and unmarshaling correctly are used in the same way in bufsizing and freeing to make sure that pointees are walked exactly once.</span></span>

<span data-ttu-id="38c70-193">**Endianess pass**</span><span class="sxs-lookup"><span data-stu-id="38c70-193">**Endianess pass**</span></span>

<span data-ttu-id="38c70-194">一開始，endianess 階段有點類似封送處理/封送處理;需要兩個階段來處理複雜的結構。</span><span class="sxs-lookup"><span data-stu-id="38c70-194">At first, the endianess pass is somewhat similar to marshaling/unmarshaling; two passes are required to process complex structures.</span></span> <span data-ttu-id="38c70-195">第一次傳遞會轉換平面元件，並在緩衝區中尋找 pointees 的位置，類似于 bufsizing 如何執行這項作業以進行封送處理。</span><span class="sxs-lookup"><span data-stu-id="38c70-195">First pass converts the flat part and finds the pointees' location in the buffer similar to how bufsizing performs this operation for unmarshaling.</span></span> <span data-ttu-id="38c70-196">第二次傳遞會轉換 pointees。</span><span class="sxs-lookup"><span data-stu-id="38c70-196">The second pass then converts the pointees.</span></span>

<span data-ttu-id="38c70-197">Endianess 的傳遞會以下列方式不同：每個結構和每個成員都必須逐步執行，直到分葉成員或元素是簡單類型。</span><span class="sxs-lookup"><span data-stu-id="38c70-197">Endianess passes differ in the following manner: every structure and every member has to be stepped until the leaf member or element is a simple type.</span></span> <span data-ttu-id="38c70-198">這與封送的不同;例如，在進行封送處理時，永遠不需要處理內嵌在符合標準結構中的符合結構，也不需要處理任何符合標準之結構的成員。</span><span class="sxs-lookup"><span data-stu-id="38c70-198">This is different from unmarshaling; in unmarshaling, for example, there is never a need to process conformant structures embedded in conformant structures, or any member of the conformant structure, for that matter.</span></span> <span data-ttu-id="38c70-199">另一個問題是，轉換不是等冪作業，因此，封送處理階段可能會取消對部分片段的封送處理，而不會造成損害，而轉換必須針對每個簡單的類型執行。</span><span class="sxs-lookup"><span data-stu-id="38c70-199">Another issue is that the conversion is not an idempotent operation—hence the unmarshaling pass could redo unmarshaling of some pieces without harm, while conversion has to be performed on a strictly once-per-any-simple-type basis.</span></span>

<span data-ttu-id="38c70-200">因此，endianess 演算法可摘要如下所示。</span><span class="sxs-lookup"><span data-stu-id="38c70-200">Hence, the endianess algorithm can be summarized as the following.</span></span> <span data-ttu-id="38c70-201">NDR 具有最上層一致結構的概念，以及適當的旗標。</span><span class="sxs-lookup"><span data-stu-id="38c70-201">NDR has a notion of the top-level conformant structure and a flag to mark that, as appropriate.</span></span> <span data-ttu-id="38c70-202">當您第一次進行時（例如轉換一般部分以及取得 pointees 的位置），不會使用這個概念。</span><span class="sxs-lookup"><span data-stu-id="38c70-202">When walking the first time, such as to convert the flat portion and to obtain the location of the pointees, this notion would not be used.</span></span> <span data-ttu-id="38c70-203">NDR 會流經所有層級結構的一般部分，而且永遠不會進入指標處理。</span><span class="sxs-lookup"><span data-stu-id="38c70-203">NDR would descend through the flat parts of all levels of structures and never venture into pointer processing.</span></span> <span data-ttu-id="38c70-204">最後，NDR 會在最上層轉換陣列。</span><span class="sxs-lookup"><span data-stu-id="38c70-204">Finally, NDR would flat convert the array at the top-level.</span></span>

<span data-ttu-id="38c70-205">當您第二次進行時，旗標會用來標示內嵌指標的傳遞，以避免輸入較深層的符合結構，然後是最符合標準的結構。</span><span class="sxs-lookup"><span data-stu-id="38c70-205">When walking the second time, the flag would be used to mark the embedded pointer's pass to avoid entering deeper levels of the conformant structures, then the top-most conformant structure.</span></span> <span data-ttu-id="38c70-206">如此一來，旗標會強制執行常見的封送處理/封送處理行為，這是為了避免將較深層的一致性結構遞減。</span><span class="sxs-lookup"><span data-stu-id="38c70-206">In this way, the flag would force the common marshaling/unmarshaling behavior, which is to avoid descending into deeper levels of conformant structures.</span></span>

<span data-ttu-id="38c70-207">具有一致陣列的複雜結構的第二個傳遞會如下所示：複雜結構的運作方式如下：這表示更深層的層級絕對不會查看或略過其一致大小或其符合標準的陣列，而是只會在不觸及陣列的情況下引導其成員。</span><span class="sxs-lookup"><span data-stu-id="38c70-207">The second pass for complex structures with conformant arrays works as follows: the complex structures work the common way; which means deeper levels would never look at or skip their conformant size or their conformant arrays, and would rather simply walk their members without touching the array.</span></span>

<span data-ttu-id="38c70-208">對於具有符合結構的複雜結構，符合標準的結構必須知道它是否為最上層，以及它是否在複雜的結構中。</span><span class="sxs-lookup"><span data-stu-id="38c70-208">For complex structures with conformant structures, the conformant structure must be aware whether it is top level, and whether it is in a complex structure.</span></span> <span data-ttu-id="38c70-209">陣列的平面部分是由最上層最符合標準的結構所處理。</span><span class="sxs-lookup"><span data-stu-id="38c70-209">The flat portion of the array is processed by the top-most conformant structure.</span></span> <span data-ttu-id="38c70-210">在第二次行程中，最符合標準的結構會略過一般部分，並經過指標配置，然後再返回。</span><span class="sxs-lookup"><span data-stu-id="38c70-210">On the second pass, the top-most conformant structure would skip the flat portion and go through the pointer layout and return.</span></span> <span data-ttu-id="38c70-211">最上層的複雜結構會略過它的一般部分，也會略過指標版面配置。</span><span class="sxs-lookup"><span data-stu-id="38c70-211">The top-most complex structure would skip its flat portion, and would also skip the pointer layout.</span></span>

<span data-ttu-id="38c70-212">**Endianess 逐步解說的強大層面**</span><span class="sxs-lookup"><span data-stu-id="38c70-212">**The robust aspect of the endianess walks**</span></span>

<span data-ttu-id="38c70-213">Endianess 逐步檢查常見的緩衝區外狀況，並執行其他不相關本質的檢查。</span><span class="sxs-lookup"><span data-stu-id="38c70-213">The endianess walk checks for the usual out-of-the-buffer conditions and performs other checks of an uncorrelated nature.</span></span> <span data-ttu-id="38c70-214">以關聯值為目標的檢查 (例如，調整大小引數與一致大小) 無法使用此步驟執行;它們會在稍後進行封送時執行。</span><span class="sxs-lookup"><span data-stu-id="38c70-214">The checks aimed at correlated values (such as the sizing argument versus the conformant size) cannot be performed using this step; they are performed later, when unmarshaling.</span></span>

 

 




