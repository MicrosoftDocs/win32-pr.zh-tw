---
description: Windows Installer 為套件開發人員提供撰寫具有多個功能層級之內部使用者介面的功能。
ms.assetid: 9f5796a7-e244-4fc8-af85-52a147bb2c0b
title: 消費者介面層級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a835d1b11a4db4393041e83c1b1dc885018610f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195260"
---
# <a name="user-interface-levels"></a><span data-ttu-id="27ed5-103">消費者介面層級</span><span class="sxs-lookup"><span data-stu-id="27ed5-103">User Interface Levels</span></span>

<span data-ttu-id="27ed5-104">Windows Installer 為套件開發人員提供撰寫具有多個功能層級之內部使用者介面的功能。</span><span class="sxs-lookup"><span data-stu-id="27ed5-104">Windows Installer provides package developers the capability to author an internal user interface that has multiple levels of functionality.</span></span> <span data-ttu-id="27ed5-105">因為內部 UI 必須由套件的作者所建立，所以完整 UI 的行為、縮減的 UI、基本 UI 和無層級取決於安裝套件。</span><span class="sxs-lookup"><span data-stu-id="27ed5-105">Because the internal UI must be created by the author of the package, the behavior of the full UI, reduced UI, basic UI, and None levels depends on the installation package.</span></span> <span data-ttu-id="27ed5-106">下表說明一般歸屬至 UI 層級的功能。</span><span class="sxs-lookup"><span data-stu-id="27ed5-106">The following table describes the functionality commonly ascribed to UI levels.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="27ed5-107">UI 層級</span><span class="sxs-lookup"><span data-stu-id="27ed5-107">UI Level</span></span></th>
<th><span data-ttu-id="27ed5-108">Description</span><span class="sxs-lookup"><span data-stu-id="27ed5-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27ed5-109">完整 UI</span><span class="sxs-lookup"><span data-stu-id="27ed5-109">Full UI</span></span></td>
<td><span data-ttu-id="27ed5-110">顯示已撰寫至內部 UI 的強制回應和非強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="27ed5-110">Displays modal and modeless dialog boxes that have been authored into the internal UI.</span></span> <span data-ttu-id="27ed5-111">顯示撰寫的 <a href="error-dialog.md">錯誤對話方塊</a> 。</span><span class="sxs-lookup"><span data-stu-id="27ed5-111">Displays authored <a href="error-dialog.md">Error Dialog</a> boxes.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="27ed5-112">強制回應對話方塊需要使用者輸入，才能繼續安裝，而且可以在<a href="dialog-table.md">對話方塊</a>資料表的 [屬性] 資料行中設定<a href="modal-dialog-style-bit.md">強制回應對話方塊樣式位</a>來指定。</span><span class="sxs-lookup"><span data-stu-id="27ed5-112">Modal dialog boxes require user input before the installation can continue and are specified by setting the <a href="modal-dialog-style-bit.md">Modal Dialog Style Bit</a> in the Attributes column of the <a href="dialog-table.md">Dialog</a> table.</span></span> <span data-ttu-id="27ed5-113">非強制回應對話方塊不需要使用者輸入，就能繼續進行安裝。</span><span class="sxs-lookup"><span data-stu-id="27ed5-113">A modeless dialog box does not require user input for the installation to continue.</span></span>
</blockquote>
<br/> <span data-ttu-id="27ed5-114">完整的 UI 通常會顯現 <a href="user-interface-wizard-behavior.md">消費者介面的 Wizard 行為</a>。</span><span class="sxs-lookup"><span data-stu-id="27ed5-114">A full UI commonly exhibits <a href="user-interface-wizard-behavior.md">User Interface Wizard Behavior</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27ed5-115">縮小 UI</span><span class="sxs-lookup"><span data-stu-id="27ed5-115">Reduced UI</span></span></td>
<td><span data-ttu-id="27ed5-116">顯示任何已在 UI 中撰寫的非強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="27ed5-116">Displays any modeless dialog boxes that have been authored into the UI.</span></span> <span data-ttu-id="27ed5-117">不會顯示任何撰寫的強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="27ed5-117">Does not display any authored modal dialog boxes.</span></span> <span data-ttu-id="27ed5-118">顯示撰寫的 <a href="error-dialog.md">錯誤對話方塊</a> 。</span><span class="sxs-lookup"><span data-stu-id="27ed5-118">Displays authored <a href="error-dialog.md">Error Dialog</a> boxes.</span></span> <span data-ttu-id="27ed5-119">顯示 <a href="authoring-disk-prompt-messages.md">磁片提示</a> 訊息。</span><span class="sxs-lookup"><span data-stu-id="27ed5-119">Displays <a href="authoring-disk-prompt-messages.md">Disk Prompt</a> messages.</span></span> <span data-ttu-id="27ed5-120">顯示 <a href="filesinuse-dialog.md">FilesInUse 對話方塊</a> 。</span><span class="sxs-lookup"><span data-stu-id="27ed5-120">Displays <a href="filesinuse-dialog.md">FilesInUse Dialog</a> boxes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27ed5-121">基本 UI</span><span class="sxs-lookup"><span data-stu-id="27ed5-121">Basic UI</span></span></td>
<td><span data-ttu-id="27ed5-122">顯示顯示進度訊息的內建非強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="27ed5-122">Displays the built-in modeless dialog boxes that show progress messages.</span></span> <span data-ttu-id="27ed5-123">顯示內建的錯誤對話方塊。</span><span class="sxs-lookup"><span data-stu-id="27ed5-123">Displays built-in error dialog boxes.</span></span> <span data-ttu-id="27ed5-124">不會顯示任何撰寫的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="27ed5-124">Does not display any authored dialog boxes.</span></span> <span data-ttu-id="27ed5-125">藉由顯示包含 <a href="diskprompt.md"><strong>DiskPrompt</strong></a> 屬性值的對話方塊，提示使用者插入磁片。</span><span class="sxs-lookup"><span data-stu-id="27ed5-125">Prompts users to insert a disk by displaying a dialog box containing the <a href="diskprompt.md"><strong>DiskPrompt</strong></a> property value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27ed5-126">無</span><span class="sxs-lookup"><span data-stu-id="27ed5-126">None</span></span></td>
<td><span data-ttu-id="27ed5-127">None 表示無訊息安裝，不會顯示任何 UI。</span><span class="sxs-lookup"><span data-stu-id="27ed5-127">None means a silent installation that displays no UI.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="27ed5-128">您可以使用 [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)來設定內部 UI 的層級。</span><span class="sxs-lookup"><span data-stu-id="27ed5-128">The level of the internal UI can be set using [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span></span> <span data-ttu-id="27ed5-129">安裝程式會將 [**UILevel**](uilevel.md) 屬性設定為目前的 UI 層級。</span><span class="sxs-lookup"><span data-stu-id="27ed5-129">The installer sets the [**UILevel**](uilevel.md) property to the current level of the UI.</span></span>

<span data-ttu-id="27ed5-130">如果設定了 [**LIMITUI**](limitui.md) 屬性，則在安裝套件時所使用的使用者介面 (UI) 層級會限制為「基本」。</span><span class="sxs-lookup"><span data-stu-id="27ed5-130">If the [**LIMITUI**](limitui.md) property is set, the user interface (UI) level used when installing the package is restricted to Basic.</span></span>

<span data-ttu-id="27ed5-131">如需 UI 撰寫的範例，請參閱 [安裝範例](an-installation-example.md)。</span><span class="sxs-lookup"><span data-stu-id="27ed5-131">For an example of UI authoring, see [An Installation Example](an-installation-example.md).</span></span>

 

 




