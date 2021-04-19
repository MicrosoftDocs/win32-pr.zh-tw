---
description: 變更哪些骨骼會影響哪些頂點。
ms.assetid: 0955e0ba-ffc5-408b-ab38-2abd39e1c429
title: 'ID3DX10SkinInfo：： RemapBones 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapBones
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 238e4628740fa74e055312c82de2635316f5bde5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988186"
---
# <a name="id3dx10skininforemapbones-method"></a>ID3DX10SkinInfo：： RemapBones 方法

變更哪些骨骼會影響哪些頂點。

## <a name="syntax"></a>語法


```C++
HRESULT RemapBones(
  [in] UINT NewBoneCount,
  [in] UINT *pBoneRemap
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NewBoneCount* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

新的骨骼數目。

</dd> <dt>

*pBoneRemap* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

描述重新對應之骨骼索引陣列的指標。 例如，假設 SkinInfo 包含一些骨骼，例如 bone0 對應至 v0、bone1 至 v1，以及 bone2 為 v2，而且指定了2，1，0的陣列為 pBoneRemap。 這會導致 bone0 對應至 v2、bone1 至 v1，並 bone2 至 v0。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是： E \_ OUTOFMEMORY 或 e \_ INVALIDARG。

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

 

 
