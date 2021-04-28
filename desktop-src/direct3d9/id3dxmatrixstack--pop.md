---
description: ID3DXMATRIXStack：:P op 方法 (D3dx9math) -從堆疊頂端移除目前的矩陣。
ms.assetid: 4c542012-058a-4818-8ec4-27e7d3357ca3
title: 'ID3DXMATRIXStack：:P op 方法 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Pop
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c8d9185d10b9ef98a1fc3499f49c2ccc9c17a366
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093498"
---
# <a name="id3dxmatrixstackpop-method-d3dx9mathh"></a>ID3DXMATRIXStack：:P op 方法 (D3dx9math .h) 

從堆疊頂端移除目前的矩陣。

## <a name="syntax"></a>語法


```C++
HRESULT Pop();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。

## <a name="remarks"></a>備註

請注意，這個方法會將堆疊上的專案計數遞減1，有效地從堆疊頂端移除目前的矩陣，並將矩陣升階到堆疊的頂端。 如果堆疊上目前的專案計數為0，則這個方法會傳回而不會執行任何動作。 如果堆疊上目前的專案計數是1，則這個方法會清空堆疊。

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

[**ID3DXMATRIXStack：:P ush**](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




