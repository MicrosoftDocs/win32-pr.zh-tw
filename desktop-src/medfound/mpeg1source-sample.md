---
description: MPEG1Source 範例
ms.assetid: c9f131ff-0b79-487c-9a46-a9b1350553a1
title: MPEG1Source 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c71bd541a7bd01621ca7359eb9e229a08e91a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987429"
---
# <a name="mpeg1source-sample"></a>MPEG1Source 範例

顯示如何在 Microsoft 媒體基礎中撰寫自訂媒體來源。 此範例會執行可剖析 MPEG-2 系統層串流的媒體來源，並產生包含 MPEG-2 承載的範例。

## <a name="apis-demonstrated"></a>示範的 Api

這個範例會示範下列媒體基礎介面：

-   [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

在檢查這個範例之前，您可能會想要先複習 [WavSource 範例](wavsource-sample.md)，以提供更簡單的媒體來源執行。 MPEG1Source 範例會新增一些功能，這些功能可在大部分真實世界的媒體來源執行中找到：

-   多個資料流
-   非同步方法
-   非同步 i/o

在 Windows Server 2008 的 Windows SDK 中，此範例也包含範例 MPEG-2 視頻解碼器，可顯示每個影片畫面的時間代碼。  (它實際上並不會解碼 MPEG-2 位流。 ) 

從 Windows 7 的 Windows SDK 開始，已將此解碼器移至個別的範例。 請參閱 [解碼器範例](decoder-sample.md)。

## <a name="usage"></a>使用方式

MPEG1Source 範例會建立一個 DLL，它是媒體來源、媒體來源位元組資料流程處理常式和解碼器 MFT 的 COM 伺服器。 使用媒體來源之前，您必須先註冊 DLL。

若要使用媒體來源，您可以執行 [BasicPlayback 範例](/previous-versions//bb970475(v=vs.85))。 如果您選取要播放的 MPEG-2 檔案，來源解析程式會自動載入媒體來源。  (如果發生錯誤，請確定您已成功註冊 MPEG1Source DLL。 ) 

您也可以使用 TopoEdit 工具來建立包含媒體來源的播放拓撲。 如需 TopoEdit 的詳細資訊，請參閱 [TopoEdit](topoedit.md)。

## <a name="requirements"></a>規格需求



| 產品                                                        | 版本   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>下載範例

此範例可在 [Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source)中取得。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎 SDK 範例](media-foundation-sdk-samples.md)
</dt> <dt>

[媒體來源](media-sources.md)
</dt> <dt>

[配置處理常式和 Byte-Stream 處理常式](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[教學課程：撰寫自訂媒體來源](tutorial--writing-a-custom-media-source.md)
</dt> <dt>

[WavSource 範例](wavsource-sample.md)
</dt> </dl>

 

 
