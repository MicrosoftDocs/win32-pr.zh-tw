---
description: ID3DXTextureShader：： SetVectorArray 方法-設定4D 向量的陣列。
ms.assetid: 45bc5cb1-b44a-468b-8c80-a639da8a033f
title: 'ID3DXTextureShader：： SetVectorArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetVectorArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0878594baa8828c9cca4eca8dd2c20f225fb530e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090186"
---
# <a name="id3dxtextureshadersetvectorarray-method"></a>ID3DXTextureShader：： SetVectorArray 方法

設定4D 向量的陣列。

## <a name="syntax"></a>語法


```C++
HRESULT SetVectorArray(
  [in]       D3DXHANDLE  hConstant,
  [in] const D3DXVECTOR4 *pVector,
  [in]       UINT        Count
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hConstant* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

向量常數陣列的唯一識別碼。 請參閱 [D3DXHANDLE](d3dxfx.md)。

</dd> <dt>

*pVector* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***

4D 向量的陣列。 請參閱 [**D3DXVECTOR4**](d3dxvector4.md)。

</dd> <dt>

*計數* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

陣列中的向量數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
