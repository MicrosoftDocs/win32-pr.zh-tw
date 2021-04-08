---
title: 關於 IMediaObject
description: 關於 IMediaObject
ms.assetid: c483f74a-efd8-4a9f-a719-686099755e63
keywords:
- Windows Media Player 外掛程式，介面
- 外掛程式，介面
- 數位信號處理外掛程式，介面
- DSP 外掛程式，介面
- 介面、DSP 外掛程式
- Windows Media Player 外掛程式、IMediaObject 介面
- 外掛程式，IMediaObject 介面
- 數位信號處理外掛程式，IMediaObject 介面
- DSP 外掛程式，IMediaObject 介面
- IMediaObject 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbbecd749242b67bc5c8f36b3c7a2c0a5fbe461
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671564"
---
# <a name="about-imediaobject"></a>關於 IMediaObject

**IMediaObject** 介面是 DMOs 所需的介面。 **IMediaObject** 包含 WINDOWS MEDIA PLAYER 的 DSP 外掛程式用來從 Windows Media Player 取得資料、處理資料，以及將已處理的資料傳回 Windows Media Player 的方法。 如需 **IMediaObject** 介面的完整檔，請參閱 Windows SDK 的 [DirectShow] 區段。

**IMediaObject** 的方法可分類如下：

## <a name="methods-that-handle-format-negotiation"></a>處理格式協調的方法

這些是 Windows Media Player 呼叫的方法，以取得外掛程式所支援之資料格式的相關資訊。 這些方法包括：

-   **GetInputMaxLatency**
-   **GetInputSizeInfo**
-   **GetInputStreamInfo**
-   **GetInputType**
-   **GetOutputSizeInfo**
-   **GetOutputStreamInfo**
-   **GetOutputType**
-   **GetStreamCount**
-   **SetInputMaxLatency**
-   **SetInputType**
-   **SetOutputType**

其中有幾種方法（例如 **GetInputType** 和 **SetInputType**）會使用 **sql-dmo \_ 媒體 \_ 類型** 結構來描述資料流程所使用的資料格式。 當 Windows Media Player 呼叫這些方法時，它會提供一種對等 **\_ 媒體 \_ 類型** 結構的指標。 如果方法（例如 **SetInputType** ）指定媒體類型資訊，外掛程式應該將 [] **\_ 媒體 \_ 類型** 結構複製到成員變數，並檢查其資料成員，以判斷 Windows Media Player 將在輸入緩衝區中提供的資料類型。 如果 **GetInputType** 這類方法會抓取媒體型別資訊，外掛程式應該將包含 **sql-dmo \_ 媒體 \_ 類型** 結構的成員變數位址複製到參數清單中 Windows Media Player 所提供的指標。

Windows Media Player 主要會使用兩種 **類型的 \_ 媒體 \_ 類型** 結構的成員：

-   **majortype**： (GUID) 的全域唯一識別碼，可指定媒體的整體類別，例如音訊或影片。
-   **子類型**：指定更詳細描述媒體的 GUID，例如 PCM 音訊。

這些 Guid 可以在名為 uuid 的標頭中找到，該標頭包含在 Windows SDK 中。

**GetInputSizeInfo** 之類的方法會提供相關資訊，以 Windows Media Player 配置處理緩衝區所需的記憶體數量。 **GetStreamCount** 和 **GetOutputStreamInfo** 這類方法會提供有關 DSP 外掛程式所支援資料流程之數位和字元的資訊 Windows Media Player。

在特殊情況下，DMOs 會執行 **GetInputMaxLatency** 和 **SetInputMaxLatency** 。 Windows Media Player 的 DSP 外掛程式應該會傳回 E \_ >notimpl。

## <a name="methods-that-specify-or-retrieve-state-information"></a>指定或取得狀態資訊的方法

這些方法可 Windows Media Player 呼叫來取得或設定與外掛程式目前狀態相關的值。 這些方法包括：

-   **GetInputCurrentType**
-   **GetInputStatus**
-   **GetOutputCurrentType**

**GetInputCurrentType** 和 **GetOutputCurrentType** 會使用 **： \_ 媒體 \_ 類型** 結構來傳回有關先前針對輸入和輸出資料流程設定之媒體類型 Windows Media Player 的資訊。 **GetInputStatus** 會傳回旗標，告知 Windows Media Player DSP 外掛程式是否可以接受輸入資料。

## <a name="methods-that-handle-buffering-and-processing-data"></a>處理緩衝處理和處理資料的方法

這些是 Windows Media Player 呼叫的方法，以起始外掛程式執行以執行數位信號處理的各種進程。 這些方法包括：

-   **AllocateStreamingResources**
-   **間斷**
-   **清除**
-   **FreeStreamingResources**
-   **鎖定**
-   **ProcessInput**
-   **ProcessOutput**

Windows Media Player 會呼叫 **AllocateStreamingResources** 和 **FREESTREAMINGRESOURCES** 來提供 DSP 外掛程式，讓您有機會設定或釋放外掛程式可能需要進行內部處理的任何其他緩衝區。

Windows Media Player 的 DSP 外掛程式不需要 **使用 sql-dmo 中斷** 方法。

Windows Media Player 呼叫 **Flush** 來指示 DSP 外掛程式，以排清所有內部緩衝的資料。 外掛程式應釋放 **IMediaBuffer** 介面的任何參考、清除任何指定媒體緩衝區之時間戳記或取樣長度的值，然後重新初始化相依于媒體範例內容的任何內部狀態。

Windows Media Player 會呼叫 ProcessInput，將 **IMediaBuffer** 介面的指標傳遞至 DSP 外掛程式。 這個介面可讓您存取 Windows Media Player 所配置的輸入緩衝區，以提供資料給外掛程式。 Windows Media Player 接著會呼叫 **ProcessOutput** ，將指標傳遞至 **IMediaBuffer** 介面，以提供由 Windows Media Player 所配置之輸出緩衝區的存取，以接收來自 DSP 外掛程式的已處理資料。

**IMediaObject** 介面包含名為 **Lock** 的方法。 這個方法是設計用來取得或釋放該的鎖定，以在執行多個作業時保留一次。 Wizard 程式碼中的 **IMediaObject：： Lock** 版本會覆寫 **鎖定** 的 ATL 執行。 因為 Windows Media Player 會序列化對 DSP 外掛程式的 SQL-DMO 介面進行的呼叫，所以 **鎖定** 的執行只會傳回 S \_ OK。 如需有關如何建立多執行緒的詳細資訊，請參閱 Windows SDK 的 [DirectShow] 區段。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**必要的介面**](required-interfaces.md)
</dt> </dl>

 

 




