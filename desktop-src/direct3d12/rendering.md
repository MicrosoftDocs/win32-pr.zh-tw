---
title: '轉譯 (Direct3D 12 圖形) '
description: 本章節包含 Direct3D 12 (和 Direct3D 11.3) 的新轉譯功能的相關資訊。
ms.assetid: 5BF1440E-E4D8-43C8-BF0E-F02FEFE79C93
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ad70a054881e9472ff27a76a62dca62fdf3653
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548428"
---
# <a name="rendering-direct3d-12-graphics"></a>轉譯 (Direct3D 12 圖形) 

本章節包含 Direct3D 12 (和 Direct3D 11.3) 的新轉譯功能的相關資訊。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                               | 描述                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [保守的點陣化](conservative-rasterization.md)<br/>                             | 保守地柵格化可為圖元轉譯新增一些確定性，這對碰撞偵測演算法特別有用。<br/>                                                                                                                                                                                                                                              |
| [間接繪圖](indirect-drawing.md)<br/>                                                 | 間接繪圖可讓您將一些場景遍歷和剔除從 CPU 移至 GPU，進而改善效能。 命令緩衝區可以由 CPU 或 GPU 產生。<br/>                                                                                                                                                                                              |
| [依轉譯器排序的視圖](rasterizer-order-views.md)<br/>                                   | 以轉譯器排序的視圖 (ROVs) 允許圖元著色器程式碼將 UAV 系結標示為會改變 UAVs 圖形管線結果順序的一般需求。 這可讓您 (OIT) 演算法來運作，以提供更好的轉譯結果，當多個透明物件在視圖中彼此對齊時，可提供更好的呈現結果。 <br/> |
| [著色器指定的樣板參考值](shader-specified-stencil-reference-value.md)<br/> | 啟用圖元著色器以輸出樣板參考值，而不是使用 API 指定的值，讓您能夠對樣板作業進行細微的控制。<br/>                                                                                                                                                                                                              |
| [交換鏈](swap-chains.md)<br/>                                                           | 交換鏈會控制背景的緩衝區旋轉，形成圖形動畫的基礎。<br/>                                                                                                                                                                                                                                                                                            |



 

下列主題也是 Direct3D 12 和 Direct3D 11.3 的新手：

-   [預設材質對應](default-texture-mapping.md)
-   [具類型的未排序存取視圖載入](typed-unordered-access-view-loads.md)
-   [磁片區磚資源](volume-tiled-resources.md)

## <a name="high-dynamic-range-and-wide-color-gamut"></a>高動態範圍和寬色彩範圍

請參閱支援高動態範圍 (增加最亮的 whites 與最深的黑色) 之間的差異，而寬色彩範圍 (10 位，而不是8位，) 在 [DXGI 1.5 改良功能](/windows/desktop/direct3ddxgi/dxgi-1-5-improvements)中說明。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 12 程式設計指南](directx-12-programming-guide.md)
</dt> </dl>

 

