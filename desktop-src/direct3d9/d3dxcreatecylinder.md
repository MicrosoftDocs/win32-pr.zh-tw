---
description: 使用左手座標系統建立包含圓柱的網格。
ms.assetid: 54b8a59e-d13f-44cb-84c0-f63c7b1ffb1b
title: 'D3DXCreateCylinder 函式 (D3dx9shape) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCylinder
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ec97755d45b21a85e1a73bbcd2214ee4c1e2358f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696671"
---
# <a name="d3dxcreatecylinder-function"></a>D3DXCreateCylinder 函式

使用左手座標系統建立包含圓柱的網格。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateCylinder(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Radius1,
  _In_  FLOAT             Radius2,
  _In_  FLOAT             Length,
  _In_  UINT              Slices,
  _In_  UINT              Stacks,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表與所建立之圓柱網格相關聯的裝置。

</dd> <dt>

*Radius1* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

以負 Z 結尾的半徑。 值應大於或等於 0.0 f。

</dd> <dt>

*Radius2* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

正 Z 端的半徑。 值應大於或等於 0.0 f。

</dd> <dt>

*長度* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

沿著 Z 軸的圓柱長度。

</dd> <dt>

配量 \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

主要軸的磁區數目。

</dd> <dt>

*堆疊* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

沿著主要軸的堆疊數目。

</dd> <dt>

*ppMesh* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***

輸出圖形（ [**ID3DXMesh**](id3dxmesh.md) 介面）指標的位址。

</dd> <dt>

*ppAdjacency* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址。 當方法傳回時，此參數會填入三個 Dword 的陣列，每個臉部會針對網格中的每個臉部指定三個相鄰專案。 您可以指定 **Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

建立的圓柱會以原點為中心，而且其軸會對齊 Z 軸。

此函式會使用 D3DXMESH \_ MANAGED 建立選項建立網格，並 [D3DFVF \_ XYZ \| D3DFVF \_ 標準](d3dfvf.md) 的彈性頂點格式 (FVF) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9shape。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[圖形繪圖函數](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
