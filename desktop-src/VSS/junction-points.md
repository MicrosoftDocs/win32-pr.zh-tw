---
description: 在 Windows Vista 和 Windows Server 2008 中，使用者資料和系統資料的預設位置已變更。
ms.assetid: 78679851-91f5-447f-8580-12cbf0323fb8
title: 連接點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57f1823c67e2c6b95ae366b7604054b47305062e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980803"
---
# <a name="junction-points"></a><span data-ttu-id="64dc9-103">連接點</span><span class="sxs-lookup"><span data-stu-id="64dc9-103">Junction Points</span></span>

<span data-ttu-id="64dc9-104">在 Windows Vista 和 Windows Server 2008 中，使用者資料和系統資料的預設位置已變更。</span><span class="sxs-lookup"><span data-stu-id="64dc9-104">In Windows Vista and Windows Server 2008, the default locations for user data and system data have changed.</span></span> <span data-ttu-id="64dc9-105">例如，先前儲存在% SystemDrive% Documents and Settings 目錄中的使用者資料， \\ 現在會儲存在% SystemDrive% \\ Users 目錄中。</span><span class="sxs-lookup"><span data-stu-id="64dc9-105">For example, user data that was previously stored in the %SystemDrive%\\Documents and Settings directory is now stored in the %SystemDrive%\\Users directory.</span></span> <span data-ttu-id="64dc9-106">為了回溯相容性，舊的位置具有指向新位置的連接點。</span><span class="sxs-lookup"><span data-stu-id="64dc9-106">For backward compatibility, the old locations have junction points that point to the new locations.</span></span> <span data-ttu-id="64dc9-107">例如，C： \\ Documents 和 Settings 現在是指向 C： Users 的連接點 \\ 。</span><span class="sxs-lookup"><span data-stu-id="64dc9-107">For example, C:\\Documents and Settings is now a junction point that points to C:\\Users.</span></span> <span data-ttu-id="64dc9-108">備份應用程式必須能夠備份和還原連接點。</span><span class="sxs-lookup"><span data-stu-id="64dc9-108">Backup applications must be capable of backing up and restoring junction points.</span></span>

<span data-ttu-id="64dc9-109">這些連接點可識別如下：</span><span class="sxs-lookup"><span data-stu-id="64dc9-109">These junction points can be identified as follows:</span></span>

-   <span data-ttu-id="64dc9-110">它們具有檔 \_ 屬性重新 \_ 分析 \_ 點、檔 \_ 屬性 \_ 隱藏，以及檔 \_ 屬性 \_ 系統檔案屬性設定。</span><span class="sxs-lookup"><span data-stu-id="64dc9-110">They have the FILE\_ATTRIBUTE\_REPARSE\_POINT, FILE\_ATTRIBUTE\_HIDDEN, and FILE\_ATTRIBUTE\_SYSTEM file attributes set.</span></span>
-   <span data-ttu-id="64dc9-111">它們也有 (Acl 的存取控制清單) 設定為拒絕所有人的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="64dc9-111">They also have their access control lists (ACLs) set to deny read access to everyone.</span></span>

<span data-ttu-id="64dc9-112">如果應用程式有必要的許可權，則呼叫特定路徑的應用程式可以跨越這些連接點。</span><span class="sxs-lookup"><span data-stu-id="64dc9-112">Applications that call out a specific path can traverse these junction points if they have the required permissions.</span></span> <span data-ttu-id="64dc9-113">不過，嘗試列舉連接點的內容將會導致失敗。</span><span class="sxs-lookup"><span data-stu-id="64dc9-113">However, attempts to enumerate the contents of the junction points will result in failures.</span></span> <span data-ttu-id="64dc9-114">備份應用程式不會跨越這些連接點，或嘗試在其下備份資料，原因有兩個：</span><span class="sxs-lookup"><span data-stu-id="64dc9-114">It is important that backup applications do not traverse these junction points, or attempt to backup data under them, for two reasons:</span></span>

-   <span data-ttu-id="64dc9-115">這樣做可能會導致備份應用程式多次備份相同的資料。</span><span class="sxs-lookup"><span data-stu-id="64dc9-115">Doing so can cause the backup application to back up the same data more than once.</span></span>
-   <span data-ttu-id="64dc9-116">它也可能會導致迴圈參考)  (迴圈。</span><span class="sxs-lookup"><span data-stu-id="64dc9-116">It can also lead to cycles (circular references).</span></span>

## <a name="per-user-junctions-and-system-junctions"></a><span data-ttu-id="64dc9-117">Per-User 接合和系統接合</span><span class="sxs-lookup"><span data-stu-id="64dc9-117">Per-User Junctions and System Junctions</span></span>

<span data-ttu-id="64dc9-118">在 Windows Vista 和 Windows Server 2008 中用來提供檔案和登錄虛擬化的連接點可以分為兩個類別：每個使用者的連接和系統連接。</span><span class="sxs-lookup"><span data-stu-id="64dc9-118">The junction points that are used to provide file and registry virtualization in Windows Vista and Windows Server 2008 can be divided into two classes: per-user junctions and system junctions.</span></span>

<span data-ttu-id="64dc9-119">每個使用者的連接都會建立在每個個別使用者的設定檔內，以提供使用者應用程式的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="64dc9-119">Per-user junctions are created inside each individual user's profile to provide backward compatibility for user applications.</span></span> <span data-ttu-id="64dc9-120">位於 C： \\ users 使用者名稱的連接點 \\  \\ 我的檔指向 C： \\ 使用者使用者 \\ *名稱* \\ 檔是每個使用者的連接點範例。</span><span class="sxs-lookup"><span data-stu-id="64dc9-120">The junction point at C:\\Users\\*username*\\My Documents that points to C:\\Users\\*username*\\Documents is an example of a per-user junction.</span></span> <span data-ttu-id="64dc9-121">建立使用者設定檔時，設定檔服務會建立每位使用者的連接。</span><span class="sxs-lookup"><span data-stu-id="64dc9-121">Per-user junctions are created by the Profile service when the user's profile is created.</span></span>

<span data-ttu-id="64dc9-122">其他連接是不位於使用者使用者名稱目錄下的系統連接 \\  。</span><span class="sxs-lookup"><span data-stu-id="64dc9-122">The other junctions are system junctions that do not reside under the Users\\*username* directory.</span></span> <span data-ttu-id="64dc9-123">系統接合的範例包括：</span><span class="sxs-lookup"><span data-stu-id="64dc9-123">Examples of system junctions include:</span></span>

-   <span data-ttu-id="64dc9-124">檔和設定</span><span class="sxs-lookup"><span data-stu-id="64dc9-124">Documents and Settings</span></span>
-   <span data-ttu-id="64dc9-125">所有使用者、公用和預設使用者設定檔中的連接</span><span class="sxs-lookup"><span data-stu-id="64dc9-125">Junctions within the All Users, Public, and Default User profiles</span></span>

<span data-ttu-id="64dc9-126">系統連接是由 Windows 歡迎使用 (（也稱為「電腦現成體驗」或 mOOBE) ）所叫用的 userenv.dll 所建立。</span><span class="sxs-lookup"><span data-stu-id="64dc9-126">System junctions are created by userenv.dll when it is invoked by Windows Welcome (also called the machine out-of-box-experience, or mOOBE).</span></span>

> [!Note]  
> <span data-ttu-id="64dc9-127">如果使用者將系統語言變更為英文以外的語言，則會以當地語系化名稱建立每位使用者和系統連接點。</span><span class="sxs-lookup"><span data-stu-id="64dc9-127">If the user changes the system language to a language other than English, the per-user and system junction points will be created with localized names.</span></span>

 

 

 



