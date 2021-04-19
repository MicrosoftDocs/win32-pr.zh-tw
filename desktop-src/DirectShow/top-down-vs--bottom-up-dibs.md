---
description: Top-Down 與
ms.assetid: c292f145-f385-4f18-8f98-e414d86860e2
title: Top-Down 與 Bottom-Up Dib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e719bea5923aeccc4a0a92b5f73a253e13d2e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106969403"
---
# <a name="top-down-vs-bottom-up-dibs"></a>Top-Down 與 Bottom-Up Dib

如果您不熟悉圖形程式設計，您可能會預期點陣圖會排列在記憶體中，讓影像的頂端列出現在緩衝區的開頭，後面接著下一個資料列等等。 不過，這不一定是如此。 在 Windows 中，與裝置無關的點陣圖 (Dib) 可以放在記憶體中，以兩種不同的方向（上下排列）。

在下一個 DIB 中，影像緩衝區是以圖元的底部列開始，後面接著下一個資料列，依此類推。 影像的頂端資料列是緩衝區中的最後一個資料列。 因此，記憶體中的第一個位元組是影像的左下角圖元。 在 GDI 中，所有 Dib 都是自下而上的。 下圖顯示最下層 DIB 的實體版面配置。

![右下角的 dib](images/pixel-layout-bottomup.png)

在由上而下的 DIB 中，資料列的順序會反轉。 影像的頂端資料列是記憶體中的第一個資料列，後面接著下一個資料列。 影像的底部資料列是緩衝區中的最後一個資料列。 使用由上而下的 DIB 時，記憶體中的第一個位元組是影像的左上角圖元。 DirectDraw 使用由上而下的 Dib。 下圖顯示由上而下 DIB 的實體版面配置：

![由上而下的 dib](images/pixel-layout-topdown.png)

若為 RGB Dib，影像方向會以 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構的 **biHeight** 成員來表示。 如果 **biHeight** 是正面的，則影像會靠下。 如果 **biHeight** 為負數，則影像會由上而下。

YUV 格式的 Dib 一律會由上而下，而且會忽略 **biHeight** 成員的正負號。 您應以正面的 **biHeight** 提供 yuv 格式，但它們也應接受具有負面 **biHeight** 的 yuv 格式並忽略符號。

此外，任何在 **biCompression** 成員中使用 **FOURCC** 的 DIB 型別，都應該將其 **biHeight** 表達為正數，無論其方向為何，因為 **FOURCC** 本身會識別其影像方向應該由任何相容的篩選器瞭解的壓縮配置。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用影片畫面](working-with-video-frames.md)
</dt> </dl>

 

 



