---
description: 從自訂應用程式指定的信號計算每個三角形的 IMT，這些信號會隨著格線的表面變化， (通常會高於頂點資料) 的頻率。 信號是透過使用者指定的回呼函數來評估。
ms.assetid: f1d96021-0b7d-43e6-b51b-71a90d2f5ad8
title: 'D3DXComputeIMTFromSignal 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d645e12f7159963f9b9bc5abeb960aee0bac2282537c482465be3ea08690181
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299410"
---
# <a name="d3dxcomputeimtfromsignal-function"></a>D3DXComputeIMTFromSignal 函式

從自訂應用程式指定的信號計算每個三角形的 IMT，這些信號會隨著格線的表面變化， (通常會高於頂點資料) 的頻率。 信號是透過使用者指定的回呼函數來評估。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXComputeIMTFromSignal(
  _In_  LPD3DXMESH              pMesh,
  _In_  DWORD                   dwTextureIndex,
  _In_  UINT                    uSignalDimension,
  _In_  FLOAT                   fMaxUVDistance,
  _In_  DWORD                   dwOptions,
  _In_  LPD3DXIMTSIGNALCALLBACK pSignalCallback,
  _In_  VOID                    *pUserData,
        LPD3DXUVATLASCB         pStatusCallback,
        LPVOID                  pUserContext,
  _Out_ LPD3DXBUFFER            *ppIMTData
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

*uSignalDimension* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

信號中每個資料點的元件數目。

</dd> <dt>

*fMaxUVDistance* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

頂點之間的最大距離;演算法會繼續進行細分，直到所有頂點之間的距離小於或等於 fMaxUVDistance 為止。

</dd> <dt>

*>dwoptions* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

材質換行選項。 這是一或多個 [**D3DXIMT 旗標**](./d3dximt-flags.md)的組合。

</dd> <dt>

*pSignalCallback* \[在\]
</dt> <dd>

類型： **[LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)**

使用者提供的評估工具函式的指標，該函式將用來計算任意 U、V 座標的信號值。 函數會遵循 [LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)的原型。

</dd> <dt>

*pUserData* \[在\]
</dt> <dd>

類型： **VOID \***

傳遞給信號回呼函式的使用者定義值指標。 通常由應用程式用來傳遞資料結構的指標，以提供回呼函數的內容資訊。

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

此函式要求輸入網格必須包含 (ie 的信號到網格材質對應。材質座標) 。 它可讓使用者在網格表面上任意定義信號。

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

 

 
