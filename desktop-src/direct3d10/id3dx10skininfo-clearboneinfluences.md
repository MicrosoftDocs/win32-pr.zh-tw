---
description: 清除其所影響之骨骼的頂點清單。
ms.assetid: 1ba6f43a-1f85-4057-b0ed-247cc38d4932
title: 'ID3DX10SkinInfo：： ClearBoneInfluences 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.ClearBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0dfe086738d65336c3cc2d1dbdfd793cbe0b84d916b5815b8533db8a45612efd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914294"
---
# <a name="id3dx10skininfoclearboneinfluences-method"></a>ID3DX10SkinInfo：： ClearBoneInfluences 方法

清除其所影響之骨骼的頂點清單。

## <a name="syntax"></a>語法


```C++
HRESULT ClearBoneInfluences(
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

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

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

 

 
