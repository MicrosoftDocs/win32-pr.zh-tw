---
description: 從每個頂點的資料計算每個三角形的 IMT。 此函式可讓您根據網格 (色彩、正常等) 中的任何值來計算 IMT。
ms.assetid: a417a8ad-77b1-49ae-aea0-6a32a154499f
title: 'D3DXComputeIMTFromPerVertexSignal 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerVertexSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b12ea3f15f1a185125da46f575d37ad97dd5622
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997401"
---
# <a name="d3dxcomputeimtfrompervertexsignal-function"></a>D3DXComputeIMTFromPerVertexSignal 函式

從每個頂點的資料計算每個三角形的 IMT。 此函式可讓您根據網格 (色彩、正常等) 中的任何值來計算 IMT。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXComputeIMTFromPerVertexSignal(
  _In_        LPD3DXMESH      pMesh,
  _In_  const FLOAT           *pfVertexSignal,
  _In_        UINT            uSignalDimension,
  _In_        UINT            uSignalStride,
  _In_        DWORD           dwOptions,
              LPD3DXUVATLASCB pStatusCallback,
              LPVOID          pUserContext,
  _Out_       LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMesh* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

輸入網格 (的指標，請參閱 [**ID3DXMesh**](id3dxmesh.md)) ，其中包含用來計算 IMT 的物件幾何。

</dd> <dt>

*pfVertexSignal* \[在\]
</dt> <dd>

Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***

將計算 IMT 的每個頂點資料陣列的指標。 陣列大小是 uSignalStride \* v，其中 v 是網格中的頂點數目。

</dd> <dt>

*uSignalDimension* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

每個頂點的浮點數。

</dd> <dt>

*uSignalStride* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

陣列中每個頂點的位元組數目。 這必須是 sizeof (浮點數中的倍數) 

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

 

 
