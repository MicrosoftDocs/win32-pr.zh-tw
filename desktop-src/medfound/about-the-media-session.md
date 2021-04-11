---
description: 關於媒體會話
ms.assetid: 09f50b11-0e0a-42b6-a7bf-bb0135343351
title: 關於媒體會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc490e63f623fb3c2d5efde5a80f1988566f9345
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945590"
---
# <a name="about-the-media-session"></a>關於媒體會話

媒體會話會公開 [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) 介面。 有兩種方式可以建立媒體會話，視您的應用程式是否支援受保護的內容而定：

-   如果您的應用程式不支援受保護的內容，您可以藉由呼叫 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession)來建立媒體會話。 此函式會在應用程式進程內建立媒體會話。
-   若要支援受保護的內容，請呼叫 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)來建立媒體會話。 此函式會在受保護的媒體路徑內建立媒體會話， (PMP) 進程。 應用程式會接收 proxy 物件的指標，此物件會將跨進程界限的方法呼叫封送處理。 請注意，PMP 媒體會話可以用來播放清楚的內容，以及受保護的內容。

任何使用媒體會話的應用程式將會遵循下列一般步驟：

1.  建立拓撲。
2.  藉由呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)，在媒體會話上將拓撲排入佇列。
3.  藉由呼叫 [**IMFMediaSession：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)、 [**IMFMediaSession：:P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)或 [**IMFMediaSession：： Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)來控制資料的流程。
4.  在應用程式結束之前，呼叫 [**IMFMediaSession：： close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) 以關閉媒體會話。
5.  藉由呼叫 [**IMFMediaSource：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown)，關閉應用程式所建立的任何媒體來源。
6.  藉由呼叫 [**IMFMediaSession：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)來關閉媒體會話。

使用媒體會話時，應用程式不應該直接啟動、暫停或停止媒體來源。 所有狀態變更都必須藉由呼叫 [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) 方法來啟動。 媒體會話會處理媒體來源中的狀態變更。

許多其他詳細資料將取決於您應用程式的特定功能。

## <a name="protected-content"></a>受保護內容

若要播放受保護的內容，您必須藉由呼叫 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)，在受保護的媒體路徑 (PMP) 內建立媒體會話。 此函式會在 PMP 內建立媒體會話的實例，並將指標傳回給跨進程界限封送處理介面的 proxy 物件。

在大部分的情況下，在 PMP 內使用媒體會話對應用程式而言是透明的。 不過，應用程式可能需要叫用可讓使用者播放內容的特定動作。 例如，使用者可能需要取得 DRM 授權。 媒體基礎使用 [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) 介面定義這些動作的一般機制。

如需詳細資訊，請參閱下列主題：

-   [受保護的媒體路徑](protected-media-path.md)
-   [如何播放受保護的媒體檔案](how-to-play-protected-media-files.md)

## <a name="presentation-clock"></a>簡報時鐘

媒體會話會管理簡報時鐘的所有層面：

-   建立簡報時鐘。

-   選取時間來源。

-   通知媒體接收時鐘

-   視需要啟動、停止和暫停時鐘。

-   關閉時鐘。

若要取得簡報時鐘的指標，請在媒體會話上呼叫 [**IMFMediaSession：： GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) 。 簡報時鐘不會傳回有效的時間，直到媒體會話以 MF [](mesessiontopologystatus.md) \_ TOPOSTATUS READY 旗標傳送 MESessionTopologyStatus 事件為止 \_ 。 在那之前， **GetClock** 會傳回 MF \_ E \_ 時鐘 \_ NO \_ TIME \_ SOURCE。

使用媒體會話的應用程式應該永遠不會啟動、停止或暫停簡報時鐘;變更頻率率;或關閉時鐘。

當應用程式呼叫 [**IMFMediaSession：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)時，媒體會話會啟動簡報時鐘，其開始時間等於 **Start** 方法中指定的起始位置。 如需媒體會話的詳細資訊，請參閱 [媒體會話](media-session.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體會話](media-session.md)
</dt> </dl>

 

 



