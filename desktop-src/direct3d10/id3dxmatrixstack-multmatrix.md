---
description: ID3DXMATRIXStack：： MultMatrix 方法 (D3DX10 .h) -決定目前矩陣和指定矩陣的乘積。
ms.assetid: 72388919-e474-4433-b219-41e2d312848e
title: 'ID3DXMATRIXStack：： MultMatrix 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrix
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f881e3df820df87ea948893277950bce3ca289b8f9e0dcc6a4d34d46cca463ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736077"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx10h"></a>ID3DXMATRIXStack：： MultMatrix 方法 (D3DX10 .h) 

決定目前矩陣和指定矩陣的乘積。

## <a name="syntax"></a>語法


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pM* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

要乘以目前矩陣的 D3DXMATRIX 結構指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

這個方法會將指定的矩陣靠右乘以目前的矩陣 (轉換與目前的世界原點) 有關。


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



這個方法不會將專案加入至堆疊中，它會將目前的矩陣取代為目前矩陣和指定矩陣的乘積。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
