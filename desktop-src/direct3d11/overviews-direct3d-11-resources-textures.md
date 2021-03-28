---
title: 紋理
description: 本節說明 Direct3D 11 中所使用的材質，以及一般案例的工作架構檔連結。
ms.assetid: ec833431-a7b4-4aea-91c8-e99b718de2c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc3909f354b0709e82ffd2bdffafe6cdb35516
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183821"
---
# <a name="textures"></a>紋理

材質會儲存材質資訊。 本節說明 Direct3D 11 中所使用的材質，以及一般案例的工作架構檔連結。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                    | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Direct3D 11 中的材質簡介](overviews-direct3d-11-resources-textures-intro.md)<br/> | 紋理資源是設計來儲存紋素的結構化資料集合。 紋素代表管線可讀取或寫入的最小紋理單位。 和緩衝區不同的是，紋理可依紋理樣本篩選，由著色器單位讀取。 紋理類型會影響篩選紋理的方式。 每個材質都包含1至4個元件，以 DXGI 格式列舉所定義的其中一個 DXGI 格式來排列 \_ 。<br/> |
| [Direct3D 11 中的材質區塊壓縮](texture-block-compression-in-direct3d-11.md)<br/>      | 紋理的區塊壓縮 (BC) 支援在 Direct3D 11 中已進行擴充，內含 BC6H 和 BC7 演算法。 BC6H 支援高動態範圍色彩來源資料，而 BC7 使用較少的標準 RGB 來源資料成品，提供高於平均品質的壓縮。<br/>                                                                                                                                                                           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何：建立材質](overviews-direct3d-11-resources-textures-create.md)
</dt> <dt>

[如何：以程式設計方式初始化材質](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
</dt> <dt>

[如何：從檔案初始化材質](overviews-direct3d-11-resources-textures-how-to.md)
</dt> <dt>

[資源](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





