---
title: 'EM_FINDTEXTW 訊息 (Richedit .h) '
description: 在 rich edit 控制項中尋找 Unicode 文字。
ms.assetid: 0c1579f5-3b37-4e28-86a2-f4e03e195f38
keywords:
- EM_FINDTEXTW message Windows 控制項
topic_type:
- apiref
api_name:
- EM_FINDTEXTW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73e8bae60269ab3ddb84a17c285c243e00d8117c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686239"
---
# <a name="em_findtextw-message"></a><span data-ttu-id="e019b-104">EM \_ FINDTEXTW 訊息</span><span class="sxs-lookup"><span data-stu-id="e019b-104">EM\_FINDTEXTW message</span></span>

<span data-ttu-id="e019b-105">在 rich edit 控制項中尋找 Unicode 文字。</span><span class="sxs-lookup"><span data-stu-id="e019b-105">Finds Unicode text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e019b-106">參數</span><span class="sxs-lookup"><span data-stu-id="e019b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e019b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e019b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e019b-108">指定搜尋作業的參數。</span><span class="sxs-lookup"><span data-stu-id="e019b-108">Specifies the parameters of the search operation.</span></span> <span data-ttu-id="e019b-109">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="e019b-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="e019b-110">值</span><span class="sxs-lookup"><span data-stu-id="e019b-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="e019b-111">意義</span><span class="sxs-lookup"><span data-stu-id="e019b-111">Meaning</span></span>                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="e019b-112"><dt>**FR-FR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e019b-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="e019b-113">如果設定，則作業會從目前選取範圍的結尾開始搜尋檔的結尾。</span><span class="sxs-lookup"><span data-stu-id="e019b-113">If set, the operation searches from the end of the current selection to the end of the document.</span></span> <span data-ttu-id="e019b-114">如果未設定，則作業會從目前選取範圍的結尾開始搜尋檔的開頭。</span><span class="sxs-lookup"><span data-stu-id="e019b-114">If not set, the operation searches from the end of the current selection to the beginning of the document.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="e019b-115"><dt>**FR \_ MATCHALEFHAMZA**</dt></span><span class="sxs-lookup"><span data-stu-id="e019b-115"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="e019b-116">依預設，具有不同重音的阿拉伯文和希伯來文 alefs 都會以 alef 字元進行比對。</span><span class="sxs-lookup"><span data-stu-id="e019b-116">By default, Arabic and Hebrew alefs with different accents are all matched by the alef character.</span></span> <span data-ttu-id="e019b-117">如果您想要讓搜尋區分 alefs 與不同的重音，請設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="e019b-117">Set this flag if you want the search to differentiate between alefs with different accents.</span></span><br/>               |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="e019b-118"><dt>**FR \_ MATCHCASE**</dt></span><span class="sxs-lookup"><span data-stu-id="e019b-118"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="e019b-119">如果設定，搜尋作業會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="e019b-119">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="e019b-120">如果未設定，則搜尋作業不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="e019b-120">If not set, the search operation is case-insensitive.</span></span><br/>                                                                                                       |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="e019b-121"><dt>**FR \_ MATCHDIAC**</dt></span><span class="sxs-lookup"><span data-stu-id="e019b-121"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="e019b-122">根據預設，會忽略阿拉伯文和希伯來文的變音符號。</span><span class="sxs-lookup"><span data-stu-id="e019b-122">By default, Arabic and Hebrew diacritical marks are ignored.</span></span> <span data-ttu-id="e019b-123">如果您想要讓搜尋作業考慮變音符號，請設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="e019b-123">Set this flag if you want the search operation to consider diacritical marks.</span></span><br/>                                                                  |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="e019b-124"><dt>**FR \_ MATCHKASHIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="e019b-124"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="e019b-125">依預設，會忽略阿拉伯文和希伯來文 kashidas。</span><span class="sxs-lookup"><span data-stu-id="e019b-125">By default, Arabic and Hebrew kashidas are ignored.</span></span> <span data-ttu-id="e019b-126">如果您想要搜尋作業考慮 kashidas，請設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="e019b-126">Set this flag if you want the search operation to consider kashidas.</span></span><br/>                                                                                    |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="e019b-127"><dt>**FR \_ WHOLEWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="e019b-127"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="e019b-128">如果設定，作業只會搜尋符合搜尋字串的整個單字。</span><span class="sxs-lookup"><span data-stu-id="e019b-128">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="e019b-129">如果未設定，此作業也會搜尋符合搜尋字串的文字片段。</span><span class="sxs-lookup"><span data-stu-id="e019b-129">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                  |



 

</dd> <dt>

<span data-ttu-id="e019b-130">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e019b-130">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e019b-131">[**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta)結構，其中包含尋找作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e019b-131">A [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e019b-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="e019b-132">Return value</span></span>

<span data-ttu-id="e019b-133">如果找到目標字串，則傳回值是比對之第一個字元的以零為基底的位置。</span><span class="sxs-lookup"><span data-stu-id="e019b-133">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="e019b-134">如果找不到目標，則傳回值為-1。</span><span class="sxs-lookup"><span data-stu-id="e019b-134">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="e019b-135">備註</span><span class="sxs-lookup"><span data-stu-id="e019b-135">Remarks</span></span>

<span data-ttu-id="e019b-136">**EM \_FINDTEXTW** 會使用 [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) 結構，而 [**EM \_ FINDTEXTEXW**](em-findtextexw.md) 會使用 [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) 結構。</span><span class="sxs-lookup"><span data-stu-id="e019b-136">**EM\_FINDTEXTW** uses the [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure, while [**EM\_FINDTEXTEXW**](em-findtextexw.md) uses the [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure.</span></span> <span data-ttu-id="e019b-137">差別在於 **FINDTEXTEXW** 會回報所找到的文字範圍。</span><span class="sxs-lookup"><span data-stu-id="e019b-137">The difference is that **FINDTEXTEXW** reports back the range of text that was found.</span></span>

## <a name="requirements"></a><span data-ttu-id="e019b-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="e019b-138">Requirements</span></span>



| <span data-ttu-id="e019b-139">需求</span><span class="sxs-lookup"><span data-stu-id="e019b-139">Requirement</span></span> | <span data-ttu-id="e019b-140">值</span><span class="sxs-lookup"><span data-stu-id="e019b-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e019b-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e019b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e019b-142">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e019b-142">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e019b-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e019b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e019b-144">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e019b-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e019b-145">標頭</span><span class="sxs-lookup"><span data-stu-id="e019b-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="e019b-146"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="e019b-146"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e019b-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e019b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e019b-148">**EM \_ FINDTEXTEXW**</span><span class="sxs-lookup"><span data-stu-id="e019b-148">**EM\_FINDTEXTEXW**</span></span>](em-findtextexw.md)
</dt> </dl>

 

 





