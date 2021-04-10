---
title: Text 物件模型
description: 本章節包含與 Text 物件模型搭配使用之程式設計項目的相關資訊 (TOM) 。
ms.assetid: vs|controls|~\controls\richedit\textobjectmodel.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7625ca7772da7f4e10aa7d64159971ee0e259d2a
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "103842832"
---
# <a name="text-object-model"></a><span data-ttu-id="aed94-103">Text 物件模型</span><span class="sxs-lookup"><span data-stu-id="aed94-103">Text Object Model</span></span>

<span data-ttu-id="aed94-104">本章節包含與 Text 物件模型搭配使用之程式設計項目的相關資訊 (TOM) 。</span><span class="sxs-lookup"><span data-stu-id="aed94-104">This section contains information about the programming elements used with the Text Object Model (TOM).</span></span>

<span data-ttu-id="aed94-105">TOM 會定義一組大量的文字操作介面。</span><span class="sxs-lookup"><span data-stu-id="aed94-105">The TOM defines a substantial set of text manipulation interfaces.</span></span> <span data-ttu-id="aed94-106">文字解決方案（例如 Microsoft Word 和 rich edit 控制項）支援 TOM 功能集。</span><span class="sxs-lookup"><span data-stu-id="aed94-106">Text solutions such as Microsoft Word and rich edit controls support the TOM feature set.</span></span> <span data-ttu-id="aed94-107">TOM 受到 WordBasic 的影響， (Word) 所使用的程式設計語言，而且很容易就能從 Microsoft Visual Basic for Applications (VBA) 使用。</span><span class="sxs-lookup"><span data-stu-id="aed94-107">TOM was greatly influenced by WordBasic (the programming language used for Word) and it is easy to use from Microsoft Visual Basic for Applications (VBA).</span></span> <span data-ttu-id="aed94-108">此相容性有幾個優點：</span><span class="sxs-lookup"><span data-stu-id="aed94-108">This compatibility has several advantages:</span></span>

-   <span data-ttu-id="aed94-109">程式碼可以相當輕鬆地從一個解決方案遷移到另一個方案。</span><span class="sxs-lookup"><span data-stu-id="aed94-109">Code can migrate fairly easily from one solution to another.</span></span>
-   <span data-ttu-id="aed94-110">您可以使用一種語言，在不同的文字引擎之間共用文字資訊。</span><span class="sxs-lookup"><span data-stu-id="aed94-110">One language can be used to share text information between different text engines.</span></span>
-   <span data-ttu-id="aed94-111">相較于不同的低層級元件物件模型， (COM) 和 VBA 介面，可減少檔和程式碼的需求。</span><span class="sxs-lookup"><span data-stu-id="aed94-111">It reduces the need for documentation and code compared to the separate low-level Component Object Model (COM) and VBA interfaces.</span></span>

<span data-ttu-id="aed94-112">不過，C/c + + 的使用方式可能會比使用較一般較低層級的 COM 介面更有效率。</span><span class="sxs-lookup"><span data-stu-id="aed94-112">However, it can be less efficient for C/C++ purposes than the use of more general lower level COM interfaces.</span></span>

<span data-ttu-id="aed94-113">TOM 是一組簡單的介面，可針對其主要文字解決方案、Word 和 rich edit 控制項來實行。</span><span class="sxs-lookup"><span data-stu-id="aed94-113">TOM is a straightforward set of interfaces to implement for its primary text solutions, Word and rich edit controls.</span></span> <span data-ttu-id="aed94-114">不過，對於對文字進行輕微強調的應用程式來說，最好是將文字傳送至支援 TOM 的編輯控制項，以提供 TOM 介面。</span><span class="sxs-lookup"><span data-stu-id="aed94-114">However, for applications that place minor emphasis on text, it is better to provide TOM interfaces by transferring the text to an edit control that supports TOM.</span></span> <span data-ttu-id="aed94-115">由於豐富的編輯控制項隨附于 Microsoft 作業系統，因此是取得 TOM 功能的標準方式。</span><span class="sxs-lookup"><span data-stu-id="aed94-115">Since rich edit controls ship with Microsoft operating systems, they are the standard means of obtaining TOM functionality.</span></span>

### <a name="overviews"></a><span data-ttu-id="aed94-116">概觀</span><span class="sxs-lookup"><span data-stu-id="aed94-116">Overviews</span></span>



| <span data-ttu-id="aed94-117">主題</span><span class="sxs-lookup"><span data-stu-id="aed94-117">Topic</span></span>                                                          | <span data-ttu-id="aed94-118">目錄</span><span class="sxs-lookup"><span data-stu-id="aed94-118">Contents</span></span>                                                                                                                                                                                                         |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aed94-119">關於 Text 物件模型</span><span class="sxs-lookup"><span data-stu-id="aed94-119">About Text Object Model</span></span>](about-text-object-model.md)         | <span data-ttu-id="aed94-120">最上層的文字物件模型 (TOM) 物件是由 [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) 介面所定義，這個介面具有在物件階層中較低層級建立和取得物件的方法。</span><span class="sxs-lookup"><span data-stu-id="aed94-120">The top-level Text Object Model (TOM) object is defined by the [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) interface, which has methods for creating and retrieving objects lower in the object hierarchy.</span></span><br/> |
| [<span data-ttu-id="aed94-121">使用 Text 物件模型</span><span class="sxs-lookup"><span data-stu-id="aed94-121">Using The Text Object Model</span></span>](using-the-text-object-model.md) | <span data-ttu-id="aed94-122">本檔中的程式碼範例會示範使用 Text 物件模型 (TOM) 的各種層面。</span><span class="sxs-lookup"><span data-stu-id="aed94-122">The code samples in this document show various aspects of using the Text Object Model (TOM).</span></span><br/>                                                                                                          |



 

### <a name="interfaces"></a><span data-ttu-id="aed94-123">介面</span><span class="sxs-lookup"><span data-stu-id="aed94-123">Interfaces</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aed94-124">主題</span><span class="sxs-lookup"><span data-stu-id="aed94-124">Topic</span></span></th>
<th><span data-ttu-id="aed94-125">目錄</span><span class="sxs-lookup"><span data-stu-id="aed94-125">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aed94-126"><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="aed94-126"><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a></span></span></td>
<td><span data-ttu-id="aed94-127"><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a>介面是 TOM 最上層介面，可針對檔中的任何故事，抓取作用中的選取範圍和範圍物件（不論是否為使用中）。</span><span class="sxs-lookup"><span data-stu-id="aed94-127">The <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> interface is the TOM top-level interface, which retrieves the active selection and range objects for any story in the document whether active or not.</span></span> <span data-ttu-id="aed94-128">它可讓應用程式：</span><span class="sxs-lookup"><span data-stu-id="aed94-128">It enables the application to:</span></span>
<ul>
<li><span data-ttu-id="aed94-129">開啟和儲存檔。</span><span class="sxs-lookup"><span data-stu-id="aed94-129">Open and save documents.</span></span></li>
<li><span data-ttu-id="aed94-130">控制復原行為和螢幕更新。</span><span class="sxs-lookup"><span data-stu-id="aed94-130">Control undo behavior and screen updating.</span></span></li>
<li><span data-ttu-id="aed94-131">尋找螢幕位置的範圍。</span><span class="sxs-lookup"><span data-stu-id="aed94-131">Find a range from a screen position.</span></span></li>
<li><span data-ttu-id="aed94-132">取得 <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> 案例枚舉器。</span><span class="sxs-lookup"><span data-stu-id="aed94-132">Get an <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> story enumerator.</span></span></li>
</ul>
<br/> <span data-ttu-id="aed94-133"><strong>執行時機</strong></span><span class="sxs-lookup"><span data-stu-id="aed94-133"><strong>When to Implement</strong></span></span><br/> <span data-ttu-id="aed94-134">應用程式通常不會執行 <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> 介面。</span><span class="sxs-lookup"><span data-stu-id="aed94-134">Applications typically do not implement the <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> interface.</span></span> <span data-ttu-id="aed94-135">Microsoft 文字解決方案，例如 rich edit 控制項，會在其 TOM 實行過程中執行 <strong>ITextDocument</strong> 。</span><span class="sxs-lookup"><span data-stu-id="aed94-135">Microsoft text solutions, such as rich edit controls, implement <strong>ITextDocument</strong> as part of their TOM implementation.</span></span> <br/> <span data-ttu-id="aed94-136"><strong>使用時機</strong></span><span class="sxs-lookup"><span data-stu-id="aed94-136"><strong>When to Use</strong></span></span><br/> <span data-ttu-id="aed94-137">應用程式可以從 rich edit 控制項取出 <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> 指標。</span><span class="sxs-lookup"><span data-stu-id="aed94-137">Applications can retrieve an <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> pointer from a rich edit control.</span></span> <span data-ttu-id="aed94-138">若要這樣做，請傳送 <a href="em-getoleinterface.md"><strong>EM_GETOLEINTERFACE</strong></a> 訊息，從 rich edit 控制項取出 <a href="/windows/desktop/api/Richole/nn-richole-iricheditole"><strong>IRichEditOle</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="aed94-138">To do this, send an <a href="em-getoleinterface.md"><strong>EM_GETOLEINTERFACE</strong></a> message to retrieve an <a href="/windows/desktop/api/Richole/nn-richole-iricheditole"><strong>IRichEditOle</strong></a> object from a rich edit control.</span></span> <span data-ttu-id="aed94-139">然後，呼叫物件的 <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>IUnknown：： QueryInterface</strong></a> 方法來取出 <strong>ITextDocument</strong> 指標。</span><span class="sxs-lookup"><span data-stu-id="aed94-139">Then, call the object's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>IUnknown::QueryInterface</strong></a> method to retrieve an <strong>ITextDocument</strong> pointer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aed94-140"><a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a></span><span class="sxs-lookup"><span data-stu-id="aed94-140"><a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a></span></span></td>
<td><span data-ttu-id="aed94-141">TOM rich text 範圍屬性可透過一組雙重介面（ <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> 和 <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>）來存取。</span><span class="sxs-lookup"><span data-stu-id="aed94-141">TOM rich text-range attributes are accessed through a pair of dual interfaces, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> and <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aed94-142"><a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a></span><span class="sxs-lookup"><span data-stu-id="aed94-142"><a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a></span></span></td>
<td><span data-ttu-id="aed94-143">TOM rich text 範圍屬性可透過一組雙重介面（ <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> 和 <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>）來存取。</span><span class="sxs-lookup"><span data-stu-id="aed94-143">TOM rich text-range attributes are accessed through a pair of dual interfaces, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> and <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aed94-144"><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="aed94-144"><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a></span></span></td>
<td><span data-ttu-id="aed94-145"><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a>物件是功能強大的編輯和資料系結工具，可讓程式選取案例中的文字，然後檢查或變更該文字。</span><span class="sxs-lookup"><span data-stu-id="aed94-145">The <a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a> objects are powerful editing and data-binding tools that allow a program to select text in a story and then examine or change that text.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aed94-146"><a href="/windows/desktop/api/Tom/nn-tom-itextselection"><strong>ITextSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="aed94-146"><a href="/windows/desktop/api/Tom/nn-tom-itextselection"><strong>ITextSelection</strong></a></span></span></td>
<td><span data-ttu-id="aed94-147">文字選取範圍是具有反白顯示專案的文字範圍。</span><span class="sxs-lookup"><span data-stu-id="aed94-147">A text selection is a text range with selection highlighting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aed94-148"><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a></span><span class="sxs-lookup"><span data-stu-id="aed94-148"><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a></span></span></td>
<td><span data-ttu-id="aed94-149"><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a>介面的目的是要列舉<a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a>中的故事。</span><span class="sxs-lookup"><span data-stu-id="aed94-149">The purpose of the <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> interface is to enumerate the stories in an <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

