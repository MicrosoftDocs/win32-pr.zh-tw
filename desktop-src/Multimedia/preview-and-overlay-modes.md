---
title: 預覽和重迭模式
description: 預覽和重迭模式
ms.assetid: 11e7848f-efda-452c-a9c7-405e636a2ead
keywords:
- WM_CAP_SET_PREVIEW 訊息
- capPreview 宏
- WM_CAP_SET_PREVIEWRATE 訊息
- capPreviewRate 宏
- WM_CAP_SET_SCALE 訊息
- capPreviewScale 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9359b1380c5d6efe049bc4bea52a08a92f880af5d35558f4e65e21070f20c0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372367"
---
# <a name="preview-and-overlay-modes"></a>預覽和重迭模式

Capture 驅動程式可執行兩種方法來觀看內送影片串流：預覽模式和重迭模式。 如果捕捉驅動程式同時執行這兩種方法，則使用者可以選擇要使用的方法。

[預覽] 模式會將數位化的框架從捕獲硬體傳輸到系統記憶體，然後使用圖形裝置介面 (GDI) 函式，在 [捕捉] 視窗中顯示數位化的框架。 當父視窗失去焦點時，應用程式可能會降低預覽率，並在父視窗取得焦點時增加預覽率。 此動作可改善一般系統回應性，因為預覽作業需要大量處理器。

有三個訊息可控制預覽作業。

-   若要啟用或停用 [預覽] 模式，請 [**透過將 (\_ \_ \_**](wm-cap-set-preview.md) 或 [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) 宏) 傳送至 [捕獲] 視窗。
-   使用 [**WM \_ CAP \_ SET \_ PREVIEWRATE**](wm-cap-set-previewrate.md) message (或 [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) 宏) 來設定在預覽模式中顯示畫面格的速率
-   使用「 [**WM \_ CAP \_ 集 \_ 調整**](wm-cap-set-scale.md) 訊息 (或 [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) 宏) 來啟用或停用預覽版影片的縮放。

如果同時啟用預覽和調整，則會將捕獲的影片畫面延展至 [捕捉] 視窗的維度。 啟用預覽模式會自動停用覆迭模式。

覆迭模式是一種硬體功能，會在不使用 CPU 資源的情況下，顯示監視器上的擷取緩衝區內容。 您可以藉由將 [**WM \_ CAP \_ 集合 \_**](wm-cap-set-overlay.md) 重迭訊息 (或 [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) 宏) 傳送至 [捕獲] 視窗，來啟用和停用覆迭模式。 啟用覆迭模式會自動停用預覽模式。

您也可以在 [預覽] 模式或 [覆迭模式] 的 [捕捉] 視窗的工作區中，將 [ [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos)宏) 傳送至 [捕獲] 視窗，以設定影片框架的滾動 [**(條位置 \_ \_ \_**](wm-cap-set-scroll.md) 。

 

 




