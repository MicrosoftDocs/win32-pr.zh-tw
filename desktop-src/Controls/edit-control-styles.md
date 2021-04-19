---
title: '編輯控制項樣式 (Winuser .h) '
description: 若要使用 CreateWindow 或 CreateWindowEx 函數來建立編輯控制項，請指定編輯類別、適當的視窗樣式常數，以及下列編輯控制項樣式的組合。
ms.assetid: 336c69b7-bc23-4b93-8968-ad63a1703385
topic_type:
- apiref
api_name:
- ES_AUTOHSCROLL
- ES_AUTOVSCROLL
- ES_CENTER
- ES_LEFT
- ES_LOWERCASE
- ES_MULTILINE
- ES_NOHIDESEL
- ES_NUMBER
- ES_OEMCONVERT
- ES_PASSWORD
- ES_READONLY
- ES_RIGHT
- ES_UPPERCASE
- ES_WANTRETURN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 9b255aee665c32f9a14be4946dee0122dad626bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993312"
---
# <a name="edit-control-styles"></a><span data-ttu-id="1dd48-103">編輯控制項樣式</span><span class="sxs-lookup"><span data-stu-id="1dd48-103">Edit Control Styles</span></span>

<span data-ttu-id="1dd48-104">若要使用 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數來建立編輯控制項，請指定編輯類別、適當的視窗樣式常數，以及下列編輯控制項樣式的組合。</span><span class="sxs-lookup"><span data-stu-id="1dd48-104">To create an edit control using the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specify the EDIT class, appropriate window style constants, and a combination of the following edit control styles.</span></span> <span data-ttu-id="1dd48-105">建立控制項之後，除非有注明，否則無法修改這些樣式。</span><span class="sxs-lookup"><span data-stu-id="1dd48-105">After the control has been created, these styles cannot be modified, except as noted.</span></span>

## <a name="example"></a><span data-ttu-id="1dd48-106">範例</span><span class="sxs-lookup"><span data-stu-id="1dd48-106">Example</span></span>

```cpp
LRESULT MsgCreate(HWND hwnd, UINT uMessage, WPARAM wparam, LPARAM lparam)
{
    lparam;
    wparam;
    uMessage;

    // Create Edit control for typing to be sent to server
    if (NULL == (hOutWnd = CreateWindow("EDIT",
                           NULL,
                           WS_BORDER | WS_CHILD | WS_VISIBLE | WS_VSCROLL | ES_LEFT | 
                           ES_MULTILINE | ES_AUTOVSCROLL,
                           0,0,0,0,
                           hwnd,
                           (HMENU) ID_OUTBOX,
                           (HINSTANCE) GetWindowLongPtr(hwnd, GWLP_HINSTANCE),
                           NULL)))
        return FALSE;
    return TRUE;
}
```

<span data-ttu-id="1dd48-107">從 GitHub 上的 [Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) 取得的範例。</span><span class="sxs-lookup"><span data-stu-id="1dd48-107">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) on GitHub.</span></span>

## <a name="constants"></a><span data-ttu-id="1dd48-108">常數</span><span class="sxs-lookup"><span data-stu-id="1dd48-108">Constants</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="1dd48-109">常數</span><span class="sxs-lookup"><span data-stu-id="1dd48-109">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="1dd48-110">描述</span><span class="sxs-lookup"><span data-stu-id="1dd48-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl> <span data-ttu-id="1dd48-111"><dt><strong>ES_AUTOHSCROLL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1dd48-111"><dt><strong>ES_AUTOHSCROLL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1dd48-112">當使用者在行尾輸入字元時，會自動將文字向右滾動10個字元。</span><span class="sxs-lookup"><span data-stu-id="1dd48-112">Automatically scrolls text to the right by 10 characters when the user types a character at the end of the line.</span></span> <span data-ttu-id="1dd48-113">當使用者按下 ENTER 鍵時，控制項會將所有文字滾動回零的位置。</span><span class="sxs-lookup"><span data-stu-id="1dd48-113">When the user presses the ENTER key, the control scrolls all text back to position zero.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl> <span data-ttu-id="1dd48-114"><dt><strong>ES_AUTOVSCROLL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1dd48-114"><dt><strong>ES_AUTOVSCROLL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1dd48-115">當使用者按下最後一行的 ENTER 鍵時，自動將文字向上滾動一個頁面。</span><span class="sxs-lookup"><span data-stu-id="1dd48-115">Automatically scrolls text up one page when the user presses the ENTER key on the last line.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_CENTER"></span><span id="es_center"></span><dl> <span data-ttu-id="1dd48-116"><dt><strong>ES_CENTER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1dd48-116"><dt><strong>ES_CENTER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1dd48-117">在單行或多行編輯控制項中將文字置中。</span><span class="sxs-lookup"><span data-stu-id="1dd48-117">Centers text in a single-line or multiline edit control.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_LEFT"></span><span id="es_left"></span><dl> <span data-ttu-id="1dd48-118"><dt><strong>ES_LEFT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1dd48-118"><dt><strong>ES_LEFT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1dd48-119">將文字對齊左邊界。</span><span class="sxs-lookup"><span data-stu-id="1dd48-119">Aligns text with the left margin.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_LOWERCASE"></span><span id="es_lowercase"></span><dl> <span data-ttu-id="1dd48-120"><dt><strong>ES_LOWERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1dd48-120"><dt><strong>ES_LOWERCASE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1dd48-121">將所有字元轉換成小寫，因為它們是在編輯控制項中輸入的。</span><span class="sxs-lookup"><span data-stu-id="1dd48-121">Converts all characters to lowercase as they are typed into the edit control.</span></span><br/> <span data-ttu-id="1dd48-122">若要在建立控制項之後變更這個樣式，請使用 <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="1dd48-122">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl> <span data-ttu-id="1dd48-123"><dt><strong>ES_MULTILINE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1dd48-123"><dt><strong>ES_MULTILINE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1dd48-124">指定多行編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="1dd48-124">Designates a multiline edit control.</span></span> <span data-ttu-id="1dd48-125">預設值為單行編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="1dd48-125">The default is single-line edit control.</span></span> <br/> <span data-ttu-id="1dd48-126">當多行編輯控制項在對話方塊中，按下 ENTER 鍵的預設回應是啟用預設按鈕。</span><span class="sxs-lookup"><span data-stu-id="1dd48-126">When the multiline edit control is in a dialog box, the default response to pressing the ENTER key is to activate the default button.</span></span> <span data-ttu-id="1dd48-127">若要使用 ENTER 鍵作為回車，請使用 <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> 樣式。</span><span class="sxs-lookup"><span data-stu-id="1dd48-127">To use the ENTER key as a carriage return, use the <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> style.</span></span><br/> <span data-ttu-id="1dd48-128">當多行編輯控制項不在對話方塊中並指定 <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL</strong></a> 樣式時，編輯控制項會盡可能顯示最多行數，並在使用者按下 ENTER 鍵時垂直捲動。</span><span class="sxs-lookup"><span data-stu-id="1dd48-128">When the multiline edit control is not in a dialog box and the <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL</strong></a> style is specified, the edit control shows as many lines as possible and scrolls vertically when the user presses the ENTER key.</span></span> <span data-ttu-id="1dd48-129">如果您未指定 <strong>ES_AUTOVSCROLL</strong>，則編輯控制項會盡可能顯示最多行數，並在沒有其他行可顯示時，于使用者按下 ENTER 鍵時發出嗶聲。</span><span class="sxs-lookup"><span data-stu-id="1dd48-129">If you do not specify <strong>ES_AUTOVSCROLL</strong>, the edit control shows as many lines as possible and beeps if the user presses the ENTER key when no more lines can be displayed.</span></span><br/> <span data-ttu-id="1dd48-130">如果您指定 <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL</strong></a> 樣式，當插入號超過控制項的右邊緣時，多行編輯控制項會自動水準滾動。</span><span class="sxs-lookup"><span data-stu-id="1dd48-130">If you specify the <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL</strong></a> style, the multiline edit control automatically scrolls horizontally when the caret goes past the right edge of the control.</span></span> <span data-ttu-id="1dd48-131">若要開始新的一行，使用者必須按 ENTER 鍵。</span><span class="sxs-lookup"><span data-stu-id="1dd48-131">To start a new line, the user must press the ENTER key.</span></span> <span data-ttu-id="1dd48-132">如果您未指定 <strong>ES_AUTOHSCROLL</strong>，控制項會在必要時自動將文字換行到下一行的開頭。</span><span class="sxs-lookup"><span data-stu-id="1dd48-132">If you do not specify <strong>ES_AUTOHSCROLL</strong>, the control automatically wraps words to the beginning of the next line when necessary.</span></span> <span data-ttu-id="1dd48-133">如果使用者按下 ENTER 鍵，也會啟動新的一行。</span><span class="sxs-lookup"><span data-stu-id="1dd48-133">A new line is also started if the user presses the ENTER key.</span></span> <span data-ttu-id="1dd48-134">視窗大小會決定 Wordwrap 的位置。</span><span class="sxs-lookup"><span data-stu-id="1dd48-134">The window size determines the position of the Wordwrap.</span></span> <span data-ttu-id="1dd48-135">如果視窗大小變更，Wordwrapping 位置會變更，並重新顯示文字。</span><span class="sxs-lookup"><span data-stu-id="1dd48-135">If the window size changes, the Wordwrapping position changes and the text is redisplayed.</span></span><br/> <span data-ttu-id="1dd48-136">多行編輯控制項可以有捲軸。</span><span class="sxs-lookup"><span data-stu-id="1dd48-136">Multiline edit controls can have scroll bars.</span></span> <span data-ttu-id="1dd48-137">具有捲軸的編輯控制項會處理自己的捲軸訊息。</span><span class="sxs-lookup"><span data-stu-id="1dd48-137">An edit control with scroll bars processes its own scroll bar messages.</span></span> <span data-ttu-id="1dd48-138">請注意，不含捲軸的編輯控制項會依照上一段所述的方式進行滾動，並處理父視窗所傳送的任何捲軸訊息。</span><span class="sxs-lookup"><span data-stu-id="1dd48-138">Note that edit controls without scroll bars scroll as described in the previous paragraphs and process any scroll messages sent by the parent window.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl> <span data-ttu-id="1dd48-139"><dt><strong>ES_NOHIDESEL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1dd48-139"><dt><strong>ES_NOHIDESEL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1dd48-140">對編輯控制項的預設行為否定。</span><span class="sxs-lookup"><span data-stu-id="1dd48-140">Negates the default behavior for an edit control.</span></span> <span data-ttu-id="1dd48-141">當控制項失去輸入焦點時，預設行為會隱藏選取範圍，並在控制項收到輸入焦點時反轉選取範圍。</span><span class="sxs-lookup"><span data-stu-id="1dd48-141">The default behavior hides the selection when the control loses the input focus and inverts the selection when the control receives the input focus.</span></span> <span data-ttu-id="1dd48-142">如果您指定 <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>，即使控制項沒有焦點，也會反轉選取的文字。</span><span class="sxs-lookup"><span data-stu-id="1dd48-142">If you specify <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>, the selected text is inverted, even if the control does not have the focus.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_NUMBER"></span><span id="es_number"></span><dl> <span data-ttu-id="1dd48-143"><dt><strong>ES_NUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1dd48-143"><dt><strong>ES_NUMBER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1dd48-144">只允許在編輯控制項中輸入數位。</span><span class="sxs-lookup"><span data-stu-id="1dd48-144">Allows only digits to be entered into the edit control.</span></span> <span data-ttu-id="1dd48-145">請注意，即使使用這個集合，仍然可以在編輯控制項中貼上非數位。</span><span class="sxs-lookup"><span data-stu-id="1dd48-145">Note that, even with this set, it is still possible to paste non-digits into the edit control.</span></span> <br/> <span data-ttu-id="1dd48-146">若要在建立控制項之後變更這個樣式，請使用 <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="1dd48-146">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/> <span data-ttu-id="1dd48-147">若要將輸入的文字轉譯為整數值，請使用 <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>GetDlgItemInt</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="1dd48-147">To translate text that was entered into the edit control to an integer value, use the <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>GetDlgItemInt</strong></a> function.</span></span> <span data-ttu-id="1dd48-148">若要將編輯控制項的文字設定為指定之整數的字串表示，請使用 <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>SetDlgItemInt</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="1dd48-148">To set the text of the edit control to the string representation of a specified integer, use the <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>SetDlgItemInt</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_OEMCONVERT"></span><span id="es_oemconvert"></span><dl> <span data-ttu-id="1dd48-149"><dt><strong>ES_OEMCONVERT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1dd48-149"><dt><strong>ES_OEMCONVERT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1dd48-150">轉換在編輯控制項中輸入的文字。</span><span class="sxs-lookup"><span data-stu-id="1dd48-150">Converts text entered in the edit control.</span></span> <span data-ttu-id="1dd48-151">文字會從 Windows 字元集轉換成 OEM 字元集，然後再轉換回 Windows 字元集。</span><span class="sxs-lookup"><span data-stu-id="1dd48-151">The text is converted from the Windows character set to the OEM character set and then back to the Windows character set.</span></span> <span data-ttu-id="1dd48-152">這可確保當應用程式呼叫 <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> 函式將編輯控制項中的 Windows 字串轉換成 OEM 字元時，會進行適當的字元轉換。</span><span class="sxs-lookup"><span data-stu-id="1dd48-152">This ensures proper character conversion when the application calls the <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> function to convert a Windows string in the edit control to OEM characters.</span></span> <span data-ttu-id="1dd48-153">如果編輯控制項包含的檔案名將會用於不支援 Unicode 的檔案系統，此樣式最適合用。</span><span class="sxs-lookup"><span data-stu-id="1dd48-153">This style is most useful for edit controls that contain file names that will be used on file systems that do not support Unicode.</span></span> <br/> <span data-ttu-id="1dd48-154">若要在建立控制項之後變更這個樣式，請使用 <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="1dd48-154">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_PASSWORD"></span><span id="es_password"></span><dl> <span data-ttu-id="1dd48-155"><dt><strong>ES_PASSWORD</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1dd48-155"><dt><strong>ES_PASSWORD</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1dd48-156">針對輸入編輯控制項的每個字元，顯示星號 ( \* ) 。</span><span class="sxs-lookup"><span data-stu-id="1dd48-156">Displays an asterisk (\*) for each character typed into the edit control.</span></span> <span data-ttu-id="1dd48-157">這個樣式只對單行編輯控制項有效。</span><span class="sxs-lookup"><span data-stu-id="1dd48-157">This style is valid only for single-line edit controls.</span></span> <br/> <span data-ttu-id="1dd48-158">若要變更顯示的字元，或設定或清除此樣式，請使用 <a href="em-setpasswordchar.md"><strong>EM_SETPASSWORDCHAR</strong></a> 的訊息。</span><span class="sxs-lookup"><span data-stu-id="1dd48-158">To change the characters that is displayed, or set or clear this style, use the <a href="em-setpasswordchar.md"><strong>EM_SETPASSWORDCHAR</strong></a> message.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1dd48-159">若要使用 Comctl32.dll 第6版，請在資訊清單中指定它。</span><span class="sxs-lookup"><span data-stu-id="1dd48-159">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="1dd48-160">如需資訊清單的詳細資訊，請參閱 <a href="cookbook-overview.md">啟用視覺化樣式</a>。</span><span class="sxs-lookup"><span data-stu-id="1dd48-160">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_READONLY"></span><span id="es_readonly"></span><dl> <span data-ttu-id="1dd48-161"><dt><strong>ES_READONLY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1dd48-161"><dt><strong>ES_READONLY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1dd48-162">防止使用者輸入或編輯編輯控制項中的文字。</span><span class="sxs-lookup"><span data-stu-id="1dd48-162">Prevents the user from typing or editing text in the edit control.</span></span><br/> <span data-ttu-id="1dd48-163">若要在建立控制項之後變更這個樣式，請使用 <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> 訊息。</span><span class="sxs-lookup"><span data-stu-id="1dd48-163">To change this style after the control has been created, use the <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> message.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_RIGHT"></span><span id="es_right"></span><dl> <span data-ttu-id="1dd48-164"><dt><strong>ES_RIGHT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1dd48-164"><dt><strong>ES_RIGHT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1dd48-165">在單行或多行編輯控制項中靠右對齊文字。</span><span class="sxs-lookup"><span data-stu-id="1dd48-165">Right-aligns text in a single-line or multiline edit control.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_UPPERCASE"></span><span id="es_uppercase"></span><dl> <span data-ttu-id="1dd48-166"><dt><strong>ES_UPPERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1dd48-166"><dt><strong>ES_UPPERCASE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1dd48-167">將所有字元轉換成大寫，因為它們是在編輯控制項中輸入的。</span><span class="sxs-lookup"><span data-stu-id="1dd48-167">Converts all characters to uppercase as they are typed into the edit control.</span></span> <br/> <span data-ttu-id="1dd48-168">若要在建立控制項之後變更這個樣式，請使用 <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="1dd48-168">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl> <span data-ttu-id="1dd48-169"><dt><strong>ES_WANTRETURN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1dd48-169"><dt><strong>ES_WANTRETURN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1dd48-170">指定當使用者在對話方塊中輸入文字至多行編輯控制項時按下 ENTER 鍵時，要插入的回車。</span><span class="sxs-lookup"><span data-stu-id="1dd48-170">Specifies that a carriage return be inserted when the user presses the ENTER key while entering text into a multiline edit control in a dialog box.</span></span> <span data-ttu-id="1dd48-171">如果您未指定此樣式，按下 ENTER 鍵的效果與按下對話方塊的預設推送按鈕相同。</span><span class="sxs-lookup"><span data-stu-id="1dd48-171">If you do not specify this style, pressing the ENTER key has the same effect as pressing the dialog box's default push button.</span></span> <span data-ttu-id="1dd48-172">這個樣式不會影響單行編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="1dd48-172">This style has no effect on a single-line edit control.</span></span> <br/> <span data-ttu-id="1dd48-173">若要在建立控制項之後變更這個樣式，請使用 <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="1dd48-173">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="1dd48-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="1dd48-174">Requirements</span></span>



| <span data-ttu-id="1dd48-175">需求</span><span class="sxs-lookup"><span data-stu-id="1dd48-175">Requirement</span></span> | <span data-ttu-id="1dd48-176">值</span><span class="sxs-lookup"><span data-stu-id="1dd48-176">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1dd48-177">標頭</span><span class="sxs-lookup"><span data-stu-id="1dd48-177">Header</span></span><br/> | <dl> <span data-ttu-id="1dd48-178"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="1dd48-178"><dt>Winuser.h</dt></span></span> </dl> |



