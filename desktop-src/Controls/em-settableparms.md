---
title: 'EM_SETTABLEPARMS 訊息 (Richedit .h) '
description: 變更資料表中資料列的參數。
ms.assetid: 6CE9B8D1-68C9-4692-8454-24BC81E9038F
keywords:
- EM_SETTABLEPARMS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86fa77774bd7fcf461fc74b479a57304a5f8ee3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934207"
---
# <a name="em_settableparms-message"></a><span data-ttu-id="25748-104">EM \_ SETTABLEPARMS 訊息</span><span class="sxs-lookup"><span data-stu-id="25748-104">EM\_SETTABLEPARMS message</span></span>

<span data-ttu-id="25748-105">變更資料表中資料列的參數。</span><span class="sxs-lookup"><span data-stu-id="25748-105">Changes the parameters of rows in a table.</span></span>

## <a name="parameters"></a><span data-ttu-id="25748-106">參數</span><span class="sxs-lookup"><span data-stu-id="25748-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25748-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="25748-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25748-108">[**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="25748-108">A pointer to a [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span>

</dd> <dt>

<span data-ttu-id="25748-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25748-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25748-110">[**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="25748-110">A pointer to a [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25748-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="25748-111">Return value</span></span>

<span data-ttu-id="25748-112">\_如果成功，則傳回 S OK，或下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="25748-112">Returns S\_OK if successful, or one of the following error codes.</span></span>



| <span data-ttu-id="25748-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="25748-113">Return code</span></span>                                                                                    | <span data-ttu-id="25748-114">Description</span><span class="sxs-lookup"><span data-stu-id="25748-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="25748-115"><dt>**E \_失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="25748-115"><dt>**E\_FAIL** </dt></span></span> </dl>        | <span data-ttu-id="25748-116">無法進行變更。</span><span class="sxs-lookup"><span data-stu-id="25748-116">Changes cannot be made.</span></span> <span data-ttu-id="25748-117">如果控制項是純文字或單行控制項，或插入點位於數學物件內，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="25748-117">This can occur if the control is a plain-text or single-line control, or if the insertion point is inside a math object.</span></span> <span data-ttu-id="25748-118">如果停用資料表，或者 [**EM \_ SETEDITSTYLEEX**](em-seteditstyleex.md) 訊息設定了 **SES 的 \_ \_ 值得注意** 的值，也會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="25748-118">It also occurs if tables are disabled, or if the [**EM\_SETEDITSTYLEEX**](em-seteditstyleex.md) message sets the **SES\_EX\_NOTABLE** value.</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="25748-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="25748-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="25748-120">*WParam* 或 *lParam* 為 Null 或指向不正確結構。</span><span class="sxs-lookup"><span data-stu-id="25748-120">The *wParam* or *lParam* is NULL or points to an invalid structure.</span></span> <span data-ttu-id="25748-121">[**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)結構的 **cCell** 成員必須至少為1，且不能超過63。</span><span class="sxs-lookup"><span data-stu-id="25748-121">The **cCell** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure must be at least 1 and not more than 63.</span></span> <span data-ttu-id="25748-122">**CbRow** 成員必須等於 `sizeof(TABLEROWPARMS)` 或 `sizeof(TABLEROWPARMS)   2*sizeof(long)` 。</span><span class="sxs-lookup"><span data-stu-id="25748-122">The **cbRow** member must equal `sizeof(TABLEROWPARMS)` or `sizeof(TABLEROWPARMS)   2*sizeof(long)`.</span></span> <span data-ttu-id="25748-123">第二個值是 RichEdit 4.1 **TABLEROWPARMS** 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="25748-123">The latter value is the size of the RichEdit 4.1 **TABLEROWPARMS** structure.</span></span> <span data-ttu-id="25748-124">**TABLEROWPARMS** 的 **cbCell** 成員必須相等 `sizeof(TABLECELLPARMS)` 。</span><span class="sxs-lookup"><span data-stu-id="25748-124">The **cbCell** member of **TABLEROWPARMS** must equal `sizeof(TABLECELLPARMS)`.</span></span> <span data-ttu-id="25748-125">插入點必須在資料表的開頭或在資料表資料列內，而且資料格的數目只能變更一次。</span><span class="sxs-lookup"><span data-stu-id="25748-125">The insertion point must be at the start of a table or inside a table row, and the number of cells can only change by one.</span></span> |
| <dl> <span data-ttu-id="25748-126"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="25748-126"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl> | <span data-ttu-id="25748-127">可用的記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="25748-127">Insufficient memory is available.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="25748-128">備註</span><span class="sxs-lookup"><span data-stu-id="25748-128">Remarks</span></span>

<span data-ttu-id="25748-129">如果資料表有多個連續的資料列，此訊息就會變更 [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)結構之 **魚尾紋** 成員所指定的資料列數目參數。</span><span class="sxs-lookup"><span data-stu-id="25748-129">This message changes the parameters of the number of rows specified by the **cRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure, if the table has that many consecutive rows.</span></span> <span data-ttu-id="25748-130">如果 **魚尾紋** 小於0，訊息會逐一查看到資料表的結尾。</span><span class="sxs-lookup"><span data-stu-id="25748-130">If **cRow** is less than 0, the message iterates until the end of the table.</span></span> <span data-ttu-id="25748-131">如果新的資料格計數與目前的資料格計數不同于 + 1 或1，它會插入或刪除 **TABLEROWPARMS** 的 **iCell** 成員所指定索引處的資料格。</span><span class="sxs-lookup"><span data-stu-id="25748-131">If the new cell count differs from the current cell count by +1 or  1, it inserts or deletes the cell at the index specified by the **iCell** member of **TABLEROWPARMS**.</span></span> <span data-ttu-id="25748-132">起始資料表資料列是由字元位置所識別。</span><span class="sxs-lookup"><span data-stu-id="25748-132">The starting table row is identified by a character position.</span></span> <span data-ttu-id="25748-133">這個位置是由值大於或等於零的 **cpStartRow** 成員所指定。</span><span class="sxs-lookup"><span data-stu-id="25748-133">This position is specified by **cpStartRow** members with values that are greater than or equal to zero.</span></span> <span data-ttu-id="25748-134">除非您想要變更該資料表的參數，否則位置應該在資料表資料列中，但不能在嵌套的資料表內。</span><span class="sxs-lookup"><span data-stu-id="25748-134">The position should be inside the table row, but not inside a nested table, unless you want to change that table s parameters.</span></span> <span data-ttu-id="25748-135">如果 **cpStartRow** 成員是1，則會由目前的選取範圍來指定字元位置。</span><span class="sxs-lookup"><span data-stu-id="25748-135">If the **cpStartRow** member is  1, the character position is given by the current selection.</span></span> <span data-ttu-id="25748-136">若要這樣做，請將選取範圍放在資料表資料列內的任何位置，或選取在資料表資料列結尾有選取範圍的有效資料列。</span><span class="sxs-lookup"><span data-stu-id="25748-136">For this, position the selection anywhere inside the table row, or select the row with the active end of the selection at the end of the table row.</span></span>

## <a name="requirements"></a><span data-ttu-id="25748-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="25748-137">Requirements</span></span>



| <span data-ttu-id="25748-138">需求</span><span class="sxs-lookup"><span data-stu-id="25748-138">Requirement</span></span> | <span data-ttu-id="25748-139">值</span><span class="sxs-lookup"><span data-stu-id="25748-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25748-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="25748-140">Minimum supported client</span></span><br/> | <span data-ttu-id="25748-141">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25748-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="25748-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="25748-142">Minimum supported server</span></span><br/> | <span data-ttu-id="25748-143">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25748-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="25748-144">標頭</span><span class="sxs-lookup"><span data-stu-id="25748-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="25748-145"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="25748-145"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25748-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25748-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25748-147">**EM \_ GETTABLEPARMS**</span><span class="sxs-lookup"><span data-stu-id="25748-147">**EM\_GETTABLEPARMS**</span></span>](em-gettableparms.md)
</dt> </dl>

 

 





