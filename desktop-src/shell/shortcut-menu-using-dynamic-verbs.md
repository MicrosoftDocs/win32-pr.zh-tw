---
description: 快速鍵功能表處理常式也稱為內容功能表處理常式或動詞處理常式。 快捷方式功能表處理常式是檔案類型處理常式的類型。
ms.assetid: 7FC65C6F-3798-404c-B359-2BC75D3F54E7
title: 使用動態動詞自訂快捷方式功能表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b24f035e84f0bde6dccde09f1ed94fefce421b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973464"
---
# <a name="customizing-a-shortcut-menu-using-dynamic-verbs"></a>使用動態動詞自訂快捷方式功能表

快速鍵功能表處理常式也稱為內容功能表處理常式或動詞處理常式。 快捷方式功能表處理常式是檔案類型處理常式的類型。

本主題的組織方式如下：

-   [關於靜態和動態動詞](#about-static-and-dynamic-verbs)
-   [快速鍵功能表處理常式如何搭配動態動詞](#how-shortcut-menu-handlers-work-with-dynamic-verbs)
-   [避免因為不合格的動詞名稱而發生衝突](#avoiding-collisions-due-to-unqualified-verb-names)
-   [使用動態動詞來註冊快捷方式功能表處理常式](#registering-a-shortcut-menu-handler-with-a-dynamic-verb)
-   [執行 ICoNtextMenu 介面](#implementing-the-icontextmenu-interface)
    -   [ICoNtextMenu：： GetCommandString 方法](#icontextmenugetcommandstring-method)
    -   [ICoNtextMenu：： InvokeCommand 方法](#icontextmenuinvokecommand-method)
    -   [ICoNtextMenu：： QueryCoNtextMenu 方法](#icontextmenuquerycontextmenu-method)
-   [相關主題](#related-topics)

## <a name="about-static-and-dynamic-verbs"></a>關於靜態和動態動詞

強烈建議您使用其中一個靜態動詞方法來執行快捷方式功能表。 建議您依照「使用靜態動詞來自訂快捷方式功能表」一節中所提供的指示，來 [建立內容功能表處理常式](context-menu-handlers.md)。 若要在 Windows 7 及更新版本中取得靜態動詞命令的動態行為，請參閱 [建立內容功能表處理常式](context-menu-handlers.md)中的「取得靜態動詞的動態行為」。 如需靜態動詞命令的執行，以及要避免哪些動態動詞的詳細資訊，請參閱 [為您的快捷方式功能表選擇靜態或動態動詞](shortcut-choose-method.md)。

如果您必須註冊檔案類型的動態動詞命令以擴充檔案類型的快捷方式功能表，請依照本主題稍後提供的指示進行。

> [!Note]  
> 註冊在32位應用程式內容中運作的處理常式時，會有64位 Windows 的特殊考慮：當 Shell 動詞命令在32位應用程式的內容中叫用時，WOW64 子系統會將檔案系統存取重新導向至某些路徑。 如果您的 .exe 處理常式儲存在其中一個路徑中，就無法在此內容中存取。 因此，若要解決這個問題，請將 .exe 儲存在未重新導向的路徑中，或儲存啟動實際版本之 .exe 的存根版本。

 

## <a name="how-shortcut-menu-handlers-work-with-dynamic-verbs"></a>快速鍵功能表處理常式如何搭配動態動詞

除了 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)之外，快速鍵功能表處理常式也會匯出下列其他介面，以處理執行主控描繪功能表項目所需的訊息：

-   [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (強制) 
-   [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (強制) 
-   [**ICoNtextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (選用) 
-   [**ICoNtextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (選用) 

如需主控描繪功能表項目的詳細資訊，請參閱 [使用功能表](../menurc/using-menus.md)中的 *建立 Owner-Drawn 功能表項目* 一節。

Shell 會使用 [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) 介面來初始化處理常式。 當 Shell 呼叫 [**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)時，它會將物件的名稱和指標傳遞至專案識別碼清單的資料物件， (PIDL 包含該檔案之資料夾的) 。 *HkeyProgID* 參數是用來註冊快捷方式功能表控制碼的登錄位置。 **IShellExtInit：： Initialize** 方法必須從資料物件中解壓縮檔案名稱，並將名稱和資料夾指標儲存至專案識別碼清單， (PIDL) 以供稍後使用。 如需處理常式初始化的詳細資訊，請參閱 [執行 IShellExtInit](handlers.md)。

在快捷方式功能表中顯示動詞命令時，會先探索到動詞，然後向使用者顯示，最後叫用。 下列清單會更詳細地說明這三個步驟：

1.  Shell 會呼叫 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)，它會傳回一組可以根據專案或系統狀態的動詞命令。
2.  系統會傳入 **HMENU** 控制碼，該控制碼可讓方法用來將專案加入至快捷方式功能表。
3.  如果使用者按一下其中一個處理常式的專案，則 Shell 會呼叫 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)。 然後，處理常式可以執行適當的命令。

## <a name="avoiding-collisions-due-to-unqualified-verb-names"></a>避免因為不合格的動詞名稱而發生衝突

由於動詞是針對每個類型註冊，因此相同的動詞名稱可用於不同專案的動詞。 這樣做可讓應用程式參考與專案類型無關的一般動詞。 雖然這項功能很有用，但使用不合格的名稱可能會導致選擇相同動詞名稱的多個獨立軟體廠商 (Isv) 發生衝突。 若要避免這種情況，請一律在動詞命令前面加上 ISV 名稱，如下所示：

`ISV_Name.verb`

一律使用應用程式特定的 ProgID。 採用將副檔名對應至 ISV 提供之 ProgID 的慣例，可避免可能發生的衝突。 不過，由於某些專案類型不會使用此對應，因此需要廠商唯一的名稱。 將動詞新增至可能已註冊該動詞的現有 ProgID 時，您必須先移除舊動詞命令的登錄機碼，再新增您自己的動詞命令。 您必須這樣做，才能避免合併來自兩個動詞的動詞資訊。 若未這麼做，會導致無法預期的行為。

## <a name="registering-a-shortcut-menu-handler-with-a-dynamic-verb"></a>使用動態動詞來註冊快捷方式功能表處理常式

快速鍵功能表處理常式會與檔案類型或資料夾相關聯。 針對檔案類型，會在下列子機碼下註冊處理常式。

```
HKEY_CLASSES_ROOT
   Program ID
      shellex
         ContextMenuHandlers
```

若要建立快捷方式功能表處理常式與檔案類型或資料夾的關聯，請先在 **CoNtextMenuHandlers** 子機碼底下建立子機碼。 命名處理常式的子機碼，並將子機碼的預設值設定為處理常式之類別識別碼的字串形式 (CLSID) GUID。

然後，若要將快捷方式功能表處理常式與不同類型的資料夾產生關聯，請使用與檔案類型相同的方式來註冊處理常式，但在 *FolderType* 子機碼底下，如下列範例所示。

```
HKEY_CLASSES_ROOT
   FolderType
      shellex
         ContextMenuHandlers
```

如需您可以註冊處理常式之資料夾類型的詳細資訊，請參閱 [註冊 Shell 擴充處理常式](handlers.md)。

如果檔案類型有相關聯的快捷方式功能表，則按兩下物件通常會啟動預設的命令，且不會呼叫處理常式的 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) 方法。 若要指定按兩下物件時應呼叫處理常式的 **ICoNtextMenu：： QueryCoNtextMenu** 方法，請在處理常式的 **CLSID** 子機碼底下建立子機碼，如下所示。

```
HKEY_CLASSES_ROOT
   CLSID
      {00000000-1111-2222-3333-444444444444}
         shellex
            MayChangeDefaultMenu
```

按兩下與處理常式相關聯的物件時，會呼叫 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) ，並在 *uFlags* 參數中設定 **CMF \_ DEFAULTONLY** 旗標。

只有當快捷方式功能表處理常式可能需要變更快捷方式功能表的預設動詞時，才應該設定 **MayChangeDefaultMenu** 子機碼。 設定這個子機碼會強制系統在相關聯的專案按兩下時載入處理常式的 DLL。 如果您的處理常式未變更預設動詞命令，您就不應該設定此子機碼，因為這樣做會導致系統不必要地載入您的 DLL。

下列範例說明啟用 myp 檔案類型之快捷方式功能表處理常式的登錄專案。 處理常式的 **CLSID** 子機碼包含 **MayChangeDefaultMenu** 子機碼，以保證當使用者按兩下相關物件時，會呼叫此處理程式。

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
         shellex
            MayChangeDefaultMenu
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         ContextMenuHandler
            MyCommand = {00000000-1111-2222-3333-444444444444}
```

## <a name="implementing-the-icontextmenu-interface"></a>執行 ICoNtextMenu 介面

[**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) 是最強大的功能，但也是最複雜的方法來執行。 強烈建議您使用其中一個靜態動詞方法來執行動詞。 如需詳細資訊，請參閱 [為您的快捷方式功能表選擇靜態或動態動詞](shortcut-choose-method.md)。 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) 有三種方法： **GetCommandString**、 **InvokeCommand** 和 **QueryCoNtextMenu**，在這裡會詳細討論。

### <a name="icontextmenugetcommandstring-method"></a>ICoNtextMenu：： GetCommandString 方法

處理常式的 [**ICoNtextMenu：： GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) 方法是用來傳回動詞的標準名稱。 這個方法是一個選擇項目。 在 Windows XP 和舊版的 Windows 中，當 Windows 檔案總管有狀態列時，就會使用這個方法來取得顯示在功能表項目狀態列中的解說文字。

*IdCmd* 參數會保存呼叫 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)時所定義命令的識別碼位移。 如果要求了說明字串，則 *uFlags* 會設定為 **gc \_ HELPTEXTW**。 將說明字串複製到 *pszName* 緩衝區，並將其轉換成 **PWSTR**。 將 *uFlags* 設定為 **gc \_ VERBW**，即可要求動詞字串。 將適當的字串複製到 *pszName*，就像使用說明字串一樣。 快速鍵功能表處理常式不會使用 **gc \_ VALIDATEA** 和 **gc \_ VALIDATEW** 旗標。

下列範例示範 [**ICoNtextMenu：： GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring)的簡單執行，其對應至本主題的 [ICoNtextMenu：： QueryCoNtextMenu 方法](#icontextmenuquerycontextmenu-method)一節中提供的 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)範例。 因為處理常式只會新增一個功能表項目，所以只能傳回一組字串。 方法會測試 *idCmd* 是否有效，如果是，則會傳回要求的字串。

[**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya)函式可用來將要求的字串複製到 *pszName* ，以確保複製的字串不會超過 *cchName* 所指定的緩衝區大小。 此範例只會支援 *uFlags* 的 Unicode 值，因為 Windows 2000 之後的 Windows 檔案總管中只會使用這些值。


```C++
IFACEMETHODIMP CMenuExtension::GetCommandString(UINT idCommand, 
                                                UINT uFlags, 
                                                UINT *pReserved, 
                                                PSTR pszName, 
                                                UINT cchName)
{
    HRESULT hr = E_INVALIDARG;

    if (idCommand == IDM_DISPLAY)
    {
        switch (uFlags)
        {
            case GCS_HELPTEXTW:
                // Only useful for pre-Vista versions of Windows that 
                // have a Status bar.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"Display File Name");
                break; 

            case GCS_VERBW:
                // GCS_VERBW is an optional feature that enables a caller
                // to discover the canonical name for the verb passed in
                // through idCommand.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"DisplayFileName");
                break; 
        }
    }
    return hr;
}
```



### <a name="icontextmenuinvokecommand-method"></a>ICoNtextMenu：： InvokeCommand 方法

當使用者按一下功能表項目來指示處理常式執行相關聯的命令時，會呼叫這個方法。 *Pici* 參數指向包含所需資訊的結構。

雖然 *pici* 是在 shlobj.h 中宣告為 [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) 結構，但實際上它通常會指向 [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) 結構。 此結構是 **CMINVOKECOMMANDINFO** 的延伸版本，而且有數個額外的成員可以傳遞 Unicode 字串。

檢查 *pici* 的 **cbSize** 成員，以判斷傳入的結構。 如果它是 [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) 結構，而且 **fMask** 成員已設定 **CMIC \_ MASK \_ UNICODE** 旗標，請將 *pici* 轉換成 **CMINVOKECOMMANDINFOEX**。 這可讓您的應用程式使用結構最後五個成員中包含的 Unicode 資訊。

結構的 **lpVerb** 或 **lpVerbW** 成員是用來識別要執行的命令。 您可以透過下列兩種方式之一來識別命令：

-   依命令的動詞字串
-   依命令的識別碼位移

若要區分這兩種情況，請檢查 **lpVerb** 的高序位單字是否有 Unicode 案例或 **lpVerbW** 。 如果高序位單字為非零值，則 **lpVerb** 或 **lpVerbW** 會保存動詞字串。 如果高序位字是零，命令位移就會是 **lpVerb** 的低序位字組。

下列範例示範 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) 的簡單執行，其對應于在此區段之前和之後提供的 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) 和 [**ICoNtextMenu：： GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) 範例。 方法會先決定要傳入的結構。 接著，它會判斷命令是否以其位移或其動詞來識別。 如果 **lpVerb** 或 **lpVerbW** 保存有效的動詞或位移，則方法會顯示訊息方塊。


```C++
STDMETHODIMP CShellExtension::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    BOOL fEx = FALSE;
    BOOL fUnicode = FALSE;

    if(lpcmi->cbSize == sizeof(CMINVOKECOMMANDINFOEX))
    {
        fEx = TRUE;
        if((lpcmi->fMask & CMIC_MASK_UNICODE))
        {
            fUnicode = TRUE;
        }
    }

    if( !fUnicode && HIWORD(lpcmi->lpVerb))
    {
        if(StrCmpIA(lpcmi->lpVerb, m_pszVerb))
        {
            return E_FAIL;
        }
    }

    else if( fUnicode && HIWORD(((CMINVOKECOMMANDINFOEX *) lpcmi)->lpVerbW))
    {
        if(StrCmpIW(((CMINVOKECOMMANDINFOEX *)lpcmi)->lpVerbW, m_pwszVerb))
        {
            return E_FAIL;
        }
    }

    else if(LOWORD(lpcmi->lpVerb) != IDM_DISPLAY)
    {
        return E_FAIL;
    }

    else
    {
        MessageBox(lpcmi->hwnd,
                   "The File Name",
                   "File Name",
                   MB_OK|MB_ICONINFORMATION);
    }

    return S_OK;
}
```



### <a name="icontextmenuquerycontextmenu-method"></a>ICoNtextMenu：： QueryCoNtextMenu 方法

Shell 會呼叫 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) ，以啟用快捷方式功能表處理常式，將其功能表項目加入功能表中。 它會傳入 *HMENU* 參數中的 **HMENU** 控制碼。 *IndexMenu* 參數會設定為要用於要加入之第一個功能表項目的索引。

處理常式所加入的任何功能表項目都必須有介於 *idCmdFirst* 和 *idCmdLast* 參數值之間的識別碼。 一般來說，第一個命令識別碼會設定為 *idCmdFirst*，每個額外的命令 (1) 遞增一次。 這種做法可協助您避免超出 *idCmdLast* ，並在 Shell 呼叫多個處理常式時，將可用識別碼的數目最大化。

專案識別碼的 *命令位移* 是 *idCmdFirst* 中識別碼和值之間的差異。 將您的處理常式所加入之每個專案的位移儲存至快捷方式功能表，因為如果其後呼叫 [**ICoNtextMenu：： GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) 或 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)，Shell 可能會使用它來識別該專案。

您也應該將 [動詞](launch.md) 指派給您新增的每個命令。 動詞是可在呼叫 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) 時，用來取代位移以識別命令的字串。 函式（例如 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) ）也會用來執行快捷方式功能表命令。

有三個旗標可以透過與快捷方式功能表處理常式相關的 *uFlags* 參數傳入。 如下表中所述。



| 旗標             | 描述                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CMF \_ DEFAULTONLY | 使用者選取了預設的命令，通常是按兩下物件。 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) 應該將控制權交還給 Shell，而不需修改功能表。 |
| CMF \_ NODEFAULT   | 功能表中的專案都不應該是預設專案。 方法應該將其命令新增至功能表。                                                                                                                          |
| CMF \_ 正常      | 快捷方式功能表將會正常顯示。 方法應該將其命令新增至功能表。                                                                                                                            |



 

您可以使用 [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) 或 [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) ，將功能表項目新增至清單。 然後傳回嚴重性值設定為「**嚴重性 \_ 成功**」的 **HRESULT** 值。 將 [程式碼] 值設定為已指派最大命令識別碼的位移，再加上一個 (1) 。 例如，假設 *idCmdFirst* 設為5，而您將三個專案新增至功能表，並將命令識別碼設定為5、7和8。 傳回值應為 `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)` 。

下列範例顯示的是 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) 的簡單實作為插入單一命令。 此命令的識別碼位移是 IDM \_ 顯示，其設定為零。 **M \_ pszVerb** 和 **m \_ pwszVerb** 變數是私用變數，用來以 ANSI 和 Unicode 格式儲存相關聯的語言獨立動詞字串。


```C++
#define IDM_DISPLAY 0

STDMETHODIMP CMenuExtension::QueryContextMenu(HMENU hMenu,
                                              UINT indexMenu,
                                              UINT idCmdFirst,
                                              UINT idCmdLast,
                                              UINT uFlags)
{
    HRESULT hr;
    
    if(!(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu(hMenu, 
                   indexMenu, 
                   MF_STRING | MF_BYPOSITION, 
                   idCmdFirst + IDM_DISPLAY, 
                   "&Display File Name");

    
        
        hr = StringCbCopyA(m_pszVerb, sizeof(m_pszVerb), "display");
        hr = StringCbCopyW(m_pwszVerb, sizeof(m_pwszVerb), L"display");

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_DISPLAY + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));
}
```



如需其他動詞的執行工作，請參閱 [建立內容功能表處理常式](context-menu-handlers.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[快捷方式 (內容) 功能表和快捷方式功能表處理常式](context-menu.md)
</dt> <dt>

[動詞和檔案關聯](fa-verbs.md)
</dt> <dt>

[為快捷方式功能表選擇靜態或動態動詞](shortcut-choose-method.md)
</dt> <dt>

[快速鍵功能表處理常式和多重選取動詞的最佳作法](verbs-best-practices.md)
</dt> <dt>

[建立快捷方式功能表處理常式](context-menu-handlers.md)
</dt> <dt>

[快速鍵功能表參考](context-menu-reference.md)
</dt> </dl>

 

 
