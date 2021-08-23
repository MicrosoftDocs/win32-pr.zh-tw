---
description: 取得骨骼影響的頂點和加權。
ms.assetid: 84cb064b-b6b2-402d-81cc-8c02de6f8b52
title: 'ID3DXSkinInfo：： GetBoneInfluence 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8f49afb4175559bb5338c01c0ebb22fb89801aef5e7cafa62386e25c095ea139
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847301"
---
# <a name="id3dxskininfogetboneinfluence-method"></a>ID3DXSkinInfo：： GetBoneInfluence 方法

取得骨骼影響的頂點和加權。

## <a name="syntax"></a>語法


```C++
HRESULT GetBoneInfluence(
  [in]      DWORD Bone,
  [in, out] DWORD *vertices,
  [in, out] FLOAT *weights
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*骨骼* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

骨骼編號。

</dd> <dt>

*頂點* \[in、out\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

取得由骨骼影響的頂點陣列。

</dd> <dt>

*加權* \[in、out\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

取得由骨骼影響的加權陣列。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

使用 [**ID3DXSkinInfo：： GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md) 來找出骨骼影響的頂點數目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetBoneInfluence**](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
