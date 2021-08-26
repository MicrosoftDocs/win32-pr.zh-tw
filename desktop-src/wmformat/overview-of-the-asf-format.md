---
title: ASF 格式的概觀
description: ASF 格式的概觀
ms.assetid: ef22a493-d6cf-40d2-ab17-d87159066d1d
keywords:
- Windows媒體格式 SDK，ASF 格式總覽
- Advanced Systems Format (ASF) ，格式總覽
- ASF (Advanced Systems Format) ，格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee075330e9c68ef1fbdadea12c70fd8deec584f99f8dadd31cb55070dc11eee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930558"
---
# <a name="overview-of-the-asf-format"></a>ASF 格式的概觀

Advanced Systems Format (ASF) 是一種可延伸的檔案格式，主要是用來儲存及播放同步處理的數位媒體串流，並透過網路傳輸。 ASF 是 Windows Media 音訊的容器格式，也是以 Windows Media 視訊為基礎的內容。 副檔名 wma 或 wmv 可用來指定 ASF 檔案，其中包含以 Windows Media 音訊和/或 Windows Media 視訊編解碼器編碼的內容。 Windows 媒體格式 SDK 可以用來建立和讀取 Windows 媒體檔案，以及包含其他類型壓縮或未壓縮資料的 ASF 檔案。

本節提供 ASF 格式的一般描述作為背景資訊。 由於讀取器和寫入器物件會處理所有的低層級檔案剖析和格式化工作，因此在使用此 SDK 建立 ASF 檔案之前，不需要先深入瞭解 ASF。 您可以在 [Microsoft 網站](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)上找到完整的 ASF 規格。

ASF 格式的主要目標是：

-   支援從媒體伺服器、HTTP 伺服器和本機存放裝置進行有效率的播放。
-   支援可調整的媒體類型，例如音訊和影片。
-   允許在各式各樣的頻寬上呈現單一多媒體組合。
-   允許撰寫媒體資料流程關聯性的控制權，特別是在受限頻寬的案例中。
-   獨立于任何特定的多媒體組合系統、電腦作業系統或資料通訊協定。

ASF 檔案可以包含多個獨立或相依的資料流程，包括多頻道音訊的多個音訊串流，或適用于透過不同頻寬傳輸的多重位元速率影片串流。 資料流程可以採用任何壓縮或未壓縮的格式;不過，最佳壓縮可透過 Microsoft Windows Media 音訊和 Video 9 系列編解碼器來達成。 除了標準音頻和影片媒體資料流程類型之外，ASF 檔案也可以包含文字串流、網頁和指令碼命令，以及任何其他任意資料類型。 ASF 支援即時和隨選多媒體內容。 您可以使用它作為車輛來錄製或播放 32 (例如，h.264 和 h.) 或 MBONE 會議。

ASF 檔會組織成稱為「物件」的區段。 有三個最上層物件，標頭物件和資料物件 (需要的) ，再加上選擇性的索引物件。 標頭物件包含檔案的一般資訊，例如檔案大小、資料流程數目、錯誤修正方法，以及使用的編解碼器。 中繼資料也會儲存在這裡。 標頭物件是唯一可包含其他物件的最上層物件。 資料物件包含資料流程資料，並組織成封包。 Simple Index 物件包含一份相關聯的索引/主要畫面格配對清單，可讓應用程式有效率地搜尋檔案。 與每個主要畫面格相關聯的索引可以是展示時間、影片畫面號碼或參考時間戳記。

每個最上層或較低層級的物件都是以全域唯一識別碼（ (GUID) 和大小值）作為開頭。 這些數位可讓檔案讀取器將適當位置的資訊剖析成可辨識的物件。 因為這些 Guid，較低層級的物件可以依任何順序傳送，而且仍可辨識。 ASF 格式的設計目的是克服不正確的資料接收。 部分下載的 ASF 檔案仍可讀取，只要其中包含標頭物件和至少一個資料物件。

ASF 規格中顯示之 ASF 的詳細資訊。 您可以從 [Microsoft 網站](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)下載規格。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 Windows 媒體格式 SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




