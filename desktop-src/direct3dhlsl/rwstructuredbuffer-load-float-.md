---
title: RWStructuredBuffer：： Load (int) 函數
description: 讀取緩衝區資料。 |RWStructuredBuffer：： Load (int) 函數
ms.assetid: 9CB40579-6BF8-468C-81B8-936D9940458E
keywords:
- Load function HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3cc8fbd0cfa18f2ac6c5d7109e8690d829bbde2175e8808865e68e29e63c955
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067754"
---
# <a name="rwstructuredbufferloadint-function"></a>RWStructuredBuffer：： Load (int) 函數

讀取緩衝區資料。

## <a name="syntax"></a>語法


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*位置* \[在\]
</dt> <dd>

類型： **int**

緩衝區的位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

輸入：

傳回型別符合 [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) 物件宣告中的型別。

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[載入方法](rwstructuredbuffer-load.md)
</dt> </dl>

 

 




