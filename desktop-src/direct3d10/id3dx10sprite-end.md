---
description: 在 ID3DX10Sprite：： Flush 之後呼叫此動作。 如果 \_ \_ \_ 在呼叫 ID3DX10Sprite：： begin 時指定了 D3DX10 SPRITE SAVE 狀態，此 API 會將裝置狀態還原為在呼叫 ID3DX10Sprite：： begin 之前的狀態。
ms.assetid: 71645edb-be4a-4d87-9fb0-557cf5cf10e5
title: 'ID3DX10Sprite：： End 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.End
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 02cfa1e92275230bd3a853aa9079187181089c46b4e4f193404b9dc0c709c9e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302287"
---
# <a name="id3dx10spriteend-method"></a>ID3DX10Sprite：： End 方法

在 ID3DX10Sprite：： Flush 之後呼叫此動作。 如果 \_ \_ \_ 在呼叫 ID3DX10Sprite：： begin 時指定了 D3DX10 SPRITE SAVE 狀態，此 API 會將裝置狀態還原為在呼叫 ID3DX10Sprite：： begin 之前的狀態。

## <a name="syntax"></a>語法


```C++
HRESULT End();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




