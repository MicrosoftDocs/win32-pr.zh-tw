---
title: 'EM_FINDTEXTEX 訊息 (Richedit .h) '
description: 在 rich edit 控制項中尋找文字。
ms.assetid: f1bf925b-2776-40b8-9d05-8484daf8d989
keywords:
- EM_FINDTEXTEX message Windows 控制項
topic_type:
- apiref
api_name:
- EM_FINDTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e52f7d51ee7a186a8a9e66f11884d6c2e9bca2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104225"
---
# <a name="em_findtextex-message"></a><span data-ttu-id="cec09-104">EM \_ FINDTEXTEX 訊息</span><span class="sxs-lookup"><span data-stu-id="cec09-104">EM\_FINDTEXTEX message</span></span>

<span data-ttu-id="cec09-105">在 rich edit 控制項中尋找文字。</span><span class="sxs-lookup"><span data-stu-id="cec09-105">Finds text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cec09-106">參數</span><span class="sxs-lookup"><span data-stu-id="cec09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cec09-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cec09-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cec09-108">指定搜尋操作的行為。</span><span class="sxs-lookup"><span data-stu-id="cec09-108">Specifies the behavior of the search operation.</span></span> <span data-ttu-id="cec09-109">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="cec09-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="cec09-110">值</span><span class="sxs-lookup"><span data-stu-id="cec09-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="cec09-111">意義</span><span class="sxs-lookup"><span data-stu-id="cec09-111">Meaning</span></span>                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="cec09-112"><dt>**FR-FR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cec09-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="cec09-113">Microsoft Rich Edit 2.0 和更新版本：如果設定，搜尋會從 **FINDTEXTEX. chrg. cpMin**;如果未設定，則搜尋會從 **FINDTEXTEX. chrg. cpMin**。</span><span class="sxs-lookup"><span data-stu-id="cec09-113">Microsoft Rich Edit 2.0 and later: If set, the search is forward from **FINDTEXTEX.chrg.cpMin**; if not set, the search is backward from **FINDTEXTEX.chrg.cpMin**.</span></span> <br/> <span data-ttu-id="cec09-114">Microsoft Rich Edit 1.0： \_ 已忽略 FR 旗標。</span><span class="sxs-lookup"><span data-stu-id="cec09-114">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="cec09-115">搜尋一律會向前復原。</span><span class="sxs-lookup"><span data-stu-id="cec09-115">The search is always forward.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="cec09-116"><dt>**FR \_ MATCHALEFHAMZA**</dt></span><span class="sxs-lookup"><span data-stu-id="cec09-116"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="cec09-117">Microsoft Rich Edit 3.0 和更新版本：如果設定，搜尋會區分阿拉伯文和希伯來文 alefs 與不同的強調。</span><span class="sxs-lookup"><span data-stu-id="cec09-117">Microsoft Rich Edit 3.0 and later: If set, the search differentiates between Arabic and Hebrew alefs with different accents.</span></span> <span data-ttu-id="cec09-118">如果未設定，則會將所有 alefs 單獨與 alef 字元相符。</span><span class="sxs-lookup"><span data-stu-id="cec09-118">If not set, all alefs are matched by the alef character alone.</span></span> <br/>                                                                         |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="cec09-119"><dt>**FR \_ MATCHCASE**</dt></span><span class="sxs-lookup"><span data-stu-id="cec09-119"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="cec09-120">如果設定，搜尋作業會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="cec09-120">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="cec09-121">如果未設定，則搜尋作業不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="cec09-121">If not set, the search operation is case-insensitive.</span></span> <br/>                                                                                                                                                               |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="cec09-122"><dt>**FR \_ MATCHDIAC**</dt></span><span class="sxs-lookup"><span data-stu-id="cec09-122"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="cec09-123">Microsoft Rich Edit 3.0 和更新版本：如果設定，搜尋作業會考慮阿拉伯文和希伯來文的變音符號。</span><span class="sxs-lookup"><span data-stu-id="cec09-123">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew diacritical marks.</span></span> <span data-ttu-id="cec09-124">如果未設定，則會忽略變音符號標記。</span><span class="sxs-lookup"><span data-stu-id="cec09-124">If not set, diacritical marks are ignored.</span></span> <br/>                                                                                                           |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="cec09-125"><dt>**FR \_ MATCHKASHIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="cec09-125"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="cec09-126">Microsoft Rich Edit 3.0 和更新版本：如果設定，搜尋作業會考慮阿拉伯文和希伯來文 kashidas。</span><span class="sxs-lookup"><span data-stu-id="cec09-126">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew kashidas.</span></span> <span data-ttu-id="cec09-127">如果未設定，則會忽略 kashidas。</span><span class="sxs-lookup"><span data-stu-id="cec09-127">If not set, kashidas are ignored.</span></span> <br/>                                                                                                                             |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="cec09-128"><dt>**FR \_ WHOLEWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="cec09-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="cec09-129">如果設定，作業只會搜尋符合搜尋字串的整個單字。</span><span class="sxs-lookup"><span data-stu-id="cec09-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="cec09-130">如果未設定，此作業也會搜尋符合搜尋字串的文字片段。</span><span class="sxs-lookup"><span data-stu-id="cec09-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="cec09-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cec09-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cec09-132">[**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa)結構，其中包含尋找作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cec09-132">A [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cec09-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="cec09-133">Return value</span></span>

<span data-ttu-id="cec09-134">如果找到目標字串，則傳回值是比對之第一個字元的以零為基底的位置。</span><span class="sxs-lookup"><span data-stu-id="cec09-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="cec09-135">如果找不到目標，則傳回值為-1。</span><span class="sxs-lookup"><span data-stu-id="cec09-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="cec09-136">備註</span><span class="sxs-lookup"><span data-stu-id="cec09-136">Remarks</span></span>

<span data-ttu-id="cec09-137">使用此訊息來尋找 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="cec09-137">Use this message to find ANSI strings.</span></span> <span data-ttu-id="cec09-138">若為 Unicode，請使用 [**EM \_ FINDTEXTEXW**](em-findtextexw.md)。</span><span class="sxs-lookup"><span data-stu-id="cec09-138">For Unicode, use [**EM\_FINDTEXTEXW**](em-findtextexw.md).</span></span>

<span data-ttu-id="cec09-139">**FINDTEXTEX** 的 **cpMin** 成員一律會指定搜尋的起始點，而 **cpMax** 則會指定結束點。</span><span class="sxs-lookup"><span data-stu-id="cec09-139">The **cpMin** member of **FINDTEXTEX.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="cec09-140">向前搜尋時， **cpMin** 必須等於或大於 **cpMax**。</span><span class="sxs-lookup"><span data-stu-id="cec09-140">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="cec09-141">向前搜尋時， **cpMax** 中的-1 值會將搜尋範圍延伸至文字的結尾。</span><span class="sxs-lookup"><span data-stu-id="cec09-141">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

<span data-ttu-id="cec09-142">如果搜尋作業找到相符的， [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa)結構的 **chrgText** 成員會傳回包含相符文字的字元位置範圍。</span><span class="sxs-lookup"><span data-stu-id="cec09-142">If the search operation finds a match, the **chrgText** member of the [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure returns the range of character positions that contains the matching text.</span></span>

## <a name="requirements"></a><span data-ttu-id="cec09-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="cec09-143">Requirements</span></span>



| <span data-ttu-id="cec09-144">需求</span><span class="sxs-lookup"><span data-stu-id="cec09-144">Requirement</span></span> | <span data-ttu-id="cec09-145">值</span><span class="sxs-lookup"><span data-stu-id="cec09-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cec09-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cec09-146">Minimum supported client</span></span><br/> | <span data-ttu-id="cec09-147">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cec09-147">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cec09-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cec09-148">Minimum supported server</span></span><br/> | <span data-ttu-id="cec09-149">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cec09-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cec09-150">標頭</span><span class="sxs-lookup"><span data-stu-id="cec09-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="cec09-151"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="cec09-151"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cec09-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cec09-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cec09-153">**EM \_ FINDTEXT**</span><span class="sxs-lookup"><span data-stu-id="cec09-153">**EM\_FINDTEXT**</span></span>](em-findtext.md)
</dt> </dl>

 

 





