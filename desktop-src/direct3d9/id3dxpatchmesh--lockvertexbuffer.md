---
description: 鎖定頂點緩衝區。
ms.assetid: f7e4f27d-1b40-4b0d-8173-48a0b15cfc95
title: 'ID3DXPatchMesh：： LockVertexBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d88d8a1da7ae544c5647fc844cda4966cfee7b10
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854035"
---
# <a name="id3dxpatchmeshlockvertexbuffer-method"></a>ID3DXPatchMesh：： LockVertexBuffer 方法

鎖定頂點緩衝區。

## <a name="syntax"></a>語法


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  flags,
  [out, retval] LPVOID *ppData
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
-   D3DLOCK \_ NOOVERWRITE

如需旗標的描述，請參閱 [D3DLOCK](d3dlock.md)。

</dd> <dt>

*ppData* \[退出，retval\]
</dt> <dd>

類型： **[ **LPVOID**](../winprog/windows-data-types.md)\***

\*包含所傳回頂點資料之記憶體緩衝區的 VOID 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

頂點緩衝區通常會鎖定、寫入，然後解除鎖定以進行讀取。

Patch 網格使用16位索引緩衝區。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
