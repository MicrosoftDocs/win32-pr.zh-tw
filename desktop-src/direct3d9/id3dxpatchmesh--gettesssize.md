---
description: 取得鑲嵌層級的鑲嵌網格大小。
ms.assetid: 86d1d1a0-1934-40e9-bff9-6c435d1e5183
title: 'ID3DXPatchMesh：： GetTessSize 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetTessSize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4668f50236684f104aedf0ad9ecad413a583facbc45d5f3fa0331abb5938bf5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493048"
---
# <a name="id3dxpatchmeshgettesssize-method"></a>ID3DXPatchMesh：： GetTessSize 方法

取得鑲嵌層級的鑲嵌網格大小。

## <a name="syntax"></a>語法


```C++
HRESULT GetTessSize(
  [in]  FLOAT fTessLevel,
  [in]  DWORD Adaptive,
  [out] DWORD *NumTriangles,
  [out] DWORD *NumVertices
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fTessLevel* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

鑲嵌式層級。

</dd> <dt>

*適應性* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

適應性鑲嵌。 若為適應性鑲嵌，請將此值設定為 **TRUE** ，並將 fTessLevel 設定為最大鑲嵌值。 這會導致自動調整鑲嵌所需的最大網格大小。

</dd> <dt>

*NumTriangles* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

鑲嵌網格所產生的三角形數目指標。

</dd> <dt>

*NumVertices* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

鑲嵌網格所產生之頂點數目的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

這個方法會採用統一鑲嵌。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
