---
description: 驗證網格。
ms.assetid: e5bec2f3-e914-4677-8114-77c71b8a586e
title: 'D3DXValidMesh 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 299092700b015840376f3e4b297d7825366b6083e1458155f5963e1b5b1f4d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749668"
---
# <a name="d3dxvalidmesh-function"></a>D3DXValidMesh 函式

驗證網格。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXValidMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacency,
  _Out_       LPD3DXBUFFER *ppErrorsAndWarnings
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMeshIn* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

[**ID3DXMesh**](id3dxmesh.md)介面的指標，代表要測試的網格。

</dd> <dt>

*pAdjacency* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

指標，指向每個臉部的三個 Dword 陣列，以指定要測試之網格中每個臉部的三個相鄰專案。

</dd> <dt>

*ppErrorsAndWarnings* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

傳回包含錯誤和警告字串的緩衝區，以說明在網格中找到的問題。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DXERR \_ INVALIDMESH、D3DERR \_ INVALIDCALL、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

這個方法會檢查是否有不正確索引來驗證網格。 您可以從偵錯工具輸出取得錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
