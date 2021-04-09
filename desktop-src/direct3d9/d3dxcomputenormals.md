---
description: 計算網格中每個頂點的單位法線。 提供支援繼承應用程式。 使用 D3DXComputeTangentFrameEx 以獲得更好的結果。
ms.assetid: 7c879149-2c4c-4824-9604-e88696cc6ddc
title: 'D3DXComputeNormals 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormals
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f95e5e353c318429f5340d1a831f9ca3050ba3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946150"
---
# <a name="d3dxcomputenormals-function"></a>D3DXComputeNormals 函式

計算網格中每個頂點的單位法線。 提供支援繼承應用程式。 使用 [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) 以獲得更好的結果。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXComputeNormals(
  _Inout_       LPD3DXBASEMESH pMesh,
  _In_    const DWORD          *pAdjacency
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMesh* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

[**ID3DXBaseMesh**](id3dxbasemesh.md)介面的指標，表示正規化的網格物件。

</dd> <dt>

*pAdjacency* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

指標，指向每個臉部的三個 Dword 陣列，以指定所建立漸進式網格中每個臉部的三個相鄰專案。 這個參數是選擇性的，如果未使用，應該設為 **Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為 S \_ OK。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

輸入網格必須以其彈性頂點格式指定 [D3DFVF \_ NORMAL](d3dfvf.md) 旗標， (FVF) 。

頂點的一般是透過平均共用該頂點之所有臉部的法線來產生。

如果有提供連續的，則會忽略複寫的頂點，並對其進行「平滑處理」。 如果未提供連續的，則複寫的頂點在只有臉部明確參考它們時，就會有平均的法線。

此函式只會使用下列輸入參數來呼叫 [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) ：


```
D3DXComputeTangentFrameEx( pMesh,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DDECLUSAGE_NORMAL,
                           0,
                           D3DXTANGENT_GENERATE_IN_PLACE | D3DXTANGENT_CALCULATE_NORMALS,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
