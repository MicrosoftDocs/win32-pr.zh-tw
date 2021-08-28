---
description: 取得 nontransposed 矩陣的陣列。
ms.assetid: 37b08f55-22f1-4b60-8cd4-566a77e7dbd6
title: 'ID3DXBaseEffect：： GetMatrixArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6d94820200cfc4cdc90c0a67562ac84efd57cd5cacb8e2a0ff37fcb91454db33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987788"
---
# <a name="id3dxbaseeffectgetmatrixarray-method"></a>ID3DXBaseEffect：： GetMatrixArray 方法

取得 nontransposed 矩陣的陣列。

## <a name="syntax"></a>語法


```C++
HRESULT GetMatrixArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hParameter* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

唯一識別碼。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*pMatrix* \[擴展\]
</dt> <dd>

類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***

傳回 nontransposed 矩陣的陣列。 請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。

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

如果目的地矩陣大於來源矩陣，則只會填入每個目的地矩陣的左上角元件，而其餘的目的地矩陣元件則會設定為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetMatrixArray**](id3dxbaseeffect--setmatrixarray.md)
</dt> </dl>

 

 
