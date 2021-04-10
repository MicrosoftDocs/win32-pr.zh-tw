---
description: 使用影片捕獲中的重迭混音器
ms.assetid: 43468fa2-6dea-439d-9e24-f47a053ad561
title: 使用影片捕獲中的重迭混音器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bff115d566654732e80c0bcb0f554c4ad96e65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027047"
---
# <a name="using-the-overlay-mixer-in-video-capture"></a>使用影片捕獲中的重迭混音器

[影片](video-renderer-filter.md)轉譯器篩選器本身無法顯示特定類型的影片。 在這些情況下，影片轉譯器必須搭配覆迭 [混音](overlay-mixer-filter.md) 器篩選器來使用。 重迭混音器會管理轉譯，而影片轉譯器則會管理影片視窗。 在下列情況下，需要重迭混音器：

-   影片埠 (VP) 圖釘。 如果捕捉裝置使用影片埠，重迭混音器會管理硬體重迭。
-   交錯式影片。 針對交錯式影片，此解碼器需要影片轉譯器不支援的 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式。
-   隱藏式輔助字幕。 標題文字會轉譯為每圖元8位的點陣圖，而重迭混音器會在影片上重迭。

「捕獲圖形產生器」的 **RenderStream** 方法會在每次需要時插入重迭混音器。 但是，如果您要在不使用 [Capture Graph Builder] 的情況下建立圖形，則必須檢查每一種情況，並自行插入重迭混音器。

-   \[!重要\]  
    > 如果裝置有 VP 釘選，即使您的應用程式中不需要預覽功能，您還是必須連接重迭混音器。 使用影片埠時，capture 裝置一律會將影片資料傳送至硬體重迭，因此一律需要重迭混音器。

     

影片混合轉譯器篩選器 (VMR-7 和 VMR-9) 兩者都支援交錯式影片，而且能夠將隱藏式輔助字幕點陣圖混合到主要影片上。 如果您在這些案例中使用 VMR，則不需要使用重迭混音器。 VMR-9 不支援副總 pin 連接。 VMR-7 透過「影片埠管理員」篩選器支援副總 pin 連接。 不過，您可能會發現某些驅動程式無法與影片埠管理員正常搭配運作。 基於這個理由，仍建議將重迭混音器用於 VP 圖釘。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Advanced Capture 主題](advanced-capture-topics.md)
</dt> <dt>

[影片埠釘選](video-port-pins.md)
</dt> <dt>

[VideoInfo2 格式類型](videoinfo2-format-type.md)
</dt> </dl>

 

 



