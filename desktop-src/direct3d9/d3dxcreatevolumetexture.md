---
description: 建立空的磁片區材質，視需要調整呼叫參數。
ms.assetid: 8fc515cd-2fb3-40c7-8192-a41d93ac1e99
title: 'D3DXCreateVolumeTexture 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 50baf125d2e5375bddb63a41a0d10ae063a57b78
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946103"
---
# <a name="d3dxcreatevolumetexture-function"></a>D3DXCreateVolumeTexture 函式

建立空的磁片區材質，視需要調整呼叫參數。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateVolumeTexture(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  UINT                     Width,
  _In_  UINT                     Height,
  _In_  UINT                     Depth,
  _In_  UINT                     MipLevels,
  _In_  DWORD                    Usage,
  _In_  D3DFORMAT                Format,
  _In_  D3DPOOL                  Pool,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與磁片區材質相關聯的裝置。

</dd> <dt>

*寬度* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

寬度（以圖元為單位）。 此值必須為非零。 驅動程式支援 (寬度、高度和深度) 的最大維度可在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 MaxVolumeExtent 中找到。

</dd> <dt>

*高度* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

高度（以圖元為單位）。 此值必須為非零。 驅動程式支援 (寬度、高度和深度) 的最大維度可在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 MaxVolumeExtent 中找到。

</dd> <dt>

*深度* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

以圖元為單位的深度。 此值必須為非零。 驅動程式支援 (寬度、高度和深度) 的最大維度可在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 MaxVolumeExtent 中找到。

</dd> <dt>

*MipLevels* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要求的 mip 層級數目。 如果此值為零或 D3DX \_ 預設值，則會建立完整的 mipmap 鏈。

</dd> <dt>

*使用* \[ 方式在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

0或 D3DUSAGE \_ 動態。 如需使用動態紋理的詳細資訊，請參閱 [使用動態紋理](performance-optimizations.md)。

</dd> <dt>

*格式* \[在\]
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)**

[D3DFORMAT](d3dformat.md)列舉型別的成員，描述磁片區材質所要求的像素格式。 傳回的磁片區材質可能與以格式指定的格式不同。 應用程式應該檢查所傳回之磁片區材質的格式。

</dd> <dt>

*集* \[ 區在\]
</dt> <dd>

類型： **[ **D3DPOOL**](./d3dpool.md)**

[**D3DPOOL**](./d3dpool.md)列舉型別的成員，描述應放置磁片區材質的記憶體類別。

</dd> <dt>

*ppVolumeTexture* \[擴展\]
</dt> <dd>

類型： **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***

[**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)介面指標的位址，表示已建立的磁片區材質物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DERR \_ INVALIDCALL、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

就內部而言，D3DXCreateVolumeTexture 會使用 [**D3DXCheckVolumeTextureRequirements**](d3dxcheckvolumetexturerequirements.md) 來調整呼叫參數。 因此，呼叫 D3DXCreateVolumeTexture 通常會成功，因為對 [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) 的呼叫會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 9 中的材質函數](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
