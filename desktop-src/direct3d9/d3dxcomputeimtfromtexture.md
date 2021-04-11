---
description: 從對應至網格的材質計算每個三角形的 IMT，以選擇性地當做 D3DX UVAtlas 函式的輸入使用。
ms.assetid: 6671edc4-e494-4847-ae99-b9e56651a875
title: 'D3DXComputeIMTFromTexture 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2fbed0411f3562e3a05ec2ec4df99dfad6d8c902
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035402"
---
# <a name="d3dxcomputeimtfromtexture-function"></a>D3DXComputeIMTFromTexture 函式

從對應至網格的材質計算每個三角形的 IMT，以選擇性地當做 D3DX [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)函式的輸入使用。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXComputeIMTFromTexture(
  _In_  LPD3DXMESH         pMesh,
  _In_  LPDIRECT3DTEXTURE9 pTexture,
  _In_  DWORD              dwTextureIndex,
  _In_  DWORD              dwOptions,
        LPD3DXUVATLASCB    pStatusCallback,
        LPVOID             pUserContext,
  _Out_ LPD3DXBUFFER       *ppIMTData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMesh* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

輸入網格 (的指標，請參閱 [**ID3DXMesh**](id3dxmesh.md)) ，其中包含用來計算 IMT 的物件幾何。

</dd> <dt>

*pTexture* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

紋理的指標 (查看對應至網格的 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)) 。

</dd> <dt>

*dwTextureIndex* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

以零為基礎的材質座標索引，識別要使用的材質座標集。

</dd> <dt>

*>dwoptions* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

材質換行選項。 這是一或多個 [**D3DXIMT 旗標**](./d3dximt-flags.md)的組合。

</dd> <dt>

*pStatusCallback* 
</dt> <dd>

類型： **[LPD3DXU加值稅LASCB](lpd3dxuvatlascb.md)**

回呼函式的指標，可監視 IMT 計算進度。

</dd> <dt>

*pUserCoNtext* 
</dt> <dd>

類型： **[ **LPVOID**](../winprog/windows-data-types.md)**

使用者自訂變數的指標，該變數會傳遞至狀態回呼函數。 通常由應用程式用來傳遞資料結構的指標，以提供回呼函數的內容資訊。

</dd> <dt>

*ppIMTData* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

緩衝區的指標 (查看包含所傳回 IMT 陣列的 [**ID3DXBuffer**](id3dxbuffer.md)) 。 您可以提供此陣列作為 D3DX [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) 函式的輸入，來排列材質參數化中材質配置的優先順序。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D 正常」， \_ 否則值為 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

如果紋理對應到網格的表面，演算法就會計算每個臉部的 IMT。 當參數化 UVAtlas 函式時，這會導致包含較低頻率信號資料的三角形，在最終紋理塔中佔用較少的空間。 紋理會假設是透過網格 bilinearly 來插入。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[UVAtlas 函式](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[使用 UVAtlas (Direct3D 9) ](using-uvatlas.md)
</dt> </dl>

 

 
