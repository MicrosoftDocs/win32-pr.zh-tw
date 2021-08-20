---
description: 計算紋理階段中指定之材質座標的正切向量。 提供支援繼承應用程式。 使用 D3DXComputeTangentFrameEx 以獲得更好的結果。
ms.assetid: 39748459-3f9b-4b48-ae13-7143eb29c292
title: 'D3DXComputeTangent 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangent
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 733a881d7a090aff72ae145260222136f6eeb0d2f003df101c69697acb7529de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117910947"
---
# <a name="d3dxcomputetangent-function"></a>D3DXComputeTangent 函式

計算紋理階段中指定之材質座標的正切向量。 提供支援繼承應用程式。 使用 [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) 以獲得更好的結果。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXComputeTangent(
  _In_       LPD3DXMESH Mesh,
  _In_       DWORD      TexStageIndex,
  _In_       DWORD      TangentIndex,
  _In_       DWORD      BinormIndex,
  _In_       DWORD      Wrap,
  _In_ const DWORD      *pAdjacency
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*網格* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

代表輸入網格之 [**ID3DXMesh**](id3dxmesh.md) 介面的指標。

</dd> <dt>

*TexStageIndex* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

表示紋理階段的索引。

</dd> <dt>

*TangentIndex* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

為正切資料提供使用方式索引的索引。 頂點宣告表示使用方式;此索引會使用使用方式索引來修改使用方式。 如需頂點宣告的詳細資訊，請參閱 [ (Direct3D 9) 的頂點 ](vertex-declaration.md)宣告。

</dd> <dt>

*BinormIndex* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

提供 binormal 資料之使用方式索引的索引。 頂點宣告表示使用方式;此索引會使用使用方式索引來修改使用方式。 如需頂點宣告的詳細資訊，請參閱 [ (Direct3D 9) 的頂點 ](vertex-declaration.md)宣告。

</dd> <dt>

*換行* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

將此值設定為0表示不換行，或設定為1以換行您的和 V 指示。

</dd> <dt>

*pAdjacency* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

要填入相鄰臉部索引的每個臉部陣列的指標。 此陣列中的位元組數目必須至少為 ( (3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD) ) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為 S \_ OK。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

如果網格頂點宣告指定了正切函數或 binormal 欄位， **D3DXComputeTangent** 將會更新任何使用者提供的正切函數或 binormal 資料。 或者，將 TangentIndex 設定為 [D3DX \_ 預設](other-d3dx-constants.md) 為不更新使用者提供的正切資料，或將 BINORMINDEX 設定為 D3DX \_ 預設為不更新使用者提供的 binormal 資料。 TexStageIndex 不能設定為 D3DX \_ 預設值。

**D3DXComputeTangent** 取決於包含 binormal 欄位 (BinormIndex) 、正切欄位 (TangentIndex) 或兩者的網格頂點宣告。 如果兩者都不存在，此函式將會失敗。

此函式只會使用下列輸入參數來呼叫 [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) ：


```
D3DXComputeTangentFrameEx( Mesh,
                           D3DDECLUSAGE_TEXCOORD,
                           TexStageIndex,
                           ( BinormIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_BINORMAL,
                               // provides backward function compatibility
                           BinormIndex,
                           ( TangentIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_TANGENT,
                           TangentIndex,
                           D3DX_DEFAULT, // do not store normals
                           0,
                           ( Wrap ? D3DXTANGENT_WRAP_UV : 0 )
                               | D3DXTANGENT_GENERATE_IN_PLACE
                               | D3DXTANGENT_ORTHOGONALIZE_FROM_U,
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

 

 
