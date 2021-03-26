---
description: 系統會在使用者第一次登入電腦時建立使用者設定檔。 在後續的登入時，系統會載入使用者的設定檔，然後其他系統元件會根據設定檔中的資訊來設定使用者的環境。
title: 關於使用者設定檔
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 333f1861-91fe-4796-af13-dd300a5c6ec3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bafd5df7d59787104c2904b4e83c734deaf28708
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972081"
---
# <a name="about-user-profiles"></a><span data-ttu-id="8b074-104">關於使用者設定檔</span><span class="sxs-lookup"><span data-stu-id="8b074-104">About User Profiles</span></span>

<span data-ttu-id="8b074-105">系統會在使用者第一次登入電腦時建立使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="8b074-105">The system creates a user profile the first time that a user logs on to a computer.</span></span> <span data-ttu-id="8b074-106">在後續的登入時，系統會載入使用者的設定檔，然後其他系統元件會根據設定檔中的資訊來設定使用者的環境。</span><span class="sxs-lookup"><span data-stu-id="8b074-106">At subsequent logons, the system loads the user's profile, and then other system components configure the user's environment according to the information in the profile.</span></span>

## <a name="types-of-user-profiles"></a><span data-ttu-id="8b074-107">使用者設定檔的類型</span><span class="sxs-lookup"><span data-stu-id="8b074-107">Types of User Profiles</span></span>

-   <span data-ttu-id="8b074-108">[本機使用者設定檔](local-user-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="8b074-108">[Local User Profiles](local-user-profiles.md).</span></span> <span data-ttu-id="8b074-109">使用者第一次登入電腦時，會建立本機使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="8b074-109">A local user profile is created the first time that a user logs on to a computer.</span></span> <span data-ttu-id="8b074-110">設定檔會儲存在電腦的本機硬碟上。</span><span class="sxs-lookup"><span data-stu-id="8b074-110">The profile is stored on the computer's local hard disk.</span></span> <span data-ttu-id="8b074-111">對本機使用者設定檔所做的變更，對使用者以及進行變更的電腦而言是特定的。</span><span class="sxs-lookup"><span data-stu-id="8b074-111">Changes made to the local user profile are specific to the user and to the computer on which the changes are made.</span></span>
-   <span data-ttu-id="8b074-112">[漫遊使用者設定檔](roaming-user-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="8b074-112">[Roaming User Profiles](roaming-user-profiles.md).</span></span> <span data-ttu-id="8b074-113">漫遊使用者設定檔是複製到伺服器共用並儲存在伺服器共用上的本機設定檔複本。</span><span class="sxs-lookup"><span data-stu-id="8b074-113">A roaming user profile is a copy of the local profile that is copied to, and stored on, a server share.</span></span> <span data-ttu-id="8b074-114">此設定檔會下載到使用者登入網路的任何電腦上。</span><span class="sxs-lookup"><span data-stu-id="8b074-114">This profile is downloaded to any computer that a user logs onto on a network.</span></span> <span data-ttu-id="8b074-115">當使用者登出時，對漫遊使用者設定檔所做的變更會與設定檔的伺服器複本進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="8b074-115">Changes made to a roaming user profile are synchronized with the server copy of the profile when the user logs off.</span></span> <span data-ttu-id="8b074-116">漫遊使用者設定檔的優點是，使用者不需要在網路上所使用的每部電腦上建立設定檔。</span><span class="sxs-lookup"><span data-stu-id="8b074-116">The advantage of roaming user profiles is that users do not need to create a profile on each computer they use on a network.</span></span>
-   <span data-ttu-id="8b074-117">[強制使用者設定檔](mandatory-user-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="8b074-117">[Mandatory User Profiles](mandatory-user-profiles.md).</span></span> <span data-ttu-id="8b074-118">強制使用者設定檔是一種配置檔案類型，可供系統管理員用來指定使用者的設定。</span><span class="sxs-lookup"><span data-stu-id="8b074-118">A mandatory user profile is a type of profile that administrators can use to specify settings for users.</span></span> <span data-ttu-id="8b074-119">只有系統管理員可以對強制使用者設定檔進行變更。</span><span class="sxs-lookup"><span data-stu-id="8b074-119">Only system administrators can make changes to mandatory user profiles.</span></span> <span data-ttu-id="8b074-120">使用者登出時，使用者對桌面設定所做的變更會遺失。</span><span class="sxs-lookup"><span data-stu-id="8b074-120">Changes made by users to desktop settings are lost when the user logs off.</span></span>
-   <span data-ttu-id="8b074-121">[暫時使用者設定檔](temporary-user-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="8b074-121">[Temporary User Profiles](temporary-user-profiles.md).</span></span> <span data-ttu-id="8b074-122">每次發生錯誤情況時，就會發出暫存設定檔，以防止使用者的設定檔載入。</span><span class="sxs-lookup"><span data-stu-id="8b074-122">A temporary profile is issued each time that an error condition prevents the user's profile from loading.</span></span> <span data-ttu-id="8b074-123">暫時設定檔會在每個會話結束時刪除，而使用者對桌面設定和檔案所做的變更會在使用者登出時遺失。</span><span class="sxs-lookup"><span data-stu-id="8b074-123">Temporary profiles are deleted at the end of each session, and changes made by the user to desktop settings and files are lost when the user logs off.</span></span> <span data-ttu-id="8b074-124">只有在執行 Windows 2000 和更新版本的電腦上才能使用暫存設定檔。</span><span class="sxs-lookup"><span data-stu-id="8b074-124">Temporary profiles are only available on computers running Windows 2000 and later.</span></span>

<span data-ttu-id="8b074-125">使用者設定檔是由下列元素所組成：</span><span class="sxs-lookup"><span data-stu-id="8b074-125">A user profile consists of the following elements:</span></span>

-   <span data-ttu-id="8b074-126">登錄 hive。</span><span class="sxs-lookup"><span data-stu-id="8b074-126">A registry hive.</span></span> <span data-ttu-id="8b074-127">登錄 hive 是 Ntuser.man 檔案。</span><span class="sxs-lookup"><span data-stu-id="8b074-127">The registry hive is the file NTuser.dat.</span></span> <span data-ttu-id="8b074-128">系統會在使用者登入時載入 hive，並將其對應至 **HKEY \_ CURRENT \_ user** 登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="8b074-128">The hive is loaded by the system at user logon, and it is mapped to the **HKEY\_CURRENT\_USER** registry key.</span></span> <span data-ttu-id="8b074-129">使用者的登錄 hive 會維護使用者以登錄為基礎的喜好設定和設定。</span><span class="sxs-lookup"><span data-stu-id="8b074-129">The user's registry hive maintains the user's registry-based preferences and configuration.</span></span>
-   <span data-ttu-id="8b074-130">儲存在檔案系統中的一組設定檔資料夾。</span><span class="sxs-lookup"><span data-stu-id="8b074-130">A set of profile folders stored in the file system.</span></span> <span data-ttu-id="8b074-131">使用者設定檔是以每個使用者為基礎的資料夾來儲存在 **配置** 檔目錄中。</span><span class="sxs-lookup"><span data-stu-id="8b074-131">User-profile files are stored in the **Profiles** directory, on a folder per-user basis.</span></span> <span data-ttu-id="8b074-132">使用者設定檔資料夾是應用程式和其他系統元件的容器，可填入子資料夾和個別使用者資料，例如檔和設定檔案。</span><span class="sxs-lookup"><span data-stu-id="8b074-132">The user-profile folder is a container for applications and other system components to populate with sub-folders, and per-user data such as documents and configuration files.</span></span> <span data-ttu-id="8b074-133">Windows 檔案總管將使用者設定檔資料夾廣泛使用於使用者的桌面、[ **開始** ] 功能表和 [ **檔** ] 資料夾等專案。</span><span class="sxs-lookup"><span data-stu-id="8b074-133">Windows Explorer uses the user-profile folders extensively for such items as the user's Desktop, **Start** menu and **Documents** folder.</span></span>

<span data-ttu-id="8b074-134">使用者設定檔提供下列優點：</span><span class="sxs-lookup"><span data-stu-id="8b074-134">User profiles provide the following advantages:</span></span>

-   <span data-ttu-id="8b074-135">當使用者登入電腦時，系統會使用使用者上次登出時所使用的相同設定。</span><span class="sxs-lookup"><span data-stu-id="8b074-135">When the user logs on to a computer, the system uses the same settings that were in use when the user last logged off.</span></span>
-   <span data-ttu-id="8b074-136">與其他使用者共用電腦時，每位使用者在登入後都會收到他們自訂的桌面。</span><span class="sxs-lookup"><span data-stu-id="8b074-136">When sharing a computer with other users, each user receives their customized desktop after logging on.</span></span>
-   <span data-ttu-id="8b074-137">使用者設定檔中的設定對每個使用者都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="8b074-137">Settings in the user profile are unique to each user.</span></span> <span data-ttu-id="8b074-138">其他使用者無法存取這些設定。</span><span class="sxs-lookup"><span data-stu-id="8b074-138">The settings cannot be accessed by other users.</span></span> <span data-ttu-id="8b074-139">對某個使用者設定檔所做的變更不會影響其他使用者或其他使用者的設定檔。</span><span class="sxs-lookup"><span data-stu-id="8b074-139">Changes made to one user's profile do not affect other users or other users' profiles.</span></span>

## <a name="user-profile-tiles-in-windows-7-and-later"></a><span data-ttu-id="8b074-140">Windows 7 和更新版本中的使用者設定檔磚</span><span class="sxs-lookup"><span data-stu-id="8b074-140">User Profile Tiles in Windows 7 and Later</span></span>

<span data-ttu-id="8b074-141">在 Windows 7 或更新版本中，每個使用者設定檔都有相關聯的影像顯示為使用者磚。</span><span class="sxs-lookup"><span data-stu-id="8b074-141">In Windows 7 or later, each user profile has an associated image presented as a user tile.</span></span> <span data-ttu-id="8b074-142">這些磚會顯示在 **使用者帳戶的 [使用者帳戶** ] 主控台專案和其 [ **管理帳戶** ] 子頁面上。</span><span class="sxs-lookup"><span data-stu-id="8b074-142">These tiles appear to users on the **User Accounts** Control Panel item and its **Manage Accounts** subpage..</span></span> <span data-ttu-id="8b074-143">如果您有系統管理員存取權限，預設的 Guest 和預設使用者帳戶的影像檔案也會出現在這裡。</span><span class="sxs-lookup"><span data-stu-id="8b074-143">The image files for the default Guest and default User accounts also appear here if you have Administrator access rights.</span></span>

> [!Note]  
> <span data-ttu-id="8b074-144">您可以透過 [**使用者帳戶**] 主控台專案中的 [**管理其他帳戶**] 連結來存取 [**管理帳戶**] 子頁面。</span><span class="sxs-lookup"><span data-stu-id="8b074-144">The **Manage Accounts** subpage is accessed through the **Manage another account** link in the **User Accounts** Control Panel item.</span></span>

 

-   <span data-ttu-id="8b074-145">% ProgramData% \\ Microsoft \\ 使用者帳戶圖片 \\Guest.bmp</span><span class="sxs-lookup"><span data-stu-id="8b074-145">%ProgramData%\\Microsoft\\User Account Pictures\\Guest.bmp</span></span>
-   <span data-ttu-id="8b074-146">% ProgramData% \\ Microsoft \\ 使用者帳戶圖片 \\User.bmp</span><span class="sxs-lookup"><span data-stu-id="8b074-146">%ProgramData%\\Microsoft\\User Account Pictures\\User.bmp</span></span>

<span data-ttu-id="8b074-147">使用者的磚影像會儲存在% SystemDrive% \\ Users \\ <username> \\ AppData \\ 本機 \\ Temp 資料夾中，以 <username> .bmp 形式儲存。</span><span class="sxs-lookup"><span data-stu-id="8b074-147">The user's tile image is stored in the %SystemDrive%\\Users\\<username>\\AppData\\Local\\Temp folder as <username>.bmp.</span></span> <span data-ttu-id="8b074-148"> () 的任何斜線字元 \\ 都會轉換成加號字元 (+) 。</span><span class="sxs-lookup"><span data-stu-id="8b074-148">Any slash characters (\\) are converted to plus sign characters (+).</span></span> <span data-ttu-id="8b074-149">例如，網域 \\ 使用者會轉換成網域 + 使用者。</span><span class="sxs-lookup"><span data-stu-id="8b074-149">For example, DOMAIN\\user is converted to DOMAIN+user.</span></span>

<span data-ttu-id="8b074-150">影像檔會出現在使用者的 **Temp** 資料夾中：</span><span class="sxs-lookup"><span data-stu-id="8b074-150">The image file appears in the user's **Temp** folder:</span></span>

-   <span data-ttu-id="8b074-151">使用者完成初始系統設定之後 (OOBE) 。</span><span class="sxs-lookup"><span data-stu-id="8b074-151">After the user completes the initial system setup (OOBE).</span></span>
-   <span data-ttu-id="8b074-152">當使用者第一次啟動主控台專案的 **使用者帳戶** 時。</span><span class="sxs-lookup"><span data-stu-id="8b074-152">When the user first launches the **User Accounts** Control Panel item.</span></span>
-   <span data-ttu-id="8b074-153">當使用者移至 **使用者帳戶** 的 [**管理帳戶**] 子頁面時主控台專案。</span><span class="sxs-lookup"><span data-stu-id="8b074-153">When the user goes to the **Manage Accounts** subpage of the **User Accounts** Control Panel item.</span></span> <span data-ttu-id="8b074-154">此外，也會顯示電腦上所有其他使用者的磚。</span><span class="sxs-lookup"><span data-stu-id="8b074-154">In addition, tiles for all other users on the computer are shown.</span></span>

<span data-ttu-id="8b074-155">這些實例是建立或更新映射的唯一時間。</span><span class="sxs-lookup"><span data-stu-id="8b074-155">Those instances are the only times that the images are created or updated.</span></span> <span data-ttu-id="8b074-156">因此，以程式設計方式使用 **暫存** 資料夾位置時，請注意下列幾點：</span><span class="sxs-lookup"><span data-stu-id="8b074-156">Therefore, there are several caveats to keep in mind when using the **Temp** folder location programmatically:</span></span>

1.  <span data-ttu-id="8b074-157">使用者的磚不保證存在。</span><span class="sxs-lookup"><span data-stu-id="8b074-157">The user's tile is not guaranteed to be present.</span></span> <span data-ttu-id="8b074-158">如果使用者以手動方式或透過刪除暫存檔案的公用程式來刪除 .bmp 檔，則在使用者啟動 **使用者帳戶** 主控台專案或 **管理帳戶** 子頁面之前，不會自動重新建立該使用者磚。</span><span class="sxs-lookup"><span data-stu-id="8b074-158">If the user deletes the .bmp file, for instance manually or through a utility that deletes temporary files, that user tile is not automatically recreated until the user launches the **User Accounts** Control Panel item or **Manage Accounts** subpage.</span></span>

2.  <span data-ttu-id="8b074-159">電腦上其他使用者的使用者磚可能不會出現在目前登入使用者的 **Temp** 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="8b074-159">User tiles for other users on the computer might not be present in the currently logged-on user's **Temp** folder.</span></span> <span data-ttu-id="8b074-160">例如，如果使用者 A 透過 **使用者帳戶** 主控台專案建立使用者 b，當 Windows 將使用者 a 傳送至 [**管理帳戶**] 子頁面時，使用者 b 的磚就會建立在使用者的 **Temp** 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="8b074-160">For example, if User A creates User B through the **User Accounts** Control Panel item, User B's tile is created in User A's **Temp** folder when Windows sends User A to the **Manage Accounts** subpage.</span></span> <span data-ttu-id="8b074-161">因為在登入之前，不會為使用者 B 建立目錄結構，所以使用者 A 的 **Temp** 資料夾是使用者 b 的磚的唯一儲存位置。</span><span class="sxs-lookup"><span data-stu-id="8b074-161">Because the directory structure is not created for User B until he or she logs on, User A's **Temp** folder is the only location that User B's tile is stored.</span></span> <span data-ttu-id="8b074-162">當使用者 B 登入時，儲存在使用者 B **暫存** 資料夾中的唯一影像就是他或她自己的映射。</span><span class="sxs-lookup"><span data-stu-id="8b074-162">When User B logs on, the only image stored in User B's **Temp** folder is his or her own.</span></span>

    1.  <span data-ttu-id="8b074-163">若要取得系統使用者的所有使用者磚，應用程式可能需要在每個使用者的 **暫存** 目錄中搜尋。</span><span class="sxs-lookup"><span data-stu-id="8b074-163">To get all user tiles for users on a system, applications might need to search in each user's **Temp** directory.</span></span>
    2.  <span data-ttu-id="8b074-164">由於存取控制清單 (ACL) 這些 **暫存** 目錄允許存取系統、系統管理員和目前的使用者，因此應用程式必須提升為其他使用者的存取權。</span><span class="sxs-lookup"><span data-stu-id="8b074-164">Because the access control list (ACL) of these **Temp** directories allows access to SYSTEM, Administrator, and the current user, applications need to elevate to access for other users.</span></span>

3.  <span data-ttu-id="8b074-165">在其 **暫存** 資料夾中，其他使用者的磚不保證處於最新狀態。</span><span class="sxs-lookup"><span data-stu-id="8b074-165">Other users' tiles are not guaranteed to be up-to-date in their **Temp** folders.</span></span> <span data-ttu-id="8b074-166">如果使用者 B 更新其使用者磚，使用者 A 將不會看到變更，直到使用者 A 存取 [ **管理帳戶** ] 子頁面為止。</span><span class="sxs-lookup"><span data-stu-id="8b074-166">If User B updates his or her user tile, User A will not see the change until User A accesses the **Manage Accounts** subpage.</span></span> <span data-ttu-id="8b074-167">因此，如果應用程式使用使用者 A 的 **暫存** 資料夾來取得使用者 B 的磚，則這些應用程式可能會取得過期的影像檔案。</span><span class="sxs-lookup"><span data-stu-id="8b074-167">Therefore, if applications use User A's **Temp** folder to obtain User B's tile, those applications can get an out-of-date image file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b074-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="8b074-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b074-169">本機使用者設定檔</span><span class="sxs-lookup"><span data-stu-id="8b074-169">Local User Profiles</span></span>](local-user-profiles.md)
</dt> <dt>

[<span data-ttu-id="8b074-170">漫遊使用者設定檔</span><span class="sxs-lookup"><span data-stu-id="8b074-170">Roaming User Profiles</span></span>](roaming-user-profiles.md)
</dt> <dt>

[<span data-ttu-id="8b074-171">強制使用者設定檔</span><span class="sxs-lookup"><span data-stu-id="8b074-171">Mandatory User Profiles</span></span>](mandatory-user-profiles.md)
</dt> <dt>

[<span data-ttu-id="8b074-172">暫存使用者設定檔</span><span class="sxs-lookup"><span data-stu-id="8b074-172">Temporary User Profiles</span></span>](temporary-user-profiles.md)
</dt> <dt>

[<span data-ttu-id="8b074-173">設定檔目錄</span><span class="sxs-lookup"><span data-stu-id="8b074-173">Profiles Directory</span></span>](profiles-directory.md)
</dt> <dt>

[<span data-ttu-id="8b074-174">使用者環境變數</span><span class="sxs-lookup"><span data-stu-id="8b074-174">User Environment Variables</span></span>](user-environment-variables.md)
</dt> <dt>

[<span data-ttu-id="8b074-175">快速切換使用者</span><span class="sxs-lookup"><span data-stu-id="8b074-175">Fast User Switching</span></span>](fast-user-switching.md)
</dt> </dl>

 

 



