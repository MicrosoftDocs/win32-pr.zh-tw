---
description: D3DXCreateSkinInfo 函式-使用宣告子建立空白的外觀網格物件。
ms.assetid: c98da2e5-a9eb-4070-8846-b346b5c57fb3
title: 'D3DXCreateSkinInfo 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfo
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da582d791b27d30c78583972e6f598af8af3eb9e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102736"
---
# <a name="d3dxcreateskininfo-function"></a>D3DXCreateSkinInfo 函式

使用宣告子建立空白的外觀網格物件。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateSkinInfo(
  _In_        DWORD             NumVertices,
  _In_  const D3DVERTEXELEMENT9 *pDeclaration,
  _In_        DWORD             NumBones,
  _Out_       LPD3DXSKININFO    *ppSkinInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NumVertices* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

外觀網格的頂點數目。

</dd> <dt>

*pDeclaration* \[在\]
</dt> <dd>

Type： **Const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)元素的陣列，描述傳回之網格的頂點格式。

</dd> <dt>

*NumBones* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

外觀網格的骨骼數目。

</dd> <dt>

*ppSkinInfo* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

[**ID3DXSkinInfo**](id3dxskininfo.md)介面指標的位址，表示所建立的面板網格物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是： E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

使用 [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) 來填入這個方法所傳回的空白麵板網格物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
