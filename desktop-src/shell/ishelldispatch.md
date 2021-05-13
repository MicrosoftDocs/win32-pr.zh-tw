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
ms.openlocfilehash: 02fbead4b2d40a91ec6dab70f536d1ea3241ee84
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840889"
---
# <a name="ishelldispatch-object"></a><span data-ttu-id="d8617-103">IShellDispatch 物件</span><span class="sxs-lookup"><span data-stu-id="d8617-103">IShellDispatch object</span></span>

<span data-ttu-id="d8617-104">表示 Shell 中的物件。</span><span class="sxs-lookup"><span data-stu-id="d8617-104">Represents an object in the Shell.</span></span> <span data-ttu-id="d8617-105">系統會提供方法來控制 Shell，並在 Shell 中執行命令。</span><span class="sxs-lookup"><span data-stu-id="d8617-105">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="d8617-106">也有方法可以取得其他與 Shell 相關的物件。</span><span class="sxs-lookup"><span data-stu-id="d8617-106">There are also methods to obtain other Shell-related objects.</span></span>

> [!Note]  
> <span data-ttu-id="d8617-107">**IShellDispatch** 是透過 [**Shell**](shell.md) 物件來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="d8617-107">**IShellDispatch** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="d8617-108">成員</span><span class="sxs-lookup"><span data-stu-id="d8617-108">Members</span></span>

<span data-ttu-id="d8617-109">**IShellDispatch** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d8617-109">The **IShellDispatch** object has these types of members:</span></span>

-   [<span data-ttu-id="d8617-110">方法</span><span class="sxs-lookup"><span data-stu-id="d8617-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="d8617-111">屬性</span><span class="sxs-lookup"><span data-stu-id="d8617-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d8617-112">方法</span><span class="sxs-lookup"><span data-stu-id="d8617-112">Methods</span></span>

<span data-ttu-id="d8617-113">**IShellDispatch** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d8617-113">The **IShellDispatch** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="d8617-114">方法</span><span class="sxs-lookup"><span data-stu-id="d8617-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="d8617-115">描述</span><span class="sxs-lookup"><span data-stu-id="d8617-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d8617-116"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8617-116"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d8617-117">建立對話方塊，讓使用者選取資料夾，然後傳回選取的資料夾 <a href="folder.md"><strong>資料夾</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="d8617-117">Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="folder.md"><strong>Folder</strong></a> object.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d8617-118"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8617-118"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d8617-119">將桌面上的所有視窗都串聯在一起。</span><span class="sxs-lookup"><span data-stu-id="d8617-119">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="d8617-120">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [串聯 <strong>視窗</strong>] 相同。</span><span class="sxs-lookup"><span data-stu-id="d8617-120">This method has the same effect as right-clicking the taskbar and selecting <strong>Cascade windows</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d8617-121"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8617-121"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d8617-122">執行指定的主控台應用程式。</span><span class="sxs-lookup"><span data-stu-id="d8617-122">Runs the specified Control Panel application.</span></span> <span data-ttu-id="d8617-123">如果應用程式已經開啟，則會啟動執行中的實例。</span><span class="sxs-lookup"><span data-stu-id="d8617-123">If the application is already open, it will activate the running instance.</span></span> <br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="d8617-124">從 Windows Vista 開始，大部分的主控台應用程式都是 Shell 專案，無法使用此功能開啟。</span><span class="sxs-lookup"><span data-stu-id="d8617-124">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="d8617-125">若要開啟這些主控台的應用程式，請將正式名稱傳遞給 control.exe。</span><span class="sxs-lookup"><span data-stu-id="d8617-125">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="d8617-126">例如：</span><span class="sxs-lookup"><span data-stu-id="d8617-126">For example:</span></span></p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d8617-127"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8617-127"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d8617-128">從其銜接站彈出電腦。</span><span class="sxs-lookup"><span data-stu-id="d8617-128">Ejects the computer from its docking station.</span></span> <span data-ttu-id="d8617-129">這與按一下 [ <strong>開始</strong> ] 功能表並選取 [ <strong>退出</strong>電腦] 的方式相同，如果您的電腦支援此命令。</span><span class="sxs-lookup"><span data-stu-id="d8617-129">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Eject PC</strong>, if your computer supports this command.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d8617-130"><a href="ishelldispatch-explore.md"><strong>探討</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8617-130"><a href="ishelldispatch-explore.md"><strong>Explore</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d8617-131">在 Windows 檔案總管視窗中開啟指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="d8617-131">Opens a specified folder in a Windows Explorer window.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d8617-132"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8617-132"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d8617-133">向使用者顯示 [ <strong>執行</strong> ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="d8617-133">Displays the <strong>Run</strong> dialog to the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d8617-134"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8617-134"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d8617-135">顯示 [ <strong>搜尋結果：電腦</strong> ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="d8617-135">Displays the <strong>Search Results: Computers</strong> dialog box.</span></span> <span data-ttu-id="d8617-136">此對話方塊會顯示指定電腦的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="d8617-136">The dialog box shows the result of the search for a specified computer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d8617-137"><a href="ishelldispatch-findfiles.md"><strong>Findfiles.ps1</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8617-137"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d8617-138">顯示 [ <strong>尋找：所有</strong> 檔案] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="d8617-138">Displays the <strong>Find: All Files</strong> dialog box.</span></span> <span data-ttu-id="d8617-139">這等同于按一下 [ <strong>開始</strong> ] 功能表，然後選取 [ <strong>搜尋</strong>]。</span><span class="sxs-lookup"><span data-stu-id="d8617-139">This is the same as clicking the <strong>Start</strong> menu and then selecting <strong>Search</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d8617-140"><a href="ishelldispatch-help.md"><strong>Help</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8617-140"><a href="ishelldispatch-help.md"><strong>Help</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d8617-141">顯示 [Windows 說明及支援] 視窗。</span><span class="sxs-lookup"><span data-stu-id="d8617-141">Displays the Windows Help and Support window.</span></span> <span data-ttu-id="d8617-142">這個方法與按一下 [ <strong>開始</strong> ] 功能表並選取 [說明 <strong>及支援</strong>] 的效果相同。</span><span class="sxs-lookup"><span data-stu-id="d8617-142">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Help and Support</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d8617-143"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8617-143"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d8617-144">最小化桌面上的所有視窗。</span><span class="sxs-lookup"><span data-stu-id="d8617-144">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="d8617-145">這個方法的效果與在工作列上按一下滑鼠右鍵，並選取 [將舊版系統上的 <strong>所有視窗最小化</strong> ]，或按一下工作列上的 [ <strong>顯示桌面</strong> ] 圖示。</span><span class="sxs-lookup"><span data-stu-id="d8617-145">This method has the same effect as right-clicking the taskbar and selecting <strong>Minimize All Windows</strong> on older systems or clicking the <strong>Show Desktop</strong> icon on the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d8617-146"><a href="ishelldispatch-namespace.md"><strong>命名 空間</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8617-146"><a href="ishelldispatch-namespace.md"><strong>NameSpace</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d8617-147">建立並傳回指定資料夾的 <a href="folder.md"><strong>資料夾</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="d8617-147">Creates and returns a <a href="folder.md"><strong>Folder</strong></a> object for the specified folder.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d8617-148"><a href="ishelldispatch-open.md"><strong>打開</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8617-148"><a href="ishelldispatch-open.md"><strong>Open</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d8617-149">開啟指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="d8617-149">Opens the specified folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d8617-150"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8617-150"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d8617-151">重新整理 [ <strong>開始</strong> ] 功能表的內容。</span><span class="sxs-lookup"><span data-stu-id="d8617-151">Refreshes the contents of the <strong>Start</strong> menu.</span></span> <span data-ttu-id="d8617-152">只能與 Windows XP 之前的系統搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d8617-152">Used only with systems preceding Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d8617-153"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8617-153"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d8617-154">顯示 [ <strong>日期和時間</strong> ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="d8617-154">Displays the <strong>Date and Time</strong> dialog box.</span></span> <span data-ttu-id="d8617-155">這個方法的效果與以滑鼠右鍵按一下工作列狀態區域中的時鐘，然後選取 [ <strong>調整日期/時間</strong>]。</span><span class="sxs-lookup"><span data-stu-id="d8617-155">This method has the same effect as right-clicking the clock in the taskbar status area and selecting <strong>Adjust date/time</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d8617-156"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8617-156"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d8617-157">顯示 <strong>關機 Windows</strong> ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="d8617-157">Displays the <strong>Shut Down Windows</strong> dialog box.</span></span> <span data-ttu-id="d8617-158">這等同于按一下 [ <strong>開始</strong> ] 功能表，然後選取 [ <strong>關機</strong>]。</span><span class="sxs-lookup"><span data-stu-id="d8617-158">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Shut Down</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d8617-159"><a href="ishelldispatch-suspend.md"><strong>暫止</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8617-159"><a href="ishelldispatch-suspend.md"><strong>Suspend</strong></a></span></span></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d8617-160"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8617-160"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d8617-161">以水準方式並排顯示桌面上的所有視窗。</span><span class="sxs-lookup"><span data-stu-id="d8617-161">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="d8617-162">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [ <strong>顯示視窗堆疊</strong>]。</span><span class="sxs-lookup"><span data-stu-id="d8617-162">This method has the same effect as right-clicking the taskbar and selecting <strong>Show windows stacked</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d8617-163"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8617-163"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d8617-164">垂直並排顯示桌面上的所有視窗。</span><span class="sxs-lookup"><span data-stu-id="d8617-164">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="d8617-165">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [並排 <strong>顯示視窗</strong>]。</span><span class="sxs-lookup"><span data-stu-id="d8617-165">This method has the same effect as right-clicking the taskbar and selecting <strong>Show windows side by side</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d8617-166"><a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8617-166"><a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d8617-167">顯示 [ <strong>工作列] 和 [開始功能表屬性</strong> ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="d8617-167">Displays the <strong>Taskbar and Start Menu Properties</strong> dialog box.</span></span> <span data-ttu-id="d8617-168">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [ <strong>屬性</strong>] 相同。</span><span class="sxs-lookup"><span data-stu-id="d8617-168">This method has the same effect as right-clicking the taskbar and selecting <strong>Properties</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d8617-169"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8617-169"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d8617-170">將所有桌面視窗還原到最後一個 <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> 命令之前的狀態。</span><span class="sxs-lookup"><span data-stu-id="d8617-170">Restores all desktop windows to the state they were in before the last <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> command.</span></span> <span data-ttu-id="d8617-171">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [ <strong>復原最小化</strong> 舊系統上的所有 Windows (]) 或第二次按一下工作列中的 [ <strong>顯示桌面</strong> ] 圖示。</span><span class="sxs-lookup"><span data-stu-id="d8617-171">This method has the same effect as right-clicking the taskbar and selecting <strong>Undo Minimize All Windows</strong> (on older systems) or a second clicking of the <strong>Show Desktop</strong> icon in the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d8617-172"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8617-172"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d8617-173">建立並傳回 <a href="shellwindows.md"><strong>ShellWindows</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="d8617-173">Creates and returns a <a href="shellwindows.md"><strong>ShellWindows</strong></a> object.</span></span> <span data-ttu-id="d8617-174">此物件代表屬於 Shell 的所有已開啟視窗的集合。</span><span class="sxs-lookup"><span data-stu-id="d8617-174">This object represents a collection of all of the open windows that belong to the Shell.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="d8617-175">屬性</span><span class="sxs-lookup"><span data-stu-id="d8617-175">Properties</span></span>

<span data-ttu-id="d8617-176">**IShellDispatch** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d8617-176">The **IShellDispatch** object has these properties.</span></span>



| <span data-ttu-id="d8617-177">屬性</span><span class="sxs-lookup"><span data-stu-id="d8617-177">Property</span></span>                                                     | <span data-ttu-id="d8617-178">存取類型</span><span class="sxs-lookup"><span data-stu-id="d8617-178">Access type</span></span>          | <span data-ttu-id="d8617-179">描述</span><span class="sxs-lookup"><span data-stu-id="d8617-179">Description</span></span>                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="d8617-180">**Application**</span><span class="sxs-lookup"><span data-stu-id="d8617-180">**Application**</span></span>](ishelldispatch-application.md)<br/> | <span data-ttu-id="d8617-181">唯讀</span><span class="sxs-lookup"><span data-stu-id="d8617-181">Read-only</span></span><br/> | <span data-ttu-id="d8617-182">包含代表應用程式的物件。</span><span class="sxs-lookup"><span data-stu-id="d8617-182">Contains an object that represents an application.</span></span><br/>                    |
| [<span data-ttu-id="d8617-183">**父代**</span><span class="sxs-lookup"><span data-stu-id="d8617-183">**Parent**</span></span>](ishelldispatch-parent.md)<br/>           | <span data-ttu-id="d8617-184">唯讀</span><span class="sxs-lookup"><span data-stu-id="d8617-184">Read-only</span></span><br/> | <span data-ttu-id="d8617-185">抓取物件，該物件表示目前物件的父系。</span><span class="sxs-lookup"><span data-stu-id="d8617-185">Retrieves an object that represents the parent of the current object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d8617-186">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8617-186">Requirements</span></span>



| <span data-ttu-id="d8617-187">需求</span><span class="sxs-lookup"><span data-stu-id="d8617-187">Requirement</span></span> | <span data-ttu-id="d8617-188">值</span><span class="sxs-lookup"><span data-stu-id="d8617-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8617-189">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d8617-189">Minimum supported client</span></span><br/> | <span data-ttu-id="d8617-190">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8617-190">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d8617-191">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d8617-191">Minimum supported server</span></span><br/> | <span data-ttu-id="d8617-192">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8617-192">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d8617-193">標頭</span><span class="sxs-lookup"><span data-stu-id="d8617-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8617-194"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="d8617-194"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d8617-195">Idl</span><span class="sxs-lookup"><span data-stu-id="d8617-195">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d8617-196"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d8617-196"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d8617-197">DLL</span><span class="sxs-lookup"><span data-stu-id="d8617-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8617-198"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="d8617-198"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8617-199">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8617-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8617-200">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="d8617-200">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="d8617-201">**Shell 物件**</span><span class="sxs-lookup"><span data-stu-id="d8617-201">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 
