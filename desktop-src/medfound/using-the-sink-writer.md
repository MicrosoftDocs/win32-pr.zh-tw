---
description: .
ms.assetid: BE89E2E0-711F-4BD5-BB86-AA4CCA2D3E7F
title: 使用接收寫入器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46157eae6fe851468515f9d9653adb33918ebb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943863"
---
# <a name="using-the-sink-writer"></a>使用接收寫入器

## <a name="overview"></a>概觀

### <a name="file-container-types"></a>檔案容器類型

接收寫入器有數個檔案容器類型的內建支援。 For a complete list, see [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md). 您可以藉由撰寫自訂 [媒體接收器](media-sinks.md)來支援其他容器類型。 當您建立接收寫入器的新實例時，會指定檔案容器。

### <a name="stream-formats"></a>資料流程格式

針對每個資料流程，應用程式必須指定下列各項。

-   *輸入格式* 是應用程式傳送給接收寫入器的格式。
-   *輸出格式* 是將寫入檔案的格式。

輸入和輸出格式可以是已壓縮或未壓縮。 接收寫入器支援下列組合：

-   壓縮輸出的未壓縮輸入。 這是一般案例，用於編碼或轉碼案例。 Microsoft 媒體基礎編碼器必須可接受輸入類型，並對輸出類型進行編碼。
-   具有相同輸出的壓縮輸入。 您可以使用此組合來 remux 沒有轉碼的檔案。
-   具有相同輸出的未壓縮輸入。 使用這個組合將未壓縮的音訊或影片寫入檔案容器中。

除非編碼器提供這些函式，否則接收寫入器不支援影片調整大小、畫面播放速率轉換或音訊重新取樣。 否則，應用程式可以使用 [數位訊號處理器](windowsmediadigitalsignalprocessors.md) 來轉換輸入資料，然後再將資料傳送到

## <a name="creating-the-sink-writer"></a>建立接收寫入器

有兩個函數可建立接收寫入器：

-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) 會採用輸出檔案的 URL 或位元組資料流程的指標。 此函數會在內部建立媒體接收器。
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) 會取得應用程式已建立之媒體接收器的指標。

如果您使用其中一個內建的媒體接收器， [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) 函式是較理想的作法，因為呼叫端不需要設定媒體接收器。

[**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)方法提供數個選項來指定檔案容器的類型。 在最簡單的情況下，函數會使用 URL 中的副檔名來選取檔案容器。 如需詳細資料，請參閱函數參考頁面。

例如，下列程式碼會為 URL 指定檔案名 "output"。 接收寫入器會根據副檔名載入 [Asf 媒體接收器](asf-media-sinks.md) ，以建立 Advanced 系統格式 (asf) 檔。


```C++
    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);
```



在 [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)的案例中，檔案類型是由媒體接收所決定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[接收寫入器](sink-writer.md)
</dt> </dl>

 

 



