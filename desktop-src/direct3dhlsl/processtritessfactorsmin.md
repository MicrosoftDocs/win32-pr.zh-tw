---
title: ProcessTriTessFactorsMin 函式
description: 產生三個修補程式的已更正鑲嵌因數。 |ProcessTriTessFactorsMin 函式
ms.assetid: fa1e19c2-fadf-42d4-9574-834eaf871393
keywords:
- ProcessTriTessFactorsMin 函式 HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33f82c7935d47813d833ccc21a7ec0134adee1cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104514425"
---
# <a name="processtritessfactorsmin-function"></a>ProcessTriTessFactorsMin 函式

產生三個修補程式的已更正鑲嵌因數。

## <a name="syntax"></a>語法

``` syntax
void ProcessTriTessFactorsMin(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactors,
  out float UnroundedInsideTessFactors
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

*RoundedInsideTessFactors* \[擴展\]
</dt> <dd>

類型： **float**

鑲嵌階段針對內部邊緣計算的圓角鑲嵌因數。

</dd> <dt>

*UnroundedInsideTessFactors* \[擴展\]
</dt> <dd>

類型： **float**

鑲嵌階段針對內部邊緣所計算的鑲嵌因數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

會產生三個修補程式的已更正鑲嵌因數，以最小的邊緣鑲嵌因數來計算內鑲嵌因數，然後以 InsideScale 進行調整。 結果接著會根據資料分割模式舍入，但使用 UnroundedInsideTessFactor 參數可使用 unrounded 結果。

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

 

 




