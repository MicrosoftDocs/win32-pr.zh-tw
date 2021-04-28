---
description: ID3DXMATRIXStack：： Vemap.gettop 方法 (D3DX10 .h) -在堆疊頂端抓取目前的矩陣。
ms.assetid: cf379742-3e7d-4309-a7af-b97348428682
title: 'ID3DXMATRIXStack：： Vemap.gettop 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.GetTop
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d1d96cfe8124b47a9b6ce546379af1313a02ea26
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108036"
---
# <a name="id3dxmatrixstackgettop-method-d3dx10h"></a>ID3DXMATRIXStack：： Vemap.gettop 方法 (D3DX10 .h) 

抓取堆疊頂端的目前矩陣。

## <a name="syntax"></a>語法


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

這個方法會傳回 D3DXMATRIX 結構的指標，代表目前的矩陣。

## <a name="remarks"></a>備註

在後續的堆疊作業之後，這個方法所傳回的 D3DXMATRIX 指標不保證是有效的。

請注意，此方法不會從堆疊頂端移除目前的矩陣;相反地，它只會傳回目前的矩陣。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
