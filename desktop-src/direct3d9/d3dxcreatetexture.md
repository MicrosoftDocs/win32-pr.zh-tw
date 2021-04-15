---
description: 建立空白紋理，視需要調整呼叫參數。
ms.assetid: ea028aa9-4f37-4625-9e07-9072ec1a61d0
title: 'D3DXCreateTexture 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ecbd5cbb94355af9c1e51e6c7e8fc31a862b03be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514604"
---
# <a name="d3dxcreatetexture-function"></a>D3DXCreateTexture 函式

建立空白紋理，視需要調整呼叫參數。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateTexture(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  UINT               Width,
  _In_  UINT               Height,
  _In_  UINT               MipLevels,
  _In_  DWORD              Usage,
  _In_  D3DFORMAT          Format,
  _In_  D3DPOOL            Pool,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與材質相關聯的裝置。

</dd> <dt>

*寬度* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

寬度（以圖元為單位）。 如果這個值為0，則會使用值1。 請參閱＜備註＞。

</dd> <dt>

*高度* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

高度（以圖元為單位）。 如果這個值為0，則會使用值1。 請參閱＜備註＞。

</dd> <dt>

*MipLevels* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要求的 mip 層級數目。 如果此值為零或 D3DX \_ 預設值，則會建立完整的 mipmap 鏈。

</dd> <dt>

*使用* \[ 方式在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

0、 [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)或 **D3DUSAGE \_ DYNAMIC**。 將此旗標設定為 **D3DUSAGE \_ RENDERTARGET** ，表示介面會藉由呼叫 [**SetRenderTarget**](/windows/desktop/api) 方法當做轉譯目標使用。 如果指定了 **D3DUSAGE \_ RENDERTARGET** 或 **D3DUSAGE \_ DYNAMIC** ，應用程式應該呼叫 [**CheckDeviceFormat**](/windows/desktop/api)來檢查裝置是否支援這項作業。 如需使用動態紋理的詳細資訊，請參閱 [使用動態紋理](performance-optimizations.md)。

</dd> <dt>

*格式* \[在\]
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)**

[D3DFORMAT](d3dformat.md)列舉型別的成員，描述紋理所要求的像素格式。 如果裝置不支援要求的格式，則傳回的材質可能會與指定的格式不同。 應用程式應該檢查傳回材質的格式，以查看它是否符合要求的格式。

</dd> <dt>

*集* \[ 區在\]
</dt> <dd>

類型： **[ **D3DPOOL**](./d3dpool.md)**

[**D3DPOOL**](./d3dpool.md)列舉型別的成員，描述應放置紋理的記憶體類別。

</dd> <dt>

*ppTexture* \[擴展\]
</dt> <dd>

類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)介面指標的位址，表示所建立的材質物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

就內部而言，D3DXCreateTexture 會使用 [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) 來調整呼叫參數。 因此，呼叫 D3DXCreateTexture 通常會成功，因為對 [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) 的呼叫會失敗。

如果高度和寬度都設定為 [D3DX \_ 預設](other-d3dx-constants.md)值，則兩個參數都使用256的值。 如果 [高度] 或 [寬度] 設定為 \_ [D3DX 預設值]，而另一個參數設定為數值，則紋理會是正方形，且高度和寬度都等於數位值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 9 中的材質函數](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
