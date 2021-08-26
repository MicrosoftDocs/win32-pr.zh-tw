---
title: ProcessQuadTessFactorsMax 函式
description: 產生四個修補程式的已更正鑲嵌因數。 |ProcessQuadTessFactorsMax 函式
ms.assetid: a0c91430-db25-49c9-bcc8-d2be1d0e6f6c
keywords:
- ProcessQuadTessFactorsMax 函式 HLSL
topic_type:
- apiref
api_name:
- ProcessQuadTessFactorsMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58cfa3f9e6dd69210da18d672acd2b56ad73e34be9cf2c5d8b179181e636050f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067778"
---
# <a name="processquadtessfactorsmax-function"></a>ProcessQuadTessFactorsMax 函式

產生四個修補程式的已更正鑲嵌因數。

## <a name="syntax"></a>語法

``` syntax
void ProcessQuadTessFactorsMax(
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

會產生四個修補程式的已更正鑲嵌因數，以最大的邊緣鑲嵌因數來計算內鑲嵌因數。 內部 tess 因數會是由 InsideScale 所調整之四個邊緣的最大值所決定的相同值。 結果接著會根據資料分割模式舍入，但使用 *UnroundedInsideTessFactors* 參數可使用 unrounded 結果。

### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




