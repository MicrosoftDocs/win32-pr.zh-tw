---
description: 為了確保您的資料已編制索引，並在搜尋期間正確呈現給使用者，您需要執行 Shell 資料存放區 (也稱為 Shell 命名空間延伸模組) ，以及檔案類型處理常式 (也稱為 Shell 擴充、延伸模組處理常式或 Shell 延伸模組處理常式) 。
ms.assetid: 38cebb3c-51bf-439c-8d4e-445344f6cb66
title: 新增圖示、預覽和快捷方式功能表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433fd066d63480147621d46c7c8ffb24cea348225ec5e564b5f6c799714c9bc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118052215"
---
# <a name="adding-icons-previews-and-shortcut-menus"></a>新增圖示、預覽和快捷方式功能表

為了確保您的資料已編制索引，並在搜尋期間正確呈現給使用者，您需要執行 Shell 資料存放區 (也稱為 [Shell 命名空間延伸](../shell/nse-works.md) 模組) ，以及檔案類型處理常式 (也稱為 shell 擴充、 [延伸模組處理](../shell/handlers.md)程式或 shell 延伸模組處理常式) 。

本主題說明下列介面：

-   [執行檔案類型處理常式](#implementing-file-type-handlers)
    -   [IPersist](#ipersist)
    -   [IPersistFolder](#ipersistfolder)
    -   [IShellFolder](#ishellfolder)
    -   [ICoNtextMenu](#icontextmenu)
    -   [IExtractIcon](#iextracticon)
    -   [IPreviewHandler](#ipreviewhandler)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="implementing-file-type-handlers"></a>執行檔案類型處理常式

這些 Shell 擴充或檔案類型處理常式可為您的使用者提供下列 Shell 體驗：

-   結果檢視會顯示您專案類型的特定圖示。
-   當使用者選取專案時，結果檢視會顯示專案的預覽。
-   使用者可以按兩下專案來起始事件，例如開啟檔案。
-   使用者可以滑鼠右鍵按一下專案，以存取快捷方式 (內容) 功能表。
-   使用者可以拖放專案。

如同所有元件物件模型 (COM) 物件，檔案類型處理常式必須執行 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面和 class factory。

在 Windows XP 或更早版本中，處理常式也應該執行：

-   任一個 [IPersistFile 介面](/windows/win32/api/objidl/nn-objidl-ipersistfile)
-   或 [IShellExtInit 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)

在 Windows Vista 中， [IPersistFile 介面](/windows/win32/api/objidl/nn-objidl-ipersistfile)和[IShellExtInit 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)已取代為 Shell 用來初始化處理常式的下列三個介面：

-   [IInitializeWithStream 介面](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [IInitializeWithItem 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [IInitializeWithFile 介面](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)

若要提供合理的使用者體驗，您必須使用您的通訊協定處理常式來提供 Shell 資料存放區。 然後該資料存放區會作為圖示處理常式、快捷方式功能表處理常式、預覽處理常式等的「factory」。 [IShellFolder 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)需要最基本的[IPersist 介面](/windows/desktop/api/objidl/nn-objidl-ipersist)和[IPersistFolder 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)，而且[ICoNtextMenu](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)和[IExtractIcon](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)需要最基本的 IShellFolder 介面實作為。

> [!Note]  
> 應針對 **IPersist**、 **IPersistFolder** 和 **IShellFolder** 執行相同的類別識別碼 (CLSID) 。

 

如需建立 Shell 資料存放區以支援通訊協定處理常式的詳細資訊，請參閱 [執行基本資料夾物件介面](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85))。

### <a name="ipersist"></a>IPersist

**IPersist** 介面會定義單一方法 **GetClassID**，其設計目的是要提供可持續儲存在系統中之物件的 CLSID。



| 方法     | 描述                                      |
|------------|--------------------------------------------------|
| GetClassID | 傳回 Shell 資料存放區物件的 CLSID。 |



 

### <a name="ipersistfolder"></a>IPersistFolder

**IPersistFolder** 介面是用來初始化 Shell 資料夾物件。 此介面的實作為衍生自 **IPersist** 的介面，是資料夾在 Shell 命名空間中的通知位置。 您不會直接使用此介面。 它是由 [IShellFolder：： BindToObject 方法](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) 的檔案系統實作為初始化 Shell 資料夾物件時使用。



| 方法     | 描述                                                                                            |
|------------|--------------------------------------------------------------------------------------------------------|
| 初始化 | 指示 Shell 資料夾物件根據傳遞的資訊進行初始化，並傳回 S \_ 確定 |



 

### <a name="ishellfolder"></a>IShellFolder

[IShellFolder 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)介面是用來管理資料夾，而且需要部分執行，如此一來，針對通訊協定處理常式所執行的圖示和內容介面在 Windows Search 結果使用者介面中的運作方式會正確。 需要的大部分功能都是透過 **GetUIObjectOf** 方法來公開。 這個方法可讓增益集查詢 **IExtractIcon** 和 **ICoNtextMenu** 介面。

[IShellFolder 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)介面會使用 pidl 而非 url。 相對於完整 Shell 資料存放區的需求，增益集可以使用只包含 URL 的簡單 IDL 結構。

您必須執行下列 [IShellFolder 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 的方法。 其中五種方法需要進行基本的執行。



| 方法           | 描述                                                                                                                                                                                                                                                                   |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BindToObject     | 傳回 E \_ >notimpl                                                                                                                                                                                                                                                            |
| BindToStorage    | 傳回 E \_ >notimpl                                                                                                                                                                                                                                                            |
| CreateViewObject | 傳回 E \_ >notimpl                                                                                                                                                                                                                                                            |
| SetNameOf        | 傳回 E \_ >notimpl                                                                                                                                                                                                                                                            |
| ParseDisplayName | 將 URL 轉換成 PIDL 結構                                                                                                                                                                                                                                          |
| CompareIDs       | 比較兩個 PIDL 值                                                                                                                                                                                                                                                      |
| GetDisplayNameOf | 傳回 PIDL 的 URL。                                                                                                                                                                                                                                                    |
| GetUIObjectOf    | 這個方法類似 [IUnknown：： QueryInterface 方法](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))。 如果要求圖示，呼叫端會要求 IID \_ IExtractIcon; 如果要求快捷方式功能表，則呼叫端會要求 iid \_ ICoNtextMenu |



 

**IShellFolder** 不會用來列舉資料夾。 這表示資料夾的顯示名稱將會是實體 URL。 未來可能會變更。

### <a name="icontextmenu"></a>ICoNtextMenu

當 Windows Search 向使用者顯示結果時，使用者可以在專案上按一下滑鼠右鍵，並查看 **ICoNtextMenu** 介面所定義的快捷方式功能表。 快速鍵功能表也稱為內容功能表。

操作功能表上的預設動作，與按兩下專案時所採取的動作相同。 如果專案沒有對應的 **IShellFolder** 或 **ICoNtextMenu** 介面，則按兩下事件的預設行為是將 URL 當作引數傳遞至 [ShellExecute](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) 函式函數。

如需有關建立快捷方式功能表處理常式的詳細資訊，以及範例程式碼之[通訊協定處理常式的範例： Shell 擴充](-search-3x-wds-ph-ui-samplecode.md)功能，請參閱[建立內容功能表處理常式](../shell/context-menu-handlers.md)。

### <a name="iextracticon"></a>IExtractIcon

**IExtractIcon** 會根據您的通訊協定處理常式所提供的 PIDL 中的 URL，來抓取 Windows Search 使用者介面的圖示。

如需有關如何建立圖示處理常式和範例：適用于程式碼範例的[通訊協定處理常式的 Shell 擴充](-search-3x-wds-ph-ui-samplecode.md)功能，請參閱[建立圖示處理常式](../shell/how-to-create-icon-handlers.md)。

### <a name="ipreviewhandler"></a>IPreviewHandler

[IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)會呈現 Windows 檔案總管中所選取專案的豐富預覽。 預覽可在 Windows Search 4.0 或 Windows Vista 中提供 Windows Desktop Search 3.x。

若要建立自訂預覽處理常式：

1.  遵循[預覽處理常式](../shell/preview-handlers.md)中提供的指導方針，來執行採用[IStream](/windows/win32/api/objidl/nn-objidl-istream)的[IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) 。
2.  註冊您的預覽處理常式：

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx\{8895b1c6-b41f-4c1c-a562-0d564250836f}
       @ = {<Your_PreviewHandler_GUID>}
    ```

3.  完成下列兩個步驟，以針對您的 URL 執行 Shell 資料夾：
    1.  在 [IShellFolder：： GetUIObjectOf 方法](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof)中，處理 [IQueryAssociations](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) 並傳回 Shell 專案的關聯，如下列程式碼範例所示。

        ```
        CComPtr<IQueryAssociations> spqa;
        AssocCreate(CLSID_QueryAssociations, __uuidof(IQueryAssociations), &spqa);
        spqa->Init(0, L"Your_Object_Type", NULL, NULL);
        spqa->QueryInterface(riid, ppvReturn);
        ```

        

    2.  在 Shell 查詢您的 Shell 資料夾以便讓資料流程初始化預覽處理常式之後，請移至您的 [IShellFolder：： BindToObject 方法](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) 方法、處理 IID \_ istream，然後將 [ISTREAM](/windows/win32/api/objidl/nn-objidl-istream) 傳回您的 URL。

若要針對您的檔案類型重複使用現有的預覽處理常式，請執行下列兩個步驟：

1.  使用現有預覽處理常式的 CLSID 來為您的檔案類型註冊該預覽處理常式，以取代您的 \_ PreviewHandler \_ GUID> <。
2.  執行 Shell 資料夾。

如需有關建立預覽處理常式的詳細資訊，請參閱 [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) 和 [預覽處理常式](../shell/preview-handlers.md)。

## <a name="additional-resources"></a>其他資源

-   如需索引編制程式的總覽，請參閱 [索引](-search-indexing-process-overview.md)程式。
-   如需建立處理常式的詳細資訊，請參閱 [註冊 Shell 擴充](../shell/reg-shell-exts.md)功能、 [建立 Shell 延伸模組處理常式](../shell/handlers.md)、 [內容功能表](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))、 [Shell 命名空間延伸](../shell/nse-works.md) 和 [預覽處理常式](../shell/preview-handlers.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[開發通訊協定處理常式](-search-3x-wds-phaddins.md)
</dt> <dt>

[瞭解通訊協定處理常式](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[通知索引變更](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[程式碼範例：通訊協定處理常式的 Shell 擴充功能](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[安裝和註冊通訊協定處理常式](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[建立通訊協定處理常式的搜尋連接器](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[偵錯工具通訊協定處理常式](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
