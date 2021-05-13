---
description: 表示 Shell 中的物件。 系統會提供方法來控制 Shell，並在 Shell 中執行命令。 也有方法可以取得其他與 Shell 相關的物件。
title: 命令介面物件 (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 75fc151e-5b9e-476b-b4e5-b848917357a8
ms.openlocfilehash: 55f8062b71e553ec5ceefa413b45f439874744b8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841759"
---
# <a name="shell-object"></a><span data-ttu-id="c97c9-105">Shell 物件</span><span class="sxs-lookup"><span data-stu-id="c97c9-105">Shell object</span></span>

<span data-ttu-id="c97c9-106">表示 Shell 中的物件。</span><span class="sxs-lookup"><span data-stu-id="c97c9-106">Represents the objects in the Shell.</span></span> <span data-ttu-id="c97c9-107">系統會提供方法來控制 Shell，並在 Shell 中執行命令。</span><span class="sxs-lookup"><span data-stu-id="c97c9-107">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="c97c9-108">也有方法可以取得其他與 Shell 相關的物件。</span><span class="sxs-lookup"><span data-stu-id="c97c9-108">There are also methods to obtain other Shell-related objects.</span></span>

## <a name="members"></a><span data-ttu-id="c97c9-109">成員</span><span class="sxs-lookup"><span data-stu-id="c97c9-109">Members</span></span>

<span data-ttu-id="c97c9-110">**Shell** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c97c9-110">The **Shell** object has these types of members:</span></span>

-   [<span data-ttu-id="c97c9-111">方法</span><span class="sxs-lookup"><span data-stu-id="c97c9-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c97c9-112">屬性</span><span class="sxs-lookup"><span data-stu-id="c97c9-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c97c9-113">方法</span><span class="sxs-lookup"><span data-stu-id="c97c9-113">Methods</span></span>

<span data-ttu-id="c97c9-114">**Shell** 物件具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c97c9-114">The **Shell** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="c97c9-115">方法</span><span class="sxs-lookup"><span data-stu-id="c97c9-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="c97c9-116">描述</span><span class="sxs-lookup"><span data-stu-id="c97c9-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c97c9-117"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-117"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-118">將檔案加入最近使用的 (MRU) 清單中。</span><span class="sxs-lookup"><span data-stu-id="c97c9-118">Adds a file to the most recently used (MRU) list.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c97c9-119"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-119"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-120">建立對話方塊，讓使用者選取資料夾，然後傳回選取的資料夾 <a href="folder.md"><strong>資料夾</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="c97c9-120">Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="folder.md"><strong>Folder</strong></a> object.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c97c9-121"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-121"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-122">判斷目前的使用者是否可以啟動和停止命名服務。</span><span class="sxs-lookup"><span data-stu-id="c97c9-122">Determines if the current user can start and stop the named service.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c97c9-123"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-123"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-124">將桌面上的所有視窗都串聯在一起。</span><span class="sxs-lookup"><span data-stu-id="c97c9-124">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="c97c9-125">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [串聯 <strong>視窗</strong>] 相同。</span><span class="sxs-lookup"><span data-stu-id="c97c9-125">This method has the same effect as right-clicking the taskbar and selecting <strong>Cascade Windows</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c97c9-126"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-126"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-127">執行指定的主控台 ( \* cpl) 應用程式。</span><span class="sxs-lookup"><span data-stu-id="c97c9-127">Runs the specified Control Panel (\*.cpl) application.</span></span> <span data-ttu-id="c97c9-128">如果應用程式已經開啟，則會啟動執行中的實例。</span><span class="sxs-lookup"><span data-stu-id="c97c9-128">If the application is already open, it will activate the running instance.</span></span> <br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="c97c9-129">從 Windows Vista 開始，大部分的主控台應用程式都是 Shell 專案，無法使用此功能開啟。</span><span class="sxs-lookup"><span data-stu-id="c97c9-129">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="c97c9-130">若要開啟這些主控台的應用程式，請將正式名稱傳遞給 control.exe。</span><span class="sxs-lookup"><span data-stu-id="c97c9-130">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="c97c9-131">例如：</span><span class="sxs-lookup"><span data-stu-id="c97c9-131">For example:</span></span></p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c97c9-132"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-132"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-133">從其銜接站彈出電腦。</span><span class="sxs-lookup"><span data-stu-id="c97c9-133">Ejects the computer from its docking station.</span></span> <span data-ttu-id="c97c9-134">這與按一下 [ <strong>開始</strong> ] 功能表並選取 [ <strong>退出</strong>電腦] 的方式相同，如果您的電腦支援此命令。</span><span class="sxs-lookup"><span data-stu-id="c97c9-134">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Eject PC</strong>, if your computer supports this command.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c97c9-135"><a href="shell-explore.md"><strong>探討</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-135"><a href="shell-explore.md"><strong>Explore</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-136">在 Windows 檔案總管視窗中開啟指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="c97c9-136">Opens a specified folder in a Windows Explorer window.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c97c9-137"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-137"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-138">取得指定 Internet Explorer 原則的值。</span><span class="sxs-lookup"><span data-stu-id="c97c9-138">Gets the value for a specified Internet Explorer policy.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c97c9-139"><a href="shell-filerun.md"><strong>FileRun</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-139"><a href="shell-filerun.md"><strong>FileRun</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-140">向使用者顯示 [ <strong>執行</strong> ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c97c9-140">Displays the <strong>Run</strong> dialog to the user.</span></span> <span data-ttu-id="c97c9-141">這個方法與按一下 [ <strong>開始</strong> ] 功能表並選取 [ <strong>執行</strong>] 的效果相同。</span><span class="sxs-lookup"><span data-stu-id="c97c9-141">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Run</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c97c9-142"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-142"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-143">顯示 [ <strong>搜尋結果：電腦</strong> ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c97c9-143">Displays the <strong>Search Results: Computers</strong> dialog box.</span></span> <span data-ttu-id="c97c9-144">此對話方塊會顯示指定電腦的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="c97c9-144">The dialog box shows the result of the search for a specified computer.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c97c9-145"><a href="shell-findfiles.md"><strong>Findfiles.ps1</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-145"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-146">顯示 [ <strong>尋找：所有</strong> 檔案] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c97c9-146">Displays the <strong>Find: All Files</strong> dialog box.</span></span> <span data-ttu-id="c97c9-147">這等同于按一下 [ <strong>開始</strong> ] 功能表，然後選取 [ <strong>搜尋</strong> (] 或其對等專案（在 Windows XP 之前的系統下）。</span><span class="sxs-lookup"><span data-stu-id="c97c9-147">This is the same as clicking the <strong>Start</strong> menu and then selecting <strong>Search</strong> (or its equivalent under systems earlier than Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c97c9-148"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-148"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-149">顯示 [ <strong>尋找印表機</strong> ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c97c9-149">Displays the <strong>Find Printer</strong> dialog box.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c97c9-150"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-150"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-151">捕獲全域 Shell 設定。</span><span class="sxs-lookup"><span data-stu-id="c97c9-151">Retrieves a global Shell setting.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c97c9-152"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-152"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-153">捕獲系統資訊。</span><span class="sxs-lookup"><span data-stu-id="c97c9-153">Retrieves system information.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c97c9-154"><a href="shell-help.md"><strong>Help</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-154"><a href="shell-help.md"><strong>Help</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-155">顯示 Windows 說明及支援中心。</span><span class="sxs-lookup"><span data-stu-id="c97c9-155">Displays the Windows Help and Support Center.</span></span> <span data-ttu-id="c97c9-156">這個方法與按一下 [ <strong>開始</strong> ] 功能表並選取 [說明 <strong>及支援</strong>] 的效果相同。</span><span class="sxs-lookup"><span data-stu-id="c97c9-156">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Help and Support</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c97c9-157"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-157"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-158">從登錄抓取群組的限制設定。</span><span class="sxs-lookup"><span data-stu-id="c97c9-158">Retrieves a group's restriction setting from the registry.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c97c9-159"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-159"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-160">傳回值，這個值表示特定服務是否正在執行。</span><span class="sxs-lookup"><span data-stu-id="c97c9-160">Returns a value that indicates whether a particular service is running.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c97c9-161"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-161"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-162">最小化桌面上的所有視窗。</span><span class="sxs-lookup"><span data-stu-id="c97c9-162">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="c97c9-163">這個方法的效果與在工作列上按一下滑鼠右鍵，並選取 [將舊版系統上的 <strong>所有視窗最小化</strong> ]，或在 windows 2000 或 windows XP 的工作列快速啟動區域中按一下 [ <strong>顯示桌面</strong> ] 圖示。</span><span class="sxs-lookup"><span data-stu-id="c97c9-163">This method has the same effect as right-clicking the taskbar and selecting <strong>Minimize All Windows</strong> on older systems or clicking the <strong>Show Desktop</strong> icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c97c9-164"><a href="shell-namespace.md"><strong>命名 空間</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-164"><a href="shell-namespace.md"><strong>NameSpace</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-165">建立並傳回指定資料夾的 <a href="folder.md"><strong>資料夾</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="c97c9-165">Creates and returns a <a href="folder.md"><strong>Folder</strong></a> object for the specified folder.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c97c9-166"><a href="shell-open.md"><strong>打開</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-166"><a href="shell-open.md"><strong>Open</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-167">開啟指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="c97c9-167">Opens the specified folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c97c9-168"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-168"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-169">重新整理 [ <strong>開始</strong> ] 功能表的內容。</span><span class="sxs-lookup"><span data-stu-id="c97c9-169">Refreshes the contents of the <strong>Start</strong> menu.</span></span> <span data-ttu-id="c97c9-170">只能與 Windows XP 之前的系統搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c97c9-170">Used only with systems preceding Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c97c9-171"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-171"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-172">顯示應用程式搜尋窗格。</span><span class="sxs-lookup"><span data-stu-id="c97c9-172">Displays the Apps Search pane.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c97c9-173"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-173"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-174">啟動命名服務。</span><span class="sxs-lookup"><span data-stu-id="c97c9-174">Starts a named service.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c97c9-175"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-175"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-176">停止已命名的服務。</span><span class="sxs-lookup"><span data-stu-id="c97c9-176">Stops a named service.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c97c9-177"><a href="shell-settime.md"><strong>SetTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-177"><a href="shell-settime.md"><strong>SetTime</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-178">顯示 [ <strong>日期和時間屬性</strong> ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c97c9-178">Displays the <strong>Date and Time Properties</strong> dialog box.</span></span> <span data-ttu-id="c97c9-179">這個方法的效果與以滑鼠右鍵按一下工作列狀態區域中的時鐘，然後選取 [ <strong>調整日期/時間</strong>]。</span><span class="sxs-lookup"><span data-stu-id="c97c9-179">This method has the same effect as right-clicking the clock in the taskbar status area and selecting <strong>Adjust Date/Time</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c97c9-180"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-180"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-181">在指定的檔案上執行指定的作業。</span><span class="sxs-lookup"><span data-stu-id="c97c9-181">Performs a specified operation on a specified file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c97c9-182"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-182"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-183">顯示瀏覽器列。</span><span class="sxs-lookup"><span data-stu-id="c97c9-183">Displays a browser bar.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c97c9-184"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-184"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-185">顯示 <strong>關機 Windows</strong> ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c97c9-185">Displays the <strong>Shut Down Windows</strong> dialog box.</span></span> <span data-ttu-id="c97c9-186">這等同于按一下 [ <strong>開始</strong> ] 功能表，然後選取 [ <strong>關機</strong>]。</span><span class="sxs-lookup"><span data-stu-id="c97c9-186">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Shut Down</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c97c9-187"><a href="shell-suspend.md"><strong>暫止</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-187"><a href="shell-suspend.md"><strong>Suspend</strong></a></span></span></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c97c9-188"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-188"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-189">以水準方式並排顯示桌面上的所有視窗。</span><span class="sxs-lookup"><span data-stu-id="c97c9-189">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="c97c9-190">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [ <strong>水準並排顯示視窗</strong>] 效果相同。</span><span class="sxs-lookup"><span data-stu-id="c97c9-190">This method has the same effect as right-clicking the taskbar and selecting <strong>Tile Windows Horizontally</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c97c9-191"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-191"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-192">垂直並排顯示桌面上的所有視窗。</span><span class="sxs-lookup"><span data-stu-id="c97c9-192">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="c97c9-193">這個方法的效果與在工作列上按一下滑鼠右鍵，然後垂直選取 [ <strong>並排顯示視窗</strong>] 效果相同。</span><span class="sxs-lookup"><span data-stu-id="c97c9-193">This method has the same effect as right-clicking the taskbar and selecting <strong>Tile Windows Vertically</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c97c9-194"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-194"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-195">顯示或隱藏桌面。</span><span class="sxs-lookup"><span data-stu-id="c97c9-195">Displays or hides the desktop.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c97c9-196"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-196"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-197">顯示 [ <strong>工作列] 和 [開始功能表屬性</strong> ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c97c9-197">Displays the <strong>Taskbar and Start Menu Properties</strong> dialog box.</span></span> <span data-ttu-id="c97c9-198">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [ <strong>屬性</strong>] 相同。</span><span class="sxs-lookup"><span data-stu-id="c97c9-198">This method has the same effect as right-clicking the taskbar and selecting <strong>Properties</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c97c9-199"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-199"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-200">將所有桌面視窗還原到最後一個 <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> 命令之前的相同狀態。</span><span class="sxs-lookup"><span data-stu-id="c97c9-200">Restores all desktop windows to the same state they were in before the last <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> command.</span></span> <span data-ttu-id="c97c9-201">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [復原]，將舊版系統上的 <strong>所有視窗最小化</strong> ，或第二次按一下 windows 2000 或 windows XP 中工作列的 [快速啟動] 區域中的 [ <strong>顯示桌面</strong> ] 圖示。</span><span class="sxs-lookup"><span data-stu-id="c97c9-201">This method has the same effect as right-clicking the taskbar and selecting <strong>Undo Minimize All Windows</strong> on older systems or a second clicking of the <strong>Show Desktop</strong> icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c97c9-202"><a href="shell-windows.md"><strong>Windows</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-202"><a href="shell-windows.md"><strong>Windows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-203">建立並傳回 <a href="shellwindows.md"><strong>ShellWindows</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="c97c9-203">Creates and returns a <a href="shellwindows.md"><strong>ShellWindows</strong></a> object.</span></span> <span data-ttu-id="c97c9-204">此物件代表屬於 Shell 的所有已開啟視窗的集合。</span><span class="sxs-lookup"><span data-stu-id="c97c9-204">This object represents a collection of all of the open windows that belong to the Shell.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c97c9-205"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-205"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-206">顯示 [ <strong>Windows 安全性</strong> ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c97c9-206">Displays the <strong>Windows Security</strong> dialog box.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c97c9-207"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></span><span class="sxs-lookup"><span data-stu-id="c97c9-207"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c97c9-208">將開啟的視窗顯示在您可以切換的3D 堆疊中。</span><span class="sxs-lookup"><span data-stu-id="c97c9-208">Displays your open windows in a 3D stack that you can flip through.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="c97c9-209">屬性</span><span class="sxs-lookup"><span data-stu-id="c97c9-209">Properties</span></span>

<span data-ttu-id="c97c9-210">**Shell** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c97c9-210">The **Shell** object has these properties.</span></span>



| <span data-ttu-id="c97c9-211">屬性</span><span class="sxs-lookup"><span data-stu-id="c97c9-211">Property</span></span>                                            | <span data-ttu-id="c97c9-212">存取類型</span><span class="sxs-lookup"><span data-stu-id="c97c9-212">Access type</span></span>          | <span data-ttu-id="c97c9-213">描述</span><span class="sxs-lookup"><span data-stu-id="c97c9-213">Description</span></span>                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="c97c9-214">**Application**</span><span class="sxs-lookup"><span data-stu-id="c97c9-214">**Application**</span></span>](shell-application.md)<br/> | <span data-ttu-id="c97c9-215">唯讀</span><span class="sxs-lookup"><span data-stu-id="c97c9-215">Read-only</span></span><br/> | <span data-ttu-id="c97c9-216">包含物件的應用程式物件。</span><span class="sxs-lookup"><span data-stu-id="c97c9-216">Contains the object's Application object.</span></span><br/>                        |
| [<span data-ttu-id="c97c9-217">**父代**</span><span class="sxs-lookup"><span data-stu-id="c97c9-217">**Parent**</span></span>](shell-parent.md)<br/>           | <span data-ttu-id="c97c9-218">唯讀</span><span class="sxs-lookup"><span data-stu-id="c97c9-218">Read-only</span></span><br/> | <span data-ttu-id="c97c9-219">取得物件，表示目前物件的父系。</span><span class="sxs-lookup"><span data-stu-id="c97c9-219">Gets an object that represents the parent of the current object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c97c9-220">規格需求</span><span class="sxs-lookup"><span data-stu-id="c97c9-220">Requirements</span></span>



| <span data-ttu-id="c97c9-221">需求</span><span class="sxs-lookup"><span data-stu-id="c97c9-221">Requirement</span></span> | <span data-ttu-id="c97c9-222">值</span><span class="sxs-lookup"><span data-stu-id="c97c9-222">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c97c9-223">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c97c9-223">Minimum supported client</span></span><br/> | <span data-ttu-id="c97c9-224">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c97c9-224">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c97c9-225">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c97c9-225">Minimum supported server</span></span><br/> | <span data-ttu-id="c97c9-226">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c97c9-226">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c97c9-227">標頭</span><span class="sxs-lookup"><span data-stu-id="c97c9-227">Header</span></span><br/>                   | <dl> <span data-ttu-id="c97c9-228"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="c97c9-228"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c97c9-229">Idl</span><span class="sxs-lookup"><span data-stu-id="c97c9-229">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c97c9-230"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c97c9-230"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c97c9-231">DLL</span><span class="sxs-lookup"><span data-stu-id="c97c9-231">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c97c9-232"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="c97c9-232"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
