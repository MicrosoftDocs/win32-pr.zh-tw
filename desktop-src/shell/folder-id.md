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
# <a name="getting-a-folders-id"></a>取得資料夾的識別碼

使用命名空間物件之前，您需要識別它的方法。 這表示取得專案識別碼清單的指標 (PIDL) 或者，如果是檔案系統物件，則為它的路徑。 本節將討論兩個較簡單的方法來取得物件識別碼。

若要使用更強大的方法來處理任何資料夾，請使用 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面。 如需詳細資訊，請參閱 [取得資料夾內容的相關資訊](folder-info.md) 。

-   [[OpenFiles] 對話方塊](#the-openfiles-dialog-box)
-   [[SHBrowseForFolder] 對話方塊](#the-shbrowseforfolder-dialog-box)
-   [特殊資料夾和 CSIDLs](#special-folders-and-csidls)
-   [如何使用 CSIDLs 和 SHBrowseForFolder 的簡單範例](#a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder)

## <a name="the-openfiles-dialog-box"></a>[OpenFiles] 對話方塊

若要讓使用者流覽命名空間並選取資料夾，您的應用程式可以使用 [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) 介面。 使用 **FOS \_ PICKFOLDERS** 旗標呼叫此介面會啟動 [挑選資料夾] 模式中的 [ [開啟](../dlgbox/open-and-save-as-dialog-boxes.md) 檔案] 通用對話方塊。

若為 Windows Vista 和更新版本，建議使用這種方式來挑選資料夾。

## <a name="the-shbrowseforfolder-dialog-box"></a>[SHBrowseForFolder] 對話方塊

若要讓使用者流覽命名空間並選取資料夾，您的應用程式可以直接叫用 [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera)。 呼叫此函式會啟動一個對話方塊，其中 UI 的運作方式與 [ [開啟] 或 [另存](../dlgbox/open-and-save-as-dialog-boxes.md) 為] 通用對話方塊有點類似。

當使用者選取資料夾時， [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) 會傳回資料夾的完整 PIDL 和其顯示名稱。 如果資料夾位於檔案系統中，則應用程式可以藉由呼叫 [**SHGetPathFromIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista)將 PIDL 轉換成路徑。 應用程式也可以藉由指定根資料夾，來限制使用者可選取的資料夾範圍。 只會顯示命名空間中該根目錄下方的資料夾。 下圖顯示 [ **SHBrowseForFolder** ] 對話方塊，並將根資料夾設定為 [Program Files]。

![[流覽資料夾] 對話方塊的螢幕擷取畫面](images/shell1.png)

稍後會提供如何使用 [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) 的簡單範例。

## <a name="special-folders-and-csidls"></a>特殊資料夾和 CSIDLs

系統會將一些常用的資料夾指定為 *特殊* 。 這些資料夾具有妥善定義的用途，且大部分都存在於所有系統上。 即使一開始並不存在，仍然會定義其名稱和位置，以便稍後加入。 特殊資料夾的集合包含所有系統的標準虛擬資料夾，例如 [印表機]、[我的檔] 和 [網路鄰近]。 它也包含一些標準的檔系統資料夾，例如 Program Files 和 System。

雖然這些資料夾是所有系統的標準元件，但在命名空間中的名稱和位置可能會有所不同。 例如，在某些系統上，系統目錄為 C： \\ Winnt \\ System32，而在其他系統上為 c： \\ Windows \\ system32。 在過去，環境變數提供了一種方法來判斷任何特定系統上特殊資料夾的名稱和位置。 Shell 現在提供更健全且更有彈性的方式來識別特殊資料夾 [**CSIDLs**](csidl.md)。 您通常應該使用它們來取代環境變數。

CSIDLs 提供統一的方式來識別和尋找特殊資料夾，無論其名稱或位置是否在特定系統上。 和環境變數不同的是，CSIDLs 可以與虛擬資料夾以及檔系統資料夾一起使用。 每個特殊資料夾都有指派的唯一 CSIDL。 例如，[Program Files file system] 資料夾具有 **CSIDL \_ Program \_ files** 的 CSIDL，而 [網路鄰近] 虛擬資料夾具有 **CSIDL \_ 網路** 的 CSIDL。

CSIDL 會與數個 Shell 函式的其中一個搭配使用，以抓取特殊資料夾的 PIDL 或特殊檔系統資料夾的路徑。 如果資料夾不存在於系統上，則您的應用程式可以藉由結合其 CSIDL 與 **CSIDL \_ 旗標 \_ 建立** 來強制建立。 CSIDL 可以傳遞給下列函式：

-   [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation)，可捕獲特殊資料夾的 PIDL。
-   [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)，它會抓取檔案系統特殊資料夾的路徑。

請注意，這兩個函式是以5.0 版的 Shell 引進，並取代 [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) 和 [**SHGetSpecialFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) 函數。

## <a name="a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder"></a>如何使用 CSIDLs 和 SHBrowseForFolder 的簡單範例

下列範例函式 PidlBrowse 會說明如何使用 CSIDLs 來取出資料夾的 PIDL，並使用 [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) 讓使用者選取資料夾。 它會傳回所選資料夾的 PIDL 和顯示名稱。


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



呼叫的應用程式會傳入視窗控制碼，此控制碼是 [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera)所需的。 *NCSIDL* 參數是用來指定根資料夾的選擇性 CSIDL。 只會顯示階層中根資料夾底下的資料夾。 稍早所示的圖例是藉由呼叫此函數，並將 *nCSIDL* 設定為 **CSIDL \_ PROGRAM \_ FILES** 來產生。 呼叫的應用程式也會傳入字串緩衝區 *>pszdisplayname*，以便在 PidlBrowse 傳回時保存所選資料夾的顯示名稱。 呼叫應用程式的責任是使用 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)來釋放 **SHBrowseForFolder** 所傳回的 idlist.txt。

 

 
