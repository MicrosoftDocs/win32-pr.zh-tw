---
description: 表示 Shell 中的物件。
title: 'IShellDispatch 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9B429C03-7F80-45db-B8CD-58D19FAD2E61
ms.openlocfilehash: 20c6cc9f0b3a2e2fde8f56311564d63bc1cc9c0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972409"
---
# <a name="ishelldispatch-object"></a><span data-ttu-id="3d281-103">IShellDispatch 物件</span><span class="sxs-lookup"><span data-stu-id="3d281-103">IShellDispatch object</span></span>

<span data-ttu-id="3d281-104">表示 Shell 中的物件。</span><span class="sxs-lookup"><span data-stu-id="3d281-104">Represents an object in the Shell.</span></span> <span data-ttu-id="3d281-105">系統會提供方法來控制 Shell，並在 Shell 中執行命令。</span><span class="sxs-lookup"><span data-stu-id="3d281-105">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="3d281-106">也有方法可以取得其他與 Shell 相關的物件。</span><span class="sxs-lookup"><span data-stu-id="3d281-106">There are also methods to obtain other Shell-related objects.</span></span>

> [!Note]  
> <span data-ttu-id="3d281-107">**IShellDispatch** 是透過 [**Shell**](shell.md) 物件來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="3d281-107">**IShellDispatch** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="3d281-108">成員</span><span class="sxs-lookup"><span data-stu-id="3d281-108">Members</span></span>

<span data-ttu-id="3d281-109">**IShellDispatch** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3d281-109">The **IShellDispatch** object has these types of members:</span></span>

-   [<span data-ttu-id="3d281-110">方法</span><span class="sxs-lookup"><span data-stu-id="3d281-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="3d281-111">屬性</span><span class="sxs-lookup"><span data-stu-id="3d281-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3d281-112">方法</span><span class="sxs-lookup"><span data-stu-id="3d281-112">Methods</span></span>

<span data-ttu-id="3d281-113">**IShellDispatch** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3d281-113">The **IShellDispatch** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="3d281-114">方法</span><span class="sxs-lookup"><span data-stu-id="3d281-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="3d281-115">描述</span><span class="sxs-lookup"><span data-stu-id="3d281-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3d281-116"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d281-116"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3d281-117">建立對話方塊，讓使用者選取資料夾，然後傳回選取的資料夾 <a href="folder.md"><strong>資料夾</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="3d281-117">Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="folder.md"><strong>Folder</strong></a> object.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3d281-118"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d281-118"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3d281-119">將桌面上的所有視窗都串聯在一起。</span><span class="sxs-lookup"><span data-stu-id="3d281-119">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="3d281-120">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [串聯 <strong>視窗</strong>] 相同。</span><span class="sxs-lookup"><span data-stu-id="3d281-120">This method has the same effect as right-clicking the taskbar and selecting <strong>Cascade windows</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3d281-121"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d281-121"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3d281-122">執行指定的主控台應用程式。</span><span class="sxs-lookup"><span data-stu-id="3d281-122">Runs the specified Control Panel application.</span></span> <span data-ttu-id="3d281-123">如果應用程式已經開啟，則會啟動執行中的實例。</span><span class="sxs-lookup"><span data-stu-id="3d281-123">If the application is already open, it will activate the running instance.</span></span> <br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="3d281-124">從 Windows Vista 開始，大部分的主控台應用程式都是 Shell 專案，無法使用此功能開啟。</span><span class="sxs-lookup"><span data-stu-id="3d281-124">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="3d281-125">若要開啟這些主控台的應用程式，請將正式名稱傳遞給 control.exe。</span><span class="sxs-lookup"><span data-stu-id="3d281-125">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="3d281-126">例如：</span><span class="sxs-lookup"><span data-stu-id="3d281-126">For example:</span></span></p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3d281-127"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d281-127"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3d281-128">從其銜接站彈出電腦。</span><span class="sxs-lookup"><span data-stu-id="3d281-128">Ejects the computer from its docking station.</span></span> <span data-ttu-id="3d281-129">這與按一下 [ <strong>開始</strong> ] 功能表並選取 [ <strong>退出</strong>電腦] 的方式相同，如果您的電腦支援此命令。</span><span class="sxs-lookup"><span data-stu-id="3d281-129">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Eject PC</strong>, if your computer supports this command.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3d281-130"><a href="ishelldispatch-explore.md"><strong>探索</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d281-130"><a href="ishelldispatch-explore.md"><strong>Explore</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3d281-131">在 Windows 檔案總管視窗中開啟指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="3d281-131">Opens a specified folder in a Windows Explorer window.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3d281-132"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d281-132"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3d281-133">向使用者顯示 [ <strong>執行</strong> ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="3d281-133">Displays the <strong>Run</strong> dialog to the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3d281-134"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d281-134"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3d281-135">顯示 [ <strong>搜尋結果：電腦</strong> ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="3d281-135">Displays the <strong>Search Results: Computers</strong> dialog box.</span></span> <span data-ttu-id="3d281-136">此對話方塊會顯示指定電腦的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="3d281-136">The dialog box shows the result of the search for a specified computer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3d281-137"><a href="ishelldispatch-findfiles.md"><strong>Findfiles.ps1</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d281-137"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3d281-138">顯示 [ <strong>尋找：所有</strong> 檔案] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="3d281-138">Displays the <strong>Find: All Files</strong> dialog box.</span></span> <span data-ttu-id="3d281-139">這等同于按一下 [ <strong>開始</strong> ] 功能表，然後選取 [ <strong>搜尋</strong>]。</span><span class="sxs-lookup"><span data-stu-id="3d281-139">This is the same as clicking the <strong>Start</strong> menu and then selecting <strong>Search</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3d281-140"><a href="ishelldispatch-help.md"><strong>Help</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d281-140"><a href="ishelldispatch-help.md"><strong>Help</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3d281-141">顯示 [Windows 說明及支援] 視窗。</span><span class="sxs-lookup"><span data-stu-id="3d281-141">Displays the Windows Help and Support window.</span></span> <span data-ttu-id="3d281-142">這個方法與按一下 [ <strong>開始</strong> ] 功能表並選取 [說明 <strong>及支援</strong>] 的效果相同。</span><span class="sxs-lookup"><span data-stu-id="3d281-142">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Help and Support</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3d281-143"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d281-143"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3d281-144">最小化桌面上的所有視窗。</span><span class="sxs-lookup"><span data-stu-id="3d281-144">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="3d281-145">這個方法的效果與在工作列上按一下滑鼠右鍵，並選取 [將舊版系統上的 <strong>所有視窗最小化</strong> ]，或按一下工作列上的 [ <strong>顯示桌面</strong> ] 圖示。</span><span class="sxs-lookup"><span data-stu-id="3d281-145">This method has the same effect as right-clicking the taskbar and selecting <strong>Minimize All Windows</strong> on older systems or clicking the <strong>Show Desktop</strong> icon on the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3d281-146"><a href="ishelldispatch-namespace.md"><strong>命名 空間</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d281-146"><a href="ishelldispatch-namespace.md"><strong>NameSpace</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3d281-147">建立並傳回指定資料夾的 <a href="folder.md"><strong>資料夾</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="3d281-147">Creates and returns a <a href="folder.md"><strong>Folder</strong></a> object for the specified folder.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3d281-148"><a href="ishelldispatch-open.md"><strong>打開</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d281-148"><a href="ishelldispatch-open.md"><strong>Open</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3d281-149">開啟指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="3d281-149">Opens the specified folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3d281-150"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d281-150"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3d281-151">重新整理 [ <strong>開始</strong> ] 功能表的內容。</span><span class="sxs-lookup"><span data-stu-id="3d281-151">Refreshes the contents of the <strong>Start</strong> menu.</span></span> <span data-ttu-id="3d281-152">只能與 Windows XP 之前的系統搭配使用。</span><span class="sxs-lookup"><span data-stu-id="3d281-152">Used only with systems preceding Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3d281-153"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d281-153"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3d281-154">顯示 [ <strong>日期和時間</strong> ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="3d281-154">Displays the <strong>Date and Time</strong> dialog box.</span></span> <span data-ttu-id="3d281-155">這個方法的效果與以滑鼠右鍵按一下工作列狀態區域中的時鐘，然後選取 [ <strong>調整日期/時間</strong>]。</span><span class="sxs-lookup"><span data-stu-id="3d281-155">This method has the same effect as right-clicking the clock in the taskbar status area and selecting <strong>Adjust date/time</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3d281-156"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d281-156"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3d281-157">顯示 <strong>關機 Windows</strong> ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="3d281-157">Displays the <strong>Shut Down Windows</strong> dialog box.</span></span> <span data-ttu-id="3d281-158">這等同于按一下 [ <strong>開始</strong> ] 功能表，然後選取 [ <strong>關機</strong>]。</span><span class="sxs-lookup"><span data-stu-id="3d281-158">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Shut Down</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3d281-159"><a href="ishelldispatch-suspend.md"><strong>暫停</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d281-159"><a href="ishelldispatch-suspend.md"><strong>Suspend</strong></a></span></span></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3d281-160"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d281-160"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3d281-161">以水準方式並排顯示桌面上的所有視窗。</span><span class="sxs-lookup"><span data-stu-id="3d281-161">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="3d281-162">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [ <strong>顯示視窗堆疊</strong>]。</span><span class="sxs-lookup"><span data-stu-id="3d281-162">This method has the same effect as right-clicking the taskbar and selecting <strong>Show windows stacked</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3d281-163"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d281-163"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3d281-164">垂直並排顯示桌面上的所有視窗。</span><span class="sxs-lookup"><span data-stu-id="3d281-164">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="3d281-165">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [並排 <strong>顯示視窗</strong>]。</span><span class="sxs-lookup"><span data-stu-id="3d281-165">This method has the same effect as right-clicking the taskbar and selecting <strong>Show windows side by side</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3d281-166"><a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d281-166"><a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3d281-167">顯示 [ <strong>工作列] 和 [開始功能表屬性</strong> ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="3d281-167">Displays the <strong>Taskbar and Start Menu Properties</strong> dialog box.</span></span> <span data-ttu-id="3d281-168">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [ <strong>屬性</strong>] 相同。</span><span class="sxs-lookup"><span data-stu-id="3d281-168">This method has the same effect as right-clicking the taskbar and selecting <strong>Properties</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3d281-169"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d281-169"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3d281-170">將所有桌面視窗還原到最後一個 <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> 命令之前的狀態。</span><span class="sxs-lookup"><span data-stu-id="3d281-170">Restores all desktop windows to the state they were in before the last <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> command.</span></span> <span data-ttu-id="3d281-171">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [ <strong>復原最小化</strong> 舊系統上的所有 Windows (]) 或第二次按一下工作列中的 [ <strong>顯示桌面</strong> ] 圖示。</span><span class="sxs-lookup"><span data-stu-id="3d281-171">This method has the same effect as right-clicking the taskbar and selecting <strong>Undo Minimize All Windows</strong> (on older systems) or a second clicking of the <strong>Show Desktop</strong> icon in the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3d281-172"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d281-172"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3d281-173">建立並傳回 <a href="shellwindows.md"><strong>ShellWindows</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="3d281-173">Creates and returns a <a href="shellwindows.md"><strong>ShellWindows</strong></a> object.</span></span> <span data-ttu-id="3d281-174">此物件代表屬於 Shell 的所有已開啟視窗的集合。</span><span class="sxs-lookup"><span data-stu-id="3d281-174">This object represents a collection of all of the open windows that belong to the Shell.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="3d281-175">屬性</span><span class="sxs-lookup"><span data-stu-id="3d281-175">Properties</span></span>

<span data-ttu-id="3d281-176">**IShellDispatch** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3d281-176">The **IShellDispatch** object has these properties.</span></span>



| <span data-ttu-id="3d281-177">屬性</span><span class="sxs-lookup"><span data-stu-id="3d281-177">Property</span></span>                                                     | <span data-ttu-id="3d281-178">存取類型</span><span class="sxs-lookup"><span data-stu-id="3d281-178">Access type</span></span>          | <span data-ttu-id="3d281-179">Description</span><span class="sxs-lookup"><span data-stu-id="3d281-179">Description</span></span>                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="3d281-180">**Application**</span><span class="sxs-lookup"><span data-stu-id="3d281-180">**Application**</span></span>](ishelldispatch-application.md)<br/> | <span data-ttu-id="3d281-181">唯讀</span><span class="sxs-lookup"><span data-stu-id="3d281-181">Read-only</span></span><br/> | <span data-ttu-id="3d281-182">包含代表應用程式的物件。</span><span class="sxs-lookup"><span data-stu-id="3d281-182">Contains an object that represents an application.</span></span><br/>                    |
| [<span data-ttu-id="3d281-183">**父代**</span><span class="sxs-lookup"><span data-stu-id="3d281-183">**Parent**</span></span>](ishelldispatch-parent.md)<br/>           | <span data-ttu-id="3d281-184">唯讀</span><span class="sxs-lookup"><span data-stu-id="3d281-184">Read-only</span></span><br/> | <span data-ttu-id="3d281-185">抓取物件，該物件表示目前物件的父系。</span><span class="sxs-lookup"><span data-stu-id="3d281-185">Retrieves an object that represents the parent of the current object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3d281-186">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d281-186">Requirements</span></span>



| <span data-ttu-id="3d281-187">需求</span><span class="sxs-lookup"><span data-stu-id="3d281-187">Requirement</span></span> | <span data-ttu-id="3d281-188">值</span><span class="sxs-lookup"><span data-stu-id="3d281-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d281-189">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d281-189">Minimum supported client</span></span><br/> | <span data-ttu-id="3d281-190">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d281-190">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3d281-191">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d281-191">Minimum supported server</span></span><br/> | <span data-ttu-id="3d281-192">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d281-192">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3d281-193">標頭</span><span class="sxs-lookup"><span data-stu-id="3d281-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d281-194"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="3d281-194"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3d281-195">Idl</span><span class="sxs-lookup"><span data-stu-id="3d281-195">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3d281-196"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3d281-196"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3d281-197">DLL</span><span class="sxs-lookup"><span data-stu-id="3d281-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d281-198"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="3d281-198"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d281-199">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d281-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d281-200">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="3d281-200">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="3d281-201">**Shell 物件**</span><span class="sxs-lookup"><span data-stu-id="3d281-201">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 
