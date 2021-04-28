---
title: 'EM_FINDTEXTEXW 訊息 (Richedit .h) '
description: EM_FINDTEXTEXW 訊息-在 rich edit 控制項中尋找 Unicode 文字。
ms.assetid: 7b90ef06-0395-430e-8b5d-b392481a5f70
keywords:
- EM_FINDTEXTEXW message Windows 控制項
topic_type:
- apiref
api_name:
- EM_FINDTEXTEXW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5278726ca4d3e4748e96d8095a411bcebd5637ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109806"
---
# <a name="em_findtextexw-message"></a><span data-ttu-id="8af03-104">EM \_ FINDTEXTEXW 訊息</span><span class="sxs-lookup"><span data-stu-id="8af03-104">EM\_FINDTEXTEXW message</span></span>

<span data-ttu-id="8af03-105">在 rich edit 控制項中尋找 Unicode 文字。</span><span class="sxs-lookup"><span data-stu-id="8af03-105">Finds Unicode text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8af03-106">參數</span><span class="sxs-lookup"><span data-stu-id="8af03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8af03-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8af03-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8af03-108">指定搜尋操作的行為。</span><span class="sxs-lookup"><span data-stu-id="8af03-108">Specifies the behavior of the search operation.</span></span> <span data-ttu-id="8af03-109">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="8af03-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="8af03-110">值</span><span class="sxs-lookup"><span data-stu-id="8af03-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="8af03-111">意義</span><span class="sxs-lookup"><span data-stu-id="8af03-111">Meaning</span></span>                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="8af03-112"><dt>**FR-FR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8af03-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="8af03-113">Microsoft Rich Edit 2.0 和更新版本：如果設定，搜尋會從 **FINDTEXTEX. chrg. cpMin**;如果未設定，則搜尋會從 **FINDTEXTEX. chrg. cpMin**。</span><span class="sxs-lookup"><span data-stu-id="8af03-113">Microsoft Rich Edit 2.0 and later: If set, the search is forward from **FINDTEXTEX.chrg.cpMin**; if not set, the search is backward from **FINDTEXTEX.chrg.cpMin**.</span></span> <br/> <span data-ttu-id="8af03-114">Microsoft Rich Edit 1.0： \_ 已忽略 FR 旗標。</span><span class="sxs-lookup"><span data-stu-id="8af03-114">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="8af03-115">搜尋一律會向前復原。</span><span class="sxs-lookup"><span data-stu-id="8af03-115">The search is always forward.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="8af03-116"><dt>**FR \_ MATCHALEFHAMZA**</dt></span><span class="sxs-lookup"><span data-stu-id="8af03-116"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="8af03-117">如果設定，搜尋會區分具有不同重音的 alefs。</span><span class="sxs-lookup"><span data-stu-id="8af03-117">If set, the search differentiates between alefs with different accents.</span></span> <span data-ttu-id="8af03-118">如果未設定，則具有不同重音的阿拉伯文和希伯來文 alefs 都會以 alef 字元進行比對。</span><span class="sxs-lookup"><span data-stu-id="8af03-118">If not set, Arabic and Hebrew alefs with different accents are all matched by the alef character.</span></span> <br/>                                                                                           |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="8af03-119"><dt>**FR \_ MATCHCASE**</dt></span><span class="sxs-lookup"><span data-stu-id="8af03-119"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="8af03-120">如果設定，搜尋作業會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="8af03-120">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="8af03-121">如果未設定，則搜尋作業不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="8af03-121">If not set, the search operation is case-insensitive.</span></span><br/>                                                                                                                                                                |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="8af03-122"><dt>**FR \_ MATCHDIAC**</dt></span><span class="sxs-lookup"><span data-stu-id="8af03-122"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="8af03-123">如果設定，搜尋作業會考慮變音符號。</span><span class="sxs-lookup"><span data-stu-id="8af03-123">If set, the search operation considers diacritical marks.</span></span> <span data-ttu-id="8af03-124">如果未設定，則會忽略阿拉伯文和希伯來文的變音符號。</span><span class="sxs-lookup"><span data-stu-id="8af03-124">If not set, Arabic and Hebrew diacritical marks are ignored.</span></span> <br/>                                                                                                                                              |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="8af03-125"><dt>**FR \_ MATCHKASHIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="8af03-125"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="8af03-126">如果設定，搜尋作業會考慮 kashidas。</span><span class="sxs-lookup"><span data-stu-id="8af03-126">If set, the search operation considers kashidas.</span></span> <span data-ttu-id="8af03-127">如果未設定，則會忽略阿拉伯文和希伯來文 kashidas。</span><span class="sxs-lookup"><span data-stu-id="8af03-127">If not set, Arabic and Hebrew kashidas are ignored.</span></span> <br/>                                                                                                                                                                |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="8af03-128"><dt>**FR \_ WHOLEWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="8af03-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="8af03-129">如果設定，作業只會搜尋符合搜尋字串的整個單字。</span><span class="sxs-lookup"><span data-stu-id="8af03-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="8af03-130">如果未設定，此作業也會搜尋符合搜尋字串的文字片段。</span><span class="sxs-lookup"><span data-stu-id="8af03-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="8af03-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8af03-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8af03-132">[**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa)結構，其中包含尋找作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8af03-132">A [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8af03-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="8af03-133">Return value</span></span>

<span data-ttu-id="8af03-134">如果找到目標字串，則傳回值是比對之第一個字元的以零為基底的位置。</span><span class="sxs-lookup"><span data-stu-id="8af03-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="8af03-135">如果找不到目標，則傳回值為-1。</span><span class="sxs-lookup"><span data-stu-id="8af03-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="8af03-136">備註</span><span class="sxs-lookup"><span data-stu-id="8af03-136">Remarks</span></span>

<span data-ttu-id="8af03-137">使用此訊息來尋找 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="8af03-137">Use this message to find Unicode strings.</span></span> <span data-ttu-id="8af03-138">若是 ANSI，請使用 [**EM \_ FINDTEXTEX**](em-findtextex.md)。</span><span class="sxs-lookup"><span data-stu-id="8af03-138">For ANSI;, use [**EM\_FINDTEXTEX**](em-findtextex.md).</span></span>

<span data-ttu-id="8af03-139">**FINDTEXTEX** 的 **cpMin** 成員一律會指定搜尋的起始點，而 **cpMax** 則會指定結束點。</span><span class="sxs-lookup"><span data-stu-id="8af03-139">The **cpMin** member of **FINDTEXTEX.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="8af03-140">向前搜尋時， **cpMin** 必須等於或大於 **cpMax**。</span><span class="sxs-lookup"><span data-stu-id="8af03-140">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="8af03-141">向前搜尋時， **cpMax** 中的-1 值會將搜尋範圍延伸至文字的結尾。</span><span class="sxs-lookup"><span data-stu-id="8af03-141">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

<span data-ttu-id="8af03-142">如果搜尋作業找到相符的， [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa)結構的 **chrgText** 成員會傳回包含相符文字的字元位置範圍。</span><span class="sxs-lookup"><span data-stu-id="8af03-142">If the search operation finds a match, the **chrgText** member of the [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure returns the range of character positions that contains the matching text.</span></span>

<span data-ttu-id="8af03-143">**EM \_FINDTEXTEXW** 會使用 [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) 結構，而 [**EM \_ FINDTEXTW**](em-findtextw.md) 會使用 [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) 結構。</span><span class="sxs-lookup"><span data-stu-id="8af03-143">**EM\_FINDTEXTEXW** uses the [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure, while [**EM\_FINDTEXTW**](em-findtextw.md) uses the [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure.</span></span> <span data-ttu-id="8af03-144">差別在於 **EM \_ FINDTEXTEXW** 會報告找到的文字範圍。</span><span class="sxs-lookup"><span data-stu-id="8af03-144">The difference is that **EM\_FINDTEXTEXW** reports the range of text that was found.</span></span>

## <a name="requirements"></a><span data-ttu-id="8af03-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="8af03-145">Requirements</span></span>



| <span data-ttu-id="8af03-146">需求</span><span class="sxs-lookup"><span data-stu-id="8af03-146">Requirement</span></span> | <span data-ttu-id="8af03-147">值</span><span class="sxs-lookup"><span data-stu-id="8af03-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8af03-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8af03-148">Minimum supported client</span></span><br/> | <span data-ttu-id="8af03-149">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8af03-149">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8af03-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8af03-150">Minimum supported server</span></span><br/> | <span data-ttu-id="8af03-151">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8af03-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8af03-152">標頭</span><span class="sxs-lookup"><span data-stu-id="8af03-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="8af03-153"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="8af03-153"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8af03-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8af03-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8af03-155">**EM \_ FINDTEXTW**</span><span class="sxs-lookup"><span data-stu-id="8af03-155">**EM\_FINDTEXTW**</span></span>](em-findtextw.md)
</dt> </dl>

 

 





