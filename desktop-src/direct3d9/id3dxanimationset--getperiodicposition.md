---
description: 傳回動畫集合的當地時間範圍內的時間位置。
ms.assetid: d822e1d8-f371-43a1-bbcf-2223e28a200a
title: 'ID3DXAnimationSet：： GetPeriodicPosition 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriodicPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8451e3332b61d7e6e993de7df0832a78c0c45c0240633fd5f421998816f7f26f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122059"
---
# <a name="id3dxanimationsetgetperiodicposition-method"></a>ID3DXAnimationSet：： GetPeriodicPosition 方法

傳回動畫集合的當地時間範圍內的時間位置。

## <a name="syntax"></a>語法


```C++
DOUBLE GetPeriodicPosition(
  [in] DOUBLE Position
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*位置* \[在\]
</dt> <dd>

類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**

動畫集合的本機時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**

在動畫集的時間範圍內測量的時間位置。 此值將會受動畫集合的期間所限制。

## <a name="remarks"></a>備註

這個方法所傳回的時間位置可以用來做為 [**ID3DXAnimationSet：： GetSRT**](id3dxanimationset--getsrt.md)的 PeriodicPosition 參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
