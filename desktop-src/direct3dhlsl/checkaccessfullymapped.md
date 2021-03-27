---
title: CheckAccessFullyMapped 函式
description: 判斷範例、收集或載入作業中的所有值是否已在磚資源中存取對應的磚。
ms.assetid: 2CAB7770-143E-4E29-A57F-96C27021AC5F
keywords:
- CheckAccessFullyMapped 函式 HLSL
topic_type:
- apiref
api_name:
- CheckAccessFullyMapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c7310e0ebac496fc8f5a56ba3843b7496b8ce7c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682875"
---
# <a name="checkaccessfullymapped-function"></a>CheckAccessFullyMapped 函式

判斷 **範例**、 **收集** 或 **載入** 作業中的所有值是否已在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚。

## <a name="syntax"></a>語法

``` syntax
bool CheckAccessFullyMapped(
  in uint_only status
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*狀態* \[在\]
</dt> <dd>

類型： **\_ 僅限 uint**

從 **範例**、 **收集** 或 **載入** 作業傳回的狀態值。 因為您無法直接存取此狀態值，所以您必須將它傳遞給 **CheckAccessFullyMapped**。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **bool**

傳回 **布林** 值，這個值會指出 **範例**、 **收集** 或 **載入** 作業中的所有值是否都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚。 如果作業中的所有值都已存取對應的磚，則傳回 **TRUE** ;否則，如果從未對應的磚取得任何值，則會傳回 **FALSE** 。

## <a name="remarks"></a>備註

### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 