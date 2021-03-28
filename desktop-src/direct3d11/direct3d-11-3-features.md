---
title: Direct3D 11.3 功能
description: 下列各節說明 Direct3D 11.3 中已新增的功能。 這些功能也可在 Direct3D 12 中使用。
ms.assetid: CA79A315-22C4-4141-8E66-89C0DCF29191
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc256b9b85dd807e2e6c923affdec496fe92e075
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383353"
---
# <a name="direct3d-113-features"></a>Direct3D 11.3 功能

下列各節說明 Direct3D 11.3 中已新增的功能。 這些功能也可在 Direct3D 12 中使用。


## <a name="in-this-section"></a>本節內容



| 主題                                                                                               | 描述                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [保守的點陣化](conservative-rasterization.md)<br/>                             | 保守地柵格化可為圖元轉譯新增一些確定性，這對碰撞偵測演算法特別有用。<br/>                                                                                                                                                                                                                                              |
| [預設材質對應](default-texture-mapping.md)<br/>                                   | 使用預設材質對應可減少在 GPU 和 CPU 之間共用映射資料時的複製和記憶體使用量。 不過，它應該只在特定情況下使用。 標準 swizzle 配置可避免複製或 swizzling 多個版面配置中的資料。<br/>                                                                                                               |
| [轉譯器順序視圖](rasterizer-order-views.md)<br/>                                     | 以轉譯器排序的視圖 (ROVs) 允許圖元著色器程式碼將 UAV 系結標示為會改變 UAVs 圖形管線結果順序的一般需求。 這可讓您 (OIT) 演算法來運作，以提供更好的轉譯結果，當多個透明物件在視圖中彼此對齊時，可提供更好的呈現結果。 <br/> |
| [著色器指定的樣板參考值](shader-specified-stencil-reference-value.md)<br/> | 啟用圖元著色器以輸出樣板參考值，而不是使用 API 指定的值，讓您能夠對樣板作業進行細微的控制。<br/>                                                                                                                                                                                                              |
| [具類型的未排序存取視圖載入](typed-unordered-access-view-loads.md)<br/>               | 未排序的存取視圖 (UAV) 具類型的負載，是可讓著色器從具有特定 DXGI 格式的 UAV 讀取的能力 \_ 。<br/>                                                                                                                                                                                                                                                               |
| [統一記憶體架構](unified-memory-architecture.md)<br/>                           | 查詢是否支援統一記憶體架構 (UMA) 可協助判斷如何處理某些資源。<br/>                                                                                                                                                                                                                                                              |
| [磁片區磚資源](volume-tiled-resources.md)<br/>                                     | 磁片區 (3D) 材質可以用來做為並排的資源，請注意磚解析度是三維。<br/>                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 11 的新功能](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 





