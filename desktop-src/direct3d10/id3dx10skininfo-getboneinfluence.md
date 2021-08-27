---
description: 取得指定之骨骼對指定頂點的影響量。
ms.assetid: 0586fdfd-e5b1-4699-b489-c54a0f305ee4
title: 'ID3DX10SkinInfo：： GetBoneInfluence 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9b53f642b6e62bb37c6979602b1ae66e09ffc2eb42a6d47c70c6b895a01ba273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096548"
---
# <a name="id3dx10skininfogetboneinfluence-method"></a>ID3DX10SkinInfo：： GetBoneInfluence 方法

取得指定之骨骼對指定頂點的影響量。

## <a name="syntax"></a>語法


```C++
HRESULT GetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float *pWeight
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*BoneIndex* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

指定現有骨骼的索引。 必須介於0和 [**ID3DX10SkinInfo：： GetNumBones**](id3dx10skininfo-getnumbones.md)所傳回的值之間。

</dd> <dt>

*InfluenceIndex* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

在骨骼的頂點清單中，其會影響的索引。

</dd> <dt>

*pWeight* \[在\]
</dt> <dd>

類型： **float \***

骨骼在頂點上的影響數量，介於0和1之間。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 E \_ INVALIDARG。

## <a name="remarks"></a>備註

使用 ID3DX10SkinInfo：： GetBoneInfluenceCount 來找出骨骼影響的頂點數目。

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

 

 
