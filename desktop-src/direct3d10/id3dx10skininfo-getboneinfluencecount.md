---
description: 取得指定之骨骼影響的頂點數目。
ms.assetid: e92361ea-4269-4d63-a8d1-560a486b6563
title: 'ID3DX10SkinInfo：： GetBoneInfluenceCount 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluenceCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5ad6ddc6ebc80c51e07b7ff0c887371fd45fd42b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999010"
---
# <a name="id3dx10skininfogetboneinfluencecount-method"></a>ID3DX10SkinInfo：： GetBoneInfluenceCount 方法

取得指定之骨骼影響的頂點數目。

## <a name="syntax"></a>語法


```C++
UINT GetBoneInfluenceCount(
  [in] UINT BoneIndex
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*BoneIndex* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

指定現有骨骼的索引。 必須介於0和 [**ID3DX10SkinInfo：： GetNumBones**](id3dx10skininfo-getnumbones.md)所傳回的值之間。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **UINT**](../winprog/windows-data-types.md)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是： E \_ INVALIDARG。

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

 

 
