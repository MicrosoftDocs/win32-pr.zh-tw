---
description: 強制將所有批次中的 sprite 提交至裝置。 裝置狀態會維持在最後一次呼叫 ID3DXSprite：： Begin 之後。 然後會清除批次中的子後 sprite 清單。
ms.assetid: e5717bde-e339-4344-8ce7-b0c3fe118887
title: 'ID3DXSprite：： Flush 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Flush
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3bcd89984672f0dcfa2df120ede1abdfee23d171
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985892"
---
# <a name="id3dxspriteflush-method"></a>ID3DXSprite：： Flush 方法

強制將所有批次中的 sprite 提交至裝置。 裝置狀態會維持在最後一次呼叫 [**ID3DXSprite：： Begin**](id3dxsprite--begin.md)之後。 然後會清除批次中的子後 sprite 清單。

## <a name="syntax"></a>語法


```C++
HRESULT Flush();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite：： End**](id3dxsprite--end.md)
</dt> </dl>

 

 




