---
title: 'EM_INSERTTABLE 訊息 (Richedit .h) '
description: 插入一或多個具有空白資料格的相同資料表資料列。
ms.assetid: 7F9B2F28-1035-44AA-9DF6-57BC62886A4E
keywords:
- EM_INSERTTABLE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_INSERTTABLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea5de278df98e412f219d246164221cfea75255
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464533"
---
# <a name="em_inserttable-message"></a><span data-ttu-id="6805c-104">EM \_ INSERTTABLE 訊息</span><span class="sxs-lookup"><span data-stu-id="6805c-104">EM\_INSERTTABLE message</span></span>

<span data-ttu-id="6805c-105">插入一或多個具有空白資料格的相同資料表資料列。</span><span class="sxs-lookup"><span data-stu-id="6805c-105">Inserts one or more identical table rows with empty cells.</span></span>


```C++
#define EM_INSERTTABLE       (WM_USER + 232)
```



## <a name="parameters"></a><span data-ttu-id="6805c-106">參數</span><span class="sxs-lookup"><span data-stu-id="6805c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6805c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6805c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6805c-108">[**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6805c-108">A pointer to a [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6805c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6805c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6805c-110">[**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6805c-110">A pointer to a [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6805c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6805c-111">Return value</span></span>

<span data-ttu-id="6805c-112">\_如果插入資料表，則傳回，否則傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6805c-112">Returns S\_OK if the table is inserted, or an error code if not.</span></span>

## <a name="remarks"></a><span data-ttu-id="6805c-113">備註</span><span class="sxs-lookup"><span data-stu-id="6805c-113">Remarks</span></span>

<span data-ttu-id="6805c-114">如果 [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)的 **cpStartRow** 成員是1，則此訊息會刪除選取的文字 (如果有任何) ，然後使用 *wParam* 和 *lParam* 所指定的資料列和資料格參數插入空的資料表資料列。</span><span class="sxs-lookup"><span data-stu-id="6805c-114">If the **cpStartRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) is  1, this message deletes the selected text (if any), and then inserts empty table rows with the row and cell parameters given by *wParam* and *lParam*.</span></span> <span data-ttu-id="6805c-115">它會將選取範圍指向第一個資料列中第一個資料格的開頭。</span><span class="sxs-lookup"><span data-stu-id="6805c-115">It leaves the selection pointing to the start of the first cell in the first row.</span></span> <span data-ttu-id="6805c-116">然後，用戶端可以將選取範圍 (或 [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange)) 指向各種資料格結束記號，然後插入並格式化所需的文字，以填入資料表單元格。</span><span class="sxs-lookup"><span data-stu-id="6805c-116">The client can then populate the table cells by pointing the selection (or an [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange)) to the various cell end marks and inserting and formatting the desired text.</span></span> <span data-ttu-id="6805c-117">這類文字可以包含內嵌的資料表資料列。</span><span class="sxs-lookup"><span data-stu-id="6805c-117">Such text can include nested table rows.</span></span> <span data-ttu-id="6805c-118">或者，如果 **TABLEROWPARMS** 的 **cpStartRow** 成員為0或更大，則會在 **cpStartRow** 指定的字元位置插入資料表資料列。</span><span class="sxs-lookup"><span data-stu-id="6805c-118">Alternatively, if the **cpStartRow** member of the **TABLEROWPARMS** is 0 or greater, table rows are inserted at the character position given by **cpStartRow**.</span></span> <span data-ttu-id="6805c-119">只有在選取的文字中插入資料表時，才會變更目前的選取範圍。</span><span class="sxs-lookup"><span data-stu-id="6805c-119">This only changes the current selection if the table is inserted inside the selected text.</span></span>

<span data-ttu-id="6805c-120">Microsoft Rich Edit 資料表是由一連串的資料表資料列所組成，而這些資料列會由段落順序組成。</span><span class="sxs-lookup"><span data-stu-id="6805c-120">A Microsoft Rich Edit table consists of a sequence of table rows which, in turn, consist of sequences of paragraphs.</span></span> <span data-ttu-id="6805c-121">資料表資料列會以特殊的雙字元分隔符號（U + FFF9 U + 000D）開頭，並以兩個字元的分隔符號段落 U + FFFB U + 000D 做為結尾。</span><span class="sxs-lookup"><span data-stu-id="6805c-121">A table row starts with the special two-character delimiter paragraph U+FFF9 U+000D and ends with the two-character delimiter paragraph U+FFFB U+000D.</span></span> <span data-ttu-id="6805c-122">每個資料格都會以儲存格標記 U + 0007 來結束，如同 U + 000D (CR) 為。</span><span class="sxs-lookup"><span data-stu-id="6805c-122">Each cell is terminated by the cell mark U+0007, which is treated as a hard end-of-paragraph mark just as U+000D (CR) is.</span></span> <span data-ttu-id="6805c-123">資料表資料列和資料格參數會被視為資料表資料列分隔符號的特殊段落格式。</span><span class="sxs-lookup"><span data-stu-id="6805c-123">The table row and cell parameters are treated as special paragraph formatting of the table-row delimiters.</span></span> <span data-ttu-id="6805c-124">格式包含 [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) 結構中的資訊。</span><span class="sxs-lookup"><span data-stu-id="6805c-124">The formatting contains the information in the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span> <span data-ttu-id="6805c-125">[**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms)結構所指定的資料格參數會儲存在擴充版的索引標籤陣列中。</span><span class="sxs-lookup"><span data-stu-id="6805c-125">The cell parameters given by the [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure are stored in an expanded version of the tabs array.</span></span> <span data-ttu-id="6805c-126">此格式可讓資料表嵌套在其他資料表中，最多可達十五個層級。</span><span class="sxs-lookup"><span data-stu-id="6805c-126">This format allows tables to be nested within other tables, up to fifteen levels deep.</span></span>

## <a name="requirements"></a><span data-ttu-id="6805c-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="6805c-127">Requirements</span></span>



| <span data-ttu-id="6805c-128">需求</span><span class="sxs-lookup"><span data-stu-id="6805c-128">Requirement</span></span> | <span data-ttu-id="6805c-129">值</span><span class="sxs-lookup"><span data-stu-id="6805c-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6805c-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6805c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6805c-131">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6805c-131">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6805c-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6805c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6805c-133">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6805c-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6805c-134">標頭</span><span class="sxs-lookup"><span data-stu-id="6805c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6805c-135"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="6805c-135"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6805c-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6805c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6805c-137">**EM \_ INSERTIMAGE**</span><span class="sxs-lookup"><span data-stu-id="6805c-137">**EM\_INSERTIMAGE**</span></span>](em-insertimage.md)
</dt> </dl>

 

 





