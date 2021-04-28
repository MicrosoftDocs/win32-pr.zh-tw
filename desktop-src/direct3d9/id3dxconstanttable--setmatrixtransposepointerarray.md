---
description: ID3DXConstantTable：： SetMatrixTransposePointerArray 方法-將指標陣列設定為已轉換的矩陣。
ms.assetid: f2db10cb-a146-412d-8de8-f093253470fd
title: 'ID3DXConstantTable：： SetMatrixTransposePointerArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fefb5a0b62174499a4631f2fe8020c25a3a8efa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115036"
---
# <a name="id3dxconstanttablesetmatrixtransposepointerarray-method"></a>ID3DXConstantTable：： SetMatrixTransposePointerArray 方法

將指標的陣列設定為已轉置的矩陣。

## <a name="syntax"></a>語法


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與常數資料表相關聯的裝置。

</dd> <dt>

*hConstant* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

矩陣常數陣列的唯一識別碼。 請參閱 [D3DXHANDLE](dx9-graphics-reference-effects-constants.md)。

</dd> <dt>

*ppMatrix* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \* \***

已轉置矩陣的指標陣列。 請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。

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

已轉換的矩陣包含資料行主要資料;也就是說，每個向量都包含在資料行中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
