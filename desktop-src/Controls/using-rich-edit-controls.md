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
# <a name="using-rich-edit-controls"></a>使用 Rich Edit 控制項

本章節包含的主題會示範如何建立和使用 rich edit 控制項。

## <a name="in-this-section"></a>本節內容



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="create-rich-edit-controls.md">如何建立 Rich Edit 控制項</a><br/></td>
<td>若要建立 rich edit 控制項，請呼叫 <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> 函數，並指定 rich edit 視窗類別。 若為 Microsoft Rich Edit 4.1 (Msftedit.dll) ，請將 MSFTEDIT_CLASS 指定為 window 類別。 針對所有先前的版本，指定 RICHEDIT_CLASS。 如需詳細資訊，請參閱 <a href="about-rich-edit-controls.md">Rich Edit 的版本</a>。 <br/> Rich edit 控制項支援大部分與編輯控制項搭配使用的視窗樣式，以及額外的樣式。 如果您想要在控制項中允許多行文字，則應該指定 <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> 視窗樣式。 如需詳細資訊，請參閱 <a href="rich-edit-control-styles.md">Rich Edit 控制項樣式</a>。 <br/></td>
</tr>
<tr class="even">
<td><a href="format-text-in-rich-edit-controls.md">如何格式化 Rich Edit 控制項中的文字</a><br/></td>
<td>應用程式可以將訊息傳送至 rich edit 控制項，以便格式化字元和段落，並取出格式資訊。 段落格式化屬性包括對齊、索引標籤、縮排、編號和簡單的資料表。 若為字元，您可以指定字型名稱、大小、色彩和效果，例如粗體、斜體和 protected。 <br/></td>
</tr>
<tr class="odd">
<td><a href="interact-with-the-current-selection.md">如何與目前的選取範圍互動</a><br/></td>
<td>使用者可以使用滑鼠或鍵盤選取 rich edit 控制項中的文字。 <em>目前的選取</em>範圍是選定字元的範圍，或者，如果未選取任何字元，則為插入點的位置。 應用程式可以取得目前選取範圍的相關資訊、設定它、判斷其變更時間，以及顯示或隱藏選取專案反白顯示。 <br/></td>
</tr>
<tr class="even">
<td><a href="use-rich-edit-text-operations.md">如何使用豐富的編輯文字作業</a><br/></td>
<td>應用程式可以傳送訊息，以在 rich edit 控制項中取得或尋找文字。 您可以取出選取的文字或指定的文字範圍。 <br/></td>
</tr>
<tr class="odd">
<td><a href="use-word-and-line-break-information.md">如何使用單字和換行資訊</a><br/></td>
<td>Rich edit 控制項會呼叫稱為斷詞程式的函式，以找出單字之間的中斷，以及判斷它可以中斷行的位置。 控制項在執行自動換行作業時，以及處理 CTRL + 向左鍵和 CTRL + 向右鍵按鍵組合時，會使用這項資訊。 應用程式可以傳送訊息至 Rich Edit 控制項來取代預設斷字程序、擷取斷字資訊，以及決定指定的字元落在哪一行的位置。 <br/></td>
</tr>
<tr class="even">
<td><a href="use-rich-edit-clipboard-operations.md">如何使用 Rich Edit 剪貼簿作業</a><br/></td>
<td>應用程式可以使用最適合的剪貼簿格式或特定的剪貼簿格式，將剪貼簿的內容貼入 rich edit 控制項。 您也可以判斷 rich edit 控制項是否能夠貼上剪貼簿格式。 <br/></td>
</tr>
<tr class="odd">
<td><a href="use-streams.md">如何使用資料流程</a><br/></td>
<td>您可以使用資料流程將資料傳入或傳出 rich edit 控制項。 資料流程是由 <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>EDITSTREAM</strong></a> 結構所定義，它會指定緩衝區和應用程式定義的回呼函數。 <br/></td>
</tr>
<tr class="even">
<td><a href="automatically-resize-rich-edit-controls.md">如何自動調整 Rich Edit 控制項的大小</a><br/></td>
<td>應用程式可以視需要調整 rich edit 控制項的大小，使其大小一律與內容相同。 Rich edit 控制項支援這種所謂的 <em>無底邊</em> 功能，方法是在控制項內容的大小變更時，將 <a href="en-requestresize.md">EN_REQUESTRESIZE</a> 通知程式碼傳送給它的父視窗。 <br/></td>
</tr>
<tr class="odd">
<td><a href="use-rich-edit-control-notification-codes.md">如何使用 Rich Edit 控制項通知碼</a><br/></td>
<td>Rich edit 控制項的父視窗可以處理通知碼來監視影響控制項的事件。 Rich edit 控制項支援與編輯控制項搭配使用的所有通知碼，以及數個其他專案。 <br/></td>
</tr>
<tr class="even">
<td><a href="use-font-binding-in-rich-edit-controls.md">如何在 Rich Edit 控制項中使用字型系結</a><br/></td>
<td>Microsoft Rich Edit 3.0 會根據其內容將字元集指派為純文字字元。 部分範例如下： <br/>
<ul>
<li>希臘文字元會指派 <strong>GREEK_CHARSET</strong>。</li>
<li>韓文符號會指派 <strong>HANGUL_CHARSET</strong>。</li>
<li>如果找到附近的假名字元，則會將中文字元指派 <strong>SHIFTJIS_CHARSET</strong> ; 如果附近找不到假名，則為 <strong>GB2312_CHARSET</strong> 。</li>
<li>在任何事件中， <strong>ANSI_CHARSET</strong> 指派非中性的 ANSI 字元。</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="using-rich-edit-com.md">如何在 Rich Edit 控制項中使用 OLE</a><br/></td>
<td>本章節包含在 rich edit 控制項中使用物件連結和內嵌 (OLE) 的相關資訊。 <br/></td>
</tr>
<tr class="even">
<td><a href="printing-rich-edit-controls.md">如何列印 Rich Edit 控制項的內容</a><br/></td>
<td>本章節包含如何列印 rich edit 控制項內容的相關資訊。 <br/></td>
</tr>
</tbody>
</table>



 

 

