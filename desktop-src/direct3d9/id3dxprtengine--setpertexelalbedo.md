---
description: 設定每個材質的 >albedo 值，並覆寫先前的 >albedo 值。
ms.assetid: 2928c861-a07e-4099-b04f-cdfa41e70874
title: 'ID3DXPRTEngine：： SetPerTexelAlbedo 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce977a1ab28477ab8e40d59d18cfbcc55f558f88
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386478"
---
# <a name="id3dxprtenginesetpertexelalbedo-method"></a>ID3DXPRTEngine：： SetPerTexelAlbedo 方法

設定每個材質的 >albedo 值，並覆寫先前的 >albedo 值。

## <a name="syntax"></a>語法


```C++
HRESULT SetPerTexelAlbedo(
  [in] LPDIRECT3DTEXTURE9        pAlbedoTexture,
  [in] UINT                      NumChannels,
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAlbedoTexture* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

要在其中儲存 >albedo 值之 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) 材質物件的指標。

</dd> <dt>

*NumChannels* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要設定的色彩通道數目。 設定為1以指定灰色材質 (R = G = B) 或3，以啟用色彩不規則效果。

</dd> <dt>

*pGH* \[在\]
</dt> <dd>

類型： **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**

[**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md)物件的選擇性指標。 如果未提供，就會在內部建立並終結材質裝訂邊 helper 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DERR \_ NOTAVAILABLED3DERR \_ OUTOFVIDEOMEMORY、D3DERR \_ WASSTILLDRAWING、E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
