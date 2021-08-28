---
description: Microsoft 提供數個具有 Windows Search 的標準篩選。 用戶端會呼叫這些篩選器處理常式 (這些是 IFilter 介面的執行，) 從檔中解壓縮文字和屬性。
ms.assetid: e19ae220-5c59-482e-8b02-00889600c4d6
title: Windows 隨附的篩選處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1a245978482e0334d91e35031aa80186fd2cb32
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624364"
---
# <a name="filter-handlers-that-ship-with-windows"></a>Windows 隨附的篩選處理常式

Microsoft 提供數個具有 Windows Search 的標準篩選。 用戶端會呼叫這些篩選器處理常式 (這些是 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的執行，) 從檔中解壓縮文字和屬性。

本主題的組織方式如下：

- [Windows搜尋執行注意事項](#windows-search-implementation-notes)
  - [Windows 7 和10實行](#windows-7-and-10-implementation)
  - [WindowsVista 的執行](#windows-vista-implementation)
  - [舊版的執行](#legacy-implementation)
- [Windows搜尋篩選](#filter-handlers-that-ship-with-windows)
  - [MIME 篩選處理常式](#mime-filter-handler)
  - [HTML 篩選處理常式](#html-filter-handler)
  - [檔篩選器處理常式](#document-filter-handler)
  - [純文字篩選處理常式](#plain-text-filter-handler)
  - [Binary 或 Null 篩選處理常式](#binary-or-null-filter-handler)
- [其他資源](#additional-resources)
- [相關主題](#related-topics)

## <a name="windows-search-implementation-notes"></a>Windows搜尋執行注意事項

在 Windows 7 和更新版本中，會明確封鎖以 managed 程式碼撰寫的篩選準則。 篩選準則必須以機器碼撰寫，因為有多個增益集在中執行的進程可能發生 CLR 版本控制問題。

### <a name="windows-7-and-10-implementation"></a>Windows 7 和10實行

在 Windows 7 和更新版本中，註冊篩選處理常式、屬性處理常式或新的延伸模組時，會發生新的行為。 當安裝新的屬性處理常式和（或）篩選器處理常式時，會自動重新編制具有對應副檔名的檔案的索引。

在 Windows 7 和更新版本中，我們建議您將篩選器處理常式與對應的屬性處理常式一起安裝，並在屬性處理常式之前註冊篩選處理常式。 註冊屬性處理常式時，會立即開始重新編制先前索引檔案的索引，而不需要重新開機，而且會利用任何先前註冊的篩選處理常式來進行內容編制索引。

如果未在沒有對應的屬性處理常式的情況下安裝篩選處理常式，則會在重新開機索引服務或重新開機系統之後，自動重新建立索引。

如 Windows 7 特有的屬性描述旗標，請參閱下列參考主題： [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags)、 [PROPDESC \_ COLUMNINDEX \_ TYPE](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)和[PROPDESC \_ SEARCHINFO \_ flags](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)。

### <a name="windows-vista-implementation"></a>WindowsVista 的執行

在 Windows Vista 及更早版本中，除非獨立的軟體供應商 (ISV) 明確地呼叫相符 url 的重建或重新編制索引，否則安裝 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)或屬性處理常式並不會起始現有專案的重新編制索引。

繼承應用程式之間有兩個主要的差異，例如索引服務和較新的應用程式，例如在執行篩選時應注意的 Windows Search：

- 使用 [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) 介面。
- 使用屬性處理常式。

首先，Windows Vista 和 Windows Search 3.0 和更新版本會要求您使用[IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) ，原因如下：

- 以確保效能和未來的相容性。
- 有助於提高安全性。 使用 [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) 來執行的篩選更為安全，因為篩選執行所在的內容不需要在磁片上或透過網路開啟檔案的許可權。

雖然 Windows Search 只使用[IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)，您也可以在篩選中包含[IPersistFile 介面](/windows/win32/api/objidl/nn-objidl-ipersistfile)和/或[IPersistStorage 介面](/windows/win32/api/objidl/nn-objidl-ipersiststorage)，以提供回溯相容性。

第二個主要差異是 Windows Vista 和 Windows Search 3.0 和更新版本都有新的[屬性系統](../properties/building-property-handlers.md)，使用屬性處理常式來列舉專案的屬性。

不過，有時候您需要執行可處理內容和屬性的篩選準則，以便：

- 支援舊版 MSSearch 實作為。
- 跨越連結。
- 保留語言資訊。
- 以遞迴方式篩選內嵌的專案。

在這些情況下，您需要完整的篩選器執行，包括用來存取屬性值的 [**IFilter：： GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) 方法。

### <a name="legacy-implementation"></a>舊版的執行

如先前所述，Windows Vista 和 Windows Search 包含一個新的屬性系統，其會封裝與專案內容不同的專案屬性。 舊版的 Microsoft Windows Desktop Search (WDS) 2.x 中不存在此屬性系統。 如果您的篩選準則必須支援其他應用程式（如上所述），則可能需要處理內容和屬性。

如需有關開發相容的篩選器的詳細資訊，請參閱下列主題、 [適用于繼承應用程式的 IFilter () ](/windows/win32/api/filter/nn-filter-ifilter)，以及 [針對繼承應用程式) 開發篩選增益集 (](../lwef/-search-2x-wds-ifilteraddins.md)。

## <a name="windows-search-filters"></a>Windows搜尋篩選

Microsoft 提供數個具有 Windows Search 的標準篩選。 下表摘要說明 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  DLL 內容。 按一下篩選器處理常式的名稱，會帶您前往該 **IFilter** 執行的描述。

| 篩選處理常式                                                  | 篩選的檔案                              | IFilter DLL  |
|-----------------------------------------------------------------|---------------------------------------------|--------------|
| [MIME 篩選處理常式](#mime-filter-handler)                     | 多用途網際網路郵件延伸 (MIME)  | mimefilt.dll |
| [HTML 篩選處理常式](#html-filter-handler)                     | HTML 3.0 或更早版本                         | nlhtml.dll   |
| [檔篩選器處理常式](#document-filter-handler)             | Microsoft Word、Excel、PowerPoint           | offfilt.dll  |
| [純文字篩選處理常式](#plain-text-filter-handler)         | 純文字檔-預設 IFilter          | query.dll    |
| [Binary 或 Null 篩選處理常式](#binary-or-null-filter-handler) | 二進位檔案-Null IFilter                 | query.dll    |

### <a name="mime-filter-handler"></a>MIME 篩選處理常式

mimefilt.dll 中的 MIME 篩選處理常式 () 會從副檔名為 .eml、.mht 和 mhtml 的檔案中解壓縮文字和屬性資訊。

### <a name="html-filter-handler"></a>HTML 篩選處理常式

) nlhtml.dll 中的 HTML 篩選處理常式 (會從 "htmlfiles" 類別中解壓縮文字和屬性資訊，以便 Windows Search 進行編制索引。 如需 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 與檔案類型之間關聯的描述，請參閱 [註冊篩選處理常式](-search-ifilter-registering-filters.md)中的「尋找檔案的 IFilter DLL」。

您可以使用 `META` html 檔的標記功能，將特殊處理要求傳送至 Html [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)。 `META` 標記會出現在標記內 html 檔案的開頭附近 `HEAD ... /HEAD` ，如下列範例所示。

```XML
   <head>
     <META NAME="DESCRIPTION"
           CONTENT="This text appears on the results page as the document's summary.">
   </head>
```

某些 HTML `META` 標記會自動對應到知名的屬性集和屬性識別碼 (屬性識別碼 (PID) ) 值，以便這些屬性的查詢將會搜尋對應的內容。 下表列出一些範例。 如需可用於檔案格式的系統屬性清單，請參閱 [自訂檔案格式的系統定義屬性](-shell-systemdefinedpropertiesforfileformats.md)。

| 屬性範例                              | 對應至                                                               |
|-----------------------------------------------|-------------------------------------------------------------------------|
| meta name = "author" content = "ruth"             | 摘要資訊屬性集中的 author 屬性。            |
| meta name = "subject" content = "word 處理" | 摘要資訊屬性集中的 subject 屬性。           |
| meta name = "關鍵字" content = "字型，serif"   | 摘要資訊屬性集中的關鍵字屬性。           |
| meta name = "ms. category" content = "小說"     | 檔摘要資訊屬性集中的 category 屬性。 |

下表列出 HTML [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 的部分功能。

[comment]: # (這個資料表必須是 HTML，才能正確地將範例格式化)

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>工作</th>
<th>動作</th>
<th>範例</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>從檔案建立特殊的摘要</td>
<td>您 <code>META NAME=&quot;DESCRIPTION&quot;...</code> 可以使用標記來指示 <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> 在檔摘要中使用後面接著關鍵字的字串 <code>CONTENT</code> 。
<blockquote>
[!Note]<br />
篩選程式可以針對每個篩選過的檔案產生摘要，這會預設為檔開頭的一組字元。
</blockquote>
<br/></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;head&gt;
  &lt;META NAME=&quot;DESCRIPTION&quot; CONTENT=&quot;This text will appear on the results page as the document&#39;s summary.&quot;&gt;
&lt;/head&gt;
 </pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>防止篩選個別檔案</td>
<td>將 <code>meta name</code> 標記新增至檔案。</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
  &lt;meta name=&quot;robots&quot; content=&quot;noindex&quot;&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>設定檔案 (的語言代碼，以確保系統選擇正確的語言斷詞工具和非搜尋字檔案) </td>
<td>在檔案中新增下列 <code>meta name</code> 標記，其中 content 欄位會以字元或使用地區設定值) 來指定適當的語言代碼 (。</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;meta name=&quot;ms.locale&quot; content=&quot;EN&quot;&gt;
&lt;meta name=&quot;ms.locale&quot; content=1033&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

### <a name="document-filter-handler"></a>檔篩選器處理常式

檔篩選器處理常式 (在 offilt.dll) 會篩選 Microsoft Office 中某些檔副檔名的檔案。 例如，其中包含副檔名為 .doc、.mdb、.ppt 和 .xlt 的檔案。

### <a name="plain-text-filter-handler"></a>純文字篩選處理常式

若為純文字檔，Windows Search 會使用文字篩選處理常式，此處理程式會篩選系統屬性 (例如檔案名) 以及檔案的內容。 當檔案類型在登錄中沒有 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)關聯時，Windows Search 只會為檔案的 Shell 屬性編制索引。 不過，使用者可以使用 [**編制索引選項**] 控制台中的 [ **Advanced] 選項** 來 **編制屬性的索引**，或 **索引屬性和檔案內容**。

![顯示 [advanced options （選項）] 對話方塊的螢幕擷取畫面](images/ifilteradvancedoptions.png)

如果使用者為沒有相關聯的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)的檔案類型選擇此選項，則會使用文字篩選處理常式來解壓縮檔案的內容。 文字篩選處理常式不會「瞭解」任何檔案格式;篩選檔案的內容時，會將檔案視為字元序列。 它會檢查檔開頭的 Unicode 位元組順序標記。

### <a name="binary-or-null-filter-handler"></a>Binary 或 Null 篩選處理常式

當遇到已註冊的二進位檔案時，會使用 null 篩選處理常式。 Null 篩選處理常式只會捕獲系統屬性。 二進位檔案的內容不會進行篩選。 系統屬性的範例包括 **檔案名**、 **LastWriteTime**、 **FileSize** 和 **屬性**。

## <a name="additional-resources"></a>其他資源

- [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)上提供的 [IFilterSample](-search-sample-ifiltersample.md)程式碼範例，示範如何建立用來執行 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter)介面的 ifilter 基礎類別。
- 如需索引編制程式的總覽，請參閱 [索引](-search-indexing-process-overview.md)程式。
- 如需檔案類型的總覽，請參閱 [檔案類型](../shell/fa-file-types.md)。
- 若要查詢檔案類型的檔案關聯屬性，請參閱 [PerceivedTypes、SystemFileAssociations 和應用程式註冊](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))。

## <a name="related-topics"></a>相關主題

[開發篩選處理常式](-search-ifilter-conceptual.md)

[關於 Windows Search 中的篩選處理常式](-search-ifilter-about.md)

[在 Windows Search 中建立篩選處理常式的最佳作法](-search-3x-wds-extidx-filters.md)

[從篩選處理常式傳回屬性](-search-ifilter-property-filtering.md)

[在 Windows Search 中執行篩選處理常式](-search-ifilter-constructing-filters.md)

[註冊篩選處理常式](-search-ifilter-registering-filters.md)

[測試篩選處理常式](-search-ifilter-testing-filters.md)
