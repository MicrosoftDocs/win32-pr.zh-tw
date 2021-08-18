---
description: Unassociates 具有 ID3DXPRTBuffer 物件的附加 ID3DXTextureGutterHelper 物件。
ms.assetid: 0bd8322a-8af1-4173-bbe3-9134c831cf3a
title: 'ID3DXPRTBuffer：： ReleaseGH 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ReleaseGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5691fc2601624733bb8d41b63140b694bd78027e0f6d548b02984bbc12406a47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120532"
---
# <a name="id3dxprtbufferreleasegh-method"></a>ID3DXPRTBuffer：： ReleaseGH 方法

Unassociates 具有 [**ID3DXPRTBuffer**](id3dxprtbuffer.md)物件的附加 [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md)物件。

## <a name="syntax"></a>語法


```C++
HRESULT ReleaseGH();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。

## <a name="remarks"></a>備註

這個方法會釋放 [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) 介面的指標。

您必須確保 [**ID3DXPRTBuffer：： AttachGH**](id3dxprtbuffer--attachgh.md) 呼叫的數目符合 **ID3DXPRTBuffer：： ReleaseGH** 呼叫的數目。 在呼叫 **ID3DXPRTBuffer：： ReleaseGH** 之後，不應該再使用 **ID3DXPRTBuffer：： AttachGH** 所傳回的 pGH 指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer::AttachGH**](id3dxprtbuffer--attachgh.md)
</dt> </dl>

 

 




