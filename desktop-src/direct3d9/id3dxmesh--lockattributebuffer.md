---
description: 鎖定包含網格屬性資料的網狀緩衝區，並傳回其指標。
ms.assetid: 17a321b8-bfb4-4018-869f-6b09e0a811eb
title: 'ID3DXMesh：： LockAttributeBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8ca767c6bc223c40d6013b93162de057aac9f4fb1b71303990f9128e4eca1ee6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802151"
---
# <a name="id3dxmeshlockattributebuffer-method"></a>ID3DXMesh：： LockAttributeBuffer 方法

鎖定包含網格屬性資料的網狀緩衝區，並傳回其指標。

## <a name="syntax"></a>語法


```C++
HRESULT LockAttributeBuffer(
  [in]  DWORD Flags,
  [out] DWORD **ppData
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

*ppData* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\*\***

緩衝區指標的位址，其中包含網格中每個臉部的 DWORD。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

如果已呼叫 [**ID3DXMesh：： Optimize**](id3dxmesh--optimize.md) ，則網格也會有可使用 [**ID3DXBaseMesh：： GetAttributeTable**](id3dxbasemesh--getattributetable.md) 方法存取的屬性資料表。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh::UnlockAttributeBuffer**](id3dxmesh--unlockattributebuffer.md)
</dt> <dt>

[**ID3DXBaseMesh::GetAttributeTable**](id3dxbasemesh--getattributetable.md)
</dt> <dt>

[**ID3DXMesh::SetAttributeTable**](id3dxmesh--setattributetable.md)
</dt> </dl>

 

 
