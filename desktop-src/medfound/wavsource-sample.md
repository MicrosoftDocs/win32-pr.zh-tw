---
description: WavSource 範例
ms.assetid: 905fbba5-0a04-4048-80bd-f8707c4879da
title: WavSource 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffba8ab5bfd5ae1ccfb4df4c90b447c412e9e835a403d496834224f012f8bad7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972537"
---
# <a name="wavsource-sample"></a>WavSource 範例

顯示如何在 Microsoft 媒體基礎中建立自訂媒體來源。 此範例會執行分析 wav 音訊檔案的媒體來源。

此範例是媒體來源的相對簡單範例：

-   只有一個資料流程，因此沒有可執行資料流程選取的程式碼。
-   媒體來源不會執行速率控制 (也就是向前快轉或反向播放) 。
-   所有來源和資料流程方法都會實作為同步方法。
-   由於 .wav 檔案的資料部分是未壓縮 PCM 音訊的單一區塊，因此媒體來源不需要讀取封包標頭，或在播放期間剖析串流，而非讀取初始 [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) 標頭。

如需更先進的媒體來源範例，請參閱 [MPEG1Source 範例](mpeg1source-sample.md)。

## <a name="apis-demonstrated"></a>示範的 Api

這個範例會示範下列媒體基礎介面：

-   [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

## <a name="usage"></a>使用方式

WavSource 範例會建立一個 DLL，它是媒體來源和媒體來源位元組資料流程處理常式的 COM 伺服器。 使用媒體來源之前，您必須先註冊 DLL。

若要使用媒體來源，您可以執行 [BasicPlayback](/previous-versions//bb970475(v=vs.85))。 如果您選取 .wav 檔案來播放，來源解析程式會自動載入媒體來源。  (如果發生錯誤，請確定您已成功註冊 WavSource DLL。 ) 

您也可以使用 TopoEdit 工具來建立包含媒體來源的播放拓撲。 如需 TopoEdit 的詳細資訊，請參閱 [TopoEdit](topoedit.md)。

## <a name="requirements"></a>規格需求



| 產品                                                        | 版本   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>下載範例

此範例可在[Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource)中取得。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎 SDK 範例](media-foundation-sdk-samples.md)
</dt> <dt>

[媒體來源](media-sources.md)
</dt> <dt>

[MPEG1Source 範例](mpeg1source-sample.md)
</dt> <dt>

[配置處理常式和 Byte-Stream 處理常式](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[撰寫自訂媒體來源](writing-a-custom-media-source.md)
</dt> </dl>

 

 
