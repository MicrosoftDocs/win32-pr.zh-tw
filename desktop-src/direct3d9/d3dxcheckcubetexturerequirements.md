---
description: 檢查 cube 材質建立參數。
ms.assetid: 56ced947-1142-4d05-95e3-ca6a26b147d4
title: 'D3DXCheckCubeTextureRequirements 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckCubeTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f800617920c5d79361b5e6da291fd88b5b963b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696844"
---
# <a name="d3dxcheckcubetexturerequirements-function"></a>D3DXCheckCubeTextureRequirements 函式

檢查 cube 材質建立參數。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCheckCubeTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pSize,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與 cube 材質相關聯的裝置。

</dd> <dt>

*pSize* \[in、out\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

要求的寬度和高度（以圖元為單位）的指標，或為 **Null**。 傳回已更正的大小。

</dd> <dt>

*pNumMipLevels* \[in、out\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

要求的 mipmap 層級數目的指標，或 **為 Null**。 傳回已更正的 mipmap 層級數目。

</dd> <dt>

*使用* \[ 方式在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

0或 D3DUSAGE \_ RENDERTARGET。 將此旗標設定為 D3DUSAGE \_ RENDERTARGET 表示介面要當做轉譯目標使用。 然後，您可以將資源傳遞給 [**SetRenderTarget**](/windows/desktop/api) 方法的 pNewRenderTarget 參數。 如果指定了 D3DUSAGE \_ RENDERTARGET，應用程式應該藉由呼叫 [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)來檢查裝置是否支援這項操作。

</dd> <dt>

*pformatetc 架構* \[in、out\]
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)\***

[D3DFORMAT](d3dformat.md)列舉型別的成員指標。 指定所需的像素格式，或 **為 Null**。 傳回更正的格式。

</dd> <dt>

*集* \[ 區在\]
</dt> <dd>

類型： **[ **D3DPOOL**](./d3dpool.md)**

[**D3DPOOL**](./d3dpool.md)列舉型別的成員，描述應放置紋理的記憶體類別。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ NOTAVAILABLE，D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

如果此函式的參數無效，此函式會傳回已更正的參數。

Cube 紋理不同于其他表面，因為它們是表面的集合。 若要使用 cube 材質來呼叫 [**SetRenderTarget**](/windows/desktop/api) ，您必須使用 [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) 選取個別臉部，並將產生的介面傳遞至 **SetRenderTarget**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 9 中的材質函數](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
