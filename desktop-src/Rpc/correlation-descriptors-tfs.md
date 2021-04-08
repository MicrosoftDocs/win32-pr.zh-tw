---
title: 相互關聯描述元
description: 相互關聯描述元是一個格式字串，它會根據與另一個引數相關的一個引數來描述運算式。
ms.assetid: 9f5f5077-d6a9-4253-bddf-b8cd0c868973
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f13f0793b99b80b7abb0b493c249b30ad53d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842667"
---
# <a name="correlation-descriptors"></a><span data-ttu-id="982ef-103">相互關聯描述元</span><span class="sxs-lookup"><span data-stu-id="982ef-103">Correlation Descriptors</span></span>

<span data-ttu-id="982ef-104">相互關聯描述元是一個格式字串，它會根據與另一個引數相關的一個引數來描述運算式。</span><span class="sxs-lookup"><span data-stu-id="982ef-104">A correlation descriptor is a format string that describes an expression based on one argument related to another argument.</span></span> <span data-ttu-id="982ef-105">需要相互關聯描述項，才能處理與屬性相關的語法 \[ ，例如，**大小 \_ 為 ()** \] 、 \[ **長度 \_ 為 ()** \] 、 \[ **參數 \_ ()** \] 且 \[ **iid \_ 為 ()** \] 。</span><span class="sxs-lookup"><span data-stu-id="982ef-105">A correlation descriptor is needed for handling semantics related to attributes like \[**size\_is()**\], \[**length\_is()**\], \[**switch\_is()**\] and \[**iid\_is()**\].</span></span> <span data-ttu-id="982ef-106">相互關聯描述項會搭配陣列、大小的指標、等位和介面指標使用。</span><span class="sxs-lookup"><span data-stu-id="982ef-106">Correlation descriptors are used with arrays, sized pointers, unions, and interface pointers.</span></span> <span data-ttu-id="982ef-107">最終運算式值可以是大小、長度、聯集判別或 IID 的指標。</span><span class="sxs-lookup"><span data-stu-id="982ef-107">The eventual expression value can be a size, a length, a union discriminant, or a pointer to an IID, respectively.</span></span> <span data-ttu-id="982ef-108">就格式字串而言，相互關聯描述項會搭配陣列、等位和介面指標使用。</span><span class="sxs-lookup"><span data-stu-id="982ef-108">In terms of format strings, correlation descriptors are used with arrays, unions, and interface pointers.</span></span> <span data-ttu-id="982ef-109">格式字串中會將大小的指標描述為數組的指標。</span><span class="sxs-lookup"><span data-stu-id="982ef-109">A sized pointer is described in format strings as a pointer to an array.</span></span>

<span data-ttu-id="982ef-110">有兩個執行基本運算式計算的常式： NdrpComputeConformance 用於大小、參數和 IID， \* 而 NdrpComputeVariance 則用於長度。</span><span class="sxs-lookup"><span data-stu-id="982ef-110">There are two routines performing basic expression calculations: NdrpComputeConformance is used for sizes, switches and IID\* while NdrpComputeVariance is used for lengths.</span></span> <span data-ttu-id="982ef-111">另外也有一個常式可以針對阻絕攻擊功能執行相互關聯值驗證。</span><span class="sxs-lookup"><span data-stu-id="982ef-111">There is also a single routine to perform a correlation value validation for denial-of-attack functionality.</span></span>

<span data-ttu-id="982ef-112">相互關聯描述項的設計僅支援非常有限的運算式。</span><span class="sxs-lookup"><span data-stu-id="982ef-112">Correlation descriptors have been designed to support only very limited expressions.</span></span> <span data-ttu-id="982ef-113">在複雜的情況下，編譯器會在需要時產生引擎所要呼叫的運算式評估常式。</span><span class="sxs-lookup"><span data-stu-id="982ef-113">For complicated situations, the compiler generates an expression evaluation routine to be called by the engine when needed.</span></span>

<span data-ttu-id="982ef-114">相互關聯描述項的格式如下：</span><span class="sxs-lookup"><span data-stu-id="982ef-114">A correlation descriptor has the following format:</span></span>

``` syntax
correlation_type<1>
correlation_operator<1>
offset<2>
[robust_flags<2>]
```

<span data-ttu-id="982ef-115">相互關聯描述項相互關聯 \_ 類型<1> 包含兩個 nibbles：上面的4個位描述可找到運算式的位置，而較低的4個位則描述運算式值的類型。</span><span class="sxs-lookup"><span data-stu-id="982ef-115">The correlation descriptor correlation\_type<1> consists of two nibbles: the upper 4 bits describe where the expression can be found and the lower 4 bits describe the type of the expression value.</span></span>

<span data-ttu-id="982ef-116">上半個位元組可以有下列五個值的其中一個：</span><span class="sxs-lookup"><span data-stu-id="982ef-116">The upper nibble can have one of these five values:</span></span>

``` syntax
00  FC_NORMAL_CONFORMANCE
10  FC_POINTER_CONFORMANCE
20  FC_TOP_LEVEL_CONFORMANCE
80  FC_TOP_LEVEL_MULTID_CONFORMANCE
40  FC_CONSTANT_CONFORMANCE
```

<dl> <dt>

<span data-ttu-id="982ef-117"><span id="FC_NORMAL_CONFORMANCE"></span><span id="fc_normal_conformance"></span>FC \_ 正常 \_ 一致性</span><span class="sxs-lookup"><span data-stu-id="982ef-117"><span id="FC_NORMAL_CONFORMANCE"></span><span id="fc_normal_conformance"></span>FC\_NORMAL\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="982ef-118">符合標準的標準案例，例如在結構的欄位中所述。</span><span class="sxs-lookup"><span data-stu-id="982ef-118">A normal case of conformance, such as that described in a field of a structure.</span></span>

</dd> <dt>

<span data-ttu-id="982ef-119"><span id="FC_POINTER_CONFORMANCE"></span><span id="fc_pointer_conformance"></span>FC \_ 指標 \_ 一致性</span><span class="sxs-lookup"><span data-stu-id="982ef-119"><span id="FC_POINTER_CONFORMANCE"></span><span id="fc_pointer_conformance"></span>FC\_POINTER\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="982ef-120">若為屬性化指標 (**\_ () 的大小**，則 **長度 \_ 會 ()** 為結構中欄位的) 。</span><span class="sxs-lookup"><span data-stu-id="982ef-120">For attributed pointers (**size\_is()**, **length\_is()**) which are fields in a structure.</span></span> <span data-ttu-id="982ef-121">這會影響基底記憶體指標的設定方式。</span><span class="sxs-lookup"><span data-stu-id="982ef-121">This affects the way the base memory pointer is set.</span></span>

</dd> <dt>

<span data-ttu-id="982ef-122"><span id="FC_TOP_LEVEL_CONFORMANCE"></span><span id="fc_top_level_conformance"></span>FC \_ 最 \_ 上層 \_ 一致性</span><span class="sxs-lookup"><span data-stu-id="982ef-122"><span id="FC_TOP_LEVEL_CONFORMANCE"></span><span id="fc_top_level_conformance"></span>FC\_TOP\_LEVEL\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="982ef-123">適用于其他參數所描述的最上層一致性。</span><span class="sxs-lookup"><span data-stu-id="982ef-123">For top-level conformance described by another parameter.</span></span>

</dd> <dt>

<span data-ttu-id="982ef-124"><span id="FC_TOP_LEVEL_MULTID_CONFORMANCE"></span><span id="fc_top_level_multid_conformance"></span>FC \_ 最 \_ 上層 \_ MULTID \_ 一致性</span><span class="sxs-lookup"><span data-stu-id="982ef-124"><span id="FC_TOP_LEVEL_MULTID_CONFORMANCE"></span><span id="fc_top_level_multid_conformance"></span>FC\_TOP\_LEVEL\_MULTID\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="982ef-125">針對其他參數所描述之多維度陣列的最高層級一致性。</span><span class="sxs-lookup"><span data-stu-id="982ef-125">For top-level conformance of a multidimensional array described by another parameter.</span></span>

> [!Note]  
> <span data-ttu-id="982ef-126">多維度大小的陣列和指標會觸發切換至 [**– Oicf**](/windows/desktop/Midl/-oi)。</span><span class="sxs-lookup"><span data-stu-id="982ef-126">Multidimensional sized arrays and pointers trigger a switch to [**–Oicf**](/windows/desktop/Midl/-oi).</span></span>

 

</dd> <dt>

<span data-ttu-id="982ef-127"><span id="FC_CONSTANT_CONFORMANCE"></span><span id="fc_constant_conformance"></span>FC \_ 常數 \_ 一致性</span><span class="sxs-lookup"><span data-stu-id="982ef-127"><span id="FC_CONSTANT_CONFORMANCE"></span><span id="fc_constant_conformance"></span>FC\_CONSTANT\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="982ef-128">若為常數值。</span><span class="sxs-lookup"><span data-stu-id="982ef-128">For a constant value.</span></span> <span data-ttu-id="982ef-129">編譯器會從使用者提供的常數運算式之該層值。</span><span class="sxs-lookup"><span data-stu-id="982ef-129">The compiler precalculates the value from a constant expression supplied by the user.</span></span> <span data-ttu-id="982ef-130">當發生這種情況時，一致性描述中的後續3個位元組會包含較長的3個位元組，以描述一致性大小。</span><span class="sxs-lookup"><span data-stu-id="982ef-130">When this is the case, the subsequent 3 bytes in the conformance description contain the lower 3 bytes of a long describing the conformance size.</span></span> <span data-ttu-id="982ef-131">不需要進一步的計算。</span><span class="sxs-lookup"><span data-stu-id="982ef-131">No further computation is required.</span></span>

</dd> </dl>

<span data-ttu-id="982ef-132">較低的半值會提供需要從記憶體解壓縮的數值型別：</span><span class="sxs-lookup"><span data-stu-id="982ef-132">The lower nibble gives the type of the value that needs to be extracted from memory:</span></span>

``` syntax
FC_LONG | FC_ULONG | 
FC_SHORT | FC_USHORT | 
FC_SMALL | FC_USMALL | 
FC_HYPER
```

> [!Note]
> <span data-ttu-id="982ef-133">不支援64位運算式。</span><span class="sxs-lookup"><span data-stu-id="982ef-133">64-bit expressions are not supported.</span></span> <span data-ttu-id="982ef-134">\_只有在64位平臺上 **\_ () IID** 才能將 iid 的指標值解壓縮時，才會使用 FC hyper-v \* 。</span><span class="sxs-lookup"><span data-stu-id="982ef-134">FC\_HYPER is used only for **iid\_is()** on 64-bit platforms to extract the pointer value for IID\*.</span></span>
>
> <span data-ttu-id="982ef-135">編譯器會在下列情況下，將類型半值設定為零：上述常數運算式以及需要呼叫評估運算式常式（例如，當 \_ 使用 fc 常數 \_ 一致性和 fc 回呼時） \_ 。</span><span class="sxs-lookup"><span data-stu-id="982ef-135">The compiler sets the type nibble to zero for the following cases: constant expression mentioned above and when evaluation expression routine needs to be called, for example, when FC\_CONSTANT\_CONFORMANCE and FC\_CALLBACK are used.</span></span>

 

<span data-ttu-id="982ef-136">大小 \_ 為 \_ op<1> 欄位允許將下列其中一項作業套用至一致性變數：</span><span class="sxs-lookup"><span data-stu-id="982ef-136">The size\_is\_op<1> field allows for one of the following operations to be applied to the conformance variable:</span></span>

``` syntax
FC_DEREFERENCE | 
FC_DIV_2 | FC_MULT_2 | FC_SUB_1 | FC_ADD_1 | 
FC_CALLBACK
```

<span data-ttu-id="982ef-137">FC 取值 \_ 常數用於相互關聯的 pointee，例如 **\[ 大小 \_ 是 (\* pL) \]**。</span><span class="sxs-lookup"><span data-stu-id="982ef-137">The FC\_DEREFERENCE constant is used for correlation being a pointee, like for **\[size\_is(\*pL)\]**.</span></span> <span data-ttu-id="982ef-138">算術運算子只會使用指定的常數。</span><span class="sxs-lookup"><span data-stu-id="982ef-138">Arithmetic operators just use the indicated constant.</span></span> <span data-ttu-id="982ef-139">FC \_ 回呼常數表示需要呼叫運算式評估常式。</span><span class="sxs-lookup"><span data-stu-id="982ef-139">The FC\_CALLBACK constant indicates that an expression evaluation routine needs to be called.</span></span>

<span data-ttu-id="982ef-140">Offset<2> 欄位通常是運算式引數變數的相對記憶體位移。</span><span class="sxs-lookup"><span data-stu-id="982ef-140">The offset<2> field is typically a relative memory offset to the expression argument variable.</span></span> <span data-ttu-id="982ef-141">它也可以是運算式評估–常式索引。</span><span class="sxs-lookup"><span data-stu-id="982ef-141">It can also be an expression evaluation–routine index.</span></span> <span data-ttu-id="982ef-142">如本檔先前所述，針對常數運算式，它是實際的最終運算式值的一部分。</span><span class="sxs-lookup"><span data-stu-id="982ef-142">As mentioned previously in this document, for constant expressions it is a part of actual, final expression value.</span></span>

<span data-ttu-id="982ef-143">位移<2> 欄位為記憶體位移的解讀，取決於運算式的複雜度、運算式變數的位置，以及陣列的大小寫，不論陣列實際上是否為屬性化指標。</span><span class="sxs-lookup"><span data-stu-id="982ef-143">The interpretation of the offset<2> field as memory offset depends on the complexity of the expression, the location of the expression variable, and in the case of an array, whether the array is actually an attributed pointer.</span></span>

<span data-ttu-id="982ef-144">如果陣列是屬性化指標，而一致性變數是結構中的欄位，則位移欄位包含從結構開頭到符合性描述欄位的位移。</span><span class="sxs-lookup"><span data-stu-id="982ef-144">If the array is an attributed pointer and the conformance variable is a field in a structure, the offset field contains the offset from the beginning of the structure to the conformance-describing field.</span></span> <span data-ttu-id="982ef-145">如果陣列不是屬性化指標，且一致性變數是結構中的欄位，則位移欄位包含從結構的 nonconformant 部分結尾到符合性描述欄位的位移。</span><span class="sxs-lookup"><span data-stu-id="982ef-145">If the array is not an attributed pointer and the conformance variable is a field in a structure, the offset field contains the offset from the end of the nonconformant part of the structure to the conformance-describing field.</span></span> <span data-ttu-id="982ef-146">一般來說，符合標準的陣列位於結構的結尾。</span><span class="sxs-lookup"><span data-stu-id="982ef-146">Typically, the conformant array is at the end of the structure.</span></span>

<span data-ttu-id="982ef-147">針對最上層的一致性，offset 欄位包含從存根的第一個參數在堆疊上的位置到描述一致性之參數的位移。</span><span class="sxs-lookup"><span data-stu-id="982ef-147">For top-level conformance, the offset field contains the offset from the stub's first parameter's location on the stack to the parameter that describes the conformance.</span></span> <span data-ttu-id="982ef-148">這不會用在 **–作業系統** 模式中。</span><span class="sxs-lookup"><span data-stu-id="982ef-148">This is not used in **–Os** mode.</span></span> <span data-ttu-id="982ef-149">位移欄位的解釋還有其他例外狀況;這些類型的描述中會說明這類例外狀況。</span><span class="sxs-lookup"><span data-stu-id="982ef-149">There are other exceptions to the interpretation of the offset field; such exceptions are described in the description of those types.</span></span>

<span data-ttu-id="982ef-150">當 offset<2> 用於 FC 回呼時 \_ ，它會在編譯器所產生的運算式評估常式資料表中包含索引。</span><span class="sxs-lookup"><span data-stu-id="982ef-150">When offset<2> is used with FC\_CALLBACK, it contains an index in the expression evaluation routine table generated by the compiler.</span></span> <span data-ttu-id="982ef-151">存根訊息會傳遞至評估常式，然後計算一致性值，並將它指派給存根訊息的 MaxCount 欄位。</span><span class="sxs-lookup"><span data-stu-id="982ef-151">The stub message is passed to the evaluation routine, which then computes the conformance value and assigns it to the MaxCount field of the stub message.</span></span>

<span data-ttu-id="982ef-152">已 \_ 新增 Windows 2000 的健全旗標<2> 欄位以支援 [**/robust**](/windows/desktop/Midl/-robust)，例如拒絕攻擊功能。</span><span class="sxs-lookup"><span data-stu-id="982ef-152">The robust\_flags<2> field has been added for Windows 2000 to support [**/robust**](/windows/desktop/Midl/-robust), such as the denial-of-attacks feature.</span></span> <span data-ttu-id="982ef-153">第一個位元組定義了下列旗標：</span><span class="sxs-lookup"><span data-stu-id="982ef-153">The following flags are defined on the first byte:</span></span>

``` syntax
typedef  struct  _NDR_CORRELATION_FLAGS
  {
  unsigned char   Early     : 1;
  unsigned char   Split     : 1;
  unsigned char   IsIidIs   : 1;
  unsigned char   DontCheck : 1;
  unsigned char   Unused    : 4;
  } NDR_CORRELATION_FLAGS;
```

<span data-ttu-id="982ef-154">早期旗標表示早期與晚期關聯。</span><span class="sxs-lookup"><span data-stu-id="982ef-154">The Early flag indicates early versus late correlation.</span></span> <span data-ttu-id="982ef-155">早期關聯性是指運算式引數在所述引數的前面，例如，size 引數是在調整大小的指標引數之前。</span><span class="sxs-lookup"><span data-stu-id="982ef-155">An early correlation is when the expression argument precedes the described argument, for example a size argument is before a sized pointer argument.</span></span> <span data-ttu-id="982ef-156">當運算式引數位於相關引數之後時，就會使用晚期關聯。</span><span class="sxs-lookup"><span data-stu-id="982ef-156">A late correlation is when the expression argument comes after the related argument.</span></span> <span data-ttu-id="982ef-157">引擎會立即執行早期關聯值的驗證，並儲存延遲的相互關聯值，以便在封送處理完成之後檢查。</span><span class="sxs-lookup"><span data-stu-id="982ef-157">The engine performs validation of early correlation values right away, the late correlation values are stored for checking after unmarshaling is done.</span></span>

<span data-ttu-id="982ef-158">分割旗標表示 \[ 在 in \] 和 \[ out \] 引數之間進行非同步分割。</span><span class="sxs-lookup"><span data-stu-id="982ef-158">The Split flag indicates an async split among \[in\] and \[out\] arguments.</span></span> <span data-ttu-id="982ef-159">例如，大小的引數可能是 \[ ， \] 而調整大小的指標可能會 \[ 輸出 \] 。</span><span class="sxs-lookup"><span data-stu-id="982ef-159">For example, a size argument may be \[in\] while the sized pointer may be \[out\].</span></span> <span data-ttu-id="982ef-160">在 DCOM 非同步內容中，這些引數會出現在不同的堆疊上，因此引擎必須知道這一點。</span><span class="sxs-lookup"><span data-stu-id="982ef-160">In the DCOM async context, these arguments happen to be on different stacks, so the engine must be aware of this.</span></span>

<span data-ttu-id="982ef-161">IsIidIs 旗標表示 **iid \_ ()** 相互關聯。</span><span class="sxs-lookup"><span data-stu-id="982ef-161">The IsIidIs flag indicates an **iid\_is()** correlation.</span></span> <span data-ttu-id="982ef-162">NdrComputeConformance 常式會被欺騙，以運算式值的形式取得 IID 的指標，但驗證常式無法比較這類值 (它們會是指標) ，因此旗標表示需要比較實際的 Iid。</span><span class="sxs-lookup"><span data-stu-id="982ef-162">The NdrComputeConformance routine is tricked to obtain a pointer to IID as an expression value, but the validation routine cannot compare such values (they would be pointers) and so the flag indicates that actual IIDs need to be compared.</span></span>

### <a name="variance-description-and-other-array-attributes"></a><span data-ttu-id="982ef-163">差異描述和其他陣列屬性</span><span class="sxs-lookup"><span data-stu-id="982ef-163">Variance Description and Other Array Attributes</span></span>

<span data-ttu-id="982ef-164">變異數描述欄位格式與 [一致性描述] 欄位相同。</span><span class="sxs-lookup"><span data-stu-id="982ef-164">The variance description field format is identical to the conformance description field.</span></span> <span data-ttu-id="982ef-165">差別在於，NDR 引擎會使用不同的存根訊息欄位作為暫存變數。</span><span class="sxs-lookup"><span data-stu-id="982ef-165">The difference is that a different stub message field is used by the NDR engine as a temporary variable.</span></span> <span data-ttu-id="982ef-166">在變異數描述的案例中，這是評估的長度，而且對應的欄位稱為 ActualLength。</span><span class="sxs-lookup"><span data-stu-id="982ef-166">In the case of variance description, it is the length that is evaluated and the corresponding field is called ActualLength.</span></span>

<span data-ttu-id="982ef-167">使用變異數時，起始位移通常為零，且引擎會據以調整。</span><span class="sxs-lookup"><span data-stu-id="982ef-167">With variance, the starting offset is typically zero and the engine is tuned accordingly.</span></span> <span data-ttu-id="982ef-168">如果 **第一個 \_ 是 ()** 屬性套用至一致的不同陣列，則會強制執行運算式評估常式的回呼。</span><span class="sxs-lookup"><span data-stu-id="982ef-168">If the **first\_is()** attribute is applied to a conformant varying array, a callback to an expression evaluation routine is forced.</span></span>

 

 