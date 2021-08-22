---
description: 清除網格以進行簡化。
ms.assetid: 2b586ecc-db87-4b20-a4fc-c8b547bebf65
title: 'D3DXCleanMesh 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCleanMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: adc5d60b66dc9eaa06314e18ead26412b8572e9dbc649070c37891a62fb9ecbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495908"
---
# <a name="d3dxcleanmesh-function"></a>D3DXCleanMesh 函式

清除網格以進行簡化。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCleanMesh(
  _In_        D3DXCLEANTYPE CleanType,
  _In_        LPD3DXMESH    pMeshIn,
  _In_  const DWORD         *pAdjacencyIn,
  _Out_       LPD3DXMESH    *ppMeshOut,
  _Out_       DWORD         *pAdjacencyOut,
  _Out_       LPD3DXBUFFER  *ppErrorsAndWarnings
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*CleanType* \[在\]
</dt> <dd>

類型： **[ **D3DXCLEANTYPE**](./d3dxcleantype.md)**

要在準備進行網格清除時執行的頂點作業。 請參閱 [**D3DXCLEANTYPE**](./d3dxcleantype.md)。

</dd> <dt>

*pMeshIn* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

[**ID3DXMesh**](id3dxmesh.md)介面的指標，代表要清除的網格。

</dd> <dt>

*pAdjacencyIn* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

指標，指向每個臉部的三個 Dword 陣列，以指定要清除網格中每個臉部的三個相鄰專案。

</dd> <dt>

*ppMeshOut* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***

[**ID3DXMesh**](id3dxmesh.md)介面指標的位址，表示傳回的已清除網格。 如果不需要進行清理，則會傳回相同的網格。

</dd> <dt>

*pAdjacencyOut* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

指標，指向每個臉部的三個 Dword 陣列，以針對輸出網格中的每個臉部指定三個相鄰專案。

</dd> <dt>

*ppErrorsAndWarnings* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

傳回包含錯誤和警告字串的緩衝區，以說明在網格中找到的問題。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

此函式會使用 CleanType 參數中指定的清除方法和選項來清除網格。 如需可用選項的描述，請參閱 [**D3DXCLEANTYPE**](./d3dxcleantype.md) 列舉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
