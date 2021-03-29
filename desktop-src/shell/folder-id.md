---
description: 使用命名空間物件之前，您需要識別它的方法。
ms.assetid: 54225481-a147-4d29-a642-24c9b59fc3ac
title: 取得資料夾的識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2e62454bf27f2c203f59aecb325cefe6537d2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991590"
---
# <a name="getting-a-folders-id"></a><span data-ttu-id="6917b-103">取得資料夾的識別碼</span><span class="sxs-lookup"><span data-stu-id="6917b-103">Getting a Folder's ID</span></span>

<span data-ttu-id="6917b-104">使用命名空間物件之前，您需要識別它的方法。</span><span class="sxs-lookup"><span data-stu-id="6917b-104">Before you can make use of a namespace object, you need a way to identify it.</span></span> <span data-ttu-id="6917b-105">這表示取得專案識別碼清單的指標 (PIDL) 或者，如果是檔案系統物件，則為它的路徑。</span><span class="sxs-lookup"><span data-stu-id="6917b-105">This means obtaining either its pointer to an item identifier list (PIDL) or, in the case of file system objects, its path.</span></span> <span data-ttu-id="6917b-106">本節將討論兩個較簡單的方法來取得物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="6917b-106">This section discusses two of the simpler ways to obtain object IDs.</span></span>

<span data-ttu-id="6917b-107">若要使用更強大的方法來處理任何資料夾，請使用 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面。</span><span class="sxs-lookup"><span data-stu-id="6917b-107">For a more powerful approach that will work with any folder, use the [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span> <span data-ttu-id="6917b-108">如需詳細資訊，請參閱 [取得資料夾內容的相關資訊](folder-info.md) 。</span><span class="sxs-lookup"><span data-stu-id="6917b-108">See [Getting Information About the Contents of a Folder](folder-info.md) for more details.</span></span>

-   <span data-ttu-id="6917b-109">[[OpenFiles] 對話方塊](#the-openfiles-dialog-box)</span><span class="sxs-lookup"><span data-stu-id="6917b-109">[The OpenFiles Dialog Box](#the-openfiles-dialog-box)</span></span>
-   <span data-ttu-id="6917b-110">[[SHBrowseForFolder] 對話方塊](#the-shbrowseforfolder-dialog-box)</span><span class="sxs-lookup"><span data-stu-id="6917b-110">[The SHBrowseForFolder Dialog Box](#the-shbrowseforfolder-dialog-box)</span></span>
-   [<span data-ttu-id="6917b-111">特殊資料夾和 CSIDLs</span><span class="sxs-lookup"><span data-stu-id="6917b-111">Special Folders and CSIDLs</span></span>](#special-folders-and-csidls)
-   [<span data-ttu-id="6917b-112">如何使用 CSIDLs 和 SHBrowseForFolder 的簡單範例</span><span class="sxs-lookup"><span data-stu-id="6917b-112">A Simple Example of How to Use CSIDLs and SHBrowseForFolder</span></span>](#a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder)

## <a name="the-openfiles-dialog-box"></a><span data-ttu-id="6917b-113">[OpenFiles] 對話方塊</span><span class="sxs-lookup"><span data-stu-id="6917b-113">The OpenFiles Dialog Box</span></span>

<span data-ttu-id="6917b-114">若要讓使用者流覽命名空間並選取資料夾，您的應用程式可以使用 [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) 介面。</span><span class="sxs-lookup"><span data-stu-id="6917b-114">To enable the user to navigate the namespace and select a folder, your application can use the [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) interface.</span></span> <span data-ttu-id="6917b-115">使用 **FOS \_ PICKFOLDERS** 旗標呼叫此介面會啟動 [挑選資料夾] 模式中的 [ [開啟](../dlgbox/open-and-save-as-dialog-boxes.md) 檔案] 通用對話方塊。</span><span class="sxs-lookup"><span data-stu-id="6917b-115">Calling this interface with the **FOS\_PICKFOLDERS** flag launches the [Open Files](../dlgbox/open-and-save-as-dialog-boxes.md) common dialog box in "pick folders" mode.</span></span>

<span data-ttu-id="6917b-116">若為 Windows Vista 和更新版本，建議使用這種方式來挑選資料夾。</span><span class="sxs-lookup"><span data-stu-id="6917b-116">For Windows Vista and later, this is the recommended way to pick folders.</span></span>

## <a name="the-shbrowseforfolder-dialog-box"></a><span data-ttu-id="6917b-117">[SHBrowseForFolder] 對話方塊</span><span class="sxs-lookup"><span data-stu-id="6917b-117">The SHBrowseForFolder Dialog Box</span></span>

<span data-ttu-id="6917b-118">若要讓使用者流覽命名空間並選取資料夾，您的應用程式可以直接叫用 [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera)。</span><span class="sxs-lookup"><span data-stu-id="6917b-118">To enable the user to navigate the namespace and select a folder, your application can simply invoke [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span></span> <span data-ttu-id="6917b-119">呼叫此函式會啟動一個對話方塊，其中 UI 的運作方式與 [ [開啟] 或 [另存](../dlgbox/open-and-save-as-dialog-boxes.md) 為] 通用對話方塊有點類似。</span><span class="sxs-lookup"><span data-stu-id="6917b-119">Calling this function launches a dialog box with a UI that works somewhat like the [Open or SaveAs](../dlgbox/open-and-save-as-dialog-boxes.md) common dialog boxes.</span></span>

<span data-ttu-id="6917b-120">當使用者選取資料夾時， [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) 會傳回資料夾的完整 PIDL 和其顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="6917b-120">When the user selects a folder, [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) returns the folder's fully qualified PIDL and its display name.</span></span> <span data-ttu-id="6917b-121">如果資料夾位於檔案系統中，則應用程式可以藉由呼叫 [**SHGetPathFromIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista)將 PIDL 轉換成路徑。</span><span class="sxs-lookup"><span data-stu-id="6917b-121">If the folder is in the file system, the application can convert the PIDL to a path by calling [**SHGetPathFromIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista).</span></span> <span data-ttu-id="6917b-122">應用程式也可以藉由指定根資料夾，來限制使用者可選取的資料夾範圍。</span><span class="sxs-lookup"><span data-stu-id="6917b-122">The application can also restrict the range of folders that the user can select from by specifying a root folder.</span></span> <span data-ttu-id="6917b-123">只會顯示命名空間中該根目錄下方的資料夾。</span><span class="sxs-lookup"><span data-stu-id="6917b-123">Only folders that are below that root in the namespace will appear.</span></span> <span data-ttu-id="6917b-124">下圖顯示 [ **SHBrowseForFolder** ] 對話方塊，並將根資料夾設定為 [Program Files]。</span><span class="sxs-lookup"><span data-stu-id="6917b-124">The following illustration shows the **SHBrowseForFolder** dialog box, with the root folder set to Program Files.</span></span>

![[流覽資料夾] 對話方塊的螢幕擷取畫面](images/shell1.png)

<span data-ttu-id="6917b-126">稍後會提供如何使用 [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) 的簡單範例。</span><span class="sxs-lookup"><span data-stu-id="6917b-126">A simple example of how to use [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) is provided later.</span></span>

## <a name="special-folders-and-csidls"></a><span data-ttu-id="6917b-127">特殊資料夾和 CSIDLs</span><span class="sxs-lookup"><span data-stu-id="6917b-127">Special Folders and CSIDLs</span></span>

<span data-ttu-id="6917b-128">系統會將一些常用的資料夾指定為 *特殊* 。</span><span class="sxs-lookup"><span data-stu-id="6917b-128">A number of commonly used folders are designated as *special* by the system.</span></span> <span data-ttu-id="6917b-129">這些資料夾具有妥善定義的用途，且大部分都存在於所有系統上。</span><span class="sxs-lookup"><span data-stu-id="6917b-129">These folders have a well-defined purpose, and most of them are present on all systems.</span></span> <span data-ttu-id="6917b-130">即使一開始並不存在，仍然會定義其名稱和位置，以便稍後加入。</span><span class="sxs-lookup"><span data-stu-id="6917b-130">Even if they are not present initially, their names and locations are still defined, so they can be added later.</span></span> <span data-ttu-id="6917b-131">特殊資料夾的集合包含所有系統的標準虛擬資料夾，例如 [印表機]、[我的檔] 和 [網路鄰近]。</span><span class="sxs-lookup"><span data-stu-id="6917b-131">The collection of special folders includes all of the system's standard virtual folders, such as Printers, My Documents, and Network Neighborhood.</span></span> <span data-ttu-id="6917b-132">它也包含一些標準的檔系統資料夾，例如 Program Files 和 System。</span><span class="sxs-lookup"><span data-stu-id="6917b-132">It also includes a number of standard file system folders, such as Program Files and System.</span></span>

<span data-ttu-id="6917b-133">雖然這些資料夾是所有系統的標準元件，但在命名空間中的名稱和位置可能會有所不同。</span><span class="sxs-lookup"><span data-stu-id="6917b-133">Even though the folders are a standard component of all systems, their names and locations in the namespace can vary.</span></span> <span data-ttu-id="6917b-134">例如，在某些系統上，系統目錄為 C： \\ Winnt \\ System32，而在其他系統上為 c： \\ Windows \\ system32。</span><span class="sxs-lookup"><span data-stu-id="6917b-134">For example, the System directory is C:\\Winnt\\System32 on some systems and C:\\Windows\\System32 on others.</span></span> <span data-ttu-id="6917b-135">在過去，環境變數提供了一種方法來判斷任何特定系統上特殊資料夾的名稱和位置。</span><span class="sxs-lookup"><span data-stu-id="6917b-135">In the past, environment variables provided a way to determine the name and location of a special folder on any particular system.</span></span> <span data-ttu-id="6917b-136">Shell 現在提供更健全且更有彈性的方式來識別特殊資料夾 [**CSIDLs**](csidl.md)。</span><span class="sxs-lookup"><span data-stu-id="6917b-136">The Shell now provides a more robust and flexible way to identify special folders, [**CSIDLs**](csidl.md).</span></span> <span data-ttu-id="6917b-137">您通常應該使用它們來取代環境變數。</span><span class="sxs-lookup"><span data-stu-id="6917b-137">You should generally use them instead of environment variables.</span></span>

<span data-ttu-id="6917b-138">CSIDLs 提供統一的方式來識別和尋找特殊資料夾，無論其名稱或位置是否在特定系統上。</span><span class="sxs-lookup"><span data-stu-id="6917b-138">CSIDLs provide a uniform way of identifying and locating special folders, regardless of their name or location on a particular system.</span></span> <span data-ttu-id="6917b-139">和環境變數不同的是，CSIDLs 可以與虛擬資料夾以及檔系統資料夾一起使用。</span><span class="sxs-lookup"><span data-stu-id="6917b-139">Unlike environment variables, CSIDLs can be used with virtual folders as well as file system folders.</span></span> <span data-ttu-id="6917b-140">每個特殊資料夾都有指派的唯一 CSIDL。</span><span class="sxs-lookup"><span data-stu-id="6917b-140">Each special folder has a unique CSIDL assigned to it.</span></span> <span data-ttu-id="6917b-141">例如，[Program Files file system] 資料夾具有 **CSIDL \_ Program \_ files** 的 CSIDL，而 [網路鄰近] 虛擬資料夾具有 **CSIDL \_ 網路** 的 CSIDL。</span><span class="sxs-lookup"><span data-stu-id="6917b-141">For example, the Program Files file system folder has a CSIDL of **CSIDL\_PROGRAM\_FILES**, and the Network Neighborhood virtual folder has a CSIDL of **CSIDL\_NETWORK**.</span></span>

<span data-ttu-id="6917b-142">CSIDL 會與數個 Shell 函式的其中一個搭配使用，以抓取特殊資料夾的 PIDL 或特殊檔系統資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="6917b-142">A CSIDL is used in conjunction with one of several Shell functions to retrieve a special folder's PIDL, or a special file system folder's path.</span></span> <span data-ttu-id="6917b-143">如果資料夾不存在於系統上，則您的應用程式可以藉由結合其 CSIDL 與 **CSIDL \_ 旗標 \_ 建立** 來強制建立。</span><span class="sxs-lookup"><span data-stu-id="6917b-143">If the folder does not exist on a system, your application can force it to be created by combining its CSIDL with **CSIDL\_FLAG\_CREATE**.</span></span> <span data-ttu-id="6917b-144">CSIDL 可以傳遞給下列函式：</span><span class="sxs-lookup"><span data-stu-id="6917b-144">The CSIDL can be passed to the following functions:</span></span>

-   <span data-ttu-id="6917b-145">[**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation)，可捕獲特殊資料夾的 PIDL。</span><span class="sxs-lookup"><span data-stu-id="6917b-145">[**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation), which retrieves the PIDL of a special folder.</span></span>
-   <span data-ttu-id="6917b-146">[**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)，它會抓取檔案系統特殊資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="6917b-146">[**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha), which retrieves the path of a file system special folder.</span></span>

<span data-ttu-id="6917b-147">請注意，這兩個函式是以5.0 版的 Shell 引進，並取代 [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) 和 [**SHGetSpecialFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) 函數。</span><span class="sxs-lookup"><span data-stu-id="6917b-147">Note that these two functions were introduced with version 5.0 of the Shell and supersede the [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) and [**SHGetSpecialFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) functions.</span></span>

## <a name="a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder"></a><span data-ttu-id="6917b-148">如何使用 CSIDLs 和 SHBrowseForFolder 的簡單範例</span><span class="sxs-lookup"><span data-stu-id="6917b-148">A Simple Example of How to Use CSIDLs and SHBrowseForFolder</span></span>

<span data-ttu-id="6917b-149">下列範例函式 PidlBrowse 會說明如何使用 CSIDLs 來取出資料夾的 PIDL，並使用 [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) 讓使用者選取資料夾。</span><span class="sxs-lookup"><span data-stu-id="6917b-149">The following sample function, PidlBrowse, illustrates how to use CSIDLs to retrieve a folder's PIDL, and use [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) to have the user select a folder.</span></span> <span data-ttu-id="6917b-150">它會傳回所選資料夾的 PIDL 和顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="6917b-150">It returns the PIDL and display name of the selected folder.</span></span>


```
LPITEMIDLIST PidlBrowse(HWND hwnd, int nCSIDL, LPSTR pszDisplayName)
{
    LPITEMIDLIST pidlRoot = NULL;
    LPITEMIDLIST pidlSelected = NULL;
    BROWSEINFO bi = {0};

    if(nCSIDL)
    {
        SHGetFolderLocation(hwnd, nCSIDL, NULL, NULL, &pidlRoot);
    }

    else
    {
        pidlRoot = NULL;
    }

    bi.hwndOwner = hwnd;
    bi.pidlRoot = pidlRoot;
    bi.pszDisplayName = pszDisplayName;
    bi.lpszTitle = "Choose a folder";
    bi.ulFlags = 0;
    bi.lpfn = NULL;
    bi.lParam = 0;

    pidlSelected = SHBrowseForFolder(&bi);

    if(pidlRoot)
    {
        CoTaskMemFree(pidlRoot);
    }

    return pidlSelected;
}
```



<span data-ttu-id="6917b-151">呼叫的應用程式會傳入視窗控制碼，此控制碼是 [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera)所需的。</span><span class="sxs-lookup"><span data-stu-id="6917b-151">The calling application passes in a window handle, which is needed by [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span></span> <span data-ttu-id="6917b-152">*NCSIDL* 參數是用來指定根資料夾的選擇性 CSIDL。</span><span class="sxs-lookup"><span data-stu-id="6917b-152">The *nCSIDL* parameter is an optional CSIDL that is used to specify a root folder.</span></span> <span data-ttu-id="6917b-153">只會顯示階層中根資料夾底下的資料夾。</span><span class="sxs-lookup"><span data-stu-id="6917b-153">Only folders below the root folder in the hierarchy will be displayed.</span></span> <span data-ttu-id="6917b-154">稍早所示的圖例是藉由呼叫此函數，並將 *nCSIDL* 設定為 **CSIDL \_ PROGRAM \_ FILES** 來產生。</span><span class="sxs-lookup"><span data-stu-id="6917b-154">The illustration shown earlier was generated by calling this function with *nCSIDL* set to **CSIDL\_PROGRAM\_FILES**.</span></span> <span data-ttu-id="6917b-155">呼叫的應用程式也會傳入字串緩衝區 *>pszdisplayname*，以便在 PidlBrowse 傳回時保存所選資料夾的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="6917b-155">The calling application also passes in a string buffer, *pszDisplayName*, to hold the display name of the selected folder when PidlBrowse returns.</span></span> <span data-ttu-id="6917b-156">呼叫應用程式的責任是使用 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)來釋放 **SHBrowseForFolder** 所傳回的 idlist.txt。</span><span class="sxs-lookup"><span data-stu-id="6917b-156">It is the responsibility of the calling application to free the IDList returned by **SHBrowseForFolder** using [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

 

 
