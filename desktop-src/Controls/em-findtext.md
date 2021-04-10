---
title: 'EM_FINDTEXT 訊息 (Richedit .h) '
description: 在 rich edit 控制項中尋找文字。
ms.assetid: f19e19a0-d8dd-4d31-b76d-f1f09577dd2d
keywords:
- EM_FINDTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_FINDTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e50034337f05d2df17af777986136881c503d05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934552"
---
# <a name="em_findtext-message"></a><span data-ttu-id="a0b52-104">EM \_ FINDTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="a0b52-104">EM\_FINDTEXT message</span></span>

<span data-ttu-id="a0b52-105">在 rich edit 控制項中尋找文字。</span><span class="sxs-lookup"><span data-stu-id="a0b52-105">Finds text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a0b52-106">參數</span><span class="sxs-lookup"><span data-stu-id="a0b52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0b52-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a0b52-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0b52-108">指定搜尋作業的參數。</span><span class="sxs-lookup"><span data-stu-id="a0b52-108">Specify the parameters of the search operation.</span></span> <span data-ttu-id="a0b52-109">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="a0b52-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="a0b52-110">值</span><span class="sxs-lookup"><span data-stu-id="a0b52-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="a0b52-111">意義</span><span class="sxs-lookup"><span data-stu-id="a0b52-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="a0b52-112"><dt>**FR-FR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a0b52-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="a0b52-113">Microsoft Rich Edit 2.0 和更新版本：如果設定，搜尋會從目前選取範圍的結尾到檔的結尾。</span><span class="sxs-lookup"><span data-stu-id="a0b52-113">Microsoft Rich Edit 2.0 and later: If set, the search is from the end of the current selection to the end of the document.</span></span> <span data-ttu-id="a0b52-114">如果未設定，則會從目前選取範圍的結尾到檔的開頭進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="a0b52-114">If not set, the search is from the end of the current selection to the beginning of the document.</span></span> <br/> <span data-ttu-id="a0b52-115">Microsoft Rich Edit 1.0： \_ 已忽略 FR 旗標。</span><span class="sxs-lookup"><span data-stu-id="a0b52-115">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="a0b52-116">搜尋一律會從目前選取範圍的結尾到檔的結尾。</span><span class="sxs-lookup"><span data-stu-id="a0b52-116">The search is always from the end of the current selection to the end of the document.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="a0b52-117"><dt>**FR \_ MATCHALEFHAMZA**</dt></span><span class="sxs-lookup"><span data-stu-id="a0b52-117"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="a0b52-118">Microsoft Rich Edit 3.0 和更新版本：如果設定，搜尋會區分阿拉伯文 alefs 與不同的重音。</span><span class="sxs-lookup"><span data-stu-id="a0b52-118">Microsoft Rich Edit 3.0 and later: If set, the search differentiates between Arabic alefs with different accents.</span></span> <span data-ttu-id="a0b52-119">如果未設定，則會將所有 alefs 單獨與 alef 字元相符。</span><span class="sxs-lookup"><span data-stu-id="a0b52-119">If not set, all alefs are matched by the alef character alone.</span></span> <br/>                                                                                                                                                                                                      |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="a0b52-120"><dt>**FR \_ MATCHDIAC**</dt></span><span class="sxs-lookup"><span data-stu-id="a0b52-120"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="a0b52-121">Microsoft Rich Edit 3.0 和更新版本：如果設定，搜尋作業會考慮阿拉伯文和希伯來文的變音符號。</span><span class="sxs-lookup"><span data-stu-id="a0b52-121">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew diacritical marks.</span></span> <span data-ttu-id="a0b52-122">如果未設定，則會忽略變音符號標記。</span><span class="sxs-lookup"><span data-stu-id="a0b52-122">If not set, diacritical marks are ignored.</span></span> <br/>                                                                                                                                                                                                                             |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="a0b52-123"><dt>**FR \_ MATCHKASHIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="a0b52-123"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="a0b52-124">Microsoft Rich Edit 3.0 和更新版本：如果設定，搜尋作業會考慮阿拉伯文 kashidas。</span><span class="sxs-lookup"><span data-stu-id="a0b52-124">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic kashidas.</span></span> <span data-ttu-id="a0b52-125">如果未設定，則會忽略 kashidas。</span><span class="sxs-lookup"><span data-stu-id="a0b52-125">If not set, kashidas are ignored.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="FR_MATCHWIDTH"></span><span id="fr_matchwidth"></span><dl> <span data-ttu-id="a0b52-126"><dt>**FR \_ MATCHWIDTH**</dt></span><span class="sxs-lookup"><span data-stu-id="a0b52-126"><dt>**FR\_MATCHWIDTH**</dt></span></span> </dl>             | <span data-ttu-id="a0b52-127">Windows 8：如果設定，則相同字元的單一位元組和雙位元組版本會視為不相等。</span><span class="sxs-lookup"><span data-stu-id="a0b52-127">Windows 8: If set, single-byte and double-byte versions of the same character are considered to be not equal.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="a0b52-128"><dt>**FR \_ WHOLEWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="a0b52-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="a0b52-129">如果設定，作業只會搜尋符合搜尋字串的整個單字。</span><span class="sxs-lookup"><span data-stu-id="a0b52-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="a0b52-130">如果未設定，此作業也會搜尋符合搜尋字串的文字片段。</span><span class="sxs-lookup"><span data-stu-id="a0b52-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="a0b52-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0b52-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0b52-132">[**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta)結構，其中包含尋找作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a0b52-132">A [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0b52-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="a0b52-133">Return value</span></span>

<span data-ttu-id="a0b52-134">如果找到目標字串，則傳回值是比對之第一個字元的以零為基底的位置。</span><span class="sxs-lookup"><span data-stu-id="a0b52-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="a0b52-135">如果找不到目標，則傳回值為-1。</span><span class="sxs-lookup"><span data-stu-id="a0b52-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0b52-136">備註</span><span class="sxs-lookup"><span data-stu-id="a0b52-136">Remarks</span></span>

<span data-ttu-id="a0b52-137">**FINDTEXT** 的 **cpMin** 成員一律會指定搜尋的起始點，而 **cpMax** 則會指定結束點。</span><span class="sxs-lookup"><span data-stu-id="a0b52-137">The **cpMin** member of **FINDTEXT.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="a0b52-138">向前搜尋時， **cpMin** 必須等於或大於 **cpMax**。</span><span class="sxs-lookup"><span data-stu-id="a0b52-138">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="a0b52-139">向前搜尋時， **cpMax** 中的-1 值會將搜尋範圍延伸至文字的結尾。</span><span class="sxs-lookup"><span data-stu-id="a0b52-139">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0b52-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0b52-140">Requirements</span></span>



| <span data-ttu-id="a0b52-141">需求</span><span class="sxs-lookup"><span data-stu-id="a0b52-141">Requirement</span></span> | <span data-ttu-id="a0b52-142">值</span><span class="sxs-lookup"><span data-stu-id="a0b52-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0b52-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0b52-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a0b52-144">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0b52-144">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a0b52-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0b52-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a0b52-146">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0b52-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a0b52-147">標頭</span><span class="sxs-lookup"><span data-stu-id="a0b52-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0b52-148"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="a0b52-148"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0b52-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0b52-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0b52-150">**FINDTEXT**</span><span class="sxs-lookup"><span data-stu-id="a0b52-150">**FINDTEXT**</span></span>](/windows/win32/api/richedit/ns-richedit-findtexta)
</dt> </dl>

 

 





