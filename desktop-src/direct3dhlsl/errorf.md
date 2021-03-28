---
title: errorf 函式
description: 將錯誤訊息提交至資訊佇列。
ms.assetid: bf4dc6dc-b36e-4b71-ad61-b7a5ba332879
keywords:
- errorf 函式 HLSL
topic_type:
- apiref
api_name:
- errorf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76c8fbcd9b6cb15dbbb735296a3aada8f5e568cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022336"
---
# <a name="errorf-function"></a>errorf 函式

將錯誤訊息提交至資訊佇列。

## <a name="syntax"></a>語法

``` syntax
void errorf(
   string format,
    argument ...
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*format* 
</dt> <dd>

格式字串。

</dd> <dt>

*參數。。。* 
</dt> <dd>

選擇性引數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

此作業不會在不支援的裝置上執行任何動作。

### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                        | 支援 |
|---------------------------------------------------------------------|-----------|
| [著色器模型 4 (DirectX HLSL) 或更新版本。](dx-graphics-hlsl-sm3.md) | 是       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




