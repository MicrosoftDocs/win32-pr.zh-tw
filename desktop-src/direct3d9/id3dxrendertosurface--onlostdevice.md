---
description: ID3DXRenderToSurface：： OnLostDevice 方法-使用此方法釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。 只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。
ms.assetid: 8962236d-4801-46a3-9944-a7c4ad762882
title: 'ID3DXRenderToSurface：： OnLostDevice 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 772b678dc4260954c2e03c13d7259565cd896bdc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093109"
---
# <a name="id3dxrendertosurfaceonlostdevice-method"></a>ID3DXRenderToSurface：： OnLostDevice 方法

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

只要裝置遺失或使用者呼叫 [**IDirect3DDevice9：： Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)，就應該呼叫這個方法。 即使裝置真的沒有遺失，ID3DXRenderToSurface：： OnLostDevice 也負責釋放 stateblocks 和其他資源，在重設裝置之前可能需要先釋出這些資源。 因此，在呼叫 **IDirect3DDevice9：： Reset** 之前無法再次使用字型物件，然後再呼叫 ID3DXRenderToSurface：： OnResetDevice。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> </dl>

 

 
