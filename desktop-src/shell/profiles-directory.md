---
description: 系統會將使用者設定檔資訊儲存在不同 Windows 版本中具有不同名稱的特定目錄中： &\# 0034; 檔和設定&\# 0034; windows XP 和 &\# 0034;使用者&\# 0034; 在 Windows Vista 和更新版本中。
title: 設定檔目錄
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 41056f40-fa1a-488a-b213-49cbdd8d4fdf
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3eb310434e5665dd8f28a661785403d72c4c1e46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973348"
---
# <a name="profiles-directory"></a><span data-ttu-id="1205f-103">設定檔目錄</span><span class="sxs-lookup"><span data-stu-id="1205f-103">Profiles Directory</span></span>

<span data-ttu-id="1205f-104">系統會將使用者設定檔資訊儲存在不同 Windows 版本的特定目錄中： Windows XP 中的「檔和設定」和 Windows Vista 和更新版本中的「使用者」。</span><span class="sxs-lookup"><span data-stu-id="1205f-104">The system stores user profile information in a specific directory, which has different names in different versions of Windows: "Documents and Settings" in Windows XP and "Users" in Windows Vista and later.</span></span> <span data-ttu-id="1205f-105">若要取得設定檔目錄的路徑，請使用 [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya) 函數。</span><span class="sxs-lookup"><span data-stu-id="1205f-105">To obtain the path of the profiles directory, use the [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya) function.</span></span>

<span data-ttu-id="1205f-106">設定檔目錄包含下列使用者設定檔的子目錄。</span><span class="sxs-lookup"><span data-stu-id="1205f-106">The profiles directory contains the following subdirectories for user profiles.</span></span>



| <span data-ttu-id="1205f-107">目錄</span><span class="sxs-lookup"><span data-stu-id="1205f-107">Directory</span></span>                                      | <span data-ttu-id="1205f-108">描述</span><span class="sxs-lookup"><span data-stu-id="1205f-108">Description</span></span>                                                                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1205f-109">ProgramData (Windows Vista 或更新版本) /All 使用者</span><span class="sxs-lookup"><span data-stu-id="1205f-109">ProgramData (Windows Vista or later)/All Users</span></span> | <span data-ttu-id="1205f-110">適用于所有使用者的程式資訊。</span><span class="sxs-lookup"><span data-stu-id="1205f-110">Program information that applies to all users.</span></span> <span data-ttu-id="1205f-111">在 Windows Vista 或更新版本中，[所有使用者] 目錄仍然存在，以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="1205f-111">The All Users directory still exists in Windows Vista or later, for backward compatibility.</span></span> |
| <span data-ttu-id="1205f-112">預設</span><span class="sxs-lookup"><span data-stu-id="1205f-112">Default</span></span>                                        | <span data-ttu-id="1205f-113">適用于預設使用者的設定檔資訊。</span><span class="sxs-lookup"><span data-stu-id="1205f-113">Profile information that applies to the default user.</span></span>                                                                                      |
| <span data-ttu-id="1205f-114">*使用者*</span><span class="sxs-lookup"><span data-stu-id="1205f-114">*User*</span></span>                                         | <span data-ttu-id="1205f-115">適用于指定使用者的設定檔資訊。</span><span class="sxs-lookup"><span data-stu-id="1205f-115">Profile information that applies to the specified user.</span></span> <span data-ttu-id="1205f-116">每個使用者都有自己的設定檔子目錄。</span><span class="sxs-lookup"><span data-stu-id="1205f-116">Each user has their own profile subdirectory.</span></span>                                      |



 

<span data-ttu-id="1205f-117">若要取得 ProgramData/All Users 目錄的位置，請呼叫 [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya) 函數。</span><span class="sxs-lookup"><span data-stu-id="1205f-117">To obtain the location of the ProgramData/All Users directory, call the [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya) function.</span></span> <span data-ttu-id="1205f-118">此目錄包含下列子目錄：</span><span class="sxs-lookup"><span data-stu-id="1205f-118">This directory contains the following subdirectories:</span></span>



| <span data-ttu-id="1205f-119">目錄</span><span class="sxs-lookup"><span data-stu-id="1205f-119">Directory</span></span>  | <span data-ttu-id="1205f-120">描述</span><span class="sxs-lookup"><span data-stu-id="1205f-120">Description</span></span>                          |
|------------|--------------------------------------|
| <span data-ttu-id="1205f-121">桌面</span><span class="sxs-lookup"><span data-stu-id="1205f-121">Desktop</span></span>    | <span data-ttu-id="1205f-122">要顯示在桌面上的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="1205f-122">Shortcuts to display on the desktop.</span></span> |
| <span data-ttu-id="1205f-123">開始功能表</span><span class="sxs-lookup"><span data-stu-id="1205f-123">Start Menu</span></span> | <span data-ttu-id="1205f-124">[ **開始** ] 功能表的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="1205f-124">Menu items for the **Start** menu.</span></span>   |



 

<span data-ttu-id="1205f-125">若要取得預設使用者目錄的位置，請呼叫 [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya) 函數。</span><span class="sxs-lookup"><span data-stu-id="1205f-125">To obtain the location of the default user's directory, call the [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya) function.</span></span> <span data-ttu-id="1205f-126">若要取得特定使用者目錄的位置，請呼叫 [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya) 函數。</span><span class="sxs-lookup"><span data-stu-id="1205f-126">To obtain the location of a particular user's directory, call the [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya) function.</span></span> <span data-ttu-id="1205f-127">預設的使用者和特定的使用者目錄都包含下列子目錄。</span><span class="sxs-lookup"><span data-stu-id="1205f-127">Both the default user and specific user directories contain the following subdirectories.</span></span> <span data-ttu-id="1205f-128">斜體的目錄表示預設會隱藏的目錄。</span><span class="sxs-lookup"><span data-stu-id="1205f-128">Directories in italics indicate directories that are hidden by default.</span></span> <span data-ttu-id="1205f-129">您可以選取 [**資料夾選項**] 控制台專案中的 [**顯示隱藏的檔案、資料夾和磁片磁碟機**] 選項來查看這些目錄。</span><span class="sxs-lookup"><span data-stu-id="1205f-129">You can view these directories by selecting the **Show hidden files, folders, and drives** option in the **Folder Options** control panel item.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1205f-130">目錄</span><span class="sxs-lookup"><span data-stu-id="1205f-130">Directory</span></span></th>
<th><span data-ttu-id="1205f-131">描述</span><span class="sxs-lookup"><span data-stu-id="1205f-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1205f-132">應用程式資料</span><span class="sxs-lookup"><span data-stu-id="1205f-132">Application Data</span></span></td>
<td><span data-ttu-id="1205f-133">應用程式特定資料。</span><span class="sxs-lookup"><span data-stu-id="1205f-133">Application-specific data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1205f-134">Cookie</span><span class="sxs-lookup"><span data-stu-id="1205f-134">Cookies</span></span></td>
<td><span data-ttu-id="1205f-135">Windows Internet Explorer cookies。</span><span class="sxs-lookup"><span data-stu-id="1205f-135">Windows Internet Explorer cookies.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1205f-136">桌面</span><span class="sxs-lookup"><span data-stu-id="1205f-136">Desktop</span></span></td>
<td><span data-ttu-id="1205f-137">要顯示在桌面上的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="1205f-137">Shortcuts to display on the desktop.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1205f-138">我的最愛</span><span class="sxs-lookup"><span data-stu-id="1205f-138">Favorites</span></span></td>
<td><span data-ttu-id="1205f-139">連結至我的最愛網站。</span><span class="sxs-lookup"><span data-stu-id="1205f-139">Links to favorite websites.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1205f-140">本機設定</span><span class="sxs-lookup"><span data-stu-id="1205f-140">Local Settings</span></span></td>
<td><span data-ttu-id="1205f-141">未隨設定檔漫遊的應用程式設定和資料。</span><span class="sxs-lookup"><span data-stu-id="1205f-141">Application settings and data that do not roam with the profile.</span></span> <span data-ttu-id="1205f-142">此目錄中的設定或資料通常是電腦特定的，或太大而無法有效漫遊。</span><span class="sxs-lookup"><span data-stu-id="1205f-142">Usually the settings or data in this directory are computer-specific, or they are too large to roam effectively.</span></span> <span data-ttu-id="1205f-143">此目錄包含下列子資料夾：</span><span class="sxs-lookup"><span data-stu-id="1205f-143">This directory contains the following subfolders:</span></span>
<ul>
<li><span data-ttu-id="1205f-144">應用程式資料</span><span class="sxs-lookup"><span data-stu-id="1205f-144">Application Data</span></span></li>
<li><span data-ttu-id="1205f-145">記錄</span><span class="sxs-lookup"><span data-stu-id="1205f-145">History</span></span></li>
<li><span data-ttu-id="1205f-146">Temp</span><span class="sxs-lookup"><span data-stu-id="1205f-146">Temp</span></span></li>
<li><span data-ttu-id="1205f-147">Temporary Internet Files</span><span class="sxs-lookup"><span data-stu-id="1205f-147">Temporary Internet Files</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1205f-148">我的文件</span><span class="sxs-lookup"><span data-stu-id="1205f-148">My Documents</span></span></td>
<td><span data-ttu-id="1205f-149">使用者所建立檔的預設位置。</span><span class="sxs-lookup"><span data-stu-id="1205f-149">The default location for documents that the user creates.</span></span> <span data-ttu-id="1205f-150">根據預設，應用程式應該會將檔檔儲存到這個目錄。</span><span class="sxs-lookup"><span data-stu-id="1205f-150">Applications should save document files to this directory by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1205f-151"><em>NetHood</em></span><span class="sxs-lookup"><span data-stu-id="1205f-151"><em>NetHood</em></span></span></td>
<td><span data-ttu-id="1205f-152">網路鄰近專案的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="1205f-152">Shortcuts to Network Neighborhood items.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1205f-153"><em>PrintHood</em></span><span class="sxs-lookup"><span data-stu-id="1205f-153"><em>PrintHood</em></span></span></td>
<td><span data-ttu-id="1205f-154">印表機資料夾專案的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="1205f-154">Shortcuts to printer folder items.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1205f-155"><em>最近</em></span><span class="sxs-lookup"><span data-stu-id="1205f-155"><em>Recent</em></span></span></td>
<td><span data-ttu-id="1205f-156">最近使用之檔的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="1205f-156">Shortcuts to the most recently used documents.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1205f-157">SendTo</span><span class="sxs-lookup"><span data-stu-id="1205f-157">SendTo</span></span></td>
<td><span data-ttu-id="1205f-158">使用者通常傳送檔案之位置的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="1205f-158">Shortcuts to locations to which the user often sends files.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1205f-159">開始功能表</span><span class="sxs-lookup"><span data-stu-id="1205f-159">Start Menu</span></span></td>
<td><span data-ttu-id="1205f-160">[ <strong>開始</strong> ] 功能表的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="1205f-160">Menu items for the <strong>Start</strong> menu.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1205f-161"><em>範本</em></span><span class="sxs-lookup"><span data-stu-id="1205f-161"><em>Templates</em></span></span></td>
<td><span data-ttu-id="1205f-162">範本專案的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="1205f-162">Shortcuts to template items.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1205f-163">若要取得這些目錄之子目錄的位置，請使用 [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) 或 [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) 函式。</span><span class="sxs-lookup"><span data-stu-id="1205f-163">To obtain the location of subdirectories of these directories, use the [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) or [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) functions.</span></span>

 

 



