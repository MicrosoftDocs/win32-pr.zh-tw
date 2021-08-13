---
description: 為三角形清單產生優化的臉部重新對應。
ms.assetid: 428c2af8-43e7-4cf7-8b9b-04ba5cff82c8
title: 'D3DXOptimizeFaces 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeFaces
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 165f81d9b829ce7a7b22ced6fb37851f926ed861f11b79feca3a63c763dabbb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525227"
---
# <a name="d3dxoptimizefaces-function"></a>D3DXOptimizeFaces 函式

為三角形清單產生優化的臉部重新對應。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXOptimizeFaces(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pFaceRemap
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pIndices* \[在\]
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**

用來排序頂點的三角形清單索引指標。

</dd> <dt>

*NumFaces* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

三角形清單中的臉部數目。 若為16位網格，這僅限於 2 ^ 16-1 (65535) 或較少的臉部。

</dd> <dt>

*NumVertices* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

三角形清單所參考的頂點數目。

</dd> <dt>

*Indices32Bit* \[在\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

表示索引類型的旗標：如果索引是32位 (65535 個以上的索引) ，則為 **TRUE** ，如果索引為16位 (65535 或較少的索引) ，則為 **FALSE** 。

</dd> <dt>

*pFaceRemap* \[in、out\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

已分割以產生目前臉部的原始網狀臉部指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

這個函式的優化程式在功能上相當於呼叫 [**ID3DXMesh：： Optimize**](id3dxmesh--optimize.md) WITH with D3DXMESHOPT \_ DEVICEINDEPENDENT 旗標，但此函式可讓您更有效率地使用頂點快取。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
