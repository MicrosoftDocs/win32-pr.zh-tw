---
title: RWTexture1DArray：： Load (int) 函數
description: 讀取紋理資料。 |RWTexture1DArray：： Load (int) 函數
ms.assetid: 8A9ABE4A-C9FA-4092-8C2B-24E55645CA64
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
ms.openlocfilehash: 7c918066d2b93b30b72b1ebe620bf623fdeadff81396331a4d08291858db171a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117906284"
---
# <a name="rwtexture1darrayloadint-function"></a>RWTexture1DArray：： Load (int) 函數

讀取紋理資料。

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

材質的位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

輸入：

傳回型別符合 [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) 物件宣告中的型別。

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[載入方法](rwtexture1darray-load.md)
</dt> </dl>

 

 




