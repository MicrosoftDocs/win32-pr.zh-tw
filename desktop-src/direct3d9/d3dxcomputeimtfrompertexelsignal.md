---
description: 計算每個材質資料的每個三角形 IMT。 此函式類似于 D3DXComputeIMTFromTexture，但它會使用浮點數陣列來傳入資料，而且它可以計算高於4的維度值。
ms.assetid: 4a151184-e67e-41e9-83c6-63da72f262fa
title: 'D3DXComputeIMTFromPerTexelSignal 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerTexelSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3db71fbc931f7bdb3e73c8d949a163607e66c31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981836"
---
# <a name="d3dxcomputeimtfrompertexelsignal-function"></a>D3DXComputeIMTFromPerTexelSignal 函式

計算每個材質資料的每個三角形 IMT。 此函式類似于 [**D3DXComputeIMTFromTexture**](d3dxcomputeimtfromtexture.md)，但它會使用浮點數陣列來傳入資料，而且它可以計算高於4的維度值。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXComputeIMTFromPerTexelSignal(
  _In_  LPD3DXMESH      pMesh,
  _In_  DWORD           dwTextureIndex,
  _In_  FLOAT           *pfTexelSignal,
  _In_  UINT            uWidth,
  _In_  UINT            uHeight,
  _In_  UINT            uSignalDimension,
  _In_  UINT            uComponents,
  _In_  DWORD           dwOptions,
        LPD3DXUVATLASCB pStatusCallback,
        LPVOID          pUserContext,
  _Out_ LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMesh* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

輸入網格 (的指標，請參閱 [**ID3DXMesh**](id3dxmesh.md)) ，其中包含用來計算 IMT 的物件幾何。

</dd> <dt>

*dwTextureIndex* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

以零為基礎的材質座標索引，識別要使用的材質座標集。

</dd> <dt>

*pfTexelSignal* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

將計算 IMT 的輸入材質陣列指標。 陣列大小是 uWidth \* uHeight \* uComponents。

</dd> <dt>

*uWidth* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

材質寬度（以圖元為單位）。

</dd> <dt>

*uHeight* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

材質高度（以圖元為單位）。

</dd> <dt>

*uSignalDimension* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

每個元件在信號陣列的每個元素中的浮點數。

</dd> <dt>

*uComponents* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

每個材質中的元件數目。

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

 

 
