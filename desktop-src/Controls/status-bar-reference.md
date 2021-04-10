---
title: 狀態列
description: 本章節包含與狀態列控制項搭配使用之程式設計項目的相關資訊。
ms.assetid: 77923055-9d00-4528-bda7-b602a26b577f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca6e46f1c573b75439cc10aa27ae3245e47e3de9
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "103683405"
---
# <a name="status-bar"></a><span data-ttu-id="d1a25-103">狀態列</span><span class="sxs-lookup"><span data-stu-id="d1a25-103">Status Bar</span></span>

<span data-ttu-id="d1a25-104">本章節包含與狀態列控制項搭配使用之程式設計項目的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d1a25-104">This section contains information about the programming elements used with status bar controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="d1a25-105">概觀</span><span class="sxs-lookup"><span data-stu-id="d1a25-105">Overviews</span></span>



| <span data-ttu-id="d1a25-106">主題</span><span class="sxs-lookup"><span data-stu-id="d1a25-106">Topic</span></span>                          | <span data-ttu-id="d1a25-107">目錄</span><span class="sxs-lookup"><span data-stu-id="d1a25-107">Contents</span></span>                                                                                                                                                   |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1a25-108">狀態列</span><span class="sxs-lookup"><span data-stu-id="d1a25-108">Status Bars</span></span>](status-bars.md) | <span data-ttu-id="d1a25-109">*狀態列* 是父視窗底部的水準視窗，其中應用程式可以顯示各種類型的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="d1a25-109">A *status bar* is a horizontal window at the bottom of a parent window in which an application can display various kinds of status information.</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="d1a25-110">函式</span><span class="sxs-lookup"><span data-stu-id="d1a25-110">Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d1a25-111">主題</span><span class="sxs-lookup"><span data-stu-id="d1a25-111">Topic</span></span></th>
<th><span data-ttu-id="d1a25-112">目錄</span><span class="sxs-lookup"><span data-stu-id="d1a25-112">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d1a25-113"><a href="/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa"><strong>CreateStatusWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1a25-113"><a href="/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa"><strong>CreateStatusWindow</strong></a></span></span></td>
<td><span data-ttu-id="d1a25-114">建立狀態視窗，通常用來顯示應用程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="d1a25-114">Creates a status window, which is typically used to display the status of an application.</span></span> <span data-ttu-id="d1a25-115">視窗通常會出現在父視窗的底部，並且包含指定的文字。</span><span class="sxs-lookup"><span data-stu-id="d1a25-115">The window generally appears at the bottom of the parent window, and it contains the specified text.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="d1a25-116">此函式已過時。</span><span class="sxs-lookup"><span data-stu-id="d1a25-116">This function is obsolete.</span></span> <span data-ttu-id="d1a25-117">請改用 <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>CreateWindow</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="d1a25-117">Use <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>CreateWindow</strong></a> instead.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1a25-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1a25-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a></span></span></td>
<td><span data-ttu-id="d1a25-119"><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a>函式會以具有框線的狀態視窗樣式來繪製指定文字。</span><span class="sxs-lookup"><span data-stu-id="d1a25-119">The <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a> function draws the specified text in the style of a status window with borders.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d1a25-120"><a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>MenuHelp</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1a25-120"><a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>MenuHelp</strong></a></span></span></td>
<td><span data-ttu-id="d1a25-121">處理 <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> 和 <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> 訊息，並在指定的狀態視窗中顯示目前功能表的解說文字。</span><span class="sxs-lookup"><span data-stu-id="d1a25-121">Processes <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> and <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> messages and displays Help text about the current menu in the specified status window.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a><span data-ttu-id="d1a25-122">訊息</span><span class="sxs-lookup"><span data-stu-id="d1a25-122">Messages</span></span>



| <span data-ttu-id="d1a25-123">主題</span><span class="sxs-lookup"><span data-stu-id="d1a25-123">Topic</span></span>                                               | <span data-ttu-id="d1a25-124">目錄</span><span class="sxs-lookup"><span data-stu-id="d1a25-124">Contents</span></span>                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1a25-125">**SB \_ GETBORDERS**</span><span class="sxs-lookup"><span data-stu-id="d1a25-125">**SB\_GETBORDERS**</span></span>](sb-getborders.md)             | <span data-ttu-id="d1a25-126">抓取狀態視窗水準和垂直框線的目前寬度。</span><span class="sxs-lookup"><span data-stu-id="d1a25-126">Retrieves the current widths of the horizontal and vertical borders of a status window.</span></span> <br/>                                                                                                  |
| [<span data-ttu-id="d1a25-127">**SB \_ GETICON**</span><span class="sxs-lookup"><span data-stu-id="d1a25-127">**SB\_GETICON**</span></span>](sb-geticon.md)                   | <span data-ttu-id="d1a25-128">抓取狀態列中元件的圖示。</span><span class="sxs-lookup"><span data-stu-id="d1a25-128">Retrieves the icon for a part in a status bar.</span></span> <br/>                                                                                                                                           |
| [<span data-ttu-id="d1a25-129">**SB \_ GETPARTS**</span><span class="sxs-lookup"><span data-stu-id="d1a25-129">**SB\_GETPARTS**</span></span>](sb-getparts.md)                 | <span data-ttu-id="d1a25-130">捕獲狀態視窗中的部分計數。</span><span class="sxs-lookup"><span data-stu-id="d1a25-130">Retrieves a count of the parts in a status window.</span></span> <span data-ttu-id="d1a25-131">此訊息也會抓取指定之部分數目的右邊緣座標。</span><span class="sxs-lookup"><span data-stu-id="d1a25-131">The message also retrieves the coordinate of the right edge of the specified number of parts.</span></span> <br/>                                         |
| [<span data-ttu-id="d1a25-132">**SB \_ GETRECT**</span><span class="sxs-lookup"><span data-stu-id="d1a25-132">**SB\_GETRECT**</span></span>](sb-getrect.md)                   | <span data-ttu-id="d1a25-133">抓取狀態視窗中某部分的周框。</span><span class="sxs-lookup"><span data-stu-id="d1a25-133">Retrieves the bounding rectangle of a part in a status window.</span></span> <br/>                                                                                                                           |
| [<span data-ttu-id="d1a25-134">**SB \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="d1a25-134">**SB\_GETTEXT**</span></span>](sb-gettext.md)                   | <span data-ttu-id="d1a25-135">[**SB \_ GETTEXT**](sb-gettext.md)訊息會從狀態視窗的指定部分抓取文字。</span><span class="sxs-lookup"><span data-stu-id="d1a25-135">The [**SB\_GETTEXT**](sb-gettext.md) message retrieves the text from the specified part of a status window.</span></span> <br/>                                                                             |
| [<span data-ttu-id="d1a25-136">**SB \_ GETTEXTLENGTH**</span><span class="sxs-lookup"><span data-stu-id="d1a25-136">**SB\_GETTEXTLENGTH**</span></span>](sb-gettextlength.md)       | <span data-ttu-id="d1a25-137">[**SB \_ GETTEXTLENGTH**](sb-gettextlength.md)訊息會從狀態視窗的指定部分抓取文字的長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d1a25-137">The [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) message retrieves the length, in characters, of the text from the specified part of a status window.</span></span> <br/>                                   |
| [<span data-ttu-id="d1a25-138">**SB \_ GETTIPTEXT**</span><span class="sxs-lookup"><span data-stu-id="d1a25-138">**SB\_GETTIPTEXT**</span></span>](sb-gettiptext.md)             | <span data-ttu-id="d1a25-139">抓取狀態列中某部分的工具提示文字。</span><span class="sxs-lookup"><span data-stu-id="d1a25-139">Retrieves the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="d1a25-140">您必須使用 [**SBT \_ 工具提示**](status-bar-styles.md) 樣式來建立狀態列，才能啟用工具提示。</span><span class="sxs-lookup"><span data-stu-id="d1a25-140">The status bar must be created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span> <br/>         |
| [<span data-ttu-id="d1a25-141">**SB \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="d1a25-141">**SB\_GETUNICODEFORMAT**</span></span>](sb-getunicodeformat.md) | <span data-ttu-id="d1a25-142">抓取控制項的 Unicode 字元格式旗標。</span><span class="sxs-lookup"><span data-stu-id="d1a25-142">Retrieves the Unicode character format flag for the control.</span></span> <br/>                                                                                                                             |
| [<span data-ttu-id="d1a25-143">**SB \_ ISSIMPLE**</span><span class="sxs-lookup"><span data-stu-id="d1a25-143">**SB\_ISSIMPLE**</span></span>](sb-issimple.md)                 | <span data-ttu-id="d1a25-144">檢查狀態列控制項是否為簡單模式。</span><span class="sxs-lookup"><span data-stu-id="d1a25-144">Checks a status bar control to determine if it is in simple mode.</span></span> <br/>                                                                                                                        |
| [<span data-ttu-id="d1a25-145">**SB \_ SETBKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="d1a25-145">**SB\_SETBKCOLOR**</span></span>](sb-setbkcolor.md)             | <span data-ttu-id="d1a25-146">設定狀態列中的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="d1a25-146">Sets the background color in a status bar.</span></span> <br/>                                                                                                                                               |
| [<span data-ttu-id="d1a25-147">**SB \_ SETICON**</span><span class="sxs-lookup"><span data-stu-id="d1a25-147">**SB\_SETICON**</span></span>](sb-seticon.md)                   | <span data-ttu-id="d1a25-148">設定狀態列中元件的圖示。</span><span class="sxs-lookup"><span data-stu-id="d1a25-148">Sets the icon for a part in a status bar.</span></span> <br/>                                                                                                                                                |
| [<span data-ttu-id="d1a25-149">**SB \_ SETMINHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="d1a25-149">**SB\_SETMINHEIGHT**</span></span>](sb-setminheight.md)         | <span data-ttu-id="d1a25-150">設定狀態視窗之繪圖區域的最小高度。</span><span class="sxs-lookup"><span data-stu-id="d1a25-150">Sets the minimum height of a status window's drawing area.</span></span> <br/>                                                                                                                               |
| [<span data-ttu-id="d1a25-151">**SB \_ SETPARTS**</span><span class="sxs-lookup"><span data-stu-id="d1a25-151">**SB\_SETPARTS**</span></span>](sb-setparts.md)                 | <span data-ttu-id="d1a25-152">設定狀態視窗中的部分數目，以及每個元件右邊緣的座標。</span><span class="sxs-lookup"><span data-stu-id="d1a25-152">Sets the number of parts in a status window and the coordinate of the right edge of each part.</span></span> <br/>                                                                                           |
| [<span data-ttu-id="d1a25-153">**SB \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="d1a25-153">**SB\_SETTEXT**</span></span>](sb-settext.md)                   | <span data-ttu-id="d1a25-154">SB \_ SETTEXT 訊息會在狀態視窗的指定部分設定文字。</span><span class="sxs-lookup"><span data-stu-id="d1a25-154">The SB\_SETTEXT message sets the text in the specified part of a status window.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="d1a25-155">**SB \_ SETTIPTEXT**</span><span class="sxs-lookup"><span data-stu-id="d1a25-155">**SB\_SETTIPTEXT**</span></span>](sb-settiptext.md)             | <span data-ttu-id="d1a25-156">設定狀態列中某部分的工具提示文字。</span><span class="sxs-lookup"><span data-stu-id="d1a25-156">Sets the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="d1a25-157">您必須使用 [**SBT \_ 工具提示**](status-bar-styles.md) 樣式來建立狀態列，才能啟用工具提示。</span><span class="sxs-lookup"><span data-stu-id="d1a25-157">The status bar must have been created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span><br/>        |
| [<span data-ttu-id="d1a25-158">**SB \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="d1a25-158">**SB\_SETUNICODEFORMAT**</span></span>](sb-setunicodeformat.md) | <span data-ttu-id="d1a25-159">設定控制項的 Unicode 字元格式旗標。</span><span class="sxs-lookup"><span data-stu-id="d1a25-159">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="d1a25-160">此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。</span><span class="sxs-lookup"><span data-stu-id="d1a25-160">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <br/> |
| [<span data-ttu-id="d1a25-161">**SB \_ 簡單**</span><span class="sxs-lookup"><span data-stu-id="d1a25-161">**SB\_SIMPLE**</span></span>](sb-simple.md)                     | <span data-ttu-id="d1a25-162">指定狀態視窗是否顯示簡單文字，或顯示先前 [**SB \_ SETPARTS**](sb-setparts.md) 訊息所設定的所有視窗元件。</span><span class="sxs-lookup"><span data-stu-id="d1a25-162">Specifies whether a status window displays simple text or displays all window parts set by a previous [**SB\_SETPARTS**](sb-setparts.md) message.</span></span> <br/>                                       |



 

### <a name="notifications"></a><span data-ttu-id="d1a25-163">通知</span><span class="sxs-lookup"><span data-stu-id="d1a25-163">Notifications</span></span>



| <span data-ttu-id="d1a25-164">主題</span><span class="sxs-lookup"><span data-stu-id="d1a25-164">Topic</span></span>                                                 | <span data-ttu-id="d1a25-165">目錄</span><span class="sxs-lookup"><span data-stu-id="d1a25-165">Contents</span></span>                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1a25-166">NM \_ 按一下 (狀態列) </span><span class="sxs-lookup"><span data-stu-id="d1a25-166">NM\_CLICK (status bar)</span></span>](nm-click-status-bar.md)     | <span data-ttu-id="d1a25-167">通知狀態列控制項的父視窗，使用者在控制項內按一下滑鼠左鍵。</span><span class="sxs-lookup"><span data-stu-id="d1a25-167">Notifies the parent window of a status bar control that the user has clicked the left mouse button within the control.</span></span> <span data-ttu-id="d1a25-168">[NM \_按一下 [ (狀態列](nm-click-status-bar.md) ]，) 以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="d1a25-168">[NM\_CLICK (status bar)](nm-click-status-bar.md) is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/>              |
| [<span data-ttu-id="d1a25-169">NM \_ DBLCLK (狀態列) </span><span class="sxs-lookup"><span data-stu-id="d1a25-169">NM\_DBLCLK (status bar)</span></span>](nm-dblclk-status-bar.md)   | <span data-ttu-id="d1a25-170">通知狀態列控制項的父視窗，使用者在控制項內按兩下滑鼠左鍵。</span><span class="sxs-lookup"><span data-stu-id="d1a25-170">Notifies the parent window of a status bar control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="d1a25-171">此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="d1a25-171">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/>                                       |
| [<span data-ttu-id="d1a25-172">NM \_ RCLICK (狀態列) </span><span class="sxs-lookup"><span data-stu-id="d1a25-172">NM\_RCLICK (status bar)</span></span>](nm-rclick-status-bar.md)   | <span data-ttu-id="d1a25-173">通知狀態列控制項的父視窗，使用者在控制項內按一下滑鼠右鍵。</span><span class="sxs-lookup"><span data-stu-id="d1a25-173">Notifies the parent window of a status bar control that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="d1a25-174">此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="d1a25-174">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/>                                             |
| [<span data-ttu-id="d1a25-175">NM \_ RDBLCLK (狀態列) </span><span class="sxs-lookup"><span data-stu-id="d1a25-175">NM\_RDBLCLK (status bar)</span></span>](nm-rdblclk-status-bar.md) | <span data-ttu-id="d1a25-176">通知狀態列控制項的父視窗，使用者在控制項內按兩下滑鼠右鍵。</span><span class="sxs-lookup"><span data-stu-id="d1a25-176">Notifies the parent windows of a status bar control that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="d1a25-177">[NM \_RDBLCLK (狀態列)](nm-rdblclk-status-bar.md) 會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="d1a25-177">[NM\_RDBLCLK (status bar)](nm-rdblclk-status-bar.md) is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/> |
| [<span data-ttu-id="d1a25-178">SBN \_ SIMPLEMODECHANGE</span><span class="sxs-lookup"><span data-stu-id="d1a25-178">SBN\_SIMPLEMODECHANGE</span></span>](sbn-simplemodechange.md)     | <span data-ttu-id="d1a25-179">當簡單模式因為 [**SB \_ 簡單**](sb-simple.md) 訊息而變更時，由狀態列控制項傳送。</span><span class="sxs-lookup"><span data-stu-id="d1a25-179">Sent by a status bar control when the simple mode changes due to a [**SB\_SIMPLE**](sb-simple.md) message.</span></span> <span data-ttu-id="d1a25-180">此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="d1a25-180">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/>                                                        |



 

### <a name="constants"></a><span data-ttu-id="d1a25-181">常數</span><span class="sxs-lookup"><span data-stu-id="d1a25-181">Constants</span></span>



| <span data-ttu-id="d1a25-182">主題</span><span class="sxs-lookup"><span data-stu-id="d1a25-182">Topic</span></span>                                      | <span data-ttu-id="d1a25-183">目錄</span><span class="sxs-lookup"><span data-stu-id="d1a25-183">Contents</span></span>                                                                                                              |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1a25-184">狀態列樣式</span><span class="sxs-lookup"><span data-stu-id="d1a25-184">Status Bar Styles</span></span>](status-bar-styles.md) | <span data-ttu-id="d1a25-185">除了由 *狀態列* 控制項支援的標準視窗樣式之外，本節還會列出樣式。</span><span class="sxs-lookup"><span data-stu-id="d1a25-185">This section lists the styles, in addition to standard window styles, supported by *status bar* controls.</span></span> <br/> |



 

 

