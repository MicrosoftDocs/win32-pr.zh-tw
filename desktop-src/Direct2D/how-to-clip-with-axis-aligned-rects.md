---
title: 如何使用 Axis-Aligned 剪切矩形裁剪
description: 顯示如何使用軸對齊的剪輯矩形來裁剪區域。
ms.assetid: 4196653a-9177-4a41-9db9-4738a41313aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f666bac88d93cb8ea0f27bfb9c2d5b14975e0dc8bb67aba4f0e767178f6ebddc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569310"
---
# <a name="how-to-clip-with-an-axis-aligned-clip-rectangle"></a>如何使用 Axis-Aligned 剪切矩形裁剪

本主題說明如何使用軸對齊的剪輯矩形來裁剪影像。 這種方法只會產生矩形剪輯，因為內容界限會對齊矩形的座標軸。 這種方法比使用具有內容界限的圖層更有效率。 如需詳細資訊，請參閱[圖層總覽](direct2d-layers-overview.md)。

**若要使用軸對齊的剪輯矩形進行裁剪**

1.  從資源載入原始映射。 如需有關如何載入點陣圖的詳細資訊，請參閱 [如何從資源載入點陣圖](how-to-load-a-bitmap-from-a-resource.md)。
2.  呼叫 [**ID2D1RenderTarget：:P ushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) 來指定矩形。 轉譯命令會裁剪至矩形。

3.  小畫家原始影像。
4.  呼叫 [**ID2D1RenderTarget：:P opaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) ，從轉譯目標中移除最後一個軸對齊的剪輯。

例如，在下圖中，左邊的原始點陣圖是 200 \* 130 圖元。 右邊的點陣圖是裁剪成軸對齊剪切矩形的原始點陣圖。 維度 (20，20) 至 (100，100) 。

![裁剪點陣圖前後的金魚點陣圖圖例](images/cliparegion-axisalignedclip.png)

若要建立裁剪的影像，請建立矩形結構作為裁剪區域。 使用裁剪區域來呼叫 [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) ，並繪製原始影像。 呼叫 [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) 以從轉譯目標中移除剪輯。 下列程式碼示範如何執行這項操作。


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct2D 參考](reference.md)
</dt> </dl>

 

 