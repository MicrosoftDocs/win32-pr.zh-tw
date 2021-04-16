---
description: 本主題說明什麼是程式庫，以及它們如何受益于使用者和開發人員。
ms.assetid: D5F5FE96-11D2-4fc5-A68B-6E594C09BE20
title: 關於程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e577e7b5df0a1e072a07a096434af84ff8e2c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563030"
---
# <a name="about-libraries"></a><span data-ttu-id="c8694-103">關於程式庫</span><span class="sxs-lookup"><span data-stu-id="c8694-103">About Libraries</span></span>

<span data-ttu-id="c8694-104">本主題說明什麼是程式庫，以及它們如何受益于使用者和開發人員。</span><span class="sxs-lookup"><span data-stu-id="c8694-104">This topic describes what libraries are and how they can benefit users and developers.</span></span>

<span data-ttu-id="c8694-105">程式庫是使用者定義的資料夾集合。</span><span class="sxs-lookup"><span data-stu-id="c8694-105">Libraries are user-defined collections of folders.</span></span> <span data-ttu-id="c8694-106">程式庫會持續追蹤每個資料夾的實體儲存位置，以免除使用者和該工作的軟體。</span><span class="sxs-lookup"><span data-stu-id="c8694-106">A library keeps track of each folder's physical storage location, which relieves the user and the software of that task.</span></span> <span data-ttu-id="c8694-107">使用者可以在程式庫中將相關資料夾群組在一起，即使這些資料夾儲存在不同的硬碟或不同的電腦上也一樣。</span><span class="sxs-lookup"><span data-stu-id="c8694-107">Users can group related folders together in a library even if those folders are stored on different hard drives or different computers.</span></span>

<span data-ttu-id="c8694-108">在文件庫中，資料夾和檔案會以單一集合的形式顯示給使用者，而使用 Shell 程式庫 API，程式庫的內容也可能會出現在程式的單一位置中。</span><span class="sxs-lookup"><span data-stu-id="c8694-108">In a library, the folders and files appear to the user as a single collection and, using the Shell Library API, the library's contents can also appear to be in a single location to a program.</span></span>

<span data-ttu-id="c8694-109">在文件庫中，內容（例如使用者的檔、相片、影片或音樂）可以依使用者的需要排序並顯示，而不像檔案系統的需求。</span><span class="sxs-lookup"><span data-stu-id="c8694-109">In a library, the contents, such as a user's documents, photos, videos, or music, can be sorted and displayed as the user wants and not simply as how the file system requires.</span></span> <span data-ttu-id="c8694-110">例如，使用者可以使用程式庫中專案的屬性來組織文件庫的內容，如此一來，即使相關專案儲存在不同的資料夾中，也會一起排序。</span><span class="sxs-lookup"><span data-stu-id="c8694-110">For example, users can organize the contents of a library using the properties of the items in the library so that related items will sort together even if they are stored in different folders.</span></span>

![程式庫使用者介面的螢幕擷取畫面](images/libraries-whatare.png)

<span data-ttu-id="c8694-112">本主題內容：</span><span class="sxs-lookup"><span data-stu-id="c8694-112">In this topic:</span></span>

-   [<span data-ttu-id="c8694-113">程式庫優點</span><span class="sxs-lookup"><span data-stu-id="c8694-113">Library Benefits</span></span>](#library-benefits)
    -   [<span data-ttu-id="c8694-114">使用者權益</span><span class="sxs-lookup"><span data-stu-id="c8694-114">User Benefits</span></span>](#user-benefits)
    -   [<span data-ttu-id="c8694-115">開發人員權益</span><span class="sxs-lookup"><span data-stu-id="c8694-115">Developer Benefits</span></span>](#developer-benefits)
-   [<span data-ttu-id="c8694-116">管理程式庫中的資料夾</span><span class="sxs-lookup"><span data-stu-id="c8694-116">Managing Folders in Libraries</span></span>](#managing-folders-in-libraries)
-   [<span data-ttu-id="c8694-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="c8694-117">Related topics</span></span>](#related-topics)

## <a name="library-benefits"></a><span data-ttu-id="c8694-118">程式庫優點</span><span class="sxs-lookup"><span data-stu-id="c8694-118">Library Benefits</span></span>

<span data-ttu-id="c8694-119">本節將說明程式庫從終端使用者的觀點和程式開發人員觀點的一些優點。</span><span class="sxs-lookup"><span data-stu-id="c8694-119">This section describes some of the benefits of libraries from the end-user's perspective and the program developer's perspective.</span></span>

### <a name="user-benefits"></a><span data-ttu-id="c8694-120">使用者權益</span><span class="sxs-lookup"><span data-stu-id="c8694-120">User Benefits</span></span>

<span data-ttu-id="c8694-121">將程式庫支援新增至您的程式，可為使用者提供下列優點：</span><span class="sxs-lookup"><span data-stu-id="c8694-121">Adding library support to your program provides the following benefits to the user:</span></span>

-   <span data-ttu-id="c8694-122">**程式庫在 Windows 7 中提供一致的使用者介面**</span><span class="sxs-lookup"><span data-stu-id="c8694-122">**Libraries provide a consistent user interface in Windows 7**</span></span>

    <span data-ttu-id="c8694-123">[一般檔案] 對話方塊支援程式庫，並提供與 Windows 7 中的 Windows 檔案總管相同的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="c8694-123">The common file dialog boxes support libraries and provide the same user experience as the Windows Explorer in Windows 7.</span></span> <span data-ttu-id="c8694-124">當您在 Windows 7 中使用程式時，您程式中的支援程式庫將有助於為使用者提供更順暢的互動。</span><span class="sxs-lookup"><span data-stu-id="c8694-124">Supporting libraries in your program will help provide a more seamless interaction for the user when using your program in Windows 7.</span></span>

-   <span data-ttu-id="c8694-125">**使用者決定儲存內容的位置**</span><span class="sxs-lookup"><span data-stu-id="c8694-125">**Users decide where to store content**</span></span>

    <span data-ttu-id="c8694-126">程式庫讓使用者可以控制其內容的儲存位置。</span><span class="sxs-lookup"><span data-stu-id="c8694-126">Libraries make it possible for users to control where their content is stored.</span></span> <span data-ttu-id="c8694-127">同時，程式庫會為不想要在電腦中管理該詳細資料層級的使用者提供合理的預設值。</span><span class="sxs-lookup"><span data-stu-id="c8694-127">At the same time, libraries provide reasonable defaults for users who do not want to manage that level of detail in their computer.</span></span> <span data-ttu-id="c8694-128">使用者會決定要在何處及如何儲存其內容，以及程式庫如何以任何方式運作，來控制他們想要執行的控制程度。</span><span class="sxs-lookup"><span data-stu-id="c8694-128">Users decide how much, or how little, control they want to exercise over where and how their content is stored and the library works fine either way.</span></span>

### <a name="developer-benefits"></a><span data-ttu-id="c8694-129">開發人員權益</span><span class="sxs-lookup"><span data-stu-id="c8694-129">Developer Benefits</span></span>

<span data-ttu-id="c8694-130">您可以使用程式中的程式庫提供更具彈性且方便的使用者介面，而不需要新增許多複雜的程式碼。</span><span class="sxs-lookup"><span data-stu-id="c8694-130">You can use libraries in your program to provide a more flexible and convenient user interface without having to add a lot of complex program code.</span></span> <span data-ttu-id="c8694-131">新增程式庫支援的一些優點包括：</span><span class="sxs-lookup"><span data-stu-id="c8694-131">Some of the advantages of adding library support include:</span></span>

-   <span data-ttu-id="c8694-132">**程式庫支援程式庫和檔案系統存取**</span><span class="sxs-lookup"><span data-stu-id="c8694-132">**Libraries support library and file-system access**</span></span>

    <span data-ttu-id="c8694-133">使用 [**Shell 程式庫 API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)，程式可以為使用者提供程式庫支援，同時減少其檔案和資料夾管理程式碼的複雜度。</span><span class="sxs-lookup"><span data-stu-id="c8694-133">Using the [**Shell Library API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary), programs can provide library support for the user while reducing the complexity of their file and folder management code.</span></span> <span data-ttu-id="c8694-134">如果您的程式已使用檔案系統 API，您可以視需要保留大部分的現有程式碼，並藉由從 **Shell 程式庫 API** 取得必要的檔案系統資訊，為使用者提供程式庫支援。</span><span class="sxs-lookup"><span data-stu-id="c8694-134">If your program already uses the file-system API, you can preserve as much of that existing code as you want and still provide library support to the user by getting the necessary file-system information from the **Shell Library API**.</span></span>

-   <span data-ttu-id="c8694-135">**更簡單的變更通知**</span><span class="sxs-lookup"><span data-stu-id="c8694-135">**Simpler change notification**</span></span>

    <span data-ttu-id="c8694-136">當受監視資料夾或程式庫的內容變更時，檔案系統和 Shell API 都可以通知您的程式。</span><span class="sxs-lookup"><span data-stu-id="c8694-136">Both the file-system and the Shell API can notify your program when the contents of a monitored folder or library change.</span></span> <span data-ttu-id="c8694-137">不過，您可以使用 Shell API 來監視程式庫中的所有資料夾，並使用單一通知，即使程式庫中的資料夾可能儲存在不同的磁片磁碟機或甚至不同的電腦上也一樣。</span><span class="sxs-lookup"><span data-stu-id="c8694-137">Using the Shell API, however, you can monitor all the folders in the library with a single notification, even though the folder in the library may be stored on different drives or even different computers.</span></span>

-   <span data-ttu-id="c8694-138">**程式庫使用檔案屬性**</span><span class="sxs-lookup"><span data-stu-id="c8694-138">**Libraries use file properties**</span></span>

    <span data-ttu-id="c8694-139">程式可以使用檔案屬性，控制在開啟和儲存使用一般檔案對話方塊的作業期間所顯示的檔案。</span><span class="sxs-lookup"><span data-stu-id="c8694-139">Programs can use the file properties to control which files are displayed during open and save operations that use the common file dialog boxes.</span></span> <span data-ttu-id="c8694-140">程式也可以使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面存取檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="c8694-140">Programs can also have access to file properties by using the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interfaces.</span></span> <span data-ttu-id="c8694-141">您也可以設定 [一般檔案] 對話方塊，讓使用者更新與其內容相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="c8694-141">The common file dialog boxes can also be configured allow users to update the properties that are associated with their content.</span></span>

-   <span data-ttu-id="c8694-142">**程式可以建立專用程式庫**</span><span class="sxs-lookup"><span data-stu-id="c8694-142">**Programs can create dedicated libraries**</span></span>

    <span data-ttu-id="c8694-143">當現有的使用者程式庫不符合程式的需求時，就可以建立新的程式庫，例如，如果程式建立新類型的使用者內容。</span><span class="sxs-lookup"><span data-stu-id="c8694-143">A new library can be created when an existing user libraries does not meet the program's needs—for example, if a program creates a new type of user content.</span></span> <span data-ttu-id="c8694-144">您可以使用代表其內容的唯一圖示來設定新的程式庫，並讓程式庫易於在 Windows 檔案總管中識別。</span><span class="sxs-lookup"><span data-stu-id="c8694-144">The new library can be configured with a unique icon that represents their content and makes the library easy to identify in the Windows Explorer.</span></span>

## <a name="managing-folders-in-libraries"></a><span data-ttu-id="c8694-145">管理程式庫中的資料夾</span><span class="sxs-lookup"><span data-stu-id="c8694-145">Managing Folders in Libraries</span></span>

<span data-ttu-id="c8694-146">使用者可以藉由新增、移動或移除文件庫中的資料夾來組織其程式庫。</span><span class="sxs-lookup"><span data-stu-id="c8694-146">Users can organize their libraries by adding, moving, or removing folders in the library.</span></span> <span data-ttu-id="c8694-147">不過，並非所有資料夾都支援文件庫可提供的所有功能。</span><span class="sxs-lookup"><span data-stu-id="c8694-147">Not all folders, however, support all the functionality that a library can provide.</span></span> <span data-ttu-id="c8694-148">許多程式庫功能都需要快速存取資料夾的不同屬性，以及只能透過 Windows Search 使用的內容。</span><span class="sxs-lookup"><span data-stu-id="c8694-148">Many library features require quick access to the different properties of the folder and its contents that are only available through Windows Search.</span></span> <span data-ttu-id="c8694-149">若要提供完整的程式庫功能，必須能夠 Windows Search 的資料夾編制索引。</span><span class="sxs-lookup"><span data-stu-id="c8694-149">To provide full library functionality, a folder must be able to be indexed by Windows Search.</span></span>

<span data-ttu-id="c8694-150">程式庫不允許使用者新增未提供完整程式庫功能的資料夾。</span><span class="sxs-lookup"><span data-stu-id="c8694-150">A library does not allow a user to add folders that do not provide full library functionality.</span></span> <span data-ttu-id="c8694-151">不過， [**Shell 程式庫 API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) 可以新增這類資料夾。</span><span class="sxs-lookup"><span data-stu-id="c8694-151">The [**Shell Library API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) can, however, add such folders.</span></span> <span data-ttu-id="c8694-152">如果程式庫包含不支援完整程式庫功能的資料夾，程式庫將在安全模式下運作，並提供有限的功能。</span><span class="sxs-lookup"><span data-stu-id="c8694-152">If a library contains a folder that does not support full library functionality, the library will operate in a safe mode and provide a limited functionality.</span></span> <span data-ttu-id="c8694-153">下表說明支援完整程式庫功能的資料夾，以及不支援這些功能的資料夾。</span><span class="sxs-lookup"><span data-stu-id="c8694-153">The following table describes the folders that support full library functionality and those that do not.</span></span>



| <span data-ttu-id="c8694-154">支援完整程式庫功能的資料夾類型</span><span class="sxs-lookup"><span data-stu-id="c8694-154">Folder types that support full library functionality</span></span>                                                               | <span data-ttu-id="c8694-155">不支援完整程式庫功能的資料夾類型</span><span class="sxs-lookup"><span data-stu-id="c8694-155">Folder types that do not support full library functionality</span></span>                                  |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8694-156">固定和外部 NTFS 和 FAT32 硬碟。</span><span class="sxs-lookup"><span data-stu-id="c8694-156">Fixed and external NTFS and FAT32 hard drives.</span></span>                                                                     | <span data-ttu-id="c8694-157">抽取式磁碟機（例如 USB 快閃磁片磁碟機）或安全的數位 (SD) 記憶卡。</span><span class="sxs-lookup"><span data-stu-id="c8694-157">Removable drives such as USB flash drives or Secure Digital (SD) memory cards.</span></span>               |
| <span data-ttu-id="c8694-158">由 Windows Search （例如部門伺服器、Windows 7 或 Windows Vista 家用電腦）編制索引的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="c8694-158">File shares that are indexed by Windows Search such as departmental servers, Windows 7, or Windows Vista home PCs.</span></span> | <span data-ttu-id="c8694-159">卸載式媒體，例如 CD-ROM 或 DVD 媒體。</span><span class="sxs-lookup"><span data-stu-id="c8694-159">Removable media such as CD-ROM or DVD media.</span></span>                                                 |
| <span data-ttu-id="c8694-160">可離線使用的檔案共用，例如重新導向的 **我的檔** 資料夾或 Client-Side 快取。</span><span class="sxs-lookup"><span data-stu-id="c8694-160">File shares that are available offline such as a redirected **My Documents** folder or a Client-Side Cache.</span></span>        | <span data-ttu-id="c8694-161">無法離線使用或從遠端索引的網路共用，例如 NAS 磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c8694-161">Network shares that are neither available offline nor remotely indexed such as NAS drives.</span></span>   |
|                                                                                                                    | <span data-ttu-id="c8694-162">其他資料來源，例如 Microsoft SharePoint、Microsoft Exchange 和 Microsoft OneDrive。</span><span class="sxs-lookup"><span data-stu-id="c8694-162">Other data sources such as Microsoft SharePoint, Microsoft Exchange, and Microsoft OneDrive.</span></span> |



 

<span data-ttu-id="c8694-163">下圖顯示在安全模式下，程式庫內容的有限顯示。</span><span class="sxs-lookup"><span data-stu-id="c8694-163">The following image shows the limited display of library contents while in safe mode.</span></span>

![當程式庫處於安全模式時開啟對話方塊](images/libraries-supportedfolders.png)

## <a name="related-topics"></a><span data-ttu-id="c8694-165">相關主題</span><span class="sxs-lookup"><span data-stu-id="c8694-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8694-166">關於程式庫</span><span class="sxs-lookup"><span data-stu-id="c8694-166">About Libraries</span></span>](library-leverage-to-manage-folders.md)
</dt> <dt>

[<span data-ttu-id="c8694-167">**IShellLibrary**</span><span class="sxs-lookup"><span data-stu-id="c8694-167">**IShellLibrary**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[<span data-ttu-id="c8694-168">Shell 連結</span><span class="sxs-lookup"><span data-stu-id="c8694-168">Shell Links</span></span>](./links.md)
</dt> <dt>

[<span data-ttu-id="c8694-169">已知的資料夾</span><span class="sxs-lookup"><span data-stu-id="c8694-169">Known Folders</span></span>](known-folders.md)
</dt> <dt>

[<span data-ttu-id="c8694-170">程式庫描述架構</span><span class="sxs-lookup"><span data-stu-id="c8694-170">Library Description Schema</span></span>](library-schema-entry.md)
</dt> </dl>

 

 
