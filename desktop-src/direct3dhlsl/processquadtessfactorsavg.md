---
title: ProcessQuadTessFactorsAvg 函式
description: 產生四個修補程式的已更正鑲嵌因數。 |ProcessQuadTessFactorsAvg 函式
ms.assetid: 3af1dad3-1923-45f3-9908-ca403e7f0cfe
keywords:
- ProcessQuadTessFactorsAvg 函式 HLSL
topic_type:
- apiref
api_name:
- ProcessQuadTessFactorsAvg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36a50dd971161f3e03514947db447774da5b6a62
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992050"
---
# <a name="processquadtessfactorsavg-function"></a>ProcessQuadTessFactorsAvg 函式

產生四個修補程式的已更正鑲嵌因數。

## <a name="syntax"></a>語法

``` syntax
void ProcessQuadTessFactorsAvg(
  in  float4 RawEdgeFactors,
  in  float InsideScale,
  out float4 RoundedEdgeTessFactors,
  out float2 RoundedInsideTessFactors,
  out float2 UnroundedInsideTessFactors
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*RawEdgeFactors* \[在\]
</dt> <dd>

類型： **float4**

傳遞至鑲嵌階段的邊緣鑲嵌因數。

</dd> <dt>

*InsideScale* \[在\]
</dt> <dd>

類型： **float**

調整因數會套用至鑲嵌式階段所計算的 UV 鑲嵌因數。 InsideScale 的允許範圍是0.0 到1.0。

</dd> <dt>

*RoundedEdgeTessFactors* \[擴展\]
</dt> <dd>

類型： **float4**

鑲嵌階段所計算的圓角邊緣鑲嵌因數。

</dd> <dt>

*RoundedInsideTessFactors* \[擴展\]
</dt> <dd>

類型： **float2**

鑲嵌階段針對內部邊緣計算的圓角鑲嵌因數。

</dd> <dt>

*UnroundedInsideTessFactors* \[擴展\]
</dt> <dd>

類型： **float2**

鑲嵌階段針對內部邊緣所計算的鑲嵌因數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

會產生四個修補程式的已更正鑲嵌因數，並計算出鑲嵌因數作為邊緣鑲嵌因數的平均值。 內部 tess 因數將會是相同的值，由 InsideScale 所調整的四個邊緣的平均值所決定。 結果接著會根據資料分割模式舍入，但使用 UnroundedInsideTessFactors 參數可使用 unrounded 結果。

### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




