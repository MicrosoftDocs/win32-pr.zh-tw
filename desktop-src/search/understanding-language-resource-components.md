---
description: 語言資源是由斷詞工具和字幹分析器所組成，可將索引建立和查詢功能延伸至新的語言和地區設定。
ms.assetid: 7963805e-e279-42cf-ba95-f81a7de8e68e
title: 瞭解語言資源元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e03c9294eaf6e50de024b866372093a0359fc79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511076"
---
# <a name="understanding-language-resource-components"></a>瞭解語言資源元件

語言資源是由斷詞工具和字幹分析器所組成，可將索引建立和查詢功能延伸至新的語言和地區設定。 建立和查詢索引期間都會使用斷詞工具。 字幹分析器僅用於查詢。 Windows Search 使用語言資源 Dll 來系結至特定語言地區設定的 [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) 和 [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) 執行。

本主題的組織方式如下：

-   [關於語言資源](#about-language-resources)
-   [斷詞](#word-breaking)
-   [堵塞](#stemming)
-   [正規化](#normalization)
-   [非搜尋字](#noise-words)
-   [相關主題](#related-topics)

## <a name="about-language-resources"></a>關於語言資源

Windows Search 使用篩選 ([**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的執行) 和 [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) 以原生格式存取檔。 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)元件會從檔中解壓縮文字內容、屬性和格式。 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)會識別其正在篩選之檔的地區設定。 索引元件會針對該地區設定叫用適當的斷詞工具。 如果沒有可用的，則索引元件會叫用中性斷詞工具。 斷詞工具會從 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)接收，此為斷詞工具所剖析的 Unicode 字元輸入資料流程，以產生個別的單字和片語。 斷詞工具也會將日期和時間格式標準化。 索引子會將字組轉換成全部大寫字母，以正規化斷詞工具所產生的單字。 索引子會將大寫單字儲存至全文檢索索引，但針對該地區設定所識別的非搜尋字除外。

下表列出「圖1說明在建立索引時，Windows Search 語言資源的角色」一詞的動作和對應的結果。



| 動作                  | 產生的文字                                                                                                               |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------|
| 原始文字           | [圖 1] 說明在建立索引的過程中 Windows Search 語言資源的角色。                    |
| 篩選               | [圖 1] 說明在建立索引的過程中 Windows Search 語言資源的角色。                    |
| 斷詞           | 圖1、說明、role、of、language、resources、for、Windows、Search、期間、、索引、建立、進程、EOS |
| 正規化           | 圖1、說明、角色、、語言、資源、視窗、搜尋、期間、索引、建立、進程           |
| 移除非搜尋字      | 圖、說明、角色、語言、資源、WINDOWS、搜尋、期間、索引、建立、處理                            |
| 儲存至全文檢索索引 | 圖、說明、角色、語言、資源、WINDOWS、搜尋、期間、索引、建立、處理                            |



 

斷詞工具和字幹分析器是用來在查詢時展開 [FREETEXT](-search-sql-freetext.md) 查詢。 除非將語言代碼識別碼 (LCID) 作為查詢參數傳遞，否則查詢的地區設定為預設地區設定。 查詢元件會在查詢的 [WHERE](-search-sql-where.md) 子句中列出的查詢詞彙上叫用適當的斷詞工具。 例如，如果查詢的 WHERE 子句包含 "FREETEXT (蘋果、橘子和 pears) 」，則斷詞工具會收到文字" 蘋果，橘子，and pears "。 如果查詢 WHERE 子句使用 [CONTAINS](-search-sql-contains.md) 全文檢索述詞，則會正規化斷詞工具的文字輸出。 否則，查詢元件會將斷詞工具所識別的每個單字傳遞給該語言和地區設定的適當字幹分析器。 此字詞表會針對該單字產生替代或屈折變化表單的清單。 查詢元件會將展開的查詢詞彙清單標準化，並移除非搜尋字。

下表列出查詢 "蘋果，橘子，and pears" 的動作和對應的結果。



| 動作                       | 產生的文字                                            |
|------------------------------|-----------------------------------------------------------|
| 原始文字                | 蘋果、橘子和 pears                                |
| 斷詞                | 蘋果、橘子、and、pears、EOS                          |
| 詞幹分析                     | apple、蘋果、橙色、orangey、橘子、pears、梨 |
| 正規化                | APPLE、蘋果、橙色、ORANGEY、橘子、PEARS、梨 |
| 移除非搜尋字           | APPLE、蘋果、橙色、ORANGEY、橘子、梨、PEARS      |
| 展開的查詢詞彙清單 | APPLE、蘋果、橙色、ORANGEY、橘子、梨、PEARS      |



 

展開的查詢詞彙會提高查詢尋找符合原始查詢意圖之檔的可能性。 在查詢時，斷詞工具或字幹分析器所產生的文字不會儲存在磁片上。

## <a name="word-breaking"></a>斷詞

斷字是將文字分隔成個別的文字標記或單字。 許多語言（尤其是使用羅馬字母的語言）都有一個字組分隔符號的陣列 (例如，用來辨別單字、片語和句子的空白字元) 和標點符號。 斷詞工具必須依賴正確的語言啟發學習法，以提供可靠且精確的結果。 以字元為基礎的寫入或以腳本為基礎的字母來區分斷詞，其中個別字元的意義取決於內容。 如需可能影響斷詞工具執行的語言考慮詳細資訊，請參閱 [語言和 Unicode 考慮](linguistic-and-unicode-considerations.md)。

## <a name="stemming"></a>詞幹分析

Windows Search 在查詢時獨佔套用字幹分析器，以針對 [FREETEXT](-search-sql-freetext.md) 和屬性查詢中的字詞產生額外的單字形式。 字幹分析器執行形態分析並套用語法規則，以產生文字的替代清單或屈折變化形式。 替代形式通常具有相同的詞幹或基底形式。 藉由為單字產生屈折變化表單，編制索引服務會傳回與查詢相關的統計查詢結果。 例如，「泳道」的全文檢索查詢會比對包含「泳道、泳道、游泳、游泳」、游泳、swam、swum」或「符合」、「符合」、「符合」、「符合」、「符合」、「符合」、「符合」、「符合」和「符合」這些條款組合的檔。

某些語言需要在索引時間和查詢時間產生屈折變化詞彙，以進行標準和變數 inflections。 在此情況下，詞幹分析會發生在斷詞工具元件中，最短詞幹分析在實際的字幹分析器中可正常運作。 例如，日文斷詞工具會在建立索引和查詢期間執行詞幹分析，以便讓查詢尋找不同的屈折變化形式的搜尋字詞。

## <a name="normalization"></a>正規化

所有語言的檔都會儲存在單一索引中。 雖然單字和語言規則有很大的差異，但仍有一些考慮，例如數位、日期和時間，這些都是以一致的方式在所有斷詞工具中處理。 如需可能影響斷詞工具實作為正規化考慮的詳細資訊，請參閱 [曲面形式](surface-form-normalization.md)正規化。

## <a name="noise-words"></a>非搜尋字

非搜尋字（也稱為「停用字詞」）是指不是內容明顯指標的單字。 「索引服務」會從查詢詞彙以及全文檢索索引所包含的內容中移除非搜尋字。 *位移* 是檔或查詢詞彙清單中的文字出現次數。 檔或查詢中的非搜尋字組位移會記錄為空白。 移除非搜尋字可避免不必要的索引成長，藉以改善查詢效能。 它也可以改善查詢結果的相關性。 您可以將 Windows Search 設定為使用特定語言的非搜尋字清單。 當針對該語言叫用斷詞工具時，會使用這些清單。 例如，英文語言中的 "" "（英文）通常會有很少的值做為唯一索引鍵。 "In in in 非搜尋字清單，不會寫入內容索引，如果查詢，則不會傳回任何結果。

非搜尋字作為片語查詢中的預留位置。 包含 "wag" 狗 "文字的檔會儲存在索引中，" wag "在第1次和" dog "的索引中。 片語查詢 "wag dog" 不相符，但片語查詢 "wag" dog "，因為出現的資訊相符。 「Wag 紫色狗」片語不相符，因為在出現2的索引中找不到 "紫色"。 但是，「wag 狗」的查詢會傳回包含 "wag 紫色狗" 的檔，因為沒有辦法有效率地判斷檔是否在 "wag" 和 "dog" 之間有非干擾字。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[擴充語言資源](extending-language-resources-in-windows-search.md)
</dt> <dt>

[執行斷詞工具和字幹分析器](implementing-a-word-breaker-and-stemmer.md)
</dt> <dt>

[語言和 Unicode 考慮](linguistic-and-unicode-considerations.md)
</dt> <dt>

[疑難排解語言資源和最佳作法](troubleshooting-language-resources.md)
</dt> </dl>

 

 
