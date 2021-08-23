---
description: WavSink 範例
ms.assetid: 9e1af25f-d55c-45db-8c76-abf814e16700
title: WavSink 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1bd754e426d848e9d84aea337225ea51940d8727c63d1e1c78c93aeea43110
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737133"
---
# <a name="wavsink-sample"></a>WavSink 範例

顯示如何在 Microsoft 媒體基礎中執行自訂媒體接收器。 此範例會執行封存接收器，以將未壓縮的 PCM 音訊寫入 .wav 檔案。

## <a name="apis-demonstrated"></a>示範的 Api

這個範例會示範下列媒體基礎介面：

-   [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)
-   [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
-   [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)

## <a name="usage"></a>使用方式

WavSink 範例包含兩個 Visual Studio 專案：

-   WavSink 會建立包含媒體接收執行的靜態程式庫。
-   WriteWavFile 會建立一個主控台應用程式，該應用程式會使用媒體接收器來產生 .wav 檔。 此應用程式會連結至 WavSink 專案所建立的程式庫。

## <a name="requirements"></a>規格需求



| 產品                                                        | 版本   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>下載範例

此範例可在[Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink)中取得。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎 SDK 範例](media-foundation-sdk-samples.md)
</dt> <dt>

[媒體接收器](media-sinks.md)
</dt> </dl>

 

 



