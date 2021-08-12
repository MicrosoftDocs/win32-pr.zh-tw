---
description: ID3DXEffect：： OnLostDevice 方法-使用此方法釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。 只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。
ms.assetid: f56925d8-17f7-44c5-a371-3cde41804613
title: 'ID3DXEffect：： OnLostDevice 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.OnLostDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d198cb06461fc377933f2dc90c1e3fb687559ef7b83cc7becd9f04bdf1b78d1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118521214"
---
# <a name="id3dxeffectonlostdevice-method"></a>ID3DXEffect：： OnLostDevice 方法

您可以使用此方法來釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。 只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。

## <a name="syntax"></a>語法


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

只要裝置遺失或使用者呼叫 [**IDirect3DDevice9：： Reset**](/windows/desktop/api)，就應該呼叫這個方法。 即使裝置真的沒有遺失， **ID3DXEffect：： OnLostDevice** 也負責釋放 stateblocks 和其他資源，在重設裝置之前可能需要先釋出這些資源。 因此，在呼叫 **IDirect3DDevice9：： Reset** 之前無法再次使用字型物件，然後再呼叫 [**ID3DXEffect：： OnResetDevice**](id3dxeffect--onresetdevice.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




