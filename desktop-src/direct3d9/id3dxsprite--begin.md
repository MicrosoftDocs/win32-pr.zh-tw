---
description: 準備裝置以繪製 sprite。
ms.assetid: ec9eb069-0a41-4dd5-bbd5-5a31133550b6
title: 'ID3DXSprite：： Begin 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7670c3c516627283a466b3adbb369dc76bbe0d45
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992328"
---
# <a name="id3dxspritebegin-method"></a>ID3DXSprite：： Begin 方法

準備裝置以繪製 sprite。

## <a name="syntax"></a>語法


```C++
HRESULT Begin(
  [in] DWORD Flags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

描述 sprite 轉譯選項的零或多個旗標組合。 針對此方法，有效的旗標為：

-   D3DXSPRITE \_ ALPHABLEND
-   D3DXSPRITE \_ \_ 佈告欄
-   D3DXSPRITE \_ DONOTMODIFY \_ RENDERSTATE
-   D3DXSPRITE \_ DONOTSAVESTATE
-   D3DXSPRITE \_ OBJECTSPACE
-   D3DXSPRITE \_ \_ 排序 \_ 深度 \_ BACKTOFRONT
-   D3DXSPRITE \_ \_ 排序 \_ 深度 \_ FRONTTOBACK
-   D3DXSPRITE \_ \_ 排序 \_ 材質

如需旗標的描述，以及如何控制裝置狀態捕捉和裝置視圖轉換的詳細資訊，請參閱 [D3DXSPRITE](d3dxsprite.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DERR \_ OUTOFVIDEOMEMORY、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

您必須從 [**IDirect3DDevice9：： BeginScene**](/windows/desktop/api) 內部呼叫這個方法。 . . [**IDirect3DDevice9：： EndScene**](/windows/desktop/api) sequence。 **ID3DXSprite：： Begin** 不能用來取代 **IDirect3DDevice9：： BeginScene** 或 [**ID3DXRenderToSurface：： BeginScene**](id3dxrendertosurface--beginscene.md)。

此方法會在裝置上設定下列狀態。

轉譯狀態：



| 輸入 ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md))  | 值                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| D3DRS \_ ALPHABLENDENABLE                                       | true                                                                                                              |
| D3DRS \_ ALPHAFUNC                                              | D3DCMP \_ 更大                                                                                                   |
| D3DRS \_ ALPHAREF                                               | 0x00                                                                                                              |
| D3DRS \_ ALPHATESTENABLE                                        | AlphaCmpCaps                                                                                                      |
| D3DRS \_ BLENDOP                                                | D3DBLENDOP \_ 新增                                                                                                   |
| D3DRS \_ 剪切                                               | true                                                                                                              |
| D3DRS \_ CLIPPLANEENABLE                                        | FALSE                                                                                                             |
| D3DRS \_ COLORWRITEENABLE                                       | D3DCOLORWRITEENABLE \_ ALPHA \| D3DCOLORWRITEENABLE \_ BLUE \| D3DCOLORWRITEENABLE \_ 綠 \| D3DCOLORWRITEENABLE \_ RED |
| D3DRS \_ CULLMODE                                               | D3DCULL \_ 無                                                                                                     |
| D3DRS \_ DESTBLEND                                              | D3DBLEND \_ INVSRCALPHA                                                                                             |
| D3DRS \_ DIFFUSEMATERIALSOURCE                                  | D3DMCS \_ COLOR1                                                                                                    |
| D3DRS \_ ENABLEADAPTIVETESSELLATION                             | FALSE                                                                                                             |
| D3DRS \_ FILLMODE                                               | D3DFILL \_ 固態                                                                                                    |
| D3DRS \_ FOGENABLE                                              | FALSE                                                                                                             |
| D3DRS \_ INDEXEDVERTEXBLENDENABLE                               | FALSE                                                                                                             |
| D3DRS \_ 光源                                               | FALSE                                                                                                             |
| D3DRS \_ RANGEFOGENABLE                                         | FALSE                                                                                                             |
| D3DRS \_ SEPARATEALPHABLENDENABLE                               | FALSE                                                                                                             |
| D3DRS \_ SHADEMODE                                              | D3DSHADE \_ GOURAUD                                                                                                 |
| D3DRS \_ SPECULARENABLE                                         | FALSE                                                                                                             |
| D3DRS \_ SRCBLEND                                               | D3DBLEND \_ SRCALPHA                                                                                                |
| D3DRS \_ SRGBWRITEENABLE                                        | FALSE                                                                                                             |
| D3DRS \_ STENCILENABLE                                          | FALSE                                                                                                             |
| D3DRS \_ VERTEXBLEND                                            | FALSE                                                                                                             |
| D3DRS \_ WRAP0                                                  | 0                                                                                                                 |



 

材質階段狀態：



| 階段識別碼 | 輸入 ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md))  | 值            |
|------------------|---------------------------------------------------------------------------|------------------|
| 0                | D3DTSS \_ ALPHAARG1                                                         | D3DTA \_ 材質   |
| 0                | D3DTSS \_ ALPHAARG2                                                         | D3DTA \_ 擴散   |
| 0                | D3DTSS \_ ALPHAOP                                                           | D3DTOP \_ lambert |
| 0                | D3DTSS \_ COLORARG1                                                         | D3DTA \_ 材質   |
| 0                | D3DTSS \_ COLORARG2                                                         | D3DTA \_ 擴散   |
| 0                | D3DTSS \_ COLOROP                                                           | D3DTOP \_ lambert |
| 0                | D3DTSS \_ TEXCOORDINDEX                                                     | 0                |
| 0                | D3DTSS \_ TEXTURETRANSFORMFLAGS                                             | D3DTTFF \_ DISABLE |
| 1                | D3DTSS \_ ALPHAOP                                                           | D3DTOP \_ DISABLE  |
| 1                | D3DTSS \_ COLOROP                                                           | D3DTOP \_ DISABLE  |



 

取樣器狀態：



| 取樣器階段索引 | 輸入 ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md))  | 值                                                                                                          |
|---------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 0                   | D3DSAMP \_ ADDRESSU                                               | D3DTADDRESS \_ 夾具                                                                                             |
| 0                   | D3DSAMP \_ ADDRESSV                                               | D3DTADDRESS \_ 夾具                                                                                             |
| 0                   | D3DSAMP \_ MAGFILTER                                              | \_如果 TextureFilterCaps 包含 D3DPTFILTERCAPS MAGFANISOTROPIC，則為 D3DTEXF \_ ，否則為 D3DTEXF \_ 線性 |
| 0                   | D3DSAMP \_ MAXMIPLEVEL                                            | 0                                                                                                              |
| 0                   | D3DSAMP \_ MAXANISOTROPY                                          | MaxAnisotropy                                                                                                  |
| 0                   | D3DSAMP \_ MINFILTER                                              | \_如果 TextureFilterCaps 包含 D3DPTFILTERCAPS MINFANISOTROPIC，則為 D3DTEXF \_ ，否則為 D3DTEXF \_ 線性 |
| 0                   | D3DSAMP \_ MIPFILTER                                              | \_如果 TextureFilterCaps 包含 D3DPTFILTERCAPS \_ MIPFLINEAR，則為線性 D3DTEXF，否則為 D3DTEXF \_ 點            |
| 0                   | D3DSAMP \_ MIPMAPLODBIAS                                          | 0                                                                                                              |
| 0                   | D3DSAMP \_ SRGBTEXTURE                                            | 0                                                                                                              |



 

> [!Note]  
> 這個方法會停用 N 個修補程式。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[D3DXSPRITE](d3dxsprite.md)
</dt> </dl>

 

 
