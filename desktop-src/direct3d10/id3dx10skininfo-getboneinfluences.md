---
description: 取得指定之骨骼影響的頂點清單，以及骨骼對每個頂點的影響數量清單。
ms.assetid: d1dea694-874d-4f21-87a8-f6b013617544
title: 'ID3DX10SkinInfo：： GetBoneInfluences 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9aead6b1dd381011a922c5bfbc1874976a78417c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196452"
---
# <a name="id3dx10skininfogetboneinfluences-method"></a>ID3DX10SkinInfo：： GetBoneInfluences 方法

取得指定之骨骼影響的頂點清單，以及骨骼對每個頂點的影響數量清單。

## <a name="syntax"></a>語法


```C++
HRESULT GetBoneInfluences(
  [in]      UINT  BoneIndex,
  [in]      UINT  Offset,
  [in]      UINT  Count,
  [in, out] UINT  *pDestIndices,
  [in, out] float *pDestWeights
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*BoneIndex* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

指定現有骨骼的索引。 必須介於0和 [**ID3DX10SkinInfo：： GetNumBones**](id3dx10skininfo-getnumbones.md)所傳回的值之間。

</dd> <dt>

*位移* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

來自骨骼受影響頂點清單頂端的位移。 這必須介於0和 [**ID3DX10SkinInfo：： GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md)所傳回的值之間。

</dd> <dt>

*計數* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要取出的索引和加權數目。 必須介於0和 ID3DX10SkinInfo：： GetBoneInfluenceCount 所傳回的值之間。

</dd> <dt>

*pDestIndices* \[in、out\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

頂點緩衝區中的索引清單，每一個都代表一個由骨骼影響的頂點。 這些值會對應至 pDestWeights 中的值，因此 pDestIndices \[ 我 \] 對應到 pDestWeights \[ i \] 。

</dd> <dt>

*pDestWeights* \[in、out\]
</dt> <dd>

類型： **float \***

此骨骼對每個頂點的影響數量清單。 這些值會對應到 pDestIndices 中的值，因此，pDestWeights \[ i \] 對應到 pDestIndices 的 \[ \] f

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是： E \_ INVALIDARG 或 e \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
