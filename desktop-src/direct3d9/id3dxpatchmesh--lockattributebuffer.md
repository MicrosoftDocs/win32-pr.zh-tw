---
description: 鎖定屬性緩衝區。
ms.assetid: 6e05e613-ca93-41b0-a3b3-a9564ada3b0c
title: 'ID3DXPatchMesh：： LockAttributeBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71e50fdc27f3f50b560324c74f5a1609f900772d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988625"
---
# <a name="id3dxpatchmeshlockattributebuffer-method"></a>ID3DXPatchMesh：： LockAttributeBuffer 方法

鎖定屬性緩衝區。

## <a name="syntax"></a>語法


```C++
HRESULT LockAttributeBuffer(
  [in]          DWORD flags,
  [out, retval] DWORD **ppData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*旗標* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

零或多個鎖定旗標的組合，這些旗標描述要執行的鎖定類型。 針對此方法，有效的旗標為：

-   D3DLOCK \_ 捨棄
-   D3DLOCK \_ 沒有 \_ 中途 \_ 更新
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ READONLY

如需旗標的描述，請參閱 [D3DLOCK](d3dlock.md)。

</dd> <dt>

*ppData* \[退出，retval\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\*\***

緩衝區指標的位址，其中包含網格中每個臉部的 DWORD。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

屬性緩衝區通常會鎖定、寫入，然後解除鎖定以進行讀取。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
