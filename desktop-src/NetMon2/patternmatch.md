---
description: PATTERNMATCH 結構會定義用來評估框架的模式元素。
ms.assetid: 3ad27197-92da-49e5-bb0e-daf54de6c54c
title: 'PATTERNMATCH 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATTERNMATCH
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 286a331f4baeb1dde79a720385c61606835248f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944518"
---
# <a name="patternmatch-structure"></a><span data-ttu-id="58862-103">PATTERNMATCH 結構</span><span class="sxs-lookup"><span data-stu-id="58862-103">PATTERNMATCH structure</span></span>

<span data-ttu-id="58862-104">**PATTERNMATCH** 結構會定義用來評估框架的模式元素。</span><span class="sxs-lookup"><span data-stu-id="58862-104">The **PATTERNMATCH** structure defines pattern elements used to evaluate a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="58862-105">語法</span><span class="sxs-lookup"><span data-stu-id="58862-105">Syntax</span></span>


```C++
typedef struct _PATTERNMATCH {
  DWORD        Flags;
  BYTE         OffsetBasis;
  GENERIC_PORT Port;
  WORD         Offset;
  WORD         Length;
  BYTE         PatternToMatch[MAX_PATTERN_LENGTH];
} PATTERNMATCH, *LPPATTERNMATCH;
```



## <a name="members"></a><span data-ttu-id="58862-106">成員</span><span class="sxs-lookup"><span data-stu-id="58862-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="58862-107">**旗標**</span><span class="sxs-lookup"><span data-stu-id="58862-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="58862-108">模式相符旗標：</span><span class="sxs-lookup"><span data-stu-id="58862-108">Pattern match flags:</span></span>



| <span data-ttu-id="58862-109">值</span><span class="sxs-lookup"><span data-stu-id="58862-109">Value</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="58862-110">意義</span><span class="sxs-lookup"><span data-stu-id="58862-110">Meaning</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="PATTERN_MATCH_FLAGS_NOT"></span><span id="pattern_match_flags_not"></span><dl> <span data-ttu-id="58862-111"><dt>**模式 \_比對 \_ 旗標 \_ 不**</dt>是 <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="58862-111"><dt>**PATTERN\_MATCH\_FLAGS\_NOT**</dt> <dt>0x00000001</dt></span></span> </dl>                                   | <span data-ttu-id="58862-112">設定時，此旗標會在適當的位置保留缺少指定模式的框架。</span><span class="sxs-lookup"><span data-stu-id="58862-112">When set, this flag retains frames that lack the specified pattern in the proper spot.</span></span><br/> |
| <span id="PATTERN_MATCH_FLAGS_PORT_SPECIFIED"></span><span id="pattern_match_flags_port_specified"></span><dl> <span data-ttu-id="58862-113"><dt>**模式 \_符合 \_ 旗標 \_ 埠 \_ 指定**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="58862-113"><dt>**PATTERN\_MATCH\_FLAGS\_PORT\_SPECIFIED**</dt> <dt>0x00000008</dt></span></span> </dl> | <span data-ttu-id="58862-114">搜尋埠號碼值。</span><span class="sxs-lookup"><span data-stu-id="58862-114">Seeks a port number value.</span></span><br/>                                                             |



 

</dd> <dt>

<span data-ttu-id="58862-115">**OffsetBasis**</span><span class="sxs-lookup"><span data-stu-id="58862-115">**OffsetBasis**</span></span>
</dt> <dd>

<span data-ttu-id="58862-116">Offset 的類型，可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="58862-116">Types of offset, which can be one of the following:</span></span>



| <span data-ttu-id="58862-117">值</span><span class="sxs-lookup"><span data-stu-id="58862-117">Value</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="58862-118">意義</span><span class="sxs-lookup"><span data-stu-id="58862-118">Meaning</span></span>                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="OFFSET_BASIS_RELATIVE_TO_FRAME"></span><span id="offset_basis_relative_to_frame"></span><dl> <span data-ttu-id="58862-119"><dt>**\_ \_ 相對 \_ 于框架的位移基準 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="58862-119"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_FRAME**</dt></span></span> </dl>                                         | <span data-ttu-id="58862-120">設定相對於框架開頭的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="58862-120">Sets an offset, in bytes, relative to start of the frame.</span></span><br/>                   |
| <span id="OFFSET_BASIS_RELATIVE_TO_EFFECTIVE_PROTOCOL"></span><span id="offset_basis_relative_to_effective_protocol"></span><dl> <span data-ttu-id="58862-121"><dt>**\_ \_ 相對 \_ 于 \_ 有效 \_ 通訊協定的位移**</dt></span><span class="sxs-lookup"><span data-stu-id="58862-121"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_EFFECTIVE\_PROTOCOL**</dt></span></span> </dl> | <span data-ttu-id="58862-122">設定相對於參考之通訊協定開頭的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="58862-122">Sets an offset, in bytes, relative to the start of the referenced protocol.</span></span><br/> |
| <span id="OFFSET_BASIS_RELATIVE_TO_IPX"></span><span id="offset_basis_relative_to_ipx"></span><dl> <span data-ttu-id="58862-123"><dt>**\_ \_ 相對 \_ 于 IPX 的位移基礎 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="58862-123"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_IPX**</dt></span></span> </dl>                                               | <span data-ttu-id="58862-124">設定相對於 IPX 的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="58862-124">Sets an offset, in bytes, only relative to IPX.</span></span><br/>                             |
| <span id="OFFSET_BASIS_RELATIVE_TO_IP"></span><span id="offset_basis_relative_to_ip"></span><dl> <span data-ttu-id="58862-125"><dt>**\_ \_ 相對 \_ 于 IP 的位移基準 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="58862-125"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_IP**</dt></span></span> </dl>                                                  | <span data-ttu-id="58862-126">設定相對於 IP 的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="58862-126">Sets an offset, in bytes, only relative to IP.</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="58862-127">**通訊埠**</span><span class="sxs-lookup"><span data-stu-id="58862-127">**Port**</span></span>
</dt> <dd>

<span data-ttu-id="58862-128">埠值（如果有指定）。</span><span class="sxs-lookup"><span data-stu-id="58862-128">Port value, if specified.</span></span>

</dd> <dt>

<span data-ttu-id="58862-129">**Offset**</span><span class="sxs-lookup"><span data-stu-id="58862-129">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="58862-130">相對於 **OffsetBasis** 的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="58862-130">The offset, in bytes, relative to the **OffsetBasis**.</span></span>

</dd> <dt>

<span data-ttu-id="58862-131">**長度**</span><span class="sxs-lookup"><span data-stu-id="58862-131">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="58862-132">相符模式的長度。</span><span class="sxs-lookup"><span data-stu-id="58862-132">Length of the matched pattern.</span></span>

</dd> <dt>

<span data-ttu-id="58862-133">**PatternToMatch**</span><span class="sxs-lookup"><span data-stu-id="58862-133">**PatternToMatch**</span></span>
</dt> <dd>

<span data-ttu-id="58862-134">要比對的模式。</span><span class="sxs-lookup"><span data-stu-id="58862-134">Pattern to match.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58862-135">備註</span><span class="sxs-lookup"><span data-stu-id="58862-135">Remarks</span></span>

<span data-ttu-id="58862-136">此結構是用來建立 capture 篩選器。</span><span class="sxs-lookup"><span data-stu-id="58862-136">This structure is used to construct a capture filter.</span></span> <span data-ttu-id="58862-137">如需有關如何執行此結構的詳細資訊，請參閱「 [捕獲篩選準則](capture-filters.md)」。</span><span class="sxs-lookup"><span data-stu-id="58862-137">For more information about implementing this structure, see [Capture Filters](capture-filters.md).</span></span>

<span data-ttu-id="58862-138">捕獲篩選最多可包含四個 **PATTERNMATCH** 結構。</span><span class="sxs-lookup"><span data-stu-id="58862-138">A capture filter can contain up to four **PATTERNMATCH** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="58862-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="58862-139">Requirements</span></span>



| <span data-ttu-id="58862-140">需求</span><span class="sxs-lookup"><span data-stu-id="58862-140">Requirement</span></span> | <span data-ttu-id="58862-141">值</span><span class="sxs-lookup"><span data-stu-id="58862-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="58862-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58862-142">Minimum supported client</span></span><br/> | <span data-ttu-id="58862-143">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58862-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="58862-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58862-144">Minimum supported server</span></span><br/> | <span data-ttu-id="58862-145">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58862-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="58862-146">標頭</span><span class="sxs-lookup"><span data-stu-id="58862-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="58862-147"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="58862-147"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58862-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58862-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58862-149">CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="58862-149">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




