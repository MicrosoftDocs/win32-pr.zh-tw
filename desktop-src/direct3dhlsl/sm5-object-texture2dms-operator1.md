---
title: Texture2DMS：： Operator 函數
description: 從位於範例索引0所提供位置的資源抓取值。
ms.assetid: 80380D3F-1E71-4C43-A17B-F94F6E5215B1
keywords:
- 運算子函式 HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6ae7976e6871dc2547ed5c372e1551e5bf0ca148
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104971852"
---
# <a name="texture2dmsoperator--function"></a>Texture2DMS：： Operator 函數

從位於範例索引0所提供位置的資源抓取值。

## <a name="syntax"></a>語法

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*pos* \[在\]
</dt> <dd>

類型： **uint2**

索引位置。 包含 (x，y) 座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **R**

唯讀的資源變數。

## <a name="remarks"></a>備註

若要選取特定的範例，請參閱 [**範例。\[運算子 \] 。 \[ \]**](sm5-object-texture2dms-sampleoperatorindex.md)

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




