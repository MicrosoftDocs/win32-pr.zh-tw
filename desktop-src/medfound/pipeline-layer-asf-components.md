---
description: 在媒體基礎管線模型中，媒體來源會連接到與媒體接收器進一步連線的轉換。
ms.assetid: 55ab3a53-d9fd-438c-998c-8888f99958ce
title: 管線層 ASF 元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3b6eb2d00404d193e50cebf174210a1c25655e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993018"
---
# <a name="pipeline-layer-asf-components"></a>管線層 ASF 元件

在媒體基礎的管線模型中，媒體來源會連接到與媒體接收器進一步連線的轉換。 來源中包含的資料會流經轉換，並在接收中產生輸出媒體範例，以供播放或編碼之用。 視應用程式是否想要播放 ASF 內容或編碼為 ASF 檔案而定，應用程式必須以不同的方式建立管線。

下列主題包含管線層元件的相關資訊。

-   [ASF 媒體來源](asf-media-source.md)
-   [Windows Media 編碼器](windows-media-encoders.md)
-   [ASF 媒體接收](asf-media-sinks.md)

用於播放之 ASF 管線的三個主要元件如下：

-   ASF 媒體來源是由代表 ASF 檔案媒體基礎提供。
-   音訊 resamplers、影片影像 resizers 等， (轉換) 
-   音訊和影片轉譯器 (接收器) 

如需建立播放管線的詳細資訊，請參閱建立 [播放拓撲](creating-playback-topologies.md)。

適用于編碼的 ASF 管線的三個主要元件如下：

-   媒體來源，代表需要轉換之格式的資料。 此元件可以是媒體基礎所提供的其中一個預設媒體來源，或是公開 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 介面的自訂來源。
-   Windows Media 編碼器 (轉換) ，以執行格式轉換。
-   由媒體基礎提供的 ASF 媒體接收器，會在應用程式指定的輸出檔中寫入 ASF 物件和媒體範例。

管線會在拓撲中表示，而管線中的每個物件會以拓撲節點表示。 針對播放和編碼，所有的管線作業都是由媒體會話處理。 媒體會話的職責之一，就是要確保管線具有產生輸出所需的所有元件。 例如，在編碼管線中，如果音訊來源格式與目標格式不同，則媒體會話會插入其他轉換元件，例如執行適當取樣速率轉換的 resampler。 透過管線的資料流程控制也會由媒體會話管理。 在播放案例中，啟動媒體會話時，媒體會話會將範例傳送給 SAR 和 EVR，並將其呈現在輸出裝置上。 針對編碼，啟動媒體會話會開始編碼程式。 當編碼完成時，會話會以非同步方式通知應用程式。

下列主題包含有關使用管線層元件建立編碼拓撲的逐步指示。 用來讀取和寫入 ASF 檔案的元件。

-   [教學課程： 1-傳遞 Windows Media 編碼](tutorial--1-pass-windows-media-encoding.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎中的 ASF 支援](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



