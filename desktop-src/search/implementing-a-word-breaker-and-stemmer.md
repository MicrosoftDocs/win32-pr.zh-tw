---
description: Microsoft 提供許多語言的斷詞工具和字幹分析器。 本主題說明如何針對語言使用自訂斷詞工具和字幹分析器，以及在 Microsoft 提供的地區設定以外的地區設定。
ms.assetid: 47768691-7071-440e-bfbf-975713880c00
title: 執行斷詞工具和字幹分析器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd4f4e3210e7f4e17bb035115fd694656cc6e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026114"
---
# <a name="implementing-a-word-breaker-and-stemmer"></a>執行斷詞工具和字幹分析器

Microsoft 提供許多語言的斷詞工具和字幹分析器。 本主題說明如何針對語言使用自訂斷詞工具和字幹分析器，以及在 Microsoft 提供的地區設定以外的地區設定。

> [!Note]
> 從2018年7月起，Windows Server 2019 的安全性變更，可防止 SearchIndexer.exe 載入沒有 Microsoft 簽章的 Dll。 因此，Windows Server 2019 不再支援非 Microsoft 簽署的自訂斷詞工具。 

本主題的組織方式如下：

-   [註冊語言資源 DLL](#registering-a-language-resource-dll)
-   [註冊語言](#registering-a-language-resource-dll)
-   [執行單字小燒杯](#implementing-a-word-beaker)
    -   [WordSink 和 PhraseSink](#wordsink-and-phrasesink)
    -   [分隔設定](#breaks)
    -   [擴充性、Performancy 和安全性](#scalability-performancy-and-security)
-   [執行字幹分析器](#implementing-a-stemmer)
    -   [擴充性、Performancy 和安全性](#scalability-performancy-and-security)
-   [相關主題](#related-topics)

## <a name="registering-a-language-resource-dll"></a>註冊語言資源 DLL

每個語言資源 DLL 都必須執行並匯出下列進入點。 DLL 可以註冊在任何資料夾中。

-   DllMain 是 DLL 的標準進入點。
-   DllRegisterServer 會在登錄中註冊 DLL，例如 `regsvr32.exe %SystemRoot%\MyFolder\wordbreaker.dll`
-   DllCanUnloadNow 可讓用戶端透過元件物件模型 (COM) 來呼叫這個進入點，以判斷是否可以卸載語言資源 DLL。
-   DllUnRegisterServer 會將 DLL 從登錄中移除。

## <a name="registering-a-language"></a>註冊語言

登錄包含要編制索引之語言的特定語言專案，而這些專案會控制特定語言之索引和查詢程式的元件。 您可以在下列登錄機碼下找到這些登錄專案。

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         ContentIndex
            Control
               Language
                  
```

## <a name="implementing-a-word-beaker"></a>執行單字小燒杯

斷詞工具會執行 [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker)。 [**IWordBreaker：： BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext)方法會執行所有文字處理和剖析。 若要執行斷詞工具元件，您必須具有語言的語言啟發學習法。 這包括語法和 morphology 的相關資訊。 您也可能需要排除或包含的字詞清單。 您可以從排除字組清單中，為您的語言地區設定建立非搜尋字的檔。 如需有關語言考慮以及這些考慮如何影響斷詞工具的詳細資訊，請參閱 [語言和 Unicode 考慮](linguistic-and-unicode-considerations.md)。

[**IWordBreaker：： BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext)的主要目的是要在所有文字都經過處理或斷詞工具遇到錯誤之前，從 [**文字 \_ 來源**](/windows/win32/api/indexsrv/ns-indexsrv-text_source)連續處理文字。 在此資料處理迴圈中， **IWordBreaker：： BreakText** 會呼叫執行該處理常式之特定工作的剖析和公用程式方法。 例如，德文斷詞工具可能會處理複合字，而法文斷詞工具可能會處理變 [音符](surface-form-normalization.md) 號或 [clitics](surface-form-normalization.md)。 斷詞工具所執行的特定函式，以及它用來執行這些工作的策略完全取決於該語言的需求。

當斷詞時，斷詞工具會針對可能具有多個表示的單字識別「替代」表單。 產生的單字之間不會隱含任何語義關聯性。 事實上，原始字組可能不會包含在替代專案清單中。 替代形式會儲存在索引中的相同位置，以做為原始單字，表示兩者相同。

當檔包含在索引中時，每個單字都會被指派一個整數值，代表位移，或從檔開頭開始的單字距離。 查詢中的單字之間的相對距離會與儲存在全文檢索索引中的位移進行比較。 「Kyle 的檔」查詢會比對任何包含 "Where" at offset n 的檔、"at" at n + 1、"Kyle's" at n + 2 和 "document" （n + 3）。 「Kyle 的檔記載于資料基底？」 表示為：



|       |     |                        |          |       |     |     |                               |
|-------|-----|------------------------|----------|-------|-----|-----|-------------------------------|
| Where | is  | Kyle Kyle<br/> | 文件 | 提交 | in  | the | 資料庫資料基底<br/> |



 

在此範例中，斷詞工具會在索引中儲存 "Kyle" ( "Kyle" ) 和 "database" ( "data base" ) 的替代形式。 在下列情況下，斷詞工具會在索引建立程式期間產生並儲存替代單字：

-   如果另一個字可能會在查詢中顯示為單一單字
-   如果字幹分析器不太可能從替代方式衍生原始單字

產生替代的單字表單會增加查詢表示及符合句子的方式數目，如下列變化所示：

1.  Kyle 檔在資料庫中的記錄位置
2.  Kyle 在資料庫中的檔歸檔位置
3.  其中是 Kyle 檔在資料基底中的欄位
4.  Kyle 在資料基底中的檔歸檔位置

### <a name="wordsink-and-phrasesink"></a>WordSink 和 PhraseSink

斷詞工具會使用 [**IWordSink**](iwordsink.md) 和 [**IPhraseSink**](/windows/win32/api/indexsrv/nn-indexsrv-iphrasesink) 物件來收集和儲存它們從文字中解壓縮的所有單字和片語。 斷詞工具會以盡可能接近檔中原始單字形式的形式來儲存文字。 **IPhraseSink** 會在查詢時儲存片語。 片語可改善查詢結果的相關性，因為較長的單字序列是罕見，並提供比較小片語更大的差異。 當索引子在查詢時將片語放在 **IPhraseSink** 中時，它會建立斷詞工具的實例，以將片語分成單字。 然後，索引子會藉由檢查片語中的單字是否出現在索引中彼此連續的方式來評估片語。 例如，如果 "ABCD" 出現在索引中的位置 *x*、 *x*+ 1、 *x*+ 2 和 *x*+ 3，則如果在查詢中提交 "abcd" 的任何相鄰子字串，就會發生片語相符的情況。 這項策略適用于以字元為基礎的斷詞工具，可在索引建立期間分割片語和長字組，並在查詢期間產生片語。

### <a name="breaks"></a>分隔設定

「中斷」是單字之間的空格。 空白字元、標點符號、格式化或只是語言本身的本質可能會導致中斷。 索引子會使用四種不同類型的中斷：字尾 (EOW) 、句子結尾 (EOS) 、段落結尾 (EOP) 和 (的第一章) 。 EOW 中斷是預設中斷。 在每個 token 之後，每個 break 都會指出任一邊單字之間的不同語義距離。 以 EOW 分隔的單字具有嚴謹語義連結，後面接著 EOS、EOP 和 EOC。 多個 [**IWordSink 呼叫：:P utbreak**](iwordsink-putbreak.md) 是累計的，而且類似于插入 null 單字或句子。

### <a name="scalability-performancy-and-security"></a>擴充性、Performancy 和安全性

斷詞工具回應同時呼叫的方式，主要取決於您選擇的執行緒模型。 索引子是單一執行緒應用程式。 若要讓斷詞工具在單一執行緒環境中運作，必須使用「免費」或「兩個」執行緒模型來撰寫斷詞工具。 斷詞工具不得使用「單元」執行緒模型向 COM 註冊。

我們建議斷詞工具避免全域狀態，並將資料儲存在該斷詞工具的實例中。 唯一應儲存在斷詞工具實作為參數 *fQuery* 和 *ulMaxTokenSize* 的內容。 斷詞工具的速度不應超過英文斷詞工具所建立的基準。 斷詞工具效能也應以增加的硬體功能來改善。

索引子在本機系統安全性內容中執行的斷詞工具。 它們應該寫入來管理緩衝區，並正確地堆疊。 所有字串複本都必須有明確的檢查，以防止緩衝區溢位。 您應該一律確認已配置的緩衝區大小，並根據緩衝區大小測試資料的大小。 斷詞工具無法假設傳遞給 [**IWordBreaker：： BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) 方法的文字格式正確。 如需疑難排解斷詞工具的詳細資訊，請參閱 [疑難排解語言資源和最佳作法](troubleshooting-language-resources.md)。

## <a name="implementing-a-stemmer"></a>執行字幹分析器

字幹分析器會執行 [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) 介面。 [**IStemmer：： GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms)方法會產生特定輸入字組的屈折變化字表單清單。 若要執行詞幹分析器元件，您必須具有語言的語言啟發學習法。 這包括 morphology 的相關資訊。 您也可能需要排除或包含的字詞清單。 如需有關語言考慮以及這些考慮如何影響字幹分析器的詳細資訊，請參閱 [語言和 Unicode 考慮](linguistic-and-unicode-considerations.md)。

我們建議字幹分析器不應為單字產生所有格（或所有格）案例。 例如，"David" 不會產生為 "David" 的替代形式。 斷詞工具在剖析「David」時，會產生「David」和「David」。

詞幹分析器會使用 [IWordFormSink](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) 物件來收集替代字的清單。 [**IWordFormSink：:P utword**](iwordformsink-putword.md) 會從詞幹分析器產生最後一個字組。 在所有情況下，這個最後的單字與 [**IStemmer：： GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms)的輸入字相同。 例如，假設「泳道」一字，則字幹分析器會產生下列單字格式： "游泳"、"swimmer"、"游泳"、"swam" 和 "swum" （透過呼叫 [**IWordFormSink：:P utaltword**](iwordformsink-putphrase.md)）。 此字幹分析器會透過 **IWordFormSink：:P utword** 來產生「泳道」。

### <a name="scalability-performancy-and-security"></a>擴充性、Performancy 和安全性

字幹分析器（例如斷詞工具）必須使用「免費」執行緒模型，並向 COM 註冊，其執行緒模型設定為「免費」或「兩者」。 Windows Search 會同時從不同的執行緒呼叫不同的詞幹分析器實例。 因此，字幹分析器應該會有基本的實例資料。

分析器精確度對查詢相關性有顯著的影響。 如果字幹分析器不正確地詞幹文字，查詢可能會傳回無法預測且不正確的結果。 字幹分析器必須每秒處理數百個查詢，而不會對查詢效能產生負面影響。 分析器效能應可利用增加的硬體功能來改善。 如需疑難排解字幹分析器的相關資訊，請參閱 [疑難排解語言資源和最佳作法](troubleshooting-language-resources.md)。

Windows Search 在本機安全性內容中執行的字幹分析器。 它們應該寫入來管理緩衝區，並正確地堆疊。 所有字串複本都必須有明確的檢查，以防止緩衝區溢位。 您應該一律確認已配置的緩衝區大小，並根據緩衝區大小測試資料的大小。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[擴充語言資源](extending-language-resources-in-windows-search.md)
</dt> <dt>

[瞭解語言資源元件](understanding-language-resource-components.md)
</dt> <dt>

[語言和 Unicode 考慮](linguistic-and-unicode-considerations.md)
</dt> <dt>

[疑難排解語言資源和最佳作法](troubleshooting-language-resources.md)
</dt> </dl>

 

 
