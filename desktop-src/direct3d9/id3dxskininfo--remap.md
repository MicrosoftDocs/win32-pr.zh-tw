---
description: 更新骨骼影響資訊，使其在重新排序之後符合頂點。 如果目標頂點緩衝區已從外部重新排序，則應該呼叫這個方法。
ms.assetid: bff5229f-e547-4ab3-84c6-58b15a7825e9
title: 'ID3DXSkinInfo：：重新對應方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Remap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 657cf0977592a8e19e68b8aeb950c62d404e7cdb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106979869"
---
# <a name="id3dxskininforemap-method"></a>ID3DXSkinInfo：：重新對應方法

更新骨骼影響資訊，使其在重新排序之後符合頂點。 如果目標頂點緩衝區已從外部重新排序，則應該呼叫這個方法。

## <a name="syntax"></a>語法


```C++
HRESULT Remap(
  [in] DWORD NumVertices,
  [in] DWORD *pVertexRemap
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NumVertices* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

要重新對應的頂點數目。

</dd> <dt>

*pVertexRemap* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

DWORD 的陣列，其長度是由 NumVertices 所指定。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

PVertexRemap 中的每個元素會指定該位置的先前頂點索引。 例如，如果頂點位於位置3，但已重新對應到位置5，則 pVertexRemap 的第五個元素應包含3個。 您可以使用 [**ID3DXMesh：： Optimize**](id3dxmesh--optimize.md) 傳回的頂點重新對應陣列。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
