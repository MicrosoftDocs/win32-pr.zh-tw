---
description: 瞭解在 Windows Search 中建立篩選處理常式的最佳做法。 搜尋會使用篩選來將專案解壓縮，以包含在全文檢索索引中。
ms.assetid: 7b86a1b4-c8a9-400d-a9f1-a3b821c0269d
title: Windows Search 中篩選處理常式的最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a864cb2651d6236a212f3bf356eed3380869284
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989303"
---
# <a name="best-practices-for-creating-filter-handlers-in-windows-search"></a>在 Windows Search 中建立篩選處理常式的最佳作法

Microsoft Windows Search 會使用篩選器來解壓縮專案的內容，以包含在全文檢索索引中。 您可以藉由撰寫篩選處理常式來將內容解壓縮，並將屬性處理常式解壓縮以解壓縮檔案的內容，藉此擴充 Windows Search 來為新的或專屬的檔案類型編制索引。 篩選器會與檔案類型相關聯，如副檔名、MIME 類型或類別識別碼， (Clsid) 。 雖然一個篩選準則可以處理多個檔案類型，但每個類型只能使用一個篩選準則。

本主題包含下列幾節：

-   [機器碼](#native-code)
-   [Windows Search 的安全程式碼做法](#secure-code-practices-for-windows-search)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="native-code"></a>機器碼

在 Windows 7 和更新版本中，會明確封鎖以 managed 程式碼撰寫的篩選。 篩選準則必須以機器碼撰寫，因為有多個增益集在中執行的進程可能發生 CLR 版本控制問題。

## <a name="secure-code-practices-for-windows-search"></a>Windows Search 的安全程式碼做法

以下是撰寫安全應用程式以搭配 Windows Search 使用的做法。

**針對查詢應用程式：**

-   撰寫搜尋用戶端時，您應該選擇在安全性內容中執行的 API，讓使用者擁有最低許可權。 例如，ASP 頁面可以使用 IXSSO query 物件，該物件會以使用者進程的形式執行。

**針對 Ifilter 和語言資源：**

-   如果將檔案類型的新篩選處理常式安裝為現有篩選註冊的取代，則安裝程式應儲存目前的註冊，並在新的篩選器處理常式卸載時還原。 沒有任何機制可連結篩選。 因此，新的篩選處理常式會負責複寫舊篩選器的任何必要功能。
-   Windows Search 在本機安全性內容中執行的 Ifilter、斷詞工具和字幹分析器。 它們應該寫入來管理緩衝區，並正確地堆疊。 所有字串複本都必須有明確的檢查，以防止緩衝區溢位。 您應該一律確認已配置的緩衝區大小，並根據緩衝區大小測試資料的大小。 緩衝區溢位是利用不會強制執行緩衝區大小限制之程式碼的常見技術。
-   [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)、斷詞工具和字幹分析器元件絕對不應該呼叫 [ExitProcess](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) 函式函式或會終止進程及其所有線程的類似 API。
-   請勿在 DllMain 進入點中配置或釋放資源。 這可能會導致低資源壓力測試期間發生失敗。
-   將所有物件編寫為安全線程。 Windows Search 一次在一個執行緒中呼叫斷詞工具或分析器的任一個實例，但它可能會在多個執行緒上同時呼叫多個實例。
-   避免建立暫存檔案或寫入登錄。
-   如果您使用 Microsoft Visual C++ 編譯器，請務必使用 **/gs** 選項來編譯應用程式。 **/Gs** 選項可用來偵測緩衝區溢位。 /GS 選項會將安全性檢查放入已編譯的程式碼中。 如需詳細資訊， [](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx)請參閱  / Platform SDK Visual C++ 編譯器選項一節中的 DllGetClassObject 函式 **GS** (緩衝區安全性檢查) 。

## <a name="additional-resources"></a>其他資源

-   [IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)範例會示範如何建立用來執行 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)介面的 ifilter 基類。
-   如需索引編制程式的總覽，請參閱 [索引](-search-indexing-process-overview.md)程式。
-   如需檔案類型的總覽，請參閱 [檔案類型](../shell/fa-file-types.md)。
-   若要查詢檔案類型的檔案關聯屬性，請參閱 [PerceivedTypes、SystemFileAssociations 和應用程式註冊](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[開發篩選處理常式](-search-ifilter-conceptual.md)
</dt> <dt>

[關於 Windows Search 中的篩選處理常式](-search-ifilter-about.md)
</dt> <dt>

[從篩選處理常式傳回屬性](-search-ifilter-property-filtering.md)
</dt> <dt>

[Windows 隨附的篩選處理常式](-search-ifilter-implementations.md)
</dt> <dt>

[在 Windows Search 中執行篩選處理常式](-search-ifilter-constructing-filters.md)
</dt> <dt>

[註冊篩選處理常式](-search-ifilter-registering-filters.md)
</dt> <dt>

[測試篩選處理常式](-search-ifilter-testing-filters.md)
</dt> </dl>

 

 
