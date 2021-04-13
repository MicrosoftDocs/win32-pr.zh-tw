---
title: 使用 Rich Edit 控制項
description: 本章節包含的主題會示範如何建立和使用 rich edit 控制項。
ms.assetid: 2c4717c9-3257-42d5-9c36-89b7e524e788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0489660bb6849d0de76ae7fc2f4e21ca931662a8
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104463845"
---
# <a name="using-rich-edit-controls"></a><span data-ttu-id="e1ba2-103">使用 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="e1ba2-103">Using Rich Edit Controls</span></span>

<span data-ttu-id="e1ba2-104">本章節包含的主題會示範如何建立和使用 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-104">This section contains topics that demonstrate how to create and use rich edit controls.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e1ba2-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="e1ba2-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e1ba2-106">主題</span><span class="sxs-lookup"><span data-stu-id="e1ba2-106">Topic</span></span></th>
<th><span data-ttu-id="e1ba2-107">描述</span><span class="sxs-lookup"><span data-stu-id="e1ba2-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1ba2-108"><a href="create-rich-edit-controls.md">如何建立 Rich Edit 控制項</a></span><span class="sxs-lookup"><span data-stu-id="e1ba2-108"><a href="create-rich-edit-controls.md">How to Create Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="e1ba2-109">若要建立 rich edit 控制項，請呼叫 <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> 函數，並指定 rich edit 視窗類別。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-109">To create a rich edit control, call the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> function, specifying the rich edit window class.</span></span> <span data-ttu-id="e1ba2-110">若為 Microsoft Rich Edit 4.1 (Msftedit.dll) ，請將 MSFTEDIT_CLASS 指定為 window 類別。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-110">For Microsoft Rich Edit 4.1 (Msftedit.dll), specify MSFTEDIT_CLASS as the window class.</span></span> <span data-ttu-id="e1ba2-111">針對所有先前的版本，指定 RICHEDIT_CLASS。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-111">For all previous versions, specify RICHEDIT_CLASS.</span></span> <span data-ttu-id="e1ba2-112">如需詳細資訊，請參閱 <a href="about-rich-edit-controls.md">Rich Edit 的版本</a>。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-112">For more information, see <a href="about-rich-edit-controls.md">Versions of Rich Edit</a>.</span></span> <br/> <span data-ttu-id="e1ba2-113">Rich edit 控制項支援大部分與編輯控制項搭配使用的視窗樣式，以及額外的樣式。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-113">Rich edit controls support most of the window styles used with edit controls as well as additional styles.</span></span> <span data-ttu-id="e1ba2-114">如果您想要在控制項中允許多行文字，則應該指定 <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> 視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-114">You should specify the <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> window style if you want to allow more than one line of text in the control.</span></span> <span data-ttu-id="e1ba2-115">如需詳細資訊，請參閱 <a href="rich-edit-control-styles.md">Rich Edit 控制項樣式</a>。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-115">For more information, see <a href="rich-edit-control-styles.md">Rich Edit Control Styles</a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1ba2-116"><a href="format-text-in-rich-edit-controls.md">如何格式化 Rich Edit 控制項中的文字</a></span><span class="sxs-lookup"><span data-stu-id="e1ba2-116"><a href="format-text-in-rich-edit-controls.md">How to Format Text in Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="e1ba2-117">應用程式可以將訊息傳送至 rich edit 控制項，以便格式化字元和段落，並取出格式資訊。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-117">An application can send messages to a rich edit control in order to format characters and paragraphs and retrieve formatting information.</span></span> <span data-ttu-id="e1ba2-118">段落格式化屬性包括對齊、索引標籤、縮排、編號和簡單的資料表。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-118">Paragraph formatting attributes include alignment, tabs, indents, numbering, and simple tables.</span></span> <span data-ttu-id="e1ba2-119">若為字元，您可以指定字型名稱、大小、色彩和效果，例如粗體、斜體和 protected。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-119">For characters, you can specify font name, size, color, and effects such as bold, italic, and protected.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1ba2-120"><a href="interact-with-the-current-selection.md">如何與目前的選取範圍互動</a></span><span class="sxs-lookup"><span data-stu-id="e1ba2-120"><a href="interact-with-the-current-selection.md">How to Interact with the Current Selection</a></span></span><br/></td>
<td><span data-ttu-id="e1ba2-121">使用者可以使用滑鼠或鍵盤選取 rich edit 控制項中的文字。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-121">The user can select text in a rich edit control by using the mouse or the keyboard.</span></span> <span data-ttu-id="e1ba2-122"><em>目前的選取</em>範圍是選定字元的範圍，或者，如果未選取任何字元，則為插入點的位置。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-122">The <em>current selection</em> is the range of selected characters, or the position of the insertion point if no characters are selected.</span></span> <span data-ttu-id="e1ba2-123">應用程式可以取得目前選取範圍的相關資訊、設定它、判斷其變更時間，以及顯示或隱藏選取專案反白顯示。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-123">An application can get information about the current selection, set it, determine when it changes, and show or hide the selection highlight.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1ba2-124"><a href="use-rich-edit-text-operations.md">如何使用豐富的編輯文字作業</a></span><span class="sxs-lookup"><span data-stu-id="e1ba2-124"><a href="use-rich-edit-text-operations.md">How to Use Rich Edit Text Operations</a></span></span><br/></td>
<td><span data-ttu-id="e1ba2-125">應用程式可以傳送訊息，以在 rich edit 控制項中取得或尋找文字。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-125">An application can send messages to retrieve or find text in a rich edit control.</span></span> <span data-ttu-id="e1ba2-126">您可以取出選取的文字或指定的文字範圍。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-126">You can retrieve either the selected text or a specified range of text.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1ba2-127"><a href="use-word-and-line-break-information.md">如何使用單字和換行資訊</a></span><span class="sxs-lookup"><span data-stu-id="e1ba2-127"><a href="use-word-and-line-break-information.md">How to Use Word and Line Break Information</a></span></span><br/></td>
<td><span data-ttu-id="e1ba2-128">Rich edit 控制項會呼叫稱為斷詞程式的函式，以找出單字之間的中斷，以及判斷它可以中斷行的位置。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-128">A rich edit control calls a function called a word-break procedure to find breaks between words and to determine where it can break lines.</span></span> <span data-ttu-id="e1ba2-129">控制項在執行自動換行作業時，以及處理 CTRL + 向左鍵和 CTRL + 向右鍵按鍵組合時，會使用這項資訊。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-129">The control uses this information when performing word-wrap operations and when processing CTRL+LEFT ARROW key and CTRL+RIGHT ARROW key combinations.</span></span> <span data-ttu-id="e1ba2-130">應用程式可以傳送訊息至 Rich Edit 控制項來取代預設斷字程序、擷取斷字資訊，以及決定指定的字元落在哪一行的位置。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-130">An application can send messages to a rich edit control to replace the default word-break procedure, to retrieve word-break information, and to determine what line a given character falls on.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1ba2-131"><a href="use-rich-edit-clipboard-operations.md">如何使用 Rich Edit 剪貼簿作業</a></span><span class="sxs-lookup"><span data-stu-id="e1ba2-131"><a href="use-rich-edit-clipboard-operations.md">How to Use Rich Edit Clipboard Operations</a></span></span><br/></td>
<td><span data-ttu-id="e1ba2-132">應用程式可以使用最適合的剪貼簿格式或特定的剪貼簿格式，將剪貼簿的內容貼入 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-132">An application can paste the contents of the clipboard into a rich edit control by using either the best available clipboard format or a specific clipboard format.</span></span> <span data-ttu-id="e1ba2-133">您也可以判斷 rich edit 控制項是否能夠貼上剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-133">You can also determine whether a rich edit control is capable of pasting a clipboard format.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1ba2-134"><a href="use-streams.md">如何使用資料流程</a></span><span class="sxs-lookup"><span data-stu-id="e1ba2-134"><a href="use-streams.md">How to Use Streams</a></span></span><br/></td>
<td><span data-ttu-id="e1ba2-135">您可以使用資料流程將資料傳入或傳出 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-135">You can use streams to transfer data into or out of a rich edit control.</span></span> <span data-ttu-id="e1ba2-136">資料流程是由 <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>EDITSTREAM</strong></a> 結構所定義，它會指定緩衝區和應用程式定義的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-136">A stream is defined by an <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>EDITSTREAM</strong></a> structure, which specifies a buffer and an application-defined callback function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1ba2-137"><a href="automatically-resize-rich-edit-controls.md">如何自動調整 Rich Edit 控制項的大小</a></span><span class="sxs-lookup"><span data-stu-id="e1ba2-137"><a href="automatically-resize-rich-edit-controls.md">How to Automatically Resize Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="e1ba2-138">應用程式可以視需要調整 rich edit 控制項的大小，使其大小一律與內容相同。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-138">An application can resize a rich edit control as needed so that it is always the same size as its contents.</span></span> <span data-ttu-id="e1ba2-139">Rich edit 控制項支援這種所謂的 <em>無底邊</em> 功能，方法是在控制項內容的大小變更時，將 <a href="en-requestresize.md">EN_REQUESTRESIZE</a> 通知程式碼傳送給它的父視窗。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-139">A rich edit control supports this so-called <em>bottomless</em> functionality by sending its parent window an <a href="en-requestresize.md">EN_REQUESTRESIZE</a> notification code whenever the size of the control's content changes.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1ba2-140"><a href="use-rich-edit-control-notification-codes.md">如何使用 Rich Edit 控制項通知碼</a></span><span class="sxs-lookup"><span data-stu-id="e1ba2-140"><a href="use-rich-edit-control-notification-codes.md">How to Use Rich Edit Control Notification Codes</a></span></span><br/></td>
<td><span data-ttu-id="e1ba2-141">Rich edit 控制項的父視窗可以處理通知碼來監視影響控制項的事件。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-141">A rich edit control's parent window can process notification codes to monitor events that affect the control.</span></span> <span data-ttu-id="e1ba2-142">Rich edit 控制項支援與編輯控制項搭配使用的所有通知碼，以及數個其他專案。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-142">Rich edit controls support all of the notification codes that are used with edit controls, as well as several additional ones.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1ba2-143"><a href="use-font-binding-in-rich-edit-controls.md">如何在 Rich Edit 控制項中使用字型系結</a></span><span class="sxs-lookup"><span data-stu-id="e1ba2-143"><a href="use-font-binding-in-rich-edit-controls.md">How to Use Font Binding in Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="e1ba2-144">Microsoft Rich Edit 3.0 會根據其內容將字元集指派為純文字字元。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-144">Microsoft Rich Edit 3.0 assigns a character set to plain-text characters depending on their context.</span></span> <span data-ttu-id="e1ba2-145">部分範例如下：</span><span class="sxs-lookup"><span data-stu-id="e1ba2-145">Some examples are:</span></span> <br/>
<ul>
<li><span data-ttu-id="e1ba2-146">希臘文字元會指派 <strong>GREEK_CHARSET</strong>。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-146">Greek characters are assigned <strong>GREEK_CHARSET</strong>.</span></span></li>
<li><span data-ttu-id="e1ba2-147">韓文符號會指派 <strong>HANGUL_CHARSET</strong>。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-147">Hangul symbols are assigned <strong>HANGUL_CHARSET</strong>.</span></span></li>
<li><span data-ttu-id="e1ba2-148">如果找到附近的假名字元，則會將中文字元指派 <strong>SHIFTJIS_CHARSET</strong> ; 如果附近找不到假名，則為 <strong>GB2312_CHARSET</strong> 。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-148">Chinese characters are assigned <strong>SHIFTJIS_CHARSET</strong> if kana characters are found nearby, or <strong>GB2312_CHARSET</strong> if no kana are found nearby.</span></span></li>
<li><span data-ttu-id="e1ba2-149">在任何事件中， <strong>ANSI_CHARSET</strong> 指派非中性的 ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-149">Non-neutral ANSI characters are assigned <strong>ANSI_CHARSET</strong> in any event.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1ba2-150"><a href="using-rich-edit-com.md">如何在 Rich Edit 控制項中使用 OLE</a></span><span class="sxs-lookup"><span data-stu-id="e1ba2-150"><a href="using-rich-edit-com.md">How to Use OLE in Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="e1ba2-151">本章節包含在 rich edit 控制項中使用物件連結和內嵌 (OLE) 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-151">This section contains information about using object linking and embedding (OLE) in rich edit controls.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1ba2-152"><a href="printing-rich-edit-controls.md">如何列印 Rich Edit 控制項的內容</a></span><span class="sxs-lookup"><span data-stu-id="e1ba2-152"><a href="printing-rich-edit-controls.md">How to Print the Contents of Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="e1ba2-153">本章節包含如何列印 rich edit 控制項內容的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-153">This section contains information about how to print the contents of rich edit controls.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

 

