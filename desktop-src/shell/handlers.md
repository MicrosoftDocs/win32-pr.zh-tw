---
description: 您可以使用登錄專案和 .ini 檔案來擴充 Shell 的功能。
ms.assetid: 74a81e4f-7357-4901-a118-ba44e8892f25
title: 建立 Shell 擴充功能處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991f3c1684b7491e2ad29fae29f48164ffdd47cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991574"
---
# <a name="creating-shell-extension-handlers"></a>建立 Shell 擴充功能處理常式

您可以使用登錄專案和 .ini 檔案來擴充 Shell 的功能。 雖然這種擴充 Shell 的方法很簡單，且適用于許多用途，但有限。 例如，如果您使用登錄來指定檔案類型的自訂圖示，就會針對該類型的每個檔案顯示相同的圖示。 使用登錄延伸 Shell 不允許您變更相同類型之不同檔案的圖示。 Shell 的其他層面（例如，在檔案以滑鼠右鍵按一下時可顯示的 [ **屬性** ] 屬性工作表），無法透過登錄來修改。

擴充 Shell 的一個更強大且靈活的方法，就是執行 *shell 擴充處理常式*。 您可以針對 Shell 可執行檔各種動作，執行這些處理常式。 在採取動作之前，Shell 會查詢延伸模組處理常式，讓它有機會修改動作。 常見的範例是快捷方式功能表延伸模組處理常式。 如果是針對檔案類型所執行，則會在每次以滑鼠右鍵按一下其中一個檔案時進行查詢。 然後，處理常式可以依檔案逐一指定其他功能表項目，而不是對整個檔案類型使用相同的集合。

本檔將討論如何執行延伸模組處理常式，讓您修改各種 Shell 動作。 下列處理常式會與特定檔案類型相關聯，並可讓您以檔案為基礎來指定：



| 處理常式                                               | 描述                                                                                                                                                                |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [快速鍵功能表處理常式](context-menu-handlers.md)    | 在顯示檔案的快捷方式功能表之前呼叫。 它可讓您依檔案逐一將專案新增至快捷方式功能表。                                               |
| [資料處理程式](how-to-create-data-handlers.md)       | 在 dragShell 物件上執行拖放作業時呼叫。 它可讓您提供其他剪貼簿格式給放置目標。                        |
| [捨棄處理常式](how-to-create-drop-handlers.md)       | 當資料物件在檔案上拖放或卸載時呼叫。 它可讓您將檔案放入放置目標。                                                          |
| [圖示處理常式](how-to-create-icon-handlers.md)       | 在顯示檔案的圖示之前呼叫。 它可讓您以檔案為基礎，以自訂圖示取代檔案的預設圖示。                                    |
| [屬性工作表處理常式](propsheet-handlers.md)      | 在顯示物件的 [ **屬性** ] 屬性工作表之前呼叫。 它可讓您新增或取代頁面。                                                              |
| [**縮圖影像處理常式**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) | 提供表示專案的影像。                                                                                                                                   |
| [**資訊提示處理常式**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                 | 當使用者將滑鼠指標移至物件上方時，提供快顯視窗。                                                                                               |
| [**元資料處理程式**](/windows/win32/api/propsys/nn-propsys-ipropertystore)     | 提供中繼資料的讀取和寫入存取 (屬性) 儲存在檔案中。 這可以用來擴充詳細資料檢視、提示、屬性頁和群組功能。 |



 

其他處理常式不會與特定檔案類型相關聯，但會在某些 Shell 作業之前呼叫：



| 處理常式                                                            | 描述                                                                                                                                  |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [資料行處理常式](../lwef/column-handlers.md)                             | 由 Windows 檔案總管呼叫，然後才會顯示資料夾的詳細資料檢視。 它可讓您將自訂資料行新增至詳細資料檢視。        |
| [複製勾點處理常式](how-to-create-copy-hook-handlers.md)          | 當資料夾或印表機物件即將移動、複製、刪除或重新命名時呼叫。 它可讓您核准或拒絕此作業。   |
| [拖放功能處理常式](context-menu-handlers.md)                 | 在使用滑鼠右鍵拖曳檔案時呼叫。 它可讓您修改所顯示的快捷方式功能表。                     |
| [圖示重迭處理常式](how-to-implement-icon-overlay-handlers.md) | 在顯示檔案的圖示之前呼叫。 它可讓您指定檔案圖示的覆迭。                                          |
| [搜尋處理常式](../lwef/search-handlers.md)                             | 呼叫以啟動搜尋引擎。 它可讓您執行可從 [ **開始** ] 功能表或 Windows 檔案總管存取的自訂搜尋引擎。 |



 

上述各節將說明如何執行特定延伸模組處理常式的詳細資料。 本檔的其餘部分涵蓋所有 Shell 延伸模組處理常式通用的一些執行問題。

-   [執行 Shell 延伸模組處理常式](#implementing-shell-extension-handlers)
    -   [執行 IPersistFile](#implementing-ipersistfile)
    -   [執行 IShellExtInit](#implementing-ishellextinit)
    -   [提示自訂](#infotip-customization)
-   [使用 Shell 擴充處理常式增強 Windows Search](#enhancing-windows-search-with-shell-extension-handlers)
-   [註冊 Shell 延伸模組處理常式](#registering-shell-extension-handlers)
    -   [處理常式名稱](#handler-names)
    -   [預先定義的 Shell 物件](#predefined-shell-objects)
    -   [擴充處理常式註冊的範例](#example-of-an-extension-handler-registration)
-   [相關主題](#related-topics)

## <a name="implementing-shell-extension-handlers"></a>執行 Shell 延伸模組處理常式

Shell 擴充處理常式物件的許多實作為相依于其型別。 不過，有一些常見的元素。 本節將討論所有 Shell 延伸模組處理常式所共用的執行層面。

許多 Shell 擴充處理常式都是同進程元件物件模型 (COM) 物件。 您必須將 GUID 指派給它們，如註冊 Shell 擴充處理常式中所述。 它們會實作為 Dll，而且必須匯出下列標準函式：

-   [**DllMain**](../dlls/dllmain.md)。 DLL 的標準進入點。
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)。 公開物件的 class factory。
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)。 COM 會呼叫這個函式，以判斷物件是否為任何用戶端提供服務。 如果不是，則系統可以卸載 DLL 並釋放相關聯的記憶體。

Shell 擴充處理常式和所有 COM 物件一樣，都必須執行 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面和 [class factory](../com/implementing-iclassfactory.md)。 大部分的延伸模組處理常式也都必須在 Windows XP 或更早版本中執行 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 或 [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) 介面。 這些已由 Windows Vista 中的 [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)、 [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) 和 [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) 取代。 Shell 會使用這些介面來初始化處理常式。

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)介面必須由下列各項執行：

-   資料處理程式
-   捨棄處理常式

在過去，也需要圖示處理常式來執行 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)，但這已不再成立。 針對圖示處理常式， **IPersistFile** 現在是選擇性的，而其他介面（例如 [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) ）則是慣用的。

[**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)介面必須由下列各項執行：

-   快速鍵功能表處理常式
-   拖放處理常式
-   屬性工作表處理常式

### <a name="implementing-ipersistfile"></a>執行 IPersistFile

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)介面的目的是要允許將物件載入或儲存到磁片檔案。 除了 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)、其本身的五個方法，以及它繼承自 [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist)的 [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid)方法之外，它還有六個方法。 使用 Shell 擴充功能時， **IPersist** 只會用來初始化 Shell 擴充處理常式物件。 因為通常不需要讀取或寫入磁片，所以只有 **GetClassID** 和 [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) 方法需要 nontoken 執行。

Shell 會先呼叫 [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) ，函式會傳回擴充處理常式物件 (CLSID) 的類別識別碼。 然後，Shell 會呼叫 [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) 並以兩個值傳遞。 第一個 *>pszfilename* 是 Unicode 字串，其中包含 Shell 即將操作的檔案或資料夾的名稱。 第二個是 *dwMode*，表示檔案存取模式。 因為通常不需要存取檔案， *dwMode* 通常是零。 方法會視需要儲存這些值以供稍後參考。

下列程式碼片段說明一般 Shell 擴充處理常式如何執行 [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) 和 [**載入**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) 方法。 它是設計來處理 ANSI 或 Unicode。 CLSID \_ SampleExtHandler 是延伸模組處理常式物件的 GUID，而 CSampleExtHandler 是用來執行介面的類別名稱。 **M \_ szFileName** 和 **m \_ dwMode** 變數是私用變數，用來儲存檔案的名稱和存取旗標。


```C++
wchar_t m_szFileName[MAX_PATH];    // The file name
DWORD m_dwMode;                  // The file access mode

CSampleExtHandler::GetClassID(CLSID *pCLSID)
{
    *pCLSID = CLSID_SampleExtHandler;
}

CSampleExtHandler::Load(PCWSTR pszFile, DWORD dwMode)
{
    m_dwMode = dwMode;
    return StringCchCopy(_szFileName, ARRAYSIZE(m_szFileName), pszFile);
}
```

### <a name="implementing-ishellextinit"></a>執行 IShellExtInit

[**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)介面除了 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)之外，只有一個方法 [**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)。 方法有三個參數，可供 Shell 用來傳入各種類型的資訊。 傳入的值取決於處理常式的類型，而部分可以設定為 **Null**。

-   *pIDFolder* 會保留資料夾的 (PIDL) 專案識別碼清單的指標。 若為屬性工作表延伸，則為 **Null**。 如果是快捷方式功能表延伸，則是包含要顯示其快捷方式功能表之專案的資料夾 PIDL。 若是非預設的拖放處理常式，則為目的檔案夾的 PIDL。
-   *pDataObject* 會保留資料物件的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面指標。 資料物件會以 [CF \_ HDROP](dragdrop.md) 格式保存一或多個檔案名。
-   *hRegKey* 會保留檔案物件或資料夾類型的登錄機碼。

[**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)方法會視需要儲存檔案名、 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)指標和登錄機碼，以供稍後使用。 下列程式碼片段說明 **IShellExtInit：： Initialize** 的實作為。 為了簡單起見，此範例假設資料物件只包含單一檔案。 一般情況下，它可能會包含多個需要解壓縮的檔案。


```C++
LPCITEMIDLIST  m_pIDFolder;           //The folder's PIDL
wchar_t        m_szFile[MAX_PATH];    //The file name
IDataObject   *m_pDataObj;            //The IDataObject pointer
HKEY           m_hRegKey;             //The file or folder's registry key

STDMETHODIMP CShellExt::Initialize(LPCITEMIDLIST pIDFolder, 
                                   IDataObject *pDataObj, 
                                   HKEY hRegKey) 
{ 
    // If Initialize has already been called, release the old PIDL
    ILFree(m_pIDFolder);
    m_pIDFolder = nullptr;

    // Store the new PIDL.
    if (pIDFolder)
    {
        m_pIDFolder = ILClone(pIDFolder);
    }
    
    // If Initialize has already been called, release the old
    // IDataObject pointer.
    if (m_pDataObj)
    { 
        m_pDataObj->Release(); 
    }
     
    // If a data object pointer was passed in, save it and
    // extract the file name. 
    if (pDataObj) 
    { 
        m_pDataObj = pDataObj; 
        pDataObj->AddRef(); 
      
        STGMEDIUM   medium;
        FORMATETC   fe = {CF_HDROP, NULL, DVASPECT_CONTENT, -1, TYMED_HGLOBAL};
        UINT        uCount;

        if (SUCCEEDED(m_pDataObj->GetData(&fe, &medium)))
        {
            // Get the count of files dropped.
            uCount = DragQueryFile((HDROP)medium.hGlobal, (UINT)-1, NULL, 0);

            // Get the first file name from the CF_HDROP.
            if (uCount)
                DragQueryFile((HDROP)medium.hGlobal, 0, m_szFile, 
                              sizeof(m_szFile)/sizeof(TCHAR));

            ReleaseStgMedium(&medium);
        }
    }

    // Duplicate the registry handle. 
    if (hRegKey) 
        RegOpenKeyEx(hRegKey, nullptr, 0L, MAXIMUM_ALLOWED, &m_hRegKey); 
    return S_OK; 
}
```

CSampleExtHandler 是用來執行介面之類別的名稱。 **M \_ pIDFolder**、 **m \_ pDataObject**、 **m \_ szFileName** 和 **m \_ hRegKey** 變數是用來儲存傳入資訊的私用變數。 為了簡單起見，此範例假設資料物件只會保留一個檔案名。 從資料物件中取出 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 結構之後，就會使用 [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) 從 **FORMATETC** 結構的 **medium. hGlobal** 成員解壓縮檔案名。 如果傳入登錄機碼，方法會使用 [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) 開啟金鑰，並將控制碼指派給 **m \_ hRegKey**。

### <a name="infotip-customization"></a>提示自訂

有兩種方式可以自訂提示：

-   執行支援 [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) 的物件，然後在登錄中的適當子機碼下註冊該物件 (請參閱) 下方 [註冊 Shell 擴充處理常式](#registering-shell-extension-handlers) 。
-   指定要顯示的固定字串或特定檔案屬性的清單。

若要顯示命名空間延伸的固定字串，請 `InfoTip` 在命名空間延伸模組的 *{CLSID}* 機碼中建立名為的專案。 將該專案的值設定為您想要顯示的常值字串（如本範例所示），或將該資源中指定資源和索引的間接字串設定為當地語系化用途) 的 (。

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

若要顯示檔案類型的固定字串，請 `InfoTip` 在該檔案類型的 *ProgID* 機碼中建立名為的專案。 將該專案的值設為您想要顯示的常值字串，或將該 (資源中指定資源和索引的間接字串設定為當地語系化用途) ，如此範例所示。

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = Resource.dll, 3
```

如果您希望 Shell 在特定檔案類型的提示中顯示特定檔案屬性，請在該 `InfoTip` 檔案類型的 *ProgID* 機碼中建立呼叫的專案。 將該專案的值設定為以分號分隔的標準屬性名稱清單、格式識別碼 (FMTID) /property 識別碼 (PID) 組或兩者。 此值必須以 "property：" 開頭，以將它識別為屬性清單字串。 如果您省略 "a："，則會將值視為常值字串，並顯示為此。

在下列範例中， *propname* 是標準的屬性名稱 (例如 System. Date) 和 *{fmtid}，pid* 是 [**fmtid/pid**](./objects.md) 組。

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = prop:propname;propname;{fmtid},pid;{fmtid},pid
```

您可以使用下列屬性名稱：



| 屬性名稱    | 描述                   | 取出來源                                                                             |
|------------------|-------------------------------|--------------------------------------------------------------------------------------------|
| 作者           | 檔作者        | [**PIDSI \_ 作者**](../stg/the-summary-information-property-set.md)                              |
| 標題            | 檔的標題         | [**PIDSI \_ 標題**](../stg/the-summary-information-property-set.md)                               |
| 主體          | 主題摘要               | [**PIDSI \_ 主旨**](../stg/the-summary-information-property-set.md)                             |
| 註解          | 檔批註             | [**PIDSI \_批註**](../stg/the-summary-information-property-set.md) 或資料夾/驅動程式屬性 |
| PageCount        | 頁面數目               | [**PIDSI \_ PAGECOUNT**](../stg/the-summary-information-property-set.md)                           |
| Name             | 易記名稱                 | 標準資料夾檢視                                                                       |
| OriginalLocation | 原始檔案的位置     | [公事包] 資料夾和資源回收筒資料夾                                                    |
| DateDeleted      | 資料檔案已刪除         | 資源回收筒資料夾                                                                         |
| 類型             | 檔案類型                  | 標準資料夾詳細資料檢視                                                               |
| 大小             | 檔案大小                  | 標準資料夾詳細資料檢視                                                               |
| SyncCopyIn       | 與 OriginalLocation 相同      | 與 OriginalLocation 相同                                                                   |
| 修改日期         | 上次修改日期            | 標準資料夾詳細資料檢視                                                               |
| 建立時間          | 建立日期                  | 標準資料夾詳細資料檢視                                                               |
| 訪問         | 上次存取日期            | 標準資料夾詳細資料檢視                                                               |
| InFolder         | 包含檔案的目錄 | 檔搜尋結果                                                                    |
| 排名             | 搜尋符合品質       | 檔搜尋結果                                                                    |
| FreeSpace        | 可用的儲存空間       | 磁碟機                                                                                |
| NumberOfVisits   | 瀏覽次數              | 我的最愛資料夾                                                                           |
| 屬性       | 檔案屬性               | 標準資料夾詳細資料檢視                                                               |
| 公司          | 公司名稱                  | [**PIDDSI \_ 公司**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)    |
| 類別         | 檔類別             | [**PIDDSI \_ 類別**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| 著作權        | 媒體著作權               | [**PIDMSI \_ 著作權**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| HTMLInfoTipFile  | HTML 提示檔             | 資料夾的 Desktop.ini 檔案                                                                |



 

## <a name="enhancing-windows-search-with-shell-extension-handlers"></a>使用 Shell 擴充處理常式增強 Windows Search

Shell 擴充處理常式可以用來增強 Windows Search 通訊協定處理常式所提供的使用者體驗。 若要啟用這類增強功能，支援的 Shell 擴充處理常式必須設計成與搜尋通訊協定處理常式整合，以作為資料來源。 如需有關如何透過與 Shell 擴充處理常式整合來增強 Windows Search 通訊協定處理常式的詳細資訊，請參閱 [加入圖示、預覽和快捷方式功能表](../search/-search-3x-wds-ph-ui-extensions.md)。 如需 Windows Search 通訊協定處理常式的詳細資訊，請參閱 [開發通訊協定處理常式](../search/-search-3x-wds-phaddins.md)。

## <a name="registering-shell-extension-handlers"></a>註冊 Shell 延伸模組處理常式

您必須先註冊 Shell 擴充處理常式物件，Shell 才能使用它。 本節是如何註冊 Shell 延伸模組處理常式的一般討論。

每當您建立或變更 Shell 延伸模組處理常式時，請務必使用 [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)來通知系統您已進行變更，並指定 **SHCNE \_ ASSOCCHANGED** 事件。 如果您未呼叫 **SHChangeNotify**，在系統重新開機之前，可能無法辨識變更。

如同所有 COM 物件，您必須使用 UUIDGEN.exe 之類的工具來建立處理常式的 GUID。 在 **HKEY \_ 類別 \_ 根目錄** CLSID 下建立索引鍵， \\ 其名稱是 GUID 的字串形式。 由於 Shell 擴充處理常式是同進程伺服器，因此您必須在 GUID 索引鍵下建立 **InProcServer32** 索引鍵，並將預設值設定為處理常式 DLL 的路徑。 使用單元執行緒模型。

每當 Shell 採取的動作都可能牽涉到 Shell 擴充處理常式時，就會檢查適當的登錄機碼。 用來註冊擴充處理常式的索引鍵，因此將會控制其呼叫的時間。 比方說，當 Shell 針對 [檔案類型](fa-file-types.md)的成員顯示快捷方式功能表時，會呼叫快捷方式功能表處理常式，是常見的作法。 在此情況下，必須在檔案類型的 **ProgID** 索引鍵下註冊處理常式。

### <a name="handler-names"></a>處理常式名稱

若要啟用 Shell 延伸模組處理常式，請使用處理程式子機碼名稱來建立子機碼 (在 [檔) 類型] 的 **ProgID** (的 [ **ShellEx** ] 子機碼下) ，或 ([預先定義之 shell 物件](#predefined-shell-objects)的 [shell 物件類型名稱) ]。

例如，如果您想要註冊 Myprogram.exe 的快捷方式功能表延伸模組處理常式，您必須先建立下列子機碼：

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

針對下列處理常式，在「處理常式子機碼名稱」機碼底下建立子機碼，其名稱是 Shell 擴充的 CLSID 的字串版本。 藉由建立多個子機碼，可以在處理常式子機碼名稱索引鍵下註冊多個擴充功能。



| 處理常式                                               | 介面          | 處理常式子機碼名稱       |
|-------------------------------------------------------|--------------------|---------------------------|
| 快速鍵功能表處理常式                                 | ICoNtextMenu       | **CoNtextMenuHandlers**   |
| Copyhook 處理常式                                      | ICopyHook          | **CopyHookHandlers**      |
| 拖放功能處理常式                                 | ICoNtextMenu       | **DragDropHandlers**      |
| 屬性工作表處理常式                                | IShellPropSheetExt | **PropertySheetHandlers** |
| Windows Vista) 中的資料行提供者處理常式 (已淘汰 | IColumnProvider    | **ColumnHandlers**        |



 

針對下列處理常式，「處理常式子機碼名稱」索引鍵的預設值是 Shell 延伸模組之 CLSID 的字串版本。 您只能為這些處理常式註冊一個擴充功能。



| 處理常式                 | 介面                                         | 處理常式子機碼名稱                        |
|-------------------------|---------------------------------------------------|--------------------------------------------|
| 資料處理程式            | IDataObject                                       | **DataHandler**                            |
| 捨棄處理常式            | IDropTarget                                       | **DropHandler**                            |
| 圖示處理常式            | IExtractIconA/W                                   | **IconHandler**                            |
| 影像處理常式           | IExtractImage                                     | **{BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}** |
| 縮圖影像處理常式 | IThumbnailProvider                                | **{E357FCCD-A995-4576-B01F-234630154E96}** |
| 資訊提示處理常式         | IQueryInfo                                        | **{00021500-0000-0000-C000-000000000046}** |
|  (ANSI ) 的 Shell 連結      | IShellLinkA                                       | **{000214EE-0000-0000-C000-000000000046}** |
| Shell 連結 (UNICODE)     | IShellLinkW                                       | **{000214F9-0000-0000-C000-000000000046}** |
| 結構化儲存體      | IStorage                                          | **{0000000B-0000-0000-C000-000000000046}** |
| 中繼資料                | IPropertyStore                                    | **PropertyHandler**                        |
| 中繼資料                | IPropertySetStorage (已在 Windows Vista) 中淘汰 | **PropertyHandler**                        |
| 釘選到開始功能表       | IStartMenuPinnedList                              | **{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}** |
| 釘選到工作列          |                                                   | **{90AA3A4E-1CBA-4233-B8BB-535773D48449}** |



 

只有包含 [IsShortCut](./links.md)專案的檔案類型才需要指定的子機碼，以將 [釘選到 **開始] 功能表** 和 [**釘選到工作列**] 新增至專案的快捷方式功能表。

在 Windows Vista 中已移除對資料行提供者處理常式的支援。 此外，從 Windows Vista 起， [**IPropertySetStorage**](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) 已被取代為 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

雖然仍支援 [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) ，但 Windows Vista 和更新版本的建議是 [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) 。

### <a name="predefined-shell-objects"></a>預先定義的 Shell 物件

Shell 會在 **HKEY \_ 類別 \_ 根目錄** 下定義其他物件，其可透過與檔案類型相同的方式來擴充。 例如，若要加入所有檔案的屬性工作表處理常式，您可以在 **PropertySheetHandlers** 索引鍵下註冊。

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

下表提供 **HKEY \_ 類別 \_ 根目錄** 的各種子機碼，您可以在這些子機碼下註冊擴充處理常式。 請注意，許多擴充程式處理常式無法在所有列出的子機碼下註冊。 如需進一步的詳細資料，請參閱特定處理常式的檔。



| 子機碼                    | Description                                                          | 可能的處理常式                                | 版本 |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|---------|
| **\** _                    | 所有檔案                                                            | 快速鍵功能表、屬性工作表、動詞 (請參閱以下)  | 全部     |
| _ *AllFileSystemObjects**  | 所有檔案和檔案資料夾                                           | 快速鍵功能表、屬性工作表、動詞             | 4.71    |
| **資料夾**                | 全部資料夾                                                          | 快速鍵功能表、屬性工作表、動詞             | 全部     |
| **目錄**             | 資料夾                                                         | 快速鍵功能表、屬性工作表、動詞             | 全部     |
| **目錄 \\ 背景** | 檔案資料夾背景                                               | 僅快捷方式功能表                               | 4.71    |
| **磁碟機**                 | MyComputer 中的所有磁片磁碟機，例如 "C： \\ "                             | 快速鍵功能表、屬性工作表、動詞             | 全部     |
| **Network**               | 網路下的整個網路 ()                              | 快速鍵功能表、屬性工作表、動詞             | 全部     |
| **網路 \\ 類型\\\#**     |  (類型的所有物件 \# 如下所示)                                    | 快速鍵功能表、屬性工作表、動詞             | 4.71    |
| **NetShare**              | 所有網路共用                                                   | 快速鍵功能表、屬性工作表、動詞             | 4.71    |
| **NetServer**             | 所有網路伺服器                                                  | 快速鍵功能表、屬性工作表、動詞             | 4.71    |
| *網路 \_ 提供者 \_ 名稱* | 網路提供者「*網路 \_ 提供者 \_ 名稱*」提供的所有物件 | 快速鍵功能表、屬性工作表、動詞             | 全部     |
| **印表機**              | 所有印表機                                                         | 快速鍵功能表，屬性工作表                    | 全部     |
| **AudioCD**               | CD 光碟機中的音訊 CD                                                 | 僅限動詞                                       | 全部     |
| **Dvd**                   | DVD 光碟機 (Windows 2000)                                              | 快速鍵功能表、屬性工作表、動詞             | 4.71    |



 

注意：

-   您可以用滑鼠右鍵按一下檔案資料夾，而不是在資料夾的任何內容中，來存取檔案資料夾背景快捷方式功能表。
-   「動詞」是在 **HKEY \_ 類別 \_ 根** 子機碼 \\  \\ **Shell** \\ **動詞** 命令下註冊的特殊命令。
-   針對 **網路** \\ **類型** \\ **\#** ，" \# " 是十進位中的網路提供者類型代碼。 網路提供者類型代碼是網路類型的最高文字。 網路類型清單是在 Winnetwk 中提供的， (WNNC \_ NET \_ \* values) 。 例如，WNNC \_ NET \_ SHIVA 是0x00330000，因此對應的型別索引鍵會是 **HKEY 類別的 \_ \_ 根** \\ **網路** \\ **類型** \\ **51** 。
-   「*網路 \_ 提供者 \_ 名稱*」是 [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea)所指定的網路提供者名稱，並已將空格轉換成底線。 例如，如果已安裝 Microsoft 網路網路提供者，其提供者名稱為「Microsoft Windows 網路」，而對應的 *網路 \_ 提供者 \_ 名稱* 為 **Microsoft \_ windows \_ network**。

### <a name="example-of-an-extension-handler-registration"></a>擴充處理常式註冊的範例

若要啟用特定處理常式，請使用處理程式的名稱，在擴充處理常式類型索引鍵下建立子機碼。 Shell 不會使用處理程式的名稱，但它必須與該類型子機碼下的所有其他名稱不同。 將名稱子機碼的預設值設定為處理常式 GUID 的字串形式。

下列範例說明使用 myp 檔案類型啟用快捷方式功能表和屬性工作表延伸模組處理常式的登錄專案：

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
      {11111111-2222-3333-4444-555555555555}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      Shellex
         ContextMenuHandler
            MyCommand
               (Default) = {00000000-1111-2222-3333-444444444444}
         PropertySheetHandlers
            MyPropSheet
               (Default) = {11111111-2222-3333-4444-555555555555}
```

本章節中討論的註冊程式必須遵循所有的 Windows 系統。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[執行擴充功能的指引 In-Process](shell-and-managed-code.md)
</dt> </dl>

 

 
