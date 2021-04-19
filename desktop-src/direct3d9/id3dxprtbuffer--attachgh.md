---
description: 將 ID3DXTextureGutterHelper 物件與 ID3DXPRTBuffer 物件建立關聯。
ms.assetid: 095fea82-ac7a-42fa-990a-084715c73823
title: 'ID3DXPRTBuffer：： AttachGH 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AttachGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1ba5afa238107d60620291b50b8f184eb4e5d361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988606"
---
# <a name="id3dxprtbufferattachgh-method"></a>ID3DXPRTBuffer：： AttachGH 方法

將 [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) 物件與 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件建立關聯。

## <a name="syntax"></a>語法


```C++
HRESULT AttachGH(
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pGH* \[在\]
</dt> <dd>

類型： **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**

包含材質裝訂邊資料之物件的 [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) 介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。

## <a name="remarks"></a>備註

[**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md)物件的參考計數會自動遞增1。 將會釋放任何現有的 **ID3DXTextureGutterHelper** 指標。

您必須確保 **ID3DXPRTBuffer：： AttachGH** 呼叫的數目符合 [**ID3DXPRTBuffer：： ReleaseGH**](id3dxprtbuffer--releasegh.md) 呼叫的數目。 在呼叫 **ID3DXPRTBuffer：： ReleaseGH** 之後，不應該再使用 **ID3DXPRTBuffer：： AttachGH** 所傳回的 pGH 指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer::ReleaseGH**](id3dxprtbuffer--releasegh.md)
</dt> </dl>

 

 




