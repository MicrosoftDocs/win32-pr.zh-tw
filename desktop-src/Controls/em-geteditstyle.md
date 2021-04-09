---
title: 'EM_GETEDITSTYLE 訊息 (Richedit .h) '
description: 抓取目前的編輯樣式旗標。
ms.assetid: 568e51a4-0767-4a59-bf34-bc0281b5fe65
keywords:
- EM_GETEDITSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9264338ea525cc0165e1ed942d90654b95357b17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025211"
---
# <a name="em_geteditstyle-message"></a><span data-ttu-id="826ee-104">EM \_ GETEDITSTYLE 訊息</span><span class="sxs-lookup"><span data-stu-id="826ee-104">EM\_GETEDITSTYLE message</span></span>

<span data-ttu-id="826ee-105">抓取目前的編輯樣式旗標。</span><span class="sxs-lookup"><span data-stu-id="826ee-105">Retrieves the current edit style flags.</span></span>

## <a name="parameters"></a><span data-ttu-id="826ee-106">參數</span><span class="sxs-lookup"><span data-stu-id="826ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="826ee-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="826ee-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="826ee-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="826ee-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="826ee-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="826ee-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="826ee-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="826ee-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="826ee-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="826ee-111">Return value</span></span>

<span data-ttu-id="826ee-112">傳回目前的編輯樣式旗標，其中可包含下列一或多個值：</span><span class="sxs-lookup"><span data-stu-id="826ee-112">Returns the current edit style flags, which can include one or more of the following values:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="826ee-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="826ee-113">Return code</span></span></th>
<th><span data-ttu-id="826ee-114">Description</span><span class="sxs-lookup"><span data-stu-id="826ee-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="826ee-115"><dt><strong>SES_BEEPONMAXTEXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-115"><dt><strong>SES_BEEPONMAXTEXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-116">如果使用者嘗試輸入的字元數超過最大值，Rich Edit 將會呼叫系統 beeper。</span><span class="sxs-lookup"><span data-stu-id="826ee-116">Rich Edit will call the system beeper if the user attempts to enter more than the maximum characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="826ee-117"><dt><strong>SES_BIDI</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-117"><dt><strong>SES_BIDI</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-118">開啟雙向處理。</span><span class="sxs-lookup"><span data-stu-id="826ee-118">Turns on bidirectional processing.</span></span> <span data-ttu-id="826ee-119">如果下列任一視窗樣式為作用中，就會自動開啟此功能： <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>、 <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a> <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="826ee-119">This is automatically turned on by Rich Edit if any of the following window styles are active: <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>.</span></span> <span data-ttu-id="826ee-120">不過，使用 <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>ITextHost</strong></a> 的自訂執行時，這項設定適用于處理這些視窗樣式 (預設值： 0) 。</span><span class="sxs-lookup"><span data-stu-id="826ee-120">However, this setting is useful for handling these window styles when using a custom implementation of <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>ITextHost</strong></a> (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="826ee-121"><dt><strong>SES_CTFALLOWEMBED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-121"><dt><strong>SES_CTFALLOWEMBED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-122"><strong>WINDOWS XP （含 SP1</strong>）：允許使用 TSF 插入內嵌物件 (預設值： 0) 。</span><span class="sxs-lookup"><span data-stu-id="826ee-122"><strong>Windows XP with SP1</strong>: Allow embedded objects to be inserted using TSF (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="826ee-123"><dt><strong>SES_CTFALLOWPROOFING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-123"><dt><strong>SES_CTFALLOWPROOFING</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-124"><strong>WINDOWS XP （含 SP1</strong>）：允許 TSF 的校對提示 (預設值： 0) 。</span><span class="sxs-lookup"><span data-stu-id="826ee-124"><strong>Windows XP with SP1</strong>: Allows TSF proofing tips (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="826ee-125"><dt><strong>SES_CTFALLOWSMARTTAG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-125"><dt><strong>SES_CTFALLOWSMARTTAG</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-126"><strong>WINDOWS XP （含 SP1</strong>）：允許 TSF 的智慧標籤提示 (預設值： 0) 。</span><span class="sxs-lookup"><span data-stu-id="826ee-126"><strong>Windows XP with SP1</strong>: Allows TSF SmartTag tips (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="826ee-127"><dt><strong>SES_CTFNOLOCK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-127"><dt><strong>SES_CTFNOLOCK</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-128"><strong>Windows 8</strong>：不允許 TSF 鎖定讀取/寫入存取。</span><span class="sxs-lookup"><span data-stu-id="826ee-128"><strong>Windows 8</strong>: Do not allow the TSF lock read/write access.</span></span> <span data-ttu-id="826ee-129">這會暫停 TSF 輸入。</span><span class="sxs-lookup"><span data-stu-id="826ee-129">This pauses TSF input.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="826ee-130"><dt><strong>SES_DEFAULTLATINLIGA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-130"><dt><strong>SES_DEFAULTLATINLIGA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-131"><strong>Windows 8</strong>：使用預設 OpenType 功能來顯示具有 wi-fi 連字的字型，以產生改良的印刷樣式 (預設值： 0) 。</span><span class="sxs-lookup"><span data-stu-id="826ee-131"><strong>Windows 8</strong>: Fonts with an fi ligature are displayed with default OpenType features resulting in improved typography (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="826ee-132"><dt><strong>SES_DRAFTMODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-132"><dt><strong>SES_DRAFTMODE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-133"><strong>WINDOWS XP （含 SP1</strong>）：使用草稿模式字型來顯示文字。</span><span class="sxs-lookup"><span data-stu-id="826ee-133"><strong>Windows XP with SP1</strong>: Use draft mode fonts to display text.</span></span> <span data-ttu-id="826ee-134">草稿模式是一個協助工具選項，可讓控制項顯示具有單一字型的文字;字型是由訊息方塊中所使用之字型的系統設定所決定。</span><span class="sxs-lookup"><span data-stu-id="826ee-134">Draft mode is an accessibility option where the control displays the text with a single font; the font is determined by the system setting for the font used in message boxes.</span></span> <span data-ttu-id="826ee-135">例如，可存取的使用者可以更輕鬆地讀取文字，而不是將字型和樣式混合 (預設值： 0) 。</span><span class="sxs-lookup"><span data-stu-id="826ee-135">For example, accessible users may read text easier if it is uniform, rather than a mix of fonts and styles (default: 0).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="826ee-136"><dt><strong>SES_EMULATE10</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-136"><dt><strong>SES_EMULATE10</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-137"><strong>Windows 8</strong>：模擬 RichEdit 1.0 行為。</span><span class="sxs-lookup"><span data-stu-id="826ee-137"><strong>Windows 8</strong>: Emulate RichEdit 1.0 behavior.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="826ee-138">如果您真的想要此行為，請使用 Windows riched32.dll，而不是 riched20.dll 或 msftedit.dll。</span><span class="sxs-lookup"><span data-stu-id="826ee-138">If you really want this behavior, use the Windows riched32.dll instead of riched20.dll or msftedit.dll.</span></span> <span data-ttu-id="826ee-139">Riched32.dll 有更多功能。</span><span class="sxs-lookup"><span data-stu-id="826ee-139">Riched32.dll had more functionality.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="826ee-140"><dt><strong>SES_EMULATESYSEDIT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-140"><dt><strong>SES_EMULATESYSEDIT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-141">當這個位開啟時，豐富的編輯會嘗試模擬系統編輯控制項 (預設值： 0) 。</span><span class="sxs-lookup"><span data-stu-id="826ee-141">When this bit is on, rich edit attempts to emulate the system edit control (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="826ee-142"><dt><strong>SES_EXTENDBACKCOLOR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-142"><dt><strong>SES_EXTENDBACKCOLOR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-143">將背景色彩全部延伸至用戶端矩形的邊緣 (預設值： 0) 。</span><span class="sxs-lookup"><span data-stu-id="826ee-143">Extends the background color all the way to the edges of the client rectangle (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="826ee-144"><dt><strong>SES_HIDEGRIDLINES</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-144"><dt><strong>SES_HIDEGRIDLINES</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-145"><strong>WINDOWS XP （含 SP1</strong>）：如果資料表格線的寬度為零，則不會顯示格線。</span><span class="sxs-lookup"><span data-stu-id="826ee-145"><strong>Windows XP with SP1</strong>: If the width of table gridlines is zero, gridlines are not displayed.</span></span> <span data-ttu-id="826ee-146">這相當於 Word 的 [表格] 功能表中的 [隱藏格線] 功能 (預設值： 0) 。</span><span class="sxs-lookup"><span data-stu-id="826ee-146">This is equivalent to the hide gridlines feature in Word's table menu (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="826ee-147"><dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-147"><dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-148"><strong>Windows 8</strong>：當游標停留在連結上時，會顯示具有目標連結位址的工具提示 (預設值： 0) 。</span><span class="sxs-lookup"><span data-stu-id="826ee-148"><strong>Windows 8</strong>: When the cursor is over a link, display a tooltip with the target link address (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="826ee-149"><dt><strong>SES_LOGICALCARET</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-149"><dt><strong>SES_LOGICALCARET</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-150"><strong>Windows 8</strong>：提供邏輯插入號資訊，而不是插入號點陣圖，如 <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>ITextHost：： TxSetCaretPos</strong></a> (default： 0) 所述。</span><span class="sxs-lookup"><span data-stu-id="826ee-150"><strong>Windows 8</strong>: Provide logical caret information instead of a caret bitmap as described in <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>ITextHost::TxSetCaretPos</strong></a> (default: 0).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="826ee-151"><dt><strong>SES_LOWERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-151"><dt><strong>SES_LOWERCASE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-152">將所有輸入字元轉換成小寫 (預設值： 0) 。</span><span class="sxs-lookup"><span data-stu-id="826ee-152">Converts all input characters to lowercase (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="826ee-153"><dt><strong>SES_MAPCPS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-153"><dt><strong>SES_MAPCPS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-154">已過時。</span><span class="sxs-lookup"><span data-stu-id="826ee-154">Obsolete.</span></span> <span data-ttu-id="826ee-155">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="826ee-155">Do not use.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="826ee-156"><dt><strong>SES_MULTISELECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-156"><dt><strong>SES_MULTISELECT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-157"><strong>Windows 8</strong>：啟用多重選取，並在按下 Ctrl 鍵時進行個別選取 (預設： 0) 。</span><span class="sxs-lookup"><span data-stu-id="826ee-157"><strong>Windows 8</strong>: Enable multiselection with individual mouse selections made while the Ctrl key is pressed (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="826ee-158"><dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-158"><dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-159"><strong>Windows 8</strong>：不要調整東亞文字的行高 (預設值：0，將行高調整為 15% ) 。</span><span class="sxs-lookup"><span data-stu-id="826ee-159"><strong>Windows 8</strong>: Do not adjust line height for East Asian text (default: 0 which adjusts the line height by 15%).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="826ee-160"><dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-160"><dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-161">從沒有焦點的連結傳送 <a href="en-link.md">EN_LINK</a> 通知。</span><span class="sxs-lookup"><span data-stu-id="826ee-161">Sends <a href="en-link.md">EN_LINK</a> notification from links that do not have focus.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="826ee-162"><dt><strong>SES_NOIME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-162"><dt><strong>SES_NOIME</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-163">不允許這個 rich edit 控制項實例的 Ime (預設值： 0) 。</span><span class="sxs-lookup"><span data-stu-id="826ee-163">Disallows IMEs for this instance of the rich edit control (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="826ee-164"><dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-164"><dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-165">當這個位開啟時，rich edit 不會驗證輸入文字的順序。</span><span class="sxs-lookup"><span data-stu-id="826ee-165">When this bit is on, rich edit does not verify the sequence of typed text.</span></span> <span data-ttu-id="826ee-166">某些語言 (例如泰文和越南) 需要先驗證輸入順序，再將它提交至備份存放區 (預設值： 0) 。</span><span class="sxs-lookup"><span data-stu-id="826ee-166">Some languages (such as Thai and Vietnamese) require verifying the input sequence order before submitting it to the backing store (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="826ee-167"><dt><strong>SES_SCROLLONKILLFOCUS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-167"><dt><strong>SES_SCROLLONKILLFOCUS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-168">發生 KillFocus 時，請將文字的開頭 (字元位置等於 0)  (預設值： 0) 。</span><span class="sxs-lookup"><span data-stu-id="826ee-168">When KillFocus occurs, scroll to the beginning of the text (character position equal to 0) (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="826ee-169"><dt><strong>SES_SMARTDRAGDROP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-169"><dt><strong>SES_SMARTDRAGDROP</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-170"><strong>Windows 8</strong>：在卸載文字 (預設值： 0) 時，根據內容新增或刪除空格。</span><span class="sxs-lookup"><span data-stu-id="826ee-170"><strong>Windows 8</strong>: Add or delete a space according to the context when dropping text (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="826ee-171"><dt><strong>SES_USECRLF</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-171"><dt><strong>SES_USECRLF</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-172">已過時。</span><span class="sxs-lookup"><span data-stu-id="826ee-172">Obsolete.</span></span> <span data-ttu-id="826ee-173">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="826ee-173">Do not use.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="826ee-174"><dt><strong>SES_WORDDRAGDROP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-174"><dt><strong>SES_WORDDRAGDROP</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-175"><strong>Windows 8</strong>：如果 [word 選取] 為 [使用中]，請確定放置位置位於單字界限 (預設值： 0) 。</span><span class="sxs-lookup"><span data-stu-id="826ee-175"><strong>Windows 8</strong>: If word select is active, ensure that the drop location is at a word boundary (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="826ee-176"><dt><strong>SES_UPPERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-176"><dt><strong>SES_UPPERCASE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-177">將所有輸入字元轉換成大寫 (預設值： 0) 。</span><span class="sxs-lookup"><span data-stu-id="826ee-177">Converts all input characters to uppercase (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="826ee-178"><dt><strong>SES_USEAIMM</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-178"><dt><strong>SES_USEAIMM</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-179">使用隨附于 Internet Explorer 4.0 或更新版本的主動式 IMM 輸入方法元件 (預設值： 0) 。</span><span class="sxs-lookup"><span data-stu-id="826ee-179">Uses the Active IMM input method component that ships with Internet Explorer 4.0 or later (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="826ee-180"><dt><strong>SES_USEATFONT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-180"><dt><strong>SES_USEATFONT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-181"><strong>WINDOWS XP （含 SP1</strong>）：使用 @ 字型，其設計目的為垂直文字;這會與 <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> 視窗樣式搭配使用。</span><span class="sxs-lookup"><span data-stu-id="826ee-181"><strong>Windows XP with SP1</strong>: Uses an @ font, which is designed for vertical text; this is used with the <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> window style.</span></span> <span data-ttu-id="826ee-182">@ 字型的名稱是以 @ 符號開頭，例如 &quot; @Batang &quot; (預設值：0，但是會自動開啟垂直文字配置) 。</span><span class="sxs-lookup"><span data-stu-id="826ee-182">The name of an @ font begins with the @ symbol, for example, &quot;@Batang&quot; (default: 0, but is automatically turned on for vertical text layout).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="826ee-183"><dt><strong>SES_USECTF</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-183"><dt><strong>SES_USECTF</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-184"><strong>WINDOWS XP （含 SP1</strong>）：開啟 TSF 支援。</span><span class="sxs-lookup"><span data-stu-id="826ee-184"><strong>Windows XP with SP1</strong>: Turns on TSF support.</span></span> <span data-ttu-id="826ee-185"> (預設值： 0) </span><span class="sxs-lookup"><span data-stu-id="826ee-185">(default: 0)</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="826ee-186"><dt><strong>SES_XLTCRCRLFTOCR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="826ee-186"><dt><strong>SES_XLTCRCRLFTOCR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="826ee-187">開啟將 CRCRLFs 轉譯為 CRs。</span><span class="sxs-lookup"><span data-stu-id="826ee-187">Turns on translation of CRCRLFs to CRs.</span></span> <span data-ttu-id="826ee-188">當這個位開啟且已讀取檔案時，CRCRLF 的所有實例都會在內部轉換成硬性 CRs。</span><span class="sxs-lookup"><span data-stu-id="826ee-188">When this bit is on and a file is read in, all instances of CRCRLF will be converted to hard CRs internally.</span></span> <span data-ttu-id="826ee-189">這會影響文字換行。</span><span class="sxs-lookup"><span data-stu-id="826ee-189">This will affect the text wrapping.</span></span> <span data-ttu-id="826ee-190">請注意，如果這類檔案儲存為純文字，則 CRs 將會被 CRLFs 取代。</span><span class="sxs-lookup"><span data-stu-id="826ee-190">Note that if such a file is saved as plain text, the CRs will be replaced by CRLFs.</span></span> <span data-ttu-id="826ee-191">這是純文字的 .txt 標準 (預設值：0，會刪除輸入) 上的 CRCRLFs。</span><span class="sxs-lookup"><span data-stu-id="826ee-191">This is the .txt standard for plain text (default: 0, which deletes CRCRLFs on input).</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="826ee-192">規格需求</span><span class="sxs-lookup"><span data-stu-id="826ee-192">Requirements</span></span>



| <span data-ttu-id="826ee-193">需求</span><span class="sxs-lookup"><span data-stu-id="826ee-193">Requirement</span></span> | <span data-ttu-id="826ee-194">值</span><span class="sxs-lookup"><span data-stu-id="826ee-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="826ee-195">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="826ee-195">Minimum supported client</span></span><br/> | <span data-ttu-id="826ee-196">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="826ee-196">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="826ee-197">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="826ee-197">Minimum supported server</span></span><br/> | <span data-ttu-id="826ee-198">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="826ee-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="826ee-199">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="826ee-199">Redistributable</span></span><br/>          | <span data-ttu-id="826ee-200">Rich Edit 3。0</span><span class="sxs-lookup"><span data-stu-id="826ee-200">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="826ee-201">標頭</span><span class="sxs-lookup"><span data-stu-id="826ee-201">Header</span></span><br/>                   | <dl> <span data-ttu-id="826ee-202"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="826ee-202"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="826ee-203">另請參閱</span><span class="sxs-lookup"><span data-stu-id="826ee-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="826ee-204">**EM \_ SETEDITSTYLE**</span><span class="sxs-lookup"><span data-stu-id="826ee-204">**EM\_SETEDITSTYLE**</span></span>](em-seteditstyle.md)
</dt> </dl>

 

