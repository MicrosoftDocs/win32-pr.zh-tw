---
description: 本節說明 Shell 所執行的 Windows 物件。
title: 腳本和 Microsoft Visual Basic 的 Shell 物件
ms.topic: article
ms.date: 05/31/2018
ms.assetid: eee58404-808b-451c-8325-8dcd9537fd11
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 52958c68edfd81771267c7a7ed29e42ab8ed1d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513609"
---
# <a name="shell-objects-for-scripting-and-microsoft-visual-basic"></a><span data-ttu-id="f4e90-103">腳本和 Microsoft Visual Basic 的 Shell 物件</span><span class="sxs-lookup"><span data-stu-id="f4e90-103">Shell Objects for Scripting and Microsoft Visual Basic</span></span>

<span data-ttu-id="f4e90-104">本節說明 Shell 所執行的 Windows 物件。</span><span class="sxs-lookup"><span data-stu-id="f4e90-104">This section describes the Windows objects implemented by the Shell.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f4e90-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="f4e90-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f4e90-106">主題</span><span class="sxs-lookup"><span data-stu-id="f4e90-106">Topic</span></span></th>
<th><span data-ttu-id="f4e90-107">描述</span><span class="sxs-lookup"><span data-stu-id="f4e90-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f4e90-108"><a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-108"><a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-109">允許用戶端管理 NTFS 磁片區的全域磁片配額設定。</span><span class="sxs-lookup"><span data-stu-id="f4e90-109">Allows a client to manage an NTFS volume's global disk quota settings.</span></span> <span data-ttu-id="f4e90-110">這個物件讓 <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a> 介面的基本功能可供腳本和 Microsoft Visual Basic 應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="f4e90-110">This object makes the essential functionality of the <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a> interface available to scripting and Microsoft Visual Basic-based applications.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f4e90-111"><a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-111"><a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-112">可讓系統管理員管理磁片區的磁片配額屬性。</span><span class="sxs-lookup"><span data-stu-id="f4e90-112">Allows an administrator to manage a volume's disk quota properties.</span></span> <span data-ttu-id="f4e90-113">NTFS 檔案系統可讓系統管理員藉由為每個使用者配置指定的磁碟空間數量或 <em>配額限制</em>，來管理共用磁片區上的磁片使用量。</span><span class="sxs-lookup"><span data-stu-id="f4e90-113">The NTFS file system allows an administrator to manage disk usage on a shared volume by allocating a specified amount of disk space, or <em>quota limit</em>, to each user.</span></span> <span data-ttu-id="f4e90-114">您可以使用此物件來設定將自動指派給所有新使用者的預設配額限制。</span><span class="sxs-lookup"><span data-stu-id="f4e90-114">You can use this object to set the default quota limit that will be automatically assigned to all new users.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f4e90-115"><a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-115"><a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-116">接收 <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a> 視窗註冊事件。</span><span class="sxs-lookup"><span data-stu-id="f4e90-116">Receives <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a> window registration events.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f4e90-117"><a href="folder.md"><strong>資料夾</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-117"><a href="folder.md"><strong>Folder</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-118">表示 Shell 資料夾。</span><span class="sxs-lookup"><span data-stu-id="f4e90-118">Represents a Shell folder.</span></span> <span data-ttu-id="f4e90-119">此物件包含屬性和方法，可讓您取得資料夾的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f4e90-119">This object contains properties and methods that allow you to retrieve information about the folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f4e90-120"><a href="folder2-object.md"><strong>Folder2</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-120"><a href="folder2-object.md"><strong>Folder2</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-121">擴充 <a href="folder.md"><strong>資料夾</strong></a> 物件以支援離線資料夾。</span><span class="sxs-lookup"><span data-stu-id="f4e90-121">Extends the <a href="folder.md"><strong>Folder</strong></a> object to support offline folders.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f4e90-122"><a href="folderitem.md"><strong>FolderItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-122"><a href="folderitem.md"><strong>FolderItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-123">表示 Shell 資料夾中的專案。</span><span class="sxs-lookup"><span data-stu-id="f4e90-123">Represents an item in a Shell folder.</span></span> <span data-ttu-id="f4e90-124">此物件包含屬性和方法，可讓您取得專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f4e90-124">This object contains properties and methods that allow you to retrieve information about the item.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f4e90-125"><a href="folderitems.md"><strong>FolderItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-125"><a href="folderitems.md"><strong>FolderItems</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-126">表示 Shell 資料夾中的專案集合。</span><span class="sxs-lookup"><span data-stu-id="f4e90-126">Represents the collection of items in a Shell folder.</span></span> <span data-ttu-id="f4e90-127">此物件包含屬性和方法，可讓您取得集合的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f4e90-127">This object contains properties and methods that allow you to retrieve information about the collection.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f4e90-128"><a href="folderitems2-object.md"><strong>FolderItems2</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-128"><a href="folderitems2-object.md"><strong>FolderItems2</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-129">擴充 <a href="folderitems.md"><strong>FolderItems</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="f4e90-129">Extends the <a href="folderitems.md"><strong>FolderItems</strong></a> object.</span></span> <span data-ttu-id="f4e90-130">它支援一個額外的方法。</span><span class="sxs-lookup"><span data-stu-id="f4e90-130">It supports one additional method.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f4e90-131"><a href="folderitems3-object.md"><strong>FolderItems3</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-131"><a href="folderitems3-object.md"><strong>FolderItems3</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-132">擴充 <a href="folderitems2-object.md"><strong>FolderItems2</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="f4e90-132">Extends the <a href="folderitems2-object.md"><strong>FolderItems2</strong></a> object.</span></span> <span data-ttu-id="f4e90-133">此物件支援其他方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="f4e90-133">This object supports an additional method and property.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f4e90-134"><a href="folderitemverb.md"><strong>FolderItemVerb</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-134"><a href="folderitemverb.md"><strong>FolderItemVerb</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-135">表示專案可用的單一動詞。</span><span class="sxs-lookup"><span data-stu-id="f4e90-135">Represents a single verb available to an item.</span></span> <span data-ttu-id="f4e90-136">此物件包含屬性和方法，可讓您取得動詞的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f4e90-136">This object contains properties and methods that allow you to retrieve information about the verb.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f4e90-137"><a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-137"><a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-138">表示 Shell 資料夾中專案的動詞集合。</span><span class="sxs-lookup"><span data-stu-id="f4e90-138">Represents the collection of verbs for an item in a Shell folder.</span></span> <span data-ttu-id="f4e90-139">此物件包含屬性和方法，可讓您取得集合的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f4e90-139">This object contains properties and methods that allow you to retrieve information about the collection.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f4e90-140"><a href="ishelldispatch.md"><strong>IShellDispatch</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-140"><a href="ishelldispatch.md"><strong>IShellDispatch</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-141">表示 Shell 中的物件。</span><span class="sxs-lookup"><span data-stu-id="f4e90-141">Represents an object in the Shell.</span></span> <span data-ttu-id="f4e90-142">系統會提供方法來控制 Shell，並在 Shell 中執行命令。</span><span class="sxs-lookup"><span data-stu-id="f4e90-142">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="f4e90-143">也有方法可以取得其他與 Shell 相關的物件。</span><span class="sxs-lookup"><span data-stu-id="f4e90-143">There are also methods to obtain other Shell-related objects.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="f4e90-144">
<a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> 是透過 <a href="shell.md"><strong>Shell</strong></a> 物件來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="f4e90-144">
<a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f4e90-145"><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-145"><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-146">使用各種新功能來擴充 <a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="f4e90-146">Extends the <a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> object with a variety of new functionality.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="f4e90-147">
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> 是透過 <a href="shell.md"><strong>Shell</strong></a> 物件來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="f4e90-147">
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f4e90-148"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-148"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-149">擴充 <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="f4e90-149">Extends the <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> object.</span></span> <span data-ttu-id="f4e90-150">除了<strong>IShellDispatch2</strong>支援的屬性和方法之外， <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a>還支援一個新的方法。</span><span class="sxs-lookup"><span data-stu-id="f4e90-150"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> supports one new method in addition to the properties and methods supported by <strong>IShellDispatch2</strong>.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="f4e90-151">
<a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> 是透過 <a href="shell.md"><strong>Shell</strong></a> 物件來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="f4e90-151">
<a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f4e90-152"><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-152"><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-153">擴充 <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="f4e90-153">Extends the <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> object.</span></span> <span data-ttu-id="f4e90-154">除了 <strong>IShellDispatch3</strong>支援的屬性和方法之外， <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> 還支援四個額外的方法。</span><span class="sxs-lookup"><span data-stu-id="f4e90-154">In addition to the properties and methods supported by <strong>IShellDispatch3</strong>, <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> supports four additional methods.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="f4e90-155">
<a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> 是透過 <a href="shell.md"><strong>Shell</strong></a> 物件來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="f4e90-155">
<a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f4e90-156"><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-156"><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-157">擴充 <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="f4e90-157">Extends the <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> object.</span></span> <span data-ttu-id="f4e90-158">除了 <strong>IShellDispatch4</strong>所支援的屬性和方法之外， <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> 還新增了在3d 堆疊中顯示開啟視窗的方法。</span><span class="sxs-lookup"><span data-stu-id="f4e90-158">In addition to the properties and methods supported by <strong>IShellDispatch4</strong>, <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> adds a method that displays open windows in a 3D stack.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="f4e90-159">
<a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> 是透過 <a href="shell.md"><strong>Shell</strong></a> 物件來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="f4e90-159">
<a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f4e90-160"><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-160"><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-161">擴充 <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="f4e90-161">Extends the <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> object.</span></span> <span data-ttu-id="f4e90-162">除了 <strong>IShellDispatch5</strong>支援的屬性和方法之外， <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> 也會新增可顯示應用程式搜尋窗格的方法。</span><span class="sxs-lookup"><span data-stu-id="f4e90-162">In addition to the properties and methods supported by <strong>IShellDispatch5</strong>, <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> adds a method that displays the Apps Search pane.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="f4e90-163">
<a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> 是透過 <a href="shell.md"><strong>Shell</strong></a> 物件來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="f4e90-163">
<a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f4e90-164"><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-164"><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-165">擴充 <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a> 物件，並支援一個額外的屬性。</span><span class="sxs-lookup"><span data-stu-id="f4e90-165">Extends the <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a> object and supports one additional property.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f4e90-166"><a href="newwdevents.md"><strong>NewWDEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-166"><a href="newwdevents.md"><strong>NewWDEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-167">藉由啟用在 wizard 中裝載的伺服器端頁面，來擴充 <a href="webwizardhost.md"><strong>WebWizardHost</strong></a> 物件，以確認使用者已通過 Microsoft 帳戶驗證。</span><span class="sxs-lookup"><span data-stu-id="f4e90-167">Extends the <a href="webwizardhost.md"><strong>WebWizardHost</strong></a> object by enabling server-side pages hosted in a wizard to verify that the user has been authenticated through a Microsoft account.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f4e90-168"><a href="shell.md"><strong>殼層</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-168"><a href="shell.md"><strong>Shell</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-169">表示 Shell 中的物件。</span><span class="sxs-lookup"><span data-stu-id="f4e90-169">Represents the objects in the Shell.</span></span> <span data-ttu-id="f4e90-170">系統會提供方法來控制 Shell，並在 Shell 中執行命令。</span><span class="sxs-lookup"><span data-stu-id="f4e90-170">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="f4e90-171">也有方法可以取得其他與 Shell 相關的物件。</span><span class="sxs-lookup"><span data-stu-id="f4e90-171">There are also methods to obtain other Shell-related objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f4e90-172"><a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-172"><a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-173">擴充 <a href="folderitem.md"><strong>FolderItem</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="f4e90-173">Extends the <a href="folderitem.md"><strong>FolderItem</strong></a> object.</span></span> <span data-ttu-id="f4e90-174">除了 <strong>FolderItem</strong>支援的屬性和方法之外， <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a> 還有兩個額外的方法。</span><span class="sxs-lookup"><span data-stu-id="f4e90-174">In addition to the properties and methods supported by <strong>FolderItem</strong>, <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a> has two additional methods.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f4e90-175"><a href="shellfolderview.md"><strong>ShellFolderView</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-175"><a href="shellfolderview.md"><strong>ShellFolderView</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-176">代表視圖中的物件，並提供用來取得視圖內容相關資訊的屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="f4e90-176">Represents the objects in a view and provides properties and methods used to obtain information about the contents of the view.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f4e90-177"><a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-177"><a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-178">將指定之 <a href="shellfolderview.md"><strong>ShellFolderView</strong></a> 物件所引發的事件轉送到對應的 <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a> 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="f4e90-178">Forwards the events fired by a specified <a href="shellfolderview.md"><strong>ShellFolderView</strong></a> object to corresponding <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a> event handlers.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f4e90-179"><a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-179"><a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-180">管理 Shell 連結。</span><span class="sxs-lookup"><span data-stu-id="f4e90-180">Manages Shell links.</span></span> <span data-ttu-id="f4e90-181">這個物件讓 <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a> 介面的許多功能可供腳本應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="f4e90-181">This object makes much of the functionality of the <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a> interface available to scripting applications.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f4e90-182"><a href="shelluihelper.md"><strong>ShellUIHelper</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-182"><a href="shelluihelper.md"><strong>ShellUIHelper</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-183">由 Shell 所執行，以協助編寫腳本和 Visual Basic 開發人員使用 Shell 中提供的一些功能。</span><span class="sxs-lookup"><span data-stu-id="f4e90-183">Implemented by the Shell to help script and Visual Basic developers use some of the features available in the Shell.</span></span> <span data-ttu-id="f4e90-184"><a href="shelluihelper.md"><strong>ShellUIHelper</strong></a>物件沒有任何屬性或事件。</span><span class="sxs-lookup"><span data-stu-id="f4e90-184">The <a href="shelluihelper.md"><strong>ShellUIHelper</strong></a> object does not have any properties or events.</span></span> <span data-ttu-id="f4e90-185">提供方法以將專案新增至 Shell。</span><span class="sxs-lookup"><span data-stu-id="f4e90-185">Methods are provided to add items to the Shell.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f4e90-186"><a href="shellwindows.md"><strong>ShellWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-186"><a href="shellwindows.md"><strong>ShellWindows</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-187">表示屬於 Shell 之開啟視窗的集合。</span><span class="sxs-lookup"><span data-stu-id="f4e90-187">Represents a collection of the open windows that belong to the Shell.</span></span> <span data-ttu-id="f4e90-188">與這個物件相關聯的方法可以控制和執行 Shell 內的命令，以及取得其他與 Shell 相關的物件。</span><span class="sxs-lookup"><span data-stu-id="f4e90-188">Methods associated with this objects can control and execute commands within the Shell, and obtain other Shell-related objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f4e90-189"><a href="webwizardhost.md"><strong>WebWizardHost</strong></a></span><span class="sxs-lookup"><span data-stu-id="f4e90-189"><a href="webwizardhost.md"><strong>WebWizardHost</strong></a></span></span><br/></td>
<td><span data-ttu-id="f4e90-190">公開方法，這些方法可讓您在 wizard 擴充功能中裝載的 HTML 網頁與 wizard 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="f4e90-190">Exposes methods that enable HTML pages which are hosted in a wizard extension to communicate with the wizard.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




