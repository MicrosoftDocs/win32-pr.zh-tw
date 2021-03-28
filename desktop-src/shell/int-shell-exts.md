---
description: Shell 擴充處理常式物件的大部分執行都是由其型別所決定。 不過，有一些常見的元素。 本主題討論所有 Shell 延伸模組處理常式所共用的執行層面。
ms.assetid: ce21ca0f-157c-4f69-bcf9-dc259c3bac80
title: 初始化 Shell 擴充處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6a27b6273c5e342dc4caf545fb3593cdad66261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973761"
---
# <a name="initializing-shell-extension-handlers"></a>初始化 Shell 擴充處理常式

Shell 擴充處理常式物件的大部分執行都是由其型別所決定。 不過，有一些常見的元素。 本主題討論所有 Shell 延伸模組處理常式所共用的執行層面。

所有 Shell 擴充處理常式都是 (COM) 物件的同進程元件物件模型。 您必須將 GUID 指派給它們，如 [註冊 Shell 擴充處理常式](handlers.md)中所述。 它們會實作為 Dll，而且必須匯出下列標準函式：

-   [**DllMain**](../dlls/dllmain.md)。 DLL 的標準進入點。
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)。 公開物件的 class factory。
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)。 COM 會呼叫這個函式，以判斷物件是否為任何用戶端提供服務。 如果不是，則系統可以卸載 DLL 並釋放相關聯的記憶體。

Shell 擴充處理常式和所有 COM 物件一樣，都必須執行 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面和 [class factory](../com/implementing-iclassfactory.md)。 大部分也必須在 Windows XP 或更早版本中執行 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 或 [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) 介面。 這些已由 Windows Vista 中的 [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)、 [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) 和 [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) 取代。 Shell 會使用這些介面來初始化處理常式。

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)介面必須由下列各項執行：

-   圖示處理常式
-   資料處理程式
-   捨棄處理常式

[**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)介面必須由下列各項執行：

-   快速鍵功能表處理常式
-   拖放處理常式
-   屬性工作表處理常式

本主題的其餘部分將討論下列主題：

-   [執行 IPersistFile](#implementing-ipersistfile)
-   [執行 IShellExtInit](#implementing-ishellextinit)
-   [提示自訂](#infotip-customization)
-   [相關主題](#related-topics)

## <a name="implementing-ipersistfile"></a>執行 IPersistFile

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)介面是設計來允許將物件載入或儲存到磁片檔案。 除了 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)、其本身的五個方法，以及它繼承自 [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist)的 [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid)方法之外，它還有六個方法。 使用 Shell 擴充功能時， **IPersist** 只會用來初始化 Shell 擴充處理常式物件。 因為通常不需要讀取或寫入磁片，所以只有 **GetClassID** 和 [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) 方法需要 nontoken 執行。

Shell 會先呼叫 [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) ，函式會傳回擴充處理常式物件 (CLSID) 的類別識別碼。 然後，Shell 會呼叫 [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) 並以兩個值傳遞。 第一個 *pszFile* 是 Unicode 字串，其中包含 Shell 即將操作的檔案或資料夾的名稱。 第二個是 *dwMode*，表示檔案存取模式。 因為通常不需要存取檔案， *dwMode* 通常是零。 方法會視需要儲存這些值以供稍後參考。

下列程式碼片段說明一般 Shell 擴充處理常式如何執行 [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) 和 [**載入**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) 方法。 它是設計來處理 ANSI 或 Unicode。 CLSID \_ SampleExtHandler 是延伸模組處理常式物件的 GUID，而 CSampleShellExtension 是用來執行介面的類別名稱。 **M \_ szFileName** 和 **m \_ dwMode** 變數是私用變數，用來儲存檔案的名稱和存取旗標。


```C++
class CSampleShellExtension : public IPersistFile
{
    // Method declarations not included

    private:
    WCHAR m_szFileName[MAX_PATH];    // The file name
    DWORD m_dwMode;                  // The file access mode
}

IFACEMETHODIMP CSampleShellExtension::GetClassID(__out CLSID *pCLSID)
{
    *pCLSID = CLSID_SampleExtHandler;
}

IFACEMETHODIMP CSampleShellExtension::Load(PCWSTR pszFile, DWORD dwMode)
{
    m_dwMode = dwMode;
    return StringCchCopy(m_szFileName, ARRAYSIZE(m_szFileName), pszFile); 
}

// The implementation sample is continued in the next section.
```



## <a name="implementing-ishellextinit"></a>執行 IShellExtInit

[**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)介面除了 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)之外，只有一個方法 [**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)。 方法有三個參數，可供 Shell 用來傳入各種類型的資訊。 傳入的值取決於處理常式的類型，而部分可以設定為 **Null**。

-   *pidlFolder* 會保留資料夾的 (PIDL) 專案識別碼清單的指標。 這是絕對 PIDL。 若為屬性工作表延伸，此值為 **Null**。 如果是快捷方式功能表延伸，則是包含要顯示其快捷方式功能表之專案的資料夾 PIDL。 若是非預設的拖放處理常式，則為目的檔案夾的 PIDL。
-   *pDataObject* 會保留資料物件的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面指標。 資料物件會以 [CF \_ HDROP](dragdrop.md) 格式保存一或多個檔案名。
-   *hRegKey* 會保留檔案物件或資料夾類型的登錄機碼。

[**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)方法會視需要儲存檔案名、 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)指標和登錄機碼，以供稍後使用。 下列程式碼片段說明 **IShellExtInit：： Initialize** 的實作為。 為了簡單起見，此範例假設資料物件只包含單一檔案。 一般而言，資料物件可能包含多個檔案，每個檔案都需要解壓縮。


```C++
// This code continues the CSampleShellExtension sample shown in the
// "Implementing IPersistFile" section above.

class CSampleShellExtension : public IShellExtInit
{
    // Method declarations not included
    
    private:
    // IDList of the folder for extensions invoked on the folder, such as 
    // background context menu handlers or nondefault drag-and-drop handlers. 
    PIDLIST_ABSOLUTE m_pidlFolder;
    
    // The data object contains an expression of the items that the handler is 
    // being initialized for. Use SHCreateShellItemArrayFromDataObject to 
    // convert this object to an array of items. Use SHGetItemFromObject if you
    // are only interested in a single Shell item. If you need a file system
    // path, use IShellItem::GetDisplayName(SIGDN_FILESYSPATH, ...).
    IDataObject *m_pdtobj;
    
    // For context menu handlers, the registry key provides access to verb 
    // instance data that might be stored there. This is a rare feature to use 
    // so most extensions do not need this variable.
    HKEY m_hRegKey;             
}
    
// This method must be very efficient. Do not do any unnecessary work here.
// Use Initialize to acquire resources that will be used later.

IFACEMETHODIMP CSampleShellExtension::Initialize(__in_opt PCIDLIST_ABSOLUTE pidlFolder,
                                                 __in_opt IDataObject *pDataObject, 
                                                 __in_opt HKEY hRegKey) 
{ 
    // In some cases, handlers are initialized multiple times. Therefore, 
    // clear any previous state here.
    CoTaskMemFree(m_pidlFolder);
    m_pidlFolder = NULL;
    
    if (m_pdtobj)
    { 
        m_pdtobj->Release(); 
    }
    
    if (m_hRegKey)
    {
        RegCloseKey(m_hRegKey);
        m_hRegKey = NULL;
    }
    
    // Capture the inputs for use later.
    HRESULT hr = S_OK;
    
    if (pidlFolder)
    {
        m_pidlFolder = ILClone(pidlFolder);   // Make a copy to use later.
        hr = m_pidlFolder ? S_OK : E_OUTOFMEMORY;
    }
    
    if (SUCCEEDED(hr))
    {
        // If a data object pointer was passed into the method, save it and
        // extract the file name. 
        if (pDataObject) 
        { 
            m_pdtobj = pDataObject; 
            m_pdtobj->AddRef(); 
        }
    
        // It is uncommon to use the registry handle, but if you need it,
        // duplicate it now.
        if (hRegKey)
        {
            LSTATUS const result = RegOpenKeyEx(hRegKey, NULL, 0, KEY_READ, &m_hRegKey); 
            hr = HRESULT_FROM_WIN32(result);
        }
    }
    
    return hr;
}
```



## <a name="infotip-customization"></a>提示自訂

有兩種方式可以自訂提示。 其中一種方式是執行支援 [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) 的物件，然後在登錄中的適當子機碼下註冊物件 (請參閱下面的) 。 或者，您可以指定要顯示的固定字串或特定檔案屬性的清單。

若要顯示命名空間延伸的固定字串，請在命名空間延伸模組的 CLSID 機 **碼底下建立** 名為 [提示] 的子機碼。 將該子機碼的資料設定為您想要顯示的字串。

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

若要顯示檔案類型的固定字串，請在您要提供提示的檔案類型的 **ProgID** 索引 **鍵下方，** 建立名為 [提示] 的子機碼。 將該子機碼的資料設定為您想要顯示的字串。

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = InfoTip string for all files of this type
```

如果您想要讓 Shell 在特定檔案類型的提示中顯示特定的檔案屬性，請在該檔案類型的 **ProgID** **金鑰下方建立** 名為 [提示] 的子機碼。 將該子機碼的資料設定為以分號分隔的標準屬性名稱清單或 {fmtid}、pid 組，其中 *propname* 是標準的屬性名稱，而 *{fmtid}，pid* 是 [**fmtid/pid**](./objects.md)組。

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = propname;propname;{fmtid},pid;{fmtid},pid
```

您可以使用下列屬性名稱。



| 屬性名稱    | 描述                   | 取出來源                                                                            |
|------------------|-------------------------------|-------------------------------------------------------------------------------------------|
| 作者           | 檔作者        | [**PIDSI \_ 作者**](../stg/the-summary-information-property-set.md)                             |
| 標題            | 檔的標題         | [**PIDSI \_ 標題**](../stg/the-summary-information-property-set.md)                              |
| 主體          | 主題摘要               | [**PIDSI \_ 主旨**](../stg/the-summary-information-property-set.md)                            |
| 註解          | 檔批註             | [**PIDSI \_批註**](../stg/the-summary-information-property-set.md) 或資料夾/磁片磁碟機屬性 |
| PageCount        | 頁面數目               | [**PIDSI \_ PAGECOUNT**](../stg/the-summary-information-property-set.md)                          |
| Name             | 易記名稱                 | 標準資料夾檢視                                                                      |
| OriginalLocation | 原始檔案的位置     | [公事包] 資料夾和資源回收筒資料夾                                                   |
| DateDeleted      | 資料檔案已刪除         | 資源回收筒資料夾                                                                        |
| 類型             | 檔案類型                  | 標準資料夾詳細資料檢視                                                              |
| 大小             | 檔案大小                  | 標準資料夾詳細資料檢視                                                              |
| SyncCopyIn       | 與 OriginalLocation 相同      | 與 OriginalLocation 相同                                                                  |
| 修改日期         | 上次修改日期            | 標準資料夾詳細資料檢視                                                              |
| 建立時間          | 建立日期                  | 標準資料夾詳細資料檢視                                                              |
| 訪問         | 上次存取日期            | 標準資料夾詳細資料檢視                                                              |
| InFolder         | 包含檔案的目錄 | 檔搜尋結果                                                                   |
| 排名             | 搜尋符合品質       | 檔搜尋結果                                                                   |
| FreeSpace        | 可用的儲存空間       | 磁碟機                                                                               |
| NumberOfVisits   | 瀏覽次數              | 我的最愛資料夾                                                                          |
| 屬性       | 檔案屬性               | 標準資料夾詳細資料檢視                                                              |
| 公司          | 公司名稱                  | [**PIDDSI \_ 公司**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| 類別         | 檔類別             | [**PIDDSI \_ 類別**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| 著作權        | 媒體著作權               | [**PIDMSI \_ 著作權**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md) |
| HTMLInfoTipFile  | HTML 提示檔             | 資料夾的 Desktop.ini 檔案                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[註冊 Shell 延伸模組處理常式](reg-shell-exts.md)
</dt> </dl>

 

 
