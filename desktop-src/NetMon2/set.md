---
description: SET 結構會定義一組值。
ms.assetid: 88e0ffa1-71a2-4a3f-bdf1-964de0adea62
title: '將結構設定 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: fdefc6f1233f820321bae6795f457e345fb5d4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192773"
---
# <a name="set-structure"></a><span data-ttu-id="1ddbd-103">設定結構</span><span class="sxs-lookup"><span data-stu-id="1ddbd-103">SET structure</span></span>

<span data-ttu-id="1ddbd-104">**Set** 結構會定義一組值。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-104">The **SET** structure defines a set of values.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ddbd-105">語法</span><span class="sxs-lookup"><span data-stu-id="1ddbd-105">Syntax</span></span>


```C++
typedef struct _SET {
  DWORD nEntries;
  union {
    LPBYTE               lpByteTable;
    LPWORD               lpWordTable;
    LPDWORD              lpDwordTable;
    LPLARGEINT           lpLargeIntTable;
    LPSYSTEMTIME         lpSystemTimeTable;
    LPLABELED_BYTE       lpLabeledByteTable;
    LPLABELED_WORD       lpLabeledWordTable;
    LPLABELED_DWORD      lpLabeledDwordTable;
    LPLABELED_LARGEINT   lpLabeledLargeIntTable;
    LPLABELED_SYSTEMTIME lpLabeledSystemTimeTable;
    LPLABELED_BIT        lpLabeledBit;
    LPVOID               lpVoidTable;
  };
} SET, *LPSET;
```



## <a name="members"></a><span data-ttu-id="1ddbd-106">成員</span><span class="sxs-lookup"><span data-stu-id="1ddbd-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1ddbd-107">**nEntries**</span><span class="sxs-lookup"><span data-stu-id="1ddbd-107">**nEntries**</span></span>
</dt> <dd>

<span data-ttu-id="1ddbd-108">集合中的總專案數。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-108">Total number of entries in a set.</span></span>

</dd> <dt>

<span data-ttu-id="1ddbd-109">**lpByteTable**</span><span class="sxs-lookup"><span data-stu-id="1ddbd-109">**lpByteTable**</span></span>
</dt> <dd>

<span data-ttu-id="1ddbd-110">位元組值陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-110">Pointer to an array of BYTE values.</span></span>

</dd> <dt>

<span data-ttu-id="1ddbd-111">**lpWordTable**</span><span class="sxs-lookup"><span data-stu-id="1ddbd-111">**lpWordTable**</span></span>
</dt> <dd>

<span data-ttu-id="1ddbd-112">文字值陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-112">Pointer to an array of WORD values.</span></span>

</dd> <dt>

<span data-ttu-id="1ddbd-113">**lpDwordTable**</span><span class="sxs-lookup"><span data-stu-id="1ddbd-113">**lpDwordTable**</span></span>
</dt> <dd>

<span data-ttu-id="1ddbd-114">DWORD 值陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-114">Pointer to an array of DWORD values.</span></span>

</dd> <dt>

<span data-ttu-id="1ddbd-115">**lpLargeIntTable**</span><span class="sxs-lookup"><span data-stu-id="1ddbd-115">**lpLargeIntTable**</span></span>
</dt> <dd>

<span data-ttu-id="1ddbd-116">[LARGEINT](largeint.md)結構陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-116">Pointer to an array of [LARGEINT](largeint.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="1ddbd-117">**lpSystemTimeTable**</span><span class="sxs-lookup"><span data-stu-id="1ddbd-117">**lpSystemTimeTable**</span></span>
</dt> <dd>

<span data-ttu-id="1ddbd-118">SYSTEMTIME 值陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-118">Pointer to an array of SYSTEMTIME values.</span></span>

</dd> <dt>

<span data-ttu-id="1ddbd-119">**lpLabeledByteTable**</span><span class="sxs-lookup"><span data-stu-id="1ddbd-119">**lpLabeledByteTable**</span></span>
</dt> <dd>

<span data-ttu-id="1ddbd-120">[標記之 \_ 位元組](labeled-byte.md)結構陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-120">Pointer to an array of [LABELED\_BYTE](labeled-byte.md) structures.</span></span> <span data-ttu-id="1ddbd-121">每個 **標示的 \_ 位元組** 結構都會定義值和標籤。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-121">Each **LABELED\_BYTE** structure defines a value and label.</span></span> <span data-ttu-id="1ddbd-122">如果在通訊協定封包中找到對應的值，網路監視器會顯示標籤。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-122">Network Monitor displays a label if it finds a corresponding value in the protocol packet.</span></span>

</dd> <dt>

<span data-ttu-id="1ddbd-123">**lpLabeledWordTable**</span><span class="sxs-lookup"><span data-stu-id="1ddbd-123">**lpLabeledWordTable**</span></span>
</dt> <dd>

<span data-ttu-id="1ddbd-124">[標記的 \_ 單字](labeled-word.md)結構陣列的指標，此陣列會定義一組文字值和標籤。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-124">Pointer to an array of [LABELED\_WORD](labeled-word.md) structures that define a set of WORD values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="1ddbd-125">**lpLabeledDwordTable**</span><span class="sxs-lookup"><span data-stu-id="1ddbd-125">**lpLabeledDwordTable**</span></span>
</dt> <dd>

<span data-ttu-id="1ddbd-126">[標記 \_ dword](labeled-dword.md)結構陣列的指標，該陣列會定義一組 dword 值和標籤。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-126">Pointer to an array of [LABELED\_DWORD](labeled-dword.md) structures that define a set of DWORD values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="1ddbd-127">**lpLabeledLargeIntTable**</span><span class="sxs-lookup"><span data-stu-id="1ddbd-127">**lpLabeledLargeIntTable**</span></span>
</dt> <dd>

<span data-ttu-id="1ddbd-128">[標記 \_ LARGEINT](labeled-largeint.md)結構陣列的指標，這些結構會定義一組 LARGEINT 值和標籤。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-128">Pointer to an array of [LABELED\_LARGEINT](labeled-largeint.md) structures that define a set of LARGEINT values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="1ddbd-129">**lpLabeledSystemTimeTable**</span><span class="sxs-lookup"><span data-stu-id="1ddbd-129">**lpLabeledSystemTimeTable**</span></span>
</dt> <dd>

<span data-ttu-id="1ddbd-130">[標記 \_ SYSTEMTIME](labeled-systemtime.md)結構陣列的指標，這些結構會定義一組系統值和標籤。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-130">Pointer to an array of [LABELED\_SYSTEMTIME](labeled-systemtime.md) structures that define a set of SYSTEM values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="1ddbd-131">**lpLabeledBit**</span><span class="sxs-lookup"><span data-stu-id="1ddbd-131">**lpLabeledBit**</span></span>
</dt> <dd>

<span data-ttu-id="1ddbd-132">[標記的 \_ 位](labeled-bit.md)結構陣列的指標，該陣列會定義一組標記的位配對。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-132">Pointer to an array of [LABELED\_BIT](labeled-bit.md) structures that define a set of labeled BIT pairs.</span></span> <span data-ttu-id="1ddbd-133">每個位都可以針對每個狀態指定兩個標籤 (0 或 1) 位。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-133">Each BIT can specify two labels   one label for each state (0 or 1) of the BIT.</span></span>

</dd> <dt>

<span data-ttu-id="1ddbd-134">**lpVoidTable**</span><span class="sxs-lookup"><span data-stu-id="1ddbd-134">**lpVoidTable**</span></span>
</dt> <dd>

<span data-ttu-id="1ddbd-135">值陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-135">Pointer to an array of values.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ddbd-136">備註</span><span class="sxs-lookup"><span data-stu-id="1ddbd-136">Remarks</span></span>

<span data-ttu-id="1ddbd-137">**Set** 結構是用來定義一組比較資料，網路監視器可以用來解讀通訊協定封包中的屬性值。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-137">The **SET** structure is used to define a set of comparison data that Network Monitor can use to interpret the value of a property in a protocol packet.</span></span> <span data-ttu-id="1ddbd-138">當需要比較資料集時，會在 [PROPERTYINFO](propertyinfo.md)結構的 **lpSet** 成員中指定 **set** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-138">When a set of comparison data is required, a pointer to the **SET** structure is specified in the **lpSet** member of the [PROPERTYINFO](propertyinfo.md) structure.</span></span>

<span data-ttu-id="1ddbd-139">剖析器 DLL 可以提供設定的值和標籤。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-139">The parser DLL can provide a value set and a label set.</span></span> <span data-ttu-id="1ddbd-140">您在 **集合** 結構中選取之 **聯集的** 成員會指向定義集合每個成員的結構陣列。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-140">The member of the **UNION** that you select in a **SET** structure points to an array of structures that define each member of a set.</span></span>

-   <span data-ttu-id="1ddbd-141">值集</span><span class="sxs-lookup"><span data-stu-id="1ddbd-141">Value set</span></span>

    <span data-ttu-id="1ddbd-142">當您想要網路監視器使用在通訊協定封包中找到的值來包含內建或非內建的指標時，就會使用值集。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-142">A value set is used when you want Network Monitor to include an in-set or not-in-set indicator with the value found in the protocol packet.</span></span> <span data-ttu-id="1ddbd-143">例如，如果指定了 DWORD 集合，網路監視器會顯示在通訊協定封包中找到之每個 DWORD 值的標籤，指出 DWORD 是或未在集合中指定。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-143">For example, if a DWORD set is specified, Network Monitor displays a label for each DWORD value found in the protocol packet, indicating that the DWORD is or is not specified in the set.</span></span>

    <span data-ttu-id="1ddbd-144">設定的值可以根據 BYTE、WORD、DWORD、LARGEINT 和 SYSTEMTIME 資料類型。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-144">A value set can be based on BYTE, WORD, DWORD, LARGEINT, and SYSTEMTIME data types.</span></span>

-   <span data-ttu-id="1ddbd-145">標籤集合</span><span class="sxs-lookup"><span data-stu-id="1ddbd-145">Label set</span></span>

    <span data-ttu-id="1ddbd-146">當您想要網路監視器顯示使用者定義的標籤，而不是集合中指定的屬性值時，會使用標籤集合。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-146">A label set is used when you want Network Monitor to display a user-defined label instead of the property values specified in a set.</span></span>

    <span data-ttu-id="1ddbd-147">標籤集可以根據位元組、字組、DWORD、LARGEINT、SYSTEMTIME 和位標籤配對來設定。</span><span class="sxs-lookup"><span data-stu-id="1ddbd-147">A label set can be based on BYTE, WORD, DWORD, LARGEINT, SYSTEMTIME and BIT label pairs.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ddbd-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ddbd-148">Requirements</span></span>



| <span data-ttu-id="1ddbd-149">需求</span><span class="sxs-lookup"><span data-stu-id="1ddbd-149">Requirement</span></span> | <span data-ttu-id="1ddbd-150">值</span><span class="sxs-lookup"><span data-stu-id="1ddbd-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1ddbd-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ddbd-151">Minimum supported client</span></span><br/> | <span data-ttu-id="1ddbd-152">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ddbd-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1ddbd-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ddbd-153">Minimum supported server</span></span><br/> | <span data-ttu-id="1ddbd-154">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ddbd-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1ddbd-155">標頭</span><span class="sxs-lookup"><span data-stu-id="1ddbd-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ddbd-156"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="1ddbd-156"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ddbd-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ddbd-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ddbd-158">標示為 \_ 位</span><span class="sxs-lookup"><span data-stu-id="1ddbd-158">LABELED\_BIT</span></span>](labeled-bit.md)
</dt> <dt>

[<span data-ttu-id="1ddbd-159">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="1ddbd-159">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> </dl>

 

 




