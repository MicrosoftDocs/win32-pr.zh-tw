---
description: 準備裝置來繪製線條。
ms.assetid: c597703d-6466-4b55-b1a6-a4e7c667e50c
title: 'ID3DXLine：： Begin 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ee241b39f2d0c1939cf2cb0cc09e079abd3430a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989221"
---
# <a name="id3dxlinebegin-method"></a>ID3DXLine：： Begin 方法

準備裝置來繪製線條。

## <a name="syntax"></a>語法


```C++
HRESULT Begin();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="remarks"></a>備註

呼叫 **ID3DXLine：： Begin** 是選擇性的。 如果在 ID3DXLine：： Begin/ID3DXLine：： End sequence 之外呼叫，draw 函數將會在內部呼叫 ID3DXLine：： Begin 和 ID3DXLine：： End。 為了避免額外負荷，如果連續呼叫多個繪製函數，則應該使用這個方法。

您必須從 [**IDirect3DDevice9：： BeginScene**](/windows/desktop/api) 和 [**IDirect3DDevice9：： EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) 序列內呼叫這個方法。

ID3DXLine：： Begin 不能用來取代 [**IDirect3DDevice9：： BeginScene**](/windows/desktop/api) 或 [**ID3DXRenderToSurface：： BeginScene**](id3dxrendertosurface--beginscene.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
