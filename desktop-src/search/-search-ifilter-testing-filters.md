---
description: IFilter 測試套件會驗證您的篩選處理常式。
ms.assetid: 5ee02af1-1dc9-4d21-868f-4c439970b1ba
title: 測試篩選處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf58f14f0f8de4458dd887bf52b32fb68f869d64
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122621944"
---
# <a name="testing-filter-handlers"></a>測試篩選處理常式

[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)測試套件會驗證您的篩選處理常式。 測試套件會透過下列方式來執行：呼叫 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter) 方法，並檢查傳回的值是否符合 **IFilter** 介面規格的規範;而且，檢查區塊識別碼是唯一且不斷增加的， **ifilter** 介面會在重新初始化之後一致地運作，而且具有無效參數的任何 **IFilter** 方法呼叫都會傳回預期的錯誤碼。 測試套件程式也會傾印篩選處理常式所篩選之檔案的輸出，並檢查登錄中的 **IFilter** 註冊資訊。

本主題的組織方式如下：

- [命令列調用](#command-line-invocation)
  - [ifilttst.exe](#ifilttstexe)
  - [filtdump.exe](#filtdumpexe)
  - [filtreg.exe](#filtregexe)
  - [ifilttst.ini](#ifilttstini)
- [IFilter 測試程式](#ifilter-test-procedure)
  - [驗證測試](#validation-test)
  - [一致性測試](#consistency-test)
  - [不正確輸入測試](#invalid-input-test)
  - [測試不同的 IFilter 設定](#testing-different-ifilter-configurations)
- [確定已註冊的專案已編制索引](#ensuring-registered-items-get-indexed)
  - [範例記錄檔](#sample-log-file)
  - [範例傾印檔案](#sample-dump-file)
- [其他資源](#additional-resources)
- [相關主題](#related-topics)

> [!NOTE]  
> 如果將檔案類型的新篩選處理常式安裝為現有篩選註冊的取代，則安裝程式應儲存目前的註冊，並在新的篩選器處理常式卸載時還原。 沒有任何機制可連結篩選。 因此，新的篩選處理常式會負責複寫舊篩選器的任何必要功能。

## <a name="command-line-invocation"></a>Command-Line 調用

[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)測試套件包含三個命令列應用程式- [ifilttst.exe](#ifilttstexe)、 [filtdump.exe](#filtdumpexe)和 [filtreg.exe](#filtregexe) ，以及 [ifilttst.ini](#ifilttstini)的初始化檔。

> [!IMPORTANT]
> 在 Windows 7 和更新版本中，會明確封鎖以 managed 程式碼撰寫的篩選準則。 您必須以機器碼撰寫篩選器，因為可能的 common language runtime (CLR) 在中執行多個增益集的進程的版本控制問題。

### <a name="ifilttstexe"></a>ifilttst.exe

ifilttst.exe 程式會執行數個測試，以驗證篩選處理常式。 下列範例說明如何從命令列叫用 ifilttst.exe 程式：


```
ifilttst /i test.htm /l /d /v 1
```

此範例會執行下列工作：

- 指示程式篩選檔案 test.htm
- 將記錄檔訊息重新導向至 test.htm .log。
- 將傾印訊息重新導向至 test.htm dmp
- 將詳細資訊設定為1

若要讓上述命令能夠運作，您必須在目前的工作目錄中找到三個檔案： `test.htm` 、 [ifilttst.exe](#ifilttstexe)和 [ifilttst.ini](#ifilttstini)。 命令列參數列于下表中。

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>切換和可能的變數</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>/i 檔案名</strong></td>
<td>要篩選的輸入檔或目錄。 檔案名可以包含萬用字元 <code>*</code> 和 <code>?</code> 。</td>
</tr>
<tr class="even">
<td><strong>/l</strong></td>
<td>記錄訊息會被導向至檔案，而不是畫面。 記錄訊息會描述所執行的個別測試，以及測試的通過/失敗結果。 記錄檔名稱與輸入檔案名相同，但副檔名為 .log。</td>
</tr>
<tr class="odd">
<td><strong>/d</strong></td>
<td>傾印訊息會被導向至檔案，而不是畫面。 傾印訊息會描述區塊的內容。 當詳細程度層級為3時，會傾印區塊結構。 傾印檔案名與輸入檔名稱相同，但副檔名為 dmp。</td>
</tr>
<tr class="even">
<td><strong>/-l</strong></td>
<td>停用記錄。 此旗標會覆寫 <code>/l</code> 參數。</td>
</tr>
<tr class="odd">
<td><strong>/-d</strong></td>
<td>停用傾印。 此旗標會覆寫 <code>/d</code> 參數。</td>
</tr>
<tr class="even">
<td><strong>/v 整數</strong></td>
<td>詳細等級。 預設值為 3。
<ul>
<li>0-測試只會記錄有關特定 <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> 介面失敗的訊息。 測試會傾印區塊內容。</li>
<li>1-測試會記錄警告訊息以及層級0的訊息。</li>
<li>2-測試會記錄有關傳遞的測試和層級1的訊息。</li>
<li>3-測試會記錄參考用訊息以及層級2的訊息。 此外，測試會傾印區塊的結構。</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>/t 整數</strong></td>
<td>要啟動的執行緒數目。 預設值是 1。</td>
</tr>
<tr class="even">
<td><strong>/r 整數</strong>]</td>
<td>以遞迴方式篩選子目錄。 選擇性的整數參數會指定要對其執行遞迴的深度。 如果未指定整數，或整數為0，則會假設為完整遞迴。 根據預設，遞迴深度為1。</td>
</tr>
<tr class="odd">
<td><strong>/c 整數</strong></td>
<td>要迴圈的次數。 如果整數是0，則測試會無限迴圈。 根據預設，測試只會迴圈一次。</td>
</tr>
</tbody>
</table>

> [!NOTE]  
> 您必須在命令列參數與值之間加上空格。

### <a name="filtdumpexe"></a>filtdump.exe

filtdump.exe 程式會載入指定檔的篩選處理常式，並列印 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL 所產生的輸出。 下列範例說明如何叫用 filtdump.exe 程式。

```
filtdump filename.ext
```
Filtdump.exe 使用 [ILoadFilter：： LoadIFilter](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) 方法載入適用于指定副檔名的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL，並列印結果。 例如，下列命令會指示 filtdump.exe 載入擴充功能的 smpfilt.dll 篩選處理常式、從 myfile.txt 檔案中解壓縮所有文字和屬性，然後列印結果。

```
filtdump myfile.smp
```

### <a name="filtregexe"></a>filtreg.exe

filtreg.exe 程式會檢查登錄中的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 安裝資訊。 您可以藉由輸入命令列的名稱，從命令列叫用 filtreg.exe 程式，如下列範例所示。

```
filtreg
```

Filtreg.exe 會針對延伸模組列印副檔名和 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL 的名稱，以列舉所有具有相關聯篩選器處理常式的副檔名。 這是驗證 **IFilter** 正確安裝的簡單方式。

### <a name="ifilttstini"></a>ifilttst.ini

藉由呼叫 [**ifilter：： Init**](/windows/win32/api/filter/nf-filter-ifilter-init)方法來初始化 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter)介面。 **IFilter：： Init** 方法會採用下列四個參數：

1. *grfFlags*
2. *cAttributes*
3. *aAttributes*
4. *pdwFlags*

[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)測試套件 ifilttst.exe 程式的使用者可以在稱為 ifilttst.ini 的檔案中指定這些參數的值。 下表描述 ifilttst.ini 檔案中的專案，以指定) 輸入參數 (前三個參數。 如需範例檔案，請參閱 [範例 ifilttst.ini](#sample-ifilttstini-file)檔。

> [!NOTE]  
> *PdwFlags* 參數沒有資料表專案，因為它是輸出參數。在呼叫 [**IFilter：： Init**](/windows/win32/api/filter/nf-filter-ifilter-init)方法之前，不需要有任何特殊值。

 | 進入         | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Flags         | 要由 OR 運算子聯結的 [**ifilter \_ INIT**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85))旗標名稱，以形成 [**ifilter：： INIT**](/windows/win32/api/filter/nf-filter-ifilter-init)方法的 *grfFlags* 參數。 旗標名稱必須全部都是大寫，並且在同一行上。                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *cAttributes* | 表示 *cAttributes* 參數值的十進位整數。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| *aAttributes* | 這個專案必須以 *aAttributes* 開頭，且必須與區段內的其他 *aAttributes* 專案不同。 *AAttributes* 專案的法定名稱如下： *aAttributes*、 *aAttributes1*、 *aAttributes2* 等等。 第一個 token 必須是 GUID。 GUID 的格式必須完全如同 `[Test3]` [範例 ifilttst.ini](#sample-ifilttstini-file)檔案一節中所述。 第二個權杖可以是屬性識別碼 (PID) 由十六進位標記法中的數位組成，或 (lpwstr) 的寬字元字串指標。 您可以用雙引號括住字串來指定 lpwstr，如範例 ifilttst.ini 檔中的 `[Test6]` 一節所示。 |

如果未指定 Flags 和 *cAttributes* 專案，則會預設為0。 如果您將 *cAttributes* 設定為等於2，您應該指定兩個 *aAttributes* 名稱。 在 `[Test5]` 範例的區段中， *cAttributes* 為1，但未指定 *aAttributes* 。 然後，測試會呼叫 *cAttributes* 等於1且 *aAttributes* 等於 **Null** 的 [**IFilter：： Init**](/windows/win32/api/filter/nf-filter-ifilter-init)方法。 這是很有用的測試案例，因為它可能會導致 **IFilter：： Init** 方法發生存取違規。

如果 ifilttst.exe 在工作目錄中找不到名為 ifilttst.ini 的檔案，則會使用預設設定來初始化 [**IFilter：： Init**](/windows/win32/api/filter/nf-filter-ifilter-init) 物件。 下列範例說明預設設定。

```
[default]
            grfFlags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

```

### <a name="sample-ifilttstini-file"></a>範例 ifilttst.ini 檔案

ifilttst.ini 檔會組織成區段，並以方括弧括住區段名稱。 在此範例中，區段的名稱為 `[Test1]` 、等等 `[Test2]` 。 所有區段名稱都必須是唯一的。 測試會從第一個區段讀取值，並使用這些值來初始化 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 。 然後使用此 **IFilter** 設定來執行所有測試。 然後使用上述的參數釋出並重新初始化 **IFilter** 。 此程式會重複，直到所有設定都經過測試為止。

```
; Only extract text from the object
            [Test1]
            Flags =
            cAttributes = 0

            // Get all attributes (text-type and internal value-type properties.
            [Test2]
            Flags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

            // This also extracts just text from the object (the GUID is PSGUID_STORAGE, and the propid is
            // PID_STG_CONTENTS).
            [Test3]
            Flags = IFILTER_INIT_CANON_PARAGRAPHS IFILTER_INIT_HARD_LINE_BREAKS
            cAttributes = 1
            aAttributes1 = b725f130-47ef-101a-a5f1-02608c9eebac 13

            // Only extract requested attribute from the html object (the GUID corresponds to the HTML IFilter.
            [Test4]
            Flags = IFILTER_INIT_CANON_HYPHENS IFILTER_INIT_CANON_SPACES
            cAttributes = 1
            aAttributes1 = 70eb7a10-55d9-11cf-b75b-00aa0051fe20 2

            // Question: what happens if cAttributes is nonzero, but aAttributes is empty?
            [Test5]
            Flags = IFILTER_INIT_CANON_SPACES IFILTER_INIT_APPLY_INDEX_ATTRIBUTES IFILTER_INIT_APPLY_OTHER_ATTRIBUTES
            cAttributes = 1

            // Here is an attribute with a lpwstr instead of a propid (the lpwstr is enclosed in quotes).
            // The GUID corresponds to the meta tag clsid for the HTML IFilter.
            [Test6]
            Flags =
            cAttributes = 1
            aAttributes1 = D1B5D3F0-C0B3-11CF-9A92-00A0C908DBF1 "GENERATOR"
```

## <a name="ifilter-test-procedure"></a>IFilter 測試程式

在將 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter) 初始化之後，ifilttst.exe 程式會在 **ifilter** 上進行一系列的測試。 除了將 **ifilter** 測試程式進行之後，請確定您的 **IFilter** 實行採用安全的程式碼作法。 請參閱[Windows Search 中執行篩選處理常式](-search-ifilter-constructing-filters.md)的「Windows Search 的安全程式碼實務」。

### <a name="validation-test"></a>驗證測試

驗證測試會以一次一個區塊的物件為單位來檢查每個個別區塊和所有傳回碼。 驗證測試會將所有傳回的 [**STAT \_ 區塊**](/windows/win32/api/filter/ns-filter-stat_chunk) 結構儲存在清單中。

驗證測試會驗證下列條件：

- [**STAT \_ 區塊**](/windows/win32/api/filter/ns-filter-stat_chunk)。*idChunk* 區塊識別碼必須是唯一的，而且必須是遞增的。
- [**STAT \_ 區塊**](/windows/win32/api/filter/ns-filter-stat_chunk)。*旗標* 參數是可辨識的區塊狀態，例如 [**CHUNKSTATE**](/windows/win32/api/filter/ne-filter-chunkstate)、區塊 \_ 文字或 CenabledHUNK \_ 值常數。
- [**STAT \_ 區塊**](/windows/win32/api/filter/ns-filter-stat_chunk)。*breakType* 參數是可辨識的分隔類型 (0、1、2、3、4) 。
- 如果 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter) 初始化屬性指定 **ifilter** 只傳回包含內部數值型別屬性的區塊，則 *idChunkSource* 必須等於0。
- 如果區塊不是衍生的，則為，如果它不是內部數值型別的屬性，則為 [**STAT \_ 區塊**](/windows/win32/api/filter/ns-filter-stat_chunk)。*idChunkSource* 必須等於 **STAT \_ 區塊**。*idChunk*。
- [**IFilter：： GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) 會傳回 \_ [確定] 或其他可接受的傳回值，例如 [篩選 \_ e \_ 區塊結尾] \_ 、[ \_ 篩選 \_ e \_ 連結 \_ 無法使用] 等等。
- 如果區塊包含文字，則 [**IFilter：： GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) 會傳回 S \_ OK、 \_ FILTER \_ LAST \_ text 或 filter \_ E \_ NO \_ \_ text。
- 如果 [**ifilter：： GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) 傳回篩選 \_ 條件 \_ 的最後一個 \_ 文字，則下次對 **IFilter：： GetText** 的呼叫會傳回篩選 E，而不會傳回 \_ \_ 任何 \_ \_ 文字。
- 如果區塊包含值， [**IFilter：： GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) 會傳回 S \_ OK 或 FILTER \_ E \_ NO \_ \_ VALUES。

### <a name="consistency-test"></a>一致性測試

ifilttxt.exe 程式會使用與驗證測試中相同的參數來重新初始化 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面，並執行一致性測試。 如果 **ifilter** 實作為以 [**ifilter \_ 初始**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85))ifilter \_ 初始 \_ 編制索引旗標初始化 \_ ，則測試會在對 [**ifilter：： INIT**](/windows/win32/api/filter/nf-filter-ifilter-init)方法進行另一次呼叫之前，先釋出 **ifilter** 介面並重新系結。

一致性測試會驗證下列條件：

- [**IFilter：： GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk)方法所傳回的每個 [**stat \_ 區塊**](/windows/win32/api/filter/ns-filter-stat_chunk)結構，與驗證測試中所傳回的對應 **STAT \_ 區塊** 相同。
- [**IFilter：： GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) 會傳回 \_ [確定] 或其他可接受的傳回值，例如 [篩選 \_ e \_ 區塊結尾] \_ 、[ \_ 篩選 \_ e \_ 連結 \_ 無法使用] 等等。

### <a name="invalid-input-test"></a>不正確輸入測試

ifilttst.exe 程式會使用相同的參數重新初始化 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面，並執行不正確輸入測試。 這項測試會逐步解說檔的一個區塊，讓函式呼叫不正確，例如，當目前的 chuck 包含文字時呼叫 [**IFilter：： GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) 方法。 此測試會檢查所有傳回碼是否符合 **IFilter** 規格。

不正確輸入測試會驗證下列條件：

- 如果目前的區塊包含文字， [**ifilter：： GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) 會傳回篩選 \_ E \_ 沒有 \_ 值，且對 [**IFilter：： GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) 的呼叫會成功。
- 如果目前的區塊包含值， [**ifilter：： GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) 會傳回 FILTER \_ E \_ NO \_ TEXT，且對 [**IFilter：： GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) 的呼叫會成功。
- 如果先前對 [**ifilter：： GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) 的呼叫傳回篩選 \_ E，則不會再傳回 \_ 任何 \_ \_ 文字，而對 **ifilter：： GetText** 的後續呼叫會傳回篩選 \_ e \_ \_ \_ 。
- 如果之前對 [**ifilter：： getvalue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) 的呼叫傳回篩選器 \_ e \_ 沒有 \_ 其他 \_ 值，則對 **ifilter：： getvalue** 的連續呼叫會傳回篩選 \_ e \_ 沒有 \_ 其他 \_ 值。
- 如果之前對 [**ifilter：： GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) 的呼叫傳回篩選 \_ E \_ \_ 區塊結尾 \_ ，則連續呼叫 **ifilter：： GetChunk** 會傳回濾波器 \_ e \_ \_ 區塊結尾 \_ 。

> [!NOTE]  
> 不正確輸入測試會比較目前的區塊結構與驗證測試中傳回的結構，以確保它們完全相同。

### <a name="testing-different-ifilter-configurations"></a>測試不同的 IFilter 設定

ifilttst.exe 程式會釋出 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面並重新系結，這次使用下一組參數將它初始化。 測試會重複執行迴圈：驗證測試、一致性測試和不正確輸入測試，直到 [ifilttst.ini](#ifilttstini)檔案中指定的所有所需的 **IFilter** 設定都經過測試為止。

## <a name="ensuring-registered-items-get-indexed"></a>確定已註冊的專案已編制索引

您的 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter) 最終測試可確保您的 **ifilter** 已正確註冊，而且會叫用它來為您註冊用它的專案編制索引。 您可以使用目錄管理員來起始重新建立索引，或使用編目範圍管理員 (CSM) 來設定預設規則，指出您想要讓索引子編目的 Url。 完成索引之後，請使用 Windows Search UI 來搜尋專案內容或屬性中的字串。 如果專案已編制索引，這些專案會出現在搜尋結果中。

如需重新編制索引的詳細資訊，請參閱 [使用目錄管理員](-search-3x-wds-mngidx-catalog-manager.md) 和 [使用編目範圍管理員](-search-3x-wds-extidx-csm.md)。 ReindexMatchingUrls 程式碼範例會示範如何指定要重新建立索引的檔案和方法。 CrawlScopeCommandLine 程式碼範例會示範如何定義編目範圍管理員 (CSM) 索引編制作業的命令列選項。 這兩個程式碼範例都可在[GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)上取得。

### <a name="sample-log-file"></a>範例記錄檔

在要求時，Ifilttst.exe 程式可以產生記錄，其中包含執行期間所需步驟的描述。 下列範例是記錄檔中的摘錄，其詳細資訊設定為最高的可能值3。

```
            1. INFO----**** New configuration ****
            2.
            3. Section name : Test2
            4. grfFlags     : 63
            5. cAttributes  : 0
            6. aAttributes  : NONE
            7. pdwFlags     : 0
            8.
            9. INFO----Successfully bound filter.
            10.
            11. PASS----Init() returned a valid value for pdwFlags.
            12.
            13. INFO----Successfully initialized filter.
            14.
            15. INFO----Performing validation test. In this part of the test, the chunks structures
            16.         returned by the IFilter are checked for correctness, and the return values
            17.         of the IFilter calls are checked.
            18.
            19. PASS----GetChunk() succeeded.
            20.
            21. PASS----The current chunk has a legal value for the flags field.

```

第一行是告知性訊息，表示已從 ifilttst.ini 檔案載入新的設定。 第 (3 行) 表示已讀取目前設定之 ifilttst.ini 檔案中的區段名稱。 行 (4) 到 (7) 列出 [**IFilter：： Init**](/windows/win32/api/filter/nf-filter-ifilter-init)的參數。 開頭的行 `INFO` 是關於 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 系結和驗證測試開頭的參考訊息。 開頭的行 `PASS` 是關於已通過之特定測試的訊息。

下列記錄範例中的程式程式碼為警告。 警告會注意到有問題的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 行為（雖然合法）。 此警告表示 [**IFilter：： GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) 方法傳回的文字區塊不包含任何文字。

```
WARNING-First call to GetText() returned FILTER_E_NO_MORE_TEXT.
```

下列範例錯誤訊息表示 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 發出未要求的區塊。

```
            ERROR---The IFilter has emitted a chunk which it was not requested to emit.
            Check the initialization parameters in section Test1 of the initialization file.
            INFO----Current chunk propid : 0x5
```

在此範例錯誤訊息的情況下， [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 發出了具有 PID 的區塊 `0x5` 。 檢查 `[Test1]` ifilttst.ini 中的區段會顯示已將 **IFilter** 設定為不使用此 PID 發出區塊。 例如，如果 IFILTER init 套用 \_ \_ \_ 索引屬性， \_ 或 Ifilter init 套用了 \_ \_ \_ \_ Flags 專案中指定的其他屬性，而如果 *CATTRIBUTES* 為0，則 **ifilter** 只會發出 pid 為的區塊， `0x13` 並對應至 pid \_ stg. \_ 內容。

### <a name="sample-dump-file"></a>範例傾印檔案

在要求時，Ifilttst.exe 程式可能會產生一個傾印，其中包含所找到的區塊及其內容。 下列範例是這類傾印檔案的摘錄。

```
                1. Chunk ID: ........... 2
                2. Chunk Break Type: ... END OF SENTENCE
                3. Chunk State: ........ TEXT
                4. Chunk Locale: ....... 0x411
                5. Chunk Source ID: .... 2
                6. Chunk Start Source .. 0x0
                7. Chunk Length Source . 0x0
                8. GUID ................ b725f130-47ef-101a-a5f1-02608c9eebac
                9. Property ID ......... 0x13

                10. This is a HTML IFilter test page

                11. Chunk ID: ........... 3
                12. Chunk Break Type: ... END OF SENTENCE
                13. Chunk State: ........ TEXT
                14. Chunk Locale: ....... 0x411
                15. Chunk Source ID: .... 2
                16. Chunk Start Source .. 0x0
                17. Chunk Length Source . 0x0
                18. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                19. Property ID ......... 0x2

                20. This is a HTML IFilter test page

                21. Chunk ID: ........... 4
                22. Chunk Break Type: ... END OF SENTENCE
                23. Chunk State: ........ VALUE
                24. Chunk Locale: ....... 0x411
                25. Chunk Source ID: .... 2
                26. Chunk Start Source .. 0x0
                27. Chunk Length Source . 0x0
                28. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                29. Property ID ......... 0x2

                30. This is an HTML IFilter test page
```

前九行描述目前的區塊結構。 GUID 和 PID 對應于 PSGUID \_ STORAGE/PID \_ stg. \_ 內容。 這是包含純文字的區塊。 文字位於下列區塊結構中：

```
10. This is an HTML IFilter test page
```

下一個區塊（從第11行開始）有不同的 GUID，對應至與 `HTML IFilter` HTML HREF 對應的和不同的 PID。 這是由匯出的內部實值型別屬性 `HTML IFilter` 。

下一個區塊（從第21行開始）有相同的 GUID 和 PID，但是它的區塊狀態是 `VALUE` 而非 `TEXT` 。 請注意，最後兩個區塊中的文字與第一個區塊的文字相同。 但因為 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 是針對三個屬性所設計 (純文字、html href 做為文字，而 html href 作為值) 套用至這個片語，則會以三個不同的區塊來發出結果。

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

[Windows 隨附的篩選處理常式](-search-ifilter-implementations.md)

[在 Windows Search 中執行篩選處理常式](-search-ifilter-constructing-filters.md)

[註冊篩選處理常式](-search-ifilter-registering-filters.md)
