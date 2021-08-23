---
description: 取得骨骼的影響數目。
ms.assetid: 6383f990-2989-46b3-a634-b3bb7bd1d65b
title: 'ID3DXSkinInfo：： GetNumBoneInfluences 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetNumBoneInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: abacdaab2feccda81e321f1c73bbb93d15711ba3b3a492f0ca99d33df77d5a1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492208"
---
# <a name="id3dxskininfogetnumboneinfluences-method"></a>ID3DXSkinInfo：： GetNumBoneInfluences 方法

取得骨骼的影響數目。

## <a name="syntax"></a>語法


```C++
DWORD GetNumBoneInfluences(
  [in] DWORD bone
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

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

傳回對骨骼的影響數目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
