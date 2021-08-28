---
description: Microsoft Windows Search 使用屬性處理常式從專案中將屬性值解壓縮，並使用屬性系統架構來決定應該如何編制特定屬性的索引。
ms.assetid: b475329a-1ed7-43a4-8e11-3700889a4ce9
title: 開發 Windows Search 的屬性處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3933353d8bf00c3a68a2259daf94a1ce4f13d295
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627323"
---
# <a name="developing-property-handlers-for-windows-search"></a>開發 Windows Search 的屬性處理常式

Microsoft Windows Search 使用屬性處理常式從專案中將屬性值解壓縮，並使用屬性系統架構來決定應該如何編制特定屬性的索引。 若要讀取和編制屬性值的索引，Windows Search 來叫用跨進程的屬性處理常式，以提升安全性和穩定性。 相反地，屬性處理常式會由 Windows 檔案總管在進程中叫用，以讀取和寫入屬性值。

本主題會使用 Windows Search 的特定資訊來補充[屬性系統](../properties/building-property-handlers.md)主題，並包含下列各節：

-   [屬性處理常式的設計決策](#design-decisions-for-property-handlers)
    -   [屬性決策](#property-decisions)
    -   [全文檢索支援](#full-text-support)
    -   [作業系統 Implementatation 考慮](#operating-system-implementatation-considerations)
-   [寫入屬性描述檔](#writing-property-description-files)
-   [執行屬性處理常式](#implementing-property-handlers)
    -   [IInitializeWithStream](#iinitializewithstream)
    -   [IPropertyStore](#ipropertystore)
    -   [IPropertyStoreCapabilities](#ipropertystorecapabilities)
-   [確保您的專案獲得索引](#ensuring-your-items-get-indexed)
-   [安裝和註冊屬性處理常式](#installing-and-registering-property-handlers)
-   [測試和疑難排解屬性處理常式](#testing-and-troubleshooting-property-handlers)
    -   [安裝和設定測試](#installation-and-setup-tests)
    -   [針對屬性處理常式進行疑難排解](#troubleshooting-property-handlers)
-   [使用 System-Supplied 屬性處理常式](#using-system-supplied-property-handlers)
-   [相關主題](#related-topics)

 

## <a name="design-decisions-for-property-handlers"></a>屬性處理常式的設計決策

執行屬性處理常式涉及下列步驟：

1.  針對您想要支援的屬性做出設計決策。
2.  針對尚未存在於屬性系統中的屬性，建立屬性描述 ( propdesc) 檔。
3.  執行和測試屬性處理常式。
4.  安裝和註冊屬性處理常式和屬性描述檔。
5.  測試屬性處理常式的安裝和註冊。

開始之前，您必須考慮下列設計問題：

-   檔案格式支援哪些屬性（property）？
-   這些屬性是否已存在於系統架構中？
-   我可以使用現有的系統提供的屬性處理常式嗎？
-   哪些屬性可以顯示給終端使用者？
-   使用者可以編輯哪些屬性？
-   全文檢索搜尋是否應該支援來自屬性處理常式或篩選準則？
-   我是否需要支援繼承應用程式？ 如果是，該如何實行？

> [!Note]  
> 繼續之前，請參閱 [使用 System-Supplied 屬性處理常式](#using-system-supplied-property-handlers) 來查看您是否可以使用系統提供的屬性處理常式，同時為您節省時間和開發資源。

 

完成這些決策之後，您可以撰寫自訂屬性的正式描述，讓 Windows Search 引擎可以開始編制檔案和屬性的索引。 這些正式描述是 XML 檔案，如 [屬性描述架構](/previous-versions//cc144127(v=vs.85))中所述。

### <a name="property-decisions"></a>屬性決策

當考慮要支援哪些屬性時，您應該找出使用者的索引編制和搜尋需求。 例如，您可以為您的檔案類型找出100可能有用的屬性，但使用者可能只想要搜尋少數內容。 此外，您可能會想要對 Windows 檔案總管中的使用者顯示不同、較大或較小的屬性群組，並允許使用者只編輯顯示的部分屬性。

您的檔案類型可以支援您所定義的任何自訂屬性，以及一組系統定義的屬性。 在您建立自訂屬性之前，請先檢查 [系統屬性](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) ，以查看您要支援的屬性是否已由系統屬性定義。 務必確定您支援最重要的系統定義屬性。

我們建議使用矩陣來協助您設計屬性：



| 屬性名稱 | 可編制索引嗎？ | 可顯示嗎？ | 是否可編輯？ |
|---------------|---------------|-----------------|--------------|
| property1     | Y             | Y               | N            |
| 財產。。。   | Y             | Y               | N            |
| propertyn     | N             | N               | N            |



 

針對上述每個屬性，您必須決定應該擁有哪些屬性，然後在屬性描述 XML 檔案 ( propdesc) 中正式描述這些屬性。 屬性包含屬性的資料類型、標籤、說明字串等等。 針對可編制索引的屬性，您應該特別注意在屬性描述檔的 [searchInfo](../properties/propdesc-schema-searchinfo.md)   XML 元素中找到的下列屬性屬性。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>inInvertedIndex</td>
<td>選擇性。 指出是否應該將字串屬性值分成單字，並將每個單字儲存在反向索引中。 反向索引可讓您有效率地使用 CONTAINS 或 FREETEXT (的屬性值搜尋單字和片語，例如，SELECT .。。其中包含 &quot; sometext &quot;) 。 如果設定為 <strong>FALSE</strong>，則會對整個字串執行搜尋。 大部分的字串屬性都必須設為 <strong>TRUE</strong>。非字串屬性的值應該設定為 <strong>FALSE</strong>。 預設值為 <strong>FALSE</strong>。</td>
</tr>
<tr class="even">
<td>isColumn</td>
<td>選擇性。 指出屬性是否應該以資料行的形式儲存在 Windows Search 資料庫中。 將屬性儲存為數據行可讓您使用任何述詞來進行抓取、排序、分組和篩選 (也就是在整個資料行值上使用 CONTAINS 或 FREETEXT) 以外的任何述詞。 顯示給使用者的屬性應該設定為 [ <strong>TRUE</strong> ]，除非它是非常大的文字屬性 (像是要在反向索引中搜尋之檔) 的主體。 預設值為 <strong>FALSE</strong>。</td>
</tr>
<tr class="odd">
<td>isColumnSparse</td>
<td>選擇性。 指出如果值為 <strong>Null</strong>時，屬性是否不使用空格。 非 sparse 屬性會針對每個專案採用空間，即使值為 <strong>Null</strong>也是一樣。 如果屬性是多重值，則這個屬性一律 <strong>為 TRUE</strong>。 只有在每個專案都有值時，這個屬性才會是 <strong>FALSE</strong> 。 預設值為 <strong>TRUE</strong>。</td>
</tr>
<tr class="even">
<td>columnIndexType</td>
<td>選擇性。 為了優化查詢，Windows Search 引擎可以針對具有 isColumn =<strong>TRUE</strong>的屬性建立次要索引。 在編制索引期間，這需要更多處理和磁碟空間，但在查詢期間可改善效能。 如果屬性通常會排序、分組或篩選 (也就是使用 =、！ =、<、>，例如，會比對使用者經常) ，則此屬性應該設定為 &quot; OnDisk &quot; 。 預設值為 &quot; NotIndexed &quot; 。 下列是有效值：
<ul>
<li>NotIndexed：未建立次要索引。</li>
<li>OnDisk：在磁片上建立並儲存次要索引。</li>
</ul></td>
</tr>
<tr class="odd">
<td>maxSize</td>
<td>選擇性。 指出 Windows 搜尋資料庫中儲存的屬性值所允許的大小上限。 這項限制適用于向量的 indvidual 元素，而不是整個向量。 超出此大小的值會被截斷。 預設值為 &quot; 128 &quot; (bytes) 。<br/> 目前，Windows Search 在計算從檔案接受的資料量時，不會使用 maxSize。 相反地，Windows Search 使用的限制是檔案大小的產品，而 MaxGrowFactor (檔案大小 N * MaxGrowFactor) 從登錄的 HKEY_LOCAL_MACHINE >軟體 >>Windows Search >>。 預設 MaxGrowFactor 為四個 (4) 。 因此，如果您的檔案類型通常較小，但具有較大的屬性，Windows Search 可能不會接受您要發出的所有屬性資料。 不過，您可以增加 MaxGrowFactor 以符合您的需求。 <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> 在 columnIndexType 屬性中，更快速的查詢優點需要針對次要索引可能產生的較高索引時間和空間成本進行權衡。 不過，此成本只會針對具有非 **null** 值的專案付費，因此大部分屬性都可以將此屬性設定為 "OnDisk"。

 

### <a name="full-text-support"></a>全文檢索支援

一般來說，稱為 [篩選器](-search-3x-wds-extidx-filters.md)的元件支援全文檢索搜尋;不過，對於以非使用檔案格式的文字型檔案類型而言，屬性處理常式可能會以較少的開發工作來提供此功能。 您應參閱 [全文檢索內容](../properties/building-property-handlers-property-handlers.md) 一節，以取得篩選和屬性處理常式功能的比較，以協助您決定最適合您的檔案類型。 特別重要的是，篩選器可以處理多個語言程式碼識別碼 (Lcid) 每個檔案，而屬性處理常式則無法處理。

> [!Note]  
> 由於屬性處理常式無法以篩選器的方式來將內容區塊，因此大型檔案 (即使它們是簡單的檔案格式) 必須完全載入記憶體中。

 

### <a name="operating-system-implementatation-considerations"></a>作業系統 Implementatation 考慮

### <a name="implementation-information-for-windows-7"></a>Windows 7 的執行資訊

在 Windows 7 和更新版本中，註冊屬性處理常式、 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)或新的擴充功能時，會有新的行為。 當安裝新的屬性處理常式和（或） **IFilter** 時，會自動重新建立索引具有對應副檔名的檔案。

在 Windows 7 中，建議您將 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter)與其對應的屬性處理常式一起安裝，並在屬性處理常式之前註冊 **ifilter** 。 註冊屬性處理常式時，會立即開始重新編制先前索引檔案的索引，而不需要重新開機，而且會利用任何先前註冊的 IFilter (s) 來進行內容編制索引。

如果只安裝了 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) （沒有對應的屬性處理常式），則會在重新開機索引服務或系統重新開機之後，自動重新建立索引。

如需 Windows 7 特有的屬性描述旗標，請參閱下列參考主題：

-   [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags)
-   [PROPDESC \_ COLUMNINDEX \_ 類型](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)
-   [PROPDESC \_ SEARCHINFO \_ 旗標](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)

### <a name="implementation-information-for-windows-vista-and-earlier"></a>Windows Vista 及更早版本的執行資訊

在 Windows Vista 之前，篩選器提供了剖析和列舉檔案內容和屬性的支援。 隨著屬性系統的推出，屬性處理常式會在篩選處理檔案內容時，處理檔案屬性。 針對 Windows Vista，您只需要在與屬性處理常式協調的情況下開發 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)介面的部分執行，如在 [Windows Search 中建立篩選處理常式的最佳作法](-search-3x-wds-extidx-filters.md)所述。

雖然屬性系統也包含在 Windows XP 的 Windows Search 安裝中，但協力廠商和繼承應用程式可能需要篩選器處理內容和屬性。 因此，如果您是在 Windows XP 平臺上進行開發，則應該提供完整的篩選器，以及檔案類型或自訂屬性的屬性處理常式。

 

## <a name="writing-property-description-files"></a>寫入屬性描述檔

Propdesc) 屬性描述 ( XML 檔案的結構會在 [propertyDescription](../properties/propdesc-schema-propertydescription.md) 主題中說明。 搜尋的特殊興趣是 [searchInfo](../properties/propdesc-schema-searchinfo.md) 元素的屬性。 一旦決定要支援哪些屬性之後，您必須為每個屬性建立並註冊屬性描述檔案。 當您註冊 propdesc 檔案時，這些檔案會包含在架構的屬性描述清單中，並成為搜尋引擎屬性存放區中的資料行名稱。

您可以使用 [PSRegisterPropertySchema](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) 函式（呼叫架構子系統的 IPropertySystem：： RegisterPropertySchema 的包裝函式 API）來註冊自訂屬性描述。 此函式會通知架構子系統新增屬性描述架構 (. propdesc) 檔案，使用檔案路徑 (s) 至本機電腦上 (的 propdesc 檔案，通常是應用程式在 [Program Files] 下的安裝目錄。 一般而言，安裝程式或應用程式 (例如，您的屬性處理常式安裝程式) 會在安裝 propdesc 檔 (s) 之後，呼叫這個方法。

 

## <a name="implementing-property-handlers"></a>執行屬性處理常式

開發屬性處理常式牽涉到執行下列介面：

-   IInitialzeWithStream：為您的屬性處理常式提供以資料流程為基礎的初始化。
-   IPropertyStore：列舉、取得和設定屬性值。
-   IPropertyStoreCapabilities：選擇性。 識別使用者是否可以從使用者介面編輯屬性。

### <a name="iinitializewithstream"></a>IInitializeWithStream

如 [屬性系統](../properties/building-property-handlers.md) 主題所述，我們強烈建議使用 **IInitializeWithStream** 執行屬性處理常式，以執行以資料流程為基礎的初始化。 如果您選擇不執行 IInitializeWithStream，屬性處理常式必須在屬性處理常式的登錄機碼上設定 DisableProcessIsolation 旗標，以選擇不在隔離程式中執行。 停用進程隔離通常僅適用于舊版的屬性處理常式，而任何新的程式碼都應避免 strenuously。

### <a name="ipropertystore"></a>IPropertyStore

若要建立屬性處理常式，您必須使用下列方法來執行 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面。



| 方法   | 描述                                                         |
|----------|---------------------------------------------------------------------|
| Commit   | 將屬性變更儲存至檔案。                                |
| GetAt    | 從專案的屬性陣列抓取屬性索引鍵。        |
| GetCount | 取得附加至檔案的屬性數目。                 |
| GetValue | 捕獲特定屬性的資料。                             |
| SetValue | 設定新的屬性值，或取代或移除現有的值。 |



 

 

 

[**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)檔中包含執行此介面的重要考慮。

> [!Note]  
> 如果您的屬性處理常式針對指定的專案發出相同屬性的多個值，則只會將最後發出的值儲存在目錄中。

 

 

### <a name="ipropertystorecapabilities"></a>IPropertyStoreCapabilities

屬性處理常式可以選擇性地執行此介面，以停用使用者編輯特定屬性的能力。 這些屬性通常可在 [詳細資料] 頁面和窗格中編輯，但在 [執行] 屬性處理常式下不允許編輯這些屬性。 正確地執行此介面可提供比替代程式更好的使用者體驗，這是來自 Shell 的簡單執行階段錯誤。

 

## <a name="ensuring-your-items-get-indexed"></a>確保您的專案獲得索引

既然您已完成屬性處理常式，您會想要確定您的處理常式已註冊為取得索引的專案。 您可以使用 [目錄管理員](-search-3x-wds-mngidx-catalog-manager.md) 來起始重新建立索引，也可以使用 [編目範圍管理員](-search-3x-wds-extidx-csm.md) 設定預設規則，指出您想要讓索引子編目的 url。 另一個選項是遵循[Windows Search SDK 範例](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)中的重新索引程式碼範例。

如需詳細資訊，請參閱 [使用目錄管理員](-search-3x-wds-mngidx-catalog-manager.md) 和 [使用編目範圍管理員](-search-3x-wds-extidx-csm.md)。

 

## <a name="installing-and-registering-property-handlers"></a>安裝和註冊屬性處理常式

在實作為屬性處理常式的情況下，必須註冊它以及與處理常式相關聯的副檔名。 下列範例會顯示執行此動作所需的登錄機碼和值。

```
HKEY_CLASSES_ROOT
   CLSID
      {<CLSID for property handler>}
         (Default) = <Property Handler Name>
         InProcServer32
            (Default) = <full path to property handler dll>
            ThreadingModel = <your threading model>
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PropertySystem
                  PropertyHandlers
                     <.fileextention>
                        (Default) = {<CLSID for property handler>}
```

 

## <a name="testing-and-troubleshooting-property-handlers"></a>測試和疑難排解屬性處理常式

下列清單提供您應該執行的測試類型的建議：

-   測試是否從檔案類型所支援的每個單一屬性取得輸出。
-   例如，使用大屬性值（例如，在 HTML 檔案中使用大型 metatag）。
-   從屬性處理常式取得輸出之後，或使用像是在列舉檔案屬性之前和之後的 oh.exe 之類的工具，檢查屬性處理常式是否未洩漏檔案控制代碼。
-   測試與屬性處理常式相關聯的所有檔案類型。 例如，檢查 HTML 篩選器是否可搭配 .htm 和 .html 檔案類型使用。
-   使用損毀的檔案進行測試。 屬性處理常式應該會正常失敗。
-   如果應用程式支援加密，請測試屬性處理常式是否未輸出加密文字。
-   如果您的屬性處理常式支援全文檢索搜尋：
    -   在檔案內容中使用多個特殊的 Unicode 字元，並測試其輸出。
    -   測試非常大型檔的處理，以確保屬性處理常式能如預期般運作。

### <a name="installation-and-setup-tests"></a>安裝和設定測試

最後，您需要測試安裝和卸載常式。

-   安裝必須從失敗的安裝復原 (例如，從取消並重新啟動安裝) 。
-   卸載必須刪除與屬性處理常式相關聯的所有檔案。
-   卸載不能刪除與屬性處理常式安裝相關聯的檔案。
-   卸載時，與屬性處理常式相關聯的登錄機碼必須移除。
-   即使已從安裝目錄中刪除檔案，也必須使用卸載。

### <a name="troubleshooting-property-handlers"></a>針對屬性處理常式進行疑難排解

以下是開發屬性處理常式時所做的一些常見錯誤：

-   在使用者目錄下安裝 propdesc 檔案或 Dll。
-   使用相對路徑註冊元件。
-   在 HKEY CURRENT USER 下註冊元件 \_ \_ ，而不是在 HKEY \_ 本機電腦上註冊 \_ 。
-   忘記為非資料流程處理常式設定 DisableProcessIsolation。
-   將測試檔案放在未編制索引的位置。

如果您在取得屬性處理常式時遇到問題，以下是一些可協助您進行疑難排解的秘訣：

-   確認 ( 的屬性描述) 標記為 isColumn = "**true**"、isViewable = "**True**" 和 isQueryable = "**true**"。
-   確認您的 propdesc 檔案位於全域位置。
-   確認您已使用絕對路徑註冊您的 propdesc 檔案。
-   確認事件記錄檔未記錄 propdesc 檔案的註冊失敗。
-   確認您的 Dll 位於全域位置 (而不是在您的使用者設定檔) 。
-   確認 Dll 已在 HKEY \_ 本機 \_ 電腦 \\ 軟體類別下註冊 \\ 。
-   請確認您的 Dll 是使用完整路徑註冊 (或 REG 會 \_ \_ 使用系統帳戶) 已知的環境變數，展開擴充至絕對路徑的 SZ 字串。
-   確認您的屬性處理常式在 Windows 檔案總管下運作。
-   雖然我們建議使用 IInitializeWithStream，但如果您必須使用 IInitializeWithFile 或 IInitializeWithItem，請確認您指定的是 DisableProcessIsolation。
-   確認 [索引選項主控台] 將您的檔案類型列為已編制索引的檔案類型。
-   確認測試檔案位於索引位置。
-   確認自您安裝屬性處理常式之後，已修改過測試檔案。

如果您的測試檔案位於索引位置，而索引子已經將該位置編目，您需要以某種方式修改檔案，以觸發檔案的重新編制索引。

 

## <a name="using-system-supplied-property-handlers"></a>使用 System-Supplied 屬性處理常式

Windows 包含許多系統提供的屬性處理常式，您可以在檔案類型的格式相容時使用這些處理常式。 如果您定義的新副檔名使用這些格式的其中一種，您可以註冊處理常式類別識別碼 (CLSID) 的副檔名，以使用系統提供的處理常式。

您可以使用下表所列的 CLSID，針對您的檔案格式類型註冊系統提供的屬性處理常式。



| 格式          | CLSID                                  |
|-----------------|----------------------------------------|
| OLE e     | {8d80504a-0826-40c5-97e1-ebc68f953792} |
| 儲存遊戲 XML   | {ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60} |
| XPS/OPC 處理常式 | {45670FA8-ED97-4F44-BC93-305082590BFB} |
| XML             | {c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9} |



 

在建立自訂屬性之前，您應該確定沒有可改用的系統定義屬性。 您可以藉由呼叫 [**PSEnumeratePropertyDescriptions**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) 或使用 prop.exe 命令列工具來列舉系統定義的屬性。

系統架構會定義這些屬性如何與索引子互動，而且您無法變更此屬性。 此外，您用來建立、編輯及儲存檔案類型的應用程式也必須符合特定行為。 例如，如果應用程式會執行安全儲存 (在編輯期間建立暫存檔案，然後使用 ReplaceFile () 來交換舊) 的新版本，則必須將原始檔案的所有屬性傳送至新的檔案。 失敗的原因表示檔案遺失使用者或其他應用程式所新增的屬性。

 

**範例**

下圖顯示使用之檔案類型的系統提供的 OLE e 處理常式註冊。OLEDocFile 延伸模組。

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         shellex
            {BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}
               (Default) = {9DBD2C50-62AD-11d0-B806-00C04FD706EC}
```

下圖顯示內容清單資訊的註冊，以及的屬性。OLEDocFile 檔案會顯示在 [詳細資料] 索引標籤和窗格上。

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         ExtendedTileInfo = prop:System.ItemType;System.Size;System.DateModified;System.Author;System.OfflineAvailability
         FullDetails = prop:System.PropGroup.Description;System.Title;System.Subject;
System.Keywords;System.Category;System.Comment;System.PropGroup.Origin;
System.Author;System.Document.LastAuthor;System.Document.RevisionNumber;
System.Document.Version;System.ApplicationName;System.Company;System.Document.Manager;
System.Document.DateCreated;System.Document.DateSaved;System.Document.DatePrinted;
System.Document.TotalEditingTime;System.PropGroup.Content;System.ContentStatus;
System.ContentType;System.Document.PageCount;System.Document.WordCount;
System.Document.CharacterCount;System.Document.LineCount;
System.Document.ParagraphCount;System.Document.Template;System.Document.Scale;
System.Document.LinksDirty;System.Language;System.PropGroup.FileSystem;
System.ItemNameDisplay;System.ItemType;System.ItemFolderPathDisplay;
System.DateCreated;System.DateModified;System.Size;System.FileAttributes;
System.OfflineAvailability;System.OfflineStatus;System.SharedWith;
System.FileOwner;System.ComputerName
         InfoTip = prop:System.ItemType;System.Size;System.DateModified;System.Document.PageCoun
         PerceivedType = document
         PreviewDetails = prop:*System.DateModified;System.Author;System.Keywords;
*System.Size;System.Title;System.Comment;System.Category;
*System.Document.PageCount;System.ContentStatus;System.ContentType;
*System.OfflineAvailability;*System.OfflineStatus;System.Subject;
*System.DateCreated;*System.SharedWith
```

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[屬性對應](-search-3x-wds-propertymappings.md)
</dt> <dt>

**概念**
</dt> <dt>

[在 Windows Search 中建立篩選處理常式的最佳作法](-search-3x-wds-extidx-filters.md)
</dt> <dt>

[索引處理常式](-search-indexing-process-overview.md)
</dt> <dt>

[開發通訊協定處理常式](-search-3x-wds-phaddins.md)
</dt> <dt>

[自訂檔案格式的系統定義屬性](-shell-systemdefinedpropertiesforfileformats.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[屬性系統](../properties/building-property-handlers.md)
</dt> <dt>

[系統屬性](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> <dt>

[Windows搜尋 SDK 範例](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
</dt> </dl>

 

 
