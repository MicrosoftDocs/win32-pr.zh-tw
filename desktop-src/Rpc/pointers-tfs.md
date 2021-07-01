---
title: 'RPC (的指標) '
description: 瞭解 RPC 一般指標，其定義為介面指標和位元組計數指標以外的所有專案。
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade676610a310e230eb6fa89dd666996bb82040f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119703"
---
# <a name="pointers-rpc"></a><span data-ttu-id="d500d-103">RPC (的指標) </span><span class="sxs-lookup"><span data-stu-id="d500d-103">Pointers (RPC)</span></span>

## <a name="common-pointers"></a><span data-ttu-id="d500d-104">一般指標</span><span class="sxs-lookup"><span data-stu-id="d500d-104">Common Pointers</span></span>

<span data-ttu-id="d500d-105">一般指標會定義為介面指標和位元組計數指標以外的所有專案。</span><span class="sxs-lookup"><span data-stu-id="d500d-105">A common pointer is defined as everything other than interface pointers and byte count pointers.</span></span>

<span data-ttu-id="d500d-106">描述有兩個可能的版面配置：</span><span class="sxs-lookup"><span data-stu-id="d500d-106">There are two possible layouts for the description:</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
simple_type<1> FC_PAD
```

<span data-ttu-id="d500d-107">–或–</span><span class="sxs-lookup"><span data-stu-id="d500d-107">–or–</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
offset_to_complex_description<2>
```

<span data-ttu-id="d500d-108">如果指標是簡單類型或 nonsized 字串指標的指標，則會使用第一個格式。</span><span class="sxs-lookup"><span data-stu-id="d500d-108">The first format is used if the pointer is a pointer to a simple type or a nonsized string pointer.</span></span> <span data-ttu-id="d500d-109">第二種格式是用於所有其他類型的指標。</span><span class="sxs-lookup"><span data-stu-id="d500d-109">The second format is used for pointers to all other types.</span></span> <span data-ttu-id="d500d-110">指標屬性會使用 FC \_ 簡單指標旗標來指出描述的版面配置 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d500d-110">Pointer attributes indicate which description layout it is with the FC\_SIMPLE\_POINTER flag.</span></span>

<span data-ttu-id="d500d-111">指標 \_ 類型<1> 是下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="d500d-111">pointer\_type<1> is one of the following.</span></span>



| <span data-ttu-id="d500d-112">格式字元</span><span class="sxs-lookup"><span data-stu-id="d500d-112">Format character</span></span> | <span data-ttu-id="d500d-113">說明</span><span class="sxs-lookup"><span data-stu-id="d500d-113">Description</span></span>                              |
|------------------|------------------------------------------|
| <span data-ttu-id="d500d-114">FC \_ RP</span><span class="sxs-lookup"><span data-stu-id="d500d-114">FC\_RP</span></span>           | <span data-ttu-id="d500d-115">參考指標。</span><span class="sxs-lookup"><span data-stu-id="d500d-115">A reference pointer.</span></span>                     |
| <span data-ttu-id="d500d-116">FC \_ UP</span><span class="sxs-lookup"><span data-stu-id="d500d-116">FC\_UP</span></span>           | <span data-ttu-id="d500d-117">唯一指標。</span><span class="sxs-lookup"><span data-stu-id="d500d-117">A unique pointer.</span></span>                        |
| <span data-ttu-id="d500d-118">FC \_ FP</span><span class="sxs-lookup"><span data-stu-id="d500d-118">FC\_FP</span></span>           | <span data-ttu-id="d500d-119">完整指標。</span><span class="sxs-lookup"><span data-stu-id="d500d-119">A full pointer.</span></span>                          |
| <span data-ttu-id="d500d-120">FC \_ OP</span><span class="sxs-lookup"><span data-stu-id="d500d-120">FC\_OP</span></span>           | <span data-ttu-id="d500d-121">物件介面中的唯一指標。</span><span class="sxs-lookup"><span data-stu-id="d500d-121">A unique pointer in an object interface.</span></span> |



 

<span data-ttu-id="d500d-122">區分 FC OP 的原因 \_ 是語義：在物件介面中，必須 \[ 先釋出 in、out 指標，然後 \] 才能將新的物件封送至新的物件，並指派新的指標值。</span><span class="sxs-lookup"><span data-stu-id="d500d-122">The reason to distinguish FC\_OP is semantic: in object interfaces, an \[in,out\] pointer should be freed before unmarshaling a new object and assigning a new pointer value.</span></span>

<span data-ttu-id="d500d-123">指標 \_ 屬性<1> 可以有下表所示的任何旗標。</span><span class="sxs-lookup"><span data-stu-id="d500d-123">Pointer\_attributes<1> can have any of the flags shown in the following table.</span></span>



| <span data-ttu-id="d500d-124">屬性</span><span class="sxs-lookup"><span data-stu-id="d500d-124">Attribute</span></span> | <span data-ttu-id="d500d-125">旗標</span><span class="sxs-lookup"><span data-stu-id="d500d-125">Flag</span></span>              | <span data-ttu-id="d500d-126">描述</span><span class="sxs-lookup"><span data-stu-id="d500d-126">Description</span></span>                                                                                                                                                                                                                                      |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d500d-127">01</span><span class="sxs-lookup"><span data-stu-id="d500d-127">01</span></span>   | <span data-ttu-id="d500d-128">FC \_ 配置 \_ 所有 \_ 節點</span><span class="sxs-lookup"><span data-stu-id="d500d-128">FC\_ALLOCATE\_ALL\_NODES</span></span> | <span data-ttu-id="d500d-129">指標是配置 (所有 \_ 節點) 配置配置的一部分。</span><span class="sxs-lookup"><span data-stu-id="d500d-129">The pointer is a part of an allocate(all\_nodes) allocation scheme.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="d500d-130">02</span><span class="sxs-lookup"><span data-stu-id="d500d-130">02</span></span>   | <span data-ttu-id="d500d-131">FC \_ \_ 沒有任何可用</span><span class="sxs-lookup"><span data-stu-id="d500d-131">FC\_DONT\_FREE</span></span>           | <span data-ttu-id="d500d-132">配置 (不會 \_ 釋放) 指標。</span><span class="sxs-lookup"><span data-stu-id="d500d-132">An allocate(dont\_free) pointer.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="d500d-133">04</span><span class="sxs-lookup"><span data-stu-id="d500d-133">04</span></span>   | <span data-ttu-id="d500d-134">\_ \_ 堆疊上的 FC ALLOCED \_</span><span class="sxs-lookup"><span data-stu-id="d500d-134">FC\_ALLOCED\_ON\_STACK</span></span>   | <span data-ttu-id="d500d-135">在存根的堆疊上配置其引用的指標。</span><span class="sxs-lookup"><span data-stu-id="d500d-135">A pointer whose referent is allocated on the stub's stack.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="d500d-136">08</span><span class="sxs-lookup"><span data-stu-id="d500d-136">08</span></span>   | <span data-ttu-id="d500d-137">FC \_ 簡單 \_ 指標</span><span class="sxs-lookup"><span data-stu-id="d500d-137">FC\_SIMPLE\_POINTER</span></span>      | <span data-ttu-id="d500d-138">簡單類型或 nonsized 符合標準之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="d500d-138">A pointer to a simple type or nonsized conformant string.</span></span> <span data-ttu-id="d500d-139">設定此旗標表示指標描述的版面配置是上述的簡單指標配置，否則會指出具有位移的描述項格式。</span><span class="sxs-lookup"><span data-stu-id="d500d-139">This flag being set indicates layout of the pointer description as the simple pointer layout described above, otherwise the descriptor format with the offset is indicated.</span></span> |
| <span data-ttu-id="d500d-140">10</span><span class="sxs-lookup"><span data-stu-id="d500d-140">10</span></span>   | <span data-ttu-id="d500d-141">FC \_ 指標 \_ DEREF</span><span class="sxs-lookup"><span data-stu-id="d500d-141">FC\_POINTER\_DEREF</span></span>       | <span data-ttu-id="d500d-142">必須先取值的指標，才能處理指標的參考。</span><span class="sxs-lookup"><span data-stu-id="d500d-142">A pointer that must be dereferenced before handling the pointer's referent.</span></span>                                                                                                                                                           |



 

<span data-ttu-id="d500d-143">具有 () 大小的指標 \_ 、最大值是 \_ () 、 \_ () 長度、最後一個 \_ () ，以及/或第一個 \_ 套用 () 套用至這些指標的格式字串描述與適當類型陣列的指標相同 (例如，如果大小為 () ，則符合標準的陣列 \_ ，如果大小為 () \_ 且長度為) \_ 。</span><span class="sxs-lookup"><span data-stu-id="d500d-143">Pointers that have size\_is(), max\_is(), length\_is(), last\_is(), and/or first\_is() applied to them have format string descriptions identical to a pointer to an array of the appropriate type (for example, a conformant array if size\_is() is applied, a conformant varying array if size\_is() and length\_is are applied).</span></span>

## <a name="interface-pointers"></a><span data-ttu-id="d500d-144">介面指標</span><span class="sxs-lookup"><span data-stu-id="d500d-144">Interface Pointers</span></span>

<span data-ttu-id="d500d-145">物件介面指標格式字串具有兩種格式的其中一種，取決於編譯器是否知道對應的 IID。</span><span class="sxs-lookup"><span data-stu-id="d500d-145">An object interface pointer format string has one of two formats, depending on whether the corresponding IID is known to the compiler.</span></span>

<span data-ttu-id="d500d-146">具有常數 IID 的介面指標具有下列描述：</span><span class="sxs-lookup"><span data-stu-id="d500d-146">An interface pointer with a constant IID has the following description:</span></span>

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

<span data-ttu-id="d500d-147">Iid<16> 部分是介面指標的實際 IID。</span><span class="sxs-lookup"><span data-stu-id="d500d-147">The iid<16> part is the actual IID for the interface pointer.</span></span> <span data-ttu-id="d500d-148">Iid 會以與 GUID 資料結構相同的格式寫入格式字串： long、short、short、char \[ 8 \] 。</span><span class="sxs-lookup"><span data-stu-id="d500d-148">The iid is written to the format string in a format identical to the GUID data structure: long, short, short, char \[8\].</span></span>

<span data-ttu-id="d500d-149">具有 iid 之介面指標的描述 \_ () 套用至：</span><span class="sxs-lookup"><span data-stu-id="d500d-149">The description of an interface pointer with iid\_is() applied to it is:</span></span>

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

<span data-ttu-id="d500d-150">Iid \_ 描述<> 是相互關聯描述項，而且有4或6個位元組，視是否使用 [**/robust**](/windows/desktop/Midl/-robust) 而定。</span><span class="sxs-lookup"><span data-stu-id="d500d-150">The iid\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="d500d-151">**NdrComputeConformance** 函數所計算的值是 IID 指標。</span><span class="sxs-lookup"><span data-stu-id="d500d-151">The value calculated by the **NdrComputeConformance** function is the IID pointer.</span></span>

## <a name="byte-count-pointers"></a><span data-ttu-id="d500d-152">位元組計數指標</span><span class="sxs-lookup"><span data-stu-id="d500d-152">Byte Count Pointers</span></span>

<span data-ttu-id="d500d-153">Byte count 指標與稱為 \[ **byte \_ count** 的特殊優化屬性相關 \] 。</span><span class="sxs-lookup"><span data-stu-id="d500d-153">Byte count pointers relate to a special optimization attribute called \[**byte\_count**\].</span></span> <span data-ttu-id="d500d-154">使用的格式如下：</span><span class="sxs-lookup"><span data-stu-id="d500d-154">The following formats are used:</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

<span data-ttu-id="d500d-155">還</span><span class="sxs-lookup"><span data-stu-id="d500d-155">–and –</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

<span data-ttu-id="d500d-156"><> 的位元組 \_ 計數 \_ 描述是相互關聯描述項，而且有4或6個位元組，視是否使用 [**/robust**](/windows/desktop/Midl/-robust) 而定。</span><span class="sxs-lookup"><span data-stu-id="d500d-156">The byte\_count\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

<span data-ttu-id="d500d-157">Pointee \_ 描述<> 是 pointee 類型的描述。</span><span class="sxs-lookup"><span data-stu-id="d500d-157">The pointee\_description<> is a description of the pointee type.</span></span>

 

 
