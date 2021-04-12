---
description: 從網格複製每個頂點的 >albedo 值。
ms.assetid: 3a6f1cc2-a870-4463-98df-599d9fbd9d78
title: 'ID3DXPRTEngine：： ExtractPerVertexAlbedo 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ExtractPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed23b75b3113421b6242f49416e4b54bfce336f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946232"
---
# <a name="id3dxprtengineextractpervertexalbedo-method"></a>ID3DXPRTEngine：： ExtractPerVertexAlbedo 方法

從網格複製每個頂點的 >albedo 值。

## <a name="syntax"></a>語法


```C++
HRESULT ExtractPerVertexAlbedo(
  [in] LPD3DXMESH   pMesh,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         NumChanIn
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMesh* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

[**D3DXCreatePRTEngine**](d3dxcreateprtengine.md)中用來建立 [**ID3DXPRTEngine**](id3dxprtengine.md)物件之 [**ID3DXMesh**](id3dxmesh.md)網格物件的指標。

</dd> <dt>

*使用* \[ 方式在\]
</dt> <dd>

類型： **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

要從網格複製的頂點使用方式描述。 請參閱 [**D3DDECLUSAGE**](./d3ddeclusage.md)。

</dd> <dt>

*NumChanIn* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要從網格複製的色彩頻道數目。 設定為1以指定灰色材質 (R = G = B) 或3，以啟用色彩不規則效果。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
