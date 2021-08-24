---
description: ID3DXRenderToEnvMap：： OnLostDevice 方法-使用此方法釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。 只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。
ms.assetid: 76dcf5f3-0d2f-4388-9b75-c4dbd1c74982
title: 'ID3DXRenderToEnvMap：： OnLostDevice 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65aee3724cf4596f4ab54a1a27fcbb4ba482070c0aa3eb0ba68262fa94d24145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747688"
---
# <a name="id3dxrendertoenvmaponlostdevice-method"></a>ID3DXRenderToEnvMap：： OnLostDevice 方法

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

只要裝置遺失或使用者呼叫 [**IDirect3DDevice9：： Reset**](/windows/desktop/api)，就應該呼叫這個方法。 即使裝置真的沒有遺失， **ID3DXRenderToEnvMap：： OnLostDevice** 也負責釋放 stateblocks 和其他資源，在重設裝置之前可能需要先釋出這些資源。 因此，在呼叫 **IDirect3DDevice9：： Reset** 之前無法再次使用字型物件，然後再呼叫 [**ID3DXRenderToEnvMap：： OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




