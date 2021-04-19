---
description: CAPTUREFILTER 結構包含 capture 篩選資料。
ms.assetid: 773187c6-31c7-4439-850d-1dd43d42f701
title: 'CAPTUREFILTER 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILTER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 129575ba401aed0e78f52695a49139f4143c9c87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983710"
---
# <a name="capturefilter-structure"></a><span data-ttu-id="835d8-103">CAPTUREFILTER 結構</span><span class="sxs-lookup"><span data-stu-id="835d8-103">CAPTUREFILTER structure</span></span>

<span data-ttu-id="835d8-104">**CAPTUREFILTER** 結構包含 capture 篩選資料。</span><span class="sxs-lookup"><span data-stu-id="835d8-104">The **CAPTUREFILTER** structure contains capture filter data.</span></span>

## <a name="syntax"></a><span data-ttu-id="835d8-105">語法</span><span class="sxs-lookup"><span data-stu-id="835d8-105">Syntax</span></span>


```C++
typedef struct _CAPTUREFILTER {
  DWORD          FilterFlags;
  LPBYTE         lpSapTable;
  LPWORD         lpEtypeTable;
  WORD           nSaps;
  WORD           nEtypes;
  LPADDRESSTABLE AddressTable;
  EXPRESSION     FilterExpression;
  TRIGGER        Trigger;
  DWORD          nFrameBytesToCopy;
  RESERVED       Reserved;
} CAPTUREFILTER, *LPCAPTUREFILTER;
```



## <a name="members"></a><span data-ttu-id="835d8-106">成員</span><span class="sxs-lookup"><span data-stu-id="835d8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="835d8-107">**FilterFlags**</span><span class="sxs-lookup"><span data-stu-id="835d8-107">**FilterFlags**</span></span>
</dt> <dd>

<span data-ttu-id="835d8-108">描述 capture 篩選器內容的旗標。</span><span class="sxs-lookup"><span data-stu-id="835d8-108">Flags that describe the contents of the capture filter.</span></span>



| <span data-ttu-id="835d8-109">值</span><span class="sxs-lookup"><span data-stu-id="835d8-109">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="835d8-110">意義</span><span class="sxs-lookup"><span data-stu-id="835d8-110">Meaning</span></span>                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_SAPS"></span><span id="capturefilter_flags_include_all_saps"></span><dl> <span data-ttu-id="835d8-111"><dt>**CAPTUREFILTER \_旗標 \_ 包括 \_ 所有 \_ sap**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="835d8-111"><dt>**CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_SAPS**</dt> <dt>0x0001</dt></span></span> </dl>       | <span data-ttu-id="835d8-112">包含所有 Sap 作為可接受的框架。</span><span class="sxs-lookup"><span data-stu-id="835d8-112">Includes all SAPs as acceptable frames.</span></span><br/>  |
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_ETYPES"></span><span id="capturefilter_flags_include_all_etypes"></span><dl> <span data-ttu-id="835d8-113"><dt>**CAPTUREFILTER \_旗標 \_ 包含 \_ 所有 \_ ETYPES**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="835d8-113"><dt>**CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_ETYPES**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="835d8-114">將所有 Etypes 包含為可接受的框架。</span><span class="sxs-lookup"><span data-stu-id="835d8-114">Include all Etypes as acceptable frames.</span></span><br/> |
| <span id="CAPTUREFILTER_FLAGS_LOCAL_ONLY"></span><span id="capturefilter_flags_local_only"></span><dl> <span data-ttu-id="835d8-115"><dt>**CAPTUREFILTER \_旗 \_ 標 \_ 僅限本機**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="835d8-115"><dt>**CAPTUREFILTER\_FLAGS\_LOCAL\_ONLY**</dt> <dt>0x0008</dt></span></span> </dl>                          | <span data-ttu-id="835d8-116">無 P 模式</span><span class="sxs-lookup"><span data-stu-id="835d8-116">No P-mode</span></span><br/>                                |
| <span id="CAPTUREFILTER_FLAGS_KEEP_RAW"></span><span id="capturefilter_flags_keep_raw"></span><dl> <span data-ttu-id="835d8-117"><dt>**CAPTUREFILTER \_旗標 \_ 保留 \_ 原始**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="835d8-117"><dt>**CAPTUREFILTER\_FLAGS\_KEEP\_RAW**</dt> <dt>0x0020</dt></span></span> </dl>                                | <span data-ttu-id="835d8-118">保留 SMT 和權杖環形 MAC 框架。</span><span class="sxs-lookup"><span data-stu-id="835d8-118">Keep SMT and token ring MAC frames.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="835d8-119">**lpSapTable**</span><span class="sxs-lookup"><span data-stu-id="835d8-119">**lpSapTable**</span></span>
</dt> <dd>

<span data-ttu-id="835d8-120">SAP 值陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="835d8-120">Pointer to an array of SAP values.</span></span> <span data-ttu-id="835d8-121">此成員會指出傳遞至驅動程式的有效 SAP 值。</span><span class="sxs-lookup"><span data-stu-id="835d8-121">This member indicates the SAP values that are valid to pass to the driver.</span></span> <span data-ttu-id="835d8-122">如果 \_ 已設定 CAPTUREFILTER 旗標 \_ 包括 \_ 所有 \_ sap，則會變成例外狀況清單， (包含這些) 以外的所有 sap。</span><span class="sxs-lookup"><span data-stu-id="835d8-122">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_SAPS is set, this becomes an exception list (include all SAPS except these).</span></span>

</dd> <dt>

<span data-ttu-id="835d8-123">**lpEtypeTable**</span><span class="sxs-lookup"><span data-stu-id="835d8-123">**lpEtypeTable**</span></span>
</dt> <dd>

<span data-ttu-id="835d8-124">Etype 值陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="835d8-124">Pointer to an array of Etype values.</span></span> <span data-ttu-id="835d8-125">這會指出傳遞給驅動程式的這些 Etype 值都是有效的。</span><span class="sxs-lookup"><span data-stu-id="835d8-125">This indicates those Etype values that are valid to pass to the driver.</span></span> <span data-ttu-id="835d8-126">如果 \_ 已設定 CAPTUREFILTER 旗標，則會 \_ \_ \_ 變成例外清單， (包含這些) 以外的所有 ETYPES。</span><span class="sxs-lookup"><span data-stu-id="835d8-126">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_ETYPES is set, this becomes an exception list (include all Etypes except these).</span></span>

</dd> <dt>

<span data-ttu-id="835d8-127">**nSaps**</span><span class="sxs-lookup"><span data-stu-id="835d8-127">**nSaps**</span></span>
</dt> <dd>

<span data-ttu-id="835d8-128">SAP 資料表中的 sap 數目。</span><span class="sxs-lookup"><span data-stu-id="835d8-128">Number of SAPs in the SAP table.</span></span>

</dd> <dt>

<span data-ttu-id="835d8-129">**nEtypes**</span><span class="sxs-lookup"><span data-stu-id="835d8-129">**nEtypes**</span></span>
</dt> <dd>

<span data-ttu-id="835d8-130">Etype 資料表中的 Etypes 數目。</span><span class="sxs-lookup"><span data-stu-id="835d8-130">Number of Etypes in the Etype table.</span></span>

</dd> <dt>

<span data-ttu-id="835d8-131">**AddressTable**</span><span class="sxs-lookup"><span data-stu-id="835d8-131">**AddressTable**</span></span>
</dt> <dd>

<span data-ttu-id="835d8-132">位址資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="835d8-132">Name of the address table.</span></span>

</dd> <dt>

<span data-ttu-id="835d8-133">**FilterExpression**</span><span class="sxs-lookup"><span data-stu-id="835d8-133">**FilterExpression**</span></span>
</dt> <dd>

<span data-ttu-id="835d8-134">運算式結構。</span><span class="sxs-lookup"><span data-stu-id="835d8-134">An EXPRESSION structure.</span></span> <span data-ttu-id="835d8-135">這包含 capture 篩選器的模式比對部分。</span><span class="sxs-lookup"><span data-stu-id="835d8-135">This contains the pattern match portion of the capture filter.</span></span>

</dd> <dt>

<span data-ttu-id="835d8-136">**觸發程序**</span><span class="sxs-lookup"><span data-stu-id="835d8-136">**Trigger**</span></span>
</dt> <dd>

<span data-ttu-id="835d8-137">保留的。</span><span class="sxs-lookup"><span data-stu-id="835d8-137">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="835d8-138">**nFrameBytesToCopy**</span><span class="sxs-lookup"><span data-stu-id="835d8-138">**nFrameBytesToCopy**</span></span>
</dt> <dd>

<span data-ttu-id="835d8-139">如果此成員不是0，則會指定要保留每個框架的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="835d8-139">If this member is not 0, then it specifies how many bytes to keep of each frame received.</span></span> <span data-ttu-id="835d8-140">如果是0，則保留整個框架。</span><span class="sxs-lookup"><span data-stu-id="835d8-140">If it is 0, then keep the whole frame.</span></span>

</dd> <dt>

<span data-ttu-id="835d8-141">**已保留**</span><span class="sxs-lookup"><span data-stu-id="835d8-141">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="835d8-142">保留的。</span><span class="sxs-lookup"><span data-stu-id="835d8-142">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="835d8-143">備註</span><span class="sxs-lookup"><span data-stu-id="835d8-143">Remarks</span></span>

<span data-ttu-id="835d8-144">旗標、值和運算式的組合，會決定使用此結構資料的驅動程式將會傳遞哪些框架。</span><span class="sxs-lookup"><span data-stu-id="835d8-144">The combination of flags, values, and expressions determine which frames will be passed by the driver that uses this structure data.</span></span> <span data-ttu-id="835d8-145">如需有關如何執行 **CAPTUREFILTER** 結構的詳細資訊，請參閱 [Capture 篩選器](capture-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="835d8-145">For more information about implementing a **CAPTUREFILTER** structure, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="835d8-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="835d8-146">Requirements</span></span>



| <span data-ttu-id="835d8-147">需求</span><span class="sxs-lookup"><span data-stu-id="835d8-147">Requirement</span></span> | <span data-ttu-id="835d8-148">值</span><span class="sxs-lookup"><span data-stu-id="835d8-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="835d8-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="835d8-149">Minimum supported client</span></span><br/> | <span data-ttu-id="835d8-150">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="835d8-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="835d8-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="835d8-151">Minimum supported server</span></span><br/> | <span data-ttu-id="835d8-152">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="835d8-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="835d8-153">標頭</span><span class="sxs-lookup"><span data-stu-id="835d8-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="835d8-154"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="835d8-154"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="835d8-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="835d8-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="835d8-156">ADDRESSTABLE</span><span class="sxs-lookup"><span data-stu-id="835d8-156">ADDRESSTABLE</span></span>](addresstable.md)
</dt> <dt>

[<span data-ttu-id="835d8-157">ADDRESSPAIR</span><span class="sxs-lookup"><span data-stu-id="835d8-157">ADDRESSPAIR</span></span>](addresspair.md)
</dt> <dt>

[<span data-ttu-id="835d8-158">表達</span><span class="sxs-lookup"><span data-stu-id="835d8-158">EXPRESSION</span></span>](expression.md)
</dt> <dt>

[<span data-ttu-id="835d8-159">ANDEXP</span><span class="sxs-lookup"><span data-stu-id="835d8-159">ANDEXP</span></span>](andexp.md)
</dt> <dt>

[<span data-ttu-id="835d8-160">PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="835d8-160">PATTERNMATCH</span></span>](patternmatch.md)
</dt> </dl>

 

 




