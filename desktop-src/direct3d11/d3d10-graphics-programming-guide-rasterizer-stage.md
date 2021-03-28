---
title: 轉譯器階段
description: 點陣化階段會轉換向量資訊 (由圖形或基本類型組成) 為點陣影像 (由像素組成)，以顯示即時 3D 圖形。
ms.assetid: efd3f819-7c63-4e1a-9923-8e7198354ec6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e746c5ace3512f36f9b9ad34d34a3ea578e1de36
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933746"
---
# <a name="rasterizer-stage"></a>轉譯器階段

點陣化階段會轉換向量資訊 (由圖形或基本類型組成) 為點陣影像 (由像素組成)，以顯示即時 3D 圖形。

在點陣化期間，每個基本類型會轉換成像素，同時針對每個基本類型插入每個頂點值。 點陣化包含裁剪頂點到檢視範圍、執行以 z 相除以提供透視圖、將基本類型對應到 2D 檢視區，以及決定如何叫用像素著色器。 當使用像素著色器為選擇性時，而轉譯器階段始終會執行裁剪，分割透視圖以將點轉換為同質空間，以及將頂點對應到檢視區。

進入轉譯器階段的頂點 (x、y、z、w) ，會假設位於同質的剪輯空間中。 在這個座標空間中，X 軸指向右，Y 指向上，Z 偏離相機。

您可以使用 [**>id3d11devicecoNtext：:P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)) ，並停用深度和樣板測試 (將 [**D3D11 \_ 深度樣板 \_ \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)) 中的 **DepthEnable** 和 **StencilEnable** 設定為 **FALSE** ，以停用柵格化，方法是告知管線沒有圖元著色器 (將圖元著色器階段設定為 **Null** 。 停用時，不會更新與點陣化相關的管線計數器。 此外，也提供了 [柵格化規則](d3d10-graphics-programming-guide-rasterizer-stage-rules.md)的完整描述。

在執行階層式 Z 緩衝區優化的硬體上，您可以在啟用深度和樣板測試時，將圖元著色器階段設定為 **Null** ，藉以啟用載入 z 緩衝區。


## <a name="in-this-section"></a>本節內容



| 主題                                                                                                                         | 描述                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [使用轉譯器階段開始使用](d3d10-graphics-programming-guide-rasterizer-stage-getting-started.md)<br/> | 本節說明如何設定視口、剪刀矩形、轉譯器狀態和多取樣。<br/>                                                                                                                                                                                                |
| [柵格化規則](d3d10-graphics-programming-guide-rasterizer-stage-rules.md)<br/>                                 | 點陣化規則定義向量資料對應至點陣資料的方式。 點陣資料會貼齊至整數位置，該整數位置接著會進行揀選和裁剪 (以繪製像素數目下限)，而每個像素屬性會在傳遞至像素著色器之前進行插入 (從每個頂點屬性)。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖形管線](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[ (Direct3D 10) 的管線階段 ](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

