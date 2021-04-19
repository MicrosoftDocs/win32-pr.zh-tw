---
description: 調整所有與指定 submesh 相關聯的範例。 方法適用于計算地下散佈。
ms.assetid: abb9ca6a-5fc2-4986-8a38-29998fe5e537
title: 'ID3DXPRTEngine：： ScaleMeshChunk 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ScaleMeshChunk
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f688a5175e7b50c33dd93d06a4f988a14c062c86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986541"
---
# <a name="id3dxprtenginescalemeshchunk-method"></a>ID3DXPRTEngine：： ScaleMeshChunk 方法

調整所有與指定 submesh 相關聯的範例。 方法適用于計算地下散佈。

## <a name="syntax"></a>語法


```C++
HRESULT ScaleMeshChunk(
  [in]      UINT            uMeshChunk,
  [in]      FLOAT           fScale,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*uMeshChunk* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

在網格中開始調整範例的位置。

</dd> <dt>

*fScale* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

用來將 submesh 中的每個向量相乘的值。

</dd> <dt>

*pDataOut* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

[**ID3DXPRTBuffer**](id3dxprtbuffer.md)物件的指標，用來接收 submesh 中的重新調整範例。

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

 

 
