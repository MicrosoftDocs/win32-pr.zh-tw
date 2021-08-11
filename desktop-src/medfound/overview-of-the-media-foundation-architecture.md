---
description: 本主題說明 Microsoft 媒體基礎的一般設計。 如需使用媒體基礎進行特定程式設計工作的詳細資訊，請參閱媒體基礎程式設計指南。
ms.assetid: DEA2B19A-CF15-4BF4-84C3-9A6417C942E2
title: 媒體基礎架構的總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de953d05c55c96d1affa2213e1a7f11143a71aa319b4671c159f085e65268d05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239627"
---
# <a name="overview-of-the-media-foundation-architecture"></a>媒體基礎架構的總覽

本主題說明 Microsoft 媒體基礎的一般設計。 如需使用媒體基礎進行特定程式設計工作的詳細資訊，請參閱 [媒體基礎程式設計指南](media-foundation-programming-guide.md)。

下圖顯示媒體基礎架構的高階觀點。

![此圖顯示 media foundation 架構的高階觀點。](images/mfarch01.png)

媒體基礎提供兩種不同的程式設計模型。 圖表左側所顯示的第一個模型會使用媒體資料的端對端管線。 應用程式會初始化管線，例如，藉由提供要播放之檔案的 URL，然後呼叫方法來控制串流。 在第二個模型（顯示于圖表右側）中，應用程式會從來源提取資料，或將資料推送至目的地 (或兩個) 。 如果您需要處理資料，此模型特別有用，因為應用程式可以直接存取資料流程。

### <a name="primitives-and-platform"></a>基本和平臺

從圖表底部開始， *基本* 專案是在整個媒體基礎 API 中使用的 helper 物件：

-   [屬性](attributes-and-properties.md) 是在物件內儲存資訊的一般方式，作為索引鍵/值組的清單。
-   [媒體類型](media-types.md) 描述媒體資料流程的格式。
-   [媒體緩衝區](media-buffers.md) 會保存媒體資料的區塊，例如影片畫面和音訊範例，並可用來在物件之間傳輸資料。
-   [媒體範例](media-samples.md) 是媒體緩衝區的容器。 它們也包含有關緩衝區的中繼資料，例如時間戳記。

[媒體基礎平臺 api](media-foundation-platform-apis.md)提供媒體基礎管線所使用的一些核心功能，例如非同步回呼和工作佇列。 某些應用程式可能需要直接呼叫這些 Api;此外，如果您針對媒體基礎執行自訂來源、轉換或接收，則需要它們。

### <a name="media-pipeline"></a>媒體管線

媒體管線包含產生或處理媒體資料的三種物件類型：

-   [媒體來源](media-sources.md) 會將資料導入管線中。 媒體來源可能會從本機檔案（例如影片檔案）取得資料;從網路資料流程;或從硬體捕獲裝置。
-   [媒體基礎轉換](media-foundation-transforms.md) (MFTs) 處理來自資料流程的資料。 編碼器和解碼器會實作為 MFTs。
-   [媒體接收器](media-sinks.md) 耗用資料;例如，藉由顯示顯示器上的影片、播放音訊，或將資料寫入媒體檔案。

協力廠商可以實行自己的自訂來源、接收和 MFTs;例如，支援新的媒體檔案格式。

[媒體會話](media-session.md)可控制流經管線的資料流程，並處理品質控制、音訊/影片同步處理及回應格式變更等工作。

### <a name="source-reader-and-sink-writer"></a>來源讀取器和接收寫入器

[來源讀取](source-reader.md)器和[接收寫入器](sink-writer.md)提供另一種方式，可讓您使用基本媒體基礎元件 (媒體來源、轉換和媒體接收器) 。 來源讀取器會裝載媒體來源和零或多個編碼器，而接收寫入器則會裝載媒體接收器和零或多個編碼器。 您可以使用來源讀取器從媒體來源取得壓縮或未壓縮的資料，並使用接收寫入器來對資料進行編碼，並將資料傳送至媒體接收。

> [!Note]  
> 來源讀取器和接收寫入器可在 Windows 7 中取得。

 

此程式設計模型可讓應用程式更充分掌控資料的流程，也可讓應用程式直接存取來源的資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎：基本概念](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[媒體基礎架構](media-foundation-architecture.md)
</dt> </dl>

 

 



