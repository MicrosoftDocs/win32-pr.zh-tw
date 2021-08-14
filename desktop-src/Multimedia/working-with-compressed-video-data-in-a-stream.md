---
title: 在資料流程中使用壓縮的影片資料
description: 在資料流程中使用壓縮的影片資料
ms.assetid: b701e072-f162-438f-b607-aea7491a02f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7c09de239fa28f3d9739dafc953ce10c2a6f1d69c0c607aeb03bc388a0f3003
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622088"
---
# <a name="working-with-compressed-video-data-in-a-stream"></a>在資料流程中使用壓縮的影片資料

AVIFile 提供數種方式讓您存取壓縮的影片串流。

如果您想要顯示一或多個已壓縮影片資料流程的框架，您可以使用 [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) 函式來取出框架，然後將壓縮的框架資料轉送至 DrawDib 函式來顯示它們。 DrawDib 函式可以顯示數個影像深度的影像，並自動顯示無法處理特定類型的裝置獨立點陣圖 (Dib) 的顯示器影像。 這些函式適用于未壓縮和壓縮的影像。 如需 DrawDib 函數的詳細資訊，請參閱 [DrawDib 函數](drawdib-functions.md)。

AVIFile 提供可解壓縮單一影片框架的函式。 若要配置資源，請使用 [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) 函數。 此函數會建立解壓縮資料的緩衝區。

您可以使用 [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) 函式來解壓縮單一的影片畫面。 此函式會將框架解壓縮，並抓取影像資料的完整框架，以傳回 [BITMAPINFOHEADER](/previous-versions//ms532290(v=vs.85)) 結構中的 DIB 位址。 您的應用程式可以使用標準繪圖函數或使用 DrawDib 函式來顯示 DIB。

如果您的應用程式會連續呼叫 **AVIStreamGetFrame**，函式會將每個抓取的框架覆寫緩衝區。

當您完成使用 **AVIStreamGetFrame** ，且解壓縮的 DIB 位於其緩衝區時，您可以使用 [**AVIStreamGetFrameClose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose) 函數來釋放已配置的資源。

如需解壓縮影像的詳細資訊，請參閱 [影片壓縮管理員](video-compression-manager.md)。

 

 