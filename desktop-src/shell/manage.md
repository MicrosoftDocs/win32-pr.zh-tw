---
description: Shell 提供許多方式來管理檔案系統。
ms.assetid: d9ffda6f-adc0-44a3-b410-e23bf5f4f165
title: 管理檔案系統
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0f3b47e17e691c540a9775f3b8588b311b9878
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581616"
---
# <a name="managing-the-file-system"></a><span data-ttu-id="377b9-103">管理檔案系統</span><span class="sxs-lookup"><span data-stu-id="377b9-103">Managing the File System</span></span>

<span data-ttu-id="377b9-104">Shell 提供許多方式來管理檔案系統。</span><span class="sxs-lookup"><span data-stu-id="377b9-104">The Shell provides a number of ways to manage file systems.</span></span> <span data-ttu-id="377b9-105">Shell 提供可讓應用程式以程式設計方式移動、複製、重新命名和刪除檔案的函式 [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa)。</span><span class="sxs-lookup"><span data-stu-id="377b9-105">The Shell provides a function, [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa), that allows an application to programmatically move, copy, rename, and delete files.</span></span> <span data-ttu-id="377b9-106">Shell 也支援一些額外的檔案管理功能。</span><span class="sxs-lookup"><span data-stu-id="377b9-106">The Shell also supports some additional file management capabilities.</span></span>

-   <span data-ttu-id="377b9-107">HTML 檔案可以 *連接* 到相關的檔案，例如圖形檔案或樣式表單。</span><span class="sxs-lookup"><span data-stu-id="377b9-107">HTML documents can be *connected* to related files, such as graphics files or style sheets.</span></span> <span data-ttu-id="377b9-108">移動或複製檔時，也會自動移動或複製連接的檔案。</span><span class="sxs-lookup"><span data-stu-id="377b9-108">When the document is moved or copied, the connected files are automatically moved or copied as well.</span></span>
-   <span data-ttu-id="377b9-109">針對多個使用者可用的系統，可以每個使用者為基礎來管理檔案。</span><span class="sxs-lookup"><span data-stu-id="377b9-109">For systems that are available to more than one user, files can be managed on a per-user basis.</span></span> <span data-ttu-id="377b9-110">使用者可以輕鬆地存取其資料檔案，但不能存取屬於其他使用者的檔案。</span><span class="sxs-lookup"><span data-stu-id="377b9-110">Users have easy access to their data files, but not to files belonging to other users.</span></span>
-   <span data-ttu-id="377b9-111">如果新增或修改檔檔案，則可以將它們新增至命令介面的最新檔案清單。</span><span class="sxs-lookup"><span data-stu-id="377b9-111">If document files are added or modified, they can be added to the Shell's list of recent documents.</span></span> <span data-ttu-id="377b9-112">當使用者按一下 [開始] 功能表上的 [**檔**] 命令時，會顯示檔的連結清單。</span><span class="sxs-lookup"><span data-stu-id="377b9-112">When the user clicks the **Documents** command on the Start menu, a list of links to the documents appears.</span></span>

<span data-ttu-id="377b9-113">本檔討論這些檔案管理技術的運作方式。</span><span class="sxs-lookup"><span data-stu-id="377b9-113">This document discusses how these file management technologies work.</span></span> <span data-ttu-id="377b9-114">接著，它會概述如何使用 Shell 來移動、複製、重新命名和刪除檔案，以及如何管理資源回收筒中的物件。</span><span class="sxs-lookup"><span data-stu-id="377b9-114">It then outlines how to use the Shell to move, copy, rename, and delete files, and how to manage objects in the Recycle Bin.</span></span>

-   [<span data-ttu-id="377b9-115">每位使用者的檔案管理</span><span class="sxs-lookup"><span data-stu-id="377b9-115">Per-User File Management</span></span>](#per-user-file-management)
-   [<span data-ttu-id="377b9-116">我的檔和我的圖片資料夾</span><span class="sxs-lookup"><span data-stu-id="377b9-116">My Documents and My Pictures Folders</span></span>](#my-documents-and-my-pictures-folders)
-   [<span data-ttu-id="377b9-117">連接的檔案</span><span class="sxs-lookup"><span data-stu-id="377b9-117">Connected Files</span></span>](#connected-files)
-   [<span data-ttu-id="377b9-118">移動、複製、重新命名和刪除檔案</span><span class="sxs-lookup"><span data-stu-id="377b9-118">Moving, Copying, Renaming, and Deleting Files</span></span>](#moving-copying-renaming-and-deleting-files)
    -   [<span data-ttu-id="377b9-119">通知 Shell</span><span class="sxs-lookup"><span data-stu-id="377b9-119">Notifying the Shell</span></span>](#notifying-the-shell)
-   [<span data-ttu-id="377b9-120">使用 SHFileOperation 管理檔案的簡單範例</span><span class="sxs-lookup"><span data-stu-id="377b9-120">Simple Example of Managing Files with SHFileOperation</span></span>](#simple-example-of-managing-files-with-shfileoperation)
-   [<span data-ttu-id="377b9-121">將檔案新增至最新檔的 Shell 清單</span><span class="sxs-lookup"><span data-stu-id="377b9-121">Adding Files to the Shell's List of Recent Documents</span></span>](#adding-files-to-the-shells-list-of-recent-documents)

## <a name="per-user-file-management"></a><span data-ttu-id="377b9-122">Per-User 檔案管理</span><span class="sxs-lookup"><span data-stu-id="377b9-122">Per-User File Management</span></span>

<span data-ttu-id="377b9-123">Windows 2000 Shell 可讓檔案與特定使用者建立關聯，讓其他使用者無法看見檔案。</span><span class="sxs-lookup"><span data-stu-id="377b9-123">The Windows 2000 Shell allows files to be associated with a particular user so the files remain hidden from other users.</span></span> <span data-ttu-id="377b9-124">就檔案系統而言，檔案會儲存在使用者的設定檔資料夾下，通常是 C： \\ Documents，而設定 \\  \\ Windows 2000 系統上的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="377b9-124">In terms of the file system, the files are stored under the user's profile folder, typically C:\\Documents and Settings\\*Username*\\ on Windows 2000 systems.</span></span> <span data-ttu-id="377b9-125">這項功能可讓許多人使用同一部電腦，同時維持其他使用者的檔案隱私權。</span><span class="sxs-lookup"><span data-stu-id="377b9-125">This feature allows many individuals to use the same computer, while maintaining the privacy of their files from other users.</span></span> <span data-ttu-id="377b9-126">不同的使用者可以使用不同的程式。</span><span class="sxs-lookup"><span data-stu-id="377b9-126">Different users can have different programs available.</span></span> <span data-ttu-id="377b9-127">此外，它也為系統管理員和應用程式提供簡單的方式，讓系統管理員和應用程式儲存 (.ini) 或連結 ( .lnk) 檔案等專案。</span><span class="sxs-lookup"><span data-stu-id="377b9-127">It also provides a straightforward way for administrators and applications to store such things as initialization (.ini) or link (.lnk) files.</span></span> <span data-ttu-id="377b9-128">因此，應用程式可以為每個使用者保留不同的狀態，並在需要時輕鬆地復原該特定狀態。</span><span class="sxs-lookup"><span data-stu-id="377b9-128">Applications can thus preserve a different state for each user and easily recover that particular state when needed.</span></span> <span data-ttu-id="377b9-129">另外還有一個設定檔資料夾，用來儲存所有使用者通用的資訊。</span><span class="sxs-lookup"><span data-stu-id="377b9-129">There is also a profile folder for storing information that is common to all users.</span></span>

<span data-ttu-id="377b9-130">因為無法判斷登入的使用者及其檔案的位置，所以標準的每個使用者資料夾是特殊的資料夾，而且是由 [**CSIDL**](csidl.md)所識別。</span><span class="sxs-lookup"><span data-stu-id="377b9-130">Because it is inconvenient to determine which user is logged in and where their files are located, the standard per-user folders are special folders and are identified by a [**CSIDL**](csidl.md).</span></span> <span data-ttu-id="377b9-131">比方說，每個使用者 Program Files 資料夾的 CSIDL 是 CSIDL \_ 程式。</span><span class="sxs-lookup"><span data-stu-id="377b9-131">For instance, the CSIDL for the per-user Program Files folder is CSIDL\_PROGRAMS.</span></span> <span data-ttu-id="377b9-132">如果您的應用程式使用其中一個每個使用者 CSIDLs 呼叫 [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) 或 [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) ，此函式會傳回專案識別碼清單的指標 (PIDL) 或適用于目前登入使用者的路徑。</span><span class="sxs-lookup"><span data-stu-id="377b9-132">If your application calls [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) or [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) with one of the per-user CSIDLs, the function returns the pointer to an item identifier list (PIDL) or path appropriate to the currently logged-in user.</span></span> <span data-ttu-id="377b9-133">如果您的應用程式需要取出設定檔資料夾的路徑或 PIDL，其 CSIDL 為 **CSIDL \_ 設定檔**。</span><span class="sxs-lookup"><span data-stu-id="377b9-133">If your application needs to retrieve the path or PIDL of the profile folder, its CSIDL is **CSIDL\_PROFILE**.</span></span>

## <a name="my-documents-and-my-pictures-folders"></a><span data-ttu-id="377b9-134">我的檔和我的圖片資料夾</span><span class="sxs-lookup"><span data-stu-id="377b9-134">My Documents and My Pictures Folders</span></span>

<span data-ttu-id="377b9-135">在桌面上找到的其中一個標準圖示是 **我的檔**。</span><span class="sxs-lookup"><span data-stu-id="377b9-135">One of the standard icons found on the desktop is **My Documents**.</span></span> <span data-ttu-id="377b9-136">當您開啟這個資料夾時，它會包含目前使用者的檔檔案。</span><span class="sxs-lookup"><span data-stu-id="377b9-136">When you open this folder, it contains the current user's document files.</span></span> <span data-ttu-id="377b9-137">我的檔的桌面實例是虛擬資料夾，也就是用來實際儲存使用者檔的檔案系統位置（位於命名空間階層的桌面上）的別名。</span><span class="sxs-lookup"><span data-stu-id="377b9-137">The desktop instance of My Documents is a virtual folder—an alias to the file system location used to physically store the user's documents—located immediately below the desktop in the namespace hierarchy.</span></span>

<span data-ttu-id="377b9-138">[我的檔] 和 [我的圖片] 資料夾的目的是要提供簡單且安全的方式，讓使用者在可能有多位使用者的系統上存取其檔和圖片檔案。</span><span class="sxs-lookup"><span data-stu-id="377b9-138">The purpose of the My Documents and My Pictures folders is to provide a straightforward and secure way for users to access their document and picture files on a system that might have multiple users.</span></span> <span data-ttu-id="377b9-139">每位使用者都會為其檔案指派個別的檔系統資料夾。</span><span class="sxs-lookup"><span data-stu-id="377b9-139">Each user is assigned separate file system folders for his or her files.</span></span> <span data-ttu-id="377b9-140">例如，使用者在檔案系統中的 [檔] 資料夾位置通常是 C： \\ documents 和設定使用者 \\ *名稱* \\ 我的檔等內容。</span><span class="sxs-lookup"><span data-stu-id="377b9-140">For example, the location of a user's documents folder in the file system is typically something like C:\\Documents and Settings\\*username*\\My Documents.</span></span> <span data-ttu-id="377b9-141">使用者不需要知道其檔系統資料夾的實體位置。</span><span class="sxs-lookup"><span data-stu-id="377b9-141">There is no need for users to know anything about the physical location of their file system folders.</span></span> <span data-ttu-id="377b9-142">他們只需透過我的檔圖示來存取檔案。</span><span class="sxs-lookup"><span data-stu-id="377b9-142">They simply access their files through the My Documents icon.</span></span>

> [!Note]  
> <span data-ttu-id="377b9-143">我的檔可讓使用者存取自己的檔案，但不能存取任何其他使用者的檔案。</span><span class="sxs-lookup"><span data-stu-id="377b9-143">My Documents allows a user to access his or her own files but not those of any other user.</span></span> <span data-ttu-id="377b9-144">如果有多個人使用同一部電腦，系統管理員可以在儲存實際檔案的檔案系統部分鎖定使用者。</span><span class="sxs-lookup"><span data-stu-id="377b9-144">If multiple individuals use the same computer, an administrator can lock users out of the part of the file system where the actual files are stored.</span></span> <span data-ttu-id="377b9-145">如此一來，使用者就能夠透過我的檔資料夾來處理自己的檔，但不能處理屬於任何其他使用者的檔。</span><span class="sxs-lookup"><span data-stu-id="377b9-145">Users will thus be able to work on their own documents through the My Documents folder but not on documents that belong to any other users.</span></span>

 

<span data-ttu-id="377b9-146">應用程式通常不需要知道哪些使用者已登入，或是使用者的我的檔資料夾所在的檔案系統中。</span><span class="sxs-lookup"><span data-stu-id="377b9-146">There is usually no need for an application to know which user is logged in or where in the file system that user's My Documents folder is located.</span></span> <span data-ttu-id="377b9-147">相反地，您的應用程式可以藉由呼叫桌面的 [**IShellFolder：:P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) 方法，來取出我的檔桌面圖示的 PIDL。</span><span class="sxs-lookup"><span data-stu-id="377b9-147">Instead, your application can retrieve the PIDL of the My Documents desktop icon by calling the desktop's [**IShellFolder::ParseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) method.</span></span> <span data-ttu-id="377b9-148">用來識別我的檔資料夾的剖析名稱不是檔案路徑，而是：： {450d8fba-ad25-11d0-98a8-0800361b1103}。</span><span class="sxs-lookup"><span data-stu-id="377b9-148">The parsing name used to identify the My Documents folder is not a file path but rather ::{450d8fba-ad25-11d0-98a8-0800361b1103}.</span></span> <span data-ttu-id="377b9-149">以括弧括住的運算式是我的檔 GUID 的文字形式。</span><span class="sxs-lookup"><span data-stu-id="377b9-149">The bracketed expression is the text form of the My Documents GUID.</span></span> <span data-ttu-id="377b9-150">例如，若要取出我的檔的 PIDL，您的應用程式應該使用此呼叫來 **IShellFolder：:P arsedisplayname**。</span><span class="sxs-lookup"><span data-stu-id="377b9-150">For example, to retrieve the PIDL of My Documents, your application should use this call to **IShellFolder::ParseDisplayName**.</span></span>


```C++
hr = psfDeskTop->ParseDisplayName(NULL, 
                                  NULL, 
                                  L"::{450d8fba-ad25-11d0-98a8-0800361b1103}", 
                                  &chEaten, 
                                  &pidlDocFiles, 
                                  NULL);
```



<span data-ttu-id="377b9-151">當您的應用程式有我的檔 PIDL 之後，它就可以像一般的檔系統資料夾一樣處理資料夾，例如列舉專案、剖析、系結和執行任何其他有效的資料夾作業。</span><span class="sxs-lookup"><span data-stu-id="377b9-151">Once your application has the My Documents PIDL, it can handle the folder just as it would a normal file system folder—enumerating items, parsing, binding, and performing any other valid folder operations.</span></span> <span data-ttu-id="377b9-152">Shell 會自動將我的檔或其子資料夾中的變更對應到適當的檔系統資料夾。</span><span class="sxs-lookup"><span data-stu-id="377b9-152">The Shell automatically maps changes in My Documents or its subfolders to the appropriate file system folders.</span></span>

<span data-ttu-id="377b9-153">如果您的應用程式需要存取包含目前使用者檔的實際檔系統資料夾，請 \_ 將 CSIDL PERSONAL 傳遞給 [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation)。</span><span class="sxs-lookup"><span data-stu-id="377b9-153">If your application needs access to the actual file system folder that contains the current user's documents, pass CSIDL\_PERSONAL to [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation).</span></span> <span data-ttu-id="377b9-154">函數會傳回目前使用者的我的檔資料夾中顯示之檔系統資料夾的 PIDL。</span><span class="sxs-lookup"><span data-stu-id="377b9-154">The function returns the PIDL of the file system folder that is displayed in the current user's My Documents folder.</span></span>

## <a name="connected-files"></a><span data-ttu-id="377b9-155">連接的檔案</span><span class="sxs-lookup"><span data-stu-id="377b9-155">Connected Files</span></span>

<span data-ttu-id="377b9-156">HTML 檔案通常會有許多相關聯的圖形檔案、樣式表單檔案、數個 Microsoft JScript (與 ECMA 262 語言規格 ) 檔案等相容。</span><span class="sxs-lookup"><span data-stu-id="377b9-156">HTML documents often have a number of associated graphics files, a style sheet file, several Microsoft JScript (compatible with ECMA 262 language specification ) files, and so on.</span></span> <span data-ttu-id="377b9-157">當您移動或複製主要的 HTML 檔案時，通常也會想要移動或複製其相關聯的檔案，以避免中斷連結。</span><span class="sxs-lookup"><span data-stu-id="377b9-157">When you move or copy the primary HTML document, you also usually want to move or copy its associated files to avoid breaking links.</span></span> <span data-ttu-id="377b9-158">可惜的是，到目前為止，我們都沒有簡單的方法可以判斷哪些檔案與任何指定的 HTML 檔案相關，而不是藉由分析其內容。</span><span class="sxs-lookup"><span data-stu-id="377b9-158">Unfortunately, there has been no easy way until now to determine which files are related to any given HTML document other than by analyzing their contents.</span></span> <span data-ttu-id="377b9-159">為了減輕這個問題，Windows 2000 提供簡單的方式，將主要 HTML 檔案 *連接* 到其相關聯的檔案群組。</span><span class="sxs-lookup"><span data-stu-id="377b9-159">To alleviate this problem, Windows 2000 provides a simple way to *connect* a primary HTML document to its group of associated files.</span></span> <span data-ttu-id="377b9-160">如果已啟用檔案連接，則在移動或複製檔時，會將其所有連接的檔案移至其中。</span><span class="sxs-lookup"><span data-stu-id="377b9-160">If file connection is enabled, when the document is moved or copied all its connected files go with it.</span></span>

<span data-ttu-id="377b9-161">若要建立已連接的檔案群組，主要檔必須有 .htm 或 .html 副檔名。</span><span class="sxs-lookup"><span data-stu-id="377b9-161">To create a group of connected files, the primary document must have an .htm or .html file name extension.</span></span> <span data-ttu-id="377b9-162">建立主要檔的父資料夾的子資料夾。</span><span class="sxs-lookup"><span data-stu-id="377b9-162">Create a subfolder of the primary document's parent folder.</span></span> <span data-ttu-id="377b9-163">子資料夾的名稱必須是主要檔的名稱，而不是 .htm 或 .html 副檔名，後面接著下列其中一個延伸模組。</span><span class="sxs-lookup"><span data-stu-id="377b9-163">The subfolder's name must be the name of the primary document, minus the .htm or .html extension, followed by one of the extensions listed below.</span></span> <span data-ttu-id="377b9-164">最常使用的延伸模組為 ". files" 或 " \_ files"。</span><span class="sxs-lookup"><span data-stu-id="377b9-164">The most commonly used extensions are ".files" or "\_files".</span></span> <span data-ttu-id="377b9-165">比方說，如果主要檔命名為 MyDoc.htm，則將子資料夾命名為 "MyDoc \_ files" 會將子資料夾定義為檔連接檔案的容器。</span><span class="sxs-lookup"><span data-stu-id="377b9-165">For instance, if the primary document is named MyDoc.htm, naming the subfolder "MyDoc\_files" defines the subfolder as the container for the document's connected files.</span></span> <span data-ttu-id="377b9-166">如果移動或複製主要檔，也會移動或複製子資料夾及其檔案。</span><span class="sxs-lookup"><span data-stu-id="377b9-166">If the primary document is moved or copied, the subfolder and its files are moved or copied as well.</span></span>

<span data-ttu-id="377b9-167">針對某些語言，您可以使用「檔案」的當地語系化對等專案 \_ 來建立連接檔案的子資料夾。</span><span class="sxs-lookup"><span data-stu-id="377b9-167">For some languages, it is possible to use a localized equivalent of "\_files" to create a subfolder for connected files.</span></span> <span data-ttu-id="377b9-168">下表列出可以附加至檔案名稱以建立連接檔案子資料夾的有效字串。</span><span class="sxs-lookup"><span data-stu-id="377b9-168">The following table lists the valid strings that can be appended to a document name to create a connected files subfolder.</span></span> <span data-ttu-id="377b9-169">請注意，其中有些字串的第一個字元是 '-'，而不是 ' \_ ' 或 '. '。</span><span class="sxs-lookup"><span data-stu-id="377b9-169">Note that some of these strings have '-' as their first character rather than '\_' or '.'.</span></span>



:::row:::
   :::column span="":::
      <span data-ttu-id="377b9-170">" \_ archivos"</span><span class="sxs-lookup"><span data-stu-id="377b9-170">"\_archivos"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="377b9-171">" \_ arquivos"</span><span class="sxs-lookup"><span data-stu-id="377b9-171">"\_arquivos"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="377b9-172">" \_ bestanden"</span><span class="sxs-lookup"><span data-stu-id="377b9-172">"\_bestanden"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="377b9-173">" \_ bylos"</span><span class="sxs-lookup"><span data-stu-id="377b9-173">"\_bylos"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="377b9-174">"-檔案"</span><span class="sxs-lookup"><span data-stu-id="377b9-174">"-Dateien"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="377b9-175">" \_ datoteke"</span><span class="sxs-lookup"><span data-stu-id="377b9-175">"\_datoteke"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="377b9-176">" \_ dosyalar"</span><span class="sxs-lookup"><span data-stu-id="377b9-176">"\_dosyalar"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="377b9-177">" \_ elemei"</span><span class="sxs-lookup"><span data-stu-id="377b9-177">"\_elemei"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="377b9-178">" \_ failid"</span><span class="sxs-lookup"><span data-stu-id="377b9-178">"\_failid"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="377b9-179">「 \_ 失敗」</span><span class="sxs-lookup"><span data-stu-id="377b9-179">"\_fails"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="377b9-180">" \_ fajlovi"</span><span class="sxs-lookup"><span data-stu-id="377b9-180">"\_fajlovi"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="377b9-181">" \_ ficheiros"</span><span class="sxs-lookup"><span data-stu-id="377b9-181">"\_ficheiros"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="377b9-182">" \_ fichiers"</span><span class="sxs-lookup"><span data-stu-id="377b9-182">"\_fichiers"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="377b9-183">"-檔案管理工具"</span><span class="sxs-lookup"><span data-stu-id="377b9-183">"-filer"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="377b9-184">". files"</span><span class="sxs-lookup"><span data-stu-id="377b9-184">".files"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="377b9-185">" \_ files"</span><span class="sxs-lookup"><span data-stu-id="377b9-185">"\_files"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="377b9-186">" \_ file"</span><span class="sxs-lookup"><span data-stu-id="377b9-186">"\_file"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="377b9-187">" \_ fitxers"</span><span class="sxs-lookup"><span data-stu-id="377b9-187">"\_fitxers"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="377b9-188">" \_ fitxategiak"</span><span class="sxs-lookup"><span data-stu-id="377b9-188">"\_fitxategiak"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="377b9-189">" \_ pliki"</span><span class="sxs-lookup"><span data-stu-id="377b9-189">"\_pliki"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="377b9-190">" \_ 檔案"</span><span class="sxs-lookup"><span data-stu-id="377b9-190">"\_soubory"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="377b9-191">" \_ tiedostot"</span><span class="sxs-lookup"><span data-stu-id="377b9-191">"\_tiedostot"</span></span>
   :::column-end:::
   :::column span="":::
   :::column-end:::
   :::column span="":::
   :::column-end:::
:::row-end:::



 

> [!Note]  
> <span data-ttu-id="377b9-192">這項功能對延伸模組的大小寫很敏感。</span><span class="sxs-lookup"><span data-stu-id="377b9-192">This feature is sensitive to the case of the extension.</span></span> <span data-ttu-id="377b9-193">例如，在上述範例中，名為 "MyDoc Files" 的子資料夾 \_ 將不會連接到 MyDoc.htm。</span><span class="sxs-lookup"><span data-stu-id="377b9-193">For instance, for the example given above, a subfolder named "MyDoc\_Files" will not be connected to MyDoc.htm.</span></span>

 

<span data-ttu-id="377b9-194">啟用或停用檔案連接時，是由下列登錄機碼的 **REG \_ DWORD** 值 NoFileFolderConnection 所控制。</span><span class="sxs-lookup"><span data-stu-id="377b9-194">Whether file connection is enabled or disabled is controlled by a **REG\_DWORD** value, NoFileFolderConnection, of the following registry key.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
```

<span data-ttu-id="377b9-195">此值通常未定義，且已啟用檔案連接。</span><span class="sxs-lookup"><span data-stu-id="377b9-195">This value normally is not defined, and file connection is enabled.</span></span> <span data-ttu-id="377b9-196">如有必要，您可以將此值新增至機碼，並將它設定為1，以停用檔案連接。</span><span class="sxs-lookup"><span data-stu-id="377b9-196">If necessary, you can disable file connection by adding this value to the key and setting it to 1.</span></span> <span data-ttu-id="377b9-197">若要再次啟用檔案連接，請將 NoFileFolderConnection 設定為零。</span><span class="sxs-lookup"><span data-stu-id="377b9-197">To enable file connection again, set NoFileFolderConnection to zero.</span></span>

> [!Note]  
> <span data-ttu-id="377b9-198">通常應該啟用檔案連接，因為其他應用程式可能相依于該連接。</span><span class="sxs-lookup"><span data-stu-id="377b9-198">File connection should normally be enabled because other applications might depend on it.</span></span> <span data-ttu-id="377b9-199">只有在絕對必要時才停用檔案連接。</span><span class="sxs-lookup"><span data-stu-id="377b9-199">Disable file connection only if absolutely necessary.</span></span>

 

## <a name="moving-copying-renaming-and-deleting-files"></a><span data-ttu-id="377b9-200">移動、複製、重新命名和刪除檔案</span><span class="sxs-lookup"><span data-stu-id="377b9-200">Moving, Copying, Renaming, and Deleting Files</span></span>

<span data-ttu-id="377b9-201">命名空間不是靜態的，而且應用程式通常需要藉由執行下列其中一項作業來管理檔案系統。</span><span class="sxs-lookup"><span data-stu-id="377b9-201">The namespace is not static, and applications commonly need to manage the file system by performing one of the following operations.</span></span>

-   <span data-ttu-id="377b9-202">將物件複製到另一個資料夾。</span><span class="sxs-lookup"><span data-stu-id="377b9-202">Copying an object to another folder.</span></span>
-   <span data-ttu-id="377b9-203">將物件移到另一個資料夾。</span><span class="sxs-lookup"><span data-stu-id="377b9-203">Moving an object to another folder.</span></span>
-   <span data-ttu-id="377b9-204">刪除物件。</span><span class="sxs-lookup"><span data-stu-id="377b9-204">Deleting an object.</span></span>
-   <span data-ttu-id="377b9-205">重新命名物件。</span><span class="sxs-lookup"><span data-stu-id="377b9-205">Renaming an object.</span></span>

<span data-ttu-id="377b9-206">這些作業都是使用 [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa)執行。</span><span class="sxs-lookup"><span data-stu-id="377b9-206">These operations are all performed with [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa).</span></span> <span data-ttu-id="377b9-207">此函式會接受一或多個原始檔，並產生對應的目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="377b9-207">This function takes one or more source files and produces corresponding destination files.</span></span> <span data-ttu-id="377b9-208">在刪除操作的情況下，系統會嘗試將已刪除的檔案放入資源回收筒中。</span><span class="sxs-lookup"><span data-stu-id="377b9-208">In the case of the delete operation, the system attempts to put the deleted files into the Recycle Bin.</span></span>

<span data-ttu-id="377b9-209">您也可以使用 [拖放](dragdrop.md) 功能來移動檔案。</span><span class="sxs-lookup"><span data-stu-id="377b9-209">It is also possible to move files using the [drag-and-drop](dragdrop.md) functionality.</span></span>

<span data-ttu-id="377b9-210">若要使用函式，您必須填入 [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) 結構的成員，並將其傳遞至 [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa)。</span><span class="sxs-lookup"><span data-stu-id="377b9-210">To use the function, you must fill in the members of an [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure and pass it to [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa).</span></span> <span data-ttu-id="377b9-211">結構的索引鍵成員為 **pFrom** 和 **pTo**。</span><span class="sxs-lookup"><span data-stu-id="377b9-211">The key members of the structure are **pFrom** and **pTo**.</span></span>

<span data-ttu-id="377b9-212">**PFrom** 成員是雙 **null** 終止的字串，其中包含一或多個原始程式檔名稱。</span><span class="sxs-lookup"><span data-stu-id="377b9-212">The **pFrom** member is a double **null**-terminated string that contains one or more source file names.</span></span> <span data-ttu-id="377b9-213">這些名稱可以是完整路徑或標準的 DOS 萬用字元，例如 \* 。 \*</span><span class="sxs-lookup"><span data-stu-id="377b9-213">These names can be either fully qualified paths or standard DOS wildcards such as \*.\*.</span></span> <span data-ttu-id="377b9-214">雖然這個成員是宣告為以 **null** 終止的字串，但它會用來做為保存多個檔案名的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="377b9-214">Although this member is declared as a **null**-terminated string, it is used as a buffer to hold multiple file names.</span></span> <span data-ttu-id="377b9-215">每個檔案名都必須以一般的單一 **Null** 字元來終止。</span><span class="sxs-lookup"><span data-stu-id="377b9-215">Each file name must be terminated by the usual single **NULL** character.</span></span> <span data-ttu-id="377b9-216">必須將額外的 **Null** 字元附加到最後名稱的結尾，以指出 **pFrom** 的結尾。</span><span class="sxs-lookup"><span data-stu-id="377b9-216">An additional **NULL** character must be appended to the end of the final name to indicate the end of **pFrom**.</span></span>

<span data-ttu-id="377b9-217">**PTo** 成員是雙 **null** 終止的字串，與 **pFrom** 很類似。</span><span class="sxs-lookup"><span data-stu-id="377b9-217">The **pTo** member is a double **null**-terminated string, much like **pFrom**.</span></span> <span data-ttu-id="377b9-218">**PTo** 成員包含一或多個完整目的地名稱的名稱。</span><span class="sxs-lookup"><span data-stu-id="377b9-218">The **pTo** member contains the names of one or more fully qualified destination names.</span></span> <span data-ttu-id="377b9-219">它們封裝成 **pTo** 的方式與 **pFrom** 相同。</span><span class="sxs-lookup"><span data-stu-id="377b9-219">They are packed into **pTo** in the same way as they are for **pFrom**.</span></span> <span data-ttu-id="377b9-220">如果 **pTo** 包含多個名稱，您也必須在 **fFlags** 成員中設定 **FOF \_ MULTIDESTFILES** 旗標。</span><span class="sxs-lookup"><span data-stu-id="377b9-220">If **pTo** contains multiple names, you must also set the **FOF\_MULTIDESTFILES** flag in the **fFlags** member.</span></span> <span data-ttu-id="377b9-221">**PTo** 的使用取決於此作業，如下所述。</span><span class="sxs-lookup"><span data-stu-id="377b9-221">The usage of **pTo** depends on the operation as described here.</span></span>

-   <span data-ttu-id="377b9-222">若為複製和移動作業，如果所有檔案都移至單一目錄， **pTo** 就會包含完整的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="377b9-222">For copy and move operations, if all the files are going to a single directory, **pTo** contains the fully qualified directory name.</span></span> <span data-ttu-id="377b9-223">如果檔案要前往不同的目的地， **pTo** 也可以針對每個原始程式檔包含一個完整目錄或檔案名。</span><span class="sxs-lookup"><span data-stu-id="377b9-223">If the files are going to different destinations, **pTo** can also contain one fully qualified directory or file name for each source file.</span></span> <span data-ttu-id="377b9-224">如果目錄不存在，系統會加以建立。</span><span class="sxs-lookup"><span data-stu-id="377b9-224">If a directory does not exist, the system creates it.</span></span>
-   <span data-ttu-id="377b9-225">針對重新命名作業， **pTo** 會在 **pFrom** 中包含每個原始程式檔的一個完整路徑。</span><span class="sxs-lookup"><span data-stu-id="377b9-225">For rename operations, **pTo** contains one fully qualified path for each source file in **pFrom**.</span></span>
-   <span data-ttu-id="377b9-226">若為刪除作業，則不會使用 **pTo** 。</span><span class="sxs-lookup"><span data-stu-id="377b9-226">For delete operations, **pTo** is not used.</span></span>

### <a name="notifying-the-shell"></a><span data-ttu-id="377b9-227">通知 Shell</span><span class="sxs-lookup"><span data-stu-id="377b9-227">Notifying the Shell</span></span>

<span data-ttu-id="377b9-228">使用 [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) 移動、複製、重新命名或刪除檔案，或採取任何其他影響命名空間的動作之後，請通知 Shell 變更。</span><span class="sxs-lookup"><span data-stu-id="377b9-228">Notify the Shell of the change after using [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) to move, copy, rename, or delete files, or after taking any other action that affects the namespace.</span></span> <span data-ttu-id="377b9-229">應伴隨通知的動作包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="377b9-229">Actions that should be accompanied by notification include the following:</span></span>

-   <span data-ttu-id="377b9-230">新增或刪除檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="377b9-230">Adding or deleting files or folders.</span></span>
-   <span data-ttu-id="377b9-231">移動、複製或重新命名檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="377b9-231">Moving, copying, or renaming files or folders.</span></span>
-   <span data-ttu-id="377b9-232">變更檔案關聯。</span><span class="sxs-lookup"><span data-stu-id="377b9-232">Changing a file association.</span></span>
-   <span data-ttu-id="377b9-233">變更檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="377b9-233">Changing file attributes.</span></span>
-   <span data-ttu-id="377b9-234">新增或移除磁片磁碟機或存放裝置媒體。</span><span class="sxs-lookup"><span data-stu-id="377b9-234">Adding or removing drives or storage media.</span></span>
-   <span data-ttu-id="377b9-235">建立或停用共用資料夾。</span><span class="sxs-lookup"><span data-stu-id="377b9-235">Creating or disabling a shared folder.</span></span>
-   <span data-ttu-id="377b9-236">變更系統映射清單。</span><span class="sxs-lookup"><span data-stu-id="377b9-236">Changing the system image list.</span></span>

<span data-ttu-id="377b9-237">應用程式會藉由呼叫 [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) 以及已變更內容的詳細資料，來通知 Shell。</span><span class="sxs-lookup"><span data-stu-id="377b9-237">An application notifies the Shell by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) with the details of what has changed.</span></span> <span data-ttu-id="377b9-238">然後，Shell 可以更新其命名空間的影像，以正確地反映其新狀態。</span><span class="sxs-lookup"><span data-stu-id="377b9-238">The Shell can then update its image of the namespace to accurately reflect its new state.</span></span>

## <a name="simple-example-of-managing-files-with-shfileoperation"></a><span data-ttu-id="377b9-239">使用 SHFileOperation 管理檔案的簡單範例</span><span class="sxs-lookup"><span data-stu-id="377b9-239">Simple Example of Managing Files with SHFileOperation</span></span>

<span data-ttu-id="377b9-240">下列範例主控台應用程式說明如何使用 [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) 將檔案從一個目錄複寫到另一個目錄。</span><span class="sxs-lookup"><span data-stu-id="377b9-240">The following sample console application illustrates the use of [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) to copy files from one directory to another.</span></span> <span data-ttu-id="377b9-241">為了簡單起見，來源和目的地目錄（C： \\ my 檔 \_ 和 c： \\ my \_ Docs2）會硬式編碼到應用程式中。</span><span class="sxs-lookup"><span data-stu-id="377b9-241">The source and destination directories, C:\\My\_Docs and C:\\My\_Docs2, are hard-coded into the application for simplicity.</span></span>


```C++
#include <shlobj.h>
#include <shlwapi.h>
#include <strsafe.h>

int main(void)
{
    IShellFolder *psfDeskTop = NULL;
    IShellFolder *psfDocFiles = NULL;
    LPITEMIDLIST pidlDocFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IEnumIDList *ppenum = NULL;
    SHFILEOPSTRUCT sfo;
    STRRET strDispName;
    TCHAR szParseName[MAX_PATH];
    TCHAR szSourceFiles[256];
    int i;
    int iBufPos = 0;
    ULONG chEaten;
    ULONG celtFetched;
    size_t ParseNameSize = 0;
    HRESULT hr;
    

    szSourceFiles[0] = '\0';
    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->ParseDisplayName(NULL, NULL, L"c:\\My_Docs", 
         &chEaten, &pidlDocFiles, NULL);
    hr = psfDeskTop->BindToObject(pidlDocFiles, NULL, IID_IShellFolder, 
         (LPVOID *) &psfDocFiles);
    hr = psfDeskTop->Release();

    hr = psfDocFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, 
         &ppenum);

    while( (hr = ppenum->Next(1,&pidlItems, &celtFetched)) == S_OK 
       && (celtFetched) == 1)
    {
        psfDocFiles->GetDisplayNameOf(pidlItems, SHGDN_FORPARSING, 
            &strDispName);
        StrRetToBuf(&strDispName, pidlItems, szParseName, MAX_PATH);
        
        hr = StringCchLength(szParseName, MAX_PATH, &ParseNameSize);
        
        if (SUCCEEDED(hr))
        {
            for(i=0; i<=ParseNameSize; i++)
            {
                szSourceFiles[iBufPos++] = szParseName[i];
            }
            CoTaskMemFree(pidlItems);
        }
    }
    ppenum->Release();
    
    szSourceFiles[iBufPos] = '\0';

    sfo.hwnd = NULL;
    sfo.wFunc = FO_COPY;
    sfo.pFrom = szSourceFiles;
    sfo.pTo = "c:\\My_Docs2\0";
    sfo.fFlags = FOF_SILENT | FOF_NOCONFIRMATION | FOF_NOCONFIRMMKDIR;

    hr = SHFileOperation(&sfo);
    
    SHChangeNotify(SHCNE_UPDATEDIR, SHCNF_PATH, (LPCVOID) "c:\\My_Docs2", 0);

    CoTaskMemFree(pidlDocFiles);
    psfDocFiles->Release();

    return 0;
}
```



<span data-ttu-id="377b9-242">應用程式會先抓取桌面 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="377b9-242">The application first retrieves a pointer to the desktop's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span> <span data-ttu-id="377b9-243">然後，它會將其完整路徑傳遞至 [**IShellFolder：:P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname)，以抓取來原始目錄的 PIDL。</span><span class="sxs-lookup"><span data-stu-id="377b9-243">It then retrieves the source directory's PIDL by passing its fully qualified path to [**IShellFolder::ParseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname).</span></span> <span data-ttu-id="377b9-244">請注意， **IShellFolder：:P arsedisplayname** 需要目錄的路徑是 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="377b9-244">Note that **IShellFolder::ParseDisplayName** requires the directory's path to be a Unicode string.</span></span> <span data-ttu-id="377b9-245">然後，應用程式會系結至來原始目錄，並使用其 **IShellFolder** 介面來取得列舉值物件的 [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) 介面。</span><span class="sxs-lookup"><span data-stu-id="377b9-245">The application then binds to the source directory and uses its **IShellFolder** interface to retrieve an enumerator object's [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) interface.</span></span>

<span data-ttu-id="377b9-246">列舉來原始目錄中的每個檔案時，會使用 [**IShellFolder：： GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) 來取出其名稱。</span><span class="sxs-lookup"><span data-stu-id="377b9-246">As each file in the source directory is enumerated, [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) is used to retrieve its name.</span></span> <span data-ttu-id="377b9-247">\_已設定 SHGDN FORPARSING 旗標，這會導致 **IShellFolder：： GetDisplayNameOf** 傳回檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="377b9-247">The SHGDN\_FORPARSING flag is set, which causes **IShellFolder::GetDisplayNameOf** to return the file's fully qualified path.</span></span> <span data-ttu-id="377b9-248">檔案路徑（包括結束的 **Null** 字元）會串連成單一陣列 *szSourceFiles*。</span><span class="sxs-lookup"><span data-stu-id="377b9-248">The file paths, including the terminating **NULL** characters, are concatenated into a single array, *szSourceFiles*.</span></span> <span data-ttu-id="377b9-249">第二個 **Null** 字元會附加到最後一個路徑，以正確地終止陣列。</span><span class="sxs-lookup"><span data-stu-id="377b9-249">A second **NULL** character is appended to the final path to terminate the array properly.</span></span>

<span data-ttu-id="377b9-250">列舉完成後，應用程式會將值指派給 [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) 結構。</span><span class="sxs-lookup"><span data-stu-id="377b9-250">Once the enumeration is complete, the application assigns values to an [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure.</span></span> <span data-ttu-id="377b9-251">請注意，指派給 **pTo** 以指定目的地的陣列也必須由 double **Null** 來終止。</span><span class="sxs-lookup"><span data-stu-id="377b9-251">Note that the array assigned to **pTo** to specify the destination must also be terminated by a double **NULL**.</span></span> <span data-ttu-id="377b9-252">在此情況下，它只會包含在指派給 **pTo** 的字串中。</span><span class="sxs-lookup"><span data-stu-id="377b9-252">In this case, it is simply included in the string that is assigned to **pTo**.</span></span> <span data-ttu-id="377b9-253">因為這是主控台應用程式，所以 FOF \_ 無訊息、FOF \_ NOCONFIRMATION 和 FOF \_ NOCONFIRMMKDIR 旗標會設定為隱藏任何可能出現的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="377b9-253">Because this is a console application, the FOF\_SILENT, FOF\_NOCONFIRMATION, and FOF\_NOCONFIRMMKDIR flags are set to suppress any dialog boxes that might appear.</span></span> <span data-ttu-id="377b9-254">[**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa)傳回之後，會呼叫 [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)來通知 Shell 變更。</span><span class="sxs-lookup"><span data-stu-id="377b9-254">After [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) returns, [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) is called to notify the Shell of the change.</span></span> <span data-ttu-id="377b9-255">然後，應用程式會執行一般的清除並傳回。</span><span class="sxs-lookup"><span data-stu-id="377b9-255">Then the application performs the usual cleanup and returns.</span></span>

## <a name="adding-files-to-the-shells-list-of-recent-documents"></a><span data-ttu-id="377b9-256">將檔案新增至最新檔的 Shell 清單</span><span class="sxs-lookup"><span data-stu-id="377b9-256">Adding Files to the Shell's List of Recent Documents</span></span>

<span data-ttu-id="377b9-257">Shell 會為每個使用者維護最近新增或修改過的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="377b9-257">The Shell maintains a list of recently added or modified documents for each user.</span></span> <span data-ttu-id="377b9-258">使用者可以按一下 [開始] 功能表上的 [檔]，以顯示這些檔案的連結清單。</span><span class="sxs-lookup"><span data-stu-id="377b9-258">The user can display a list of links to these files by clicking Documents on the Start menu.</span></span> <span data-ttu-id="377b9-259">如同我的檔，每個使用者都有一個檔案系統目錄來保存實際的連結。</span><span class="sxs-lookup"><span data-stu-id="377b9-259">As with My Documents, each user has a file system directory to hold the actual links.</span></span> <span data-ttu-id="377b9-260">若要取得目前使用者最新目錄的 PIDL，您的應用程式可以使用最近的 CSIDL 來呼叫 [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) \_ ，或呼叫 [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) 來取出其路徑。</span><span class="sxs-lookup"><span data-stu-id="377b9-260">To retrieve the PIDL of the current user's Recent directory, your application can call [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) with CSIDL\_RECENT, or call [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) to retrieve its path.</span></span>

<span data-ttu-id="377b9-261">您的應用程式可以使用本檔稍早所討論的技術來列舉最新資料夾的內容。</span><span class="sxs-lookup"><span data-stu-id="377b9-261">Your application can enumerate the contents of the Recent folder using the techniques discussed earlier in this document.</span></span> <span data-ttu-id="377b9-262">但是，應用程式不應該像一般檔系統資料夾一樣修改資料夾的內容。</span><span class="sxs-lookup"><span data-stu-id="377b9-262">However, an application should not modify the contents of the folder as if it were a normal file system folder.</span></span> <span data-ttu-id="377b9-263">如果這樣做，就不會正確更新 Shell 的最新檔案清單，且變更將不會反映在 [開始] 功能表中。</span><span class="sxs-lookup"><span data-stu-id="377b9-263">If it does so, the Shell's list of recent documents will not be updated properly, and the changes will not be reflected in the Start menu.</span></span> <span data-ttu-id="377b9-264">相反地，若要將檔連結新增至使用者的最新資料夾，您的應用程式可以呼叫 [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)。</span><span class="sxs-lookup"><span data-stu-id="377b9-264">Instead, to add a document link to a user's Recent folder, your application can call [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs).</span></span> <span data-ttu-id="377b9-265">Shell 會將連結新增至適當的檔系統資料夾，以及更新其最近使用的檔和 [開始] 功能表的清單。</span><span class="sxs-lookup"><span data-stu-id="377b9-265">The Shell will add a link to the appropriate file system folder, as well as updating its list of recent documents and the Start menu.</span></span> <span data-ttu-id="377b9-266">您也可以使用此函數來清除資料夾。</span><span class="sxs-lookup"><span data-stu-id="377b9-266">You can also use this function to clear the folder.</span></span>

 

 
