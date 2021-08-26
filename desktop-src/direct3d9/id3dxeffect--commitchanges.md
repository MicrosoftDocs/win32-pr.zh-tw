---
description: 在轉譯之前，將作用中傳遞內發生的狀態變更傳播至裝置。
ms.assetid: 3a779b63-c106-4a81-afeb-82bd6e556de4
title: 'ID3DXEffect：： CommitChanges 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CommitChanges
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5b81cd2674e08473358e031b827528121537264df11dba54c6a1f610ac054ee4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951758"
---
# <a name="id3dxeffectcommitchanges-method"></a>ID3DXEffect：： CommitChanges 方法

在轉譯之前，將作用中傳遞內發生的狀態變更傳播至裝置。

## <a name="syntax"></a>語法


```C++
HRESULT CommitChanges();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="remarks"></a>備註

如果應用程式使用 [**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)ID3DXEffect：： EndPass 比對配對內的任何 [**ID3DXEffect：： Setx**](id3dxeffect.md)方法變更任何效果狀態 / [](id3dxeffect--endpass.md) ，則在轉譯之前，應用程式必須呼叫 **ID3DXEffect：： CommitChanges** ，才能將狀態變更傳播至裝置。 如果 **ID3DXEffect：： BeginPass** 和 **ID3DXEffect：： EndPass** 比對配對中沒有發生狀態變更，則不需要呼叫 **ID3DXEffect：： CommitChanges**。

這對複製效果中的任何共用參數稍有不同。 當某個技術在複製的效果上處於作用中狀態時 (也就是，呼叫 [**ID3DXEffect：： Begin**](id3dxeffect--begin.md) 但未呼叫 [**ID3DXEffect：： End**](id3dxeffect--end.md) 時) ， **ID3DXEffect：： CommitChanges** 會更新未如預期般共用的參數。 若要更新共用參數 (僅適用于其技術為使用中) 的複製效果，請呼叫 **ID3DXEffect：： End** 以停用此技術，並使用 **ID3DXEffect：： Begin** 在呼叫 **ID3DXEffect：： CommitChanges** 之前重新啟用該技術。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




