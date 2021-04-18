---
description: 本教學課程說明如何使用 Media Session 物件播放媒體檔案。
ms.assetid: cdd67082-8153-4f48-abc5-278be82ae082
title: 如何使用媒體基礎播放媒體檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163dba2f9f67139ce7477470889e13a54e2c8b5d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104560230"
---
# <a name="how-to-play-media-files-with-media-foundation"></a>如何使用媒體基礎播放媒體檔案

本教學課程說明如何使用 [Media Session](media-session.md) 物件播放媒體檔案。

## <a name="prerequisites"></a>必要條件

閱讀本主題之前，您應該先熟悉下列媒體基礎概念：

-   [媒體會話](media-session.md)
-   [來源解析程式](source-resolver.md)
-   [拓撲](topologies.md)
-   [媒體事件產生器](media-event-generators.md)
-   [簡報描述項](presentation-descriptors.md)

> [!Note]  
> 本主題不會說明如何播放受到數位版權管理 (DRM) 保護的檔案。 如需 Microsoft 媒體基礎中 DRM 的詳細資訊，請參閱 [如何播放受保護的媒體](how-to-play-protected-media-files.md)檔案。

 

## <a name="overview"></a>概觀

下列物件是用來播放媒體檔案和媒體會話：

-   *媒體來源* 是剖析媒體檔案或其他媒體資料來源的物件。 媒體來源會為檔案中的每個音訊或影片串流建立 *資料流程* 物件。 *解碼器* 會將編碼的媒體資料轉換成未壓縮的影片和音訊。
-   *來源解析程式* 會從 URL 建立媒體來源。
-   [增強型影片](enhanced-video-renderer.md)轉譯器 (EVR) 將影片轉譯至螢幕。
-   [串流音訊](streaming-audio-renderer.md)轉譯器 (SAR) 將音訊轉譯成喇叭或其他音訊輸出裝置。
-   *拓撲* 會定義從媒體來源到 EVR 和 SAR 的資料流程。
-   *媒體會話* 可控制資料流程並將狀態事件傳送至應用程式。 下圖說明此程序。

![顯示使用媒體會話播放的圖表](images/session-playback.gif)

以下是使用媒體會話播放媒體檔案時所需步驟的一般大綱：

1.  呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) 函式來初始化媒體基礎平臺。
2.  呼叫 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) 來建立媒體會話的新實例。
3.  使用來源解析程式來建立媒體來源。 如需詳細資訊，請參閱 [使用來源解析程式](using-the-source-resolver.md)。
4.  建立將媒體來源連接至 EVR 和 SAR 的拓撲。 在這個步驟中，應用程式會建立不包含該解碼器的 *部分* 拓撲。 如需詳細資訊，請參閱 [建立播放拓撲](creating-playback-topologies.md)。
5.  呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) 來設定媒體會話上的拓撲。
6.  使用 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面從媒體會話取得事件。
7.  呼叫 [**IMFMediaSession：： start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) 以開始播放。 播放開始之後，您可以藉由呼叫 [**IMFMediaSession：:P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)來暫停它，或呼叫 [**IMFMediaSession：： stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)來停止它。
8.  當應用程式結束時，釋放資源：

    1.  呼叫 [**IMFMediaSession：： close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) 以關閉媒體會話。 這個方法是非同步方法。 完成時，媒體會話會傳送 [MESessionClosed](mesessionclosed.md) 事件。 然後可以安全地執行其餘步驟。
    2.  呼叫 [**IMFMediaSource：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) 以關閉媒體來源。
    3.  呼叫 [**IMFMediaSession：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) 以關閉媒體會話。
    4.  呼叫 [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) 以關閉媒體基礎平臺。

下列各節顯示完整的程式碼範例：

-   [步驟1：宣告 CPlayer 類別](step-1--declare-the-cplayer-class.md)
-   [步驟2：建立 CPlayer 物件](step-2--create-the-cplayer-object.md)
-   [步驟3：開啟媒體檔案](step-3--open-a-media-file.md)
-   [步驟4：建立媒體會話](step-4--create-the-media-session.md)
-   [步驟5：處理媒體會話事件](step-5--handle-media-session-events.md)
-   [步驟6：控制播放](step-6--control-playback.md)
-   [步驟7：關機媒體會話](step-7--shut-down-the-media-session.md)
-   [媒體會話播放範例](media-session-playback-example.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體會話](media-session.md)
</dt> <dt>

[音訊/視訊播放](audio-video-playback.md)
</dt> </dl>

 

 



