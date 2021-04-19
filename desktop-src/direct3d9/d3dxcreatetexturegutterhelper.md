---
description: 從輸入網格和材質資料建立 ID3DXTextureGutterHelper 物件。
ms.assetid: 1696fc3d-5b35-48cc-a79b-c0d4ed44e420
title: 'D3DXCreateTextureGutterHelper 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureGutterHelper
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8957649f3cef6ea67932579918163613160ee993
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999008"
---
# <a name="d3dxcreatetexturegutterhelper-function"></a>D3DXCreateTextureGutterHelper 函式

從輸入網格和材質資料建立 [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) 物件。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateTextureGutterHelper(
  _In_    UINT                      Width,
  _In_    UINT                      Height,
  _In_    LPD3DXMESH                pMesh,
  _In_    FLOAT                     GutterSize,
  _Inout_ LPD3DXTEXTUREGUTTERHELPER *ppBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*寬度* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

材質的寬度（以圖元為單位）。

</dd> <dt>

*高度* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

紋理的高度（以圖元為單位）。

</dd> <dt>

*pMesh* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

輸入 [**ID3DXMesh**](id3dxmesh.md) 網格物件的指標。

</dd> <dt>

*GutterSize* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

用來過度取樣材質和建立裝訂邊區域的材質數目。 必須至少為1。

</dd> <dt>

*ppBuffer* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)\***

要建立之 [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為 S \_ OK。 如果函式失敗，則傳回值可以是下列其中一個： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

使用 [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) 將場景轉換成新座標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[預先計算 Radiance 傳送函式](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
