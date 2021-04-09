---
title: RPC) 的結構 (
description: 遠端程序呼叫中的各種結構類型的描述， (RPC) 。
ms.assetid: edaf547d-d3d1-443c-93dd-8e036bc42944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ccae91f703badd2e0153dfc3d8acff1ace562f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023821"
---
# <a name="structures-rpc"></a><span data-ttu-id="1fc88-103">RPC) 的結構 (</span><span class="sxs-lookup"><span data-stu-id="1fc88-103">Structures (RPC)</span></span>

<span data-ttu-id="1fc88-104">結構有數種類別，在封送處理所需的動作方面逐漸複雜。</span><span class="sxs-lookup"><span data-stu-id="1fc88-104">There are several categories of structures, progressively more complicated in terms of actions required for marshaling.</span></span> <span data-ttu-id="1fc88-105">它們的開頭是可以全部封鎖複製的簡單結構，然後繼續進行必須依欄位提供服務欄位的複雜結構。</span><span class="sxs-lookup"><span data-stu-id="1fc88-105">They begin with a simple structure that can be block-copied as a whole, and continue to a complex structure that has to be serviced field by field.</span></span>

-   [<span data-ttu-id="1fc88-106">簡單結構</span><span class="sxs-lookup"><span data-stu-id="1fc88-106">Simple Structure</span></span>](#simple-structure)
-   [<span data-ttu-id="1fc88-107">具有指標的簡單結構</span><span class="sxs-lookup"><span data-stu-id="1fc88-107">Simple Structure with Pointers</span></span>](#simple-structure-with-pointers)
-   [<span data-ttu-id="1fc88-108">符合標準的結構</span><span class="sxs-lookup"><span data-stu-id="1fc88-108">Conformant Structure</span></span>](#conformant-structure)
-   [<span data-ttu-id="1fc88-109">具有指標的一致結構</span><span class="sxs-lookup"><span data-stu-id="1fc88-109">Conformant Structure with Pointers</span></span>](#conformant-structure-with-pointers)
-   [<span data-ttu-id="1fc88-110">具有或不具有指標的一致結構 () </span><span class="sxs-lookup"><span data-stu-id="1fc88-110">Conformant Varying Structure (with or without Pointers)</span></span>](#conformant-varying-structure-with-or-without-pointers)
-   [<span data-ttu-id="1fc88-111">硬結構</span><span class="sxs-lookup"><span data-stu-id="1fc88-111">Hard Structure</span></span>](#hard-structure)
-   [<span data-ttu-id="1fc88-112">複雜結構</span><span class="sxs-lookup"><span data-stu-id="1fc88-112">Complex Structure</span></span>](#complex-structure)
-   [<span data-ttu-id="1fc88-113">結構成員版面配置描述</span><span class="sxs-lookup"><span data-stu-id="1fc88-113">Structure Member Layout Description</span></span>](#structure-member-layout-description)

> [!Note]  
> <span data-ttu-id="1fc88-114">相較于陣列類別目錄，它會清楚地描述最高可達64k 大小的結構， (大小適用于結構) 的平面部分，也就是沒有適用于 SM 和 LG 陣列的專案。</span><span class="sxs-lookup"><span data-stu-id="1fc88-114">When compared to array categories, it becomes clear that only structures up to 64k in size can be described (the size is for the flat part of the structure), that is there is no equivalent of SM and LG arrays.</span></span>

 

<span data-ttu-id="1fc88-115">**結構通用的成員**</span><span class="sxs-lookup"><span data-stu-id="1fc88-115">**Members Common to Structures**</span></span>

-   <span data-ttu-id="1fc88-116">**對準**</span><span class="sxs-lookup"><span data-stu-id="1fc88-116">**alignment**</span></span>

    <span data-ttu-id="1fc88-117">封送結構之前的緩衝區所需的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="1fc88-117">The necessary alignment of the buffer before unmarshaling the structure.</span></span> <span data-ttu-id="1fc88-118">有效的值為0、1、3和 7 (實際對齊減 1) 。</span><span class="sxs-lookup"><span data-stu-id="1fc88-118">Valid values are 0, 1, 3, and 7 (the actual alignment minus 1).</span></span>

-   <span data-ttu-id="1fc88-119">**記憶體 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="1fc88-119">**memory\_size**</span></span>

    <span data-ttu-id="1fc88-120">結構在記憶體中的大小，以位元組為單位;針對符合標準的結構，這個大小不包含陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="1fc88-120">Size of the structure in memory in bytes; for conformant structures this size does not include the array's size.</span></span>

-   <span data-ttu-id="1fc88-121">**\_ \_ 陣列描述的 \_ 位移**</span><span class="sxs-lookup"><span data-stu-id="1fc88-121">**offset\_to\_array\_description**</span></span>

    <span data-ttu-id="1fc88-122">從目前的格式字串指標位移到結構中所包含之符合的陣列描述。</span><span class="sxs-lookup"><span data-stu-id="1fc88-122">Offset from the current format string pointer to the description of the conformant array contained in a structure.</span></span>

-   <span data-ttu-id="1fc88-123">**成員 \_ 版面配置**</span><span class="sxs-lookup"><span data-stu-id="1fc88-123">**member\_layout**</span></span>

    <span data-ttu-id="1fc88-124">結構中每個元素的描述。</span><span class="sxs-lookup"><span data-stu-id="1fc88-124">Description of each element of the structure.</span></span> <span data-ttu-id="1fc88-125">如果需要 endian 轉換，或者型別是複雜結構，則 NDR 常式只需要檢查類型之格式字串的這個部分。</span><span class="sxs-lookup"><span data-stu-id="1fc88-125">The NDR routines only need to examine this portion of a type's format string if endian transformation is needed or if the type is a complex structure.</span></span>

-   <span data-ttu-id="1fc88-126">**指標 \_ 版面配置**</span><span class="sxs-lookup"><span data-stu-id="1fc88-126">**pointer\_layout**</span></span>

    <span data-ttu-id="1fc88-127">請參閱 [指標版面](pointer-layout-tfs.md) 配置區段。</span><span class="sxs-lookup"><span data-stu-id="1fc88-127">See the [Pointer Layout](pointer-layout-tfs.md) section.</span></span>

## <a name="simple-structure"></a><span data-ttu-id="1fc88-128">簡單結構</span><span class="sxs-lookup"><span data-stu-id="1fc88-128">Simple Structure</span></span>

<span data-ttu-id="1fc88-129">簡單結構只包含基底類型、固定陣列和其他簡單結構。</span><span class="sxs-lookup"><span data-stu-id="1fc88-129">A simple structure contains only base types, fixed arrays, and other simple structures.</span></span> <span data-ttu-id="1fc88-130">簡單結構的主要功能是可以全部區塊複製。</span><span class="sxs-lookup"><span data-stu-id="1fc88-130">The main feature of the simple structure is that it can be block-copied as a whole.</span></span>

``` syntax
FC_STRUCT alignment<1> 
memory_size<2> 
member_layout<> 
FC_END
```

## <a name="simple-structure-with-pointers"></a><span data-ttu-id="1fc88-131">具有指標的簡單結構</span><span class="sxs-lookup"><span data-stu-id="1fc88-131">Simple Structure with Pointers</span></span>

<span data-ttu-id="1fc88-132">具有指標的簡單結構只包含基底類型、指標、固定陣列、簡單結構和其他具有指標的簡單結構。</span><span class="sxs-lookup"><span data-stu-id="1fc88-132">A simple structure with pointers contains only base types, pointers, fixed arrays, simple structures, and other simple structures with pointers.</span></span> <span data-ttu-id="1fc88-133">因為版面配置<> 只需要在進行 endianess 轉換時流覽，所以會置於描述的結尾。</span><span class="sxs-lookup"><span data-stu-id="1fc88-133">Because the layout<> will only have to be visited when doing an endianess conversion, it is placed at the end of the description.</span></span>

``` syntax
FC_PSTRUCT alignment<1> 
memory_size<2> 
pointer_layout<> 
member_layout<> 
FC_END
```

## <a name="conformant-structure"></a><span data-ttu-id="1fc88-134">符合標準的結構</span><span class="sxs-lookup"><span data-stu-id="1fc88-134">Conformant Structure</span></span>

<span data-ttu-id="1fc88-135">符合標準的結構只包含基底類型、固定陣列和簡單結構，而且必須包含符合標準的字串或符合標準的陣列。</span><span class="sxs-lookup"><span data-stu-id="1fc88-135">A conformant structure contains only base types, fixed arrays, and simple structures, and must contain either a conformant string or a conformant array.</span></span> <span data-ttu-id="1fc88-136">這個陣列實際上可以包含在另一個符合標準的結構中，或是具有內嵌在此結構中之指標的一致結構。</span><span class="sxs-lookup"><span data-stu-id="1fc88-136">This array could actually be contained in another conformant structure or conformant structure with pointers which is embedded in this structure.</span></span>

``` syntax
FC_CSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
member_layout<> 
FC_END
```

## <a name="conformant-structure-with-pointers"></a><span data-ttu-id="1fc88-137">具有指標的一致結構</span><span class="sxs-lookup"><span data-stu-id="1fc88-137">Conformant Structure with Pointers</span></span>

<span data-ttu-id="1fc88-138">具有指標的一致結構只包含基底類型、指標、固定陣列、簡單結構，以及具有指標的簡單結構;符合標準的結構必須包含符合標準的陣列。</span><span class="sxs-lookup"><span data-stu-id="1fc88-138">A conformant structure with pointers contains only base types, pointers, fixed arrays, simple structures, and simple structures with pointers; a conformant structure must contain a conformant array.</span></span> <span data-ttu-id="1fc88-139">這個陣列實際上可以包含在另一個符合標準的結構中，或是具有內嵌在此結構中的指標。</span><span class="sxs-lookup"><span data-stu-id="1fc88-139">This array could actually be contained in another conformant structure or conformant structure with pointers that is embedded in this structure.</span></span>

``` syntax
FC_CPSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
pointer_layout<> 
member_layout<> FC_END
```

## <a name="conformant-varying-structure-with-or-without-pointers"></a><span data-ttu-id="1fc88-140">具有或不具有指標的一致結構 () </span><span class="sxs-lookup"><span data-stu-id="1fc88-140">Conformant Varying Structure (with or without Pointers)</span></span>

<span data-ttu-id="1fc88-141">一致的不同結構只包含簡單類型、指標、固定陣列、簡單結構，以及具有指標的簡單結構;一致的不同結構必須包含符合標準的字串或一致的陣列。</span><span class="sxs-lookup"><span data-stu-id="1fc88-141">A conformant varying structure contains only simple types, pointers, fixed arrays, simple structures, and simple structures with pointers; a conformant varying structure must contain either a conformant string or a conformant-varying array.</span></span> <span data-ttu-id="1fc88-142">符合標準的字串或陣列實際上可以包含在另一個符合標準的結構中，也可以包含內嵌在此結構中的指標。</span><span class="sxs-lookup"><span data-stu-id="1fc88-142">The conformant string or array can actually be contained in another conformant structure or conformant structure with pointers that is embedded in this structure.</span></span>

``` syntax
FC_CVSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
[pointer_layout<>] 
layout<> 
FC_END
```

## <a name="hard-structure"></a><span data-ttu-id="1fc88-143">硬結構</span><span class="sxs-lookup"><span data-stu-id="1fc88-143">Hard Structure</span></span>

<span data-ttu-id="1fc88-144">硬結構是一種概念，目的是要消除與處理複雜結構相關的嚴厲處罰。</span><span class="sxs-lookup"><span data-stu-id="1fc88-144">The hard structure was a concept aimed at eliminating steep penalties related to processing complex structures.</span></span> <span data-ttu-id="1fc88-145">它衍生自觀察：複雜結構通常只有一或兩個條件會防止封鎖複製，因此否則沒有其效能與簡單結構相比。</span><span class="sxs-lookup"><span data-stu-id="1fc88-145">It is derived from an observation that a complex structure typically has only one or two conditions that prevent block-copying, and therefore spoil its performance compared to a simple structure.</span></span> <span data-ttu-id="1fc88-146">原因通常是等位或列舉欄位。</span><span class="sxs-lookup"><span data-stu-id="1fc88-146">The culprits are usually unions or enumeration fields.</span></span>

<span data-ttu-id="1fc88-147">「硬式結構」（hard structure）是在記憶體中有 enum16、結束填補或聯集做為最後一個成員的結構。</span><span class="sxs-lookup"><span data-stu-id="1fc88-147">A hard structure is a structure that has an enum16, end-padding in memory, or a union as the last member.</span></span> <span data-ttu-id="1fc88-148">這三個元素可防止結構進入先前的其中一個結構類別，這可享有小型的解讀負荷和最大的優化潛力，但不會將它強制進入成本極高的複雜結構類別。</span><span class="sxs-lookup"><span data-stu-id="1fc88-148">These three elements prevent the structure from falling into one of the previous structure categories, which enjoy small interpretation overhead and maximum optimization potential, but do not force it into the very costly complex structure category.</span></span>

<span data-ttu-id="1fc88-149">Enum16 不能讓結構的記憶體和線大小有所差異。</span><span class="sxs-lookup"><span data-stu-id="1fc88-149">The enum16 must not cause the memory and wire sizes of the structure to differ.</span></span> <span data-ttu-id="1fc88-150">結構不能有任何符合標準的陣列，也不能 (任何指標，除非 union) 的一部分;唯一允許的其他成員為基底類型、固定陣列和簡單結構。</span><span class="sxs-lookup"><span data-stu-id="1fc88-150">The structure cannot have any conformant array, nor any pointers (unless part of the union); the only other members allowed are base types, fixed arrays, and simple structures.</span></span>

``` syntax
FC_HARD_STRUCTURE alignment<1> 
memory_size<2> 
reserved<4> 
enum_offset<2> 
copy_size<2> 
mem_copy_incr<2> 
union_description_offset<2>
member_layout<> 
FC_END
```

<span data-ttu-id="1fc88-151">列舉 \_ offset<2> 欄位提供從記憶體中的結構開始到其中包含 enum16 的位移，否則列舉 \_ 位移<2> 欄位為–1。</span><span class="sxs-lookup"><span data-stu-id="1fc88-151">The enum\_offset<2> field provides the offset from the beginning of the structure in memory to an enum16 if it contains one; otherwise the enum\_offset<2> field is –1.</span></span>

<span data-ttu-id="1fc88-152">[複製 \_ 大小<2]> 欄位提供結構中的位元組總數，可能會區塊複製到緩衝區或從中複製。</span><span class="sxs-lookup"><span data-stu-id="1fc88-152">The copy\_size<2> field provides the total number of bytes in the structure, which may be block-copied into/from the buffer.</span></span> <span data-ttu-id="1fc88-153">此總計不包含任何尾端的聯集，也不包含記憶體中的任何結束填補。</span><span class="sxs-lookup"><span data-stu-id="1fc88-153">This total does not include any trailing union nor any end-padding in memory.</span></span> <span data-ttu-id="1fc88-154">此值也是緩衝區指標在複製之後的遞增量。</span><span class="sxs-lookup"><span data-stu-id="1fc88-154">This value is also the amount the buffer pointer should be incremented following the copy.</span></span>

<span data-ttu-id="1fc88-155">\_ \_ 記憶體複製增量<2> 欄位是記憶體指標在處理任何尾端等位之前，應該在區塊複製之後遞增的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="1fc88-155">The mem\_copy\_incr<2> field is the number of bytes the memory pointer should be incremented following the block-copy before handling any trailing union.</span></span> <span data-ttu-id="1fc88-156">依此數量遞增 (不是依複製 \_ 大小<2> 位元組) 產生適當的記憶體指標給任何尾端聯集。</span><span class="sxs-lookup"><span data-stu-id="1fc88-156">Incrementing by this amount (not by copy\_size<2> bytes) yields a proper memory pointer to any trailing union.</span></span>

## <a name="complex-structure"></a><span data-ttu-id="1fc88-157">複雜結構</span><span class="sxs-lookup"><span data-stu-id="1fc88-157">Complex Structure</span></span>

<span data-ttu-id="1fc88-158">複雜結構是包含一或多個欄位的任何結構，這些欄位會防止禁止複製結構，或必須在封送處理或封送處理期間執行額外的檢查 (例如，列舉) 的系結檢查。</span><span class="sxs-lookup"><span data-stu-id="1fc88-158">A complex structure is any structure containing one or more fields that either prevent the structure from being block-copied, or for which additional checking must be performed during marshaling or unmarshaling (for example, bound checks on an enumeration).</span></span> <span data-ttu-id="1fc88-159">下列 NDR 類型落在此類別中：</span><span class="sxs-lookup"><span data-stu-id="1fc88-159">The following NDR types fall in this category:</span></span>

-   <span data-ttu-id="1fc88-160">[簡單類型](simple-types-tfs.md)： \_ \_ 在64位平臺上的 ENUM16、INT3264 (只能) 、具有 \[ [**範圍** 的整數](/windows/desktop/Midl/range)\]</span><span class="sxs-lookup"><span data-stu-id="1fc88-160">[simple types](simple-types-tfs.md): ENUM16, \_\_INT3264 (on 64-bit platforms only), an integral with \[[**range**](/windows/desktop/Midl/range)\]</span></span>
-   <span data-ttu-id="1fc88-161">結構結尾的對齊填補</span><span class="sxs-lookup"><span data-stu-id="1fc88-161">alignment padding at the end of the structure</span></span>
-   <span data-ttu-id="1fc88-162">介面指標 (使用內嵌複雜) </span><span class="sxs-lookup"><span data-stu-id="1fc88-162">interface pointers (they go using an embedded complex)</span></span>
-   <span data-ttu-id="1fc88-163">略過的指標 (與 \[ [**ignore**](/windows/desktop/Midl/ignore) \] 屬性和 FC \_ ignore token 相關) </span><span class="sxs-lookup"><span data-stu-id="1fc88-163">ignored pointers (that is related to \[[**ignore**](/windows/desktop/Midl/ignore)\] attribute and FC\_IGNORE token)</span></span>
-   <span data-ttu-id="1fc88-164">複雜陣列、不同陣列、字串陣列</span><span class="sxs-lookup"><span data-stu-id="1fc88-164">complex arrays, varying arrays, string arrays</span></span>
-   <span data-ttu-id="1fc88-165">具有至少一個 nonfixed 維度的多維度一致陣列</span><span class="sxs-lookup"><span data-stu-id="1fc88-165">multidimensional conformant arrays with at least one nonfixed dimension</span></span>
-   <span data-ttu-id="1fc88-166">等位</span><span class="sxs-lookup"><span data-stu-id="1fc88-166">unions</span></span>
-   <span data-ttu-id="1fc88-167">以 \[ [**傳輸 \_ 為**](/windows/desktop/Midl/transmit-as)的方式定義的元素 \] ， \[ [**表示 \_ 為**](/windows/desktop/Midl/represent-as) \] 、 \[ [**電匯 \_**](/windows/desktop/Midl/wire-marshal)、 \] \[ [**使用者 \_ 封送**](/windows/desktop/Midl/user-marshal)處理\]</span><span class="sxs-lookup"><span data-stu-id="1fc88-167">elements defined with \[[**transmit\_as**](/windows/desktop/Midl/transmit-as)\], \[[**represent\_as**](/windows/desktop/Midl/represent-as)\], \[[**wire\_marshal**](/windows/desktop/Midl/wire-marshal)\], \[[**user\_marshal**](/windows/desktop/Midl/user-marshal)\]</span></span>
-   <span data-ttu-id="1fc88-168">內嵌複雜結構</span><span class="sxs-lookup"><span data-stu-id="1fc88-168">embedded complex structures</span></span>
-   <span data-ttu-id="1fc88-169">在結構結尾處填補</span><span class="sxs-lookup"><span data-stu-id="1fc88-169">padding at the end of the structure</span></span>

<span data-ttu-id="1fc88-170">複雜結構具有下列格式描述：</span><span class="sxs-lookup"><span data-stu-id="1fc88-170">A complex structure has the following format description:</span></span>

``` syntax
FC_BOGUS_STRUCT alignment<1> 
memory_size<2> 
offset_to_conformant_array_description<2> 
offset_to_pointer_layout<2> 
member_layout<> 
FC_END 
[pointer_layout<>]
```

<span data-ttu-id="1fc88-171">記憶體 \_ 大小<2> 欄位是記憶體中的結構大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1fc88-171">The memory\_size<2> field is the size of the structure in memory, in bytes.</span></span>

<span data-ttu-id="1fc88-172">如果結構包含符合標準的陣列，則 \_ 符合標準 \_ 的 \_ 陣列 \_ 描述<2> 欄位會提供相符的陣列描述的位移，否則為零。</span><span class="sxs-lookup"><span data-stu-id="1fc88-172">If the structure contains a conformant array, the offset\_to\_conformant\_array\_description<2> field provides the offset to the conformant array's description, otherwise it is zero.</span></span>

<span data-ttu-id="1fc88-173">如果結構具有指標，指標配置的 \_ 位移 \_ \_<2> 欄位會提供超過結構的版面配置到指標配置的位移，否則此欄位為零。</span><span class="sxs-lookup"><span data-stu-id="1fc88-173">If the structure has pointers, the offset\_to\_pointer\_layout<2> field provides the offset past the structure's layout to the pointer layout, otherwise this field is zero.</span></span>

<span data-ttu-id="1fc88-174">\_複雜結構的指標版面配置<> 欄位的處理方式，與其他結構的處理方式稍有不同。</span><span class="sxs-lookup"><span data-stu-id="1fc88-174">The pointer\_layout<> field of a complex structure is handled somewhat differently than for other structures.</span></span> <span data-ttu-id="1fc88-175">複雜結構的 [指標配置] \_<> 欄位只包含結構本身中實際指標欄位的描述。</span><span class="sxs-lookup"><span data-stu-id="1fc88-175">The pointer\_layout<> field of a complex structure only contains descriptions of actual pointer fields in the structure itself.</span></span> <span data-ttu-id="1fc88-176">任何內嵌陣列、等位或結構內包含的任何指標，都不會在複雜結構的指標 \_ 版面配置<> 欄位中描述。</span><span class="sxs-lookup"><span data-stu-id="1fc88-176">Any pointers contained within any embedded arrays, unions, or structures are not described in the complex structure's pointer\_layout<> field.</span></span>

> [!Note]  
> <span data-ttu-id="1fc88-177">這與其他結構相反，後者會將內嵌陣列或結構中所包含之任何指標的描述複製到它們自己的指標配置 \_<> 欄位中。</span><span class="sxs-lookup"><span data-stu-id="1fc88-177">This is in contrast to other structures, which duplicate the description of any pointers contained in embedded arrays or structures in their own pointer \_layout<> field as well.</span></span>

 

<span data-ttu-id="1fc88-178">複雜結構指標配置的格式也有截然不同的差異。</span><span class="sxs-lookup"><span data-stu-id="1fc88-178">The format of a complex structure's pointer layout is also radically different.</span></span> <span data-ttu-id="1fc88-179">因為它只包含實際指標成員的描述，而且因為複雜結構會一次封送處理和取消封送處理一個欄位，所以指標 \_ 版面配置<> 欄位只包含所有指標成員的指標描述。</span><span class="sxs-lookup"><span data-stu-id="1fc88-179">Because it only contains descriptions of actual pointer members and because a complex structure is marshaled and unmarshaled one field at a time, the pointer\_layout<> field simply contains the pointer description of all pointer members.</span></span> <span data-ttu-id="1fc88-180">沒有開始 FC \_ PP，也沒有任何一般指標 \_ 版面配置<> 資訊。</span><span class="sxs-lookup"><span data-stu-id="1fc88-180">There is no beginning FC\_PP, and none of the usual pointer\_layout<> information.</span></span>

## <a name="structure-member-layout-description"></a><span data-ttu-id="1fc88-181">結構成員版面配置描述</span><span class="sxs-lookup"><span data-stu-id="1fc88-181">Structure Member Layout Description</span></span>

<span data-ttu-id="1fc88-182">結構的版面配置描述包含下列一或多個格式字元：</span><span class="sxs-lookup"><span data-stu-id="1fc88-182">A structure's layout description contains one or more of the following format characters:</span></span>

-   <span data-ttu-id="1fc88-183">任何基底類型字元，例如 FC \_ 字元等等</span><span class="sxs-lookup"><span data-stu-id="1fc88-183">Any of the base type characters, like FC\_CHAR, and so on</span></span>
-   <span data-ttu-id="1fc88-184">對齊指示詞。</span><span class="sxs-lookup"><span data-stu-id="1fc88-184">Alignment directives.</span></span> <span data-ttu-id="1fc88-185">有三個格式字元指定記憶體指標的對齊： FC \_ ALIGNM2、fc \_ ALIGNM4 和 fc \_ ALIGNM8。</span><span class="sxs-lookup"><span data-stu-id="1fc88-185">There are three format characters specifying alignment of the memory pointer: FC\_ALIGNM2, FC\_ALIGNM4, and FC\_ALIGNM8.</span></span>
    > [!Note]  
    > <span data-ttu-id="1fc88-186">另外還有緩衝區對齊權杖，FC \_ ALIGNB2 透過 fc \_ ALIGNM8; 這些都不會使用。</span><span class="sxs-lookup"><span data-stu-id="1fc88-186">There are also buffer alignment tokens, FC\_ALIGNB2 through FC\_ALIGNM8; these are not used.</span></span>

     

-   <span data-ttu-id="1fc88-187">記憶體填補。</span><span class="sxs-lookup"><span data-stu-id="1fc88-187">Memory padding.</span></span> <span data-ttu-id="1fc88-188">這些只會發生在結構描述的結尾，並表示結構中符合標準的陣列之前的記憶體填補位元組數： FC \_ STRUCTPADn，其中 n 是填補的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="1fc88-188">These occur only at the end of a structure's description and denote the number of bytes of padding in memory before the conformant array in the structure: FC\_STRUCTPADn, where n is the number of bytes of padding.</span></span>
-   <span data-ttu-id="1fc88-189">任何內嵌的 nonbase 類型 (注意，標準的陣列永遠不會出現在結構配置) 中。</span><span class="sxs-lookup"><span data-stu-id="1fc88-189">Any embedded nonbase type (note, however, that a conformant array never occurs in the structure layout).</span></span> <span data-ttu-id="1fc88-190">這有4個位元組的描述：</span><span class="sxs-lookup"><span data-stu-id="1fc88-190">This has a 4-byte description:</span></span>

    ``` syntax
    FC_EMBEDDED_COMPLEX memory_pad<1> 
    offset_to_description<2>,
    ```

    <span data-ttu-id="1fc88-191">其中的位移不保證會對齊2個位元組。</span><span class="sxs-lookup"><span data-stu-id="1fc88-191">where the offset is not guaranteed to be 2-byte aligned.</span></span>

    <span data-ttu-id="1fc88-192">memory \_ pad<1> 是在複雜欄位之前的記憶體中所需的填補。</span><span class="sxs-lookup"><span data-stu-id="1fc88-192">memory\_pad<1> is a padding needed in memory before the complex field.</span></span>

    <span data-ttu-id="1fc88-193">\_ \_ 描述的位移<2> 是內嵌型別的相對型別位移。</span><span class="sxs-lookup"><span data-stu-id="1fc88-193">offset\_to\_description<2> is a relative type offset to the embedded type.</span></span>

<span data-ttu-id="1fc88-194">如有需要，可能也會在 \_ 終止 fc 結束之前有 FC PAD， \_ 以確保格式字串會在 FC 端之後的雙位元組界限上對齊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1fc88-194">There may also be an FC\_PAD before the terminating FC\_END if needed to ensure that the format string will be aligned at a 2-byte boundary following the FC\_END.</span></span>

 

 