---
description: Shell 連結是資料物件，其中包含用來存取 Shell 命名空間中另一個物件&\# 郵件的資訊，也就是透過 Windows 檔案總管可見的任何物件。
ms.assetid: 32ad306d-54bd-4130-ad30-08db50ef106e
title: Shell 連結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327bcb425f998bcc2a4c0714118d4461ded253ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193354"
---
# <a name="shell-links"></a>Shell 連結

*Shell 連結* 是資料物件，其中包含用來存取 Shell 命名空間中另一個物件的資訊，也就是透過 Windows 檔案總管可見的任何物件。 可以透過 Shell 連結存取的物件類型包括檔案、資料夾、磁片磁碟機和印表機。 Shell 連結可讓使用者或應用程式從命名空間中的任何位置存取物件。 使用者或應用程式不需要知道物件目前的名稱和位置。

-   [關於 Shell 連結](#about-shell-links)
    -   [連結解析](#link-resolution)
    -   [連結檔案](#link-files)
    -   [專案識別碼和識別碼清單](#item-identifiers-and-identifier-lists)
-   [使用 Shell 連結](#using-shell-links)
    -   [建立檔案的快捷方式和資料夾快捷方式](#creating-a-shortcut-and-a-folder-shortcut-to-a-file)
    -   [解析快捷方式](#resolving-a-shortcut)
    -   [建立非物件的快捷方式](#creating-a-shortcut-to-a-nonfile-object)

## <a name="about-shell-links"></a>關於 Shell 連結

使用者可從物件的快捷方式功能表選擇 [ **建立快捷方式** ] 命令，以建立 Shell 連結。 系統會自動建立 Shell 連結的圖示，方法是將物件的圖示與一個小箭號結合 (也就是顯示在圖示左下角的系統定義連結重迭圖示) 。 具有圖示的 Shell 連結稱為快捷方式;不過，詞彙 Shell 連結和快速鍵通常會交替使用。 一般而言，使用者會建立快捷方式，以快速存取儲存在子資料夾或其他電腦之共用資料夾中的物件。 例如，使用者可以建立子資料夾中的 Microsoft Word 檔的快捷方式，並將快捷方式圖示放置在桌面上。 然後，使用者就可以按兩下快捷方式圖示來開啟檔。 如果在建立快捷方式之後移動或重新命名檔，系統將會嘗試在使用者下次選取時，更新快捷方式。

應用程式也可以建立和使用 Shell 連結和快捷方式。 例如，文字處理應用程式可能會建立 Shell 連結，以執行最近使用的檔案清單。 應用程式會使用 [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) 介面來建立 shell 連結化物件，以建立 shell 連結。 應用程式會使用 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 或 [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) 介面將物件儲存在檔案或資料流程中。

> [!Note]  
> 您無法使用 [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) 來建立 URL 的連結。

 

本總覽描述 [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) 介面，並說明如何使用它從 Microsoft Win32 應用程式內建立和解析 Shell 連結。 由於 Shell 連結的設計是以 OLE 元件物件模型 (COM) 為基礎，因此您應該先熟悉 COM 和 OLE 程式設計的基本概念，再閱讀此總覽。

### <a name="link-resolution"></a>連結解析

如果使用者建立物件的快捷方式，並在稍後變更物件的名稱或位置，系統會自動採取步驟來更新或解決在下次使用者選取時的快捷方式。 但是，如果應用程式建立 Shell 連結並將它儲存在資料流程中，系統就不會自動嘗試解析連結。 應用程式必須藉由呼叫 [**IShellLink：： resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) 方法來解析連結。

建立 Shell 連結時，系統會儲存連結的相關資訊。 解析連結時（自動或透過 [**IShellLink：： Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) 呼叫），系統會先使用 shell 連結之識別碼清單的指標，來抓取與 shell 連結相關聯的路徑。 如需識別碼清單的詳細資訊，請參閱 [專案識別碼和識別碼清單](#item-identifiers-and-identifier-lists)。 系統會在該路徑中搜尋相關聯的物件，如果找到該物件，則會解析該連結。 如果系統找不到物件，它會呼叫 [分散式連結追蹤和物件識別碼](../fileio/distributed-link-tracking-and-object-identifiers.md) (DLT) 服務（如果有的話），以找出物件。 如果 DLT 服務無法使用或找不到物件，系統會在相同的目錄中尋找具有相同檔案建立時間和屬性的物件，但名稱不同。 這種類型的搜尋會將連結解析為已重新命名的物件。

如果系統仍找不到物件，它會搜尋目錄、桌面和本機磁片區，以遞迴方式查看具有相同名稱或建立時間之物件的目錄樹狀結構。 如果系統仍找不到相符項，則會顯示一個對話方塊，提示使用者輸入位置。 應用程式可以藉由在 [**IShellLink：： Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve)的呼叫中指定 **SLR \_ NO \_ UI** 值來抑制對話方塊。

### <a name="initialization-of-the-component-object-library"></a>元件物件程式庫的初始化

應用程式必須先藉由呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 函式來初始化元件物件程式庫，應用程式才能建立及解析快捷方式。 每次呼叫 **CoInitialize** 都需要對應呼叫 [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) 函式，而應用程式會在終止時呼叫該函式。 對 **CoUninitialize** 的呼叫可確保應用程式在收到所有擱置中的訊息之前都不會終止。

### <a name="location-independent-names"></a>Location-Independent 名稱

系統會為儲存在共用資料夾中的物件，提供與位置無關的 Shell 連結名稱。 如果物件儲存在本機，系統會提供物件的本機路徑和檔案名。 如果物件儲存在遠端，則系統會為物件提供通用命名慣例 (UNC) 網路資源名稱。 由於系統會提供與位置無關的名稱，因此 Shell 連結可以作為檔案的通用名稱，以傳送至其他電腦。

### <a name="link-files"></a>連結檔案

當使用者從物件的快捷方式功能表中選擇 [ **建立快捷方式** ] 命令來建立物件的快捷方式時，Windows 會將存取該物件所需的資訊儲存在連結檔案中，此二進位檔案的副檔名為 .lnk。 連結檔案包含下列資訊：

-   快速鍵 (所參考之物件的位置 (路徑) ，稱為對應的物件) 。
-   對應物件的工作目錄。
-   當快捷方式啟用 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) 方法時，系統傳遞給對應物件的引數清單。
-   顯示命令，用來設定對應物件的初始顯示狀態。 這是 \_ [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow)中所述的其中一個軟體值。
-   快捷方式圖示的位置 (路徑和索引) 。
-   快速鍵的描述字串。
-   快速鍵的鍵盤快速鍵。

刪除連結檔案時，不會影響對應的物件。

如果您建立另一個快捷方式的快捷方式，系統只會複製連結檔案，而不是建立新的連結檔案。 在此情況下，快捷方式將不會彼此獨立。

應用程式可以註冊副檔名為快捷方式檔案類型。 如果檔案的副檔名已註冊為快捷方式檔案類型，系統會自動將系統定義的連結重迭圖示 (小箭號) 至檔案的圖示。 若要將副檔名登錄為快捷方式檔案類型，您必須將 IsShortcut 值新增至副檔名的登錄描述，如下列範例所示。 請注意，必須重新開機 Shell 圖示，重迭圖示才會生效。 IsShortcut 沒有資料值。

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = XYZApp
   XYZApp
      IsShortcut
```

### <a name="shortcut-names"></a>快速鍵名稱

快速鍵的名稱（顯示在 Shell 連結圖示下方的字串）實際上是快捷方式本身的檔案名。 使用者可以藉由選取並輸入新字串來編輯描述字串。

### <a name="location-of-shortcuts-in-the-namespace"></a>命名空間中快捷方式的位置

快速鍵可以存在於桌面或 Shell 命名空間中的任何位置。 同樣地，與快捷方式相關聯的物件也可以存在於 Shell 的命名空間中的任何位置。 應用程式可以使用 [**IShellLink：： SetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setpath) 方法來設定關聯物件的路徑和檔案名，並使用 [**IShellLink：： GetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) 方法來取得物件的目前路徑和檔案名。

### <a name="shortcut-working-directory"></a>快速鍵工作目錄

工作目錄是在使用者未識別特定目錄時，快速鍵載入或儲存檔案之對應物件的目錄。 連結檔案包含對應物件之工作目錄的名稱。 應用程式可以使用 [**IShellLink：： SetWorkingDirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setworkingdirectory) 方法，為對應的物件設定工作目錄的名稱，而且可以使用 [**IShellLink：： GetWorkingDirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getworkingdirectory) 方法來抓取對應物件目前工作目錄的名稱。

### <a name="shortcut-command-line-arguments"></a>快速鍵命令列引數

連結檔案包含命令列引數，這些引數會在使用者選取連結時，讓 Shell 傳遞給對應的物件。 應用程式可以使用 [**IShellLink：： SetArguments**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setarguments) 方法來設定快速鍵的命令列引數。 當對應的應用程式（例如，連結器或編譯器）採用特殊旗標做為引數時，設定命令列引數會很有用。 應用程式可以使用 [**IShellLink：： GetArguments**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ishelllinka-getarguments) 方法，從快捷方式取得命令列引數。

### <a name="shortcut-show-commands"></a>快速鍵顯示命令

當使用者按兩下快捷方式時，系統會啟動與對應物件相關聯的應用程式，並根據快捷方式指定的 [顯示] 命令設定應用程式的初始顯示狀態。 Show 命令可以是 \_ [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) 函式描述中包含的任何 SW 值。 應用程式可以使用 [**IShellLink：： SetShowCmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setshowcmd) 方法來設定快速鍵的 show 命令，而且可以使用 [**IShellLink：： GetShowCmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getshowcmd) 方法來取出目前的 show 命令。

### <a name="shortcut-icons"></a>快速鍵圖示

就像其他 Shell 物件一樣，快捷方式也有一個圖示。 使用者只要按兩下快捷方式的圖示，即可存取與快捷方式相關聯的物件。 當系統建立快捷方式的圖示時，會使用對應物件的點陣圖，並將系統定義的連結重迭圖示 (小箭號) 至左下角。 應用程式可以使用 [**IShellLink：： SetIconLocation**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-seticonlocation) 方法，設定快速鍵的圖示 (路徑和索引) 。 應用程式可以使用 [**IShellLink：： GetIconLocation**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-geticonlocation) 方法來取得這個位置。

### <a name="shortcut-descriptions"></a>快速鍵描述

快速鍵具有描述，但使用者從未看到它們。 應用程式可以使用描述來儲存任何文字資訊。 描述是使用 [**IShellLink：： SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) 方法設定，並使用 [**IShellLink：： GetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) 方法來抓取。

### <a name="shortcut-keyboard-shortcuts"></a>快速鍵鍵盤快速鍵

快捷方式物件可以有相關聯的鍵盤快速鍵。 鍵盤快速鍵可讓使用者按下按鍵的組合，以啟用快捷方式。 應用程式可以使用 [**IShellLink：： SetHotkey**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-sethotkey) 方法來設定快速鍵的鍵盤快速鍵，而且可以使用 [**IShellLink：： GetHotkey**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-gethotkey) 方法來取得目前的鍵盤快速鍵。

### <a name="item-identifiers-and-identifier-lists"></a>專案識別碼和識別碼清單

Shell 會使用 Shell 命名空間內的物件識別碼。 Shell 中顯示的所有物件 (檔案、目錄、伺服器、工作組等) 在其父資料夾內的物件之間有唯一的識別碼。 這些識別碼稱為專案識別碼，它們具有 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 資料類型，如 shtypes.idl .h 標頭檔中所定義。 專案識別碼是可變長度的位元組資料流程，包含可識別資料夾內物件的資訊。 只有專案識別碼的建立者知道識別碼的內容和格式。 Shell 使用的專案識別碼的唯一部分是前兩個位元組，這兩個位元組會指定識別碼的大小。

每個父資料夾都有自己的專案識別碼，可在它自己的上層資料夾中識別它。 因此，任何 Shell 物件都可以透過專案識別碼清單來唯一識別。 父資料夾會保留它所包含之專案的識別碼清單。 此清單具有 [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) 資料類型。 專案識別碼清單是由 Shell 配置，並且可以跨 Shell 介面（例如 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)）傳遞。 請務必記住，專案識別碼清單中的每個識別碼，只有在其父資料夾的內容中才有意義。

應用程式可以使用 [**IShellLink：： SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) 方法來設定快捷方式的專案識別碼清單。 將快捷方式設定為非檔案的物件（例如印表機或磁片磁碟機）時，此方法很有用。 應用程式可以使用 [**IShellLink：： GetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getidlist) 方法來取得快捷方式的專案識別碼清單。

## <a name="using-shell-links"></a>使用 Shell 連結

本章節包含的範例將示範如何從 Win32 應用程式內建立和解析快捷方式。 本節假設您已熟悉 Win32、c + + 和 OLE COM 程式設計。

### <a name="creating-a-shortcut-and-a-folder-shortcut-to-a-file"></a>建立檔案的快捷方式和資料夾快捷方式

下列範例中的 CreateLink 範例函數會建立快捷方式。 這些參數包括要連結之檔案的名稱指標、您正在建立的快捷方式名稱指標，以及連結描述的指標。 描述包含字串：「 **檔案名** 的快捷方式」，其中 **檔案名** 是要連結的目的檔案名。

若要使用 CreateLink 範例函式建立資料夾快捷方式， [](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)請使用 clsid \_ FolderShortcut （而不是 CLSID \_ ShellLink (clsid \_ FolderShortcut 支援 IShellLink) 來呼叫 CoCreateInstance。 所有其他程式碼都會保持不變。

因為 CreateLink 會呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函式，所以會假設已經呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 函數。 CreateLink 會使用 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 介面來儲存快捷方式和 [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) 介面，以儲存檔案名和描述。


```C++
// CreateLink - Uses the Shell's IShellLink and IPersistFile interfaces 
//              to create and store a shortcut to the specified object. 
//
// Returns the result of calling the member functions of the interfaces. 
//
// Parameters:
// lpszPathObj  - Address of a buffer that contains the path of the object,
//                including the file name.
// lpszPathLink - Address of a buffer that contains the path where the 
//                Shell link is to be stored, including the file name.
// lpszDesc     - Address of a buffer that contains a description of the 
//                Shell link, stored in the Comment field of the link
//                properties.

#include "stdafx.h"
#include "windows.h"
#include "winnls.h"
#include "shobjidl.h"
#include "objbase.h"
#include "objidl.h"
#include "shlguid.h"

HRESULT CreateLink(LPCWSTR lpszPathObj, LPCSTR lpszPathLink, LPCWSTR lpszDesc) 
{ 
    HRESULT hres; 
    IShellLink* psl; 
 
    // Get a pointer to the IShellLink interface. It is assumed that CoInitialize
    // has already been called.
    hres = CoCreateInstance(CLSID_ShellLink, NULL, CLSCTX_INPROC_SERVER, IID_IShellLink, (LPVOID*)&psl); 
    if (SUCCEEDED(hres)) 
    { 
        IPersistFile* ppf; 
 
        // Set the path to the shortcut target and add the description. 
        psl->SetPath(lpszPathObj); 
        psl->SetDescription(lpszDesc); 
 
        // Query IShellLink for the IPersistFile interface, used for saving the 
        // shortcut in persistent storage. 
        hres = psl->QueryInterface(IID_IPersistFile, (LPVOID*)&ppf); 
 
        if (SUCCEEDED(hres)) 
        { 
            WCHAR wsz[MAX_PATH]; 
 
            // Ensure that the string is Unicode. 
            MultiByteToWideChar(CP_ACP, 0, lpszPathLink, -1, wsz, MAX_PATH); 
            
            // Add code here to check return value from MultiByteWideChar 
            // for success.
 
            // Save the link by calling IPersistFile::Save. 
            hres = ppf->Save(wsz, TRUE); 
            ppf->Release(); 
        } 
        psl->Release(); 
    } 
    return hres; 
```



### <a name="resolving-a-shortcut"></a>解析快捷方式

應用程式可能需要存取和操作先前建立的快捷方式。 這項操作稱為解析快捷方式。

下列範例中的應用程式定義 ResolveIt 函數會解析快捷方式。 其參數包括視窗控制碼、快捷方式路徑的指標，以及接收物件之新路徑的緩衝區位址。 視窗控點會識別命令介面可能需要顯示之任何訊息方塊的父視窗。 例如，如果連結位於非共用媒體上，Shell 可以顯示訊息方塊，如果發生網路問題，使用者是否需要插入磁片，依此類推。

ResolveIt 函式會呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數，並假設已呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 函式。 請注意，ResolveIt 需要使用 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 介面來儲存連結資訊。 **IPersistFile** 是由 [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) 物件所執行。 在抓取路徑資訊之前，必須先載入連結資訊，此範例稍後會顯示此資訊。 無法載入連結資訊會導致呼叫 [**IShellLink：： GetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) 和 [**IShellLink：： GetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) 成員函式失敗。


```C++
// ResolveIt - Uses the Shell's IShellLink and IPersistFile interfaces 
//             to retrieve the path and description from an existing shortcut. 
//
// Returns the result of calling the member functions of the interfaces. 
//
// Parameters:
// hwnd         - A handle to the parent window. The Shell uses this window to 
//                display a dialog box if it needs to prompt the user for more 
//                information while resolving the link.
// lpszLinkFile - Address of a buffer that contains the path of the link,
//                including the file name.
// lpszPath     - Address of a buffer that receives the path of the link
                  target, including the file name.
// lpszDesc     - Address of a buffer that receives the description of the 
//                Shell link, stored in the Comment field of the link
//                properties.

#include "stdafx.h"
#include "windows.h"
#include "shobjidl.h"
#include "shlguid.h"
#include "strsafe.h"
                            
HRESULT ResolveIt(HWND hwnd, LPCSTR lpszLinkFile, LPWSTR lpszPath, int iPathBufferSize) 
{ 
    HRESULT hres; 
    IShellLink* psl; 
    WCHAR szGotPath[MAX_PATH]; 
    WCHAR szDescription[MAX_PATH]; 
    WIN32_FIND_DATA wfd; 
 
    *lpszPath = 0; // Assume failure 

    // Get a pointer to the IShellLink interface. It is assumed that CoInitialize
    // has already been called. 
    hres = CoCreateInstance(CLSID_ShellLink, NULL, CLSCTX_INPROC_SERVER, IID_IShellLink, (LPVOID*)&psl); 
    if (SUCCEEDED(hres)) 
    { 
        IPersistFile* ppf; 
 
        // Get a pointer to the IPersistFile interface. 
        hres = psl->QueryInterface(IID_IPersistFile, (void**)&ppf); 
        
        if (SUCCEEDED(hres)) 
        { 
            WCHAR wsz[MAX_PATH]; 
 
            // Ensure that the string is Unicode. 
            MultiByteToWideChar(CP_ACP, 0, lpszLinkFile, -1, wsz, MAX_PATH); 
 
            // Add code here to check return value from MultiByteWideChar 
            // for success.
 
            // Load the shortcut. 
            hres = ppf->Load(wsz, STGM_READ); 
            
            if (SUCCEEDED(hres)) 
            { 
                // Resolve the link. 
                hres = psl->Resolve(hwnd, 0); 

                if (SUCCEEDED(hres)) 
                { 
                    // Get the path to the link target. 
                    hres = psl->GetPath(szGotPath, MAX_PATH, (WIN32_FIND_DATA*)&wfd, SLGP_SHORTPATH); 

                    if (SUCCEEDED(hres)) 
                    { 
                        // Get the description of the target. 
                        hres = psl->GetDescription(szDescription, MAX_PATH); 

                        if (SUCCEEDED(hres)) 
                        {
                            hres = StringCbCopy(lpszPath, iPathBufferSize, szGotPath);
                            if (SUCCEEDED(hres))
                            {
                                // Handle success
                            }
                            else
                            {
                                // Handle the error
                            }
                        }
                    }
                } 
            } 

            // Release the pointer to the IPersistFile interface. 
            ppf->Release(); 
        } 

        // Release the pointer to the IShellLink interface. 
        psl->Release(); 
    } 
    return hres; 
}
```



### <a name="creating-a-shortcut-to-a-nonfile-object"></a>建立非物件的快捷方式

建立非檔案系統的快捷方式（例如印表機）類似于建立檔案的快捷方式，但您必須將識別碼清單設定為印表機，而不是設定檔案的路徑。 若要設定識別碼清單，請呼叫 [**IShellLink：： SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) 方法，並指定識別碼清單的位址。

Shell 命名空間中的每個物件都有一個專案識別碼。 Shell 通常會將專案識別碼串連成以 null 終止的清單，其中包含任意數目的專案識別碼。 如需專案識別碼的詳細資訊，請參閱 [專案識別碼和識別碼清單](#item-identifiers-and-identifier-lists)。

一般情況下，如果您需要設定沒有檔案名的專案快捷方式（例如印表機），則您已經有物件的 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面指標。 **IShellFolder** 可用來建立命名空間延伸模組。

當您擁有 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)的類別識別碼之後，就可以呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數來取出介面的位址。 然後您可以呼叫介面，以列舉資料夾中的物件，並抓取您要搜尋之物件的專案識別碼位址。 最後，您可以在 [**IShellLink：： SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) 成員函式的呼叫中使用該位址，以建立物件的快捷方式。

 

 
