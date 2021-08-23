---
description: 產生網格邊緣清單以及共用每個邊緣的修補程式。
ms.assetid: 024528c0-2c0d-4448-9b38-05cf8d6ffc63
title: 'ID3DXPatchMesh：： GenerateAdjacency 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 41e821d853a8a8f981f1174d654f17475c0363cdcc97bb537e308ccd72e38190
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987198"
---
# <a name="id3dxpatchmeshgenerateadjacency-method"></a>ID3DXPatchMesh：： GenerateAdjacency 方法

產生網格邊緣清單以及共用每個邊緣的修補程式。

## <a name="syntax"></a>語法


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT fTolerance
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fTolerance* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

指定在位置中差異小於容錯的頂點應視為重合。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

在應用程式產生網格的相鄰資訊之後，可以將網格資料優化，以提升繪製效能。 這個方法會判斷哪些修補程式在提供的容錯) 內 (相鄰。 這項資訊會在內部使用，以優化鑲嵌式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**ID3DXPatchMesh：： Optimize**](id3dxpatchmesh--optimize.md)
</dt> </dl>

 

 
