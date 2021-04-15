---
description: 設定所有 sprite 的投射矩陣。
ms.assetid: cb4c5546-1a31-40d9-a943-af4fbddcee01
title: 'ID3DX10Sprite：： SetProjectionTransform 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.SetProjectionTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c49fb570f87c8c86313e1f4adcf1560fee909433
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514717"
---
# <a name="id3dx10spritesetprojectiontransform-method"></a>ID3DX10Sprite：： SetProjectionTransform 方法

設定所有 sprite 的投射矩陣。

## <a name="syntax"></a>語法


```C++
HRESULT SetProjectionTransform(
  [in] D3DXMATRIX *pProjectionTransform
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pProjectionTransform* \[在\]
</dt> <dd>

類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

要用於所有 sprite 的投射矩陣。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
