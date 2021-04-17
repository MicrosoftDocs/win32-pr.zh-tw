---
title: 'FINDMSGSTRING message (Commdlg) '
description: 當使用者按一下 [尋找下一個]、[取代] 或 [全部取代] 按鈕，或關閉對話方塊時，[尋找或取代] 對話方塊會將 FINDMSGSTRING 註冊的訊息傳送至其擁有者視窗的視窗程式。
ms.assetid: ed0b256a-96df-4588-b8f3-f7d1f89ffe74
keywords:
- FINDMSGSTRING 訊息對話方塊
topic_type:
- apiref
api_name:
- FINDMSGSTRING
- FINDMSGSTRINGA
- FINDMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0d3a73d8734d79d5ed0862f66bf9ba5c030e46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509307"
---
# <a name="findmsgstring-message"></a><span data-ttu-id="d6c41-104">FINDMSGSTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="d6c41-104">FINDMSGSTRING message</span></span>

<span data-ttu-id="d6c41-105">當使用者按一下 [**尋找下一個**]、[**取代**] 或 [**全部取代**] 按鈕，或關閉對話方塊時，[**尋找** 或 **取代**] 對話方塊會將 **FINDMSGSTRING** 註冊的訊息傳送至其擁有者視窗的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="d6c41-105">A **Find** or **Replace** dialog box sends the **FINDMSGSTRING** registered message to the window procedure of its owner window when the user clicks the **Find Next**, **Replace**, or **Replace All** button, or closes the dialog box.</span></span>


```C++
#define FINDMSGSTRING TEXT("commdlg_FindReplace")
```



## <a name="parameters"></a><span data-ttu-id="d6c41-106">參數</span><span class="sxs-lookup"><span data-stu-id="d6c41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6c41-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d6c41-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6c41-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="d6c41-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d6c41-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d6c41-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6c41-110">[**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d6c41-110">A pointer to a [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure.</span></span> <span data-ttu-id="d6c41-111">此結構的成員包含最新的使用者輸入，包括要搜尋的字串、取代字串 (是否有任何) 和搜尋和取代選項。</span><span class="sxs-lookup"><span data-stu-id="d6c41-111">The members of this structure contain the latest user input, including the string to search for, the replacement string (if any) and the search-and-replacement options.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6c41-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6c41-112">Return value</span></span>

<span data-ttu-id="d6c41-113">此訊息沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="d6c41-113">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6c41-114">備註</span><span class="sxs-lookup"><span data-stu-id="d6c41-114">Remarks</span></span>

<span data-ttu-id="d6c41-115">您必須在 [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)函數的呼叫中指定 **FINDMSGSTRING** 常數，以取得對話方塊所傳送之訊息的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d6c41-115">You must specify the **FINDMSGSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="d6c41-116">當您建立對話方塊時，請使用 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)結構的 **hwndOwner** 成員來識別要接收 **FINDMSGSTRING** 訊息的視窗。</span><span class="sxs-lookup"><span data-stu-id="d6c41-116">When you create the dialog box, use the **hwndOwner** member of the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure to identify the window to receive **FINDMSGSTRING** messages.</span></span>

<span data-ttu-id="d6c41-117">[**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)結構的 **flags** 成員包含下列其中一個旗標，以指出造成訊息的事件。</span><span class="sxs-lookup"><span data-stu-id="d6c41-117">The **Flags** member of the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure includes one of the following flags to indicate the event that caused the message.</span></span>



| <span data-ttu-id="d6c41-118">旗標</span><span class="sxs-lookup"><span data-stu-id="d6c41-118">Flag</span></span>                            | <span data-ttu-id="d6c41-119">意義</span><span class="sxs-lookup"><span data-stu-id="d6c41-119">Meaning</span></span>                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c41-120">**FR \_DIALOGTERM** (0x00000040) </span><span class="sxs-lookup"><span data-stu-id="d6c41-120">**FR\_DIALOGTERM** (0x00000040)</span></span> | <span data-ttu-id="d6c41-121">對話方塊正在關閉。</span><span class="sxs-lookup"><span data-stu-id="d6c41-121">The dialog box is closing.</span></span> <span data-ttu-id="d6c41-122">擁有者視窗處理此訊息之後，對話方塊的控制碼將不再有效。</span><span class="sxs-lookup"><span data-stu-id="d6c41-122">After the owner window processes this message, a handle to the dialog box is no longer valid.</span></span>                                                                                    |
| <span data-ttu-id="d6c41-123">**FR \_FINDNEXT** (0x00000008) </span><span class="sxs-lookup"><span data-stu-id="d6c41-123">**FR\_FINDNEXT** (0x00000008)</span></span>   | <span data-ttu-id="d6c41-124">使用者按一下 [**尋找** 或 **取代**] 對話方塊中的 [**尋找下一個]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="d6c41-124">The user clicked the **Find Next** button in a **Find** or **Replace** dialog box.</span></span> <span data-ttu-id="d6c41-125">**LpstrFindWhat** 成員會指定要搜尋的字串。</span><span class="sxs-lookup"><span data-stu-id="d6c41-125">The **lpstrFindWhat** member specifies the string to search for.</span></span>                                                         |
| <span data-ttu-id="d6c41-126">**FR \_取代** (0x00000010) </span><span class="sxs-lookup"><span data-stu-id="d6c41-126">**FR\_REPLACE** (0x00000010)</span></span>    | <span data-ttu-id="d6c41-127">使用者按一下 [**取代**] 對話方塊中的 [**取代**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="d6c41-127">The user clicked the **Replace** button in a **Replace** dialog box.</span></span> <span data-ttu-id="d6c41-128">**LpstrFindWhat** 成員會指定要取代的字串，而 **lpstrReplaceWith** 成員會指定取代字串。</span><span class="sxs-lookup"><span data-stu-id="d6c41-128">The **lpstrFindWhat** member specifies the string to replace and the **lpstrReplaceWith** member specifies the replacement string.</span></span>     |
| <span data-ttu-id="d6c41-129">**FR \_型全部型** (0x00000020) </span><span class="sxs-lookup"><span data-stu-id="d6c41-129">**FR\_REPLACEALL** (0x00000020)</span></span> | <span data-ttu-id="d6c41-130">使用者按一下 [**取代**] 對話方塊中的 [**全部取代**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="d6c41-130">The user clicked the **Replace All** button in a **Replace** dialog box.</span></span> <span data-ttu-id="d6c41-131">**LpstrFindWhat** 成員會指定要取代的字串，而 **lpstrReplaceWith** 成員會指定取代字串。</span><span class="sxs-lookup"><span data-stu-id="d6c41-131">The **lpstrFindWhat** member specifies the string to replace and the **lpstrReplaceWith** member specifies the replacement string.</span></span> |



 

<span data-ttu-id="d6c41-132">如果是 [ **尋找下一個]** 或 [ **取代全部** ] 訊息， **旗標** 成員可以包含下列一或多個旗標，以表示搜尋選項。</span><span class="sxs-lookup"><span data-stu-id="d6c41-132">For a **Find Next** or **Replace All** message, the **Flags** member can include one or more of the following flags to indicate the search options.</span></span>



| <span data-ttu-id="d6c41-133">旗標</span><span class="sxs-lookup"><span data-stu-id="d6c41-133">Flag</span></span>                           | <span data-ttu-id="d6c41-134">意義</span><span class="sxs-lookup"><span data-stu-id="d6c41-134">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c41-135">**FR \_向下** (0x00000001) </span><span class="sxs-lookup"><span data-stu-id="d6c41-135">**FR\_DOWN** (0x00000001)</span></span>      | <span data-ttu-id="d6c41-136">如果設定，則會選取 [方向] 選項按鈕的 **向下** 按鈕，表示使用者想要從目前的位置搜尋至檔的結尾。</span><span class="sxs-lookup"><span data-stu-id="d6c41-136">If set, the **Down** button of the direction radio buttons is selected indicating that user wants to search from the current location to the end of the document.</span></span> <span data-ttu-id="d6c41-137">如果未設定 **FR \_ DOWN** ，則會選取 [ **向上** ] 按鈕，讓使用者想要搜尋檔的開頭。</span><span class="sxs-lookup"><span data-stu-id="d6c41-137">If **FR\_DOWN** is not set, the **Up** button is selected so the user wants to search to the beginning of the document.</span></span>       |
| <span data-ttu-id="d6c41-138">**FR \_MATCHCASE** (0x00000004) </span><span class="sxs-lookup"><span data-stu-id="d6c41-138">**FR\_MATCHCASE** (0x00000004)</span></span> | <span data-ttu-id="d6c41-139">如果設定，則會選取 [ **符合大小寫** ] 核取方塊，表示使用者想要搜尋區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d6c41-139">If set, the **Match Case** check box is selected indicating that the user wants the search to be case-sensitive.</span></span> <span data-ttu-id="d6c41-140">如果未設定 **FR \_ MATCHCASE** ，則不會選取此核取方塊，因此搜尋應該不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d6c41-140">If **FR\_MATCHCASE** is not set, the check box is unselected so the search should be case-insensitive.</span></span>                                                                         |
| <span data-ttu-id="d6c41-141">**FR \_WHOLEWORD** (0x00000002) </span><span class="sxs-lookup"><span data-stu-id="d6c41-141">**FR\_WHOLEWORD** (0x00000002)</span></span> | <span data-ttu-id="d6c41-142">如果設定，則會選取 [ **僅符合全字** 組] 核取方塊，表示使用者只想搜尋符合搜尋字串的全字組。</span><span class="sxs-lookup"><span data-stu-id="d6c41-142">If set, the **Match Whole Word Only** check box is selected indicating that the user wants to search only for whole words that match the search string.</span></span> <span data-ttu-id="d6c41-143">如果未設定 **FR \_ WHOLEWORD** ，則不會選取此核取方塊，所以您也應該搜尋符合搜尋字串的文字片段。</span><span class="sxs-lookup"><span data-stu-id="d6c41-143">If **FR\_WHOLEWORD** is not set, the check box is unselected so you should also search for word fragments that match the search string.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d6c41-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6c41-144">Requirements</span></span>



| <span data-ttu-id="d6c41-145">需求</span><span class="sxs-lookup"><span data-stu-id="d6c41-145">Requirement</span></span> | <span data-ttu-id="d6c41-146">值</span><span class="sxs-lookup"><span data-stu-id="d6c41-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c41-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6c41-147">Minimum supported client</span></span><br/> | <span data-ttu-id="d6c41-148">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6c41-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d6c41-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6c41-149">Minimum supported server</span></span><br/> | <span data-ttu-id="d6c41-150">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6c41-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d6c41-151">標頭</span><span class="sxs-lookup"><span data-stu-id="d6c41-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6c41-152"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d6c41-152"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d6c41-153">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="d6c41-153">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d6c41-154">**FINDMSGSTRINGW** (Unicode) 和 **FINDMSGSTRINGA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="d6c41-154">**FINDMSGSTRINGW** (Unicode) and **FINDMSGSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="d6c41-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6c41-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="d6c41-156">**參考**</span><span class="sxs-lookup"><span data-stu-id="d6c41-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d6c41-157">**FINDREPLACE**</span><span class="sxs-lookup"><span data-stu-id="d6c41-157">**FINDREPLACE**</span></span>](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[<span data-ttu-id="d6c41-158">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="d6c41-158">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="d6c41-159">**概念**</span><span class="sxs-lookup"><span data-stu-id="d6c41-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d6c41-160">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="d6c41-160">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

