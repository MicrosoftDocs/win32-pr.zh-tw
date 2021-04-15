---
description: 篩選處理常式是 IFilter 介面的執行，可掃描檔中的文字和屬性。
ms.assetid: 2ee9ea19-ae03-4f14-8f06-f8aa670e204e
title: 瞭解 Windows Search 中的篩選處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49cc1d3e479ae03645665618c60a33bdcfe19ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511102"
---
# <a name="understanding-filter-handlers-in-windows-search"></a>瞭解 Windows Search 中的篩選處理常式

篩選處理常式是 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的執行，可掃描檔中的文字和屬性。 篩選處理常式會將這些專案中的文字區塊解壓縮，並篩選出內嵌的格式，並保留文字位置的相關資訊。 它們也會解壓縮值的區塊，也就是檔案屬性。 **IFilter** 是建立高階應用程式的基礎，例如檔索引子和與應用程式無關的檢視器。

本主題的組織方式如下：

- [關於 IFilter 介面](#about-the-ifilter-interface)
  - [隔離流程](#isolation-process)
  - [IFilter Dll](#ifilter-dlls)
  - [IFilter 結構](#ifilter-structure)
  - [機器碼](#native-code)
- [尋找 IFilter 類別識別碼](#finding-the-ifilter-class-identifier)
  - [IFilter：： GetChunk 和地區設定碼識別碼](#ifiltergetchunk-and-locale-code-identifiers)
- [其他資源](#additional-resources)
- [相關主題](#related-topics)

## <a name="about-the-ifilter-interface"></a>關於 IFilter 介面

Microsoft Windows Search 會使用篩選器來解壓縮專案的內容，以包含在全文檢索索引中。 您可以藉由撰寫篩選器來解壓縮內容，並使用屬性處理常式來解壓縮檔案的屬性，藉此擴充 Windows Search 來編制新的或專屬檔案類型的索引。

[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)介面的設計目的是為了符合全文搜尋引擎的特定需求。 像 Windows Search 的全文搜尋引擎會呼叫 **IFilter** 方法，以將文字和屬性資訊解壓縮，並將其新增至索引。 Windows Search 將傳回的 [**IFilter：： GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) 方法的結果分成單字，將其正規化，並將它們儲存在索引中。 如果有的話，搜尋引擎會使用文字區塊 (LCID) 的語言代碼識別碼，來執行特定語言的斷詞和正規化。

Windows Search 使用下表所述的三個函式，來存取已註冊的篩選處理常式 ([**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面) 的實作為。 這些函數在載入和系結至内嵌物件的篩選處理常式時特別有用。

| 函式               | 描述                                                                                                                                                                                               |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LoadIFilter            | 取得最適合指定之內容類型的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 指標。                                                                                            |
| BindIFilterFromStorage | 取得 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 的指標，最適合 [IStorage 介面](/windows/win32/api/objidl/nn-objidl-istorage) 物件中所含的內容。 |
| BindIFilterFromStream  | 取得最適合指定類別識別碼的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 指標， (CLSID) 從資料流程變數抓取。                                                 |

[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)介面有五個方法，如下表所述。

| 方法                                                    | 描述                                                                                                        |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**IFilter：： Init**](/windows/win32/api/filter/nf-filter-ifilter-init)          | 初始化篩選會話。                                                                                   |
| [**IFilter：： GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk)     | 在第一個或下一個區塊的開頭放置 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ，並傳回描述項。 |
| [**IFilter：： GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext)       | 抓取目前區塊中的文字。                                                                             |
| [**IFilter：： GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue)     | 從目前的區塊抓取值。                                                                           |
| [**IFilter：： BindRegion**](/windows/win32/api/filter/nf-filter-ifilter-bindregion) | 抓取代表物件之指定部分的介面。 保留供未來使用。                      |

### <a name="isolation-process"></a>隔離流程

Windows Search 在具有限制許可權的本機系統安全性內容中執行 Ifilter。 在此 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 主機隔離流程中，會移除一些許可權：

- 限制的程式碼
- 所有人
- 本機
- 互動式
- 驗證的使用者
- 內建使用者
- 使用者的安全識別碼 (SID) 

移除這些許可權表示 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面沒有磁片系統或網路或任何使用者介面或剪貼簿功能的存取權。 此外，隔離進程會在防止建立子進程的工作物件下執行，並在工作集上強加 100 MB 的限制。 **IFilter** 介面主機隔離進程會提高編制索引平臺的穩定性，因為可能會不正確地執行協力廠商篩選。

> [!NOTE]  
> 您必須撰寫篩選處理常式來管理緩衝區，並正確地堆疊。 所有字串複本都必須有明確的檢查，以防止緩衝區溢位。 您應該一律確認已配置的緩衝區大小。 您應該一律依據緩衝區大小來測試資料的大小。

### <a name="ifilter-dlls"></a>IFilter Dll

[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) Dll 會執行 **IFilter** 介面，讓用戶端可以從檔案類型、類別或察覺的型別中解壓縮文字和屬性值資訊。 Windows Search 篩選進程 **SearchFilterHost.exe** 系結至為專案註冊之類別、感知類型或副檔名的 **IFilter** 。

### <a name="ifilter-structure"></a>IFilter 結構

每個 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 都是一個 DLL 檔案，它會 (COM) server 來提供指定的篩選功能，以執行同進程元件物件模型。 下圖說明典型的 **IFilter** dll 的整體結構。 更複雜的範例可能會執行一個以上的 **IFilter** 類別。

![一般 ifilter dll 結構的圖表](images/ifilter-structure.png)

### <a name="native-code"></a>機器碼

您必須以機器碼撰寫篩選器，因為可能的 common language runtime (CLR) 在中執行多個增益集的進程的版本控制問題。 在 Windows 7 （含）以後版本和更新版本中，會明確封鎖以 managed 程式碼撰寫的篩選。

## <a name="finding-the-ifilter-class-identifier"></a>尋找 IFilter 類別識別碼

[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL 的類別會在 PersistentHandler 登錄機碼下註冊。 下列 HTML 檔案範例將說明如何尋找 HTML 檔案的 **IFilter** DLL。 這個範例會遵循類似于系統用來尋找與專案相關聯之 **IFilter** 的邏輯。

1. 檢查 DLL 所篩選之檔案類型的副檔名是否有在登錄專案 \\ HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別下註冊的 PersistentHandler。 讓此機碼成為 `Value1` 。 如果該專案已經存在，請跳到此程式的步驟4，並 `Value1` 在該機碼中使用。 值的類型是 REG \_ SZ。

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             .htm
                PersistentHandler
                   {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

2. 或者，如果沒有針對延伸模組註冊的 PersistentHandler，請在 \\ HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別的登錄專案底下，尋找與檔案類型相關聯的 CLSID。 讓此機碼成為 `Value2` 。

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                 = Class for WWW HTML files
                CLSID
                   {25336920-03F9-11CF-8FD0-00AA00686F13}
```

3. 判斷是否已為 CLSID 註冊 PersistentHandler。 `Value2`在步驟2中決定使用，尋找 \\ HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ CLSID \\ Value2 專案的 PersistentHandler。 讓此機碼成為 `Value3` 。

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                 = Class for WWW HTML files
                PersistentHandler
                   {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

4. 判斷 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 持續性處理常式 GUID。 使用 `Value1` 和 `Value3` ，尋找檔案類型的 **IFilter** 持續性處理常式 GUID。 登錄專案 \\ HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ CLSID \\ Value1 或 3 \\ PersistentAddinsRegistered \\ 89BCB740-6119-101A-BCB7-00DD010655AF "/> 下的值會產生此檔案類型的 **IFilter** PersistentHandler GUID。 讓此機碼成為 `Value4` 。 在此範例中， **IFilter** 介面 GUID 是89BCB740-6119-101A-BCB7-00DD010655AF。

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             {EEC97550-47A9-11CF-B952-00AA0051FE20}
                 = HTML File Persistent Handler
                    Data type         REG_SZ
                        PersistentAddinsRegistered
                        {89BCB740-6119-101A-BCB7-00DD010655AF}

                    Data type         REG_SZ
                        default = {E0CA5340-4534-11CF-B952-00AA0051FE20}
```

> [!NOTE]  
> 在此範例中，會 nlhtml.dll HTML 檔案的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL。

### <a name="ifiltergetchunk-and-locale-code-identifiers"></a>IFilter：： GetChunk 和地區設定碼識別碼

文字的 LCID 可以在單一檔案中變更。 例如，指令手動的文字可能會在英文 (en-us) 和西班牙文 (es) ，或文字可能包含非主要語言的單一單字。 無論是哪一種情況，您的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 都必須在每次 LCID 變更時開始新的區塊。 因為 LCID 是用來選擇適當的斷詞工具，所以請務必正確地加以識別。 如果 **IFilter** 無法判斷文字的地區設定，則它應該會傳回值為零的 LCID 和區塊。 傳回零的 LCID 會導致 Windows Search 使用語言自動偵測 (LAD) 技術來判斷區塊的地區設定識別碼。 如果 Windows Search 找不到相符項，則會藉由呼叫 [GetSystemDefaultLocaleName 函數](/windows/win32/api/winnls/nf-winnls-getsystemdefaultlocalename) 函數) ，預設為系統預設的地區設定 (。 如需詳細資訊，請參閱 [**IFilter：： GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk)、 [**區塊 \_ BREAKTYPE**](/windows/win32/api/filter/ne-filter-chunk_breaktype)、 [**CHUNKSTATE**](/windows/win32/api/filter/ne-filter-chunkstate)和 [**STAT \_ 區塊**](/windows/win32/api/filter/ns-filter-stat_chunk)。

如果您控制檔案格式，但目前不包含地區設定資訊，您應該新增使用者功能，以啟用適當的地區設定識別。 使用不相符的斷詞工具可能會導致使用者的查詢體驗不佳。 如需詳細資訊，請參閱 [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker)。

> [!NOTE]  
> 篩選器會與檔案類型相關聯，如副檔名、MIME 類型或 Clsid 所表示。 雖然一個篩選準則可以處理多個檔案類型，但每個類型只能使用一個篩選準則。

## <a name="additional-resources"></a>其他資源

- [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample7)上提供的 [IFilterSample](-search-sample-ifiltersample.md)程式碼範例會示範如何建立用來執行 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter)介面的 ifilter 基礎類別。
- 如需索引編制程式的總覽，請參閱 [索引](-search-indexing-process-overview.md)程式。
- 如需檔案類型的總覽，請參閱 [檔案類型](../shell/fa-file-types.md)。
- 若要查詢檔案類型的檔案關聯屬性，請參閱 [PerceivedTypes、SystemFileAssociations 和應用程式註冊](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))。

## <a name="related-topics"></a>相關主題

[開發篩選處理常式](-search-ifilter-conceptual.md)

[在 Windows Search 中建立篩選處理常式的最佳作法](-search-3x-wds-extidx-filters.md)

[從篩選處理常式傳回屬性](-search-ifilter-property-filtering.md)

[Windows 隨附的篩選處理常式](-search-ifilter-implementations.md)

[在 Windows Search 中執行篩選處理常式](-search-ifilter-constructing-filters.md)

[註冊篩選處理常式](-search-ifilter-registering-filters.md)

[測試篩選處理常式](-search-ifilter-testing-filters.md)
