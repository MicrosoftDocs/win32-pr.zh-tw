---
title: 'Windows (設計基本概念) '
description: Windows 是主要 \ 0034; canvas \ 0034;或桌面應用程式的 UI 介面，包括主視窗本身和快顯視窗、對話方塊和嚮導。 當您決定要使用的介面和最佳使用方式時，請遵循這些指導方針。
ms.assetid: E1FA78DA-D580-4B0E-AB59-29F013278766
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0664a6671e477f2b12f25b928fb39be69ac698ceba876aae5d8b65774e006edb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028956"
---
# <a name="windows-design-basics"></a>Windows (設計基本概念) 

> [!NOTE]
> 此設計指南是針對 Windows 7 所建立，而且尚未針對較新的 Windows 版本進行更新。 大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。

Windows 是桌面應用程式的主要「畫布」或 UI 介面，包括主視窗本身和快顯、對話方塊和嚮導。 當您決定要使用的介面和最佳使用方式時，請遵循這些指導方針。

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
<td><a href="win-window-mgt.md">視窗管理</a><br/></td>
<td>本文涵蓋 windows 最初顯示時 windows 的預設位置、相對於其他 windows (<a href="glossary.md">Z 順序</a> 的堆疊順序) 、其初始大小，以及其顯示如何影響輸入焦點。<br/></td>
</tr>
<tr class="even">
<td><a href="win-window-frames.md">窗框</a><br/></td>
<td>大部分的程式都應該使用標準的視窗框架。 沉浸式應用程式可以有隱藏視窗框架的全螢幕模式。 請考慮策略性地使用半透明，以提供更簡單、更淺、更緊密的外觀。 <br/></td>
</tr>
<tr class="odd">
<td><a href="win-dialog-box.md">對話方塊</a><br/></td>
<td>對話方塊是一種次要視窗，可讓使用者執行命令、詢問使用者問題，或是為使用者提供資訊或進度的意見反應。<br/></td>
</tr>
<tr class="even">
<td><a href="win-common-dlg.md">一般對話</a><br/></td>
<td>Microsoft Windows 通用對話方塊包含 [開啟檔案]、[儲存檔案]、[開啟資料夾]、[尋找和取代]、[列印]、[版面設定]、[字型] 和 [色彩] 對話方塊。<br/></td>
</tr>
<tr class="odd">
<td><a href="win-wizards.md">精靈</a><br/></td>
<td>比較古怪名稱雖然很棒，但卻不是一種特殊形式的使用者介面，而且只有特定範圍的公用程式。 <br/></td>
</tr>
<tr class="even">
<td><a href="win-property-win.md">屬性 Windows</a><br/></td>
<td>[屬性視窗] 是下列使用者介面類別型的集體名稱 (Ui) ：<br/>
<ul>
<li>屬性工作表：用於 <strong>在對話方塊中，用來查看和變更物件或物件集合的屬性</strong>。</li>
<li>屬性偵測器： <strong>在窗格中用來查看和變更物件或物件集合的屬性</strong>。</li>
<li>[選項] 對話方塊：用來 <strong>查看和變更應用程式的選項</strong>。</li>
</ul></td>
</tr>
</tbody>
</table>



 

 

