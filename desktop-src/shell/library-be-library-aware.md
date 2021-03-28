---
description: 本主題說明在程式中使用程式庫時要考慮的一些事項。
ms.assetid: 40ACC8F6-1416-4390-A8D7-8F924DC2C2FE
title: 在您的程式中使用程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2812a66b148d9bd16fc3951efab64a4d37afaaff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321119"
---
# <a name="using-libraries-in-your-program"></a><span data-ttu-id="5f7bf-103">在您的程式中使用程式庫</span><span class="sxs-lookup"><span data-stu-id="5f7bf-103">Using Libraries in your Program</span></span>

<span data-ttu-id="5f7bf-104">本主題說明在程式中使用程式庫時要考慮的一些事項。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-104">This topic describes some of the things to consider when using libraries in your program.</span></span>

<span data-ttu-id="5f7bf-105">本主題內容：</span><span class="sxs-lookup"><span data-stu-id="5f7bf-105">In this topic:</span></span>

-   [<span data-ttu-id="5f7bf-106">程式庫程式設計總覽</span><span class="sxs-lookup"><span data-stu-id="5f7bf-106">Library programming overview</span></span>](#library-programming-overview)
-   [<span data-ttu-id="5f7bf-107">使用程式庫進行程式設計</span><span class="sxs-lookup"><span data-stu-id="5f7bf-107">Programming with Libraries</span></span>](#programming-with-libraries)
    -   [<span data-ttu-id="5f7bf-108">從已知資料夾移至程式庫</span><span class="sxs-lookup"><span data-stu-id="5f7bf-108">Moving from Known Folders to Libraries</span></span>](#moving-from-known-folders-to-libraries)
    -   [<span data-ttu-id="5f7bf-109">家庭和共用程式庫</span><span class="sxs-lookup"><span data-stu-id="5f7bf-109">HomeGroup and shared libraries</span></span>](#homegroup-and-shared-libraries)
-   [<span data-ttu-id="5f7bf-110">使用具有程式庫的通用檔案對話方塊</span><span class="sxs-lookup"><span data-stu-id="5f7bf-110">Using a common file dialog box with libraries</span></span>](#using-a-common-file-dialog-box-with-libraries)
-   [<span data-ttu-id="5f7bf-111">從使用者介面啟用程式庫選擇</span><span class="sxs-lookup"><span data-stu-id="5f7bf-111">Enabling library selection from the user interface</span></span>](#enabling-library-selection-from-the-user-interface)
-   [<span data-ttu-id="5f7bf-112">存取程式中的程式庫內容</span><span class="sxs-lookup"><span data-stu-id="5f7bf-112">Accessing library content in a program</span></span>](#accessing-library-content-in-a-program)
    -   [<span data-ttu-id="5f7bf-113">使用 IShellLibrary 介面存取程式庫內容</span><span class="sxs-lookup"><span data-stu-id="5f7bf-113">Accessing library content with the IShellLibrary interface</span></span>](#accessing-library-content-with-the-ishelllibrary-interface)
    -   [<span data-ttu-id="5f7bf-114">使用 Shell Api 存取程式庫內容</span><span class="sxs-lookup"><span data-stu-id="5f7bf-114">Accessing library content with the Shell APIs</span></span>](#accessing-library-content-with-the-shell-apis)
-   [<span data-ttu-id="5f7bf-115">在文件庫中儲存使用者內容</span><span class="sxs-lookup"><span data-stu-id="5f7bf-115">Saving user content in a library</span></span>](#saving-user-content-in-a-library)
-   [<span data-ttu-id="5f7bf-116">支援程式庫中的拖放作業</span><span class="sxs-lookup"><span data-stu-id="5f7bf-116">Supporting drag-and-drop operations in a library</span></span>](#supporting-drag-and-drop-operations-in-a-library)
-   [<span data-ttu-id="5f7bf-117">保持與程式庫同步</span><span class="sxs-lookup"><span data-stu-id="5f7bf-117">Keeping in sync with a library</span></span>](#keeping-in-sync-with-a-library)
    -   [<span data-ttu-id="5f7bf-118">大量更新</span><span class="sxs-lookup"><span data-stu-id="5f7bf-118">Bulk Update</span></span>](#bulk-update)
    -   [<span data-ttu-id="5f7bf-119">Shell API 通知</span><span class="sxs-lookup"><span data-stu-id="5f7bf-119">Shell API Notification</span></span>](#shell-api-notification)
    -   [<span data-ttu-id="5f7bf-120">檔案系統 API 通知</span><span class="sxs-lookup"><span data-stu-id="5f7bf-120">File-system API Notification</span></span>](#file-system-api-notification)
-   [<span data-ttu-id="5f7bf-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="5f7bf-121">Related topics</span></span>](#related-topics)

## <a name="library-programming-overview"></a><span data-ttu-id="5f7bf-122">程式庫程式設計總覽</span><span class="sxs-lookup"><span data-stu-id="5f7bf-122">Library programming overview</span></span>

<span data-ttu-id="5f7bf-123">程式庫可讓使用者以有意義的方式組織其檔案內容，而不受檔案系統組織的限制。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-123">Libraries enable users to organize their file-based content in a way that is meaningful to them and not limited by the organization of the file system.</span></span> <span data-ttu-id="5f7bf-124">當您的程式支援程式庫時，它會讓使用者以對他們而言有意義的方式來尋找其內容，同時呈現與 Windows 7 使用者體驗一致的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-124">When your program supports libraries, it allows the user to find their content in a way that makes sense to them while presenting a user interface that is consistent with the Windows 7 user experience.</span></span> <span data-ttu-id="5f7bf-125">程式庫也可讓您的程式更容易找到儲存在不同資料夾或不同電腦上的檔案型內容。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-125">Libraries also make it easier for your program to locate file-based content that is stored in different folders or on different machines.</span></span>

<span data-ttu-id="5f7bf-126">本節中的主題描述如何將程式庫支援新增至您的程式，並利用程式庫所提供的新功能。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-126">The topics in this section describe how you can add library support to your program and take advantage of the new capabilities that libraries offer.</span></span> <span data-ttu-id="5f7bf-127">根據預設，Windows 7 會提供這項支援。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-127">Windows 7 provides some of this support by default.</span></span> <span data-ttu-id="5f7bf-128">如果您的程式不會修改目前使用的一般檔案對話方塊，則可能需要極少的額外程式設計來支援程式庫。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-128">If your program does not modify the common file dialog boxes that it currently uses, it might require very little additional programming to support libraries.</span></span>

<span data-ttu-id="5f7bf-129">本節說明程式庫所提供的一些主要功能，以及如何在您的程式中支援這些功能。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-129">This section describes some of the key features that libraries provide and how to support them in your program.</span></span> <span data-ttu-id="5f7bf-130">透過這種資訊，您可以決定哪些功能會從您的程式提供最佳的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-130">With this information, you can decide which features will provide the best user experience from your program.</span></span> <span data-ttu-id="5f7bf-131">如果您的程式自訂 [一般檔案] 對話方塊，本節中的資訊可協助您決定如何使用新的 [一般檔案] 對話方塊來使用程式庫，並在 Windows 7 中提供對等功能。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-131">If your program customizes the common file dialog boxes, the information in this section can help you determine how to use the new common file dialog boxes to use libraries and provide equivalent functionality in Windows 7.</span></span>

## <a name="programming-with-libraries"></a><span data-ttu-id="5f7bf-132">使用程式庫進行程式設計</span><span class="sxs-lookup"><span data-stu-id="5f7bf-132">Programming with Libraries</span></span>

<span data-ttu-id="5f7bf-133">Windows Shell 程式設計模型描述程式如何與 Windows Shell 程式設計物件互動。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-133">The Windows Shell programming model describes how a program interacts with Windows Shell programming objects.</span></span> <span data-ttu-id="5f7bf-134">雖然檔案系統物件（例如檔案和目錄）是由 Windows Shell 物件表示，但並非所有的 Windows Shell 物件都是以檔案系統表示。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-134">While file-system objects, such as files and directories, are represented by Windows Shell objects, not all Windows Shell objects are represented by the file-system.</span></span> <span data-ttu-id="5f7bf-135">例如，程式庫是沒有對等檔案系統的 Windows Shell 物件。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-135">Libraries, for example, are Windows Shell objects that do not have a file-system equivalent.</span></span> <span data-ttu-id="5f7bf-136">在程式中使用 Windows Shell 物件，可讓您的程式存取所有 Shell 物件，而不只是檔案系統物件。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-136">Using Windows Shell objects in your program enables your program to access all Shell objects and not just file-system objects.</span></span>

<span data-ttu-id="5f7bf-137">為了獲得最佳結果，您的程式會使用 [**Shell 程式庫 API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) 來與程式庫互動並存取其內容。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-137">For the best results, your program would use the [**Shell Library API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) to interact with libraries and access their contents.</span></span> <span data-ttu-id="5f7bf-138">程式庫包含資料夾和檔案等檔案系統專案時，程式庫不是檔案系統專案。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-138">While libraries contain file-system items such as folders and files, libraries are not file-system items.</span></span> <span data-ttu-id="5f7bf-139">因此，不能使用檔案系統 Api 來存取程式庫功能或程式庫內容。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-139">As such, file-system APIs cannot be used to access library features or library contents.</span></span>

<span data-ttu-id="5f7bf-140">如果您現有的程式目前使用許多檔案系統 Api，則您的程式仍可利用程式庫功能。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-140">If you have an existing program that currently uses many file-system APIs, your program can still take advantage of library features.</span></span> <span data-ttu-id="5f7bf-141">[**Shell 程式庫 API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)可提供程式庫中所找到專案的檔案系統參考，而這些檔案系統參考（例如檔案名和路徑）可以傳遞給現有程式中的現有檔案系統 api。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-141">The [**Shell Library API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) can provide file-system references to the items that are found in a library and these file-system references, such as the file name and path, can be passed to the existing file-system APIs that are in your existing program.</span></span>

### <a name="moving-from-known-folders-to-libraries"></a><span data-ttu-id="5f7bf-142">從已知資料夾移至程式庫</span><span class="sxs-lookup"><span data-stu-id="5f7bf-142">Moving from Known Folders to Libraries</span></span>

<span data-ttu-id="5f7bf-143">在 Windows 7 之前，通常會使用已知資料夾（例如我的檔資料夾）作為 [檔案儲存] 或 [檔案開啟] 作業中的預設資料夾。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-143">Before Windows 7 it was common to use a known folder, such as the My Documents folder, as the default folder in file save or file open operations.</span></span> <span data-ttu-id="5f7bf-144">在 Windows 7 中，應該使用對應的程式庫，如此一來，使用者就會在您的程式中與其他 Windows 7 程式（例如 Windows 檔案總管）擁有相同的體驗。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-144">In Windows 7, the corresponding library should be used so the user will have the same experience in your program as they would with other Windows 7 programs, such as the Windows Explorer.</span></span>

<span data-ttu-id="5f7bf-145">如果您目前在程式中使用 Windows Shell API，新增程式庫支援很簡單。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-145">If you are currently using the Windows Shell API in your program, adding library support is straightforward.</span></span> <span data-ttu-id="5f7bf-146">例如，如果您目前呼叫 [**SHGetKnownFolderItem**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderitem) 函式以取得我的檔資料夾的位置，則可以將我的檔已知資料夾的 [**KNOWNFOLDERID**](knownfolderid.md) 值取代為對應程式庫的 **KNOWNFOLDERID** 值。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-146">For example, if you currently call the [**SHGetKnownFolderItem**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderitem) function to get the location of the My Documents folder, you can replace the [**KNOWNFOLDERID**](knownfolderid.md) value of the My Documents known folder with the **KNOWNFOLDERID** value of the corresponding library.</span></span>

<span data-ttu-id="5f7bf-147">下表顯示已知資料夾的 [**KNOWNFOLDERID**](knownfolderid.md) 值與 Windows 7 中對應程式庫的 **KNOWNFOLDERID** 值之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-147">The following table shows the relationship between the [**KNOWNFOLDERID**](knownfolderid.md) values of known folders and the **KNOWNFOLDERID** value of the corresponding library in Windows 7.</span></span> 

| <span data-ttu-id="5f7bf-148">已知的資料夾 KNOWNFOLDERID 值</span><span class="sxs-lookup"><span data-stu-id="5f7bf-148">Known Folder KNOWNFOLDERID values</span></span> | <span data-ttu-id="5f7bf-149">程式庫 KNOWNFOLDERID 值</span><span class="sxs-lookup"><span data-stu-id="5f7bf-149">Library KNOWNFOLDERID values</span></span> |
|-----------------------------------|------------------------------|
| <span data-ttu-id="5f7bf-150">FOLDERID \_ 檔</span><span class="sxs-lookup"><span data-stu-id="5f7bf-150">FOLDERID\_Documents</span></span>               | <span data-ttu-id="5f7bf-151">FOLDERID \_ DocumentsLibrary</span><span class="sxs-lookup"><span data-stu-id="5f7bf-151">FOLDERID\_DocumentsLibrary</span></span>   |
| <span data-ttu-id="5f7bf-152">FOLDERID \_ 圖片</span><span class="sxs-lookup"><span data-stu-id="5f7bf-152">FOLDERID\_Pictures</span></span>                | <span data-ttu-id="5f7bf-153">FOLDERID \_ PicturesLibrary</span><span class="sxs-lookup"><span data-stu-id="5f7bf-153">FOLDERID\_PicturesLibrary</span></span>    |
| <span data-ttu-id="5f7bf-154">FOLDERID \_ 音樂</span><span class="sxs-lookup"><span data-stu-id="5f7bf-154">FOLDERID\_Music</span></span>                   | <span data-ttu-id="5f7bf-155">FOLDERID \_ MusicLibrary</span><span class="sxs-lookup"><span data-stu-id="5f7bf-155">FOLDERID\_MusicLibrary</span></span>       |
| <span data-ttu-id="5f7bf-156">FOLDERID \_ RecordedTV</span><span class="sxs-lookup"><span data-stu-id="5f7bf-156">FOLDERID\_RecordedTV</span></span>              | <span data-ttu-id="5f7bf-157">FOLDERID \_ RecordedTVLibrary</span><span class="sxs-lookup"><span data-stu-id="5f7bf-157">FOLDERID\_RecordedTVLibrary</span></span>  |



 

### <a name="homegroup-and-shared-libraries"></a><span data-ttu-id="5f7bf-158">家庭和共用程式庫</span><span class="sxs-lookup"><span data-stu-id="5f7bf-158">HomeGroup and shared libraries</span></span>

<span data-ttu-id="5f7bf-159">將程式庫支援新增至您的程式，將可支援在家庭集中共用程式庫。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-159">Adding library support to your program will enable support for shared libraries in a HomeGroup.</span></span> <span data-ttu-id="5f7bf-160">此家庭群組是由其 [**KNOWNFOLDERID**](knownfolderid.md) 值 [**FOLDERID 的 \_ 家庭**](knownfolderid.md)工作識別。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-160">The HomeGroup is identified by its [**KNOWNFOLDERID**](knownfolderid.md) value of [**FOLDERID\_HomeGroup**](knownfolderid.md).</span></span> <span data-ttu-id="5f7bf-161">您的程式可以在 [**IShellLibrary：： GetDefaultSaveFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-getdefaultsavefolder)方法的呼叫中設定 [**DEFAULTSAVEFOLDERTYPE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype)值，以找出使用者的私用或共用預設儲存位置。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-161">Your program can find identify the user's private or shared default save location by setting the [**DEFAULTSAVEFOLDERTYPE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype) value in the call to [**IShellLibrary::GetDefaultSaveFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-getdefaultsavefolder) method.</span></span>

## <a name="using-a-common-file-dialog-box-with-libraries"></a><span data-ttu-id="5f7bf-162">使用具有程式庫的通用檔案對話方塊</span><span class="sxs-lookup"><span data-stu-id="5f7bf-162">Using a common file dialog box with libraries</span></span>

<span data-ttu-id="5f7bf-163">使用具有文件庫的通用檔案對話方塊已更新 [一般檔案] 對話方塊，以支援 Windows 7 中的程式庫。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-163">Using a common file dialog box with libraries The common file dialog box has been updated to support libraries in Windows 7.</span></span> <span data-ttu-id="5f7bf-164">下圖顯示 [一般檔案] 對話方塊如何出現在 Windows 7 中的使用者。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-164">The following illustration shows how the common file dialog box appears to a user in Windows 7.</span></span>

![顯示文件庫的 [一般檔案] 對話方塊的螢幕擷取畫面](images/libraries-commonfiledialog.png)

<span data-ttu-id="5f7bf-166">在 Windows 7 中，如果您的程式目前顯示 [一般檔案] 對話方塊，而且沒有變更對話方塊範本或連結任何事件，它會自動顯示新的 Windows 7 版本的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-166">In Windows 7, if your program currently displays a common file dialog box and does not change the dialog box template or hook any of its events, it will display the new Windows 7 version of the dialog box automatically.</span></span> <span data-ttu-id="5f7bf-167">具體來說，在呼叫一般檔案對話方塊函式時， [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的 **lpfnHook**、 **hInstance**、 **lpTemplatename** 成員都必須是 **Null** ，而且 **OFN \_ ENABLEHOOK** 和 **OFN \_ ENABLETEMPLATE** 旗標必須是純文字。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-167">Specifically, in the call to the common file dialog box function, the **lpfnHook**, **hInstance**, **lpTemplatename** members of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure must be **NULL** and the **OFN\_ENABLEHOOK** and **OFN\_ENABLETEMPLATE** flags must be clear.</span></span>

<span data-ttu-id="5f7bf-168">在 Windows 7 中， [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)相關的介面會取代舊版 Windows 中使用的通用檔案對話方塊功能。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-168">In Windows 7, the [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)-related interfaces replace the common file dialog box functions that were used in earlier versions of Windows.</span></span> <span data-ttu-id="5f7bf-169">Windows 7 仍支援舊版的一般檔案對話方塊功能，但它們並不提供完整的 Windows 7 使用者體驗，也不支援程式庫。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-169">The earlier common file dialog box functions are still supported in Windows 7 but they do not provide the complete Windows 7 user experience and they do not support libraries.</span></span> <span data-ttu-id="5f7bf-170">**IFileDialog** 相關介面支援的一些新功能包括：</span><span class="sxs-lookup"><span data-stu-id="5f7bf-170">Some of the new features supported by the **IFileDialog**-related interfaces include:</span></span>

-   <span data-ttu-id="5f7bf-171">使用者可以存取 Windows 7 Windows 檔案總管所支援的檔案屬性來搜尋和選取檔案。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-171">The user can access the file properties supported by the Windows 7 Windows Explorer to search and select the files.</span></span>
-   <span data-ttu-id="5f7bf-172">程式可以使用 Shell 命名空間 API 中的介面和方法來處理專案。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-172">The program can use interfaces and methods from the Shell namespace API to work with the items.</span></span>
-   <span data-ttu-id="5f7bf-173">此程式可以使用資料驅動自訂模型（而不是資源檔案驅動的自訂模型），將新的控制項加入至 [一般檔案] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-173">The program can use a data-driven customization model instead of a resource-file-driven customization model to add new controls to the common file dialog boxes.</span></span>

<span data-ttu-id="5f7bf-174">當下列情況時，您應該使用 [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)相關的介面：</span><span class="sxs-lookup"><span data-stu-id="5f7bf-174">You should use the [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)-related interfaces when:</span></span>

-   <span data-ttu-id="5f7bf-175">您需要在 Windows 7 中為程式自訂 [一般檔案] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-175">you need to customize the common file dialog box for your program in Windows 7.</span></span> <span data-ttu-id="5f7bf-176">這可讓您的程式使用程式庫，並支援自訂對話方塊。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-176">This will allow your program to work with libraries and support customizing your dialog box.</span></span>
-   <span data-ttu-id="5f7bf-177">您希望使用者能夠從 [一般檔案] 對話方塊中選取多個檔案。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-177">you want the user to be able to select multiple files from a common file dialog box.</span></span> <span data-ttu-id="5f7bf-178">這可確保您取得所選物件的正確路徑，因為程式庫可以有儲存在不同資料夾中的內容。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-178">This will ensure you get the correct paths to the selected object because a library can have contents that are stored in different folders.</span></span>

<span data-ttu-id="5f7bf-179">如需有關 [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)相關介面的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="5f7bf-179">For more information on the [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)-related interfaces, see:</span></span>

-   [<span data-ttu-id="5f7bf-180">**IFileDialog**</span><span class="sxs-lookup"><span data-stu-id="5f7bf-180">**IFileDialog**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)
-   [<span data-ttu-id="5f7bf-181">**IFileOpenDialog**</span><span class="sxs-lookup"><span data-stu-id="5f7bf-181">**IFileOpenDialog**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)
-   [<span data-ttu-id="5f7bf-182">**IFileSaveDialog**</span><span class="sxs-lookup"><span data-stu-id="5f7bf-182">**IFileSaveDialog**</span></span>](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)
-   [<span data-ttu-id="5f7bf-183">**IFileDialogCustomize**</span><span class="sxs-lookup"><span data-stu-id="5f7bf-183">**IFileDialogCustomize**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)
-   [<span data-ttu-id="5f7bf-184">**IFileDialogEvents**</span><span class="sxs-lookup"><span data-stu-id="5f7bf-184">**IFileDialogEvents**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents)
-   [<span data-ttu-id="5f7bf-185">**IFileDialogControlEvents**</span><span class="sxs-lookup"><span data-stu-id="5f7bf-185">**IFileDialogControlEvents**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents)

## <a name="enabling-library-selection-from-the-user-interface"></a><span data-ttu-id="5f7bf-186">從使用者介面啟用程式庫選擇</span><span class="sxs-lookup"><span data-stu-id="5f7bf-186">Enabling library selection from the user interface</span></span>

<span data-ttu-id="5f7bf-187">如果您的程式允許使用者在 Windows 7 中選取資料夾，例如匯入或匯出功能，它應該也會允許使用者選取媒體櫃。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-187">If your program allows the user to select a folder, such as for import or export functions, in Windows 7, it should allow the user to select a library as well.</span></span> <span data-ttu-id="5f7bf-188">當系統提示您選取資料夾時， [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) 介面和 [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) 函數可讓使用者選取程式庫。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-188">The [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) interface and [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) function allow the user to select a library when prompted to select a folder.</span></span> <span data-ttu-id="5f7bf-189">**IFileOpenDialog** 介面優先于 **SHBrowseForFolder** 函數，因為 **IFileOpenDialog** 支援 Windows 7 使用者介面。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-189">The **IFileOpenDialog** interface is preferred over the **SHBrowseForFolder** function because **IFileOpenDialog** supports the Windows 7 user interface.</span></span>

<span data-ttu-id="5f7bf-190">若要允許使用者在使用 [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) 介面時選取資料夾，請呼叫 >setoptions \_ 並設定 fos PICKFOLDERS 旗標，並確定 \_ 已清除 [fos FORCEFILESYSTEM] 旗標。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-190">To allow users to select folders when using the [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) interface, call SetOptions with the FOS\_PICKFOLDERS flag set and make sure the FOS\_FORCEFILESYSTEM flag is clear.</span></span>


```C++
FILEOPENDIALOGOPTIONS fileOptions;

hr = fileOpenDialogBox->GetOptions(&fileOptions);
fileOptions = fileOptions | FOS_PICKFOLDERS | ~FOS_FORCEFILESYSTEM;
hr = fileOpenDialogBox->SetOptions(fileOptions);
```



<span data-ttu-id="5f7bf-191">若要允許使用者在呼叫 SHBrowseForFolder 函數時選取資料夾，請在 [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) 結構的 ulFlags 成員中，設定 BIF \_ USENEWUI 旗標，並清除 BIF \_ RETURNONLYFSDIRS 旗標。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-191">To allow users to select folders when calling the SHBrowseForFolder function, in the ulFlags member of the [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) structure, set the BIF\_USENEWUI flag and clear the BIF\_RETURNONLYFSDIRS flag.</span></span>


```C++
BROWSEINFO    browseInfo;
browseInfo.ulFlags = BIF_USENEWUI | ~BIF_RETURNONLYFSDIRS;
// Set other member values
pidl = SHBrowseForFolder(&browseInfo);
```



## <a name="accessing-library-content-in-a-program"></a><span data-ttu-id="5f7bf-192">存取程式中的程式庫內容</span><span class="sxs-lookup"><span data-stu-id="5f7bf-192">Accessing library content in a program</span></span>

<span data-ttu-id="5f7bf-193">若要存取程式庫的內容，您必須使用 Windows Shell API。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-193">To access the contents of a library, you must use the Windows Shell API.</span></span> <span data-ttu-id="5f7bf-194">無法使用檔案系統 API 的功能來存取程式庫內容，因為程式庫不是檔案系統物件。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-194">Functions of the file-system API cannot be used to access library contents because libraries are not file-system objects.</span></span> <span data-ttu-id="5f7bf-195">如果您的程式使用以檔案系統 API 為基礎的自訂檔案瀏覽器，它將無法流覽程式庫或存取程式庫內容。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-195">If your program uses a custom file browser that is based on the file-system API, it will not be able to browse libraries or access library content.</span></span>

<span data-ttu-id="5f7bf-196">本節說明如何存取程式庫內容，讓您可以選取更新程式以使用程式庫的最佳方式。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-196">This section describes how you can access library content so that you can select the best way to update your program to work with libraries.</span></span>

### <a name="accessing-library-content-with-the-ishelllibrary-interface"></a><span data-ttu-id="5f7bf-197">使用 IShellLibrary 介面存取程式庫內容</span><span class="sxs-lookup"><span data-stu-id="5f7bf-197">Accessing library content with the IShellLibrary interface</span></span>

<span data-ttu-id="5f7bf-198">程式存取程式庫內容最簡單的方式是使用 [**Shell 程式庫 API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-198">The easiest way for a program to access library content is to use the [**Shell Library API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary).</span></span> <span data-ttu-id="5f7bf-199">如果您正在處理使用檔案系統 API 的程式， **Shell 程式庫 API** 可以傳回程式庫的檔系統資料夾，以將現有程式碼的變更降至最低。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-199">If you are working on a program that uses the file-system API, the **Shell Library API** can return the file-system folders of a library, which minimizes the change to your existing program code.</span></span>


```C++
IShellLibrary *picturesLibrary;

hr = SHLoadLibraryFromKnownFolder(FOLDERID_PicturesLibrary, 
                                  STGM_READ, 
                                  IID_PPV_ARGS(&picturesLibrary));

// picturesLibrary now points to the user's picture library
    
IShellItemArray *pictureFolders; 

hr = pslLibrary->GetFolders(LFF_FORCEFILESYSTEM, IID_PPV_ARGS(&pictureFolders));

// pictureFolders now contains an array of Shell items that
// represent the folders found in the user's pictures library
```



### <a name="accessing-library-content-with-the-shell-apis"></a><span data-ttu-id="5f7bf-200">使用 Shell Api 存取程式庫內容</span><span class="sxs-lookup"><span data-stu-id="5f7bf-200">Accessing library content with the Shell APIs</span></span>

<span data-ttu-id="5f7bf-201">由於程式庫物件是 Shell 程式設計模型的一部分，因此可以與其他 Windows Shell Api 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-201">Because the library objects are part of the Shell programming model, they can be used with other Windows Shell APIs.</span></span> <span data-ttu-id="5f7bf-202">例如，您可以在程式中使用 [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) 和 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面，以及相關的協助程式函式來存取程式庫的內容，方式就如同使用檔案系統 api 來列舉資料夾和資料夾內容以存取內容一樣。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-202">For example you can use the [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) and [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interfaces in your program, along with related helper functions, to access the contents of a library in the same way as you would enumerate folders and folder contents to access content with the file system APIs.</span></span>

<span data-ttu-id="5f7bf-203">Windows Shell Api 支援兩種列舉模式來存取程式庫的內容：</span><span class="sxs-lookup"><span data-stu-id="5f7bf-203">The Windows Shell APIs support two enumeration modes to access the contents of a library:</span></span>

-   <span data-ttu-id="5f7bf-204">**流覽列舉**</span><span class="sxs-lookup"><span data-stu-id="5f7bf-204">**Browse enumeration**</span></span>

    <span data-ttu-id="5f7bf-205">流覽列舉是預設的列舉模式，會列舉程式庫資料夾的內容。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-205">Browse enumeration is the default enumeration mode and enumerates the contents of a library folder.</span></span> <span data-ttu-id="5f7bf-206">清除 SHCONTF \_ 導覽 \_ 列舉旗標以使用這個模式。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-206">Clear the SHCONTF\_NAVIGATION\_ENUM flag to use this mode.</span></span>

-   <span data-ttu-id="5f7bf-207">**導覽列舉**</span><span class="sxs-lookup"><span data-stu-id="5f7bf-207">**Navigation enumeration**</span></span>

    <span data-ttu-id="5f7bf-208">導覽列舉會列舉程式庫資料夾。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-208">Navigation enumeration enumerates the library folders.</span></span> <span data-ttu-id="5f7bf-209">將 SHCONTF \_ 導覽 \_ 列舉旗標設定為使用這個模式。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-209">Set the SHCONTF\_NAVIGATION\_ENUM flag to use this mode.</span></span>

<span data-ttu-id="5f7bf-210">如果您的程式使用自訂的樹狀目錄控制項來流覽使用者的資料夾，則在導覽列舉模式中列舉資料夾會提供程式庫資料夾的清單，與 Windows 檔案總管在 Windows 7 中列舉資料夾的方式一致。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-210">If your program uses a custom tree control to navigate the user's folders, enumerating the folders in the navigation enumeration mode will give you a list of a library's folders that is consistent with how the Windows Explorer enumerates folders in Windows 7.</span></span>

<span data-ttu-id="5f7bf-211">如需如何在程式中使用這些功能的範例，請參閱 Windows SDK 中的 ShellStorage 範例。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-211">For examples of how to uses these features in a program, see the ShellStorage sample in the Windows SDK.</span></span>

## <a name="saving-user-content-in-a-library"></a><span data-ttu-id="5f7bf-212">在文件庫中儲存使用者內容</span><span class="sxs-lookup"><span data-stu-id="5f7bf-212">Saving user content in a library</span></span>

<span data-ttu-id="5f7bf-213">您的程式可以將使用者內容儲存至文件庫，也可以儲存至文件庫中的資料夾。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-213">Your program can save user content to a library as well as to a folder in the library.</span></span> <span data-ttu-id="5f7bf-214">同樣地，使用者可以儲存至文件庫中的特定資料夾，也可以儲存至程式庫。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-214">Likewise, the user can save to a specific folder in a library or they can just save to the library.</span></span>

<span data-ttu-id="5f7bf-215">每個程式庫都有一個指定為預設儲存位置的資料夾。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-215">Every library has a folder that is designated as the default save location.</span></span> <span data-ttu-id="5f7bf-216">預設的儲存位置會在建立程式庫時定義;不過，使用者可以將預設儲存位置重新指派為文件庫中的任何資料夾。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-216">The default save location is defined when the library is created; however the user can reassign the default save location to be any folder in the library.</span></span> <span data-ttu-id="5f7bf-217">使用者不需要設定預設的儲存位置，而是可以選擇進行變更。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-217">While the user does not need to configure a default save location, they have the option to change it.</span></span> <span data-ttu-id="5f7bf-218">如果使用者刪除目前設定為預設儲存位置的資料夾，程式庫會自動將程式庫中的下一個資料夾設定為預設儲存位置。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-218">If the user deletes the folder that is currently set as the default save location, the library will automatically configure the next folder in the library to be the default save location.</span></span>

<span data-ttu-id="5f7bf-219">有數種方式可將使用者內容儲存至文件庫。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-219">There are several ways you can save user content to a library.</span></span>

-   <span data-ttu-id="5f7bf-220">**Shell API**</span><span class="sxs-lookup"><span data-stu-id="5f7bf-220">**Shell API**</span></span>

    <span data-ttu-id="5f7bf-221">如果您使用 Shell 程式設計模型並將 Shell 專案（如 [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem)、IStorage 或 IStream 所代表）儲存至程式庫物件，則會自動將 shell 專案儲存在程式庫的預設儲存位置。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-221">If you are using the Shell programming model and save a Shell item, as represented by an [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem), IStorage, or IStream, to a library object, the Shell item will be automatically stored in the default save location of the library.</span></span>

-   <span data-ttu-id="5f7bf-222">**檔案系統 API**</span><span class="sxs-lookup"><span data-stu-id="5f7bf-222">**File-system API**</span></span>

    <span data-ttu-id="5f7bf-223">如果您有現有的程式使用許多檔案系統 API 呼叫，您可以取得定義為程式庫預設儲存位置的資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-223">If you have an existing program that uses many file-system API calls, you can get a path to the folder that is defined as the library's default save location.</span></span> <span data-ttu-id="5f7bf-224">然後可以將資料夾路徑傳遞至檔案系統 API。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-224">The folder path can then be passed to a file-system API.</span></span>

<span data-ttu-id="5f7bf-225">如需如何在程式中使用這些功能的範例，請參閱 Windows SDK 中的 ShellStorage 範例。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-225">For examples of how to uses these features in a program, see the ShellStorage sample in the Windows SDK.</span></span>

## <a name="supporting-drag-and-drop-operations-in-a-library"></a><span data-ttu-id="5f7bf-226">支援程式庫中的拖放作業</span><span class="sxs-lookup"><span data-stu-id="5f7bf-226">Supporting drag-and-drop operations in a library</span></span>

<span data-ttu-id="5f7bf-227">如果您的程式支援拖放動作，則應該更新這些動作，以支援正確的程式庫互動。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-227">If your program supports drag-and-drop actions, those should be updated to support the correct library interaction.</span></span> <span data-ttu-id="5f7bf-228">如果將檔案放入文件庫中，則應該將卸載的檔案儲存在預設儲存位置。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-228">If a file is dropped into a library, the dropped file should be saved in the default save location.</span></span> <span data-ttu-id="5f7bf-229">如果資料夾已放入程式庫，則應該將放置的資料夾新增為程式庫的新資料夾。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-229">If a folder is dropped into a library, the dropped folder should be added as a new folder to the library.</span></span> <span data-ttu-id="5f7bf-230">如果將檔案放入非預設儲存位置的現有資料夾，則應該將檔案新增至選取的資料夾。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-230">If a file is dropped into an existing folder that is not the default save location, the file should be added to the selected folder.</span></span>

<span data-ttu-id="5f7bf-231">如需如何為您的程式拖放功能新增程式庫支援的範例，請參閱 Windows SDK 中的 ShellLibraryCommandLine 範例。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-231">For examples of how to add library support for your programs drag-and-drop functionality, see the ShellLibraryCommandLine sample in the Windows SDK.</span></span>

## <a name="keeping-in-sync-with-a-library"></a><span data-ttu-id="5f7bf-232">保持與程式庫同步</span><span class="sxs-lookup"><span data-stu-id="5f7bf-232">Keeping in sync with a library</span></span>

<span data-ttu-id="5f7bf-233">本主題說明程式如何將程式庫的內容保持在最新狀態。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-233">This topic describes how a program can keep its view of a library's content up-to-date.</span></span>

### <a name="bulk-update"></a><span data-ttu-id="5f7bf-234">大量更新</span><span class="sxs-lookup"><span data-stu-id="5f7bf-234">Bulk Update</span></span>

<span data-ttu-id="5f7bf-235">由於使用者可以在您的程式未執行時以互動方式修改程式庫的資料夾，因此，當程式開始探索並儲存程式庫的任何變更時，就應該呼叫 [**SHResolveLibrary**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary) 。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-235">Because the user can modify the folders of a library interactively when your program is not running, your program should call [**SHResolveLibrary**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary) when it starts to discover and store any changes to the library.</span></span> <span data-ttu-id="5f7bf-236">Shell API 提供 **SHResolveLibrary** 函式，可讓程式取得程式庫的目前內容，以及程式庫可能包含的任何資料夾的目前位置。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-236">The Shell API provides the **SHResolveLibrary** function to enable a program to get the current contents of a library and the current locations of any folders the library might contain.</span></span>

<span data-ttu-id="5f7bf-237">請注意， [**SHResolveLibrary**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary) 是封鎖函式，可能需要很長的時間才能傳回，取決於程式庫中的變更。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-237">Note that [**SHResolveLibrary**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary) is a blocking function that could take a long time to return depending on what has changed in the library.</span></span> <span data-ttu-id="5f7bf-238">因此，它不應該從 UI 執行緒呼叫。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-238">As such, it should not be called from a UI thread.</span></span>

<span data-ttu-id="5f7bf-239">當程式已更新為最新狀態之後，即可註冊變更通知以維護目前的觀點。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-239">After the program has been brought up-to-date, it can then register for change notifications to maintain a current view.</span></span>

### <a name="shell-api-notification"></a><span data-ttu-id="5f7bf-240">Shell API 通知</span><span class="sxs-lookup"><span data-stu-id="5f7bf-240">Shell API Notification</span></span>

<span data-ttu-id="5f7bf-241">Windows Shell API 提供 [**SHChangeNotifyRegister**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister) 函式，這是當非服務進程在程式庫中收到變更時的慣用方式。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-241">The Windows Shell API provides the [**SHChangeNotifyRegister**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister) function, which is the preferred way for non-service processes to be notified of a change in the library.</span></span>

<span data-ttu-id="5f7bf-242">若要使用 Windows Shell API 來偵測程式庫中專案的變更，請呼叫 [**SHChangeNotifyRegister**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister) 註冊您的程式，以取得程式庫資料夾中專案變更的通知。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-242">To detect changes to items within a library using the Windows Shell API, call [**SHChangeNotifyRegister**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister) to register your program for notifications of changes to items in a library folder.</span></span> <span data-ttu-id="5f7bf-243">如果任何程式庫或只是在特定的媒體櫃中有變更，此函式就會通知您的程式。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-243">This function can notify your program if there is a change in any library or just in a specific library.</span></span> <span data-ttu-id="5f7bf-244">當程式庫變更時，會立即傳送通知。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-244">Notifications are sent immediately when a library is changed.</span></span>

### <a name="file-system-api-notification"></a><span data-ttu-id="5f7bf-245">檔案系統 API 通知</span><span class="sxs-lookup"><span data-stu-id="5f7bf-245">File-system API Notification</span></span>

<span data-ttu-id="5f7bf-246">服務處理常式中必須使用檔案系統通知。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-246">File system notifications must be used in service processes.</span></span>

<span data-ttu-id="5f7bf-247">若要使用檔案系統 API 來偵測程式庫中專案的變更，請列舉程式庫中的資料夾，並針對每個要監視的資料夾呼叫 [**FindFirstChangeNotification**](/windows/win32/api/fileapi/nf-fileapi-findfirstchangenotificationa) 。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-247">To detect changes to items in a library using the file-system API, enumerate the folders in the library and call [**FindFirstChangeNotification**](/windows/win32/api/fileapi/nf-fileapi-findfirstchangenotificationa) for each folder to monitor.</span></span> <span data-ttu-id="5f7bf-248">當受監視的資料夾變更時，您的程式會收到通知。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-248">Your program will receive notification when a monitored folder changes.</span></span> <span data-ttu-id="5f7bf-249">若要尋找資料夾中已變更之檔案的特定檔案，請呼叫 [**ReadDirectoryChangesW**](/windows/win32/api/winbase/nf-winbase-readdirectorychangesw)。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-249">To find the specific file of files that changed in the folder, call [**ReadDirectoryChangesW**](/windows/win32/api/winbase/nf-winbase-readdirectorychangesw).</span></span> <span data-ttu-id="5f7bf-250">若要偵測程式庫描述檔案中的變更，請監視包含它的資料夾。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-250">To detect changes in the library description file, monitor the folder that contains it.</span></span> <span data-ttu-id="5f7bf-251">程式庫描述檔案可以在 FOLDERID 程式庫 [**資料夾 \_**](knownfolderid.md) 中找到。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-251">The library description file can be found in the [**FOLDERID\_Libraries**](knownfolderid.md) folder.</span></span> <span data-ttu-id="5f7bf-252">不過，程式庫描述檔案不應該開啟或修改。</span><span class="sxs-lookup"><span data-stu-id="5f7bf-252">The library description file, however, should not be opened or modified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f7bf-253">相關主題</span><span class="sxs-lookup"><span data-stu-id="5f7bf-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f7bf-254">關於程式庫</span><span class="sxs-lookup"><span data-stu-id="5f7bf-254">About Libraries</span></span>](library-leverage-to-manage-folders.md)
</dt> <dt>

[<span data-ttu-id="5f7bf-255">**IShellLibrary**</span><span class="sxs-lookup"><span data-stu-id="5f7bf-255">**IShellLibrary**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[<span data-ttu-id="5f7bf-256">Shell 連結</span><span class="sxs-lookup"><span data-stu-id="5f7bf-256">Shell Links</span></span>](./links.md)
</dt> <dt>

[<span data-ttu-id="5f7bf-257">已知的資料夾</span><span class="sxs-lookup"><span data-stu-id="5f7bf-257">Known Folders</span></span>](known-folders.md)
</dt> <dt>

[<span data-ttu-id="5f7bf-258">程式庫描述架構</span><span class="sxs-lookup"><span data-stu-id="5f7bf-258">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="5f7bf-259">**IID \_ PPV 引數 \_**</span><span class="sxs-lookup"><span data-stu-id="5f7bf-259">**IID\_PPV\_ARGS**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
