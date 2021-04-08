---
title: 關於 DrawDib 函式
description: 關於 DrawDib 函式
ms.assetid: 0ae993df-8393-479e-aa11-14301384715d
keywords:
- Windows (VFW) 的影片，DrawDib
- 適用于 Windows) 的 VFW (影片，DrawDib
- DrawDib，關於
- DrawDib，色彩表
- DrawDib，傳輸模式
- DrawDib，顯示介面卡
- DrawDib，影像延展
- DrawDib，壓縮的影像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238f3e9ba822e16a7568775378b24f69bbca12de
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682109"
---
# <a name="about-the-drawdib-functions"></a>關於 DrawDib 函式

DrawDib 函式統稱為 [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) 函式，其提供影像延展和遞色功能。 不過，DrawDib 函式支援影像解壓縮、資料串流，以及更多的顯示器介面卡數目。

在某些情況下，您會發現使用 DrawDib 函式很有説明。 但是， [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) 的多樣性比 DrawDib 函式更多樣化，當 DrawDib 函式無法提供所需的功能時，就應該使用這些功能。 下列清單描述在決定是否要使用 DrawDib 函式或 **StretchDIBits** 時要考慮的因素。

-   色彩資料表資訊格式。 DrawDib 函式會顯示在色彩表中使用 **DIB \_ RGB \_ 色彩** 格式的影像。 如果您應用程式中的影像儲存具有 **DIB \_ pal \_ 色彩** 或 **dib \_ pal \_ 索引** 格式的色彩表資訊，您就必須使用 [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) 來顯示它們。
-   傳輸模式。 DrawDib 函式要求您的應用程式必須使用 **SRCCOPY** 傳輸模式。 如果您的應用程式使用 [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) 搭配 **SRCCOPY** 以外的傳輸模式，您應該繼續使用 **StretchDIBits**。 同樣地，如果您需要在應用程式中使用其他的點陣作業（例如 XOR），請使用 **StretchDIBits**。
-   影片和動畫播放的品質。 您可以針對資料串流應用程式使用 DrawDib 函式，例如播放影片剪輯和動畫順序的函式。 DrawDib 函式優於 [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) ，因為它們提供了較高品質的影像，並改善播放期間的動作。
-   顯示介面卡。 DrawDib 函式支援的顯示器介面卡數目超過 [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) 支援的數目。 DrawDib 函式支援使用4位影像深度提供16色調色板的 VGA 色器、使用8位影像深度提供256色調色板的 SVGA 介面卡，以及使用16位、24位和32位影像深度提供數千種色彩的純色顯示器介面卡。

    DrawDib 函式也可改善在具有更多功能的顯示器介面卡上顯示影像的速度和品質。 例如，在使用8位的顯示器介面卡時，DrawDib 函式會有效率地將真色彩影像遞色至256色彩。 它們也會在使用4位顯示介面卡時，將8位影像遞色。

-   影像延展。 如同 [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits)，DrawDib 函式會使用來源和目的地矩形來控制顯示之影像的部分。 您可以藉由改變來源和目的地矩形的位置和大小，來裁剪影像的不必要部分或延展影像。 如果顯示驅動程式不支援影像延展，DrawDib 函式會提供比 **StretchDIBits** 更有效率的延展功能。
-   壓縮的影像。 DrawDib 函式會繪製您有解壓縮程式的任何格式，包括執行長度的編碼 (RLE) 、Cinepak 和 411 YUV。 Windows 包含可選擇性安裝的 RLE 和 Cinepak decompressors。
-   Windows 不再支援 Indeo 編解碼器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DrawDib](drawdib.md)
</dt> </dl>

 

 