---
description: 結束主動傳遞。
ms.assetid: e20b3e0f-db9f-48e8-ab4e-761a5861f3ce
title: 'ID3DXEffect：： EndPass 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b43cff0f14c418d08bb6d042301aa5979370b6c5f2bca16ecbc8f215ed51fd43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119372220"
---
# <a name="id3dxeffectendpass-method"></a>ID3DXEffect：： EndPass 方法

結束主動傳遞。

## <a name="syntax"></a>語法


```C++
HRESULT EndPass();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

這個方法一律會傳回值 S \_ OK。

## <a name="remarks"></a>備註

應用程式會藉由呼叫 **ID3DXEffect：： EndPass** 來表示呈現作用中階段的結束。 每個 **ID3DXEffect：： EndPass** 都必須是成對的 [**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md) 和 **ID3DXEffect：： EndPass** 呼叫的一部分。

每一組相符的 [**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md) 和 **ID3DXEffect：： EndPass** 呼叫都必須位於成對的 [**ID3DXEffect：： Begin**](id3dxeffect--begin.md) 和 [**ID3DXEffect：： End**](id3dxeffect--end.md) 呼叫中。

如果應用程式使用 [**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)ID3DXEffect：： EndPass 比對配對內的任何 [**effect：： Setx**](id3dxeffect.md)方法變更任何效果狀態 /  ，則在轉譯之前，應用程式必須呼叫 [**ID3DXEffect：： CommitChanges**](id3dxeffect--commitchanges.md) ，才能將狀態變更傳播至裝置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




