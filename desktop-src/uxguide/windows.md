---
title: 'Windows (設計基本概念) '
description: Windows 是主要 \ 0034; canvas \ 0034;或桌面應用程式的 UI 介面，包括主視窗本身和快顯視窗、對話方塊和嚮導。 當您決定要使用的介面和最佳使用方式時，請遵循這些指導方針。
ms.assetid: E1FA78DA-D580-4B0E-AB59-29F013278766
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 5b7bb58750635af25d49208992d5583c44520a04
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "103945571"
---
# <a name="windows-design-basics"></a><span data-ttu-id="2f8a0-104">Windows (設計基本概念) </span><span class="sxs-lookup"><span data-stu-id="2f8a0-104">Windows (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="2f8a0-105">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="2f8a0-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="2f8a0-106">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="2f8a0-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="2f8a0-107">Windows 是桌面應用程式的主要「畫布」或 UI 介面，包括主要的 windows 和快顯、對話方塊和嚮導。</span><span class="sxs-lookup"><span data-stu-id="2f8a0-107">Windows are the main "canvases" or UI surfaces of your desktop app, including the main windows itself and pop-ups, dialogs, and wizards.</span></span> <span data-ttu-id="2f8a0-108">當您決定要使用的介面和最佳使用方式時，請遵循這些指導方針。</span><span class="sxs-lookup"><span data-stu-id="2f8a0-108">Follow these guidelines when deciding which surface to use and how best to use them.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2f8a0-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="2f8a0-109">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2f8a0-110">主題</span><span class="sxs-lookup"><span data-stu-id="2f8a0-110">Topic</span></span></th>
<th><span data-ttu-id="2f8a0-111">描述</span><span class="sxs-lookup"><span data-stu-id="2f8a0-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2f8a0-112"><a href="win-window-mgt.md">視窗管理</a></span><span class="sxs-lookup"><span data-stu-id="2f8a0-112"><a href="win-window-mgt.md">Window Management</a></span></span><br/></td>
<td><span data-ttu-id="2f8a0-113">本文涵蓋 windows 最初顯示時 windows 的預設位置、相對於其他 windows (<a href="glossary.md">Z 順序</a> 的堆疊順序) 、其初始大小，以及其顯示如何影響輸入焦點。</span><span class="sxs-lookup"><span data-stu-id="2f8a0-113">This article covers default placement of windows when initially displayed on the screen, their stacking order relative to other windows (<a href="glossary.md">Z order</a>), their initial size, and how their display affects input focus.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f8a0-114"><a href="win-window-frames.md">窗框</a></span><span class="sxs-lookup"><span data-stu-id="2f8a0-114"><a href="win-window-frames.md">Window Frames</a></span></span><br/></td>
<td><span data-ttu-id="2f8a0-115">大部分的程式都應該使用標準的視窗框架。</span><span class="sxs-lookup"><span data-stu-id="2f8a0-115">Most programs should use standard window frames.</span></span> <span data-ttu-id="2f8a0-116">沉浸式應用程式可以有隱藏視窗框架的全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="2f8a0-116">Immersive applications can have a full screen mode that hides the window frame.</span></span> <span data-ttu-id="2f8a0-117">請考慮策略性地使用半透明，以提供更簡單、更淺、更緊密的外觀。</span><span class="sxs-lookup"><span data-stu-id="2f8a0-117">Consider using glass strategically for a simpler, lighter, more cohesive look.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f8a0-118"><a href="win-dialog-box.md">對話方塊</a></span><span class="sxs-lookup"><span data-stu-id="2f8a0-118"><a href="win-dialog-box.md">Dialog Boxes</a></span></span><br/></td>
<td><span data-ttu-id="2f8a0-119">對話方塊是一種次要視窗，可讓使用者執行命令、詢問使用者問題，或是為使用者提供資訊或進度的意見反應。</span><span class="sxs-lookup"><span data-stu-id="2f8a0-119">A dialog box is a secondary window that allows users to perform a command, asks users a question, or provides users with information or progress feedback.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f8a0-120"><a href="win-common-dlg.md">一般對話</a></span><span class="sxs-lookup"><span data-stu-id="2f8a0-120"><a href="win-common-dlg.md">Common Dialogs</a></span></span><br/></td>
<td><span data-ttu-id="2f8a0-121">Microsoft Windows 通用對話方塊包含 [開啟檔案]、[儲存檔案]、[開啟資料夾]、[尋找和取代]、[列印]、[版面設定]、[字型] 和 [色彩] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="2f8a0-121">The Microsoft Windows common dialogs consist of the Open File, Save File, Open Folder, Find and Replace, Print, Page Setup, Font, and Color dialog boxes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f8a0-122"><a href="win-wizards.md">精靈</a></span><span class="sxs-lookup"><span data-stu-id="2f8a0-122"><a href="win-wizards.md">Wizards</a></span></span><br/></td>
<td><span data-ttu-id="2f8a0-123">比較古怪名稱雖然很棒，但卻不是一種特殊形式的使用者介面，而且只有特定範圍的公用程式。</span><span class="sxs-lookup"><span data-stu-id="2f8a0-123">Despite that wonderful, whimsical name, wizards are not really a special form of user interface, and they have only a particular range of utility.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f8a0-124"><a href="win-property-win.md">屬性視窗</a></span><span class="sxs-lookup"><span data-stu-id="2f8a0-124"><a href="win-property-win.md">Property Windows</a></span></span><br/></td>
<td><span data-ttu-id="2f8a0-125">[屬性視窗] 是下列使用者介面類別型的集體名稱 (Ui) ：</span><span class="sxs-lookup"><span data-stu-id="2f8a0-125">Property window is the collective name for the following types of user interfaces (UIs):</span></span><br/>
<ul>
<li><span data-ttu-id="2f8a0-126">屬性工作表：用於 <strong>在對話方塊中，用來查看和變更物件或物件集合的屬性</strong>。</span><span class="sxs-lookup"><span data-stu-id="2f8a0-126">Property sheet: used to <strong>view and change properties for an object or collection of objects in a dialog box</strong>.</span></span></li>
<li><span data-ttu-id="2f8a0-127">屬性偵測器： <strong>在窗格中用來查看和變更物件或物件集合的屬性</strong>。</span><span class="sxs-lookup"><span data-stu-id="2f8a0-127">Property inspector: used to <strong>view and change properties for an object or collection of objects in a pane</strong>.</span></span></li>
<li><span data-ttu-id="2f8a0-128">[選項] 對話方塊：用來 <strong>查看和變更應用程式的選項</strong>。</span><span class="sxs-lookup"><span data-stu-id="2f8a0-128">Options dialog box: used to <strong>view and change options for an application</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

