---
description: 將矩陣加入至堆疊。
ms.assetid: 99bc636d-f1fd-4ace-a649-6a1a952927e0
title: 'ID3DXMATRIXStack：:P ush 方法 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Push
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1678ad9481a7c76fdb0e92a0c3b2de66d638de71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993864"
---
# <a name="id3dxmatrixstackpush-method-d3dx9mathh"></a>ID3DXMATRIXStack：:P ush 方法 (D3dx9math .h) 

將矩陣加入至堆疊。

## <a name="syntax"></a>語法


```C++
HRESULT Push();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

這個方法會將堆疊上的專案計數遞增1，以複製目前的矩陣。 隨著新增更多專案，堆疊會動態地成長。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack：： Vemap.gettop**](id3dxmatrixstack--gettop.md)
</dt> <dt>

[**ID3DXMATRIXStack：:P op**](id3dxmatrixstack--pop.md)
</dt> </dl>

 

 




