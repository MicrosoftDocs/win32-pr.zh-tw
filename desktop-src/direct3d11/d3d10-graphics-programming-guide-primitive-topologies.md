---
title: 基本拓撲
description: Direct3D 10 和更新版本支援數個基本類型 (或以 D3D \_ 基本拓撲列舉類型表示的拓撲) \_ 。 這些類型會定義管線如何轉譯和呈現頂點。
ms.assetid: 357ad085-fd91-4420-abc3-1c57e8cbb517
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e83f901d4d91d01a3cffedddb343fde7b50c20e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315217"
---
# <a name="primitive-topologies"></a>基本拓撲

Direct3D 10 和更新版本支援數個基本類型 (或以 [**D3D \_ 基本 \_ 拓撲**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology) 列舉類型表示的拓撲) 。 這些類型會定義管線如何轉譯和呈現頂點。

-   [基本基本類型](#basic-primitive-types)
-   [基本相鄰](#primitive-adjacency)
-   [纏繞方向和前置頂點位置](#winding-direction-and-leading-vertex-positions)
-   [產生多個停車線](#generating-multiple-strips)
-   [相關主題](#related-topics)

## <a name="basic-primitive-types"></a>基本基本類型

以下是支援的基本基本類型：

-   [點清單](/windows/desktop/direct3d9/point-lists)
-   [行清單](/windows/desktop/direct3d9/line-lists)
-   [行帶](/windows/desktop/direct3d9/line-strips)
-   [三角形清單](/windows/desktop/direct3d9/triangle-lists)
-   [邊帶](/windows/desktop/direct3d9/triangle-strips)

如需每個基本類型的視覺效果，請參閱本主題稍後的 [纏繞方向和前置頂點位置](#winding-direction-and-leading-vertex-positions)的圖表。

輸入組合語言階段會從頂點和索引緩衝區讀取資料、將資料組合成這些基本專案，然後將資料傳送至其餘的管線階段。  (您可以使用 [**>id3d11devicecoNtext：： IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology) 方法來指定輸入組合語言階段的基本類型。 ) 

## <a name="primitive-adjacency"></a>基本相鄰

除了點清單) 之外，所有 Direct3D 10 和更高的基本型別 (都有兩個版本：一個具有連續的基本型別，以及一個不連續的基本類型。 具有相鄰關係的基本類型包含一些周圍頂點，而不具相鄰關係的基本類型僅包含目標基本類型的頂點。 例如，「 **d3d \_ 基本 \_ 拓撲 \_ LINELIST** 值代表的行清單基本 () 具有對應的行清單原始物件，其中包含 **d3d \_ 基本 \_ 拓撲 \_ LINELIST \_** 調整值所代表的相鄰 (。 ) 

相鄰基本類型旨在提供您更多幾何的相關資訊，並僅透過幾何著色器顯示。 相鄰關係適用於使用剪影偵測、陰影磁碟區立體化等的幾何著色器。

例如，假設您想要繪圖具有相鄰關係的三角形清單。 包含 36 個頂點 (具有相鄰關係) 的三角形清單將產生 6 個已完成的基本類型。 具相鄰關係的基本類型 (帶狀線除外) 包含的頂點數是不具相鄰關係的同等基本類型正好兩倍，其中每個額外的頂點是相鄰的頂點。

## <a name="winding-direction-and-leading-vertex-positions"></a>纏繞方向和前置頂點位置

如下圖所示，前置頂點是基本類型中的第一個非相鄰頂點。 基本類型可讓多個前置頂點經過定義，只要每個前置頂點是用於不同基本類型。 具相鄰關係三角形連環，前置頂點是 0、2、4、6 等。 具相鄰關係的帶狀線，前置頂點是 1、2、3 等。 換句話說，相鄰基本類型沒有前置頂點。

下圖顯示可產生輸入組合語言的所有基本類型的頂點排序。

![基本類型頂點排序圖表](images/d3d10-primitive-topologies.png)

前述圖中的符號在下表中說明。



| 符號                                                                                   | 名稱              | 描述                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![頂點符號](images/d3d10-primitive-topologies-vertex.png)                     | 頂點            | 3D 空間中的點。                                                                                                                                                                               |
| ![線圈方向的符號](images/d3d10-primitive-topologies-winding-direction.png) | 線圈方向 | 組合基本類型時的頂點排序。 可以順時針或逆時針;藉由呼叫 [**ID3D11Device1：： CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1)來指定此項。 |
| ![前置頂點的符號](images/d3d10-primitive-topologies-leading-vertex.png)       | 前置頂點    | 包含每個常數資料的基本類型中的第一非相鄰頂點。                                                                                                                      |



 

## <a name="generating-multiple-strips"></a>產生多個停車線

您可以透過寬帶切割產生多條寬帶。 您可以明確呼叫 [RestartStrip](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-so-restartstrip) HLSL 函式或將特殊索引值插入索引緩衝區，來執行寬帶切割。 這個值是 –1，32 位元索引是 0xffffffff 或 16 位元索引是 0xffff。 –1 的索引表示明確「剪下」或」重新啟動」目前的寬帶。 上一個索引完成上一個基本類型或寬帶，而下一個索引開始新的基本類型或寬帶。 如需產生多個停車線的詳細資訊，請參閱 [幾何著色器階段](/previous-versions//bb205146(v=vs.85))。

> [!Note]  
> 您需要 [功能等級](overviews-direct3d-11-devices-downlevel-intro.md) 10.0 或更高的硬體，因為並非所有10level9 硬體都能實行這項功能。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Input-Assembler 階段開始使用](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)
</dt> <dt>

[ (Direct3D 10) 的管線階段 ](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 