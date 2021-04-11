---
description: Advanced Capture 主題
ms.assetid: 407702b2-5f4f-424d-a3ec-b0473e1b0da3
title: Advanced Capture 主題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c4e5a077f6f8b17543250efa0f10091f0917e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109545"
---
# <a name="advanced-capture-topics"></a>Advanced Capture 主題

本節說明 DirectShow 中影片捕獲的一些先進層面。 本節所述的大部分問題都會由 [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) 介面自動處理。 但是，如果您需要針對影片捕獲應用程式進行疑難排解，這裡的資訊可能會很有用。 如果您的應用程式建立某種自訂的捕獲圖形，而且您發現 ICaptureGraphBuilder2 不符合您的需求，也應該閱讀本節。 最後，本節包含一些有關在影片捕獲應用程式中使用影片混合轉譯器 (VMR) 篩選的資訊。

您可以使用 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) 方法，完全建立影片捕獲圖形。 您也可以結合這兩個介面，並使用 ICaptureGraphBuilder2 進行某些工作，並 IGraphBuilder 其他專案。

本節包含下列主題：

-   [處理影片捕獲中的重新繪製事件](handling-repaint-events-in-video-capture.md)
-   [使用 Pin 類別](working-with-pin-categories.md)
-   [使用智慧的 t a 濾波器](using-the-smart-tee-filter.md)
-   [使用影片捕獲中的重迭混音器](using-the-overlay-mixer-in-video-capture.md)
-   [影片埠釘選](video-port-pins.md)
-   [VideoInfo2 格式類型](videoinfo2-format-type.md)
-   [建立 Kernel-Mode 篩選](creating-kernel-mode-filters.md)
-   [WDM 類別驅動程式篩選](wdm-class-driver-filters.md)
-   [在 DirectShow 中使用 WDDM Capture](using-wddm-capture-in-directshow.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影片捕獲](video-capture.md)
</dt> </dl>

 

 



