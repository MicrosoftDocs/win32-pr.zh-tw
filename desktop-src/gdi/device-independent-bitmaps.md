---
description: 與裝置無關的點陣圖 (DIB) 包含色彩表。
ms.assetid: 56b39a3d-48a4-4620-9652-ec41ea4d6423
title: Device-Independent 點陣圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a6672857aadda714e7016616ca78654d7da102b48c1229c5b322953fc716f5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761387"
---
# <a name="device-independent-bitmaps"></a>Device-Independent 點陣圖

與裝置無關的點陣圖 (DIB) 包含 *色彩表*。 色彩表描述圖元值對應至 *RGB* 色彩值的方式，這些值會描述發出光線所產生的色彩。 因此，DIB 可以在任何裝置上達到適當的色彩配置。 DIB 包含下列色彩和維度資訊：

-   建立矩形影像之裝置的色彩格式。
-   矩形映射建立所在裝置的解析度。
-   建立映射之裝置的 [選擇區]。
-   將紅色、綠色、藍色 ( [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) ) triplet 對應至矩形影像中圖元的位陣列。
-   資料壓縮識別碼，指出資料壓縮配置 (是否有任何) 用來縮減位陣列的大小。

色彩和維度資訊儲存在 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) 結構中，其中包含 [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) 結構，後面接著兩個或多個 [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) 結構。 **BITMAPINFOHEADER** 結構會指定圖元矩形的維度、描述裝置的色彩技術，並識別用來縮減點陣圖大小的壓縮配置。 **RGBQUAD** 結構會識別出現在圖元矩形中的色彩。

Dib 有兩種：

-   由上而下的 DIB，來源位於左下角。
-   由上而下的 DIB，其原點位於左上角。

如果 DIB 的高度是由點陣圖資訊標頭結構的 **高度** 成員所表示，則是由上而下的 dib;如果高度是負值，則是由上而下的 DIB。 無法壓縮由上而下的 Dib。

色彩格式是根據色彩平面和色彩位的計數來指定。 色彩平面的計數一律為 1;針對單色點陣圖，色彩位的計數是1，而針對 VGA 點陣圖則為4，而在其他色彩裝置上則為點陣圖的8、16、24或32。 應用程式會藉由呼叫 [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 函式，並將 BITSPIXEL 指定為第二個引數，來抓取特定顯示器 (或印表機) 使用的色彩位數目。

顯示裝置的解析度是以每個計量的圖元為單位來指定。 應用程式可透過下列三個步驟的程式，取得影片顯示器或印表機的水準解析度。

1.  呼叫 [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 函數，並將 HORZRES 指定為第二個引數。
2.  第二次呼叫 [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) ，將 HORZSIZE 指定為第二個引數。
3.  將第一個傳回值除以第二個傳回值。

應用程式可以使用相同的三步驟程式搭配不同的參數來取得垂直解析度： VERTRES 取代 HORZRES，而 VERTSIZE 用來取代 HORZSIZE。

此調色板是以 [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) 結構的陣列來表示，以針對顯示裝置的色彩選擇區中的每個色彩指定紅色、綠色和藍色強度的元件。 選擇區陣列中的每個色彩索引都會對應到與點陣圖相關聯之矩形區域中的特定圖元。 這個陣列的大小（以位為單位）相當於矩形的寬度（以圖元為單位），乘以矩形的高度（以圖元為單位）乘以裝置的色彩位元數目。 應用程式可以藉由呼叫 [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 函式，並將 NUMCOLORS 指定為第二個引數，來取得裝置的調色板大小。

Windows 支援壓縮適用于 8 bpp 和 4 bpp 底部 dib 的調色板陣列。 您可以使用執行長度編碼 (RLE) 配置來壓縮這些陣列。 RLE 配置使用2個位元組的值，第一個位元組指定使用色彩索引的連續圖元數，以及指定索引的第二個位元組。 如需點陣圖壓縮的詳細資訊，請參閱 [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))、 [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader)、 [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)和 [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) 結構的描述。

應用程式可以藉由初始化所需的結構和呼叫 [**GetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits) 函式，從 DDB 建立 DIB。 若要判斷裝置是否支援此函式，請呼叫 [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 函式， \_ \_ 並將 RC DI 點陣圖指定為 RASTERCAPS 旗標。

需要複製點陣圖的應用程式可以使用 [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt) 將來源點陣圖中的所有圖元複製到目的地點陣圖，但是符合透明色彩的圖元除外。

應用程式可以藉由呼叫 [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) 或 [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) 函式，使用 DIB 來設定顯示裝置上的圖元。 若要判斷裝置是否支援 **SetDIBitsToDevice** 函式，請呼叫 [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 函式， \_ 並將 RC DIBTODEV 指定為 RASTERCAPS 旗標。 將 RC \_ STRETCHDIB 指定為 RASTERCAPS 旗標，以判斷裝置是否支援 **StretchDIBits**。

只需要顯示預先存在的 DIB 的應用程式可以使用 [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) 函數。 例如，試算表應用程式可以開啟現有的圖表，並使用 **SetDIBitsToDevice** 函式將它們顯示在視窗中。 不過，若要在視窗中重複重繪點陣圖，應用程式應該使用 [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) 函數。 例如，結合動畫圖形與音效的多媒體應用程式，因為其執行速度比 **SetDIBitsToDevice** 更快，所以會受益于呼叫 **BitBlt** 函數。

 

 
