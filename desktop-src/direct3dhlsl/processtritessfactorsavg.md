---
title: ProcessTriTessFactorsAvg 函式
description: 產生三個修補程式的已更正鑲嵌因數。 |ProcessTriTessFactorsAvg 函式
ms.assetid: 005a63b6-f35d-42d6-bb29-f4ebb374080e
keywords:
- ProcessTriTessFactorsAvg 函式 HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsAvg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90cfa86a09e0e76c90f0013cfa6121917ca25378
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991938"
---
# <a name="processtritessfactorsavg-function"></a>ProcessTriTessFactorsAvg 函式

產生三個修補程式的已更正鑲嵌因數。

## <a name="syntax"></a>語法

``` syntax
void ProcessTriTessFactorsAvg(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactor,
  out float UnroundedInsideTessFactor
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*RawEdgeFactors* \[在\]
</dt> <dd>

類型： **float3**

傳遞至鑲嵌階段的邊緣鑲嵌因數。

</dd> <dt>

*InsideScale* \[在\]
</dt> <dd>

類型： **float**

調整因數會套用至鑲嵌式階段所計算的 UV 鑲嵌因數。 InsideScale 的允許範圍是0.0 到1.0。

</dd> <dt>

*RoundedEdgeTessFactors* \[擴展\]
</dt> <dd>

類型： **float3**

鑲嵌階段所計算的圓角邊緣鑲嵌因數。

</dd> <dt>

*RoundedInsideTessFactor* \[擴展\]
</dt> <dd>

類型： **float**

鑲嵌階段所計算的鑲嵌因數，並且舍入。

</dd> <dt>

*UnroundedInsideTessFactor* \[擴展\]
</dt> <dd>

類型： **float**

鑲嵌階段所計算的原始、unrounded、UV 鑲嵌因數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

會產生三個修補程式的已更正鑲嵌因數，並計算內鑲嵌因數作為邊緣鑲嵌因數的平均值，然後以 InsideScale 進行調整。 結果接著會根據資料分割模式舍入，但使用 UnroundedInsideTessFactor 參數可使用 unrounded 結果。

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

 

 




