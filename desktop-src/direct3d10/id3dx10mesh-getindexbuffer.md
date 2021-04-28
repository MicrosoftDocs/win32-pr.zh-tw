---
description: ID3DX10Mesh：： GetIndexBuffer 方法-捕獲索引緩衝區中的資料。
ms.assetid: 7e25ad67-7f9d-4c23-a029-a2262034ef38
title: 'ID3DX10Mesh：： GetIndexBuffer 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 751d6dd0376dc73f0213ddb83a19954dc154d633
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084026"
---
# <a name="id3dx10meshgetindexbuffer-method"></a>ID3DX10Mesh：： GetIndexBuffer 方法

抓取索引緩衝區中的資料。

## <a name="syntax"></a>語法


```C++
HRESULT GetIndexBuffer(
  [out] ID3DX10MeshBuffer **ppIndexBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppIndexBuffer* \[擴展\]
</dt> <dd>

類型： **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

ID3DX10MeshBuffer 介面指標的位址，表示與網格相關聯的索引緩衝區。

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

 

 




