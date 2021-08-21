---
title: ProcessIsolineTessFactors 函式
description: 產生等值線的圓角鑲嵌因數。
ms.assetid: 0816b3e0-cb03-4a7a-9732-e84c637b3d48
keywords:
- ProcessIsolineTessFactors 函式 HLSL
topic_type:
- apiref
api_name:
- ProcessIsolineTessFactors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34c6f4d579ee7fbaee9416d7a607e3856a7793021cca7149723d3d6e5a2b4a49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986288"
---
# <a name="processisolinetessfactors-function"></a>ProcessIsolineTessFactors 函式

產生等值線的圓角鑲嵌因數。

## <a name="syntax"></a>語法

``` syntax
void ProcessIsolineTessFactors(
  in  float RawDetailFactor,
  in  float RawDensityFactor,
  out float RoundedDetailFactor,
  out float RoundedDensityFactor
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*RawDetailFactor* \[在\]
</dt> <dd>

類型： **float**

所需的詳細因素。

</dd> <dt>

*RawDensityFactor* \[在\]
</dt> <dd>

類型： **float**

所需的密度因數。

</dd> <dt>

*RoundedDetailFactor* \[擴展\]
</dt> <dd>

類型： **float**

圓角詳細因數壓制至可供鑲嵌使用的範圍。

</dd> <dt>

*RoundedDensityFactor* \[擴展\]
</dt> <dd>

類型： **float**

鑲嵌會使用壓制至 rangethat 的舍入密度因數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

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

 

 




