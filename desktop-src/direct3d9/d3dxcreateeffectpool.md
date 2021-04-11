---
description: 建立效果集區。 集區是用來共用效果之間的參數。
ms.assetid: 5b202f85-b32b-4041-8873-0de535c2f59f
title: 'D3DXCreateEffectPool 函式 (D3DX9Effect) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectPool
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 14753500ac15fb0ed30d46b1121431af78e1fe93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196412"
---
# <a name="d3dxcreateeffectpool-function"></a>D3DXCreateEffectPool 函式

建立效果集區。 集區是用來共用效果之間的參數。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateEffectPool(
  _Out_ LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppPool* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***

傳回已建立之集區的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。

如果引數無效，此方法將會傳回 D3DERR \_ INVALIDCALL。

如果方法失敗，傳回值將會是 E \_ 失敗。

## <a name="remarks"></a>備註

針對集區中的效果，具有相同名稱共用值的共用參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果函數](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 




