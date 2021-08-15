---
description: 啟用現有的骨骼來影響一組頂點，並定義骨骼對每個頂點的影響程度。
ms.assetid: 37ba97a8-ba40-4700-b8b8-fa7cc9118307
title: 'ID3DX10SkinInfo：： AddBoneInfluences 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7f640481c664c51614a45ff10250a4c40d769a27d793868c4bec316c2cab9ded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914344"
---
# <a name="id3dx10skininfoaddboneinfluences-method"></a>ID3DX10SkinInfo：： AddBoneInfluences 方法

啟用現有的骨骼來影響一組頂點，並定義骨骼對每個頂點的影響程度。

## <a name="syntax"></a>語法


```C++
HRESULT AddBoneInfluences(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceCount,
  [in] UINT  *pIndices,
  [in] float *pWeights
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*BoneIndex* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

指定現有骨骼的索引。 必須介於0和 [**ID3DX10SkinInfo：： GetNumBones**](id3dx10skininfo-getnumbones.md)所傳回的值之間。

</dd> <dt>

*InfluenceCount* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要加入至骨骼影響的頂點數目。

</dd> <dt>

*pIndices* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

頂點索引陣列的指標。 這個陣列的每個成員在 pWeights 中都有對應的成員，因此 pIndices \[ 我 \] 對應到 pWeights \[ i \] 。 PWeights i 中的對應值， \[ \] 會決定 BoneIndex 對 pIndices i 所編制索引之頂點的影響程度 \[ \] 。 PIndices 陣列的大小必須等於或大於 InfluenceCount。

</dd> <dt>

*pWeights* \[在\]
</dt> <dd>

類型： **float \***

骨骼加權陣列的指標。 這個陣列的每個成員在 pIndices 中都有對應的成員，因此 pWeights \[ 我 \] 對應到 pIndices \[ i \] 。 PWeights 中的每個值都介於0和1之間，而且會定義骨骼對每個頂點的影響量。 PWeights 的大小必須等於或大於 InfluenceCount。

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

 

 
