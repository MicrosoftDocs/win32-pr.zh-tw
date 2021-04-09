---
title: 'EM_AUTOURLDETECT 訊息 (Richedit .h) '
description: 啟用或停用 rich edit 控制項的超連結自動偵測。
ms.assetid: 6970ff36-ff3f-4413-a471-9389a76c8f38
keywords:
- EM_AUTOURLDETECT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_AUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc8f76b89e5e8aa529084b5c8c0898200e28ed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934638"
---
# <a name="em_autourldetect-message"></a><span data-ttu-id="fa2b2-104">EM \_ AUTOURLDETECT 訊息</span><span class="sxs-lookup"><span data-stu-id="fa2b2-104">EM\_AUTOURLDETECT message</span></span>

<span data-ttu-id="fa2b2-105">啟用或停用 rich edit 控制項的超連結自動偵測。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-105">Enables or disables automatic detection of hyperlinks by a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa2b2-106">參數</span><span class="sxs-lookup"><span data-stu-id="fa2b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa2b2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa2b2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa2b2-108">指定0會停用自動連結偵測，或指定下列其中一個值來啟用各種類型的偵測。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-108">Specify 0 to disable automatic link detection, or one of the following values to enable various kinds of detection.</span></span>



| <span data-ttu-id="fa2b2-109">值</span><span class="sxs-lookup"><span data-stu-id="fa2b2-109">Value</span></span>                                                                                                                                                                                       | <span data-ttu-id="fa2b2-110">意義</span><span class="sxs-lookup"><span data-stu-id="fa2b2-110">Meaning</span></span>                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AURL_DISABLEMIXEDLGC"></span><span id="aurl_disablemixedlgc"></span><dl> <span data-ttu-id="fa2b2-111"><dt>**AURL \_ DISABLEMIXEDLGC**</dt></span><span class="sxs-lookup"><span data-stu-id="fa2b2-111"><dt>**AURL\_DISABLEMIXEDLGC**</dt></span></span> </dl>          | <span data-ttu-id="fa2b2-112">**Windows 8**：停用包含屬於下列其中一個以上腳本的標籤之功能變數名稱的識別：拉丁、希臘文和斯拉夫文。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-112">**Windows 8**: Disable recognition of domain names that contain labels with characters belonging to more than one of the following scripts: Latin, Greek, and Cyrillic.</span></span> <br/> |
| <span id="AURL_ENABLEDRIVELETTERS"></span><span id="aurl_enabledriveletters"></span><dl> <span data-ttu-id="fa2b2-113"><dt>**AURL \_ ENABLEDRIVELETTERS**</dt></span><span class="sxs-lookup"><span data-stu-id="fa2b2-113"><dt>**AURL\_ENABLEDRIVELETTERS**</dt></span></span> </dl> | <span data-ttu-id="fa2b2-114">**Windows 8**：辨識具有前置磁片磁碟機規格的檔案名，例如 c： \\ temp。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-114">**Windows 8**: Recognize file names that have a leading drive specification, such as c:\\temp.</span></span><br/>                                                                           |
| <span id="AURL_ENABLEEA"></span><span id="aurl_enableea"></span><dl> <span data-ttu-id="fa2b2-115"><dt>**AURL \_ ENABLEEA**</dt></span><span class="sxs-lookup"><span data-stu-id="fa2b2-115"><dt>**AURL\_ENABLEEA**</dt></span></span> </dl>                               | <span data-ttu-id="fa2b2-116">此值已被取代;請改用 **AURL \_ ENABLEEAURLS** 。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-116">This value is deprecated; use **AURL\_ENABLEEAURLS** instead.</span></span><br/>                                                                                                            |
| <span id="AURL_ENABLEEAURLS"></span><span id="aurl_enableeaurls"></span><dl> <span data-ttu-id="fa2b2-117"><dt>**AURL \_ ENABLEEAURLS**</dt></span><span class="sxs-lookup"><span data-stu-id="fa2b2-117"><dt>**AURL\_ENABLEEAURLS**</dt></span></span> </dl>                   | <span data-ttu-id="fa2b2-118">辨識包含東亞字元的 Url。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-118">Recognize URLs that contain East Asian characters.</span></span> <br/>                                                                                                                      |
| <span id="AURL_ENABLEEMAILADDR"></span><span id="aurl_enableemailaddr"></span><dl> <span data-ttu-id="fa2b2-119"><dt>**AURL \_ ENABLEEMAILADDR**</dt></span><span class="sxs-lookup"><span data-stu-id="fa2b2-119"><dt>**AURL\_ENABLEEMAILADDR**</dt></span></span> </dl>          | <span data-ttu-id="fa2b2-120">**Windows 8**：辨識電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-120">**Windows 8**: Recognize email addresses.</span></span><br/>                                                                                                                                |
| <span id="AURL_ENABLETELNO"></span><span id="aurl_enabletelno"></span><dl> <span data-ttu-id="fa2b2-121"><dt>**AURL \_ ENABLETELNO**</dt></span><span class="sxs-lookup"><span data-stu-id="fa2b2-121"><dt>**AURL\_ENABLETELNO**</dt></span></span> </dl>                      | <span data-ttu-id="fa2b2-122">**Windows 8**：辨識電話號碼。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-122">**Windows 8**: Recognize telephone numbers.</span></span><br/>                                                                                                                              |
| <span id="AURL_ENABLEURL"></span><span id="aurl_enableurl"></span><dl> <span data-ttu-id="fa2b2-123"><dt>**AURL \_ ENABLEURL**</dt></span><span class="sxs-lookup"><span data-stu-id="fa2b2-123"><dt>**AURL\_ENABLEURL**</dt></span></span> </dl>                            | <span data-ttu-id="fa2b2-124">**Windows 8**：辨識包含路徑的 url。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-124">**Windows 8**: Recognize URLs that include the path.</span></span><br/>                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="fa2b2-125">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa2b2-125">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa2b2-126">此參數會決定 **AURL \_ ENABLEURL** 是否為使用中時，可辨識的 URL 架構。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-126">This parameter determines the URL schemes recognized if **AURL\_ENABLEURL** is active.</span></span> <span data-ttu-id="fa2b2-127">如果 *lParam* 為 Null，則會使用預設的配置名稱清單 (請參閱備註) 。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-127">If *lParam* is NULL, the default scheme name list is used (see Remarks).</span></span> <span data-ttu-id="fa2b2-128">或者， *lParam* 可指向以 null 終止的字串，其中包含最多50個以冒號結束的架構名稱，以取代預設的配置名稱清單。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-128">Alternatively, *lParam* can point to a null-terminated string consisting of up to 50 colon-terminated scheme names that supersede the default scheme name list.</span></span> <span data-ttu-id="fa2b2-129">例如，字串可以是 "news： HTTP： ftp： telnet："。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-129">For example, the string could be "news:http:ftp:telnet:".</span></span> <span data-ttu-id="fa2b2-130">配置名稱語法定義于 [統一資源識別項 (URI) ：]( https://www.ietf.org/rfc/rfc2396.txt) 網際網路工程任務推動 (小組) 網站上的一般語法檔。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-130">The scheme name syntax is defined in the [Uniform Resource Identifiers (URI): Generic Syntax]( https://www.ietf.org/rfc/rfc2396.txt) document on The Internet Engineering Task Force (IETF) website.</span></span> <span data-ttu-id="fa2b2-131">具體來說，配置名稱最多可以包含13個字元 (包括冒號) 、必須以 ASCII 字母開頭，且後面可以加上 ASCII Alphabetics、數位和三個標點符號字元： "."、"+" 和 "-"。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-131">Specifically, a scheme name can contain up to 13 characters (including the colon), must start with an ASCII alphabetic, and can be followed by a mixture of ASCII alphabetics, digits, and the three punctuation characters: ".", "+", and "-".</span></span> <span data-ttu-id="fa2b2-132">字串類型可以是 **char \** _ 或 _*WCHAR \*\*_; rich edit 控制項會自動偵測型別。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-132">The string type can be either **char\** _ or _*WCHAR\*\*_; the rich edit control automatically detects the type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa2b2-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa2b2-133">Return value</span></span>

<span data-ttu-id="fa2b2-134">如果訊息成功，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-134">If the message succeeds, the return value is zero.</span></span>

<span data-ttu-id="fa2b2-135">如果訊息失敗，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-135">If the message fails, the return value is a nonzero value.</span></span> <span data-ttu-id="fa2b2-136">例如，訊息可能會因為記憶體不足、不正確偵測選項或不正確配置名稱字串而失敗。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-136">For example, the message might fail due to insufficient memory, an invalid detection option, or an invalid scheme-name string.</span></span>

<span data-ttu-id="fa2b2-137">如果 _lParam \* 包含50個以上的配置名稱，訊息會失敗，並傳回值為 **E \_ INVALIDARG**。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-137">If _lParam\* contains more than 50 scheme names, the message fails with a return value of **E\_INVALIDARG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa2b2-138">備註</span><span class="sxs-lookup"><span data-stu-id="fa2b2-138">Remarks</span></span>

<span data-ttu-id="fa2b2-139">如果啟用了自動 URL 偵測 (也就是， *wParam* 包括 **AURL \_ ENABLEURL**) ，rich edit 控制項會掃描任何修改過的文字，以判斷文字是否符合 URL 的格式 (或更常用於 WINDOWS 8 或更新版本的 IRI 國際資源識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-139">If automatic URL detection is enabled (that is, *wParam* includes **AURL\_ENABLEURL**), the rich edit control scans any modified text to determine whether the text matches the format of a URL (or more generally in Windows 8 or later an IRI International Resource Identifier).</span></span> <span data-ttu-id="fa2b2-140">如果 *lParam* 為 Null，則控制項會偵測開頭為下列配置名稱的 url：</span><span class="sxs-lookup"><span data-stu-id="fa2b2-140">If *lParam* is NULL, the control detects URLs that begin with the following scheme names:</span></span>

-   <span data-ttu-id="fa2b2-141">callto</span><span class="sxs-lookup"><span data-stu-id="fa2b2-141">callto</span></span>
-   <span data-ttu-id="fa2b2-142">file</span><span class="sxs-lookup"><span data-stu-id="fa2b2-142">file</span></span>
-   <span data-ttu-id="fa2b2-143">ftp</span><span class="sxs-lookup"><span data-stu-id="fa2b2-143">ftp</span></span>
-   <span data-ttu-id="fa2b2-144">gopher</span><span class="sxs-lookup"><span data-stu-id="fa2b2-144">gopher</span></span>
-   <span data-ttu-id="fa2b2-145">http</span><span class="sxs-lookup"><span data-stu-id="fa2b2-145">http</span></span>
-   <span data-ttu-id="fa2b2-146">https</span><span class="sxs-lookup"><span data-stu-id="fa2b2-146">https</span></span>
-   <span data-ttu-id="fa2b2-147">mailto</span><span class="sxs-lookup"><span data-stu-id="fa2b2-147">mailto</span></span>
-   <span data-ttu-id="fa2b2-148">新聞</span><span class="sxs-lookup"><span data-stu-id="fa2b2-148">news</span></span>
-   <span data-ttu-id="fa2b2-149">版本</span><span class="sxs-lookup"><span data-stu-id="fa2b2-149">notes</span></span>
-   <span data-ttu-id="fa2b2-150">nntp</span><span class="sxs-lookup"><span data-stu-id="fa2b2-150">nntp</span></span>
-   <span data-ttu-id="fa2b2-151">onenote</span><span class="sxs-lookup"><span data-stu-id="fa2b2-151">onenote</span></span>
-   <span data-ttu-id="fa2b2-152">Outlook</span><span class="sxs-lookup"><span data-stu-id="fa2b2-152">outlook</span></span>
-   <span data-ttu-id="fa2b2-153">普洛斯彼羅</span><span class="sxs-lookup"><span data-stu-id="fa2b2-153">prospero</span></span>
-   <span data-ttu-id="fa2b2-154">tel</span><span class="sxs-lookup"><span data-stu-id="fa2b2-154">tel</span></span>
-   <span data-ttu-id="fa2b2-155">telnet</span><span class="sxs-lookup"><span data-stu-id="fa2b2-155">telnet</span></span>
-   <span data-ttu-id="fa2b2-156">wais</span><span class="sxs-lookup"><span data-stu-id="fa2b2-156">wais</span></span>
-   <span data-ttu-id="fa2b2-157">webcal</span><span class="sxs-lookup"><span data-stu-id="fa2b2-157">webcal</span></span>

<span data-ttu-id="fa2b2-158">啟用自動連結偵測時，rich edit 控制項會從沒有控制項可辨識之格式的修改文字中移除 **CFE \_ 連結** 效果。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-158">When automatic link detection is enabled, the rich edit control removes the **CFE\_LINK** effect from modified text that does not have a format recognized by the control.</span></span> <span data-ttu-id="fa2b2-159">如果您的應用程式使用 **CFE \_ 連結** 效果來標示其他類型的文字，請不要啟用自動連結偵測。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-159">If your application uses the **CFE\_LINK** effect to mark other types of text, do not enable automatic link detection.</span></span> <span data-ttu-id="fa2b2-160">Rich edit 控制項不會檢查偵測到的連結是否存在;該責任屬於用戶端。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-160">The rich edit control does not check whether a detected link exists; that responsibility belongs to the client.</span></span>

<span data-ttu-id="fa2b2-161">當滑鼠指標停留在具有 **CFE \_ 連結** 效果的文字上方時，rich Edit 控制項會傳送 [en-us \_ 連結](en-link.md)通知。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-161">A rich edit control sends the [EN\_LINK](en-link.md) notification when it receives various messages while the mouse pointer is over text that has the **CFE\_LINK** effect.</span></span> <span data-ttu-id="fa2b2-162">如需詳細資訊，請參閱 [自動 RichEdit 超連結](/archive/blogs/murrays/automatic-richedit-hyperlinks) 和 [RichEdit 易記名稱超連結](/archive/blogs/murrays/richedit-friendly-name-hyperlinks)。</span><span class="sxs-lookup"><span data-stu-id="fa2b2-162">For more information, see [Automatic RichEdit Hyperlinks](/archive/blogs/murrays/automatic-richedit-hyperlinks) and [RichEdit Friendly Name Hyperlinks](/archive/blogs/murrays/richedit-friendly-name-hyperlinks).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa2b2-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa2b2-163">Requirements</span></span>



| <span data-ttu-id="fa2b2-164">需求</span><span class="sxs-lookup"><span data-stu-id="fa2b2-164">Requirement</span></span> | <span data-ttu-id="fa2b2-165">值</span><span class="sxs-lookup"><span data-stu-id="fa2b2-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa2b2-166">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa2b2-166">Minimum supported client</span></span><br/> | <span data-ttu-id="fa2b2-167">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa2b2-167">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fa2b2-168">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa2b2-168">Minimum supported server</span></span><br/> | <span data-ttu-id="fa2b2-169">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa2b2-169">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fa2b2-170">標頭</span><span class="sxs-lookup"><span data-stu-id="fa2b2-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa2b2-171"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa2b2-171"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa2b2-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa2b2-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa2b2-173">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="fa2b2-173">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

[<span data-ttu-id="fa2b2-174">EN \_ 連結</span><span class="sxs-lookup"><span data-stu-id="fa2b2-174">EN\_LINK</span></span>](en-link.md)
</dt> </dl>

 

