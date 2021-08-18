---
title: asuint 函式
description: 以兩個不帶正負號的32位整數向量64位值的位模式。
ms.assetid: 29671661-4fec-46e5-9b6f-56fba8e1d756
keywords:
- asuint 函式 HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02f0df4d31ca978b8b58b50cd0c91710056aa9ac0f3cac1ae370a4edba6a9edf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626588"
---
# <a name="asuint-function"></a>asuint 函式

以兩個不帶正負號的32位整數向量64位值的位模式。

## <a name="syntax"></a>語法

``` syntax
void asuint(
  in  double value,
  out uint lowbits,
  out uint highbits
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*值* \[在\]
</dt> <dd>

類型： **double**

輸入值。

</dd> <dt>

*lowbits* \[擴展\]
</dt> <dd>

類型： **uint**

*值* 的低32位模式。

</dd> <dt>

*highbits* \[擴展\]
</dt> <dd>

類型： **uint**

*值* 的高32位模式。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

此函式是 [**asuint**](dx-graphics-hlsl-asuint.md) 內建的替代版本，已在先前的著色器模型中提供，並已針對著色器模型5引進。 原始函式 (由其不同簽章在 HLSL 編譯器中辨識) 仍可供著色器模型5使用。

### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




