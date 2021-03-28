---
description: Windows 檔案總管是功能強大的資源流覽和管理應用程式。
ms.assetid: 879CE652-EDC0-4a14-925E-C83763133BE5
title: 使用 Windows 檔案總管開發
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b7b68d48f2d1becea23311847a5ce41b3776321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468780"
---
# <a name="developing-with-windows-explorer"></a><span data-ttu-id="f08f2-103">使用 Windows 檔案總管開發</span><span class="sxs-lookup"><span data-stu-id="f08f2-103">Developing with Windows Explorer</span></span>

<span data-ttu-id="f08f2-104">Windows 檔案總管是功能強大的資源流覽和管理應用程式。</span><span class="sxs-lookup"><span data-stu-id="f08f2-104">Windows Explorer is a powerful resource-browsing and management application.</span></span> <span data-ttu-id="f08f2-105">Windows 檔案總管可以透過 Explorer.exe 或 [**IExplorerBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) 介面，以整合的方式來存取。</span><span class="sxs-lookup"><span data-stu-id="f08f2-105">Windows Explorer can be accessed as an integrated whole through Explorer.exe or the [**IExplorerBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) interface.</span></span> <span data-ttu-id="f08f2-106">Windows 檔案總管 (Explorer.exe) 可以使用 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 或類似的函式，產生為個別的進程。</span><span class="sxs-lookup"><span data-stu-id="f08f2-106">Windows Explorer (Explorer.exe) can be spawned as a separate process using [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) or a similar function.</span></span>

> [!Note]  
> <span data-ttu-id="f08f2-107">Explorer.exe 的命令列選項記載于 Microsoft Windows 支援網站上的 [Windows 檔案總管 Command-Line 選項](https://support.microsoft.com/kb/152457)。</span><span class="sxs-lookup"><span data-stu-id="f08f2-107">Command-line options for Explorer.exe are documented on the Microsoft Windows Support site in the article [Windows Explorer Command-Line Options](https://support.microsoft.com/kb/152457).</span></span>

 

<span data-ttu-id="f08f2-108">您可以使用 [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID \_ ShellWindows) ，並使用 [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (clsid ShellBrowserWindow) 來建立新的 Windows 檔案總管實例，以探索並設計開啟 explorer 視窗 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f08f2-108">Open explorer windows can be discovered and programmed by using [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID\_ShellWindows), and new instances of Windows Explorer can be created by using [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (CLSID\_ShellBrowserWindow).</span></span>

<span data-ttu-id="f08f2-109">下列程式碼範例會示範如何使用 Windows 檔案總管 automation 模型，來建立和探索執行的 Explorer 視窗。</span><span class="sxs-lookup"><span data-stu-id="f08f2-109">The following code sample demonstrates how the Windows Explorer automation model can be used to create and discover explorer windows that are running.</span></span>


```
#define _WIN32_WINNT 0x0600
#define _WIN32_IE 0x0700
#define _UNICODE

#include <windows.h>
#include <shobjidl.h>
#include <shlobj.h>
#include <shlwapi.h>
#include <strsafe.h>
#include <propvarutil.h>
 
#pragma comment(lib, "shlwapi.lib")
#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "shell32.lib")
#pragma comment(lib, "propsys.lib")
 
// Use the Shell Windows object to find all of the explorer and IExplorer 
// windows and close them.
 
void CloseExplorerWindows()
{
    IShellWindows* psw;
    
    if (SUCCEEDED(CoCreateInstance(CLSID_ShellWindows, 
                                   NULL,  
                                   CLSCTX_LOCAL_SERVER, 
                                   IID_PPV_ARGS(&psw))))
    {
        VARIANT v = { VT_I4 };
        if (SUCCEEDED(psw->get_Count(&v.lVal)))
        {
            // Walk backward to make sure that the windows that close
            // do not cause the array to be reordered.
            while (--v.lVal >= 0)
            {
                IDispatch *pdisp;
                
                if (S_OK == psw->Item(v, &pdisp))
                {
                    IWebBrowser2 *pwb;
                    if (SUCCEEDED(pdisp->QueryInterface(IID_PPV_ARGS(&pwb))))
                    {
                        pwb->Quit();
                        pwb->Release();
                    }
                    pdisp->Release();
                }
            }
        }
        psw->Release();
    }
}
 
// Convert an IShellItem or IDataObject into a VARIANT that holds an IDList
// suitable for use with IWebBrowser2::Navigate2.
 
HRESULT InitVariantFromObject(IUnknown *punk, VARIANT *pvar)
{
    VariantInit(pvar);
 
    PIDLIST_ABSOLUTE pidl;
    HRESULT hr = SHGetIDListFromObject(punk, &pidl);
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromBuffer(pidl, ILGetSize(pidl), pvar);
        CoTaskMemFree(pidl);
    }
    return hr;
}
 
HRESULT ParseItemAsVariant(PCWSTR pszItem, IBindCtx *pbc, VARIANT *pvar)
{
    VariantInit(pvar);
 
    IShellItem *psi;
    HRESULT hr = SHCreateItemFromParsingName(pszItem, NULL, IID_PPV_ARGS(&psi));
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromObject(psi, pvar);
        psi->Release();
    }
    return hr;
}

HRESULT GetKnownFolderAsVariant(REFKNOWNFOLDERID kfid, VARIANT *pvar)
{
    VariantInit(pvar);
 
    PIDLIST_ABSOLUTE pidl;
    HRESULT hr = SHGetKnownFolderIDList(kfid, 0, NULL, &pidl);
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromBuffer(pidl, ILGetSize(pidl), pvar);
        CoTaskMemFree(pidl);
    }
    return hr;
}

HRESULT GetShellItemFromCommandLine(REFIID riid, void **ppv)
{
    *ppv = NULL;
    HRESULT hr = E_FAIL;

    int cArgs;
    PWSTR *ppszCmd = CommandLineToArgvW(GetCommandLineW(), &cArgs);
    if (ppszCmd && cArgs > 1)
    {
        WCHAR szSpec[MAX_PATH];
        StringCchCopyW(szSpec, ARRAYSIZE(szSpec), ppszCmd[1]);
        PathUnquoteSpacesW(szSpec);

        hr = szSpec[0] ? S_OK : E_FAIL;   // Protect against empty data
        if (SUCCEEDED(hr))
        {
            hr = SHCreateItemFromParsingName(szSpec, NULL, riid, ppv);
            if (FAILED(hr))
            {
                WCHAR szFolder[MAX_PATH];
                GetCurrentDirectoryW(ARRAYSIZE(szFolder), szFolder);

                hr = PathAppendW(szFolder, szSpec) ? S_OK : E_FAIL;
                if (SUCCEEDED(hr))
                {
                    hr = SHCreateItemFromParsingName(szFolder, NULL, riid, ppv);
                }
            }
        }
    }
    return hr;
}

HRESULT GetShellItemFromCommandLineAsVariant(VARIANT *pvar)
{
    VariantInit(pvar);

    IShellItem *psi;
    HRESULT hr = GetShellItemFromCommandLine(IID_PPV_ARGS(&psi));
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromObject(psi, pvar);
        psi->Release();
    }
    return hr;
}

void OpenWindow()
{
    IWebBrowser2 *pwb;
    HRESULT hr = CoCreateInstance(CLSID_ShellBrowserWindow, 
                                  NULL,
                                  CLSCTX_LOCAL_SERVER, 
                                  IID_PPV_ARGS(&pwb));
    if (SUCCEEDED(hr))
    {
        CoAllowSetForegroundWindow(pwb, 0);

        pwb->put_Left(100);
        pwb->put_Top(100);
        pwb->put_Height(600);
        pwb->put_Width(800);
 
        VARIANT varTarget = {0};
        hr = GetShellItemFromCommandLineAsVariant(&varTarget);
        if (FAILED(hr))
        {
            hr = GetKnownFolderAsVariant(FOLDERID_UsersFiles, &varTarget);
        }

        if (SUCCEEDED(hr))
        {
            VARIANT vEmpty = {0};
            hr = pwb->Navigate2(&varTarget, &vEmpty, &vEmpty, &vEmpty, &vEmpty);
            if (SUCCEEDED(hr))
            {
                pwb->put_Visible(VARIANT_TRUE);
            }
            VariantClear(&varTarget);
        }
        pwb->Release();
    }
}

int WINAPI WinMain(HINSTANCE, HINSTANCE, LPSTR, int)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |  COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CloseExplorerWindows();

        OpenWindow();

        CoUninitialize();
    }
    return 0;
}
```



<span data-ttu-id="f08f2-110">您可以使用 [IExplorerBrowser](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) 介面來裝載 Windows 檔案總管的工作區。</span><span class="sxs-lookup"><span data-stu-id="f08f2-110">The Windows Explorer client area can be hosted by using the [IExplorerBrowser](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) interface.</span></span> <span data-ttu-id="f08f2-111">Windows 檔案總管用戶端和命名空間樹狀目錄控制項是 Windows Vista 和更新版本的標準元件。</span><span class="sxs-lookup"><span data-stu-id="f08f2-111">The Windows Explorer client and the namespace tree controls are standard components of Windows Vista and later.</span></span> <span data-ttu-id="f08f2-112">開發人員可以重複使用介面做為建立元件。</span><span class="sxs-lookup"><span data-stu-id="f08f2-112">Developers can reuse the interfaces as building components.</span></span> <span data-ttu-id="f08f2-113">這些控制項的其中一種常見用法是建立適用于問題領域的自訂瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="f08f2-113">One common use of these controls is to create customized explorers appropriate to the problem domain.</span></span>

<span data-ttu-id="f08f2-114">Windows 檔案總管中的控制項分類為下列功能類別：</span><span class="sxs-lookup"><span data-stu-id="f08f2-114">The controls in Windows Explorer are classified into the following functional categories:</span></span>

-   [<span data-ttu-id="f08f2-115">導覽控制項</span><span class="sxs-lookup"><span data-stu-id="f08f2-115">Navigation Controls</span></span>](#navigation-controls)
-   [<span data-ttu-id="f08f2-116">命令控制項</span><span class="sxs-lookup"><span data-stu-id="f08f2-116">Command Controls</span></span>](#command-controls)
-   [<span data-ttu-id="f08f2-117">屬性和預覽控制項</span><span class="sxs-lookup"><span data-stu-id="f08f2-117">Property and Preview Controls</span></span>](#property-and-preview-controls)
-   [<span data-ttu-id="f08f2-118">篩選和查看控制項</span><span class="sxs-lookup"><span data-stu-id="f08f2-118">Filtering and View Controls</span></span>](#filtering-and-view-controls)
-   [<span data-ttu-id="f08f2-119">Listview 控制項</span><span class="sxs-lookup"><span data-stu-id="f08f2-119">Listview Control</span></span>](#listview-control)

## <a name="navigation-controls"></a><span data-ttu-id="f08f2-120">導覽控制項</span><span class="sxs-lookup"><span data-stu-id="f08f2-120">Navigation Controls</span></span>

<span data-ttu-id="f08f2-121">導覽控制項協助使用者判斷內容和流覽相關聯的邏輯網域空間，稱為 pagespace。</span><span class="sxs-lookup"><span data-stu-id="f08f2-121">Navigation controls assist users in determining context and navigating the associated logical domain space, called the pagespace.</span></span> <span data-ttu-id="f08f2-122">例如，Windows 檔案總管的 pagespace 是 Shell 命名空間。</span><span class="sxs-lookup"><span data-stu-id="f08f2-122">For example, the pagespace for Windows Explorer is the Shell namespace.</span></span> <span data-ttu-id="f08f2-123">Pagespaces 包含零或多個頁面。</span><span class="sxs-lookup"><span data-stu-id="f08f2-123">Pagespaces are composed of zero or more pages.</span></span>

<span data-ttu-id="f08f2-124">下表列出並描述 Windows Vista 和更新版本作業系統 Windows 檔案總管中可用的導覽控制項。</span><span class="sxs-lookup"><span data-stu-id="f08f2-124">The following table lists and describes the navigation controls available in Windows Explorer in the Windows Vista and later operating systems.</span></span>



| <span data-ttu-id="f08f2-125">導覽控制項</span><span class="sxs-lookup"><span data-stu-id="f08f2-125">Navigation control</span></span>               | <span data-ttu-id="f08f2-126">Description</span><span class="sxs-lookup"><span data-stu-id="f08f2-126">Description</span></span>                                                                                                                                                                                |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f08f2-127">網址列 (階層連結控制項) </span><span class="sxs-lookup"><span data-stu-id="f08f2-127">Address Bar (Breadcrumb control)</span></span> | <span data-ttu-id="f08f2-128">顯示目前頁面在 pagespace 中的位址。</span><span class="sxs-lookup"><span data-stu-id="f08f2-128">Displays the address of the current page in the pagespace.</span></span> <span data-ttu-id="f08f2-129">您可以按一下階層連結按鈕，流覽至 pagespace 中的任何上階。</span><span class="sxs-lookup"><span data-stu-id="f08f2-129">Breadcrumb buttons can be clicked to navigate to any ancestor in the pagespace.</span></span> <span data-ttu-id="f08f2-130">使用者也可以輸入要流覽的 Url 和路徑。</span><span class="sxs-lookup"><span data-stu-id="f08f2-130">Users can also type URLs and paths to navigate.</span></span> |
| <span data-ttu-id="f08f2-131">資料夾樹狀結構</span><span class="sxs-lookup"><span data-stu-id="f08f2-131">Folder Tree</span></span>                      | <span data-ttu-id="f08f2-132">提供新版本的樹狀目錄控制項，並針對大型 pagespaces 進行優化。</span><span class="sxs-lookup"><span data-stu-id="f08f2-132">Provides a new version of a tree control, optimized for large pagespaces.</span></span>                                                                                                                  |
| <span data-ttu-id="f08f2-133">出差</span><span class="sxs-lookup"><span data-stu-id="f08f2-133">Travel</span></span>                           | <span data-ttu-id="f08f2-134">透過 web 樣式按鈕（例如 [ **上一步** ] 和 [ **轉寄**]）啟用相對導覽。</span><span class="sxs-lookup"><span data-stu-id="f08f2-134">Enables relative navigation through web-style buttons such as **Back** and **Forward**.</span></span>                                                                                                    |
| <span data-ttu-id="f08f2-135">標題</span><span class="sxs-lookup"><span data-stu-id="f08f2-135">Title</span></span>                            | <span data-ttu-id="f08f2-136">顯示目前的瀏覽器名稱和內容。</span><span class="sxs-lookup"><span data-stu-id="f08f2-136">Displays the current explorer name and context.</span></span>                                                                                                                                            |
| <span data-ttu-id="f08f2-137">Pagespace</span><span class="sxs-lookup"><span data-stu-id="f08f2-137">Pagespace</span></span>                        | <span data-ttu-id="f08f2-138">顯示 pagespace 的最新分支。</span><span class="sxs-lookup"><span data-stu-id="f08f2-138">Displays the current branch of the pagespace.</span></span> <span data-ttu-id="f08f2-139">頁面可以依不同準則排序。</span><span class="sxs-lookup"><span data-stu-id="f08f2-139">Pages can be ordered by different criteria.</span></span> <span data-ttu-id="f08f2-140">使用者可以按一下頁面來流覽至該頁面。</span><span class="sxs-lookup"><span data-stu-id="f08f2-140">Users can click a page to navigate to it.</span></span>                                                        |



 

## <a name="command-controls"></a><span data-ttu-id="f08f2-141">命令控制項</span><span class="sxs-lookup"><span data-stu-id="f08f2-141">Command Controls</span></span>

<span data-ttu-id="f08f2-142">命令控制項會向使用者通告 Windows 檔案總管的特性和功能。</span><span class="sxs-lookup"><span data-stu-id="f08f2-142">Command controls advertise the features and functionality of the Windows Explorer to users.</span></span> <span data-ttu-id="f08f2-143">這些控制項會執行一個選定專案或專案特定的一般動作或動作。</span><span class="sxs-lookup"><span data-stu-id="f08f2-143">These controls perform either general actions or actions specific to one selected item or items.</span></span>



| <span data-ttu-id="f08f2-144">命令控制項</span><span class="sxs-lookup"><span data-stu-id="f08f2-144">Command control</span></span> | <span data-ttu-id="f08f2-145">Description</span><span class="sxs-lookup"><span data-stu-id="f08f2-145">Description</span></span>                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f08f2-146">工具列</span><span class="sxs-lookup"><span data-stu-id="f08f2-146">Toolbar</span></span>         | <span data-ttu-id="f08f2-147"> (新版本的命令工具列，顯示常用命令的按鈕) 。</span><span class="sxs-lookup"><span data-stu-id="f08f2-147">Displays buttons for commonly used commands (a new version of a command toolbar).</span></span> <span data-ttu-id="f08f2-148">自訂選項包括下拉式按鈕、分割按鈕、選擇性的描述性文字，以及溢位區。</span><span class="sxs-lookup"><span data-stu-id="f08f2-148">Customization options include drop-down buttons, split buttons, optional descriptive text, and an overflow area.</span></span> |
| <span data-ttu-id="f08f2-149">主圖</span><span class="sxs-lookup"><span data-stu-id="f08f2-149">Hero</span></span>            | <span data-ttu-id="f08f2-150">顯示為工具列中央的單一選擇性自訂控制項。</span><span class="sxs-lookup"><span data-stu-id="f08f2-150">Appears as a single, optional, custom control in the center of the toolbar.</span></span> <span data-ttu-id="f08f2-151">它代表目前內容的主要命令。</span><span class="sxs-lookup"><span data-stu-id="f08f2-151">It represents the primary command for the current context.</span></span>                                                             |
| <span data-ttu-id="f08f2-152">功能表列</span><span class="sxs-lookup"><span data-stu-id="f08f2-152">Menu Bar</span></span>        | <span data-ttu-id="f08f2-153">透過功能表提供命令。</span><span class="sxs-lookup"><span data-stu-id="f08f2-153">Presents commands through menus.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="f08f2-154">操作功能表</span><span class="sxs-lookup"><span data-stu-id="f08f2-154">Context Menu</span></span>    | <span data-ttu-id="f08f2-155">列出內容的相關可用命令子集，這些命令是以滑鼠右鍵按一下專案的結果來顯示。</span><span class="sxs-lookup"><span data-stu-id="f08f2-155">Lists a contextually relevant subset of available commands that are displayed as a result of right-clicking an item.</span></span>                                                                               |



 

## <a name="property-and-preview-controls"></a><span data-ttu-id="f08f2-156">屬性和預覽控制項</span><span class="sxs-lookup"><span data-stu-id="f08f2-156">Property and Preview Controls</span></span>

<span data-ttu-id="f08f2-157">屬性和預覽控制項可用來預覽專案，以及用來查看和編輯專案屬性。</span><span class="sxs-lookup"><span data-stu-id="f08f2-157">Property and preview controls are used to preview items, and to view and edit item properties.</span></span>



| <span data-ttu-id="f08f2-158">控制</span><span class="sxs-lookup"><span data-stu-id="f08f2-158">Control</span></span>    | <span data-ttu-id="f08f2-159">描述</span><span class="sxs-lookup"><span data-stu-id="f08f2-159">Description</span></span>                                                                                                                                                                                                                                        |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f08f2-160">預覽</span><span class="sxs-lookup"><span data-stu-id="f08f2-160">Preview</span></span>    | <span data-ttu-id="f08f2-161">顯示所選取專案的預覽，例如縮圖或即時圖示。</span><span class="sxs-lookup"><span data-stu-id="f08f2-161">Displays a preview of the selected item, such as a thumbnail or a Live Icon.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="f08f2-162">屬性</span><span class="sxs-lookup"><span data-stu-id="f08f2-162">Properties</span></span> | <span data-ttu-id="f08f2-163">顯示所選取專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="f08f2-163">Displays properties of the selected item.</span></span> <span data-ttu-id="f08f2-164">針對多個選取專案，它會顯示所選取專案群組的屬性摘要。</span><span class="sxs-lookup"><span data-stu-id="f08f2-164">For multiple selections, it displays a summary of properties for the selected group of items.</span></span> <span data-ttu-id="f08f2-165">若為 null 選取範圍，它會顯示目前頁面的屬性摘要 (listview) 的內容。</span><span class="sxs-lookup"><span data-stu-id="f08f2-165">For a null selection, it displays a summary of properties for the current page (contents of the listview).</span></span> |



 

## <a name="filtering-and-view-controls"></a><span data-ttu-id="f08f2-166">篩選和查看控制項</span><span class="sxs-lookup"><span data-stu-id="f08f2-166">Filtering and View Controls</span></span>

<span data-ttu-id="f08f2-167">篩選和 view 控制項可用來管理 listview 中的專案集合，以及變更 listview 中專案的呈現方式。</span><span class="sxs-lookup"><span data-stu-id="f08f2-167">Filtering and view controls are used to manipulate the set of items in the listview and to change the presentation of items in the listview.</span></span>



| <span data-ttu-id="f08f2-168">控制</span><span class="sxs-lookup"><span data-stu-id="f08f2-168">Control</span></span>   | <span data-ttu-id="f08f2-169">描述</span><span class="sxs-lookup"><span data-stu-id="f08f2-169">Description</span></span>                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f08f2-170">Filter</span><span class="sxs-lookup"><span data-stu-id="f08f2-170">Filter</span></span>    | <span data-ttu-id="f08f2-171">根據列為資料行的屬性，篩選或排列 listview 中的專案。</span><span class="sxs-lookup"><span data-stu-id="f08f2-171">Filters or arranges items in a listview based on properties listed as columns.</span></span> <span data-ttu-id="f08f2-172">按一下資料行時，會依該屬性排序。</span><span class="sxs-lookup"><span data-stu-id="f08f2-172">Clicking on a column sorts by that property.</span></span> |
| <span data-ttu-id="f08f2-173">Wordwheel</span><span class="sxs-lookup"><span data-stu-id="f08f2-173">Wordwheel</span></span> | <span data-ttu-id="f08f2-174">根據輸入文字字串，以動態和累加方式篩選 listview 中顯示的專案。</span><span class="sxs-lookup"><span data-stu-id="f08f2-174">Dynamically and incrementally filters the displayed items in a listview based on an input text string.</span></span>                      |
| <span data-ttu-id="f08f2-175">檢視</span><span class="sxs-lookup"><span data-stu-id="f08f2-175">View</span></span>      | <span data-ttu-id="f08f2-176">可讓使用者變更 listview 控制項的視圖模式。</span><span class="sxs-lookup"><span data-stu-id="f08f2-176">Enables the user to change the view mode of a listview control.</span></span> <span data-ttu-id="f08f2-177">滑杆可以用來決定圖示大小。</span><span class="sxs-lookup"><span data-stu-id="f08f2-177">A slider can be used to determine icon size.</span></span>                |



 

## <a name="listview-control"></a><span data-ttu-id="f08f2-178">Listview 控制項</span><span class="sxs-lookup"><span data-stu-id="f08f2-178">Listview Control</span></span>

<span data-ttu-id="f08f2-179">Listview 控制項可用來以四種視圖模式之一來查看一組專案：詳細資料、磚、圖示或全景。</span><span class="sxs-lookup"><span data-stu-id="f08f2-179">The listview control is used to view a set of items in one of four view modes: details, tiles, icons, or panorama.</span></span> <span data-ttu-id="f08f2-180">Listview 控制項也可讓使用者選取和啟用一或多個專案。</span><span class="sxs-lookup"><span data-stu-id="f08f2-180">The listview control also enables the user to select and activate one or more items.</span></span>

> [!Caution]  
> <span data-ttu-id="f08f2-181">雖然其中有些控制項的名稱和（或）功能類似于標準 Windows Presentation Foundation (WPF) 控制項命名空間中找到的控制項，但它們是不同的類別。</span><span class="sxs-lookup"><span data-stu-id="f08f2-181">Although some of these controls have names and/or functionality that is similar to standard Windows Presentation Foundation (WPF) controls found in the System.Windows.Controls namespace, they are distinct classes.</span></span>

 

<span data-ttu-id="f08f2-182">這些個別的控制項主要是透過使用者互動或由控制項本身所產生的事件來共同運作。</span><span class="sxs-lookup"><span data-stu-id="f08f2-182">These separate controls work together largely through events generated either by user interaction or by the controls themselves.</span></span> <span data-ttu-id="f08f2-183">下表顯示三個主要事件類別目錄。</span><span class="sxs-lookup"><span data-stu-id="f08f2-183">The following table shows the three primary event categories.</span></span>



| <span data-ttu-id="f08f2-184">事件類別目錄</span><span class="sxs-lookup"><span data-stu-id="f08f2-184">Event category</span></span> | <span data-ttu-id="f08f2-185">範例</span><span class="sxs-lookup"><span data-stu-id="f08f2-185">Example</span></span>                                                       |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="f08f2-186">導覽</span><span class="sxs-lookup"><span data-stu-id="f08f2-186">Navigation</span></span>     | <span data-ttu-id="f08f2-187">從一個頁面前往另一個。</span><span class="sxs-lookup"><span data-stu-id="f08f2-187">Going from one page to another.</span></span>                               |
| <span data-ttu-id="f08f2-188">選取</span><span class="sxs-lookup"><span data-stu-id="f08f2-188">Selection</span></span>      | <span data-ttu-id="f08f2-189">變更 listview 中目前的選取範圍。</span><span class="sxs-lookup"><span data-stu-id="f08f2-189">Changing the current selection in the listview.</span></span>               |
| <span data-ttu-id="f08f2-190">查看變更</span><span class="sxs-lookup"><span data-stu-id="f08f2-190">View Change</span></span>    | <span data-ttu-id="f08f2-191">變更 listview 中的呈現順序或視圖模式。</span><span class="sxs-lookup"><span data-stu-id="f08f2-191">Changing the presentation order or view mode in the listview.</span></span> |



 

 

 
