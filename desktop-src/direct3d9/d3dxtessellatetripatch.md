---
description: 將三角形的較高順序介面 patch Tessellates 為三角形網格。
ms.assetid: bcc9143f-fec0-491a-8d32-1df961b8dade
title: 'D3DXTessellateTriPatch 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateTriPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 61d5a426f9fe3331b85c4a881219319622283820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696623"
---
# <a name="d3dxtessellatetripatch-function"></a>D3DXTessellateTriPatch 函式

將三角形的較高順序介面 patch Tessellates 為三角形網格。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXTessellateTriPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3TRIPATCH_INFO         *pTriPatchInfo,
  _Inout_       LPD3DXMESH              pMesh
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVB* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**

包含修補資料的頂點緩衝區。

</dd> <dt>

*pNumSegs* \[在\]
</dt> <dd>

Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***

指標，指向三個浮點值的陣列，這些值會識別三角形 patch 的每個邊緣在鑲嵌時應除以的區段數目。 請參閱 [**D3DTRIPATCH \_ 資訊**](d3dtripatch-info.md)。

</dd> <dt>

*pInDecl* \[在\]
</dt> <dd>

Type： **Const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

定義頂點資料的頂點宣告結構。 請參閱 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)。

</dd> <dt>

*pTriPatchInfo* \[在\]
</dt> <dd>

類型： **Const [**D3TRIPATCH \_ INFO**](d3dtripatch-info.md) \***

描述三角形修補程式。 請參閱 [**D3DTRIPATCH \_ 資訊**](d3dtripatch-info.md)。

</dd> <dt>

*pMesh* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

所建立之網格的指標。 請參閱 [**ID3DXMesh**](id3dxmesh.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

使用 [**D3DXTriPatchSize**](d3dxtripatchsize.md) 來取得鑲嵌式函數所需的輸出頂點和索引數目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXTessellateRectPatch**](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
