---
description: 抓取堆疊頂端的目前矩陣。
ms.assetid: 0e20af0a-a332-4cb5-bf87-2ec75aa170ab
title: 'ID3DXMATRIXStack：： Vemap.gettop 方法 (D3dx9math .h) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e635f2a825bf73234322066910c15af636ec9d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106977131"
---
# <a name="id3dxmatrixstackgettop-method-d3dx9mathh"></a>ID3DXMATRIXStack：： Vemap.gettop 方法 (D3dx9math .h) 

抓取堆疊頂端的目前矩陣。

## <a name="syntax"></a>語法


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***

這個方法會傳回 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標，代表目前的矩陣。

## <a name="remarks"></a>備註

在後續的堆疊作業之後，這個方法所傳回的 [**D3DXMATRIX**](d3dxmatrix.md) 指標不保證是有效的。

請注意，此方法不會從堆疊頂端移除目前的矩陣;相反地，它只會傳回目前的矩陣。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack：:P op**](id3dxmatrixstack--pop.md)
</dt> <dt>

[**ID3DXMATRIXStack：:P ush**](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




