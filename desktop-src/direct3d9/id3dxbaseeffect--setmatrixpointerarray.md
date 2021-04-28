---
description: ID3DXBaseEffect：： SetMatrixPointerArray 方法-將指標陣列設定為 nontransposed 矩陣。
ms.assetid: f2e62470-6882-49d8-ae12-6c5b79dd5c99
title: 'ID3DXBaseEffect：： SetMatrixPointerArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixPointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cfe30e0132cfa237ddbccc24758b35e102a62b0c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093766"
---
# <a name="id3dxbaseeffectsetmatrixpointerarray-method"></a>ID3DXBaseEffect：： SetMatrixPointerArray 方法

設定 nontransposed 矩陣的指標陣列。

## <a name="syntax"></a>語法


```C++
HRESULT SetMatrixPointerArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hParameter* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

唯一識別碼。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*ppMatrix* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \* \***

Nontransposed 矩陣的指標陣列。 請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。

</dd> <dt>

*計數* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

陣列中的矩陣數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

Nontransposed 矩陣包含資料列主要資料;也就是說，每個向量都包含在資料列中。

如果目的地矩陣小於來源矩陣，則會忽略來源矩陣的其他元件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetMatrixArray**](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
