---
description: 一旦您的應用程式找到檔案物件之後，下一個步驟通常會以某種方式採取行動。
ms.assetid: d774c3b2-4caf-460a-ac32-0ed603491d5f
title: '啟動應用程式 (ShellExecute、ShellExecuteEx、SHELLEXECUTEINFO) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ae5640acdbf4d959b97607cc66a4fd8fe8ac24
ms.sourcegitcommit: 89aa14b1f685f8d65d56ecbdb8bef12246c33cf9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/08/2021
ms.locfileid: "113508609"
---
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a>啟動應用程式 (ShellExecute、ShellExecuteEx、SHELLEXECUTEINFO) 

一旦您的應用程式找到檔案物件之後，下一個步驟通常會以某種方式採取行動。 比方說，您的應用程式可能想要啟動另一個應用程式，讓使用者修改資料檔案。 如果您感興趣的檔案是可執行檔，您的應用程式可能只想要啟動它。 本檔將討論如何使用 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 或 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 來執行這些工作。

-   [使用 ShellExecute 和 ShellExecuteEx](#using-shellexecute-and-shellexecuteex)
    -   [物件動詞](#object-verbs)
    -   [使用 ShellExecuteEx 從網站提供啟用服務](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   [使用 ShellExecute 啟動 [搜尋] 對話方塊](#using-shellexecute-to-launch-the-search-dialog-box)
-   [如何使用 ShellExecuteEx 的簡單範例](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a>使用 ShellExecute 和 ShellExecuteEx

若要使用 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 或 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)，您的應用程式必須指定要處理的檔案或資料夾物件，以及指定作業的 *動詞* 。 若為 **ShellExecute**，請將這些值指派給適當的參數。 針對 **ShellExecuteEx**，請填入 [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) 結構的適當成員。 另外還有其他幾個成員或參數可用來微調兩個函式的行為。

檔案和資料夾物件可以是檔案系統或虛擬物件的一部分，而且可以透過路徑或專案識別碼清單的指標來識別 (Pidl) 。

### <a name="object-verbs"></a>物件動詞

物件的可用動詞本質上是您在物件的快捷方式功能表上找到的專案。 若要尋找可用的動詞，請在登錄下查看

**HKEY \_類別 \_ 根目錄** \\ **CLSID** \\ *{object \_ clsid}* \\ **Shell** \\ *動詞*

其中 *物件 \_ clsid* 是物件 (clsid) 的類別識別碼，而 *verb* 則是可用動詞命令的名稱。 *動詞* \\ **命令** 子機碼包含的資料，指出叫用該動詞時所發生的情況。

若要找出可用於 [預先定義之 Shell 物件](handlers.md)的動詞，請查看位於

**HKEY \_類別 \_ 根** \\ *物件 \_ 名稱* \\ **shell** \\ *動詞* 命令

其中 *物件 \_ 名稱* 是預先定義之 Shell 物件的名稱。 同樣地，*動詞* \\ **命令** 子機碼包含的資料會指出叫用該動詞時所發生的情況。

常見的可用動詞包括：



| 動詞命令       | 描述                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| 編輯       | 啟動編輯器並開啟要編輯的檔。                                                   |
| 尋找       | 從指定的目錄起始搜尋。                                                |
| 開啟       | 啟動應用程式。 如果此檔案不是可執行檔，則會啟動其相關聯的應用程式。 |
| print      | 列印檔案檔。                                                                                |
| properties | 顯示物件的屬性。                                                                        |
| runas      | 以系統管理員身分啟動應用程式。 使用者帳戶控制 (UAC) 會提示使用者同意執行提高許可權的應用程式，或輸入用來執行應用程式之系統管理員帳戶的認證。 |



每個動詞命令都對應至用來從主控台視窗啟動應用程式的命令。 **Open** 動詞是很好的範例，因為它通常是受支援的。 針對 .exe 檔案， **開啟** 只會啟動應用程式。 不過，這通常是用來啟動在特定檔案上運作的應用程式。 比方說，Microsoft WordPad 可以開啟 .txt 的檔案。 因此，.txt 檔案的 **open** 動詞會對應至類似下列的命令：


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



當您使用 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 或 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 來開啟 .txt 檔案時，Wordpad.exe 會以指定的檔案作為其引數來啟動。 某些命令可以有額外的引數（例如旗標），可視需要新增以正確啟動應用程式。 如需快捷方式功能表和動詞的進一步討論，請參閱 [擴充快捷方式功能表](context.md)。

一般情況下，嘗試判斷特定檔案的可用動詞清單會有點複雜。 在許多情況下，您只要將 *lpVerb* 參數設定為 **Null**，就會叫用檔案類型的預設命令。 此程式通常相當於將 *lpVerb* 設定為「開啟」，但某些檔案類型可能會有不同的預設命令。 如需詳細資訊，請參閱 [擴充快捷方式功能表](context.md) 和 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 參考檔。

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a>使用 ShellExecuteEx 從網站提供啟用服務

網站鏈的服務可以控制專案啟用的許多行為。 Windows 8，您可以提供指向 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)的網站鏈指標，以啟用這些行為。 若要提供網站給 **ShellExecuteEx**：

-   \_ \_ \_ \_ \_ 在 [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa)的 **fMask** 成員中，指定 HINST 為 SITE 旗標的 [請參閱遮罩旗標]。
-   在 [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa)的 **hInstApp** 成員中提供 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 。

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a>使用 ShellExecute 啟動 [搜尋] 對話方塊

當使用者以滑鼠右鍵按一下 Windows 檔案總管中的資料夾圖示時，其中一個功能表項目是 [搜尋]。 如果他們選取該專案，則 Shell 會啟動其搜尋公用程式。 此公用程式會顯示一個對話方塊，可用來搜尋指定文字字串的檔案。 應用程式可以透過呼叫 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)，以程式設計方式啟動目錄的搜尋公用程式，並以 "find" 作為 *lpVerb* 參數，並以目錄路徑作為 *lpFile* 參數。 比方說，下面這行程式碼會啟動 c： MyPrograms 目錄的搜尋公用程式 \\ 。


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a>如何使用 ShellExecuteEx 的簡單範例

下列範例主控台應用程式示範如何使用 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)。 為了清楚起見，已省略大部分的錯誤檢查程式碼。


```C++
#include <shlobj.h>
#include <shlwapi.h>
#include <objbase.h>

main()
{
    LPITEMIDLIST pidlWinFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IShellFolder *psfWinFiles = NULL;
    IShellFolder *psfDeskTop = NULL;
    LPENUMIDLIST ppenum = NULL;
    STRRET strDispName;
    TCHAR pszParseName[MAX_PATH];
    ULONG celtFetched;
    SHELLEXECUTEINFO ShExecInfo;
    HRESULT hr;
    BOOL fBitmap = FALSE;

    hr = SHGetFolderLocation(NULL, CSIDL_WINDOWS, NULL, NULL, &pidlWinFiles);

    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->BindToObject(pidlWinFiles, NULL, IID_IShellFolder, (LPVOID *) &psfWinFiles);
    hr = psfDeskTop->Release();

    hr = psfWinFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

    while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
    {
        psfWinFiles->GetDisplayNameOf(pidlItems, SHGDN_FORPARSING, &strDispName);
        StrRetToBuf(&strDispName, pidlItems, pszParseName, MAX_PATH);
        CoTaskMemFree(pidlItems);
        if(StrCmpI(PathFindExtension(pszParseName), TEXT( ".bmp")) == 0)
        {
            fBitmap = TRUE;
            break;
        }
    }

    ppenum->Release();

    if(fBitmap)
    {
        ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
        ShExecInfo.fMask = NULL;
        ShExecInfo.hwnd = NULL;
        ShExecInfo.lpVerb = NULL;
        ShExecInfo.lpFile = pszParseName;
        ShExecInfo.lpParameters = NULL;
        ShExecInfo.lpDirectory = NULL;
        ShExecInfo.nShow = SW_MAXIMIZE;
        ShExecInfo.hInstApp = NULL;

        ShellExecuteEx(&ShExecInfo);
    }

    CoTaskMemFree(pidlWinFiles);
    psfWinFiles->Release();

    return 0;
}
```



應用程式會先抓取 Windows 目錄的 PIDL，並列舉其內容，直到找到第一個 .bmp 檔案為止。 不同于先前的範例， [**IShellFolder：： GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) 是用來抓取檔案的剖析名稱，而不是其顯示名稱。 因為這是檔系統資料夾，所以剖析名稱是完整路徑，這是 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)所需的路徑。

一旦找到第一個 .bmp 檔案，就會將適當的值指派給 [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) 結構的成員。 **LpFile** 成員會設定為檔案的剖析名稱，而 **lpVerb** 成員會設定為 **Null**，以開始預設作業。 在此情況下，預設作業為 "open"。 然後，會將結構傳遞至 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)，以啟動點陣圖檔案的預設處理常式（通常 MSPaint.exe）來開啟檔案。 函數傳回之後，pidl 就會釋出，並釋放 Windows 資料夾的 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)介面。

 

 
