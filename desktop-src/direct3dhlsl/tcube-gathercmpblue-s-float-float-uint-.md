---
title: TextureCube：： GatherCmpBlue (S，float，float，uint) 函數
description: 針對在雙線性篩選作業中使用的四個材質值，會傳回其藍色元件與比較值的比較，以及磚對應狀態。 |TextureCube：： GatherCmpBlue (S，float，float，uint) 函數
ms.assetid: 1D1FFF0E-9CA7-48A4-A305-C0B6059056E7
keywords:
- GatherCmpBlue 函式 HLSL
topic_type:
- apiref
api_name:
- GatherCmpBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2022546bb01137e730b4e0f720dbb2c3c091d609
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974032"
---
# <a name="texturecubegathercmpbluesfloatfloatuint-function"></a>TextureCube：： GatherCmpBlue (S，float，float，uint) 函數

針對在雙線性篩選作業中使用的四個材質值，會傳回其藍色元件與比較值的比較，以及磚對應狀態。

## <a name="syntax"></a>語法


``` syntax
TemplateType GatherCmpBlue(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a>參數

<dl> <dt>

 \[ 中的 S\]
</dt> <dd>

類型： **SamplerState**

以零為基底的取樣器索引。

</dd> <dt>

*位置* \[在\]
</dt> <dd>

類型： **float**

此範例會協調 (u，v) 。

</dd> <dt>

*CompareValue* \[在\]
</dt> <dd>

類型： **float**

要針對每個取樣值進行比較的值。

</dd> <dt>

*狀態* \[擴展\]
</dt> <dd>

類型： **uint**

作業的狀態。 您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。 如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。 如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **TemplateType**

四個元件的值，其類型與範本類型相同。

## <a name="remarks"></a>備註

紋理範例可用於雙線性插補。

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[GatherCmpBlue 方法](texturecube-gathercmpblue.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
