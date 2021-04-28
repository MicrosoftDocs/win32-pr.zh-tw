---
description: ID3DXMATRIXStack：： LoadMatrix 方法 (D3DX10 .h) -將指定的矩陣載入至目前的矩陣。
ms.assetid: b898f344-db90-48e0-b457-0eb8d7b31dca
title: 'ID3DXMATRIXStack：： LoadMatrix 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadMatrix
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 20c80f578abd5e35c89f3ecccedd2ab7fd59e812
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107956"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx10h"></a>ID3DXMATRIXStack：： LoadMatrix 方法 (D3DX10 .h) 

將指定的矩陣載入至目前的矩陣。

## <a name="syntax"></a>語法


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pM* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

載入至目前矩陣的 D3DXMATRIX 結構指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

請注意，這個方法不會將專案新增至堆疊。相反地，它會將目前的矩陣取代為提供的矩陣。

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

 

 
