---
description: 網格的計算正切函數、binormal 和一般向量。
ms.assetid: 54edb9a5-440d-4191-a58f-296e5b804e0c
title: 'D3DXComputeTangentFrame 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrame
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 532b265f387179d88581f6f0a05227162de6a8402e324e7be2e13a16ca4a3ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849828"
---
# <a name="d3dxcomputetangentframe-function"></a>D3DXComputeTangentFrame 函式

網格的計算正切函數、binormal 和一般向量。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXComputeTangentFrame(
  _In_ ID3DXMesh *pMesh,
  _In_ DWORD     dwOptions
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMesh* \[在\]
</dt> <dd>

類型： **[ **ID3DXMesh**](id3dxmesh.md)\***

輸入 [**ID3DXMesh**](id3dxmesh.md) 網格物件的指標。

</dd> <dt>

*>dwoptions* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

一或多個 [**D3DXTANGENT**](./d3dxtangent.md) 旗標的組合。

使用 **Null** 來指定下列選項：

-   以弧度為單位，以弧度為單位來加權標準向量長度，以弧度為單位，subtended 由兩個邊緣離開頂點。
-   從 UV 材質座標計算正笛笛卡兒座標。
-   紋理不是以 U 或 V 方向包裝
-   相對於材質座標的部分衍生會正規化。
-   頂點會依每個三角形的逆時針方向排序。
-   使用已存在於輸入網格中的每個頂點一般向量。
-   結果會儲存在原始的輸入網格中。 如果需要建立新的頂點，函式將會失敗。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為 S \_ OK。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

此函式只會使用下列輸入參數來呼叫 [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) ：


```
D3DXComputeTangentFrameEx(pMesh, D3DDECLUSAGE_TEXCOORD, 0,   
      D3DDECLUSAGE_BINORMAL, 0, D3DDECLUSAGE_TANGENT, 0, 
      D3DDECLUSAGE_NORMAL, 0, 
      dwOptions | D3DXTANGENT_GENERATE_IN_PLACE,
      NULL, 0.01f, 0.25f, 0.01f, NULL, NULL);
```



藉由群組邊緣和分割頂點，Singularities 會視需要進行處理。 如果需要分割任何頂點，函數將會失敗。 每個頂點上計算的一般向量一律會正規化為具有單位長度。

適用于計算正笛笛卡兒座標的最穩固解決方案，是不要設定 D3DXTANGENT ORTHOGONALIZE 的旗標， \_ \_ \_ 並 \_ \_ 從 V D3DXTANGENT ORTHOGONALIZE \_ ，以便從 UV 材質座標計算正向座標。 不過，在此情況下，如果 U 或 V 為零，則函式會使用 D3DXTANGENT \_ ORTHOGONALIZE \_ 從 \_ V 或 \_ \_ 從 \_ U 分別 D3DXTANGENT ORTHOGONALIZE 來計算正向座標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md)
</dt> <dt>

[**D3DXTANGENT**](./d3dxtangent.md)
</dt> </dl>

 

 
