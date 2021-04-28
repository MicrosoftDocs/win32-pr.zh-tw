---
description: ID3DXMesh：： SetAttributeTable 方法：設定網格的屬性資料表和儲存在資料表中的專案數目。
ms.assetid: 22d46708-cffd-48da-bdad-8a43f9076356
title: 'ID3DXMesh：： SetAttributeTable 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.SetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a4cdb503e934ca00b41482601b59266eee750365
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093346"
---
# <a name="id3dxmeshsetattributetable-method"></a>ID3DXMesh：： SetAttributeTable 方法

設定網格的屬性工作表和儲存在資料表中的專案數目。

## <a name="syntax"></a>語法


```C++
HRESULT SetAttributeTable(
  [in] const D3DXATTRIBUTERANGE *pAttribTable,
  [in]       DWORD              cAttribTableSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAttribTable* \[在\]
</dt> <dd>

Type： **Const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) \***

[**D3DXATTRIBUTERANGE**](d3dxattributerange.md)結構陣列的指標，表示網格屬性工作表中的專案。

</dd> <dt>

*cAttribTableSize* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

網格屬性工作表中的屬性數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

如果應用程式會追蹤屬性工作表中的資訊，並重新排列資料表，使其成為屬性或臉部變更的結果，此方法可讓應用程式更新屬性工作表，而不是再次呼叫 [**ID3DXMesh：： Optimize**](id3dxmesh--optimize.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh::LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

**ID3DXMesh::LockAttributeBuffer**
</dt> </dl>

 

 
