---
description: 取得骨骼位移矩陣。
ms.assetid: 99d47635-ffae-4668-a37c-b15442148fa1
title: 'ID3DXSkinInfo：： GetBoneOffsetMatrix 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d10586fc9d4008ebd22b7edf2fa955628ffa0ab703ef70ed06cb2f2cb1fd8d68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492298"
---
# <a name="id3dxskininfogetboneoffsetmatrix-method"></a>ID3DXSkinInfo：： GetBoneOffsetMatrix 方法

取得骨骼位移矩陣。

## <a name="syntax"></a>語法


```C++
LPD3DXMATRIX GetBoneOffsetMatrix(
  [in] DWORD Bone
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*骨骼* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

骨骼編號。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **LPD3DXMATRIX**](d3dxmatrix.md)**

傳回骨骼位移矩陣的指標。 請勿釋放此指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**SetBoneOffsetMatrix**](id3dxskininfo--setboneoffsetmatrix.md)
</dt> <dt>

[**GetNumBones**](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
