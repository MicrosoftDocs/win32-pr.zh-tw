---
description: 設定最小的骨骼影響。 影響小於此值的值會被忽略。
ms.assetid: 9af19c9e-bb6e-4f93-973f-5c38f88eea3d
title: 'ID3DXSkinInfo：： SetMinBoneInfluence 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetMinBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 03e3aeeed31a58231644784ba5070bc9422f7820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997367"
---
# <a name="id3dxskininfosetminboneinfluence-method"></a>ID3DXSkinInfo：： SetMinBoneInfluence 方法

設定最小的骨骼影響。 影響小於此值的值會被忽略。

## <a name="syntax"></a>語法


```C++
HRESULT SetMinBoneInfluence(
  [in] FLOAT MinInfl
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*MinInfl* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

最小影響值。 影響小於此值的值會被忽略。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::GetMinBoneInfluence**](id3dxskininfo--getminboneinfluence.md)
</dt> </dl>

 

 
