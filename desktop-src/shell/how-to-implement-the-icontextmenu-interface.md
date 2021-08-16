---
description: ICoNtextMenu 是最強大的功能，但也是最複雜的介面來執行。
ms.assetid: F0C1D60E-7A5A-4609-9136-F4E535E9F6F1
title: 如何執行 ICoNtextMenu 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44ec65d95a4f6d67a9f15e10f5720be21c3b6c57fba5d0cf920bd12be54f662
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223465"
---
# <a name="how-to-implement-the-icontextmenu-interface"></a>如何執行 ICoNtextMenu 介面

[**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) 是最強大的功能，但也是最複雜的介面來執行。 強烈建議您使用其中一個靜態動詞方法來執行動詞。 如需詳細資訊，請參閱 [選擇靜態或動態快捷方式功能表方法](shortcut-choose-method.md)。 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) 有三種方法： [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring)、 [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)和 [**QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)，在這裡會詳細討論。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   C++

### <a name="prerequisites"></a>必要條件

-   靜態動詞
-   快速鍵功能表

## <a name="instructions"></a>指示

### <a name="icontextmenugetcommandstring-method"></a>ICoNtextMenu：： GetCommandString 方法

處理常式的 [**ICoNtextMenu：： GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) 方法是用來傳回動詞的標準名稱。 這個方法是一個選擇項目。 在 Windows XP 和舊版的 Windows 中，當 Windows 檔案總管具有狀態列時，就會使用這個方法來取得顯示在功能表項目狀態列中的解說文字。

*IdCmd* 參數會保存呼叫 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)時所定義命令的識別碼位移。 如果要求了說明字串，則 *uFlags* 會設定為 **gc \_ HELPTEXTW**。 將說明字串複製到 *pszName* 緩衝區，並將其轉換成 **PWSTR**。 將 *uFlags* 設定為 **gc \_ VERBW**，即可要求動詞字串。 將適當的字串複製到 *pszName*，就像使用說明字串一樣。 快速鍵功能表處理常式不會使用 **gc \_ VALIDATEA** 和 **gc \_ VALIDATEW** 旗標。

下列範例顯示 [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring)的簡單執行，其對應至本主題的 [ICoNtextMenu：： QueryCoNtextMenu 方法](shortcut-menu-using-dynamic-verbs.md)一節中所提供的 [**QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)範例。 因為處理常式只會新增一個功能表項目，所以只能傳回一組字串。 方法會測試 *idCmd* 是否有效，如果是，則會傳回要求的字串。

[**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya)函式可用來將要求的字串複製到 *pszName* ，以確保複製的字串不會超過 *cchName* 所指定的緩衝區大小。 這個範例只會針對 *uFlags* 的 Unicode 值執行支援，因為 Windows 2000 之後 Windows 檔案總管中只會使用這些值。


```
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
                // to discover the canonical name for the verb that is passed in
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

當使用者按一下功能表項目來指示處理常式執行相關聯的命令時，會呼叫這個方法。 *Pici* 參數指向包含執行命令所需資訊的結構。

雖然 *pici* 是在 shlobj.h 中宣告為 [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) 結構，但實際上它通常會指向 [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) 結構。 此結構是 **CMINVOKECOMMANDINFO** 的延伸版本，而且有數個額外的成員可以傳遞 Unicode 字串。

檢查 *pici* 的 **cbSize** 成員，以判斷傳入的結構。 如果它是 [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) 結構，而且 **fMask** 成員已設定 **CMIC \_ MASK \_ UNICODE** 旗標，請將 *pici* 轉換成 **CMINVOKECOMMANDINFOEX**。 這可讓您的應用程式使用結構中最後五個成員所包含的 Unicode 資訊。

結構的 **lpVerb** 或 **lpVerbW** 成員是用來識別要執行的命令。 您可以透過下列兩種方式之一來識別命令：

-   依命令的動詞字串
-   依命令的識別碼位移

若要區分這兩種情況，請檢查 **lpVerb** 的高序位單字是否有 Unicode 案例或 **lpVerbW** 。 如果高序位單字為非零值，則 **lpVerb** 或 **lpVerbW** 會保存動詞字串。 如果高序位字是零，命令位移就會是 **lpVerb** 的低序位字組。

下列範例示範 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) 的簡單執行，其對應于在此區段之前和之後提供的 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) 和 [**ICoNtextMenu：： GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) 範例。 方法會先決定要傳入的結構。 接著，它會判斷命令是否以其位移或其動詞來識別。 如果 **lpVerb** 或 **lpVerbW** 保存有效的動詞或位移，則方法會顯示訊息方塊。


```
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

專案識別碼的 *命令位移* 是 *idCmdFirst* 中識別碼和值之間的差異。 將您的處理常式所加入之每個專案的位移儲存至快捷方式功能表，因為如果其後呼叫 [**ICoNtextMenu：： GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) 或 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)，則 Shell 可能會使用位移來識別該專案。

您也應該將 [動詞](launch.md) 指派給您新增的每個命令。 動詞是在呼叫 [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) 時，可以用來代替位移來識別命令的字串。 函式（例如 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) ）也會用來執行快捷方式功能表命令。

有三個旗標可以透過與快捷方式功能表處理常式相關的 *uFlags* 參數傳入。 如下表中所述。



| 旗標             | 描述                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CMF \_ DEFAULTONLY | 使用者選取了預設的命令，通常是按兩下物件。 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) 應該將控制權交還給 Shell，而不需修改功能表。 |
| CMF \_ NODEFAULT   | 功能表中的專案都不應該是預設專案。 方法應該將其命令新增至功能表。                                                                                                                          |
| CMF \_ 正常      | 快捷方式功能表將會正常顯示。 方法應該將其命令新增至功能表。                                                                                                                            |



 

您可以使用 [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) 或 [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) ，將功能表項目新增至清單。 然後傳回嚴重性值設定為「嚴重性成功」的 **HRESULT** 值 \_ 。 將 [程式碼] 值設定為已指派最大命令識別碼的位移，再加上一個 (1) 。 例如，假設 *idCmdFirst* 設為5，而您將三個專案新增至功能表，並將命令識別碼設定為5、7和8。 傳回值應設為 \_ HRESULT (嚴重性 \_ 成功、0、8 + 1) 。

下列範例顯示插入單一命令的 [**QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) 簡單執行。 此命令的識別碼位移是 IDM \_ 顯示，其設定為零。 **M \_ pszVerb** 和 **m \_ pwszVerb** 變數是私用變數，用來以 ANSI 和 Unicode 格式儲存相關聯的語言獨立動詞字串。


```
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

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));}
```



## <a name="remarks"></a>備註

如需其他動詞的執行工作，請參閱 [建立快捷方式功能表處理常式](context-menu-handlers.md)。

 

 
