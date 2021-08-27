---
description: 將網格相鄰資訊轉換成點代表的陣列。
ms.assetid: b8914f9c-8550-498d-813d-bb1afe0fb5b2
title: 'ID3DXBaseMesh：： ConvertAdjacencyToPointReps 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertAdjacencyToPointReps
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 729e6b67c68f5a9560cbf0aeab5d8f28b72854be49ebc00fb0f0924a5afa4b38
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096028"
---
# <a name="id3dxbasemeshconvertadjacencytopointreps-method"></a>ID3DXBaseMesh：： ConvertAdjacencyToPointReps 方法

將網格相鄰資訊轉換成點代表的陣列。

## <a name="syntax"></a>語法


```C++
HRESULT ConvertAdjacencyToPointReps(
  [in]      const DWORD *pAdjacency,
  [in, out]       DWORD *pPRep
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAdjacency* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

指標，指向每個臉部的三個 Dword 陣列，為網格中的每個臉部指定三個相鄰專案。 此陣列中的位元組數目必須至少為 3 \* [**ID3DXBaseMesh：： GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD) 。

</dd> <dt>

*pPRep* \[in、out\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

網格的指標，該陣列將以點代表資料填滿網格的每個頂點的一個 DWORD。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
