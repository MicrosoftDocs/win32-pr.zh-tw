---
description: 您可以使用此方法來釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。 只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。
ms.assetid: 1abc4e01-65c6-4034-8cbb-891a2234ad33
title: 'ID3DXFont：： OnLostDevice 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ae2dc711ffe57a2605a0cc43c7ba673d444105f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000604"
---
# <a name="id3dxfontonlostdevice-method"></a>ID3DXFont：： OnLostDevice 方法

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

只要裝置遺失或使用者呼叫 [**重設**](/windows/desktop/api)之前，都應該呼叫這個方法。 即使裝置實際上未遺失， **OnLostDevice** 仍負責釋放 stateblocks 和其他可能需要先釋出才能重設裝置的資源。 如此一來，在呼叫 **Reset** 然後 [**OnResetDevice**](id3dxfont--onresetdevice.md)之前，無法再次使用字型物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 




