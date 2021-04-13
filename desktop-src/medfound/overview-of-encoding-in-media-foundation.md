---
description: 本主題概述 Microsoft 媒體基礎中提供的檔案編碼 Api。
ms.assetid: 69dbef63-e272-4ad2-8d04-ae9366f79b33
title: 媒體基礎中的編碼總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81882bd6da43f4040614347b662d988844c7b7a6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104559715"
---
# <a name="overview-of-encoding-in-media-foundation"></a>媒體基礎中的編碼總覽

本主題概述 Microsoft 媒體基礎中提供的檔案編碼 Api。

## <a name="terminology"></a>詞彙

*編碼* 是涵蓋數個不同程式的一般詞彙：

1.  將音訊或影片串流編碼為壓縮格式。 例如，將影片串流編碼為 h.264 video。
2.  多工 ( "muxing" ) 一個或多個資料流程轉換成單一位元組資料流程。 一般而言，傳入的資料流程會先進行編碼。 此步驟可能涉及 packetizing 編碼的資料流程。
3.  將多工位元組資料流程寫入至檔案（例如，使用檔或 Advanced 系統格式） (ASF) 檔。 或者，您也可以透過網路傳送多工資料流程。

下圖顯示這三個進程：

![顯示編碼和多工處理常式的圖表](images/encoding03.png)

此流程的變化包括轉碼和 remuxing：

-   *轉碼* 表示解碼現有的檔案、重新編碼資料流程，以及重新多工編碼的資料流程。 您可以執行轉碼來將檔案從某種編碼類型轉換成另一種編碼類型;例如，若要將 h.264 video 轉換成 Windows Media 視訊 (WMV) 。 也可以這樣做來變更編碼的位元速率。影片框架大小;畫面播放速率;或其他格式參數。
-   *Remultiplexing* 或 *remuxing* 表示分離信號檔案並重新多工處理資料流程，而不使用解碼/編碼步驟。 這可能是為了變更音訊/影片封包的多工處理方式、移除資料流程或合併來自兩個不同來源檔案的資料流程。
-   *Transrating* 是轉碼的特殊案例，其中的位元速率會變更，而不會變更壓縮類型。 例如，您可以將高位元速率檔案轉換成較低的位元速率。 Transrating 可能使用的一般案例是將媒體內容從電腦同步處理到可攜式裝置。 如果可攜式裝置不支援較高的位元速率，則檔案可能會在複製到可攜式裝置之前 transrated。

下列區塊圖顯示轉碼進程。

![顯示轉碼進程的圖表](images/encoding05.png)

下列區塊圖顯示 remuxing 流程。

![顯示 remuxing 流程的圖表](images/encoding06.png)

此檔有時會使用詞彙 *編碼* 來同時包含轉碼和 remuxing。 很重要的一點是要區分它們，檔將會注意到差異。

另請參閱： [媒體基礎：基本概念](media-foundation-programming--essential-concepts.md)。

## <a name="media-foundation-encoding-architecture"></a>媒體基礎編碼架構

在媒體基礎架構的最低層級中，會使用下列類型的元件來進行編碼：

-   針對轉碼， [媒體來源](media-sources.md) 會用來 demultiplex 原始程式檔。
-   針對編碼程式， [媒體基礎轉換](media-foundation-transforms.md) 會用來將資料流程解碼和編碼。
-   針對多工處理常式，會使用 [媒體接收器](media-sinks.md) 來多工處理資料流程，並將多工資料流程寫入檔案或網路。

下圖顯示在轉碼案例中，這些元件之間的資料流程：

![顯示轉碼中使用之元件的圖表](images/encoding04.png)

大部分的應用程式都不會直接使用這些元件。 相反地，應用程式會使用較高層級的 Api 來管理這些較低層級的元件。 媒體基礎提供兩個較高層級 Api 來進行編碼：

<dl> <dt>

<span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[媒體會話](media-session.md)
</dt> <dd>

媒體會話提供端對端管線，可將資料從媒體來源、編解碼器，最後移至媒體接收器。 應用程式會控制媒體會話，並接收來自媒體會話的狀態事件。

</dd> <dt>

<span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[來源讀取器](source-reader.md) 加上 [接收寫入器](sink-writer.md)
</dt> <dd>

來源讀取器會包裝媒體來源和選擇性的解碼器。 它會為應用程式提供編碼或解碼的範例。 接收寫入器會包裝媒體接收和選擇性的編碼器。 應用程式會將範例傳遞給接收寫入器。

</dd> </dl>

下圖顯示媒體會話：

![顯示媒體會話如何執行轉碼的圖表](images/encoding01.png)

[轉碼 API](transcode-api.md) (藍色陰影方塊) 是一組在 Windows 7 中引進的 api，可讓您更輕鬆地設定媒體會話以進行編碼。

下圖顯示來源讀取器和接收寫入器：

![顯示具有來源讀取器和接收寫入器之轉碼的圖表](images/encoding02.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[編碼與檔案編寫](encoding-and-file-authoring.md)
</dt> <dt>

[媒體基礎程式設計：基本概念](media-foundation-programming--essential-concepts.md)
</dt> </dl>

 

 



