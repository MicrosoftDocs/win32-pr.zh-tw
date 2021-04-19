---
description: 使用 EVR 媒體接收
ms.assetid: cd98266a-bc62-43da-b4d7-3561447d634f
title: 使用 EVR 媒體接收
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84f8c666e88b495ad2d2e53fb1de10364f91636f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106985515"
---
# <a name="using-the-evr-media-sink"></a>使用 EVR 媒體接收

增強型影片轉譯器 (EVR) 媒體接收器可作為獨立元件使用。 但是，應用程式通常會在拓撲內建立 EVR 媒體接收器，然後使用媒體會話來控制播放。

有兩種方式可以建立 EVR 媒體接收器：

-   [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer)函式會建立媒體接收器。

-   [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate)函式會建立媒體接收器的啟用物件。

EVR 媒體接收器一開始會有一個對應至參考資料流的資料流程接收。 若要加入新的資料流程接收，請呼叫 [**IMFMediaSink：： AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[增強的影片轉譯器](enhanced-video-renderer.md)
</dt> <dt>

[媒體接收器](media-sinks.md)
</dt> </dl>

 

 



