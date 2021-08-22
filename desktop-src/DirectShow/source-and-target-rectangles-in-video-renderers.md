---
description: 影片轉譯器中的來源和目標矩形
ms.assetid: fdddbffb-c44f-4364-9e2e-b721ba39c74f
title: 影片轉譯器中的來源和目標矩形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020be0786a071c6bbdf33649405517ed3788789268052b61ee89d97a23f357f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072542"
---
# <a name="source-and-target-rectangles-in-video-renderers"></a>影片轉譯器中的來源和目標矩形

影片媒體類型的 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)、 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)和 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式結構中有三種大小。 本文將說明它們是什麼，以及它們的運作方式。

首先，這些結構的 **bmiHeader** 成員會有大小。 **BmiHeader** 成員是具有自己的寬度和高度成員（ **bmiHeader. biWidth** 和 **BmiHeader. biHeight**）的 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構。

其次，這些結構的 **rcSource** 成員中有一個矩形;最後，這些結構的 **rcTarget** 成員中有一個矩形。

假設您有兩個篩選器，A 和 B，這些篩選器會彼此連接 (左邊、上游、右邊的 B，或具有特定影片媒體類型的下游) 。

在篩選 A 和 B 之間傳遞的緩衝區大小 (**bmiHeader. biWidth**、 **bmiHeader. biHeight**) 。 篩選 A 應該採用 **rcSource** 決定的部分輸入影片，並延展該影片以填滿緩衝區的 **rcTarget** 部分。 所要使用之輸入影片的部分是根據 **rcSource** 與 (**biWidth** 的比較方式，也就是篩選 A 和 B 原本連接的媒體類型的 **biHeight**) 大小。 如果 **rcSource** 是空的，則篩選 A 會使用其整個輸入影片。 如果 **rcTarget** 是空的，則篩選會填滿整個輸出緩衝區。

例如，假設篩選 A 正在接收 160 x 120 圖元的影片資料。 也假設篩選 A 使用下列媒體類型連接至篩選 B。

-    (**biWidth**、 **biHeight**) ：320、240
-   **rcSource**： (0、0、0、0) 
-   **rcTarget**： (0、0、0、0) 

這表示篩選 A 會以 x 和 y 方向的2來延展所收到的影片，並填滿 320 x 240 輸出緩衝區。

另一個範例是，假設篩選 A 正在接收 160 x 120 video 資料，而且它是以下列媒體類型連接至篩選 B。

-    (**biWidth**、 **biHeight**) ：320、240
-   **rcSource**： (0、0、160、240) 
-   **rcTarget**： (0、0、0、0) 

**RcSource** 成員相對於連接的緩衝區大小320，240。 因為指定的 **rcSource** (0，0、160、240) 是緩衝區的左邊半部，篩選 A 會採用其輸入影片的左邊半部，或 (0、0、80、120) 部分，並將影片延展至 (320、240)  (x 方向的4，以及 y 方向的2，) 並填滿 320 x 240 輸出緩衝區。

現在假設篩選 A 呼叫 [**CBaseAllocator：： GetBuffer**](cbaseallocator-getbuffer.md)，且傳回的媒體範例有附加的媒體類型，表示篩選 B 希望篩選 a 提供不同于先前提供的大小或影片類型。 假設新的媒體類型為：

-    (**biWidth**、 **biHeight**) ：640、480
-   **rcSource**： (0、0、160、120) 
-   **rcTarget**： (0、0、80、60) 

這表示媒體範例有一個大小為 640 x 480 的緩衝區。 **RcSource** 成員相對於原始的連線媒體類型 (320、240) 不 (640、480) 的新媒體類型，因此 **rcSource** 指定要使用輸入影片的左上角 (25% ) 。 這部分的輸入影片會置於左上角 (80、60) 圖元（640 x 480 輸出緩衝區），如 (0、0、80、60) 的 **rcTarget** 所指定。 由於篩選 A 會接收 160 x 120 影片，因此輸入影片的左上角是 (80、60) 片段、相同大小的輸出點陣圖，且不需要延展。

篩選準則將不會在輸出緩衝區的其他圖元內放置任何資料，而且不會讓這些位保持不變。 **RcSource** 成員系結于篩選 A 和 B 之間原始連線媒體類型的 **biWidth** 和 **biHeight** ，而 **rcTarget** 則是由媒體範例的新 **biWidth** 和 **biHeight** 所限制。 在上述範例中， **rcSource** 無法超出 (0、0、320、240) 的界限，而且 **rcTarget** 無法超出 (0、0、640、480) 的範圍。

 

 



