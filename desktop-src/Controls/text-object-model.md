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
# <a name="text-object-model"></a>Text 物件模型

本章節包含與 Text 物件模型搭配使用之程式設計項目的相關資訊 (TOM) 。

TOM 會定義一組大量的文字操作介面。 文字解決方案（例如 Microsoft Word 和 rich edit 控制項）支援 TOM 功能集。 TOM 受到 WordBasic 的影響， (Word) 所使用的程式設計語言，而且很容易就能從 Microsoft Visual Basic for Applications (VBA) 使用。 此相容性有幾個優點：

-   程式碼可以相當輕鬆地從一個解決方案遷移到另一個方案。
-   您可以使用一種語言，在不同的文字引擎之間共用文字資訊。
-   相較于不同的低層級元件物件模型， (COM) 和 VBA 介面，可減少檔和程式碼的需求。

不過，C/c + + 的使用方式可能會比使用較一般較低層級的 COM 介面更有效率。

TOM 是一組簡單的介面，可針對其主要文字解決方案、Word 和 rich edit 控制項來實行。 不過，對於對文字進行輕微強調的應用程式來說，最好是將文字傳送至支援 TOM 的編輯控制項，以提供 TOM 介面。 由於豐富的編輯控制項隨附于 Microsoft 作業系統，因此是取得 TOM 功能的標準方式。

### <a name="overviews"></a>概觀



| 主題                                                          | 目錄                                                                                                                                                                                                         |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於 Text 物件模型](about-text-object-model.md)         | 最上層的文字物件模型 (TOM) 物件是由 [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) 介面所定義，這個介面具有在物件階層中較低層級建立和取得物件的方法。<br/> |
| [使用 Text 物件模型](using-the-text-object-model.md) | 本檔中的程式碼範例會示範使用 Text 物件模型 (TOM) 的各種層面。<br/>                                                                                                          |



 

### <a name="interfaces"></a>介面



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>目錄</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a></td>
<td><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a>介面是 TOM 最上層介面，可針對檔中的任何故事，抓取作用中的選取範圍和範圍物件（不論是否為使用中）。 它可讓應用程式：
<ul>
<li>開啟和儲存檔。</li>
<li>控制復原行為和螢幕更新。</li>
<li>尋找螢幕位置的範圍。</li>
<li>取得 <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> 案例枚舉器。</li>
</ul>
<br/> <strong>執行時機</strong><br/> 應用程式通常不會執行 <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> 介面。 Microsoft 文字解決方案，例如 rich edit 控制項，會在其 TOM 實行過程中執行 <strong>ITextDocument</strong> 。 <br/> <strong>使用時機</strong><br/> 應用程式可以從 rich edit 控制項取出 <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> 指標。 若要這樣做，請傳送 <a href="em-getoleinterface.md"><strong>EM_GETOLEINTERFACE</strong></a> 訊息，從 rich edit 控制項取出 <a href="/windows/desktop/api/Richole/nn-richole-iricheditole"><strong>IRichEditOle</strong></a> 物件。 然後，呼叫物件的 <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>IUnknown：： QueryInterface</strong></a> 方法來取出 <strong>ITextDocument</strong> 指標。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a></td>
<td>TOM rich text 範圍屬性可透過一組雙重介面（ <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> 和 <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>）來存取。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a></td>
<td>TOM rich text 範圍屬性可透過一組雙重介面（ <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> 和 <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>）來存取。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a></td>
<td><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a>物件是功能強大的編輯和資料系結工具，可讓程式選取案例中的文字，然後檢查或變更該文字。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextselection"><strong>ITextSelection</strong></a></td>
<td>文字選取範圍是具有反白顯示專案的文字範圍。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a></td>
<td><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a>介面的目的是要列舉<a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a>中的故事。<br/></td>
</tr>
</tbody>
</table>



 

 

