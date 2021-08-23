---
description: 從緩衝區的色頻中，將係數資料從指定的係數範圍中解壓縮，並將資料加入至 IDirect3DTexture9 物件。
ms.assetid: 75854676-706a-4675-857e-4f2f8fc8365b
title: 'ID3DXPRTBuffer：： ExtractTexture 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6f91186a15aa166928103073fdaca30d79809ad8c0a522abf3b136cb20a1d43a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120622"
---
# <a name="id3dxprtbufferextracttexture-method"></a>ID3DXPRTBuffer：： ExtractTexture 方法

從緩衝區的色頻中，將係數資料從指定的係數範圍中解壓縮，並將資料加入至 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) 物件。

## <a name="syntax"></a>語法


```C++
HRESULT ExtractTexture(
  [in] UINT               Channel,
  [in] UINT               StartCoefficient,
  [in] UINT               NumCoefficients,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*頻道* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

用來將材質資料解壓縮的緩衝區色彩通道。

</dd> <dt>

*StartCoefficient* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要從中解壓縮紋理資料之緩衝區係數的起始值。

</dd> <dt>

*NumCoefficients* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

從 StartCoefficient 開始解壓縮紋理資料的純量值。

</dd> <dt>

*pTexture* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)紋理物件的指標，該物件會儲存係數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
