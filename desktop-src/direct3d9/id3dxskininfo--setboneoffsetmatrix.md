---
description: 設定骨骼位移矩陣。
ms.assetid: f8ac1117-510d-42af-a6bf-422cbaaf6b74
title: 'ID3DXSkinInfo：： SetBoneOffsetMatrix 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d5daf20697777cfbf1b72d4ab18936f81c262ba9b23379d6089bffca8b9a516
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674708"
---
# <a name="id3dxskininfosetboneoffsetmatrix-method"></a>ID3DXSkinInfo：： SetBoneOffsetMatrix 方法

設定骨骼位移矩陣。

## <a name="syntax"></a>語法


```C++
HRESULT SetBoneOffsetMatrix(
  [in]       DWORD      Bone,
  [in] const D3DXMATRIX *pBoneTransform
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*骨骼* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

骨骼編號。

</dd> <dt>

*pBoneTransform* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***

骨骼位移矩陣的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

[**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md)會傳回骨骼名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::GetBoneOffsetMatrix**](id3dxskininfo--getboneoffsetmatrix.md)
</dt> </dl>

 

 
