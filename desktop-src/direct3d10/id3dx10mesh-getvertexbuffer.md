---
description: 抓取與網格相關聯的頂點緩衝區。
ms.assetid: c69a712b-8964-4a5b-a136-3f24060b7fd8
title: 'ID3DX10Mesh：： GetVertexBuffer 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b78db368f2467c25b4bb4218a314a22027d5d3f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992128"
---
# <a name="id3dx10meshgetvertexbuffer-method"></a>ID3DX10Mesh：： GetVertexBuffer 方法

抓取與網格相關聯的頂點緩衝區。

## <a name="syntax"></a>語法


```C++
HRESULT GetVertexBuffer(
  [in]  UINT              iBuffer,
  [out] ID3DX10MeshBuffer **ppVertexBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*windows.storage.streams.ibuffer* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要取得的頂點緩衝區。 這是索引值。

</dd> <dt>

*ppVertexBuffer* \[擴展\]
</dt> <dd>

類型： **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

頂點緩衝區。 請參閱 [ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
