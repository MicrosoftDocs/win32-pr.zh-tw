---
title: dst 函數
description: 計算距離向量。 |dst 函數
ms.assetid: 24d22743-5867-49db-8d0a-55cc3625c947
keywords:
- dst 函數 HLSL
topic_type:
- apiref
api_name:
- dst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58ce243cf9a9f3e6118763368445e5bcf26ba4cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853608"
---
# <a name="dst-function"></a>dst 函數

計算距離向量。

## <a name="syntax"></a>語法

``` syntax
fVector dst(
  in fVector src0,
  in fVector src1
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*src0* \[在\]
</dt> <dd>

類型： **[fVector](dx-graphics-hlsl-vector.md)**

第一個向量。

</dd> <dt>

*src1* \[在\]
</dt> <dd>

類型： **[fVector](dx-graphics-hlsl-vector.md)**

第二個向量。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[fVector](dx-graphics-hlsl-vector.md)**

計算距離向量。

## <a name="remarks"></a>備註

這個內建函式提供的功能與端點著色器的 [dst](dst---vs.md)指示相同。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




