---
description: 檔案類型驗證程式是一種工具，可讓獨立軟體廠商 (Isv) 驗證其唯一的檔案類型是否正確執行。
ms.assetid: 1BD7452B-2DF5-44e9-9B09-C29ABFFA5F93
title: 檔案類型驗證器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8e4a588e4889241762a9d8e0567d4a4542c0255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849206"
---
# <a name="file-type-verifier"></a>檔案類型驗證器

檔案類型驗證程式是一種工具，可讓獨立軟體廠商 (Isv) 驗證其唯一的檔案類型是否正確執行。 檔案類型處理常式的高品質實作為良好使用者體驗的關鍵，因為使用者會在 Windows 檔案總管中以許多方式與您的檔案格式互動。 使用者可以進行全文檢索搜尋、依自訂中繼資料排序，或查看檔案格式的豐富縮圖和預覽。

如需使用檔案類型驗證器的指示，請參閱 [如何使用檔案類型驗證](how-to-use-the-file-type-verifier.md)器。

## <a name="about-the-file-type-verifier-tool"></a>關於檔案類型驗證器工具

檔案類型驗證程式是 [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)中提供的一種程式。 它的設計目的是協助開發人員建立自訂的 Windows [檔案類型](fa-file-types.md) ，以偵測其檔案類型的潛在問題。 雖然檔案類型驗證器只會在 Windows 7 和更新版本上執行，但是檔案類型驗證器所強制執行的規則會套用至其所檢查之功能可用的所有 Windows 版本。

檔案類型驗證程式會對檔案類型執行數個測試，以確認它已正確註冊，而且會提供適當的 [檔案類型處理常式](fa-file-extensions.md) ，以便在 Windows 檔案總管適當地顯示檔案類型，並在適當的情況下支援為檔案內容編制索引。

檔案類型驗證器會測試下列專案：

-   [預覽處理常式](building-preview-handlers.md)
-   [縮圖處理常式](building-thumbnail-providers.md)
-   [屬性處理常式](../search/-search-3x-wds-extidx-propertyhandlers.md)
-   [動詞處理常式](fa-verbs.md)
-   [篩選 (IFilter) ](../search/-search-3x-wds-extidx-filters.md)
-   [種類關聯](../properties/building-property-handlers-user-friendly-kind-names.md)
-   [認知類型](fa-perceivedtypes.md)
-   [重要屬性](../search/-shell-systemdefinedpropertiesforfileformats.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何使用檔案類型驗證器](how-to-use-the-file-type-verifier.md)
</dt> <dt>

[應用程式註冊](app-registration.md)
</dt> <dt>

[檔案類型](fa-file-types.md)
</dt> <dt>

[檔案關聯的運作方式](fa-how-work.md)
</dt> <dt>

[依檔案類型或種類的內容視圖](prophand-content-view.md)
</dt> <dt>

[檔案類型處理常式](fa-file-extensions.md)
</dt> <dt>

[程式設計識別碼](fa-progids.md)
</dt> <dt>

[認知類型](fa-perceivedtypes.md)
</dt> <dt>

[關聯陣列](fa-associationarray.md)
</dt> </dl>

 

 
