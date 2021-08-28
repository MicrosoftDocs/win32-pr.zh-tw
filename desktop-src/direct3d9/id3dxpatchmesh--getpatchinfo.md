---
description: 取得修補程式的屬性。
ms.assetid: 601a3275-25ea-4e16-8297-a9fc1f5fdd49
title: 'ID3DXPatchMesh：： GetPatchInfo 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetPatchInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10b6d327b665b30418478d06d21433614587824eeb481202a9bef202b8727001
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847438"
---
# <a name="id3dxpatchmeshgetpatchinfo-method"></a>ID3DXPatchMesh：： GetPatchInfo 方法

取得修補程式的屬性。

## <a name="syntax"></a>語法


```C++
HRESULT GetPatchInfo(
  [out, retval] LPD3DXPATCHINFO PatchInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*PatchInfo* \[退出，retval\]
</dt> <dd>

類型： **[ **LPD3DXPATCHINFO**](d3dxpatchinfo.md)**

包含 patch 屬性之結構的指標。 如需修補程式屬性的詳細資訊，請參閱 [**D3DXPATCHINFO**](d3dxpatchinfo.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 




