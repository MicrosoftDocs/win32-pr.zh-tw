---
title: 影像轉譯
description: 影像轉譯
ms.assetid: de87f288-f1bd-471c-b594-e9dbde3cff0a
keywords:
- DrawDib，影像轉譯
- DrawDib，繪圖 Dib
- DrawDibDraw 函式
- DrawDibGetBuffer 函式
- DrawDibUpdate 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7be73fbe37a28ab44116d2fb2e68acb6a9a3a385603af23dca0e14aa2de4d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690748"
---
# <a name="image-rendering"></a>影像轉譯

在您呼叫 [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) 來建立 DrawDib DC (請參閱 [DrawDib 作業](drawdib-operations.md)) ，您可以使用 [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) 函式在畫面上繪製一個 DIB。 **DrawDibDraw** dithers 真色彩點陣圖，以8位的顯示器介面卡顯示。

[**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) 也支援在顯示壓縮點陣圖時透明地壓縮機影片。 您可以使用 [**DrawDibGetBuffer**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) 函式來存取包含解壓縮映射的緩衝區。 繪製未壓縮的點陣圖時， **DrawDibGetBuffer** 會傳回 **Null** 。 您應該準備您的應用程式來處理壓縮和未壓縮的點陣圖。

您可以使用 [**DrawDibUpdate**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate) 宏，重新整理應用程式所顯示的影像或部分影像。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 DrawDib 函式](about-the-drawdib-functions.md)
</dt> </dl>

 

 




