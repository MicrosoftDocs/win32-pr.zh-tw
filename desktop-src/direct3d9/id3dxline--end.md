---
description: 將裝置狀態還原為呼叫 ID3DXLine：： Begin 時的狀態。
ms.assetid: 06243c30-2d1d-4101-a373-46fd9a0d88d3
title: 'ID3DXLine：： End 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 371463bfc24cbdba63ac51c9b729c267b9d020dd260d6d1b6c6a378bb38c3524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987228"
---
# <a name="id3dxlineend-method"></a>ID3DXLine：： End 方法

將裝置狀態還原為呼叫 [**ID3DXLine：： Begin**](id3dxline--begin.md) 時的狀態。

## <a name="syntax"></a>語法


```C++
HRESULT End();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="remarks"></a>備註

**ID3DXLine：： End** 不能用來取代 [**IDirect3DDevice9：： EndScene**](/windows/desktop/api) 或 [**ID3DXRenderToSurface：： EndScene**](id3dxrendertosurface--endscene.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine：： Begin**](id3dxline--begin.md)
</dt> </dl>

 

 




