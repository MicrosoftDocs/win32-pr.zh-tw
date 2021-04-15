---
title: 使用 Least-Privileged 使用者帳戶的遊戲
description: 本文說明遊戲開發人員如何撰寫適用于最低許可權使用者帳戶的 Microsoft Windows 遊戲 (也稱為受限使用者帳戶) 。
ms.assetid: 1b7cc3c9-b180-14b1-53c8-57f9e545d009
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4c44d94345462fc02ec649c5674ed88c38c12ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463421"
---
# <a name="gaming-with-least-privileged-user-accounts"></a><span data-ttu-id="b4a7d-103">使用 Least-Privileged 使用者帳戶的遊戲</span><span class="sxs-lookup"><span data-stu-id="b4a7d-103">Gaming with Least-Privileged User Accounts</span></span>

<span data-ttu-id="b4a7d-104">本文說明遊戲開發人員如何撰寫適用于最低許可權使用者帳戶的 Microsoft Windows 遊戲 (也稱為受限使用者帳戶) 。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-104">This article describes how games developers can author Microsoft Windows games that work well with least-privileged user accounts (also known as limited-user accounts).</span></span>

-   [<span data-ttu-id="b4a7d-105">簡介</span><span class="sxs-lookup"><span data-stu-id="b4a7d-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="b4a7d-106">Least-Privileged 使用者帳戶的檔案存取</span><span class="sxs-lookup"><span data-stu-id="b4a7d-106">File Access for Least-Privileged User Accounts</span></span>](#file-access-for-least-privileged-user-accounts)
    -   [<span data-ttu-id="b4a7d-107">案例1：使用者不需要查看或變更的檔案</span><span class="sxs-lookup"><span data-stu-id="b4a7d-107">Scenario 1: Files that do not need to be viewed or altered by users</span></span>](#scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users)
    -   [<span data-ttu-id="b4a7d-108">案例2：需要由使用者查看或變更的檔案</span><span class="sxs-lookup"><span data-stu-id="b4a7d-108">Scenario 2: Files that need to be viewed or altered by users</span></span>](#scenario-2-files-that-need-to-be-viewed-or-altered-by-users)
-   [<span data-ttu-id="b4a7d-109">Least-Privileged 使用者帳戶的登錄存取權</span><span class="sxs-lookup"><span data-stu-id="b4a7d-109">Registry Access for Least-Privileged User Accounts</span></span>](#registry-access-for-least-privileged-user-accounts)
-   [<span data-ttu-id="b4a7d-110">使用 Least-Privileged 使用者帳戶進行修補</span><span class="sxs-lookup"><span data-stu-id="b4a7d-110">Patching with Least-Privileged User Accounts</span></span>](#patching-with-least-privileged-user-accounts)

## <a name="introduction"></a><span data-ttu-id="b4a7d-111">簡介</span><span class="sxs-lookup"><span data-stu-id="b4a7d-111">Introduction</span></span>

<span data-ttu-id="b4a7d-112">Windows 會以帳戶管理其使用者。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-112">Windows manages its users with accounts.</span></span> <span data-ttu-id="b4a7d-113">現今，在家裡有超過80% 的電腦使用者與其他家庭成員共用電腦。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-113">Today, more than eighty percent of computer users at home share their computer with other family members.</span></span> <span data-ttu-id="b4a7d-114">當多個使用者共用 Windows 電腦時，會建立多個使用者帳戶，而每個使用者會以個別帳戶登入，以存取電腦。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-114">When multiple users share a Windows computer, multiple user accounts are created, and each user logs in with an individual account to access the computer.</span></span> <span data-ttu-id="b4a7d-115">有了安全性的增強功能，就能讓使用者以最低許可權的使用者帳戶操作電腦，也就是不具有系統完整控制權的有限使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-115">With the increasing awareness for security, more people operate their computers with least-privileged user accounts, also known as limited-user accounts, which do not have complete control over the system.</span></span> <span data-ttu-id="b4a7d-116">系統管理員帳戶通常不受限制地存取電腦的每個部分。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-116">Administrator accounts typically have unrestricted access to every part of the computer.</span></span> <span data-ttu-id="b4a7d-117">這可能會影響 Windows 遊戲的運作方式。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-117">This can affect how Windows-based games work.</span></span>

<span data-ttu-id="b4a7d-118">針對撰寫遊戲的遊戲開發人員，有額外的權益可使用最低許可權的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-118">There are additional benefits for games developers who write their games to work with least-privileged user accounts.</span></span> <span data-ttu-id="b4a7d-119">在 Windows Vista 和更新版本中，系統會強制執行最低許可權的使用者帳戶，這表示系統上的每個帳戶（除了本機系統管理員以外）都是最低許可權的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-119">In Windows Vista and later, least-privileged user accounts are enforced, which means that every account on the system, with the exception of the local administrator, is a least-privileged user account.</span></span> <span data-ttu-id="b4a7d-120">這會影響不遵循指導方針 (繼承應用程式) 在 Windows Vista 和更新版本上執行的遊戲。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-120">This will affect how games that do not follow the guideline (legacy applications) run on Windows Vista and later.</span></span> <span data-ttu-id="b4a7d-121">例如，當應用程式嘗試寫入至沒有許可權的資料夾或登錄值時，會將檔案寫入重新導向至使用者的虛擬檔案存放區。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-121">For instance, when an application attempts to write to a folder or a registry value to which it does not have permission, the file write is redirected to a virtual file store for the user.</span></span> <span data-ttu-id="b4a7d-122">此虛擬檔案存放區將位於使用者具有寫入權限的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-122">This virtual file store will reside in a folder to which the user has write access.</span></span> <span data-ttu-id="b4a7d-123">這種行為看起來可能不像寫入嘗試失敗的情況，不過，建立虛擬檔案的應用程式可能會讓使用者混淆，因為檔案不會寫入至使用者預期的位置。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-123">This behavior may not seem as catastrophic as outright failing the write attempt; however, applications that create virtualized files may confuse users because files will not be written to the location users expect.</span></span> <span data-ttu-id="b4a7d-124">比方說，將高分數檔案寫入與可執行檔資料夾相同資料夾的遊戲，會改為將這些檔案寫入虛擬化資料夾。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-124">For instance, games that write high score files to the same folder as the executable folder will write these files to a virtualized folder instead.</span></span> <span data-ttu-id="b4a7d-125">因此，一位使用者無法看到由另一位使用者所達成的高分數，因為每位使用者都有個別的虛擬化檔案存放區。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-125">Consequently, one user cannot see the high score achieved by another user because every user has a separate virtualized file store.</span></span>

<span data-ttu-id="b4a7d-126">遵循本文指導方針的遊戲將會以最低許可權的使用者帳戶執行，因此會維持與 Windows Vista 和更新版本的相容性。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-126">Games that follow the guidelines in this article will run with least-privileged user accounts, and consequently will maintain compatibility with Windows Vista and later.</span></span>

## <a name="file-access-for-least-privileged-user-accounts"></a><span data-ttu-id="b4a7d-127">Least-Privileged 使用者帳戶的檔案存取</span><span class="sxs-lookup"><span data-stu-id="b4a7d-127">File Access for Least-Privileged User Accounts</span></span>

<span data-ttu-id="b4a7d-128">Windows 支援兩種檔案系統： FAT32 和 NTFS。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-128">Windows supports two file systems: FAT32 and NTFS.</span></span> <span data-ttu-id="b4a7d-129">FAT32 是僅為了回溯相容性所支援的舊版檔案系統;NTFS 支援功能強大且功能更強大的檔案許可權。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-129">FAT32 is a legacy file system supported only for backward compatibility; NTFS supports more powerful and robust file permissions.</span></span> <span data-ttu-id="b4a7d-130">使用 NTFS 正在擴充，因為零售商正在以 NTFS 磁片磁碟機上預先安裝的 Windows 來傳送新電腦。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-130">The use of NTFS is expanding as retailers are shipping new computers with Windows pre-installed on a NTFS-partitioned hard drive.</span></span> <span data-ttu-id="b4a7d-131">在 NTFS 型的 Windows XP 系統上，具有最低許可權使用者帳戶的使用者只會有數個資料夾的有限存取權。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-131">On an NTFS-based Windows XP system, users with least-privileged user accounts have only limited access to several folders.</span></span> <span data-ttu-id="b4a7d-132">不過，它們會在以 FAT32 為基礎的 Windows XP 系統上具有完整的存取權。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-132">However, they would have complete access on a FAT32-based Windows XP system.</span></span>

<span data-ttu-id="b4a7d-133">下表列出這些資料夾及其許可權的預設位置。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-133">The following table lists the default location of these folders and their permissions.</span></span>



| <span data-ttu-id="b4a7d-134">路徑</span><span class="sxs-lookup"><span data-stu-id="b4a7d-134">Path</span></span>                                               | <span data-ttu-id="b4a7d-135">資料夾內容</span><span class="sxs-lookup"><span data-stu-id="b4a7d-135">Folder Contents</span></span>              | <span data-ttu-id="b4a7d-136">讀取</span><span class="sxs-lookup"><span data-stu-id="b4a7d-136">Read</span></span> | <span data-ttu-id="b4a7d-137">寫入</span><span class="sxs-lookup"><span data-stu-id="b4a7d-137">Write</span></span> | <span data-ttu-id="b4a7d-138">建立/刪除</span><span class="sxs-lookup"><span data-stu-id="b4a7d-138">Create/Delete</span></span> |
|----------------------------------------------------|------------------------------|------|-------|---------------|
| <span data-ttu-id="b4a7d-139"><Drive>： \\ Windows</span><span class="sxs-lookup"><span data-stu-id="b4a7d-139"><Drive>:\\Windows</span></span>                            | <span data-ttu-id="b4a7d-140">Windows 作業系統</span><span class="sxs-lookup"><span data-stu-id="b4a7d-140">The Windows operating system</span></span> | <span data-ttu-id="b4a7d-141">X</span><span class="sxs-lookup"><span data-stu-id="b4a7d-141">X</span></span>    |       |               |
| <span data-ttu-id="b4a7d-142"><Drive>： \\ Program Files</span><span class="sxs-lookup"><span data-stu-id="b4a7d-142"><Drive>:\\Program Files</span></span>                      | <span data-ttu-id="b4a7d-143">可執行檔應用程式檔</span><span class="sxs-lookup"><span data-stu-id="b4a7d-143">Executable application files</span></span> | <span data-ttu-id="b4a7d-144">X</span><span class="sxs-lookup"><span data-stu-id="b4a7d-144">X</span></span>    |       |               |
| <span data-ttu-id="b4a7d-145"><Drive>： \\ 檔和設定使用者 \\ 名稱\*</span><span class="sxs-lookup"><span data-stu-id="b4a7d-145"><Drive>:\\Documents and Settings\\Username\*</span></span> | <span data-ttu-id="b4a7d-146">每個使用者的檔案</span><span class="sxs-lookup"><span data-stu-id="b4a7d-146">Each user's files</span></span>            | <span data-ttu-id="b4a7d-147">X</span><span class="sxs-lookup"><span data-stu-id="b4a7d-147">X</span></span>    | <span data-ttu-id="b4a7d-148">X</span><span class="sxs-lookup"><span data-stu-id="b4a7d-148">X</span></span>     | <span data-ttu-id="b4a7d-149">X</span><span class="sxs-lookup"><span data-stu-id="b4a7d-149">X</span></span>             |
| <span data-ttu-id="b4a7d-150"><Drive>： \\ 檔和設定 \\ 所有使用者</span><span class="sxs-lookup"><span data-stu-id="b4a7d-150"><Drive>:\\Documents and Settings\\All Users</span></span>  | <span data-ttu-id="b4a7d-151">所有使用者檔案</span><span class="sxs-lookup"><span data-stu-id="b4a7d-151">All user files</span></span>               | <span data-ttu-id="b4a7d-152">X</span><span class="sxs-lookup"><span data-stu-id="b4a7d-152">X</span></span>    | <span data-ttu-id="b4a7d-153">X</span><span class="sxs-lookup"><span data-stu-id="b4a7d-153">X</span></span>     | <span data-ttu-id="b4a7d-154">X</span><span class="sxs-lookup"><span data-stu-id="b4a7d-154">X</span></span>             |



 

<span data-ttu-id="b4a7d-155">\* Username 是使用者的登入名稱。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-155">\* Username is the user's login name.</span></span>

<span data-ttu-id="b4a7d-156">在最低許可權的使用者帳戶中，您可以讀取、寫入、建立和刪除資料夾中的檔案： [檔] 和 [設定使用者名稱]、[檔] \\ 和 [設定 \\ 所有使用者]。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-156">In a least-privileged user account, you may read, write, create and delete files in either folder: Documents and Settings\\Username or Documents and Settings\\All Users.</span></span>

<span data-ttu-id="b4a7d-157">這表示，您不應該將 [儲存遊戲] 放置在 [ \\ Program Files] 中，改為移至我的檔的子資料夾中 \\ 。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-157">What this means is that you should not place save games in \\Program Files, instead they should go in a sub-folder in \\My Documents.</span></span> <span data-ttu-id="b4a7d-158">此外，您不應該將暫存的應用程式資料放在 \\ 程式檔或 \\ 我的檔中，而是放置在 [應用程式資料] 資料夾中， (CSIDL \_ 本機 \_ APPDATA) 。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-158">Also you should not place temporary application data in \\Program Files or \\My Documents, instead it should be placed in Application Data folder (CSIDL\_LOCAL\_APPDATA).</span></span>

<span data-ttu-id="b4a7d-159">更具體來說，每個遊戲應該處理的案例有兩種：</span><span class="sxs-lookup"><span data-stu-id="b4a7d-159">More specifically, there are two scenarios that each game should handle:</span></span>

### <a name="scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users"></a><span data-ttu-id="b4a7d-160">案例1：使用者不需要查看或變更的檔案</span><span class="sxs-lookup"><span data-stu-id="b4a7d-160">Scenario 1: Files that do not need to be viewed or altered by users</span></span>

<span data-ttu-id="b4a7d-161">典型的範例是遊戲的設定檔、暫存檔案和遊戲快取檔案。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-161">A typical example would be the game's configuration file, temporary files, and game cache files.</span></span> <span data-ttu-id="b4a7d-162">這些檔案通常會保留在應用程式資料夾中。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-162">These files are typically kept in the Application Data folder.</span></span> <span data-ttu-id="b4a7d-163">若要取得此資料夾路徑，請[](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)使用 CSIDL \_ APPDATA 或 CSIDL LOCAL APPDATA 呼叫 SHGetFolderPath 函式， \_ \_ 如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-163">To obtain this folder path, call the [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) function with CSIDL\_APPDATA or CSIDL\_LOCAL\_APPDATA as shown in the following code example.</span></span>

``` syntax
#include <shlobj.h>
#include <strsafe.h>

#define APPNAME L"MyApp"

WCHAR wszPath[MAX_PATH];

// Local Application Data
SHGetFolderPath( hWnd, CSIDL_LOCAL_APPDATA, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
// Roaming Application Data
SHGetFolderPath( hWnd, CSIDL_APPDATA, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
```

<span data-ttu-id="b4a7d-164">本機和漫遊應用程式資料檔案夾之間的差異在於，在 Windows 2000 和 Windows XP 上，漫遊內容會在登入/登出進程期間複製到伺服器，而本機內容則不會。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-164">The difference between local and roaming Application Data folders is that on Windows 2000 and Windows XP, roaming content is copied to and from the server during the logon/logoff process, while local content is not.</span></span> <span data-ttu-id="b4a7d-165">在大部分的遊戲中，本機應用程式資料就已足夠。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-165">For most games, local Application Data is sufficient.</span></span>

### <a name="scenario-2-files-that-need-to-be-viewed-or-altered-by-users"></a><span data-ttu-id="b4a7d-166">案例2：需要由使用者查看或變更的檔案</span><span class="sxs-lookup"><span data-stu-id="b4a7d-166">Scenario 2: Files that need to be viewed or altered by users</span></span>

<span data-ttu-id="b4a7d-167">典型的範例是使用者儲存的遊戲檔案。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-167">A typical example would be a user's saved game files.</span></span> <span data-ttu-id="b4a7d-168">將檔案儲存在使用者的 [檔] 資料夾中，讓使用者可以輕鬆看見檔案。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-168">Store the files in the user's document folder so that they are easily visible to the user.</span></span> <span data-ttu-id="b4a7d-169">應用程式會藉由呼叫 [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) 與 CSIDL PERSONAL 來取得使用者的檔資料夾路徑 \_ ，如下列程式碼範例所示：</span><span class="sxs-lookup"><span data-stu-id="b4a7d-169">An application gets the user's document folder path by calling [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) with CSIDL\_PERSONAL, as the following code example shows:</span></span>

``` syntax
#include <shlobj.h>
#include <strsafe.h>

#define APPNAME L"MyApp"

WCHAR wszPath[MAX_PATH];

SHGetFolderPath( hWnd, CSIDL_PERSONAL, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
```

<span data-ttu-id="b4a7d-170">有時候，遊戲可能需要儲存所有使用者要查看和使用的檔案。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-170">At times, a game may need to store files that all users are meant to see and use.</span></span> <span data-ttu-id="b4a7d-171">其中一個範例是高分數記錄，其中所有使用者都會寫入相同的記錄檔，如此一來，就會為每位使用者維持全系統的高度分數，而不是個別的高度分數。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-171">One example is the high score record, where all users write to the same record file so that high scores are maintained system-wide instead of a separate high score for each user.</span></span> <span data-ttu-id="b4a7d-172">其他範例包括下載的地圖、任務和遊戲修改。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-172">Other examples are downloaded maps, missions, and game modifications.</span></span> <span data-ttu-id="b4a7d-173">如果共用這些共用，則只有一位使用者必須下載它們，而不是每位使用者。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-173">If these are shared, then only one user has to download them instead of every user.</span></span> <span data-ttu-id="b4a7d-174">在此案例中，請使用 [共用設定檔] 資料夾底下的 [檔] 資料夾，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-174">In this scenario, use the document folder under the shared profile folder, as demonstrated in the following code.</span></span>

``` syntax
#include <shlobj.h>
#include <strsafe.h>

#define APPNAME L"MyApp"

WCHAR wszPath[MAX_PATH];

SHGetFolderPath( hWnd, CSIDL_COMMON_DOCUMENTS, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
```

## <a name="registry-access-for-least-privileged-user-accounts"></a><span data-ttu-id="b4a7d-175">Least-Privileged 使用者帳戶的登錄存取權</span><span class="sxs-lookup"><span data-stu-id="b4a7d-175">Registry Access for Least-Privileged User Accounts</span></span>

<span data-ttu-id="b4a7d-176">應用程式通常會使用 Windows 登錄來儲存資訊。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-176">It is common for applications to use the Windows registry to store information.</span></span> <span data-ttu-id="b4a7d-177">類似于檔案存取，系統管理員和最低許可權的使用者帳戶沒有登錄的相同許可權。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-177">Similar to file access, administrator and least-privileged user accounts do not have the same permission to the registry.</span></span> <span data-ttu-id="b4a7d-178">針對最低許可權的使用者帳戶，整個 HKEY \_ 本機 \_ 電腦節點是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-178">For least-privileged user accounts, the entire HKEY\_LOCAL\_MACHINE node is read-only.</span></span> <span data-ttu-id="b4a7d-179">例如，遊戲可以讀取預設的設定資訊，但可能不會將任何新資訊寫入此節點。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-179">For instance, a game can read the default configuration information, but may not write any new information to this node.</span></span> <span data-ttu-id="b4a7d-180">因此，以最低許可權的使用者模式執行的遊戲必須寫入登錄，才能使用 [HKEY 目前的使用者] \_ \_ 節點來儲存每個使用者的資訊，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-180">Consequently, games running in least-privileged user mode that need to write to the registry will need to use the HKEY\_CURRENT\_USER node to store per-user information, as illustrated in the following code.</span></span>

``` syntax
#define APP_REGISTRY_KEY_PATH L"Software\\MyCompany\\MyApp"

LONG lRetVal;
HKEY hKey;

lRetVal = RegCreateKeyExW( HKEY_CURRENT_USER,
                           APP_REGISTRY_KEY_PATH,
                           0,
                           NULL,
                           REG_OPTION_NON_VOLATILE,
                           KEY_WRITE|KEY_READ,
                           NULL,
                           &hKey,
                           NULL );

if( ERROR_SUCCESS == lRetVal )
{
    // Store information in hKey
}
```

<span data-ttu-id="b4a7d-181">值得注意的是，在安裝期間，應該將登錄資訊寫入 HKEY \_ 本機 \_ 電腦，而不是 HKEY \_ 目前的 \_ 使用者。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-181">It is worth noting that during installation, registry information should be written to HKEY\_LOCAL\_MACHINE, not HKEY\_CURRENT\_USER.</span></span> <span data-ttu-id="b4a7d-182">這是因為執行安裝的人員通常是系統管理員，而且可能不是使用程式的唯一人員。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-182">This is because the person running the installation is usually an administrator, and may not be the only person to use the program.</span></span> <span data-ttu-id="b4a7d-183">在這種情況下，寫入 HKEY \_ 目前 \_ 的使用者會讓其他使用者無法使用該資訊。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-183">In this situation, writing to HKEY\_CURRENT\_USER makes the information unavailable to other users.</span></span> <span data-ttu-id="b4a7d-184">這通常不是問題，因為在安裝期間寫入登錄的資訊是套用至程式每個使用者的設定和預設設定。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-184">This is not usually an issue because the information written to the registry during installation is the configuration and default settings that apply to every user of the program.</span></span>

<span data-ttu-id="b4a7d-185">卸載遊戲時，必須進行額外的工作，才能移除遊戲已寫入登錄的每個值。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-185">When uninstalling the game, extra effort is necessary to remove every value that the game has written to the registry.</span></span> <span data-ttu-id="b4a7d-186">因為卸載程式是由一位人員（通常是系統管理員）執行，所以直接刪除 HKEY 本機電腦中的相關資訊， \_ \_ 而 HKEY \_ 目前的 \_ 使用者將不會移除其他使用者的值。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-186">Because the uninstaller is run by one person, usually the administrator, simply deleting the relevant information in HKEY\_LOCAL\_MACHINE and HKEY\_CURRENT\_USER will not remove values for other users.</span></span> <span data-ttu-id="b4a7d-187">移除登錄中每個使用者資訊的其中一種方式，是列舉 HKEY \_ USERS 登錄 hive 根目錄。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-187">One way to remove the per-user information in the registry is to enumerate the HKEY\_USERS registry hive root.</span></span> <span data-ttu-id="b4a7d-188">HKEY USERS 下的每個子機碼都會 \_ 對應到 \_ \_ 系統上特定使用者的 HKEY 目前使用者 hive。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-188">Each subkey under HKEY\_USERS corresponds to the HKEY\_CURRENT\_USER hive for a particular user on the system.</span></span> <span data-ttu-id="b4a7d-189">藉由列舉 HKEY \_ 使用者並移除每個子機碼下的遊戲特定資訊，卸載程式可以確保不會留下任何資訊。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-189">By enumerating HKEY\_USERS and removing the game-specific information under each subkey, the uninstaller can ensure that no information is left behind.</span></span>

## <a name="patching-with-least-privileged-user-accounts"></a><span data-ttu-id="b4a7d-190">使用 Least-Privileged 使用者帳戶進行修補</span><span class="sxs-lookup"><span data-stu-id="b4a7d-190">Patching with Least-Privileged User Accounts</span></span>

<span data-ttu-id="b4a7d-191">修補遊戲牽涉到更新遊戲的檔案。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-191">Patching a game involves updating the game's files.</span></span> <span data-ttu-id="b4a7d-192">因此，它通常需要對遊戲的程式資料夾進行寫入存取。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-192">Therefore, it usually requires write access to the game's program folder.</span></span> <span data-ttu-id="b4a7d-193">修補遊戲是由系統管理員完成的簡單程式，因為他們對遊戲的程式資料夾有不受限制的存取權。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-193">Patching a game is a straightforward process when it is done by an administrator because they have unrestricted access to the game's program folder.</span></span> <span data-ttu-id="b4a7d-194">相反地，基於存取限制，通常很難在不可能的情況下，為最低許可權的使用者修補遊戲。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-194">Conversely, it has traditionally been difficult, if not impossible, for a least privileged user to patch games because of the access restriction.</span></span> <span data-ttu-id="b4a7d-195">現在， [Windows Installer](/windows/desktop/Msi/windows-installer-portal) 已增強，可讓最低許可權的使用者帳戶進行修補。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-195">Now, [Windows Installer](/windows/desktop/Msi/windows-installer-portal) has been enhanced to make least-privileged user account patching possible.</span></span> <span data-ttu-id="b4a7d-196">為了充分利用這項功能，我們鼓勵遊戲利用 Windows Installer 進行安裝和修補。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-196">To take advantage of this feature, games are encouraged to utilize Windows Installer for installation and patching.</span></span>

<span data-ttu-id="b4a7d-197">從 Windows Installer 3.0 開始，在符合特定條件時，應用程式修補程式可由最低許可權使用者套用。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-197">Starting with Windows Installer 3.0, application patches can be applied by least privileged users when certain conditions are met.</span></span> <span data-ttu-id="b4a7d-198">這些條件包括：</span><span class="sxs-lookup"><span data-stu-id="b4a7d-198">These conditions are:</span></span>

-   <span data-ttu-id="b4a7d-199">應用程式是使用 Windows Installer 3.0 安裝的。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-199">The application was installed using Windows Installer 3.0.</span></span>
-   <span data-ttu-id="b4a7d-200">應用程式原本是依電腦安裝。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-200">The application was originally installed per-machine.</span></span>
-   <span data-ttu-id="b4a7d-201">應用程式是從卸載式媒體（例如 CD-ROM 或數位攝影機）安裝 (DVD) 。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-201">The application is installed from removable media, such a CD-ROM or digital video disc (DVD).</span></span>
-   <span data-ttu-id="b4a7d-202">修補程式是由原始安裝程式套件所識別的憑證進行數位簽署， ( .msi 檔案) 。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-202">The patches are digitally signed by a certificate that is identified by the original installer package (.msi file).</span></span>
-   <span data-ttu-id="b4a7d-203">修補程式可以針對數位簽章進行驗證。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-203">The patches can be validated against the digital signature.</span></span>
-   <span data-ttu-id="b4a7d-204">原始安裝程式套件尚未停用最低許可權的使用者帳戶修補。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-204">The original installer package has not disabled least-privileged user account patching.</span></span>
-   <span data-ttu-id="b4a7d-205">系統管理員未透過系統原則停用最低許可權的使用者帳戶修補。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-205">The system administrator has not disabled least-privileged user account patching via system policy.</span></span>

<span data-ttu-id="b4a7d-206">一般來說，最低許可權的使用者無法修改遊戲的程式檔。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-206">Normally, a least privileged user cannot modify a game's program files.</span></span> <span data-ttu-id="b4a7d-207">不過，當符合上述條件且已啟用 LUA 修補時，Windows Installer 可以更新遊戲的檔案，讓使用者取得最新的版本。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-207">However, when the above conditions are met and LUA patching is enabled, Windows Installer can update the game's files so that the user gets the latest version.</span></span>

> [!Note]  
> <span data-ttu-id="b4a7d-208">本文所包含的資訊與發行前版本的軟體產品相關，可能會在第一次商業發行之前大幅修改。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-208">The information contained in this article relates to pre-release software product, which may be substantially modified before its first commercial release.</span></span> <span data-ttu-id="b4a7d-209">因此，在第一次正式發行時，資訊可能無法正確描述或反映軟體產品。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-209">Accordingly, the information may not accurately describe or reflect the software product when first commercially released.</span></span> <span data-ttu-id="b4a7d-210">本文僅供參考之用，Microsoft 對於本文或其中包含的資訊不提供任何明示或默示的擔保。</span><span class="sxs-lookup"><span data-stu-id="b4a7d-210">This article is provided for informational purposes only, and Microsoft makes no warranties, express or implied, with respect to this article or the information contained in it.</span></span>

 

 

 