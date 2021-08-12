---
description: 在影片捕獲中使用重迭 Mixer
ms.assetid: 43468fa2-6dea-439d-9e24-f47a053ad561
title: 在影片捕獲中使用重迭 Mixer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134ada11ca55009b3ad67ba80c82575ab2d9bdf5a7329a88157ed4e003eca74c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651192"
---
# <a name="using-the-overlay-mixer-in-video-capture"></a>在影片捕獲中使用重迭 Mixer

[影片](video-renderer-filter.md)轉譯器篩選器本身無法顯示特定類型的影片。 在這些情況下，影片轉譯器必須與覆迭[Mixer](overlay-mixer-filter.md)篩選器搭配運作。 重迭 Mixer 會管理轉譯，而影片轉譯器則會管理影片視窗。 在下列情況下，需要重迭 Mixer：

-   影片埠 (VP) 圖釘。 如果捕捉裝置使用影片埠，重迭 Mixer 會管理硬體重迭。
-   交錯式影片。 針對交錯式影片，此解碼器需要影片轉譯器不支援的 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式。
-   隱藏式輔助字幕。 標題文字會轉譯為每圖元8位的點陣圖，而重迭 Mixer 重迭顯示在影片上。

Capture Graph Builder 的 **RenderStream** 方法會在每次需要時插入重迭 Mixer。 但是，如果您要在不使用 Capture Graph 產生器的情況下建立圖形，您必須檢查每一種情況，並 Mixer 自己插入重迭。

-   \[!重要\]  
    > 如果裝置有 VP 釘選，您必須連接重迭 Mixer，即使您的應用程式中不需要預覽功能也一樣。 使用影片埠時，capture 裝置一律會將影片資料傳送至硬體重迭，因此一律需要重迭 Mixer。

     

影片混合轉譯器篩選器 (VMR-7 和 VMR-9) 兩者都支援交錯式影片，而且能夠將隱藏式輔助字幕點陣圖混合到主要影片上。 如果您在這些案例中使用 VMR，則不需要使用覆迭 Mixer。 VMR-9 不支援副總 pin 連接。 VMR-7 透過「影片埠管理員」篩選器支援副總 pin 連接。 不過，您可能會發現某些驅動程式無法與影片埠管理員正常搭配運作。 基於這個理由，仍建議將重迭 Mixer 用於 VP 的 pin。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Advanced Capture 主題](advanced-capture-topics.md)
</dt> <dt>

[影片埠釘選](video-port-pins.md)
</dt> <dt>

[VideoInfo2 格式類型](videoinfo2-format-type.md)
</dt> </dl>

 

 



