---
title: firstbithigh 函式
description: 取得第一個集合位從最高順序位開始，每個元件往下工作的位置。
ms.assetid: 0fa89a9e-1706-44f7-8dd3-c37af5c11ddc
keywords:
- firstbithigh 函式 HLSL
topic_type:
- apiref
api_name:
- firstbithigh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c62b6f090126887930415fc408da4f4a6c17bc4a99429db61fd298960c07e6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949698"
---
# <a name="firstbithigh-function"></a>firstbithigh 函式

取得第一個集合位從最高順序位開始，每個元件往下工作的位置。

## <a name="syntax"></a>語法

``` syntax
int firstbithigh(
  in int value
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*值* \[在\]
</dt> <dd>

類型： **[ **int**](/windows/desktop/WinProg/windows-data-types)**

輸入值。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **int**](/windows/desktop/WinProg/windows-data-types)**

第一個設定位的位置。

## <a name="remarks"></a>備註

若為帶正負號的整數，負數的第一個有效位為零。

您也可以使用下列多載版本：

``` syntax
int2 firstbithigh(int2 value);
int3 firstbithigh(int3 value);
int4 firstbithigh(int4 value);
uint firstbithigh(uint value);
uint2 firstbithigh(uint2 value);
uint3 firstbithigh(uint3 value);
uint4 firstbithigh(uint4 value);
```

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

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 