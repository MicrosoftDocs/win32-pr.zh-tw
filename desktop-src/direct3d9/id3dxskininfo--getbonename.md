---
description: 從骨骼索引取得骨骼名稱。
ms.assetid: f56faf41-c119-4cdd-bb8a-86fc99ff5893
title: 'ID3DXSkinInfo：： GetBoneName 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fa56b175d9047935b9f92829823ba2608536ddabb90cb0ad674b86b73cc17475
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674728"
---
# <a name="id3dxskininfogetbonename-method"></a>ID3DXSkinInfo：： GetBoneName 方法

從骨骼索引取得骨骼名稱。

## <a name="syntax"></a>語法


```C++
LPCSTR GetBoneName(
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

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

傳回骨骼名稱。 請勿釋放這個字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetBoneName**](id3dxskininfo--setbonename.md)
</dt> <dt>

[**ID3DXSkinInfo::GetNumBones**](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
