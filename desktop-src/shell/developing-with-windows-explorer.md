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
# <a name="developing-with-windows-explorer"></a>使用 Windows 檔案總管開發

Windows 檔案總管是功能強大的資源流覽和管理應用程式。 Windows 檔案總管可以透過 Explorer.exe 或 [**IExplorerBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) 介面，以整合的方式來存取。 Windows 檔案總管 (Explorer.exe) 可以使用 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 或類似的函式，產生為個別的進程。

> [!Note]  
> Explorer.exe 的命令列選項記載于 Microsoft Windows 支援網站上的 [Windows 檔案總管 Command-Line 選項](https://support.microsoft.com/kb/152457)。

 

您可以使用 [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID \_ ShellWindows) ，並使用 [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (clsid ShellBrowserWindow) 來建立新的 Windows 檔案總管實例，以探索並設計開啟 explorer 視窗 \_ 。

下列程式碼範例會示範如何使用 Windows 檔案總管 automation 模型，來建立和探索執行的 Explorer 視窗。


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



您可以使用 [IExplorerBrowser](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) 介面來裝載 Windows 檔案總管的工作區。 Windows 檔案總管用戶端和命名空間樹狀目錄控制項是 Windows Vista 和更新版本的標準元件。 開發人員可以重複使用介面做為建立元件。 這些控制項的其中一種常見用法是建立適用于問題領域的自訂瀏覽器。

Windows 檔案總管中的控制項分類為下列功能類別：

-   [導覽控制項](#navigation-controls)
-   [命令控制項](#command-controls)
-   [屬性和預覽控制項](#property-and-preview-controls)
-   [篩選和查看控制項](#filtering-and-view-controls)
-   [Listview 控制項](#listview-control)

## <a name="navigation-controls"></a>導覽控制項

導覽控制項協助使用者判斷內容和流覽相關聯的邏輯網域空間，稱為 pagespace。 例如，Windows 檔案總管的 pagespace 是 Shell 命名空間。 Pagespaces 包含零或多個頁面。

下表列出並描述 Windows Vista 和更新版本作業系統 Windows 檔案總管中可用的導覽控制項。



| 導覽控制項               | Description                                                                                                                                                                                |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 網址列 (階層連結控制項)  | 顯示目前頁面在 pagespace 中的位址。 您可以按一下階層連結按鈕，流覽至 pagespace 中的任何上階。 使用者也可以輸入要流覽的 Url 和路徑。 |
| 資料夾樹狀結構                      | 提供新版本的樹狀目錄控制項，並針對大型 pagespaces 進行優化。                                                                                                                  |
| 出差                           | 透過 web 樣式按鈕（例如 [ **上一步** ] 和 [ **轉寄**]）啟用相對導覽。                                                                                                    |
| 標題                            | 顯示目前的瀏覽器名稱和內容。                                                                                                                                            |
| Pagespace                        | 顯示 pagespace 的最新分支。 頁面可以依不同準則排序。 使用者可以按一下頁面來流覽至該頁面。                                                        |



 

## <a name="command-controls"></a>命令控制項

命令控制項會向使用者通告 Windows 檔案總管的特性和功能。 這些控制項會執行一個選定專案或專案特定的一般動作或動作。



| 命令控制項 | Description                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 工具列         |  (新版本的命令工具列，顯示常用命令的按鈕) 。 自訂選項包括下拉式按鈕、分割按鈕、選擇性的描述性文字，以及溢位區。 |
| 主圖            | 顯示為工具列中央的單一選擇性自訂控制項。 它代表目前內容的主要命令。                                                             |
| 功能表列        | 透過功能表提供命令。                                                                                                                                                                   |
| 操作功能表    | 列出內容的相關可用命令子集，這些命令是以滑鼠右鍵按一下專案的結果來顯示。                                                                               |



 

## <a name="property-and-preview-controls"></a>屬性和預覽控制項

屬性和預覽控制項可用來預覽專案，以及用來查看和編輯專案屬性。



| 控制    | 描述                                                                                                                                                                                                                                        |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 預覽    | 顯示所選取專案的預覽，例如縮圖或即時圖示。                                                                                                                                                                       |
| 屬性 | 顯示所選取專案的屬性。 針對多個選取專案，它會顯示所選取專案群組的屬性摘要。 若為 null 選取範圍，它會顯示目前頁面的屬性摘要 (listview) 的內容。 |



 

## <a name="filtering-and-view-controls"></a>篩選和查看控制項

篩選和 view 控制項可用來管理 listview 中的專案集合，以及變更 listview 中專案的呈現方式。



| 控制   | 描述                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| Filter    | 根據列為資料行的屬性，篩選或排列 listview 中的專案。 按一下資料行時，會依該屬性排序。 |
| Wordwheel | 根據輸入文字字串，以動態和累加方式篩選 listview 中顯示的專案。                      |
| 檢視      | 可讓使用者變更 listview 控制項的視圖模式。 滑杆可以用來決定圖示大小。                |



 

## <a name="listview-control"></a>Listview 控制項

Listview 控制項可用來以四種視圖模式之一來查看一組專案：詳細資料、磚、圖示或全景。 Listview 控制項也可讓使用者選取和啟用一或多個專案。

> [!Caution]  
> 雖然其中有些控制項的名稱和（或）功能類似于標準 Windows Presentation Foundation (WPF) 控制項命名空間中找到的控制項，但它們是不同的類別。

 

這些個別的控制項主要是透過使用者互動或由控制項本身所產生的事件來共同運作。 下表顯示三個主要事件類別目錄。



| 事件類別目錄 | 範例                                                       |
|----------------|---------------------------------------------------------------|
| 導覽     | 從一個頁面前往另一個。                               |
| 選取      | 變更 listview 中目前的選取範圍。               |
| 查看變更    | 變更 listview 中的呈現順序或視圖模式。 |



 

 

 
