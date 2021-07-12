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
# <a name="managing-the-file-system"></a>管理檔案系統

Shell 提供許多方式來管理檔案系統。 Shell 提供可讓應用程式以程式設計方式移動、複製、重新命名和刪除檔案的函式 [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa)。 Shell 也支援一些額外的檔案管理功能。

-   HTML 檔案可以 *連接* 到相關的檔案，例如圖形檔案或樣式表單。 移動或複製檔時，也會自動移動或複製連接的檔案。
-   針對多個使用者可用的系統，可以每個使用者為基礎來管理檔案。 使用者可以輕鬆地存取其資料檔案，但不能存取屬於其他使用者的檔案。
-   如果新增或修改檔檔案，則可以將它們新增至命令介面的最新檔案清單。 當使用者按一下 [開始] 功能表上的 [**檔**] 命令時，會顯示檔的連結清單。

本檔討論這些檔案管理技術的運作方式。 接著，它會概述如何使用 Shell 來移動、複製、重新命名和刪除檔案，以及如何管理資源回收筒中的物件。

-   [每位使用者的檔案管理](#per-user-file-management)
-   [我的檔和我的圖片資料夾](#my-documents-and-my-pictures-folders)
-   [連接的檔案](#connected-files)
-   [移動、複製、重新命名和刪除檔案](#moving-copying-renaming-and-deleting-files)
    -   [通知 Shell](#notifying-the-shell)
-   [使用 SHFileOperation 管理檔案的簡單範例](#simple-example-of-managing-files-with-shfileoperation)
-   [將檔案新增至最新檔的 Shell 清單](#adding-files-to-the-shells-list-of-recent-documents)

## <a name="per-user-file-management"></a>Per-User 檔案管理

Windows 2000 Shell 可讓檔案與特定使用者建立關聯，讓其他使用者無法看見檔案。 就檔案系統而言，檔案會儲存在使用者的設定檔資料夾下，通常是 C： \\ Documents，而設定 \\  \\ Windows 2000 系統上的使用者名稱。 這項功能可讓許多人使用同一部電腦，同時維持其他使用者的檔案隱私權。 不同的使用者可以使用不同的程式。 此外，它也為系統管理員和應用程式提供簡單的方式，讓系統管理員和應用程式儲存 (.ini) 或連結 ( .lnk) 檔案等專案。 因此，應用程式可以為每個使用者保留不同的狀態，並在需要時輕鬆地復原該特定狀態。 另外還有一個設定檔資料夾，用來儲存所有使用者通用的資訊。

因為無法判斷登入的使用者及其檔案的位置，所以標準的每個使用者資料夾是特殊的資料夾，而且是由 [**CSIDL**](csidl.md)所識別。 比方說，每個使用者 Program Files 資料夾的 CSIDL 是 CSIDL \_ 程式。 如果您的應用程式使用其中一個每個使用者 CSIDLs 呼叫 [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) 或 [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) ，此函式會傳回專案識別碼清單的指標 (PIDL) 或適用于目前登入使用者的路徑。 如果您的應用程式需要取出設定檔資料夾的路徑或 PIDL，其 CSIDL 為 **CSIDL \_ 設定檔**。

## <a name="my-documents-and-my-pictures-folders"></a>我的檔和我的圖片資料夾

在桌面上找到的其中一個標準圖示是 **我的檔**。 當您開啟這個資料夾時，它會包含目前使用者的檔檔案。 我的檔的桌面實例是虛擬資料夾，也就是用來實際儲存使用者檔的檔案系統位置（位於命名空間階層的桌面上）的別名。

[我的檔] 和 [我的圖片] 資料夾的目的是要提供簡單且安全的方式，讓使用者在可能有多位使用者的系統上存取其檔和圖片檔案。 每位使用者都會為其檔案指派個別的檔系統資料夾。 例如，使用者在檔案系統中的 [檔] 資料夾位置通常是 C： \\ documents 和設定使用者 \\ *名稱* \\ 我的檔等內容。 使用者不需要知道其檔系統資料夾的實體位置。 他們只需透過我的檔圖示來存取檔案。

> [!Note]  
> 我的檔可讓使用者存取自己的檔案，但不能存取任何其他使用者的檔案。 如果有多個人使用同一部電腦，系統管理員可以在儲存實際檔案的檔案系統部分鎖定使用者。 如此一來，使用者就能夠透過我的檔資料夾來處理自己的檔，但不能處理屬於任何其他使用者的檔。

 

應用程式通常不需要知道哪些使用者已登入，或是使用者的我的檔資料夾所在的檔案系統中。 相反地，您的應用程式可以藉由呼叫桌面的 [**IShellFolder：:P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) 方法，來取出我的檔桌面圖示的 PIDL。 用來識別我的檔資料夾的剖析名稱不是檔案路徑，而是：： {450d8fba-ad25-11d0-98a8-0800361b1103}。 以括弧括住的運算式是我的檔 GUID 的文字形式。 例如，若要取出我的檔的 PIDL，您的應用程式應該使用此呼叫來 **IShellFolder：:P arsedisplayname**。


```C++
hr = psfDeskTop->ParseDisplayName(NULL, 
                                  NULL, 
                                  L"::{450d8fba-ad25-11d0-98a8-0800361b1103}", 
                                  &chEaten, 
                                  &pidlDocFiles, 
                                  NULL);
```



當您的應用程式有我的檔 PIDL 之後，它就可以像一般的檔系統資料夾一樣處理資料夾，例如列舉專案、剖析、系結和執行任何其他有效的資料夾作業。 Shell 會自動將我的檔或其子資料夾中的變更對應到適當的檔系統資料夾。

如果您的應用程式需要存取包含目前使用者檔的實際檔系統資料夾，請 \_ 將 CSIDL PERSONAL 傳遞給 [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation)。 函數會傳回目前使用者的我的檔資料夾中顯示之檔系統資料夾的 PIDL。

## <a name="connected-files"></a>連接的檔案

HTML 檔案通常會有許多相關聯的圖形檔案、樣式表單檔案、數個 Microsoft JScript (與 ECMA 262 語言規格 ) 檔案等相容。 當您移動或複製主要的 HTML 檔案時，通常也會想要移動或複製其相關聯的檔案，以避免中斷連結。 可惜的是，到目前為止，我們都沒有簡單的方法可以判斷哪些檔案與任何指定的 HTML 檔案相關，而不是藉由分析其內容。 為了減輕這個問題，Windows 2000 提供簡單的方式，將主要 HTML 檔案 *連接* 到其相關聯的檔案群組。 如果已啟用檔案連接，則在移動或複製檔時，會將其所有連接的檔案移至其中。

若要建立已連接的檔案群組，主要檔必須有 .htm 或 .html 副檔名。 建立主要檔的父資料夾的子資料夾。 子資料夾的名稱必須是主要檔的名稱，而不是 .htm 或 .html 副檔名，後面接著下列其中一個延伸模組。 最常使用的延伸模組為 ". files" 或 " \_ files"。 比方說，如果主要檔命名為 MyDoc.htm，則將子資料夾命名為 "MyDoc \_ files" 會將子資料夾定義為檔連接檔案的容器。 如果移動或複製主要檔，也會移動或複製子資料夾及其檔案。

針對某些語言，您可以使用「檔案」的當地語系化對等專案 \_ 來建立連接檔案的子資料夾。 下表列出可以附加至檔案名稱以建立連接檔案子資料夾的有效字串。 請注意，其中有些字串的第一個字元是 '-'，而不是 ' \_ ' 或 '. '。



:::row:::
   :::column span="":::
      " \_ archivos"
   :::column-end:::
   :::column span="":::
      " \_ arquivos"
   :::column-end:::
   :::column span="":::
      " \_ bestanden"
   :::column-end:::
   :::column span="":::
      " \_ bylos"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      "-檔案"
   :::column-end:::
   :::column span="":::
      " \_ datoteke"
   :::column-end:::
   :::column span="":::
      " \_ dosyalar"
   :::column-end:::
   :::column span="":::
      " \_ elemei"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      " \_ failid"
   :::column-end:::
   :::column span="":::
      「 \_ 失敗」
   :::column-end:::
   :::column span="":::
      " \_ fajlovi"
   :::column-end:::
   :::column span="":::
      " \_ ficheiros"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      " \_ fichiers"
   :::column-end:::
   :::column span="":::
      "-檔案管理工具"
   :::column-end:::
   :::column span="":::
      ". files"
   :::column-end:::
   :::column span="":::
      " \_ files"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      " \_ file"
   :::column-end:::
   :::column span="":::
      " \_ fitxers"
   :::column-end:::
   :::column span="":::
      " \_ fitxategiak"
   :::column-end:::
   :::column span="":::
      " \_ pliki"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      " \_ 檔案"
   :::column-end:::
   :::column span="":::
      " \_ tiedostot"
   :::column-end:::
   :::column span="":::
   :::column-end:::
   :::column span="":::
   :::column-end:::
:::row-end:::



 

> [!Note]  
> 這項功能對延伸模組的大小寫很敏感。 例如，在上述範例中，名為 "MyDoc Files" 的子資料夾 \_ 將不會連接到 MyDoc.htm。

 

啟用或停用檔案連接時，是由下列登錄機碼的 **REG \_ DWORD** 值 NoFileFolderConnection 所控制。

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
```

此值通常未定義，且已啟用檔案連接。 如有必要，您可以將此值新增至機碼，並將它設定為1，以停用檔案連接。 若要再次啟用檔案連接，請將 NoFileFolderConnection 設定為零。

> [!Note]  
> 通常應該啟用檔案連接，因為其他應用程式可能相依于該連接。 只有在絕對必要時才停用檔案連接。

 

## <a name="moving-copying-renaming-and-deleting-files"></a>移動、複製、重新命名和刪除檔案

命名空間不是靜態的，而且應用程式通常需要藉由執行下列其中一項作業來管理檔案系統。

-   將物件複製到另一個資料夾。
-   將物件移到另一個資料夾。
-   刪除物件。
-   重新命名物件。

這些作業都是使用 [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa)執行。 此函式會接受一或多個原始檔，並產生對應的目的地檔案。 在刪除操作的情況下，系統會嘗試將已刪除的檔案放入資源回收筒中。

您也可以使用 [拖放](dragdrop.md) 功能來移動檔案。

若要使用函式，您必須填入 [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) 結構的成員，並將其傳遞至 [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa)。 結構的索引鍵成員為 **pFrom** 和 **pTo**。

**PFrom** 成員是雙 **null** 終止的字串，其中包含一或多個原始程式檔名稱。 這些名稱可以是完整路徑或標準的 DOS 萬用字元，例如 \* 。 \* 雖然這個成員是宣告為以 **null** 終止的字串，但它會用來做為保存多個檔案名的緩衝區。 每個檔案名都必須以一般的單一 **Null** 字元來終止。 必須將額外的 **Null** 字元附加到最後名稱的結尾，以指出 **pFrom** 的結尾。

**PTo** 成員是雙 **null** 終止的字串，與 **pFrom** 很類似。 **PTo** 成員包含一或多個完整目的地名稱的名稱。 它們封裝成 **pTo** 的方式與 **pFrom** 相同。 如果 **pTo** 包含多個名稱，您也必須在 **fFlags** 成員中設定 **FOF \_ MULTIDESTFILES** 旗標。 **PTo** 的使用取決於此作業，如下所述。

-   若為複製和移動作業，如果所有檔案都移至單一目錄， **pTo** 就會包含完整的目錄名稱。 如果檔案要前往不同的目的地， **pTo** 也可以針對每個原始程式檔包含一個完整目錄或檔案名。 如果目錄不存在，系統會加以建立。
-   針對重新命名作業， **pTo** 會在 **pFrom** 中包含每個原始程式檔的一個完整路徑。
-   若為刪除作業，則不會使用 **pTo** 。

### <a name="notifying-the-shell"></a>通知 Shell

使用 [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) 移動、複製、重新命名或刪除檔案，或採取任何其他影響命名空間的動作之後，請通知 Shell 變更。 應伴隨通知的動作包括下列各項：

-   新增或刪除檔案或資料夾。
-   移動、複製或重新命名檔案或資料夾。
-   變更檔案關聯。
-   變更檔案屬性。
-   新增或移除磁片磁碟機或存放裝置媒體。
-   建立或停用共用資料夾。
-   變更系統映射清單。

應用程式會藉由呼叫 [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) 以及已變更內容的詳細資料，來通知 Shell。 然後，Shell 可以更新其命名空間的影像，以正確地反映其新狀態。

## <a name="simple-example-of-managing-files-with-shfileoperation"></a>使用 SHFileOperation 管理檔案的簡單範例

下列範例主控台應用程式說明如何使用 [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) 將檔案從一個目錄複寫到另一個目錄。 為了簡單起見，來源和目的地目錄（C： \\ my 檔 \_ 和 c： \\ my \_ Docs2）會硬式編碼到應用程式中。


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



應用程式會先抓取桌面 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面的指標。 然後，它會將其完整路徑傳遞至 [**IShellFolder：:P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname)，以抓取來原始目錄的 PIDL。 請注意， **IShellFolder：:P arsedisplayname** 需要目錄的路徑是 Unicode 字串。 然後，應用程式會系結至來原始目錄，並使用其 **IShellFolder** 介面來取得列舉值物件的 [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) 介面。

列舉來原始目錄中的每個檔案時，會使用 [**IShellFolder：： GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) 來取出其名稱。 \_已設定 SHGDN FORPARSING 旗標，這會導致 **IShellFolder：： GetDisplayNameOf** 傳回檔案的完整路徑。 檔案路徑（包括結束的 **Null** 字元）會串連成單一陣列 *szSourceFiles*。 第二個 **Null** 字元會附加到最後一個路徑，以正確地終止陣列。

列舉完成後，應用程式會將值指派給 [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) 結構。 請注意，指派給 **pTo** 以指定目的地的陣列也必須由 double **Null** 來終止。 在此情況下，它只會包含在指派給 **pTo** 的字串中。 因為這是主控台應用程式，所以 FOF \_ 無訊息、FOF \_ NOCONFIRMATION 和 FOF \_ NOCONFIRMMKDIR 旗標會設定為隱藏任何可能出現的對話方塊。 [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa)傳回之後，會呼叫 [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)來通知 Shell 變更。 然後，應用程式會執行一般的清除並傳回。

## <a name="adding-files-to-the-shells-list-of-recent-documents"></a>將檔案新增至最新檔的 Shell 清單

Shell 會為每個使用者維護最近新增或修改過的檔案清單。 使用者可以按一下 [開始] 功能表上的 [檔]，以顯示這些檔案的連結清單。 如同我的檔，每個使用者都有一個檔案系統目錄來保存實際的連結。 若要取得目前使用者最新目錄的 PIDL，您的應用程式可以使用最近的 CSIDL 來呼叫 [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) \_ ，或呼叫 [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) 來取出其路徑。

您的應用程式可以使用本檔稍早所討論的技術來列舉最新資料夾的內容。 但是，應用程式不應該像一般檔系統資料夾一樣修改資料夾的內容。 如果這樣做，就不會正確更新 Shell 的最新檔案清單，且變更將不會反映在 [開始] 功能表中。 相反地，若要將檔連結新增至使用者的最新資料夾，您的應用程式可以呼叫 [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)。 Shell 會將連結新增至適當的檔系統資料夾，以及更新其最近使用的檔和 [開始] 功能表的清單。 您也可以使用此函數來清除資料夾。

 

 
