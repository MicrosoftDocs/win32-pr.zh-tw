---
title: HLSL 著色器模型6。4
description: 描述新增至 HLSL 著色器模型6.4 的機器學習內建函式。
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 10e74b268243ab059c2d0945887a6d429d40bb53
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103853528"
---
# <a name="hlsl-shader-model-64"></a>HLSL 著色器模型6。4

描述新增至 HLSL 著色器模型6.4 的機器學習內建函式。

## <a name="shader-model-64"></a>著色器模型6。4
這些內建函式是著色器模型6.4 的必要/支援功能。 因此，除了確保使用著色器模型6.4 之外，不需要個別的功能位檢查。 這些常式的最小支援用戶端是 Windows 10 1903 版。

## <a name="shading-language-intrinsics"></a>網底語言內建函式

### <a name="unsigned-integer-dot-product-of-4-elements-and-accumulate"></a>4個元素的不帶正負號整數 Dot-Product 並累積
```syntax
uint32 dot4add_u8packed(uint32 a, uint32 b, uint32 acc); // ubyte4 a, b;
```
 
具有 add 的4維不帶正負號的整數點乘積。 將兩個輸入 Dword 中每個對應的不帶正負號的8位 int 位元組配對在一起，並將結果加總為32位不帶正負號整數的整數。 此指令會在單一32位寬 SIM資料通道內運作。 輸入也會假設為32位數量。
 
### <a name="signed-integer-dot-product-of-4-elements-and-accumulate"></a>4個元素的帶正負號整數 Dot-Product 並累積
```syntax
int32 dot4add_i8packed(uint32 a, uint32 b, int32 acc); // signed byte4 a, b;
```

具有 add 的4維帶正負號的整數點乘積。 將兩個輸入 Dword 中每個對應的帶正負號8位 int 位元組配對在一起，並將結果加總為32位帶正負號的整數。 此指令會在單一32位寬 SIM資料通道內運作。 輸入也會假設為32位數量。
 
### <a name="single-precision-floating-point-2-element-dot-product-and-accumulate"></a>單精確度浮點數 2-元素 Dot-Product 和累積
```syntax
float dot2add( half2 a, half2 b, float acc );
```

具有 add 的 half2 向量之二維浮點數點乘積。 將兩個半精確度浮點數輸入向量的元素相乘，並將結果加總為32位浮點數。 此指示會在單一32位寬 SIM資料通道內運作。 輸入是封裝至相同通道的16位數量。

這涵蓋在低精確度功能位之下 (表示) 提供原生半和簡短支援。

### <a name="sv_shadingrate"></a>SV_ShadingRate
```syntax
uint shadingRate : SV_ShadingRate
```

不帶正負號的整數，代表圖元著色器的每個調用所寫入的目標圖元數目。 有效的值屬於 [D3D12_SHADING_RATE](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate)的列舉值集。

此系統值適用于 [D3D12_VARIABLE_SHADING_RATE_TIER_2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) 或更高版本的平臺。 您可以從最多一個頂點或幾何著色器階段寫入它。 您可以從圖元著色器階段讀取它。 如需詳細資訊，請參閱 [可變速率陰影](../direct3d12/vrs.md)。