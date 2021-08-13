---
title: 互通性概觀
description: 摘要說明您可以搭配 Direct2D 使用的各種技術。
ms.assetid: 41f3b908-d218-4a47-bfc3-6a37d38ca26a
keywords:
- Direct2D，GDI 交互操作
- Direct2D，GDI+ 交互操作
- Direct2D，互通性
- Direct2D，DirectWrite 交互操作
- 互通性，Direct2D
- 互通性，Direct3D
- '圖形裝置介面 (GDI) '
- 'GDI (圖形裝置介面) '
- '互通性、圖形裝置介面 (GDI) '
- 互通性，GDI+
- DirectWrite 互通性
- 互通性，DirectWrite
- Windows 影像處理元件 (WIC)
- 'WIC (Windows 影像處理元件) '
- '互通性，Windows 影像處理元件 (WIC) '
- Direct2D，WIC 互通性
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 35567b461815d28a5fc00b2cc4049f5c81b61c6e8030f477e93efbc8a5d580e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119385320"
---
# <a name="interoperability-overview"></a>互通性概觀

Direct2d 的主要功能之一，是讓 Direct2D 和其他轉譯平臺之間的互通性，讓開發人員可以選擇一種平臺來滿足各種需求，而不會受到任何影響。 本主題摘要說明 Direct2D 可互通的不同平臺。 包含以下幾節。

-   [GDI 互通性](#gdi-interoperability)
-   [GDI+互 操作 性](#gdi-interoperability)
-   [Direct3D 互通性](#direct3d-interoperability)
-   [DirectWrite互 操作 性](#directwrite-interoperability)
-   [Windows (WIC) 互通性的影像處理元件](#windows-imaging-component-wic-interoperability)
-   [相關主題](#related-topics)

下圖摘要說明 Direct2D 可互通的不同平臺，並列出一些可提供互通性的方法和介面。

![direct2d 交互操作之平臺的圖表，包括 direct3d 10.1、directwrite、wic、gdi + 和 gdi](images/direct2dinterop.png)

## <a name="gdi-interoperability"></a>GDI 互通性

Direct2D 可啟用與 GDI 之間的雙向互通性。 您可以使用 [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) 將 Direct2D 內容寫入 (DC) 的 GDI [裝置](/windows/desktop/gdi/device-contexts) 內容，也可以使用 [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) 來取得呈現目標的 DC 標記法。

如需詳細資訊和範例，請參閱 [Direct2D 和 GDI 互通性總覽](direct2d-and-gdi-interoperation-overview.md)。

## <a name="gdi-interoperability"></a>GDI+互 操作 性

您可以使用與 Direct2D 相同的方式來使用 GDI+ 與 GDI。 您可以使用 [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)將 Direct2D 內容寫入至與 GDI+ 內容相同的 DC。 這種方法可讓您開始將 Direct2D 內容新增至主要使用 GDI+ 轉譯的應用程式。

您也可以使用 [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) 來提供使用 Direct2D 寫入之 GDI DC 的存取權，然後使用 [**FromHDC**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) 方法來建立物件。 這種方法適用于主要以 Direct2D 轉譯的應用程式，但具有擴充性模型或其他需要能夠以 GDI+ 轉譯的舊版內容。

## <a name="direct3d-interoperability"></a>Direct3D 互通性

Direct2D 可以使用由 [**CreateDxgiSurfaceRender**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) 方法建立的 DXGI 介面轉譯目標 (，) 寫入 [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface)。 此動作可讓您將2D 背景和介面新增至3-d 場景，並使用 Direct2D 內容做為3D 模型的材質。 Direct2D 也可以採用 [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) ，並使用 [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) 方法來建立點陣圖表示。

如需詳細資訊和範例，請參閱 [Direct2D 和 Direct3D 互通性總覽](direct2d-and-direct3d-interoperation-overview.md)。

## <a name="directwrite-interoperability"></a>DirectWrite互 操作 性

Direct2D 與 DirectWrite 緊密整合。 Direct2D 藉由提供 [**DrawText**](id2d1rendertarget-drawtext.md)、 [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)和 [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)方法，讓您輕鬆轉譯 DirectWrite 的內容。

## <a name="windows-imaging-component-wic-interoperability"></a>Windows (WIC) 互通性的影像處理元件

Direct2D 提供 [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md)、 [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)和 [**CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) 方法來操作 WIC 點陣圖。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct2D 和 GDI 互通性總覽](direct2d-and-gdi-interoperation-overview.md)
</dt> <dt>

[Direct2D 和 Direct3D 互通性概觀](direct2d-and-direct3d-interoperation-overview.md)
</dt> </dl>

 

 