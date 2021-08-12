---
description: 強制將所有批次的子層提交至裝置。 裝置狀態會維持在最後一次呼叫 ID3DX10Sprite：： Begin 之後。 然後會清除批次中的子後 sprite 清單。
ms.assetid: ae03e17c-1a14-4a41-a9a9-8757d2f7a81d
title: 'ID3DX10Sprite：： Flush 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Flush
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d74c96ebab8b1e174a44124aaa53b714a9ea860fc9fa2ea5ae3e25c9779aae01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302241"
---
# <a name="id3dx10spriteflush-method"></a>ID3DX10Sprite：： Flush 方法

強制將所有批次的子層提交至裝置。 裝置狀態會維持在最後一次呼叫 ID3DX10Sprite：： Begin 之後。 然後會清除批次中的子後 sprite 清單。

## <a name="syntax"></a>語法


```C++
HRESULT Flush();
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

 

 




