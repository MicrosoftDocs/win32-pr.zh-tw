---
description: 取得網狀索引緩衝區。
ms.assetid: d9152f3b-c8e6-4def-8cf1-a517ca4d34e7
title: 'ID3DXPatchMesh：： GetIndexBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c7b32c5414f72b1dd16a6c309294056e81468f8e039e73d1d43c05d5ac3dd0f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294351"
---
# <a name="id3dxpatchmeshgetindexbuffer-method"></a>ID3DXPatchMesh：： GetIndexBuffer 方法

取得網狀索引緩衝區。

## <a name="syntax"></a>語法


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppIB* \[退出，retval\]
</dt> <dd>

類型： **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***

索引緩衝區的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

索引緩衝區包含頂點緩衝區中的頂點排序。 在呈現網格時，會使用索引緩衝區來存取頂點緩衝區。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
