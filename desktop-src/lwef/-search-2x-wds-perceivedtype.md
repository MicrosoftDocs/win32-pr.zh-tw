---
title: " (舊版 Windows 環境功能的認知類型) "
description: PerceivedType 是將索引中的專案分類的屬性。
ms.assetid: 47a5cf55-79f6-48e7-a585-72fc3d7d53d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de2baa37a46a9bd78e6e8a7ad94806dffe3a918046253bb09d4dab6090838b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610828"
---
# <a name="perceived-types-legacy-windows-environment-features"></a> (舊版 Windows 環境功能的認知類型) 

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在之後的版本中，請改用[Windows Search](../search/-search-3x-wds-overview.md) 。

`PerceivedType` 是在索引中分類專案的屬性。 此分類與 [Advanced Query 語法](-search-2x-wds-aqsreference.md) 所使用的「種類」分類不同，但同樣可讓使用者精簡其搜尋結果。 AQS 種類可讓使用者在 PerceivedType 屬性讓使用者篩選其結果集時，限制其搜尋查詢。

## <a name="types"></a>類型

使用 PerceivedType 屬性來分類您的檔案類型，讓使用者可以依類型篩選其搜尋結果。 輸出必須是下列其中一個字串：

-   連絡人
-   通訊
-   通訊/電子郵件
-   通訊/行事曆
-   通訊/工作
-   通訊/im
-   文件
-   document/note
-   document/text
-   檔/試算表
-   檔/簡報
-   music
-   images
-   影像/圖片
-   影像/影片
-   folder
-   程式

例如，當您想要為新的圖片檔案類型建立篩選增益集時，您需要在您的 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)介面中執行下列程式：

-   **GetChunk** 傳回包含下列內容的 FULLPROPSPEC： D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType
-   **GetValue** 傳回包含： VT \_ LPWSTR = "images/PICTURE" 的 PROPVARIANT

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[開發 IFilter 增益集](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[開發通訊協定處理常式](-search-2x-wds-phaddins.md)
</dt> <dt>

[進階查詢語法](-search-2x-wds-aqsreference.md)
</dt> <dt>

[SchemaTable](-search-2x-wds-schematable.md)
</dt> </dl>

 

 
