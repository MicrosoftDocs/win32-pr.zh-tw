---
description: 本主題提供針對 IWordBreaker 和 IStemmer 的執行進行驗證和疑難排解的最佳作法和建議。
ms.assetid: b0e199b9-8d81-4445-92f7-de9b8a00a9cb
title: 疑難排解語言資源和最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63a0a8acda3fff1627b37f41c2d81a67b37d66a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689836"
---
# <a name="troubleshooting-language-resources-and-best-practices"></a>疑難排解語言資源和最佳作法

本主題提供針對 [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) 和 [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) 的執行進行驗證和疑難排解的最佳作法和建議。

本主題的組織方式如下：

-   [最佳作法](#best-practices)
-   [測試詞幹分析器一致性](#testing-stemmer-consistency)
-   [在詞幹分析器中測試不正確輸入](#testing-for-invalid-input-in-the-stemmer)
-   [測試斷詞工具一致性](#testing-word-breaker-consistency)
-   [測試斷詞工具中是否有不正確輸入](#testing-for-invalid-input-in-the-word-breaker)

### <a name="best-practices"></a>最佳做法

-   確定 [語言資源] 的執行緒模型在登錄中設定為 [兩者]。
-   可能的話，請將語言資料放入 DLL 中的資源，而不是放在個別的檔案中。 這樣可讓 DLL 更容易安裝且更安全。 此外，將語言資料放入資源中，會導致該語言資源元件的效能提升。
-   將語言資源元件使用的系統資源降至最低。 例如，如果語言資源物件的每個實例都需要字典的唯讀存取權，請考慮在所有實例之間共用該詞典。
-   請考慮使用中性斷詞工具，來處理不在您的斷詞工具執行語言或地區設定中的文字。 這有助於確保在所有語言中都能一致地處理文字。
-   檢查所有傳回碼，然後從 [**IStemmer：： GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) 和 [**IWordBreaker：： BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext)等函數傳回。 如果索引失敗，請務必傳遞錯誤，讓使用者收到已編制索引的檔。

### <a name="testing-stemmer-consistency"></a>測試詞幹分析器一致性

建議您在下列情況下，監視 [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) 執行的效能是否一致：

-   此字幹分析器會在 [**IStemmer：： Init**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-init)的多個呼叫中一致地執行。 使用與先前的初始化相同的參數重新初始化分析器，而不釋放參數。
-   如果有相同的測試主體和重複相同的查詢， [**IStemmer：： GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) 會產生相同的輸出，並且對 [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) 物件的方法進行相同的呼叫。

### <a name="testing-for-invalid-input-in-the-stemmer"></a>在詞幹分析器中測試不正確輸入

建議您監視 [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) 方法如何處理與無效參數相關的所有錯誤。 此外，我們建議您確定詞幹分析器方法不會引發未處理的例外狀況。 此字幹分析器應該會處理下列錯誤：

-   呼叫 [**IStemmer：： Init**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-init) ，並將 *PfLicense* 設定為 **Null**。 Init 失敗，而且不會造成存取違規。
-   呼叫 [**IStemmer：： GetLicenseToUse**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-getlicensetouse) ，並將 *ppwcsLicense* 參數設定為 **Null**。 **IStemmer：： GetLicenseToUse** 不會造成存取違規。
-   呼叫 [**IStemmer：： GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) ，並將 *pwcInBuf* 參數設定為 **Null**。 **IStemmer：： GenerateWordForms** 失敗 (傳回 E \_) 失敗，而且不會造成存取違規。
-   呼叫 [**IStemmer：： GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) ，並將 *cwc* 參數等於0。 **IStemmer：： GenerateWordForms** 會成功傳回 (傳回 S \_ 確定) 而不會導致存取違規。
-   呼叫 [**IStemmer：： GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) ，並將 *pwcInBuf* 參數設定為 **Null** ，而 *cwc* 參數等於0。 **IStemmer：： GenerateWordForms** 失敗 (傳回 E \_) 失敗，而且不會造成存取違規。

### <a name="testing-word-breaker-consistency"></a>測試斷詞工具一致性

建議您在下列情況下，確保 [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) 的執行持續一致：

-   斷詞工具會在對其 [**IWordBreaker：： Init**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-init) 方法的多個呼叫之間持續執行。 斷詞工具會使用與先前初始化相同的參數重新初始化，而不會釋放參數。
-   針對相同的測試主體和重複相同的查詢， [**IWordBreaker：： BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) 方法會產生相同的輸出，並且對 [**IWordSink**](iwordsink.md) 和 [**IPhraseSink**](/windows/win32/api/indexsrv/nn-indexsrv-iphrasesink) 物件的方法進行相同的呼叫。

### <a name="testing-for-invalid-input-in-the-word-breaker"></a>測試斷詞工具中是否有不正確輸入

建議您確保 [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) 方法會處理與無效參數相關的所有錯誤。 此外，我們建議您確定斷詞工具方法不會引發未處理的例外狀況。 斷詞工具應該執行下列功能，並處理下列錯誤：

-   呼叫 [**IWordBreaker：： Init**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-init) 必須傳回 \_ 找不到 LANGUAGE E \_ 資料庫 \_ \_ 或 S \_ OK。
-   呼叫 [**IWordBreaker：： Init**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-init) 成功將 *pfLicense* 參數初始化為 **FALSE** ，並呼叫 [**IStemmer：： GetLicenseToUse**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-getlicensetouse) ，且不會造成存取違規。
-   斷詞工具不會讀取超過 [**IWordBreaker：： BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext)方法中 *awcBuffer* 參數的結尾。
-   呼叫 [**IWordBreaker：： BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) ，並將 *PwcInBuf* 設定為 **Null**。 **IWordBreaker：： BreakText** 失敗 (傳回 E \_) 失敗，而且不會造成存取違規。
-   呼叫 [**IWordBreaker：： BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) ，並將 *cwc* 參數等於0。 **IWordBreaker：： BreakText** 會成功傳回 (傳回 S \_ 確定) 而不會導致存取違規。
-   呼叫 [**IWordBreaker：： BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) 方法，並將 *pwcInBuf* 參數設定為 **Null** ，且 *cwc* 參數等於0。 **IWordBreaker：： BreakText** 失敗 (傳回 E \_) 失敗，而且不會造成存取違規。
-   在索引建立期間產生的片語包含相同數目的文字。
-   在索引建立期間，會透過連續呼叫 [**IWordFormSink：:P utword**](iwordsink-putword.md) 和 [**IWordFormSink：:P utaltword**](iwordsink-putaltword.md) 方法來產生片語。 斷詞工具在查詢時只會使用 [**IPhraseSink**](/windows/win32/api/indexsrv/nn-indexsrv-iphrasesink) 物件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[擴充語言資源](extending-language-resources-in-windows-search.md)
</dt> <dt>

[瞭解語言資源元件](understanding-language-resource-components.md)
</dt> <dt>

[執行斷詞工具和字幹分析器](implementing-a-word-breaker-and-stemmer.md)
</dt> <dt>

[語言和 Unicode 考慮](linguistic-and-unicode-considerations.md)
</dt> </dl>

 

 
