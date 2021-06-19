---
description: 本文包含建立和註冊屬性處理常式來與 Windows 屬性系統搭配使用的最佳作法和常見問題。
ms.assetid: E583A00B-F615-41c8-AECF-061F1396DB9A
title: 屬性處理常式的最佳作法和常見問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5605c39f1021fcfe91259405bb99f8981510d3dc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405951"
---
# <a name="property-handler-best-practices-and-faq"></a>屬性處理常式的最佳作法和常見問題

本主題說明如何建立及註冊屬性處理常式，以便與 Windows 屬性系統搭配使用。

本主題的組織方式如下：

-   [最佳作法](#property-handler-best-practices-and-faq)
    -   [覆寫檔案系統屬性](#overriding-file-system-properties)
    -   [以 XML 為基礎的檔案格式儲存屬性](#storing-properties-in-xml-based-file-formats)
    -   [計算的屬性](#computed-properties)
-   [常見問題集](#property-handler-best-practices-and-faq)
-   [相關主題](#related-topics)

## <a name="best-practices"></a>最佳做法

此處所述的最佳作法提供實用的執行秘訣。

### <a name="overriding-file-system-properties"></a>覆寫檔案系統屬性

檔案系統資料來源會提供檔案的部分屬性，例如：

-   PKEY \_ 檔案名
-   PKEY \_ 延伸模組
-   PKEY \_ column.modifiedtime

一般而言，屬性處理常式無法提供這些屬性的值。 不過，在某些情況下，可以根據屬性處理常式所提供的註冊資訊來覆寫這些屬性。 屬性處理常式會以要覆寫的屬性名稱填入 **HKEY \_ 類別的 \_ 根** \\ **CLSID** \\ *{handler clsid}* \\ **OverrideFileSystemProperties** 。 這僅限於系統有知識的下列清單中所顯示的一組固定屬性。

下列屬性值支援覆寫：

-   [System.string](./props-system-kind.md)
-   [System.string](./props-system-filename.md)
-   [System. IsPinnedToNameSpaceTree](./props-system-ispinnedtonamespacetree.md)
-   [System.ItemNameDisplay](./props-system-itemnamedisplay.md)
-   [System. SFGAOFlags](./props-system-sfgaoflags.md)
-   [System. ItemPathDisplay](./props-system-itempathdisplay.md)
-   [System. ItemPathDisplayNarrow](./props-system-itempathdisplaynarrow.md)
-   [System. ItemFolderNameDisplay](./props-system-itemfoldernamedisplay.md)
-   [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md)
-   [System. ItemFolderPathDisplayNarrow](./props-system-itemfolderpathdisplaynarrow.md)

如需所有 Shell 屬性的完整清單，請參閱 [Shell 屬性](./props.md)。

> [!IMPORTANT]
> 只有在為檔案編制索引時，才會使用覆寫的屬性值。 因此，從檔案系統資料來源流覽檔案並不會顯示覆寫的值。

 

### <a name="storing-properties-in-xml-based-file-formats"></a>以 XML 為基礎的檔案格式儲存屬性

有兩個基本選項可用來儲存以 XML 為基礎的檔案格式的屬性：

-   根據檔的 XML 架構，使用 XML 元素和屬性來儲存每個屬性。 這種方法比較「XML 易記」。
-   將整個屬性存放區序列化為記憶體二進位大型物件 (BLOB) ，將 BLOB 轉換為 base64 編碼的字串，然後將該字串儲存在 XML 中。 這是這兩種方法中較簡單的方法，可用來完整提供開啟中繼資料的支援。

某些處理常式可能會結合這些方法，以標準 XML 格式儲存一些重要的值，並將其餘部分儲存在 BLOB 中，例如。

### <a name="computed-properties"></a>計算的屬性

有些屬性是衍生自檔案的特定屬性。 例如， [system.object](./props-system-image-dimensions.md) 屬性是由影像檔案中影像的實際維度所決定。 因為屬性處理常式無法變更這類屬性值，所以會 `isInnate="true"` 在屬性描述中標示它們。 其他屬性是從特定屬性的一部分或藉由匯總多個屬性的值來計算。 由於這些「計算」屬性的更新會造成「來源」值的變更方式不明確，因此應該在屬性描述中標示計算屬性，或將其 `isInnate="true"` 報告為唯讀。 第二個選項是藉由指示處理常式 \_ 從 [**IPropertyStoreCapabilities：： IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable)傳回 S FALSE 來提供。

## <a name="frequently-asked-questions"></a>常見問題集

本節提供有關屬性和屬性處理常式之常見問題的解答，以及伴隨的解答。

-   **問題：** 為什麼 Windows Search 索引子載入我的屬性處理常式？

    Windows Search 索引子會以系統服務的形式執行，而且無法載入儲存在使用者設定檔目錄中的 Dll。 如果您要使用 Microsoft Visual Studio 建立和偵錯工具，它會將 DLL 放在您的使用者設定檔中 (，因此索引子) 不會載入它。 若要解決此問題，請將您的 DLL 複製到您的設定檔資料夾外 (例如，將它複製到 **C： \\ Program Files \\ >yourappname**) ，然後在該處進行註冊。

    如需開發屬性處理常式以使用 Windows Search 索引子的特定指引，請參閱 [開發 Windows Search 的屬性處理常式](../search/-search-3x-wds-extidx-propertyhandlers.md)。

-   **問題：** 透過 [**IPropertyStore：： GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) 和 [**IPropertyStore：： GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) 列舉方法可探索哪些屬性？

    並非所有屬性存放區物件的用戶端都會使用這些方法。 某些用戶端會察覺它們打算直接要求 (PKEY name) 的屬性，或是透過屬性描述清單來接收屬性資訊。 屬性探索方法會支援其他數個案例。 如果屬性不需要參與這些案例，就不需要列舉。 因此，屬性處理常式可以 \_ 針對未透過 [**IPropertyStore：： GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) 和 [**IPropertyStore：： GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) 方法探索的屬性產生非 VT 空白值。

    不過，若符合下列任一條件，則應該透過這些方法來顯示內容：

    -   **如果屬性已編制索引，使其可供搜尋：** 這表示它包含在 Windows Search 屬性存放區中， (`isColumn = "true"` 以屬性描述架構中的表示，) 或可用於全文檢索搜尋 (`inInvertedIndex = "true"`) 。 如果沒有這些旗標或沒有屬性描述，則會自動將類型 "string" 的屬性新增至反向索引，以啟用搜尋。 由於已知屬性的清單 (屬性系統中具有已安裝屬性描述的) ， (超過800個屬性) ，因此不會對屬性系統中所註冊的每個屬性詢問每個屬性處理常式是不切實際的。 相反地，索引程式會列舉其索引之每個專案的屬性處理常式中的相關屬性，並使用列舉屬性的值來建立全文檢索索引。
    -   **如果在專案的屬性集重複時，應該複製屬性：** 若要執行「複製屬性集」函式，來源專案會讓應該複製的屬性透過 [**IPropertyStore：： GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) 和 [**IPropertyStore：： GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) 方法來顯示。 不需要複製或不需要複製任何意義的屬性，也不應該納入。
    -   **如果屬性值不是空的 (VT \_空白) ：** 空白的屬性值對於用戶端來說並不有用。 當用戶端嘗試傳回空的屬性值時， \_ 會傳回 VT 空白的值。 因此，不應該列舉具有空白值的屬性。
    -   **如果叫用 "remove properties" 函式時應移除屬性：** 這項功能的存在是為了保護隱私權;它會透過列舉來探索屬性處理常式中的所有值，並移除每一個選取供使用者移除的值。
        > [!Note]  
        > 如果處理常式支援固定的架構 (而非開啟的中繼資料) ，則列舉屬性不會傳達特定屬性處理常式支援的屬性集合。 相反地，這類處理常式應該記錄其所支援的屬性集合。

         

-   **問題：** 如何? 知道哪些檔案格式支援開放中繼資料？

    如需開啟中繼資料支援的相關資訊，請參閱 [檔案類型](../shell/fa-file-types.md)中的「支援開放中繼資料的檔案類型」。

-   **問題：** 是否可以 \_ 使用屬性處理常式來儲存 VT Null 值？

    否。 \_ \_ 在 [**IPropertyStore：： GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85))和 [**IPropertyStore：： SETVALUE**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))的呼叫上，VT Null 值會轉換成 vt 空白。

-   **問題：**[**PropVariantChangeType**](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype)函數支援哪些日期字串格式？

    一般而言，表示日期/時間值的屬性應該使用 VT FILETIME 表示 \_ 。 但是，許多資料來源會以字串形式提供此資訊。 [**PropVariantChangeType**](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) helper API 支援將某些字串日期格式強制轉成 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)值，如下表所示。

    

    | 格式                  | Windows Vista、Windows XP 和 Microsoft Windows 桌面搜尋 (WDS)  | Windows 7 | 備註                                                                                                                                                                                                 |
    |-------------------------|-----------------------------------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | yyyy/mm/dd： hh： mm： ss. uuu | 是                                                                   | 是       | UTCy = year、m = month、d = date、h = hours (24 小時制) 、m = 分鐘、s = 秒、u = 微秒                                                                                                           |
    | yyyy-mm-dd-ddThh： mm： ssZ    | 否                                                                    | 是       | **ISO8601 格式規格** UTC (以 ' Z ' 時區指標表示) ;y = year、m = month、d = date、h = hours (24 小時制) 、m = 分鐘、s = 秒;T ' 是時間部分的分隔符號。<br/> |

    

     

-   **問題：** 是否可以建立唯讀屬性處理常式？

    是。 某些屬性處理常式的執行不支援寫入屬性值。 這些屬性處理常式應該會 \_ 傳回 STGM E \_ ACCESSDENIED 呼叫 **IInitializeXXX：： Initialize** 的呼叫，該呼叫會通過 STGM \_ READWRITE 或對 [**IPropertyStore：： SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))的任何呼叫。

    所有以 STGM READ 模式開啟的屬性處理常式 \_ ，都應該 \_ \_ 在呼叫 [**IPropertyStore：： SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))時傳回 STGM E ACCESSDENIED。

-   **問題：** 屬性處理常式可以將屬性視為唯讀，即使架構指出該屬性可寫入？

    是。 在架構系統中，會將屬性標注為唯讀 (包括具有 `isInnate = "true"`) 或讀取/寫入的屬性。 不支援寫入架構所示之特定屬性的屬性處理常式應為該屬性的 [](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) \_ [**IPropertyStoreCapabilities：： IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable)呼叫執行 IPropertyStoreCapabilities 並傳回 FALSE。 這表示在此處理程式和這個檔案的內容中，無法寫入屬性。

    > [!Note]  
    > 無法進行反向動作。 您無法啟用屬性處理常式來撰寫在架構中標示為唯讀的屬性

     

## <a name="related-topics"></a>相關主題

<dl> <dt>

[瞭解屬性處理常式](./building-property-handlers-properties.md)
</dt> <dt>

[使用種類名稱](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[使用屬性清單](./building-property-handlers-property-lists.md)
</dt> <dt>

[初始化屬性處理常式](./building-property-handlers-property-handlers.md)
</dt> <dt>

[註冊和散發屬性處理常式](./prophand-reg-dist.md)
</dt> </dl>

 

 
