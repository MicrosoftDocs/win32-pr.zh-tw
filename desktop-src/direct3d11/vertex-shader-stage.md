---
title: 頂點著色器階段
description: 頂點著色器 (與) 階段會處理來自輸入組合語言的頂點，以執行每個頂點的作業，例如轉換、外觀、變形，以及每個頂點的光源。
ms.assetid: C6A39F48-A243-4049-8AED-0B521BEDFA76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3815f4c26c97e68ac0b4b20b72849052710f2f6adc0722bb3e42f5c8bf7a1c89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530406"
---
# <a name="vertex-shader-stage"></a>頂點著色器階段

頂點著色器 (與) 階段會處理來自輸入組合語言的頂點，以執行每個頂點的作業，例如轉換、外觀、變形，以及每個頂點的光源。 頂點著色器一律在單一輸入頂點上操作，並產生單一輸出頂點。 頂點著色器階段必須永遠作用中，才能讓管線執行。 不需要頂點修改或轉換時，必須建立穿通頂點著色器並將其設定至管線。

## <a name="the-vertex-shader"></a>頂點著色器

每個頂點著色器輸入頂點最多可包含 16 32 位向量 (每個) 最多4個元件，而每個輸出頂點最多可包含 16 32 位4個元件向量。 所有頂點著色器都必須最少有一個輸入與一個輸出，這最少可能是一個純量值。

頂點著色器階段可以從輸入組合語言取用兩個系統產生的值： VertexID 和 InstanceID (查看系統值和語義) 。 因為 VertexID 和 InstanceID 在頂點層級有意義，而且由硬體產生的識別碼只可以饋送到了解它們的第一階段，所以這些識別碼只可以饋送到頂點著色器階段。

頂點著色器永遠會在所有頂點上執行，包括在輸入基本類型拓撲中有相鄰關係的相鄰頂點。 使用 VSInvocations 管線統計資料，可以從 CPU 查詢頂點著色器已經執行的次數。

頂點著色器可以執行載入和紋理取樣作業，而不需要螢幕空間衍生物件 (使用 HLSL 內建函式：[Sample（DirectX HLSL 紋理物件）](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-sample)、[SampleCmpLevelZero（DirectX HLSL 紋理物件）](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplecmplevelzero)，以及[SampleGrad（DirectX HLSL 紋理物件）](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplegrad))。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖形管線](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[ (Direct3D 10) 的管線階段 ](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 