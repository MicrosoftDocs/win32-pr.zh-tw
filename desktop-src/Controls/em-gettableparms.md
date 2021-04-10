---
title: 'EM_GETTABLEPARMS 訊息 (Richedit .h) '
description: 抓取資料表資料列的資料表參數，以及指定之資料格數目的資料格參數。
ms.assetid: 36ADA41B-735B-4D6E-92B1-33260C71DF73
keywords:
- EM_GETTABLEPARMS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7eb244b64258b1cf83559e21affea51b1d0c5d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843483"
---
# <a name="em_gettableparms-message"></a><span data-ttu-id="82715-104">EM \_ GETTABLEPARMS 訊息</span><span class="sxs-lookup"><span data-stu-id="82715-104">EM\_GETTABLEPARMS message</span></span>

<span data-ttu-id="82715-105">抓取資料表資料列的資料表參數，以及指定之資料格數目的資料格參數。</span><span class="sxs-lookup"><span data-stu-id="82715-105">Retrieves the table parameters for a table row and the cell parameters for the specified number of cells.</span></span>


```C++
#define EM_GETTABLEPARMS       (WM_USER + 265)
```



## <a name="parameters"></a><span data-ttu-id="82715-106">參數</span><span class="sxs-lookup"><span data-stu-id="82715-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82715-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="82715-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82715-108">[**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="82715-108">A pointer to a [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span>

</dd> <dt>

<span data-ttu-id="82715-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="82715-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82715-110">[**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="82715-110">A pointer to a [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82715-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="82715-111">Return value</span></span>

<span data-ttu-id="82715-112">\_如果成功，則傳回 S OK，或下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="82715-112">Returns S\_OK if successful, or one of the following error codes.</span></span>



| <span data-ttu-id="82715-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="82715-113">Return code</span></span>                                                                                    | <span data-ttu-id="82715-114">Description</span><span class="sxs-lookup"><span data-stu-id="82715-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="82715-115"><dt>**E \_失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="82715-115"><dt>**E\_FAIL** </dt></span></span> </dl>        | <span data-ttu-id="82715-116">無法進行變更。</span><span class="sxs-lookup"><span data-stu-id="82715-116">Changes cannot be made.</span></span> <span data-ttu-id="82715-117">如果控制項是純文字或單行控制項，或插入點位於數學物件內，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="82715-117">This can occur if the control is a plain-text or single-line control, or if the insertion point is inside a math object.</span></span> <span data-ttu-id="82715-118">如果 [**EM \_ SETEDITSTYLEEX**](em-seteditstyleex.md) 訊息設定了「SES」（ **\_ \_ 值得注意** 的值），則也會在停用資料表時進行。</span><span class="sxs-lookup"><span data-stu-id="82715-118">It also occurs if tables are disabled if the [**EM\_SETEDITSTYLEEX**](em-seteditstyleex.md) message sets the **SES\_EX\_NOTABLE** value.</span></span> <br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="82715-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="82715-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="82715-120">*WParam* 或 *lParam* 為 Null 或指向不正確結構。</span><span class="sxs-lookup"><span data-stu-id="82715-120">The *wParam* or *lParam* is NULL or points to an invalid structure.</span></span> <span data-ttu-id="82715-121">[**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)結構的 **cbRow** 成員必須等於 `sizeof(TABLEROWPARMS)` 或 sizeof (TABLEROWPARMS) 2 \* sizeof (long) 。</span><span class="sxs-lookup"><span data-stu-id="82715-121">The **cbRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure must equal `sizeof(TABLEROWPARMS)` or sizeof(TABLEROWPARMS)   2\*sizeof(long).</span></span> <span data-ttu-id="82715-122">第二個值是 RichEdit 4.1 **TABLEROWPARMS** 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="82715-122">The latter value is the size of the RichEdit 4.1 **TABLEROWPARMS** structure.</span></span> <span data-ttu-id="82715-123">**TABLEROWPARMS** 結構的 **cbCell** 成員必須相等 `sizeof(TABLECELLPARMS)` 。</span><span class="sxs-lookup"><span data-stu-id="82715-123">The **cbCell** member of the **TABLEROWPARMS** structure must equal `sizeof(TABLECELLPARMS)`.</span></span> <span data-ttu-id="82715-124">查詢字元位置必須是資料表資料列分隔符號。</span><span class="sxs-lookup"><span data-stu-id="82715-124">The query character position must be at a table row delimiter.</span></span> |
| <dl> <span data-ttu-id="82715-125"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="82715-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl> | <span data-ttu-id="82715-126">可用的記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="82715-126">Insufficient memory is available.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="82715-127">備註</span><span class="sxs-lookup"><span data-stu-id="82715-127">Remarks</span></span>

<span data-ttu-id="82715-128">這則訊息會取得 [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)結構的 **cpStartRow** 成員所指定的字元位置之資料列的資料表參數，以及 [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms)結構的 **cCells** 成員所指定的資料格數目。</span><span class="sxs-lookup"><span data-stu-id="82715-128">This message gets the table parameters for the row at the character position specified by the **cpStartRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure, and the number of cells specified by the **cCells** member of the [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

<span data-ttu-id="82715-129">[**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)結構的 **cpStartRow** 成員所指定的字元位置應該在資料表資料列的開頭，或資料表資料列的結尾分隔符號。</span><span class="sxs-lookup"><span data-stu-id="82715-129">The character position specified by the **cpStartRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure should be at the start of the table row, or at the end delimiter of the table row.</span></span> <span data-ttu-id="82715-130">如果 **cpStartRow** 設定為1，則字元位置會由目前的選取範圍指定。</span><span class="sxs-lookup"><span data-stu-id="82715-130">If **cpStartRow** is set to  1, the character position is given by the current selection.</span></span> <span data-ttu-id="82715-131">在這種情況下，請將選取範圍放在資料列的結尾 (在資料表資料列的資料格標記與結束分隔符號之間) ，或選取資料列。</span><span class="sxs-lookup"><span data-stu-id="82715-131">In this case, position the selection at the end of the row (between the cell mark and the end delimiter of the table row), or select the row.</span></span>

## <a name="requirements"></a><span data-ttu-id="82715-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="82715-132">Requirements</span></span>



| <span data-ttu-id="82715-133">需求</span><span class="sxs-lookup"><span data-stu-id="82715-133">Requirement</span></span> | <span data-ttu-id="82715-134">值</span><span class="sxs-lookup"><span data-stu-id="82715-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82715-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="82715-135">Minimum supported client</span></span><br/> | <span data-ttu-id="82715-136">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82715-136">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="82715-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="82715-137">Minimum supported server</span></span><br/> | <span data-ttu-id="82715-138">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82715-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="82715-139">標頭</span><span class="sxs-lookup"><span data-stu-id="82715-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="82715-140"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="82715-140"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82715-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82715-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82715-142">**EM \_ SETTABLEPARMS**</span><span class="sxs-lookup"><span data-stu-id="82715-142">**EM\_SETTABLEPARMS**</span></span>](em-settableparms.md)
</dt> </dl>

 

 





