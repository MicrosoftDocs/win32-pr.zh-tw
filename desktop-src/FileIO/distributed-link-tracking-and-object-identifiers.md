---
description: 分散式連結追蹤服務可讓用戶端應用程式追蹤已移動的連結來源。
ms.assetid: 6f438c72-f23d-4ca4-83bd-fe3bc433ceeb
title: 分散式連結追蹤和物件識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d28e151c21fd5320a41950be7647c1e8e0a88b
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "106975646"
---
# <a name="distributed-link-tracking-and-object-identifiers"></a><span data-ttu-id="68647-103">分散式連結追蹤和物件識別碼</span><span class="sxs-lookup"><span data-stu-id="68647-103">Distributed Link Tracking and Object Identifiers</span></span>

<span data-ttu-id="68647-104">使用路徑和檔案名儲存檔案或目錄的參考並不可靠。</span><span class="sxs-lookup"><span data-stu-id="68647-104">Storing a reference to a file or directory by using its path and file name is not reliable.</span></span> <span data-ttu-id="68647-105">如果使用者重新命名檔案，則會中斷檔案的連結。</span><span class="sxs-lookup"><span data-stu-id="68647-105">If a user renames a file, it breaks the links to the file.</span></span> <span data-ttu-id="68647-106">如果使用者重新命名目錄，它會中斷檔案的連結，以及目錄樹狀結構中的所有檔案和子目錄。</span><span class="sxs-lookup"><span data-stu-id="68647-106">If a user renames the directory, it breaks the links to the file, and all files and subdirectories in the directory tree.</span></span>

<span data-ttu-id="68647-107">**分散式連結追蹤服務** 可讓用戶端應用程式追蹤已移動的連結來源。</span><span class="sxs-lookup"><span data-stu-id="68647-107">The **distributed link tracking service** enables client applications to track link sources that have moved.</span></span> <span data-ttu-id="68647-108">訂閱連結追蹤服務的用戶端可以維持其參考的完整性，並以對使用者而言是透明的方式來追蹤物件。</span><span class="sxs-lookup"><span data-stu-id="68647-108">Clients that subscribe to the link tracking service can maintain the integrity of their references, and the objects can be tracked in a way that is transparent to the user.</span></span>

## <a name="object-identifiers"></a><span data-ttu-id="68647-109">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="68647-109">Object Identifiers</span></span>

<span data-ttu-id="68647-110">連結追蹤服務會使用 **物件識別碼 (識別碼)** 來維護物件的連結。</span><span class="sxs-lookup"><span data-stu-id="68647-110">The link tracking service maintains its link to an object by using an **object identifier (ID)**.</span></span> <span data-ttu-id="68647-111">物件識別碼是選擇性的屬性，可唯一識別磁片區上的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="68647-111">An object ID is an optional attribute that uniquely identifies a file or directory on a volume.</span></span>

<span data-ttu-id="68647-112">所有物件識別碼的索引都會儲存在磁片區上。</span><span class="sxs-lookup"><span data-stu-id="68647-112">An index of all object IDs is stored on the volume.</span></span> <span data-ttu-id="68647-113">重新命名、備份和還原作業會保留物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="68647-113">Rename, backup, and restore operations preserve object IDs.</span></span> <span data-ttu-id="68647-114">不過，複製作業並不會保留物件識別碼，因為這樣會違反其唯一性。</span><span class="sxs-lookup"><span data-stu-id="68647-114">However, copy operations do not preserve object IDs, because that would violate their uniqueness.</span></span>

<span data-ttu-id="68647-115">您可以對物件識別碼執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="68647-115">You can perform the following operations on object IDs:</span></span>

-   <span data-ttu-id="68647-116">建立</span><span class="sxs-lookup"><span data-stu-id="68647-116">Creation</span></span>
-   <span data-ttu-id="68647-117">刪除</span><span class="sxs-lookup"><span data-stu-id="68647-117">Deletion</span></span>
-   <span data-ttu-id="68647-118">查詢</span><span class="sxs-lookup"><span data-stu-id="68647-118">Query</span></span>

<span data-ttu-id="68647-119">當您建立物件識別碼時，您會建立連結追蹤服務的檔案身分識別。</span><span class="sxs-lookup"><span data-stu-id="68647-119">When you create an object ID, you establish the identity of the file to the link tracking service.</span></span> <span data-ttu-id="68647-120">相反地，當您刪除物件識別碼時，連結追蹤服務會停止維護檔案的連結。</span><span class="sxs-lookup"><span data-stu-id="68647-120">Conversely, when you delete an object ID, the link tracking service stops maintaining links to the file.</span></span> <span data-ttu-id="68647-121">如需對物件識別碼執行作業的檔案系統控制程式代碼清單，請參閱檔案 [管理控制程式代碼](file-management-control-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="68647-121">For a list of the file system control codes that perform operations on object IDs, see [File Management Control Codes](file-management-control-codes.md).</span></span>

<span data-ttu-id="68647-122">分散式連結追蹤服務會追蹤 shell 快捷方式的連結來源，以及 NTFS 檔案系統磁片區中的 OLE 連結。</span><span class="sxs-lookup"><span data-stu-id="68647-122">The distributed link tracking service tracks link sources for shell shortcuts and OLE links within NTFS file system volumes.</span></span> <span data-ttu-id="68647-123">連結用戶端可以修正中斷的連結，其中包含連結來源新位置的更新資訊。</span><span class="sxs-lookup"><span data-stu-id="68647-123">The link client can fix a broken link with updated information on the new location of the link source.</span></span>

## <a name="link-tracking-features"></a><span data-ttu-id="68647-124">連結追蹤功能</span><span class="sxs-lookup"><span data-stu-id="68647-124">Link Tracking Features</span></span>

<span data-ttu-id="68647-125">Shell 快速鍵包含使用樹狀目錄搜尋演算法的啟發式連結追蹤，以找出與移動的連結來源相符的結果。</span><span class="sxs-lookup"><span data-stu-id="68647-125">Shell shortcuts include heuristic link tracking that uses a tree search algorithm to find a match for a moved link source.</span></span> <span data-ttu-id="68647-126">搜尋演算法是根據檔案的最後一個已知路徑，以及包含建立日期、檔案大小和檔案名與副檔名的檔案資訊。</span><span class="sxs-lookup"><span data-stu-id="68647-126">The search algorithm is based on the last known path of the file and file information that includes the creation date, file size, and file name and extension.</span></span>

<span data-ttu-id="68647-127">OLE 連結包含相同的啟發式連結追蹤。</span><span class="sxs-lookup"><span data-stu-id="68647-127">OLE linking includes the same heuristic link tracking.</span></span> <span data-ttu-id="68647-128">Windows 也包含相同的啟發式連結追蹤，其中包含一些增強的功能，可讓您在某些常見的案例中，搜尋命名空間來產生結果。</span><span class="sxs-lookup"><span data-stu-id="68647-128">Windows also includes the same heuristic link tracking with some added improvements for searching name spaces to yield results in some common scenarios.</span></span> <span data-ttu-id="68647-129">這些增強功能包括下列程式，取決於用戶端應用程式所加諸的時間限制。</span><span class="sxs-lookup"><span data-stu-id="68647-129">The improvements include the following procedure that depends on time limits imposed by an client application.</span></span>

<span data-ttu-id="68647-130">**搜尋命名空間**</span><span class="sxs-lookup"><span data-stu-id="68647-130">**To search for name spaces**</span></span>

1.  <span data-ttu-id="68647-131">從最後一個目錄搜尋四個目錄層級。</span><span class="sxs-lookup"><span data-stu-id="68647-131">Search four directory levels down from the last directory.</span></span>
2.  <span data-ttu-id="68647-132">向上移動一個目錄，然後重複步驟1和2，這三次可能會產生結果（如果物件已移到附近）。</span><span class="sxs-lookup"><span data-stu-id="68647-132">Move up one directory and repeat steps 1 and 2 another three times, which can yield results if the object has moved nearby.</span></span>
3.  <span data-ttu-id="68647-133">從桌面根目錄向下搜尋四個層級，如果物件已移至相同桌面上的位置，則會產生結果。</span><span class="sxs-lookup"><span data-stu-id="68647-133">Search four levels down from the desktop root, which can yield results if the object has moved to a location on the same desktop.</span></span>
4.  <span data-ttu-id="68647-134">從每個本機固定磁片磁碟機上的根目錄搜尋四個層級。</span><span class="sxs-lookup"><span data-stu-id="68647-134">Search four levels down from the root on each local fixed drive.</span></span>
5.  <span data-ttu-id="68647-135">重複步驟1-3，而不包含四個目錄限制。</span><span class="sxs-lookup"><span data-stu-id="68647-135">Repeat steps 1-3 without the four directory limit.</span></span>

> [!Note]  
> <span data-ttu-id="68647-136">這些連結追蹤配置對終端使用者而言是透明的。</span><span class="sxs-lookup"><span data-stu-id="68647-136">These link tracking schemes are transparent to the end-user.</span></span> <span data-ttu-id="68647-137">不過，它們不一定會產生正面的結果，而且可能相當耗時。</span><span class="sxs-lookup"><span data-stu-id="68647-137">However, they do not always yield positive results, and can be time consuming.</span></span>

 

<span data-ttu-id="68647-138">如需有關 shell 快速鍵的詳細資訊，請參閱 [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka)。</span><span class="sxs-lookup"><span data-stu-id="68647-138">For more information about shell shortcuts, see [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka).</span></span>

<span data-ttu-id="68647-139">如需 OLE 連結的詳細資訊，請參閱 [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink)。</span><span class="sxs-lookup"><span data-stu-id="68647-139">For more information about OLE links, see [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink).</span></span>

<span data-ttu-id="68647-140">如果在 NTFS 3.0 或更新版本上對檔案進行連結，而檔案移至相同網域中具有 NTFS 3.0 或更新版本的任何其他磁片區，則追蹤服務可以找到該檔案，但受限於時間考慮。</span><span class="sxs-lookup"><span data-stu-id="68647-140">If a link is made to a file on NTFS 3.0 or later, and the file is moved to any other volume with NTFS 3.0 or later within the same domain, the file can be found by the tracking service, subject to time considerations.</span></span> <span data-ttu-id="68647-141">此外，如果檔案是移至網域或工作組內，則會找到該檔案。</span><span class="sxs-lookup"><span data-stu-id="68647-141">Additionally, if the file is moved outside the domain or within a workgroup, it is found.</span></span>

<span data-ttu-id="68647-142">若要取得 NTFS 版本的磁片區，請使用系統管理員存取權限開啟命令提示字元，然後執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="68647-142">To obtain the NTFS version of a volume, open a command prompt with Administrator access rights and execute the following command:</span></span>

<span data-ttu-id="68647-143">**fsutil fsinfo ntfsinfo** \*X \*\* \* *：*</span><span class="sxs-lookup"><span data-stu-id="68647-143">**fsutil fsinfo ntfsinfo** *X\*\*\*:*\*</span></span>

<span data-ttu-id="68647-144">其中 *X* 是磁片區的磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="68647-144">where *X* is the drive letter of the volume.</span></span>

<span data-ttu-id="68647-145">在檔案中建立連結時，會將目標檔案視為 **連結來源**，而連結的建立者會是 **連結用戶端**。</span><span class="sxs-lookup"><span data-stu-id="68647-145">When a link is created to a file, the target file is considered the **link source**, and the creator of the link is the **link client**.</span></span> <span data-ttu-id="68647-146">例如，如果建立了 shell 快捷方式來連結到文字檔，則文字檔是連結來源，而 shell 快捷方式是連結用戶端。</span><span class="sxs-lookup"><span data-stu-id="68647-146">For example, if a shell shortcut is created to link to a text document, the text document is the link source, and the shell shortcut is the link client.</span></span>

<span data-ttu-id="68647-147">分散式連結追蹤服務會在網域內發生的下列情況中維護檔案連結：</span><span class="sxs-lookup"><span data-stu-id="68647-147">The distributed link tracking service maintains file links for the following situations that occur within a domain:</span></span>

-   <span data-ttu-id="68647-148">連結來源檔案會從一個 NTFS 檔案系統磁片區移至相同網域中的另一個磁片區。</span><span class="sxs-lookup"><span data-stu-id="68647-148">The link source file is moved from one NTFS file system volume to another within the same domain.</span></span>
-   <span data-ttu-id="68647-149">保存連結來源的電腦名稱稱已重新命名。</span><span class="sxs-lookup"><span data-stu-id="68647-149">The name of the computer that holds the link source is renamed.</span></span>
-   <span data-ttu-id="68647-150">連結來源電腦上的網路共用已變更。</span><span class="sxs-lookup"><span data-stu-id="68647-150">The network shares on the link source computer are changed.</span></span>
-   <span data-ttu-id="68647-151">保存連結來源檔案的磁片區會移至相同網域中的另一部電腦。</span><span class="sxs-lookup"><span data-stu-id="68647-151">The volume that holds the link source file is moved to another computer within the same domain.</span></span>

<span data-ttu-id="68647-152">分散式連結追蹤服務也會嘗試在先前的情況下維持連結，即使它們不是在網域內（也就是跨網域或工作組內）也不會發生。</span><span class="sxs-lookup"><span data-stu-id="68647-152">The distributed link tracking service also attempts to maintain links in the preceding situations even when they do not occur within a domain, that is, they are cross domain or within a workgroup.</span></span> <span data-ttu-id="68647-153">連結來源電腦上的網路共用變更時，一律可以在這些情況下維護連結。</span><span class="sxs-lookup"><span data-stu-id="68647-153">Links can always be maintained in these situations when the network share on the link source computer is changed.</span></span> <span data-ttu-id="68647-154">當連結來源在電腦內移動時，也可以進行維護。</span><span class="sxs-lookup"><span data-stu-id="68647-154">They can also be maintained when a link source is moved within a computer.</span></span> <span data-ttu-id="68647-155">連結來源移至另一部電腦時，通常可以維持連結，但是這種形式的追蹤在一段時間內會較不可靠。</span><span class="sxs-lookup"><span data-stu-id="68647-155">Links can usually be maintained when the link source is moved to another computer, but this form of tracking is less reliable over time.</span></span>

## <a name="link-tracking-functionality"></a><span data-ttu-id="68647-156">連結追蹤功能</span><span class="sxs-lookup"><span data-stu-id="68647-156">Link Tracking Functionality</span></span>

<span data-ttu-id="68647-157">連結追蹤功能主要是以下列兩個系統服務的形式來執行：</span><span class="sxs-lookup"><span data-stu-id="68647-157">Link tracking functionality is primarily implemented in the form of the following two system services:</span></span>

-   <span data-ttu-id="68647-158">散佈式連結追蹤用戶端</span><span class="sxs-lookup"><span data-stu-id="68647-158">Distributed Link Tracking Client</span></span>
-   <span data-ttu-id="68647-159">分散式連結追蹤伺服器</span><span class="sxs-lookup"><span data-stu-id="68647-159">Distributed Link Tracking Server</span></span>

<dl> <dt>

<span data-ttu-id="68647-160"><span id="Distributed_Link_Tracking_Client"></span><span id="distributed_link_tracking_client"></span><span id="DISTRIBUTED_LINK_TRACKING_CLIENT"></span>分散式連結追蹤用戶端</span><span class="sxs-lookup"><span data-stu-id="68647-160"><span id="Distributed_Link_Tracking_Client"></span><span id="distributed_link_tracking_client"></span><span id="DISTRIBUTED_LINK_TRACKING_CLIENT"></span>Distributed Link Tracking Client</span></span>
</dt> <dd>

<span data-ttu-id="68647-161">分散式連結追蹤用戶端會在所有電腦上執行，並管理該電腦的連結追蹤活動。</span><span class="sxs-lookup"><span data-stu-id="68647-161">The distributed link tracking client runs on all computers, and manages the link tracking activities for that computer.</span></span> <span data-ttu-id="68647-162">這些活動包括搜尋連結來源和處理連結來源移動。</span><span class="sxs-lookup"><span data-stu-id="68647-162">These activities include searching for link sources and processing link source moves.</span></span> <span data-ttu-id="68647-163">手機連結來源之後，服務會將資訊傳遞至在網域控制站上執行的分散式連結追蹤伺服器。</span><span class="sxs-lookup"><span data-stu-id="68647-163">When a link source is moved, the service passes information to the distributed link tracking server that runs on domain controllers.</span></span>

</dd> <dt>

<span data-ttu-id="68647-164"><span id="Distributed_Link_Tracking_Server"></span><span id="distributed_link_tracking_server"></span><span id="DISTRIBUTED_LINK_TRACKING_SERVER"></span>分散式連結追蹤伺服器</span><span class="sxs-lookup"><span data-stu-id="68647-164"><span id="Distributed_Link_Tracking_Server"></span><span id="distributed_link_tracking_server"></span><span id="DISTRIBUTED_LINK_TRACKING_SERVER"></span>Distributed Link Tracking Server</span></span>
</dt> <dd>

<span data-ttu-id="68647-165">分散式連結追蹤伺服器會在網域中的每個網域控制站上執行。</span><span class="sxs-lookup"><span data-stu-id="68647-165">The distributed link tracking server runs on each domain controller in a domain.</span></span> <span data-ttu-id="68647-166">服務會接受從電腦上的追蹤服務移動檔案和磁片區的通知，並允許分散式連結追蹤用戶端查詢連結來源的目前位置。</span><span class="sxs-lookup"><span data-stu-id="68647-166">The service accepts notifications of file and volume moves from the tracking service on a computer, and allows the distributed link tracking client to query the current location of a link source.</span></span>

<span data-ttu-id="68647-167">此伺服器服務會在網域控制站中維護已移動之磁片區和檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="68647-167">This server service maintains information in the domain controllers about volumes and files that have been moved.</span></span> <span data-ttu-id="68647-168">移動的相關資訊不能增加超過特定大小，並且會在不必要的情況下自動移除。</span><span class="sxs-lookup"><span data-stu-id="68647-168">The information about moves cannot increase beyond a specific size, and it is automatically removed if it becomes unnecessary.</span></span>

</dd> </dl>

<span data-ttu-id="68647-169">連結追蹤服務是由 [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka) 和 [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink) 介面所公開。</span><span class="sxs-lookup"><span data-stu-id="68647-169">The link tracking services are exposed by the [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka) and [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink) interfaces.</span></span> <span data-ttu-id="68647-170">因此，shell 快捷方式會使用它們。</span><span class="sxs-lookup"><span data-stu-id="68647-170">Therefore, they are used by shell shortcuts.</span></span> <span data-ttu-id="68647-171">當呼叫 [**IShellLink：： Resolve**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) 方法且找不到參照檔案時（例如，當使用者啟動 shell 快捷方式時），系統會自動呼叫追蹤服務來尋找檔案。</span><span class="sxs-lookup"><span data-stu-id="68647-171">When the [**IShellLink::Resolve**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) method is called and the referent file cannot be found, for example, when the user activates a shell shortcut, the tracking service is called automatically to find the file.</span></span> <span data-ttu-id="68647-172">同樣地，當 [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink) 執行在其 [**BindToSource**](/windows/desktop/api/oleidl/nf-oleidl-iolelink-bindtosource) 方法中找不到檔案時，它會自動在追蹤服務上呼叫。</span><span class="sxs-lookup"><span data-stu-id="68647-172">Similarly, when the [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink) implementation cannot find a file, for example, in its [**BindToSource**](/windows/desktop/api/oleidl/nf-oleidl-iolelink-bindtosource) method, it automatically calls on the tracking service.</span></span>

## <a name="link-tracking-limitations"></a><span data-ttu-id="68647-173">連結追蹤限制</span><span class="sxs-lookup"><span data-stu-id="68647-173">Link Tracking Limitations</span></span>

<span data-ttu-id="68647-174">分散式連結追蹤服務僅適用于 NTFS 檔案系統，且僅適用于 NTFS 3.0 或更新版本上的連結來源。</span><span class="sxs-lookup"><span data-stu-id="68647-174">The distributed link tracking services are available only on the NTFS file system, and are only available for link sources on NTFS 3.0 or later.</span></span> <span data-ttu-id="68647-175">因此，如果連結來源移至 FAT 檔案系統磁片區，則追蹤資訊會遺失。</span><span class="sxs-lookup"><span data-stu-id="68647-175">Therefore, if a link source is moved to a FAT file system volume the tracking information is lost.</span></span> <span data-ttu-id="68647-176">此外，如果在 NTFS 3.0 或更新版本之間手機連結來源，但執行移動的電腦正在執行舊版的 Windows，則會遺失連結追蹤資訊。</span><span class="sxs-lookup"><span data-stu-id="68647-176">Additionally, if a link source is moved between the NTFS 3.0 or later, but the computer that is performing the move is running an earlier version of Windows, the link tracking information is lost.</span></span> <span data-ttu-id="68647-177">當連結追蹤資訊遺失時，連結來源檔案本身不會有任何損害，因為分散式連結追蹤服務並不會可追蹤。</span><span class="sxs-lookup"><span data-stu-id="68647-177">When the link tracking information is lost, no harm is done to the link source file itself, it is simply not trackable by the distributed link tracking services.</span></span>

<span data-ttu-id="68647-178">若要取得 NTFS 版本的磁片區，請使用系統管理員存取權限開啟命令提示字元，然後執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="68647-178">To obtain the NTFS version of a volume, open a command prompt with Administrator access rights and execute the following command:</span></span>

<span data-ttu-id="68647-179">**fsutil fsinfo ntfsinfo** \*X \*\* \* *：*</span><span class="sxs-lookup"><span data-stu-id="68647-179">**fsutil fsinfo ntfsinfo** *X\*\*\*:*\*</span></span>

<span data-ttu-id="68647-180">其中 *X* 是磁片區的磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="68647-180">where *X* is the drive letter of the volume.</span></span>

<span data-ttu-id="68647-181">不會維護卸載式媒體上的檔案連結。</span><span class="sxs-lookup"><span data-stu-id="68647-181">Links to files on removable media are not maintained.</span></span> <span data-ttu-id="68647-182">此外，追蹤服務無法辨識新的 NTFS 檔案系統磁片區，直到系統重新開機為止。</span><span class="sxs-lookup"><span data-stu-id="68647-182">Also, the tracking service does not recognize a new NTFS file system volume until the system is re-booted.</span></span> <span data-ttu-id="68647-183">由於重新分割、將 FAT 檔案系統磁片區重新格式化為 NTFS 檔案系統，或連接新的外部磁片磁碟機，因此新的磁片區可能會變成可用。</span><span class="sxs-lookup"><span data-stu-id="68647-183">A new volume might become available because of re-partitioning, reformatting a FAT file system volume to the NTFS file system, or connecting a new external drive.</span></span>

 

 
