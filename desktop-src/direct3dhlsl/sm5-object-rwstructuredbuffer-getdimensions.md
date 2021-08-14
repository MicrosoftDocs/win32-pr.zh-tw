---
title: RWStructuredBuffer：： GetDimensions 函數
description: 取得資源維度。 |RWStructuredBuffer：： GetDimensions 函數
ms.assetid: 842b3d21-2e2b-4906-93ee-0252b2e8cf85
keywords:
- GetDimensions 函式 HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 760a546d7d60afbb41438416a9602ab55981834acd9969bc535c9a82df6e5e50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789924"
---
# <a name="rwstructuredbuffergetdimensions-function"></a>RWStructuredBuffer：： GetDimensions 函數

取得資源維度。

## <a name="syntax"></a>語法

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*numStructs* \[擴展\]
</dt> <dd>

類型： **uint**

資源中的結構數目。

</dd> <dt>

*stride* \[擴展\]
</dt> <dd>

類型： **uint**

每個結構元素的 stride （以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

Nothing

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[RWStructuredBuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




