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
ms.openlocfilehash: 712f54b0459bc3e62c61b59d001a5d27dd5a8837
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196173"
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

 

 
