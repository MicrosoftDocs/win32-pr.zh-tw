---
description: 本節說明 Windows Shell 函數。
title: Shell 函數
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f4d6c0c4-8db3-4721-80f5-2a73bb57cd99
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5c8e31bdaac8ec581504326c17d5d37012dd019d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991582"
---
# <a name="shell-functions"></a><span data-ttu-id="aa227-103">Shell 函數</span><span class="sxs-lookup"><span data-stu-id="aa227-103">Shell Functions</span></span>

<span data-ttu-id="aa227-104">\[此函式已不再實作為。\]</span><span class="sxs-lookup"><span data-stu-id="aa227-104">\[This function is no longer implemented.\]</span></span>

<span data-ttu-id="aa227-105">本節說明 Windows Shell 函數。</span><span class="sxs-lookup"><span data-stu-id="aa227-105">This section describes the Windows Shell functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="aa227-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="aa227-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aa227-107">主題</span><span class="sxs-lookup"><span data-stu-id="aa227-107">Topic</span></span></th>
<th><span data-ttu-id="aa227-108">描述</span><span class="sxs-lookup"><span data-stu-id="aa227-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aa227-109"><a href="intsafe-h-functions-bumper.md">Intsafe .h 函數</a></span><span class="sxs-lookup"><span data-stu-id="aa227-109"><a href="intsafe-h-functions-bumper.md">Intsafe.h Functions</a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="aa227-110"><a href="library-functions-bumper.md">程式庫函式</a></span><span class="sxs-lookup"><span data-stu-id="aa227-110"><a href="library-functions-bumper.md">Library Functions</a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-111"><a href="path-functions.md">路徑函式</a></span><span class="sxs-lookup"><span data-stu-id="aa227-111"><a href="path-functions.md">Path Functions</a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="aa227-112"><a href="/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses"><strong>AssocCreateForClasses</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-112"><a href="/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses"><strong>AssocCreateForClasses</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-113">抓取可實 <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a> 介面的物件。</span><span class="sxs-lookup"><span data-stu-id="aa227-113">Retrieves an object that implements an <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a> interface.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-114"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-assocgetdetailsofpropkey"><strong>AssocGetDetailsOfPropKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-114"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-assocgetdetailsofpropkey"><strong>AssocGetDetailsOfPropKey</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-115">使用 <a href="nse-works.md">命名空間延伸</a>模組所提供的檔案關聯資訊，抓取指定屬性索引鍵的值。</span><span class="sxs-lookup"><span data-stu-id="aa227-115">Retrieves the value for a given property key using the file association information provided by the <a href="nse-works.md">Namespace Extensions</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-116"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2"><strong>CDefFolderMenu_Create2</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-116"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2"><strong>CDefFolderMenu_Create2</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-117">建立所選檔案資料夾物件群組的內容功能表。</span><span class="sxs-lookup"><span data-stu-id="aa227-117">Creates a context menu for a selected group of file folder objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-118"><a href="/windows/win32/api/ntquery/nf-ntquery-cishutdown"><strong>CIShutdown</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-118"><a href="/windows/win32/api/ntquery/nf-ntquery-cishutdown"><strong>CIShutdown</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-119">關閉內容索引器，並關閉所有開啟的目錄。</span><span class="sxs-lookup"><span data-stu-id="aa227-119">Shuts down the content indexer and closes all open catalogs.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="aa227-120">Windows 8 不支援這個函數。</span><span class="sxs-lookup"><span data-stu-id="aa227-120">This function is not supported as of Windows 8.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-121"><a href="/windows/desktop/api/Shellapi/nf-shellapi-commandlinetoargvw"><strong>CommandLineToArgvW</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-121"><a href="/windows/desktop/api/Shellapi/nf-shellapi-commandlinetoargvw"><strong>CommandLineToArgvW</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-122">剖析 Unicode 命令列字串，並傳回命令列引數的指標陣列，以及這類引數的計數，其方式類似于標準 C 執行時間 <em>argv</em> 和 <em>argc</em> 值。</span><span class="sxs-lookup"><span data-stu-id="aa227-122">Parses a Unicode command line string and returns an array of pointers to the command line arguments, along with a count of such arguments, in a way that is similar to the standard C run-time <em>argv</em> and <em>argc</em> values.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-123"><a href="/windows/desktop/api/cpl/nc-cpl-applet_proc"><strong>APPLET_PROC</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-123"><a href="/windows/desktop/api/cpl/nc-cpl-applet_proc"><strong>APPLET_PROC</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-124">作為主控台應用程式的進入點。</span><span class="sxs-lookup"><span data-stu-id="aa227-124">Serves as the entry point for a Control Panel application.</span></span> <span data-ttu-id="aa227-125">這是程式庫定義的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="aa227-125">This is a library-defined callback function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-126"><a href="/windows/desktop/api/Userenv/nf-userenv-createappcontainerprofile"><strong>CreateAppContainerProfile</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-126"><a href="/windows/desktop/api/Userenv/nf-userenv-createappcontainerprofile"><strong>CreateAppContainerProfile</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-127">針對 Windows Store 應用程式建立每個使用者的個別應用程式佈建檔。</span><span class="sxs-lookup"><span data-stu-id="aa227-127">Creates a per-user, per-app profile for Windows Store apps.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-128"><a href="/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock"><strong>CreateEnvironmentBlock</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-128"><a href="/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock"><strong>CreateEnvironmentBlock</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-129">抓取指定使用者的環境變數。</span><span class="sxs-lookup"><span data-stu-id="aa227-129">Retrieves the environment variables for the specified user.</span></span> <span data-ttu-id="aa227-130">然後可以將這個區塊傳遞給 <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera"><strong>CreateProcessAsUser</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="aa227-130">This block can then be passed to the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera"><strong>CreateProcessAsUser</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-131"><a href="createmrulist.md"><strong>CreateMRUListW</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-131"><a href="createmrulist.md"><strong>CreateMRUListW</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-132">建立最近使用的新 (MRU) 清單。</span><span class="sxs-lookup"><span data-stu-id="aa227-132">Creates a new most recently used (MRU) list.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-133"><a href="/windows/desktop/api/Userenv/nf-userenv-createprofile"><strong>CreateProfile</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-133"><a href="/windows/desktop/api/Userenv/nf-userenv-createprofile"><strong>CreateProfile</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-134">建立新的使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="aa227-134">Creates a new user profile.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-135"><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-defscreensaverproc"><strong>DefScreenSaverProc</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-135"><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-defscreensaverproc"><strong>DefScreenSaverProc</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-136">提供螢幕保護裝置應用程式未處理之任何訊息的預設處理。</span><span class="sxs-lookup"><span data-stu-id="aa227-136">Provides default processing for any messages that a screen saver application does not process.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-137"><a href="/windows/desktop/api/Commctrl/nf-commctrl-defsubclassproc"><strong>DefSubclassProc</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-137"><a href="/windows/desktop/api/Commctrl/nf-commctrl-defsubclassproc"><strong>DefSubclassProc</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-138">呼叫視窗子類別鏈中的下一個處理常式。</span><span class="sxs-lookup"><span data-stu-id="aa227-138">Calls the next handler in a window's subclass chain.</span></span> <span data-ttu-id="aa227-139">子類別鏈中的最後一個處理常式會呼叫視窗的原始視窗程式。</span><span class="sxs-lookup"><span data-stu-id="aa227-139">The last handler in the subclass chain calls the original window procedure for the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-140"><a href="/windows/desktop/api/Userenv/nf-userenv-deleteappcontainerprofile"><strong>DeleteAppContainerProfile</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-140"><a href="/windows/desktop/api/Userenv/nf-userenv-deleteappcontainerprofile"><strong>DeleteAppContainerProfile</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-141">刪除指定的每個使用者、個別應用程式佈建檔。</span><span class="sxs-lookup"><span data-stu-id="aa227-141">Deletes the specified per-user, per-app profile.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-142"><a href="/windows/desktop/api/Userenv/nf-userenv-deleteprofilea"><strong>DeleteProfile</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-142"><a href="/windows/desktop/api/Userenv/nf-userenv-deleteprofilea"><strong>DeleteProfile</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-143">從指定的電腦刪除使用者設定檔和所有使用者相關的設定。</span><span class="sxs-lookup"><span data-stu-id="aa227-143">Deletes the user profile and all user-related settings from the specified computer.</span></span> <span data-ttu-id="aa227-144">呼叫端必須具有系統管理許可權，才能刪除使用者的設定檔。</span><span class="sxs-lookup"><span data-stu-id="aa227-144">The caller must have administrative privileges to delete a user's profile.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-145"><a href="/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock"><strong>DestroyEnvironmentBlock</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-145"><a href="/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock"><strong>DestroyEnvironmentBlock</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-146">釋放 <a href="/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock"><strong>CreateEnvironmentBlock</strong></a> 函數所建立的環境變數。</span><span class="sxs-lookup"><span data-stu-id="aa227-146">Frees environment variables created by the <a href="/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock"><strong>CreateEnvironmentBlock</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-147"><a href="/windows/desktop/api/Userenv/nf-userenv-deriveappcontainersidfromappcontainername"><strong>DeriveAppContainerSidFromAppContainerName</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-147"><a href="/windows/desktop/api/Userenv/nf-userenv-deriveappcontainersidfromappcontainername"><strong>DeriveAppContainerSidFromAppContainerName</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-148">取得指定設定檔的 SID。</span><span class="sxs-lookup"><span data-stu-id="aa227-148">Gets the SID of the specified profile.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-149"><a href="/windows/desktop/api/userenv/nf-userenv-deriverestrictedappcontainersidfromappcontainersidandrestrictedname"><strong>DeriveRestrictedAppContainerSidFromAppContainerSidAndRestrictedName</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-149"><a href="/windows/desktop/api/userenv/nf-userenv-deriverestrictedappcontainersidfromappcontainersidandrestrictedname"><strong>DeriveRestrictedAppContainerSidFromAppContainerSidAndRestrictedName</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-150">DeriveRestrictedAppContainerSidFromAppContainerSidAndRestrictedName 已保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="aa227-150">DeriveRestrictedAppContainerSidFromAppContainerSidAndRestrictedName is reserved for future use.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-151"><a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><em>DLLGETVERSIONPROC</em></a></span><span class="sxs-lookup"><span data-stu-id="aa227-151"><a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><em>DLLGETVERSIONPROC</em></a></span></span><br/></td>
<td><span data-ttu-id="aa227-152">由許多 Windows Shell Dll 所執行，可讓應用程式取得 DLL 特定的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="aa227-152">Implemented by many of the Windows Shell DLLs to allow applications to obtain DLL-specific version information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-153"><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles"><strong>DragAcceptFiles</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-153"><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles"><strong>DragAcceptFiles</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-154">註冊視窗是否接受已卸載的檔案。</span><span class="sxs-lookup"><span data-stu-id="aa227-154">Registers whether a window accepts dropped files.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-155"><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragfinish"><strong>DragFinish</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-155"><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragfinish"><strong>DragFinish</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-156">釋放系統組態用來將檔案名傳送至應用程式的記憶體。</span><span class="sxs-lookup"><span data-stu-id="aa227-156">Releases memory that the system allocated for use in transferring file names to the application.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-157"><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea"><strong>DragQueryFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-157"><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea"><strong>DragQueryFile</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-158">抓取成功拖放作業所產生之已卸載檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa227-158">Retrieves the names of dropped files that result from a successful drag-and-drop operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-159"><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint"><strong>DragQueryPoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-159"><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint"><strong>DragQueryPoint</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-160">在拖放作業期間卸載檔案時，捕獲滑鼠指標的位置。</span><span class="sxs-lookup"><span data-stu-id="aa227-160">Retrieves the position of the mouse pointer at the time a file was dropped during a drag-and-drop operation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-161"><a href="/windows/desktop/api/shellapi/nf-shellapi-duplicateicon"><strong>DuplicateIcon</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-161"><a href="/windows/desktop/api/shellapi/nf-shellapi-duplicateicon"><strong>DuplicateIcon</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-162">建立重複的指定圖示。</span><span class="sxs-lookup"><span data-stu-id="aa227-162">Creates a duplicate of a specified icon.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-163"><a href="/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera"><strong>ExpandEnvironmentStringsForUser</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-163"><a href="/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera"><strong>ExpandEnvironmentStringsForUser</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-164">使用針對指定使用者所建立的環境區塊來展開來源字串。</span><span class="sxs-lookup"><span data-stu-id="aa227-164">Expands the source string by using the environment block established for the specified user.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-165"><a href="/windows/desktop/api/shellapi/nf-shellapi-extractassociatedicona"><strong>ExtractAssociatedIcon</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-165"><a href="/windows/desktop/api/shellapi/nf-shellapi-extractassociatedicona"><strong>ExtractAssociatedIcon</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-166">取得在檔案中儲存為資源之圖示的控制碼，或儲存在檔案相關聯的可執行檔中的圖示。</span><span class="sxs-lookup"><span data-stu-id="aa227-166">Gets a handle to an icon stored as a resource in a file or an icon stored in a file's associated executable file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-167"><a href="/windows/desktop/api/shellapi/nf-shellapi-extracticona"><strong>ExtractIcon</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-167"><a href="/windows/desktop/api/shellapi/nf-shellapi-extracticona"><strong>ExtractIcon</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-168">從指定的可執行檔、DLL 或圖示檔取得圖示的控制碼。</span><span class="sxs-lookup"><span data-stu-id="aa227-168">Gets a handle to an icon from the specified executable file, DLL, or icon file.</span></span> <br/> <span data-ttu-id="aa227-169">若要取出大型或小型圖示的控制碼陣列，請使用 <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>ExtractIconEx</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="aa227-169">To retrieve an array of handles to large or small icons, use the <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>ExtractIconEx</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-170"><a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>ExtractIconEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-170"><a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>ExtractIconEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-171"><a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>ExtractIconEx</strong></a>函式會針對從指定的可執行檔、DLL 或圖示檔解壓縮的大型或小型圖示，建立控點的陣列。</span><span class="sxs-lookup"><span data-stu-id="aa227-171">The <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>ExtractIconEx</strong></a> function creates an array of handles to large or small icons extracted from the specified executable file, DLL, or icon file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-172"><a href="fileiconinit.md"><strong>FileIconInit</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-172"><a href="fileiconinit.md"><strong>FileIconInit</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-173">初始化或重新初始化系統映射清單。</span><span class="sxs-lookup"><span data-stu-id="aa227-173">Initializes or reinitializes the system image list.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-174"><a href="/windows/desktop/api/Shellapi/nf-shellapi-findexecutablea"><strong>FindExecutable</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-174"><a href="/windows/desktop/api/Shellapi/nf-shellapi-findexecutablea"><strong>FindExecutable</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-175">抓取與特定檔檔案相關聯的可執行檔 ( .exe) 檔案的名稱和控制碼。</span><span class="sxs-lookup"><span data-stu-id="aa227-175">Retrieves the name of and handle to the executable (.exe) file associated with a specific document file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-176"><a href="/windows/desktop/api/syncmgr/nf-syncmgr-freeconfirmconflictitem"><strong>FreeConfirmConflictItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-176"><a href="/windows/desktop/api/syncmgr/nf-syncmgr-freeconfirmconflictitem"><strong>FreeConfirmConflictItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-177">釋出已配置給 <a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_item"><strong>CONFIRM_CONFLICT_ITEM</strong></a> 結構的資源。</span><span class="sxs-lookup"><span data-stu-id="aa227-177">Frees the resources that have been allocated for a <a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_item"><strong>CONFIRM_CONFLICT_ITEM</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-178"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarray"><strong>FreeIDListArray</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-178"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarray"><strong>FreeIDListArray</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-179">釋出項目識別碼清單的指標所使用的記憶體 (PIDL) 清單陣列。</span><span class="sxs-lookup"><span data-stu-id="aa227-179">Frees the memory used by an pointer to an item identifier list (PIDL) list array.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-180"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarraychild"><strong>FreeIDListArrayChild</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-180"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarraychild"><strong>FreeIDListArrayChild</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-181">釋放子專案 Id 之指標陣列的記憶體空間。</span><span class="sxs-lookup"><span data-stu-id="aa227-181">Releases the memory space for the array of pointers to child item IDs.</span></span> <span data-ttu-id="aa227-182">這會釋放陣列內的 PITEMID_CHILDs 以及陣列本身。</span><span class="sxs-lookup"><span data-stu-id="aa227-182">This releases both the PITEMID_CHILDs within the array and the array itself.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-183"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarrayfull"><strong>FreeIDListArrayFull</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-183"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarrayfull"><strong>FreeIDListArrayFull</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-184">釋放 PIDL 陣列的記憶體空間。</span><span class="sxs-lookup"><span data-stu-id="aa227-184">Releases the memory space for the PIDL array.</span></span> <span data-ttu-id="aa227-185">這會釋放陣列內的 PIDLIST_ABSOLUTEs 以及陣列本身。</span><span class="sxs-lookup"><span data-stu-id="aa227-185">This releases both the PIDLIST_ABSOLUTEs within the array and the array itself.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-186"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeknownfolderdefinitionfields"><strong>FreeKnownFolderDefinitionFields</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-186"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeknownfolderdefinitionfields"><strong>FreeKnownFolderDefinitionFields</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-187">釋放 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getfolderdefinition"><strong>IKnownFolder：： GetFolderDefinition</strong></a>結果中的配置欄位。</span><span class="sxs-lookup"><span data-stu-id="aa227-187">Frees the allocated fields in the result from <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getfolderdefinition"><strong>IKnownFolder::GetFolderDefinition</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-188"><a href="freemrulist.md"><strong>FreeMRUList</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-188"><a href="freemrulist.md"><strong>FreeMRUList</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-189">釋出與 MRU 清單相關聯的控制碼，並將快取的資料寫入登錄中。</span><span class="sxs-lookup"><span data-stu-id="aa227-189">Frees the handle associated with the MRU list and writes cached data to the registry.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-190"><a href="/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya"><strong>GetAllUsersProfileDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-190"><a href="/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya"><strong>GetAllUsersProfileDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-191">抓取目錄根目錄的路徑，其中包含所有使用者共用的程式資料。</span><span class="sxs-lookup"><span data-stu-id="aa227-191">Retrieves the path to the root of the directory that contains program data shared by all users.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-192"><a href="/windows/desktop/api/Userenv/nf-userenv-getappcontainerfolderpath"><strong>GetAppContainerFolderPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-192"><a href="/windows/desktop/api/Userenv/nf-userenv-getappcontainerfolderpath"><strong>GetAppContainerFolderPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-193">取得指定之應用程式容器的本機應用程式資料檔案夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="aa227-193">Gets the path of the local app data folder for the specified app container.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-194"><a href="/windows/desktop/api/Userenv/nf-userenv-getappcontainerregistrylocation"><strong>GetAppContainerRegistryLocation</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-194"><a href="/windows/desktop/api/Userenv/nf-userenv-getappcontainerregistrylocation"><strong>GetAppContainerRegistryLocation</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-195">取得與應用程式容器相關聯之登錄儲存體的位置。</span><span class="sxs-lookup"><span data-stu-id="aa227-195">Gets the location of the registry storage associated with an app container.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-196"><a href="/previous-versions/windows/desktop/legacy/jj152005(v=vs.85)"><strong>GetContractDelegateWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-196"><a href="/previous-versions/windows/desktop/legacy/jj152005(v=vs.85)"><strong>GetContractDelegateWindow</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-197">抓取已設定為應用程式主要前景視窗之委派的視窗，目的是要讓委派視窗與應用程式的合約產生關聯。</span><span class="sxs-lookup"><span data-stu-id="aa227-197">Retrieves a window that has been set as a delegate for an app's primary foreground window for the purpose of associating the delegate window with the app's contracts.</span></span> <span data-ttu-id="aa227-198">如果您是在原生 c + + 中撰寫 Windows Store 應用程式的開發人員，請使用此函數。</span><span class="sxs-lookup"><span data-stu-id="aa227-198">Use this function if you are a developer writing a Windows Store app in native C++.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-199"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-getcurrentprocessexplicitappusermodelid"><strong>GetCurrentProcessExplicitAppUserModelID</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-199"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-getcurrentprocessexplicitappusermodelid"><strong>GetCurrentProcessExplicitAppUserModelID</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-200">抓取目前進程的應用程式定義、明確應用程式使用者模型識別碼 (AppUserModelID) 。</span><span class="sxs-lookup"><span data-stu-id="aa227-200">Retrieves the application-defined, explicit Application User Model ID (AppUserModelID) for the current process.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-201"><a href="/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya"><strong>GetDefaultUserProfileDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-201"><a href="/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya"><strong>GetDefaultUserProfileDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-202">抓取預設使用者設定檔之根目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="aa227-202">Retrieves the path to the root of the default user's profile.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-203"><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiforshelluicomponent"><strong>GetDpiForShellUiComponent</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-203"><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiforshelluicomponent"><strong>GetDpiForShellUiComponent</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-204">根據目前的縮放比例和<a href="/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness"><strong>PROCESS_DPI_AWARENESS</strong></a>，抓取<a href="/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-shell_ui_component"><strong>SHELL_UI_COMPONENT</strong></a>所佔用的每英寸 (DPI) 的點。</span><span class="sxs-lookup"><span data-stu-id="aa227-204">Retrieves the dots per inch (dpi) occupied by a <a href="/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-shell_ui_component"><strong>SHELL_UI_COMPONENT</strong></a> based on the current scale factor and <a href="/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness"><strong>PROCESS_DPI_AWARENESS</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-205"><a href="/windows/desktop/api/Winuser/nf-winuser-getmenucontexthelpid"><strong>GetMenuCoNtextHelpId</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-205"><a href="/windows/desktop/api/Winuser/nf-winuser-getmenucontexthelpid"><strong>GetMenuContextHelpId</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-206">抓取與指定功能表相關聯的說明內容識別碼。</span><span class="sxs-lookup"><span data-stu-id="aa227-206">Retrieves the Help context identifier associated with the specified menu.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-207"><a href="/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya"><strong>GetProfilesDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-207"><a href="/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya"><strong>GetProfilesDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-208">抓取儲存使用者設定檔之根目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="aa227-208">Retrieves the path to the root directory where user profiles are stored.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-209"><a href="/windows/desktop/api/Userenv/nf-userenv-getprofiletype"><strong>GetProfileType</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-209"><a href="/windows/desktop/api/Userenv/nf-userenv-getprofiletype"><strong>GetProfileType</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-210">抓取為目前使用者載入的配置檔案類型。</span><span class="sxs-lookup"><span data-stu-id="aa227-210">Retrieves the type of profile loaded for the current user.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-211"><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorfordevice"><strong>GetScaleFactorForDevice</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-211"><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorfordevice"><strong>GetScaleFactorForDevice</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-212">取得顯示裝置的慣用縮放比例。</span><span class="sxs-lookup"><span data-stu-id="aa227-212">Gets the preferred scale factor for a display device.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-213"><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorformonitor"><strong>GetScaleFactorForMonitor</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-213"><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorformonitor"><strong>GetScaleFactorForMonitor</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-214">取得特定監視器的縮放比例。</span><span class="sxs-lookup"><span data-stu-id="aa227-214">Gets the scale factor of a specific monitor.</span></span> <span data-ttu-id="aa227-215">此函數會取代 <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorfordevice"><strong>GetScaleFactorForDevice</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="aa227-215">This function replaces <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorfordevice"><strong>GetScaleFactorForDevice</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-216"><a href="/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya"><strong>GetUserProfileDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-216"><a href="/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya"><strong>GetUserProfileDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-217">抓取指定使用者設定檔之根目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="aa227-217">Retrieves the path to the root directory of the specified user's profile.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-218"><a href="/windows/desktop/api/Winuser/nf-winuser-getwindowcontexthelpid"><strong>GetWindowCoNtextHelpId</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-218"><a href="/windows/desktop/api/Winuser/nf-winuser-getwindowcontexthelpid"><strong>GetWindowContextHelpId</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-219">抓取與指定視窗相關聯的說明內容識別碼（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="aa227-219">Retrieves the Help context identifier, if any, associated with the specified window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-220"><a href="/windows/desktop/api/Commctrl/nf-commctrl-getwindowsubclass"><strong>GetWindowSubclass</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-220"><a href="/windows/desktop/api/Commctrl/nf-commctrl-getwindowsubclass"><strong>GetWindowSubclass</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-221">抓取所指定視窗子類別回呼的參考資料。</span><span class="sxs-lookup"><span data-stu-id="aa227-221">Retrieves the reference data for the specified window subclass callback.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-222"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-idlistcontainerisconsistent"><strong>IDListContainerIsConsistent</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-222"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-idlistcontainerisconsistent"><strong>IDListContainerIsConsistent</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-223">驗證 Idlist.txt 的容器結構是否有效。</span><span class="sxs-lookup"><span data-stu-id="aa227-223">Verifies that the container structure of an IDList is valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-224"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilappendid"><strong>ILAppendID</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-224"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilappendid"><strong>ILAppendID</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-225">將 <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> 結構附加或附加至 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構。</span><span class="sxs-lookup"><span data-stu-id="aa227-225">Appends or prepends an <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> structure to an <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-226"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclone"><strong>ILClone</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-226"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclone"><strong>ILClone</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-227">複製 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構。</span><span class="sxs-lookup"><span data-stu-id="aa227-227">Clones an <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-228"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonechild"><strong>ILCloneChild</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-228"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonechild"><strong>ILCloneChild</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-229">複製子 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構。</span><span class="sxs-lookup"><span data-stu-id="aa227-229">Clones a child <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-230"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonefirst"><strong>ILCloneFirst</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-230"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonefirst"><strong>ILCloneFirst</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-231">複製<a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a>結構中的第一個<a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a>結構。</span><span class="sxs-lookup"><span data-stu-id="aa227-231">Clones the first <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> structure in an <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-232"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonefull"><strong>ILCloneFull</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-232"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonefull"><strong>ILCloneFull</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-233">複製完整或絕對的 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構。</span><span class="sxs-lookup"><span data-stu-id="aa227-233">Clones a full, or absolute, <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-234"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilcombine"><strong>ILCombine</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-234"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilcombine"><strong>ILCombine</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-235">結合兩個 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構。</span><span class="sxs-lookup"><span data-stu-id="aa227-235">Combines two <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structures.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-236"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilcreatefrompath"><strong>ILCreateFromPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-236"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilcreatefrompath"><strong>ILCreateFromPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-237">傳回與指定檔案路徑相關聯的 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構。</span><span class="sxs-lookup"><span data-stu-id="aa227-237">Returns the <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structure associated with a specified file path.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-238"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfindchild"><strong>ILFindChild</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-238"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfindchild"><strong>ILFindChild</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-239">判斷指定的 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構是否為另一個 <strong>ITEMIDLIST</strong> 結構的子系。</span><span class="sxs-lookup"><span data-stu-id="aa227-239">Determines whether a specified <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structure is the child of another <strong>ITEMIDLIST</strong> structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-240"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfindlastid"><strong>ILFindLastID</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-240"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfindlastid"><strong>ILFindLastID</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-241">傳回<a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a>結構中最後一個<a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a>結構的指標。</span><span class="sxs-lookup"><span data-stu-id="aa227-241">Returns a pointer to the last <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> structure in an <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-242"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree"><strong>ILFree</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-242"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree"><strong>ILFree</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-243">釋放由 Shell 配置的 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構。</span><span class="sxs-lookup"><span data-stu-id="aa227-243">Frees an <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structure allocated by the Shell.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-244"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilgetnext"><strong>ILGetNext</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-244"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilgetnext"><strong>ILGetNext</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-245">捕獲<a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a>結構中的下一個<a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a>結構。</span><span class="sxs-lookup"><span data-stu-id="aa227-245">Retrieves the next <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> structure in an <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-246"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilgetsize"><strong>ILGetSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-246"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilgetsize"><strong>ILGetSize</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-247">傳回 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="aa227-247">Returns the size, in bytes, of an <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-248"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisaligned"><strong>ILIsAligned</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-248"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisaligned"><strong>ILIsAligned</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-249">驗證常數 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 是否對齊指標界限，也就是32位架構上的 <strong>DWORD</strong> 和64位架構上的 <strong>QWORD</strong> 。</span><span class="sxs-lookup"><span data-stu-id="aa227-249">Verifies whether a constant <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> is aligned on a pointer boundary, which is a <strong>DWORD</strong> on 32-bit architectures and a <strong>QWORD</strong> on 64-bit architectures.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-250"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilischild"><strong>ILIsChild</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-250"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilischild"><strong>ILIsChild</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-251">驗證 PIDL 是否為子 PIDL，也就是只有一個 <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a>的 PIDL。</span><span class="sxs-lookup"><span data-stu-id="aa227-251">Verifies whether a PIDL is a child PIDL, which is a PIDL with exactly one <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-252"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisempty"><strong>ILIsEmpty</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-252"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisempty"><strong>ILIsEmpty</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-253">確認 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構是否為空白。</span><span class="sxs-lookup"><span data-stu-id="aa227-253">Verifies whether an <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structure is empty.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-254"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisequal"><strong>ILIsEqual</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-254"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisequal"><strong>ILIsEqual</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-255">測試兩個 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構是否相等於二進位比較。</span><span class="sxs-lookup"><span data-stu-id="aa227-255">Tests whether two <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structures are equal in a binary comparison.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-256"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisparent"><strong>ILIsParent</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-256"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisparent"><strong>ILIsParent</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-257">測試 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構是否為另一個 <strong>ITEMIDLIST</strong> 結構的父代。</span><span class="sxs-lookup"><span data-stu-id="aa227-257">Tests whether an <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structure is the parent of another <strong>ITEMIDLIST</strong> structure.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-258"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilnext"><strong>ILNext (PCUIDLIST_RELATIVE) </strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-258"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilnext"><strong>ILNext(PCUIDLIST_RELATIVE)</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-259">捕獲<a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a>結構中的下一個<a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a>結構。</span><span class="sxs-lookup"><span data-stu-id="aa227-259">Retrieves the next <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> structure in an <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-260"><a href="/previous-versions/windows/desktop/legacy/bb776455(v=vs.85)"><strong>ILNext (PUIDLIST_RELATIVE) </strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-260"><a href="/previous-versions/windows/desktop/legacy/bb776455(v=vs.85)"><strong>ILNext(PUIDLIST_RELATIVE)</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-261">捕獲<a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a>結構中的下一個<a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a>結構。</span><span class="sxs-lookup"><span data-stu-id="aa227-261">Retrieves the next <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> structure in an <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-262"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilremovelastid"><strong>ILRemoveLastID</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-262"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilremovelastid"><strong>ILRemoveLastID</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-263">從<a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a>結構移除最後一個<a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a>結構。</span><span class="sxs-lookup"><span data-stu-id="aa227-263">Removes the last <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> structure from an <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-264"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilsavetostream"><strong>ILSaveToStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-264"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilsavetostream"><strong>ILSaveToStream</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-265">將 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構儲存至資料流程。</span><span class="sxs-lookup"><span data-stu-id="aa227-265">Saves an <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structure to a stream.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-266"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilskip"><strong>ILSkip (PCUIDLIST_RELATIVE，UINT) </strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-266"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilskip"><strong>ILSkip(PCUIDLIST_RELATIVE, UINT)</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-267">略過常數、未對齊、相對 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構中指定的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="aa227-267">Skips a given number of bytes in a constant, unaligned, relative <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-268"><a href="/previous-versions/windows/desktop/legacy/bb776459(v=vs.85)"><strong>ILSkip (PUIDLIST_RELATIVE，UINT) </strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-268"><a href="/previous-versions/windows/desktop/legacy/bb776459(v=vs.85)"><strong>ILSkip(PUIDLIST_RELATIVE, UINT)</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-269">略過未對齊、相對 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構中指定的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="aa227-269">Skips a given number of bytes in an unaligned, relative <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-270"><a href="/windows/desktop/api/Intshcut/nf-intshcut-inetisoffline"><strong>InetIsOffline</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-270"><a href="/windows/desktop/api/Intshcut/nf-intshcut-inetisoffline"><strong>InetIsOffline</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-271">判斷系統是否已連線到網際網路。</span><span class="sxs-lookup"><span data-stu-id="aa227-271">Determines whether the system is connected to the Internet.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-272"><a href="/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol"><strong>InitNetworkAddressControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-272"><a href="/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol"><strong>InitNetworkAddressControl</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-273">初始化網路位址控制視窗類別。</span><span class="sxs-lookup"><span data-stu-id="aa227-273">Initializes the network address control window class.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-274"><a href="/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea"><strong>LoadUserProfile</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-274"><a href="/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea"><strong>LoadUserProfile</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-275">載入指定的使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="aa227-275">Loads the specified user's profile.</span></span> <span data-ttu-id="aa227-276">設定檔可以是 <a href="local-user-profiles.md">本機使用者配置</a> 檔或 <a href="roaming-user-profiles.md">漫遊使用者設定檔</a>。</span><span class="sxs-lookup"><span data-stu-id="aa227-276">The profile can be a <a href="local-user-profiles.md">local user profile</a> or a <a href="roaming-user-profiles.md">roaming user profile</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-277"><a href="/windows/desktop/api/Intshcut/nf-intshcut-mimeassociationdialoga"><strong>MIMEAssociationDialog</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-277"><a href="/windows/desktop/api/Intshcut/nf-intshcut-mimeassociationdialoga"><strong>MIMEAssociationDialog</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-278">執行 [未註冊的 MIME 內容類型] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="aa227-278">Runs the unregistered MIME content type dialog box.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="aa227-279">Windows XP Service Pack 2 (SP2) 或更新版本：不再支援此功能。</span><span class="sxs-lookup"><span data-stu-id="aa227-279">Windows XP Service Pack 2 (SP2) or later: This function is no longer supported.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-280"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathmakeuniquename"><strong>PathMakeUniqueName</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-280"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathmakeuniquename"><strong>PathMakeUniqueName</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-281">從範本建立唯一的路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="aa227-281">Creates a unique path name from a template.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-282"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathyetanothermakeuniquename"><strong>PathYetAnotherMakeUniqueName</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-282"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathyetanothermakeuniquename"><strong>PathYetAnotherMakeUniqueName</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-283">根據現有的檔案名建立唯一的檔案名。</span><span class="sxs-lookup"><span data-stu-id="aa227-283">Creates a unique filename based on an existing filename.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-284"><a href="/windows/desktop/api/appnotify/nf-appnotify-registerappstatechangenotification"><strong>RegisterAppStateChangeNotification</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-284"><a href="/windows/desktop/api/appnotify/nf-appnotify-registerappstatechangenotification"><strong>RegisterAppStateChangeNotification</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-285">可讓應用程式註冊回呼函式，以通知其程式庫即將進入或離開暫停狀態。</span><span class="sxs-lookup"><span data-stu-id="aa227-285">Enables an app to register a callback function through which it can be notified that its library is going into or coming out of a suspended state.</span></span> <span data-ttu-id="aa227-286">應用程式可以使用此資訊來執行任何必要的作業，例如在該時間點執行的保留狀態。</span><span class="sxs-lookup"><span data-stu-id="aa227-286">The app can use this information to perform any necessary operations, such as preserving state, that should be performed at that point.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-287"><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-registerdialogclasses"><strong>RegisterDialogClasses</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-287"><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-registerdialogclasses"><strong>RegisterDialogClasses</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-288">註冊螢幕保護裝置程式的設定對話方塊所需的任何非標準視窗類別。</span><span class="sxs-lookup"><span data-stu-id="aa227-288">Registers any nonstandard window classes required by a screen saver's configuration dialog box.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-289"><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>RegisterScaleChangeEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-289"><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>RegisterScaleChangeEvent</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-290">註冊當調整規模可能變更時所觸發的事件。</span><span class="sxs-lookup"><span data-stu-id="aa227-290">Registers for an event that is triggered when the scale has possibly changed.</span></span> <span data-ttu-id="aa227-291">此函數會取代 <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangenotifications"><strong>RegisterScaleChangeNotifications</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="aa227-291">This function replaces <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangenotifications"><strong>RegisterScaleChangeNotifications</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-292"><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangenotifications"><strong>RegisterScaleChangeNotifications</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-292"><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangenotifications"><strong>RegisterScaleChangeNotifications</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-293">註冊視窗，以在調整資訊變更時接收回呼。</span><span class="sxs-lookup"><span data-stu-id="aa227-293">Registers a window to receive callbacks when scaling information changes.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="aa227-294">Windows 8.1 不支援這個函數。</span><span class="sxs-lookup"><span data-stu-id="aa227-294">This function is not supported as of Windows 8.1.</span></span> <span data-ttu-id="aa227-295">請改用 <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>RegisterScaleChangeEvent</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="aa227-295">Use <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>RegisterScaleChangeEvent</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-296"><a href="/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass"><strong>RemoveWindowSubclass</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-296"><a href="/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass"><strong>RemoveWindowSubclass</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-297">從視窗中移除子類別回呼。</span><span class="sxs-lookup"><span data-stu-id="aa227-297">Removes a subclass callback from a window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-298"><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-revokescalechangenotifications"><strong>RevokeScaleChangeNotifications</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-298"><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-revokescalechangenotifications"><strong>RevokeScaleChangeNotifications</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-299">撤銷視窗的註冊，防止它在調整資訊變更時接收回呼。</span><span class="sxs-lookup"><span data-stu-id="aa227-299">Revokes the registration of a window, preventing it from receiving callbacks when scaling information changes.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="aa227-300">Windows 8.1 不支援這個函數。</span><span class="sxs-lookup"><span data-stu-id="aa227-300">This function is not supported as of Windows 8.1.</span></span> <span data-ttu-id="aa227-301">請改用 <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-unregisterscalechangeevent"><strong>UnregisterScaleChangeEvent</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="aa227-301">Use <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-unregisterscalechangeevent"><strong>UnregisterScaleChangeEvent</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-302"><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-screensaverconfiguredialog"><strong>ScreenSaverConfigureDialog</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-302"><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-screensaverconfiguredialog"><strong>ScreenSaverConfigureDialog</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-303">接收傳送至螢幕保護裝置程式之 [設定] 對話方塊的訊息。</span><span class="sxs-lookup"><span data-stu-id="aa227-303">Receives messages sent to a screen saver's configuration dialog box.</span></span> <span data-ttu-id="aa227-304">允許使用者設定的螢幕保護裝置必須定義此功能。</span><span class="sxs-lookup"><span data-stu-id="aa227-304">A screen saver that allows user configuration must define this function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-305"><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-screensaverproc"><strong>ScreenSaverProc</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-305"><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-screensaverproc"><strong>ScreenSaverProc</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-306">接收傳送到指定螢幕保護裝置視窗的訊息。</span><span class="sxs-lookup"><span data-stu-id="aa227-306">Receives messages sent to the specified screen saver window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-307"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcontractdelegatewindow"><strong>SetContractDelegateWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-307"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcontractdelegatewindow"><strong>SetContractDelegateWindow</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-308">將主要前景視窗以外的應用程式視窗與應用程式的合約產生關聯。</span><span class="sxs-lookup"><span data-stu-id="aa227-308">Associates an app window other than the primary foreground window with an app's contracts.</span></span> <span data-ttu-id="aa227-309">如果您是在原生 c + + 中撰寫 Windows Store 應用程式的開發人員，請使用此函數。</span><span class="sxs-lookup"><span data-stu-id="aa227-309">Use this function if you are a developer writing a Windows Store app in native C++.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-310"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid"><strong>SetCurrentProcessExplicitAppUserModelID</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-310"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid"><strong>SetCurrentProcessExplicitAppUserModelID</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-311">指定唯一的應用程式定義 AppUserModelID，識別工作列目前的進程。</span><span class="sxs-lookup"><span data-stu-id="aa227-311">Specifies a unique application-defined AppUserModelID that identifies the current process to the taskbar.</span></span> <span data-ttu-id="aa227-312">此識別碼可讓應用程式在單一工作列按鈕下將其相關聯的進程和視窗分組。</span><span class="sxs-lookup"><span data-stu-id="aa227-312">This identifier allows an application to group its associated processes and windows under a single taskbar button.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-313"><a href="/windows/desktop/api/Winuser/nf-winuser-setmenucontexthelpid"><strong>SetMenuCoNtextHelpId</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-313"><a href="/windows/desktop/api/Winuser/nf-winuser-setmenucontexthelpid"><strong>SetMenuContextHelpId</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-314">讓說明內容識別碼與功能表產生關聯。</span><span class="sxs-lookup"><span data-stu-id="aa227-314">Associates a Help context identifier with a menu.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-315"><a href="/windows/desktop/api/Winuser/nf-winuser-setwindowcontexthelpid"><strong>SetWindowCoNtextHelpId</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-315"><a href="/windows/desktop/api/Winuser/nf-winuser-setwindowcontexthelpid"><strong>SetWindowContextHelpId</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-316">將說明內容識別碼與指定的視窗產生關聯。</span><span class="sxs-lookup"><span data-stu-id="aa227-316">Associates a Help context identifier with the specified window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-317"><a href="/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass"><strong>SetWindowSubclass</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-317"><a href="/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass"><strong>SetWindowSubclass</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-318">安裝或更新視窗子類別回呼。</span><span class="sxs-lookup"><span data-stu-id="aa227-318">Installs or updates a window subclass callback.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-319"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-319"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-320">通知系統已存取專案，目的是要追蹤最近和最常使用的專案。</span><span class="sxs-lookup"><span data-stu-id="aa227-320">Notifies the system that an item has been accessed, for the purposes of tracking those items used most recently and most frequently.</span></span> <span data-ttu-id="aa227-321">此函式也可用來清除所有使用方式資料。</span><span class="sxs-lookup"><span data-stu-id="aa227-321">This function can also be used to clear all usage data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-322"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage"><strong>SHAppBarMessage</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-322"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage"><strong>SHAppBarMessage</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-323">將 appbar 訊息傳送至系統。</span><span class="sxs-lookup"><span data-stu-id="aa227-323">Sends an appbar message to the system.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-324"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shassocenumhandlers"><strong>SHAssocEnumHandlers</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-324"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shassocenumhandlers"><strong>SHAssocEnumHandlers</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-325">傳回指定的一組副檔名處理常式的列舉物件。</span><span class="sxs-lookup"><span data-stu-id="aa227-325">Returns an enumeration object for a specified set of file name extension handlers.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-326"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shassocenumhandlersforprotocolbyapplication"><strong>SHAssocEnumHandlersForProtocolByApplication</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-326"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shassocenumhandlersforprotocolbyapplication"><strong>SHAssocEnumHandlersForProtocolByApplication</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-327">取得列舉介面，這個介面可讓您存取與指定通訊協定相關聯的處理常式。</span><span class="sxs-lookup"><span data-stu-id="aa227-327">Gets an enumeration interface that provides access to handlers associated with a given protocol.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-328"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparent"><strong>SHBindToFolderIDListParent</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-328"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparent"><strong>SHBindToFolderIDListParent</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-329">指定以資料夾格式指定的 Shell 命名空間專案，以及相對於該資料夾的專案識別碼清單，此函式會系結至命名空間專案的父系，並選擇性地將指標傳回至專案識別碼清單的最後一個元件。</span><span class="sxs-lookup"><span data-stu-id="aa227-329">Given a Shell namespace item specified in the form of a folder, and an item identifier list relative to that folder, this function binds to the parent of the namespace item and optionally returns a pointer to the final component of the item identifier list.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-330"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparentex"><strong>SHBindToFolderIDListParentEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-330"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparentex"><strong>SHBindToFolderIDListParentEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-331">藉由允許呼叫端指定系結內容來擴充 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparent"><strong>SHBindToFolderIDListParent</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="aa227-331">Extends the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparent"><strong>SHBindToFolderIDListParent</strong></a> function by allowing the caller to specify a bind context.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-332"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoobject"><strong>SHBindToObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-332"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoobject"><strong>SHBindToObject</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-333">使用 Shell 命名空間 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder：： BindToObject</strong></a> 方法，來抓取並系結至指定的物件。</span><span class="sxs-lookup"><span data-stu-id="aa227-333">Retrieves and binds to a specified object by using the Shell namespace <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a> method.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-334"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent"><strong>SHBindToParent</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-334"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent"><strong>SHBindToParent</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-335">取得完整專案識別碼清單的指標 (PIDL) ，並傳回父物件上的指定介面指標。</span><span class="sxs-lookup"><span data-stu-id="aa227-335">Takes a pointer to a fully qualified item identifier list (PIDL), and returns a specified interface pointer on the parent object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-336"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera"><strong>SHBrowseForFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-336"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera"><strong>SHBrowseForFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-337">顯示可讓使用者選取 Shell 資料夾的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="aa227-337">Displays a dialog box that enables the user to select a Shell folder.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-338"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotification_lock"><strong>SHChangeNotification_Lock</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-338"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotification_lock"><strong>SHChangeNotification_Lock</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-339">鎖定與 Shell 變更通知事件相關聯的共用記憶體。</span><span class="sxs-lookup"><span data-stu-id="aa227-339">Locks the shared memory associated with a Shell change notification event.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-340"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotification_unlock"><strong>SHChangeNotification_Unlock</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-340"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotification_unlock"><strong>SHChangeNotification_Unlock</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-341">將變更通知的共用記憶體解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="aa227-341">Unlocks shared memory for a change notification.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-342"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify"><strong>SHChangeNotify</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-342"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify"><strong>SHChangeNotify</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-343">通知系統已執行應用程式的事件。</span><span class="sxs-lookup"><span data-stu-id="aa227-343">Notifies the system of an event that an application has performed.</span></span> <span data-ttu-id="aa227-344">如果應用程式執行的動作可能會影響 Shell，則應該使用此函式。</span><span class="sxs-lookup"><span data-stu-id="aa227-344">An application should use this function if it performs an action that may affect the Shell.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-345"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyderegister"><strong>SHChangeNotifyDeregister</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-345"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyderegister"><strong>SHChangeNotifyDeregister</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-346">從接收 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify"><strong>SHChangeNotify</strong></a> 訊息中取消註冊用戶端的視窗進程。</span><span class="sxs-lookup"><span data-stu-id="aa227-346">Unregisters the client's window process from receiving <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify"><strong>SHChangeNotify</strong></a> messages.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-347"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister"><strong>SHChangeNotifyRegister</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-347"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister"><strong>SHChangeNotifyRegister</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-348">註冊視窗，以從檔案系統或 Shell 接收通知（如果檔案系統支援通知）。</span><span class="sxs-lookup"><span data-stu-id="aa227-348">Registers a window to receive notifications from the file system or Shell, if the file system supports notifications.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-349"><a href="/windows/desktop/api/Shlobj/nf-shlobj-shchangenotifyregisterthread"><strong>SHChangeNotifyRegisterThread</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-349"><a href="/windows/desktop/api/Shlobj/nf-shlobj-shchangenotifyregisterthread"><strong>SHChangeNotifyRegisterThread</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-350">啟用執行緒的非同步登錄和取消註冊。</span><span class="sxs-lookup"><span data-stu-id="aa227-350">Enables asynchronous register and deregister of a thread.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-351"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateassociationregistration"><strong>SHCreateAssociationRegistration</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-351"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateassociationregistration"><strong>SHCreateAssociationRegistration</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-352">根據 Windows 所提供介面的內建執行，建立 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>IApplicationAssociationRegistration</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="aa227-352">Creates an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>IApplicationAssociationRegistration</strong></a> object based on the stock implementation of the interface provided by Windows.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-353"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedataobject"><strong>SHCreateDataObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-353"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedataobject"><strong>SHCreateDataObject</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-354">在父資料夾中建立資料物件。</span><span class="sxs-lookup"><span data-stu-id="aa227-354">Creates a data object in a parent folder.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-355"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>SHCreateDefaultCoNtextMenu</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-355"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>SHCreateDefaultContextMenu</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-356">建立物件，這個物件表示 Shell 的預設內容功能表執行。</span><span class="sxs-lookup"><span data-stu-id="aa227-356">Creates an object that represents the Shell's default context menu implementation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-357"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreatedefaultextracticon"><strong>SHCreateDefaultExtractIcon</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-357"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreatedefaultextracticon"><strong>SHCreateDefaultExtractIcon</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-358">建立標準圖示解壓縮解壓縮，可透過 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultextracticoninit"><strong>IDefaultExtractIconInit</strong></a> 介面進一步設定其預設值。</span><span class="sxs-lookup"><span data-stu-id="aa227-358">Creates a standard icon extractor, whose defaults can be further configured via the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultextracticoninit"><strong>IDefaultExtractIconInit</strong></a> interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-359"><a href="/windows/desktop/api/Shobjidl/nf-shobjidl-shcreatedefaultpropertiesop"><strong>SHCreateDefaultPropertiesOp</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-359"><a href="/windows/desktop/api/Shobjidl/nf-shobjidl-shcreatedefaultpropertiesop"><strong>SHCreateDefaultPropertiesOp</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-360">建立檔案作業，此作業會在 Shell 專案上設定尚未設定的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="aa227-360">Creates a file operation that sets the default properties on the Shell item that have not already been set.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-361"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromidlist"><strong>SHCreateItemFromIDList</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-361"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromidlist"><strong>SHCreateItemFromIDList</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-362">從 PIDL 建立並初始化 Shell 專案物件。</span><span class="sxs-lookup"><span data-stu-id="aa227-362">Creates and initializes a Shell item object from a PIDL.</span></span> <span data-ttu-id="aa227-363">產生的 shell 專案物件支援 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> 介面。</span><span class="sxs-lookup"><span data-stu-id="aa227-363">The resulting shell item object supports the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-364"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-364"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-365">從剖析名稱建立並初始化殼層項目物件。</span><span class="sxs-lookup"><span data-stu-id="aa227-365">Creates and initializes a Shell item object from a parsing name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-366"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromrelativename"><strong>SHCreateItemFromRelativeName</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-366"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromrelativename"><strong>SHCreateItemFromRelativeName</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-367">從相對剖析名稱建立並初始化 Shell 專案物件。</span><span class="sxs-lookup"><span data-stu-id="aa227-367">Creates and initializes a Shell item object from a relative parsing name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-368"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateiteminknownfolder"><strong>SHCreateItemInKnownFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-368"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateiteminknownfolder"><strong>SHCreateItemInKnownFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-369">針對存在於已知資料夾內的單一檔案，建立 Shell 專案物件。</span><span class="sxs-lookup"><span data-stu-id="aa227-369">Creates a Shell item object for a single file that exists inside a known folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-370"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemwithparent"><strong>SHCreateItemWithParent</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-370"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemwithparent"><strong>SHCreateItemWithParent</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-371">建立 Shell 專案，指定父資料夾和子專案識別碼。</span><span class="sxs-lookup"><span data-stu-id="aa227-371">Create a Shell item, given a parent folder and a child item ID.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-372"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-372"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-373">建立預設 Shell 資料夾 view 物件 (DefView) 的新實例。</span><span class="sxs-lookup"><span data-stu-id="aa227-373">Creates a new instance of the default Shell folder view object (DefView).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-374"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex"><strong>SHCreateShellFolderViewEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-374"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex"><strong>SHCreateShellFolderViewEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-375">建立預設 Shell 資料夾 view 物件的新實例。</span><span class="sxs-lookup"><span data-stu-id="aa227-375">Creates a new instance of the default Shell folder view object.</span></span> <span data-ttu-id="aa227-376">建議您使用 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a> ，而不是使用此函數。</span><span class="sxs-lookup"><span data-stu-id="aa227-376">It is recommended that you use <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a> rather than this function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-377"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellitem"><strong>SHCreateShellItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-377"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellitem"><strong>SHCreateShellItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-378">建立 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="aa227-378">Creates an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> object.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="aa227-379">建議您使用 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemwithparent"><strong>SHCreateItemWithParent</strong></a> 或 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromidlist"><strong>SHCreateItemFromIDList</strong></a> ，而不是使用此函數。</span><span class="sxs-lookup"><span data-stu-id="aa227-379">It is recommended that you use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemwithparent"><strong>SHCreateItemWithParent</strong></a> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromidlist"><strong>SHCreateItemFromIDList</strong></a> instead of this function.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-380"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarray"><strong>SHCreateShellItemArray</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-380"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarray"><strong>SHCreateShellItemArray</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-381">建立 Shell 專案陣列物件。</span><span class="sxs-lookup"><span data-stu-id="aa227-381">Creates a Shell item array object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-382"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject"><strong>SHCreateShellItemArrayFromDataObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-382"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject"><strong>SHCreateShellItemArrayFromDataObject</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-383">從資料物件建立 Shell 專案陣列物件。</span><span class="sxs-lookup"><span data-stu-id="aa227-383">Creates a Shell item array object from a data object.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-384"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromidlists"><strong>SHCreateShellItemArrayFromIDLists</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-384"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromidlists"><strong>SHCreateShellItemArrayFromIDLists</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-385">從 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構的清單建立 Shell 專案陣列物件。</span><span class="sxs-lookup"><span data-stu-id="aa227-385">Creates a Shell item array object from a list of <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structures.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-386"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromshellitem"><strong>SHCreateShellItemArrayFromShellItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-386"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromshellitem"><strong>SHCreateShellItemArrayFromShellItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-387">從單一 Shell 專案建立一個元素的陣列。</span><span class="sxs-lookup"><span data-stu-id="aa227-387">Creates an array of one element from a single Shell item.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-388"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shdefextracticona"><strong>SHDefExtractIcon</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-388"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shdefextracticona"><strong>SHDefExtractIcon</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-389">提供預設的處理常式，從檔案中解壓縮圖示。</span><span class="sxs-lookup"><span data-stu-id="aa227-389">Provides a default handler to extract an icon from a file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-390"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop"><strong>SHDoDragDrop</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-390"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop"><strong>SHDoDragDrop</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-391">執行拖放操作。</span><span class="sxs-lookup"><span data-stu-id="aa227-391">Executes a drag-and-drop operation.</span></span> <span data-ttu-id="aa227-392">支援視需要拖曳來源建立，以及拖曳影像。</span><span class="sxs-lookup"><span data-stu-id="aa227-392">Supports drag source creation on demand, as well as drag images.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-393"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona"><strong>Shell_NotifyIcon</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-393"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona"><strong>Shell_NotifyIcon</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-394">將訊息傳送至工作列的狀態區域。</span><span class="sxs-lookup"><span data-stu-id="aa227-394">Sends a message to the taskbar's status area.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-395"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect"><strong>Shell_NotifyIconGetRect</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-395"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect"><strong>Shell_NotifyIconGetRect</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-396">取得通知圖示周框的螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="aa227-396">Gets the screen coordinates of the bounding rectangle of a notification icon.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-397"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shellabouta"><strong>ShellAbout</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-397"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shellabouta"><strong>ShellAbout</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-398">顯示 [ <strong>ShellAbout</strong> ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="aa227-398">Displays a <strong>ShellAbout</strong> dialog box.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-399"><a href="shellddeinit.md"><strong>ShellDDEInit</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-399"><a href="shellddeinit.md"><strong>ShellDDEInit</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-400">在目前的進程中註冊 Shell 動態資料交換 (DDE) 服務，通知系統目前的進程希望裝載 DDE 物件。</span><span class="sxs-lookup"><span data-stu-id="aa227-400">Registers the Shell Dynamic Data Exchange (DDE) services in the current process, notifying the system that the current process wishes to host DDE objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-401"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea"><strong>ShellExecute</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-401"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea"><strong>ShellExecute</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-402">在指定的檔案上執行操作。</span><span class="sxs-lookup"><span data-stu-id="aa227-402">Performs an operation on a specified file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-403"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-403"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-404">在指定的檔案上執行操作。</span><span class="sxs-lookup"><span data-stu-id="aa227-404">Performs an operation on a specified file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-405"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shemptyrecyclebina"><strong>SHEmptyRecycleBin</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-405"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shemptyrecyclebina"><strong>SHEmptyRecycleBin</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-406">清空指定磁片磁碟機上的資源回收筒。</span><span class="sxs-lookup"><span data-stu-id="aa227-406">Empties the Recycle Bin on the specified drive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-407"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shenumerateunreadmailaccountsa"><strong>SHEnumerateUnreadMailAccounts</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-407"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shenumerateunreadmailaccountsa"><strong>SHEnumerateUnreadMailAccounts</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-408">列舉具有未讀取電子郵件的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="aa227-408">Enumerates the user accounts that have unread email.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-409"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shevaluatesystemcommandtemplate"><strong>SHEvaluateSystemCommandTemplate</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-409"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shevaluatesystemcommandtemplate"><strong>SHEvaluateSystemCommandTemplate</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-410">對 <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> 或 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea"><strong>ShellExecute</strong></a>的呼叫中所使用的參數強制執行嚴格驗證。</span><span class="sxs-lookup"><span data-stu-id="aa227-410">Enforces strict validation of parameters used in a call to <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> or <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea"><strong>ShellExecute</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-411"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-411"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-412">複製、移動、重新命名或刪除檔案系統物件。</span><span class="sxs-lookup"><span data-stu-id="aa227-412">Copies, moves, renames, or deletes a file system object.</span></span> <span data-ttu-id="aa227-413"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a>已在 Windows Vista 中取代此函式。</span><span class="sxs-lookup"><span data-stu-id="aa227-413">This function has been replaced in Windows Vista by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-414"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shfreenamemappings"><strong>SHFreeNameMappings</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-414"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shfreenamemappings"><strong>SHFreeNameMappings</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-415">釋放 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> 函式所取出的檔案名對應物件。</span><span class="sxs-lookup"><span data-stu-id="aa227-415">Frees a file name mapping object that was retrieved by the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-416"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdatafromidlista"><strong>SHGetDataFromIDList</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-416"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdatafromidlista"><strong>SHGetDataFromIDList</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-417">從相對識別碼清單抓取擴充屬性資料。</span><span class="sxs-lookup"><span data-stu-id="aa227-417">Retrieves extended property data from a relative identifier list.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-418"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder"><strong>SHGetDesktopFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-418"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder"><strong>SHGetDesktopFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-419">抓取桌面資料夾的 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> 介面，也就是 Shell 命名空間的根目錄。</span><span class="sxs-lookup"><span data-stu-id="aa227-419">Retrieves the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> interface for the desktop folder, which is the root of the Shell's namespace.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-420"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetdiskfreespaceexa"><strong>SHGetDiskFreeSpaceEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-420"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetdiskfreespaceexa"><strong>SHGetDiskFreeSpaceEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-421">捕獲磁片區的磁碟空間資訊。</span><span class="sxs-lookup"><span data-stu-id="aa227-421">Retrieves disk space information for a disk volume.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-422"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetdrivemedia"><strong>SHGetDriveMedia</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-422"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetdrivemedia"><strong>SHGetDriveMedia</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-423">傳回指定磁片磁碟機中的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="aa227-423">Returns the type of media that is in the given drive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-424"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetfileinfoa"><strong>SHGetFileInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-424"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetfileinfoa"><strong>SHGetFileInfo</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-425">抓取檔案系統中物件的相關資訊，例如檔案、資料夾、目錄或磁片磁碟機根目錄。</span><span class="sxs-lookup"><span data-stu-id="aa227-425">Retrieves information about an object in the file system, such as a file, folder, directory, or drive root.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-426"><a href="/previous-versions/windows/desktop/legacy/mt757093(v=vs.85)"><strong>SHGetFolderPathEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-426"><a href="/previous-versions/windows/desktop/legacy/mt757093(v=vs.85)"><strong>SHGetFolderPathEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-427">抓取資料夾的 <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a>所識別之已知資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="aa227-427">Retrieves the full path of a known folder identified by the folder's <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a>.</span></span> <span data-ttu-id="aa227-428">這可讓您設定字串緩衝區的初始大小，藉此擴充 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath"><strong>SHGetKnownFolderPath</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="aa227-428">This extends <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath"><strong>SHGetKnownFolderPath</strong></a> by allowing you to set the initial size of the string buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-429"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgeticonoverlayindexa"><strong>SHGetIconOverlayIndex</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-429"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgeticonoverlayindexa"><strong>SHGetIconOverlayIndex</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-430">傳回系統映射清單中覆迭圖示的索引。</span><span class="sxs-lookup"><span data-stu-id="aa227-430">Returns the index of the overlay icon in the system image list.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-431"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetidlistfromobject"><strong>SHGetIDListFromObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-431"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetidlistfromobject"><strong>SHGetIDListFromObject</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-432">抓取物件的 PIDL。</span><span class="sxs-lookup"><span data-stu-id="aa227-432">Retrieves the PIDL of an object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-433"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetimagelist"><strong>SHGetImageList</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-433"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetimagelist"><strong>SHGetImageList</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-434">抓取影像清單。</span><span class="sxs-lookup"><span data-stu-id="aa227-434">Retrieves an image list.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-435"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetinstanceexplorer"><strong>SHGetInstanceExplorer</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-435"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetinstanceexplorer"><strong>SHGetInstanceExplorer</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-436">抓取允許裝載 Shell 擴充和其他元件的介面，以防止其主機進程提前關閉。</span><span class="sxs-lookup"><span data-stu-id="aa227-436">Retrieves an interface that allows hosted Shell extensions and other components to prevent their host process from closing prematurely.</span></span> <span data-ttu-id="aa227-437">主機進程通常是 Windows 檔案總管或 Windows Internet Explorer，但其他應用程式也可以使用此功能。</span><span class="sxs-lookup"><span data-stu-id="aa227-437">The host process is typically Windows Explorer or Windows Internet Explorer, but this function can also be used by other applications.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-438"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromdataobject"><strong>SHGetItemFromDataObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-438"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromdataobject"><strong>SHGetItemFromDataObject</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-439">根據<a href="/windows/desktop/api/objidl/nn-objidl-idataobject"><strong>IDataObject</strong></a>指定的專案，建立<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>或相關的物件。</span><span class="sxs-lookup"><span data-stu-id="aa227-439">Creates an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> or related object based on an item specified by an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject"><strong>IDataObject</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-440"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromobject"><strong>SHGetItemFromObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-440"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromobject"><strong>SHGetItemFromObject</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-441">抓取物件的 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="aa227-441">Retrieves an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> for an object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-442"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist"><strong>SHGetKnownFolderIDList</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-442"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist"><strong>SHGetKnownFolderIDList</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-443">以 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構的形式抓取已知資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="aa227-443">Retrieves the path of a known folder as an <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-444"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderitem"><strong>SHGetKnownFolderItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-444"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderitem"><strong>SHGetKnownFolderItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-445">抓取代表已知資料夾的 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="aa227-445">Retrieves an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> object that represents a known folder.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-446"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath"><strong>SHGetKnownFolderPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-446"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath"><strong>SHGetKnownFolderPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-447">抓取資料夾的 <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a>所識別之已知資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="aa227-447">Retrieves the full path of a known folder identified by the folder's <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-448"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetlocalizedname"><strong>SHGetLocalizedName</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-448"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetlocalizedname"><strong>SHGetLocalizedName</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-449">抓取 Shell 資料夾中檔案的當地語系化名稱。</span><span class="sxs-lookup"><span data-stu-id="aa227-449">Retrieves the localized name of a file in a Shell folder.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-450"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetnamefromidlist"><strong>SHGetNameFromIDList</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-450"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetnamefromidlist"><strong>SHGetNameFromIDList</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-451">抓取其 Idlist.txt 所識別之專案的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="aa227-451">Retrieves the display name of an item identified by its IDList.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-452"><a href="/previous-versions/windows/desktop/legacy/bb762192(v=vs.85)"><strong>SHGetNameFromPropertyKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-452"><a href="/previous-versions/windows/desktop/legacy/bb762192(v=vs.85)"><strong>SHGetNameFromPropertyKey</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-453">根據指定的 <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a>，抓取屬性的正式名稱。</span><span class="sxs-lookup"><span data-stu-id="aa227-453">Retrieves the property's canonical name given its <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-454"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetnewlinkinfoa"><strong>SHGetNewLinkInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-454"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetnewlinkinfoa"><strong>SHGetNewLinkInfo</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-455">根據快捷方式的建議目標，建立新快速鍵的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa227-455">Creates a name for a new shortcut based on the shortcut's proposed target.</span></span> <span data-ttu-id="aa227-456">此函式不會建立快捷方式，只會建立名稱。</span><span class="sxs-lookup"><span data-stu-id="aa227-456">This function does not create the shortcut, just the name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-457"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista"><strong>SHGetPathFromIDList</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-457"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista"><strong>SHGetPathFromIDList</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-458">將專案識別碼清單轉換成檔案系統路徑。</span><span class="sxs-lookup"><span data-stu-id="aa227-458">Converts an item identifier list to a file system path.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-459"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlistex"><strong>SHGetPathFromIDListEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-459"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlistex"><strong>SHGetPathFromIDListEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-460">將專案識別碼清單轉換成檔案系統路徑。</span><span class="sxs-lookup"><span data-stu-id="aa227-460">Converts an item identifier list to a file system path.</span></span> <span data-ttu-id="aa227-461">此函式可讓您設定字串緩衝區的初始大小，並宣告下列選項，藉以擴充 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista"><strong>SHGetPathFromIDList</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="aa227-461">This function extends <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista"><strong>SHGetPathFromIDList</strong></a> by allowing you to set the initial size of the string buffer and declare the options below.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-462"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsettings"><strong>SHGetSettings</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-462"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsettings"><strong>SHGetSettings</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-463">抓取目前的 Shell 選項設定。</span><span class="sxs-lookup"><span data-stu-id="aa227-463">Retrieves the current Shell option settings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-464"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>SHGetStockIconInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-464"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>SHGetStockIconInfo</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-465">抓取系統定義之 Shell 圖示的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="aa227-465">Retrieves information about system-defined Shell icons.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-466"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgettemporarypropertyforitem"><strong>SHGetTemporaryPropertyForItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-466"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgettemporarypropertyforitem"><strong>SHGetTemporaryPropertyForItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-467">抓取指定專案的暫存屬性。</span><span class="sxs-lookup"><span data-stu-id="aa227-467">Retrieves the temporary property for the given item.</span></span> <span data-ttu-id="aa227-468">暫存屬性是一種讀取/寫入存放區，只保留 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> 物件存留期的屬性，而不是保存回專案中。</span><span class="sxs-lookup"><span data-stu-id="aa227-468">A temporary property is a read/write store that holds properties only for the lifetime of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> object, rather than being persisted back into the item.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-469"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetunreadmailcountw"><strong>SHGetUnreadMailCount</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-469"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetunreadmailcountw"><strong>SHGetUnreadMailCount</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-470">抓取任何或所有電子郵件帳戶的指定使用者未讀取訊息計數。</span><span class="sxs-lookup"><span data-stu-id="aa227-470">Retrieves a specified user's unread message count for any or all email accounts.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-471"><a href="/windows/desktop/api/shellapi/nf-shellapi-shisfileavailableoffline"><strong>SHIsFileAvailableOffline</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-471"><a href="/windows/desktop/api/shellapi/nf-shellapi-shisfileavailableoffline"><strong>SHIsFileAvailableOffline</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-472">判斷檔案或資料夾是否可供離線使用。</span><span class="sxs-lookup"><span data-stu-id="aa227-472">Determines whether a file or folder is available for offline use.</span></span> <span data-ttu-id="aa227-473">此函式也會決定要從網路、本機離線檔案快取或從這兩個位置開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="aa227-473">This function also determines whether the file would be opened from the network, from the local Offline Files cache, or from both locations.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-474"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shloadinproc"><strong>SHLoadInProc</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-474"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shloadinproc"><strong>SHLoadInProc</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-475">從 Shell 進程的內容中，建立指定之物件類別的實例。</span><span class="sxs-lookup"><span data-stu-id="aa227-475">Creates an instance of the specified object class from within the context of the Shell's process.</span></span> <br/> <span data-ttu-id="aa227-476"><strong>Windows Vista</strong> 和更新版本：此函式已停用，並傳回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="aa227-476"><strong>Windows Vista</strong> and later: This function has been disabled and returns E_NOTIMPL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-477"><a href="/windows/desktop/api/shellapi/nf-shellapi-shloadnonloadediconoverlayidentifiers"><strong>SHLoadNonloadedIconOverlayIdentifiers</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-477"><a href="/windows/desktop/api/shellapi/nf-shellapi-shloadnonloadediconoverlayidentifiers"><strong>SHLoadNonloadedIconOverlayIdentifiers</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-478">表示在下一次執行需要重迭資訊的作業期間，應該載入可能無法建立或不存在於啟動時建立的圖示重迭識別碼。</span><span class="sxs-lookup"><span data-stu-id="aa227-478">Signals the Shell that during the next operation requiring overlay information, it should load icon overlay identifiers that either failed creation or were not present for creation at startup.</span></span> <span data-ttu-id="aa227-479">已載入的識別碼不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="aa227-479">Identifiers that have already been loaded are not affected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-480"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shlocalstrdupa"><strong>SHLocalStrDup</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-480"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shlocalstrdupa"><strong>SHLocalStrDup</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-481">在新配置的記憶體中建立字串的複本。</span><span class="sxs-lookup"><span data-stu-id="aa227-481">Makes a copy of a string in newly allocated memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-482"><a href="/windows/desktop/api/Shlobj/nf-shlobj-shmultifileproperties"><strong>SHMultiFileProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-482"><a href="/windows/desktop/api/Shlobj/nf-shlobj-shmultifileproperties"><strong>SHMultiFileProperties</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-483">顯示一組檔案的合併屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="aa227-483">Displays a merged property sheet for a set of files.</span></span> <span data-ttu-id="aa227-484">會顯示所有檔案通用的屬性值，而不同的屬性值會顯示 <strong> (多個值) </strong>的字串。</span><span class="sxs-lookup"><span data-stu-id="aa227-484">Property values common to all the files are shown while those that differ display the string <strong>(multiple values)</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-485"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenfolderandselectitems"><strong>SHOpenFolderAndSelectItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-485"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenfolderandselectitems"><strong>SHOpenFolderAndSelectItems</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-486">開啟 Windows 檔案總管視窗，其中已選取特定資料夾中的指定專案。</span><span class="sxs-lookup"><span data-stu-id="aa227-486">Opens a Windows Explorer window with specified items in a particular folder selected.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-487"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenwithdialog"><strong>SHOpenWithDialog</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-487"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenwithdialog"><strong>SHOpenWithDialog</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-488">顯示 [ <strong>開啟方式</strong> ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="aa227-488">Displays the <strong>Open With</strong> dialog box.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-489"><a href="/windows/desktop/shell/showsharefolderui"><strong>ShowShareFolderUI</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-489"><a href="/windows/desktop/shell/showsharefolderui"><strong>ShowShareFolderUI</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-490">在 [內容] 工作表上，顯示指定資料夾的 [ <strong>資料夾共用</strong> ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="aa227-490">Displays the <strong>Folder Sharing</strong> tab on the properties sheet for the specified folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-491"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shparsedisplayname"><strong>SHParseDisplayName</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-491"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shparsedisplayname"><strong>SHParseDisplayName</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-492">將 Shell 命名空間物件的顯示名稱轉譯為專案識別碼清單，並傳回物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="aa227-492">Translates a Shell namespace object's display name into an item identifier list and returns the attributes of the object.</span></span> <span data-ttu-id="aa227-493">此函數是將字串轉換成 PIDL 的慣用方法。</span><span class="sxs-lookup"><span data-stu-id="aa227-493">This function is the preferred method to convert a string to a PIDL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-494"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shpathprepareforwritea"><strong>SHPathPrepareForWrite</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-494"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shpathprepareforwritea"><strong>SHPathPrepareForWrite</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-495">檢查路徑是否存在。</span><span class="sxs-lookup"><span data-stu-id="aa227-495">Checks to see if the path exists.</span></span> <span data-ttu-id="aa227-496">這包括重新掛接對應的網路磁碟機機、提示 ejectable 媒體重新插入、建立路徑、提示媒體格式化，以及提供適當的使用者介面（如有必要）。</span><span class="sxs-lookup"><span data-stu-id="aa227-496">This includes remounting mapped network drives, prompting for ejectable media to be reinserted, creating the paths, prompting for the media to be formatted, and providing the appropriate user interfaces, if necessary.</span></span> <span data-ttu-id="aa227-497">系統不會檢查媒體的讀取/寫入權限。</span><span class="sxs-lookup"><span data-stu-id="aa227-497">Read/write permissions for the medium are not checked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-498"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryrecyclebina"><strong>SHQueryRecycleBin</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-498"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryrecyclebina"><strong>SHQueryRecycleBin</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-499">針對指定的磁片磁碟機抓取資源回收筒的大小和其中的專案數目。</span><span class="sxs-lookup"><span data-stu-id="aa227-499">Retrieves the size of the Recycle Bin and the number of items in it, for a specified drive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-500"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate"><strong>SHQueryUserNotificationState</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-500"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate"><strong>SHQueryUserNotificationState</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-501">檢查目前使用者電腦的狀態，以判斷傳送通知是否適當。</span><span class="sxs-lookup"><span data-stu-id="aa227-501">Checks the state of the computer for the current user to determine whether sending a notification is appropriate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-502"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shremovelocalizedname"><strong>SHRemoveLocalizedName</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-502"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shremovelocalizedname"><strong>SHRemoveLocalizedName</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-503">移除 Shell 資料夾中檔案的當地語系化名稱。</span><span class="sxs-lookup"><span data-stu-id="aa227-503">Removes the localized name of a file in a Shell folder.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-504"><a href="/windows/desktop/api/Shlobj/nf-shlobj-shruncontrolpanel"><strong>SHRunControlPanel</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-504"><a href="/windows/desktop/api/Shlobj/nf-shlobj-shruncontrolpanel"><strong>SHRunControlPanel</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-505">開啟主控台專案。</span><span class="sxs-lookup"><span data-stu-id="aa227-505">Opens a Control Panel item.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="aa227-506">Windows Vista 不支援此功能</span><span class="sxs-lookup"><span data-stu-id="aa227-506">This function is not supported as of Windows Vista</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-507"><a href="/windows/desktop/api/Shobjidl/nf-shobjidl-shsetdefaultproperties"><strong>SHSetDefaultProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-507"><a href="/windows/desktop/api/Shobjidl/nf-shobjidl-shsetdefaultproperties"><strong>SHSetDefaultProperties</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-508">套用 Shell 專案的預設屬性集。</span><span class="sxs-lookup"><span data-stu-id="aa227-508">Applies the default set of properties on a Shell item.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-509"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetinstanceexplorer"><strong>SHSetInstanceExplorer</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-509"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetinstanceexplorer"><strong>SHSetInstanceExplorer</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-510">提供介面，允許裝載的 Shell 擴充和其他元件，以防止其主機進程提前關閉。</span><span class="sxs-lookup"><span data-stu-id="aa227-510">Provides an interface that allows hosted Shell extensions and other components to prevent their host process from closing prematurely.</span></span> <span data-ttu-id="aa227-511">主機進程通常是 Windows 檔案總管或 Internet Explorer，但其他應用程式也可以使用此函數。</span><span class="sxs-lookup"><span data-stu-id="aa227-511">The host process is typically Windows Explorer or Internet Explorer, but this function can also be used by other applications.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-512"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath"><strong>SHSetKnownFolderPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-512"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath"><strong>SHSetKnownFolderPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-513">將已知資料夾重新導向至新的位置。</span><span class="sxs-lookup"><span data-stu-id="aa227-513">Redirects a known folder to a new location.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-514"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shsetlocalizedname"><strong>SHSetLocalizedName</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-514"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shsetlocalizedname"><strong>SHSetLocalizedName</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-515">設定 Shell 資料夾中檔案的當地語系化名稱。</span><span class="sxs-lookup"><span data-stu-id="aa227-515">Sets the localized name of a file in a Shell folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-516"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shsettemporarypropertyforitem"><strong>SHSetTemporaryPropertyForItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-516"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shsettemporarypropertyforitem"><strong>SHSetTemporaryPropertyForItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-517">設定指定之專案的暫時屬性。</span><span class="sxs-lookup"><span data-stu-id="aa227-517">Sets a temporary property for the specified item.</span></span> <span data-ttu-id="aa227-518">暫存屬性會保留在讀取/寫入存放區中，只保留 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> 物件存留期的屬性，而不是將它們寫回專案中。</span><span class="sxs-lookup"><span data-stu-id="aa227-518">A temporary property is kept in a read/write store that holds properties only for the lifetime of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> object, instead of writing them back into the item.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-519"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shsetunreadmailcountw"><strong>SHSetUnreadMailCount</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-519"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shsetunreadmailcountw"><strong>SHSetUnreadMailCount</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-520">將指定之電子郵件帳戶的目前使用者未讀取訊息計數儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="aa227-520">Stores the current user's unread message count for a specified email account in the registry.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-521"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shtesttokenmembership"><strong>SHTestTokenMembership</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-521"><a href="/windows/desktop/api/Shellapi/nf-shellapi-shtesttokenmembership"><strong>SHTestTokenMembership</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-522">使用 <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-checktokenmembership"><strong>CheckTokenMembership</strong></a> 來測試指定的標記是否為具有指定 RID 之本機群組的成員。</span><span class="sxs-lookup"><span data-stu-id="aa227-522">Uses <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-checktokenmembership"><strong>CheckTokenMembership</strong></a> to test whether the given token is a member of the local group with the specified RID.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-523"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shupdateimagea"><strong>SHUpdateImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-523"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shupdateimagea"><strong>SHUpdateImage</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-524">通知 Shell 系統映射清單中的影像已變更。</span><span class="sxs-lookup"><span data-stu-id="aa227-524">Notifies the Shell that an image in the system image list has changed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-525"><a href="/windows/desktop/api/Shlobj/nf-shlobj-softwareupdatemessagebox"><strong>SoftwareUpdateMessageBox</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-525"><a href="/windows/desktop/api/Shlobj/nf-shlobj-softwareupdatemessagebox"><strong>SoftwareUpdateMessageBox</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-526">顯示標準訊息方塊，可用來通知使用者應用程式已更新。</span><span class="sxs-lookup"><span data-stu-id="aa227-526">Displays a standard message box that can be used to notify a user that an application has been updated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-527"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-stgmakeuniquename"><strong>StgMakeUniqueName</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-527"><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-stgmakeuniquename"><strong>StgMakeUniqueName</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-528">從範本建立資料流程或儲存物件的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="aa227-528">Creates a unique name for a stream or storage object from a template.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-529"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstrniw"><strong>StrStrNIW</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-529"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstrniw"><strong>StrStrNIW</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-530">在字串中尋找第一個出現的子字串。</span><span class="sxs-lookup"><span data-stu-id="aa227-530">Finds the first occurrence of a substring within a string.</span></span> <span data-ttu-id="aa227-531">此比較不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="aa227-531">The comparison is case-insensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-532"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstrnw"><strong>StrStrNW</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-532"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstrnw"><strong>StrStrNW</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-533">在字串中尋找第一個出現的子字串。</span><span class="sxs-lookup"><span data-stu-id="aa227-533">Finds the first occurrence of a substring within a string.</span></span> <span data-ttu-id="aa227-534">比較會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="aa227-534">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-535"><a href="/windows/desktop/api/Intshcut/nf-intshcut-translateurla"><strong>TranslateURL</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-535"><a href="/windows/desktop/api/Intshcut/nf-intshcut-translateurla"><strong>TranslateURL</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-536">將一般翻譯套用至指定的 URL 字串，建立新的 URL 字串。</span><span class="sxs-lookup"><span data-stu-id="aa227-536">Applies common translations to a given URL string, creating a new URL string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-537"><a href="/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile"><strong>UnloadUserProfile</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-537"><a href="/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile"><strong>UnloadUserProfile</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-538">卸載 <a href="/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea"><strong>LoadUserProfile</strong></a> 函數所載入的使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="aa227-538">Unloads a user's profile that was loaded by the <a href="/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea"><strong>LoadUserProfile</strong></a> function.</span></span> <span data-ttu-id="aa227-539">呼叫端必須具有電腦的系統管理許可權。</span><span class="sxs-lookup"><span data-stu-id="aa227-539">The caller must have administrative privileges on the computer.</span></span> <span data-ttu-id="aa227-540">如需詳細資訊，請參閱 <strong>LoadUserProfile</strong> 函數的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="aa227-540">For more information, see the Remarks section of the <strong>LoadUserProfile</strong> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-541"><a href="/windows/desktop/api/appnotify/nf-appnotify-unregisterappstatechangenotification"><strong>UnregisterAppStateChangeNotification</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-541"><a href="/windows/desktop/api/appnotify/nf-appnotify-unregisterappstatechangenotification"><strong>UnregisterAppStateChangeNotification</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-542">取消透過 <a href="/windows/desktop/api/appnotify/nf-appnotify-registerappstatechangenotification"><strong>RegisterAppStateChangeNotification</strong></a>註冊的變更通知。</span><span class="sxs-lookup"><span data-stu-id="aa227-542">Cancels a change notification registered through <a href="/windows/desktop/api/appnotify/nf-appnotify-registerappstatechangenotification"><strong>RegisterAppStateChangeNotification</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-543"><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-unregisterscalechangeevent"><strong>UnregisterScaleChangeEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-543"><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-unregisterscalechangeevent"><strong>UnregisterScaleChangeEvent</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-544">取消註冊透過 <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>RegisterScaleChangeEvent</strong></a>註冊的調整變更事件。</span><span class="sxs-lookup"><span data-stu-id="aa227-544">Unregisters for the scale change event registered through <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>RegisterScaleChangeEvent</strong></a>.</span></span> <span data-ttu-id="aa227-545">此函數會取代 <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-revokescalechangenotifications"><strong>RevokeScaleChangeNotifications</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="aa227-545">This function replaces <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-revokescalechangenotifications"><strong>RevokeScaleChangeNotifications</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-546"><a href="/windows/desktop/api/Intshcut/nf-intshcut-urlassociationdialoga"><strong>URLAssociationDialog</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-546"><a href="/windows/desktop/api/Intshcut/nf-intshcut-urlassociationdialoga"><strong>URLAssociationDialog</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-547">叫用未註冊的 [URL 通訊協定] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="aa227-547">Invokes the unregistered URL protocol dialog box.</span></span> <span data-ttu-id="aa227-548">此對話方塊可讓使用者選取要與先前未知通訊協定相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="aa227-548">This dialog box allows the user to select an application to associate with a previously unknown protocol.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="aa227-549">Windows XP SP2 或更新版本：不再支援此功能。</span><span class="sxs-lookup"><span data-stu-id="aa227-549">Windows XP SP2 or later: This function is no longer supported.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa227-550"><a href="/previous-versions/windows/desktop/legacy/bb762266(v=vs.85)"><strong>WinExecError</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-550"><a href="/previous-versions/windows/desktop/legacy/bb762266(v=vs.85)"><strong>WinExecError</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-551">如果 <a href="/windows/win32/api/winbase/nf-winbase-winexec">WinExec</a> 函式無法執行指定的應用程式，則抓取產生的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="aa227-551">Retrieves the error value generated if the <a href="/windows/win32/api/winbase/nf-winbase-winexec">WinExec</a> function cannot run a specified application.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa227-552"><a href="/windows/desktop/api/Winuser/nf-winuser-winhelpa"><strong>WinHelp</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa227-552"><a href="/windows/desktop/api/Winuser/nf-winuser-winhelpa"><strong>WinHelp</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa227-553">啟動 Windows 說明 (Winhelp.exe) 並傳遞其他資料，以指出應用程式所要求之說明的本質。</span><span class="sxs-lookup"><span data-stu-id="aa227-553">Launches Windows Help (Winhelp.exe) and passes additional data that indicates the nature of the help requested by the application.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 
