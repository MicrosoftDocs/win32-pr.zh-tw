---
description: 呼叫 ID3DXSprite：： Flush，然後將裝置狀態還原為 ID3DXSprite：： Begin 之前的狀態。
ms.assetid: 603c69f7-13a8-4646-b367-6f2d21b1a2a0
title: 'ID3DXSprite：： End 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2991cb8a4ae62b5d9ec71450d8e55fbdcdce050
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386487"
---
# <a name="id3dxspriteend-method"></a>ID3DXSprite：： End 方法

呼叫 [**ID3DXSprite：： Flush**](id3dxsprite--flush.md) ，然後將裝置狀態還原為 [**ID3DXSprite：： Begin**](id3dxsprite--begin.md) 之前的狀態。

## <a name="syntax"></a>語法


```C++
HRESULT End();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL

## <a name="remarks"></a>備註

**ID3DXSprite：： End** 不能用來取代 [**IDirect3DDevice9：： EndScene**](/windows/desktop/api) 或 [**ID3DXRenderToSurface：： EndScene**](id3dxrendertosurface--endscene.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite：： Begin**](id3dxsprite--begin.md)
</dt> </dl>

 

 




