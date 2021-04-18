---
title: 影像的順序
description: 影像的順序
ms.assetid: fbfb944c-a927-4c92-b3d6-2f8c278408e6
keywords:
- DrawDib，映射序列
- DrawDib，點陣圖順序
- DrawDibDraw 函式
- DrawDibBegin 函式
- DrawDibEnd 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a7ae2c85d62e93e4149518221aa520eabe13ee2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968490"
---
# <a name="sequences-of-images"></a>影像的順序

您可以搭配使用 [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) 函式和 [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) 函式，以顯示具有相同維度和格式的一系列點陣圖。 **DrawDibBegin** 藉由準備 DrawDib DC 來進行繪製，以改善 **DrawDibDraw** 的效率。

> [!Note]  
> 如果您的應用程式不使用 [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)， [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) 會在繪製之前隱含地執行。 如果您的應用程式在 **DrawDibDraw** 之前使用 **DrawDibBegin** ， **DrawDibDraw** 就不需要處理函式並等候它完成。

 

[**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)函式會為 [**DRAWDIBDRAW**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw)提供 DrawDib DC、DC 控制碼、 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構的位址，以及來源和目的地矩形維度。 當您顯示一系列的點陣圖時， **DrawDibDraw** 會針對序列中的每個影像檢查這些專案的值。 如果 **DrawDibDraw** 偵測到任何這些專案的變更，它會隱含地再次呼叫 **DrawDibBegin** 來調整 DrawDib DC 設定。

使用 [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)之後，您可以使用 [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) 並適當地指定一或多個旗標，以繪製影像順序。 指定 **DDF \_ 相同的 \_ HDC** 旗標，但 DC 控制碼未變更。 \_ \_ 當下列 **DrawDibDraw** 參數未變更時，請指定 DDF 相同的繪圖旗標： [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構的位址和來源和目的矩形維度。

您可以使用 [**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend)函數，然後再呼叫 **DrawDibBegin**，以更新使用 [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)設定的旗標。 然後使用 **DrawDibEnd** 清除其目前旗標和設定的 DrawDib DC。 後續的 **DrawDibBegin** 呼叫會重新初始化具有適當旗標和設定的 DrawDib DC。 或者，您可以使用 **DrawDibBegin** 而不 **DrawDibEnd** 來更新 DrawDib DC 的旗標。 若要這樣做，您必須同時變更下列其中一項設定： [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構的位址，或是來源或目的矩形維度。

您可以使用 [**DrawDibStart**](/windows/desktop/api/Vfw/nf-vfw-drawdibstart)和 [**DrawDibStop**](/windows/desktop/api/Vfw/nf-vfw-drawdibstop)函式，來提高使用壓縮影像（例如播放影片剪輯）之資料串流作業的 [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw)效率。 **DrawDibStart** 函式會將訊息傳送至視訊壓縮管理員 (bc-vcm-lvm-hyperv) ，以準備 DrawDib DC 以接收影像的資料流程。 當串流結束時， **DrawDibStop** 會將訊息傳送至 bc-vcm-lvm-hyperv，指出它可以釋放為數據串流作業所配置的資源。 如需 BC-VCM-LVM-HYPERV 的詳細資訊，請參閱 [影片壓縮管理員](video-compression-manager.md)。

> [!Note]  
> 您必須在應用程式中指定來源和目的地矩形的寬度和高度。 不過，您不需要指定矩形的來源。 您的應用程式可以在 [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) 中重新定義來源，以使用影像的不同部分或更新顯示的不同部分。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影像轉譯](image-rendering.md)
</dt> </dl>

 

 