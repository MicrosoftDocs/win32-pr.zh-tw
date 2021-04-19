---
description: 計算網格的周框球體。
ms.assetid: efa1365b-fe3a-4165-a3cb-bc1cd2ba03c0
title: 'D3DXComputeBoundingSphere 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c9e6a0c9fb67abe8a98ccf8b3f9b895fd63fc3e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997402"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx9meshh"></a>D3DXComputeBoundingSphere 函式 (D3DX9Mesh) 

計算網格的周框球體。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pCenter,
  _Out_       FLOAT       *pRadius
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFirstPosition* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***

第一個位置的指標。

</dd> <dt>

*NumVertices* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

頂點數目。

</dd> <dt>

*dwStride* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

位置向量之間的位元組數目。 使用 [**GetNumBytesPerVertex**](id3dxbasemesh--getnumbytespervertex.md)、 [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md)或 [**D3DXGetDeclVertexSize**](d3dxgetdeclvertexsize.md) 來取得頂點跨距。

</dd> <dt>

*pCenter* \[擴展\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***

[**D3DXVECTOR3**](d3dxvector3.md) 結構，定義傳回之周框球體的座標中心。

</dd> <dt>

*pRadius* \[擴展\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

傳回之周框球體的半徑。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
