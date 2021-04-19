---
description: 篩選材質的 mipmap 層級。
ms.assetid: bfeae9b0-9480-4a26-a225-4a34780546ce
title: 'D3DXFilterTexture 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFilterTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e8a0d1c211b50379451c8b04830e9c97fe988137
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997394"
---
# <a name="d3dxfiltertexture-function"></a>D3DXFilterTexture 函式

篩選材質的 mipmap 層級。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXFilterTexture(
  _In_        LPDIRECT3DBASETEXTURE9 pBaseTexture,
  _Out_ const PALETTEENTRY           *pPalette,
  _In_        UINT                   SrcLevel,
  _In_        DWORD                  MipFilter
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pBaseTexture* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

[**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)介面的指標，代表要篩選的材質物件。

</dd> <dt>

*pPalette* \[擴展\]
</dt> <dd>

Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，代表要填入的256色調色板，或 nonpalettized 格式的 **Null** 。 如果未指定調色板，則會提供預設的 Direct3D 調色板 (所有不透明的白色調色板) 。 請參閱＜備註＞。

</dd> <dt>

*SrcLevel* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

映射用來產生後續層級的層級。 指定 \_ 此參數的 D3DX 預設值，相當於指定0。

</dd> <dt>

*MipFilter* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

一或多個 [D3DX \_ 篩選準則](d3dx-filter.md) 的組合，可控制 mipmap 的篩選方式。 \_如果紋理大小是2的乘冪，則指定這個參數的 D3DX 預設值就相當於指定 D3DX \_ 篩選方塊 \_ ， \_ 否則 D3DX 篩選方塊 \_ \| D3DX \_ 篩選 \_ 遞色。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="remarks"></a>備註

篩選會以遞迴方式套用到每個材質層級，以產生下一個材質層級。

寫入至非層級零的材質介面，不會讓中途的矩形更新。 如果呼叫 **D3DXFilterTexture** ，但介面尚未變更 (這在正常使用方式下不太可能) ，應用程式必須在紋理上明確呼叫 [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) 。

在預設集區中建立的材質 (D3DPOOL \_ 預設) 不能搭配 **D3DXFilterTexture** (使用， \_) 除非物件需要鎖定作業。 請注意，預設集區中的材質不允許鎖定 (除非它們是動態) 。

如需 [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)的詳細資訊，請參閱 Platform SDK。 請注意，從 DirectX 8.0 起， **PALETTEENTRY** 結構的 peFlags 成員無法如 Platform SDK 中所述運作。 PeFlags 成員現在是8位調色盤格式的 Alpha 通道。

只有一個材質篩選函式，但是有兩個宏呼叫這個方法。


```
#define D3DXFilterCubeTexture D3DXFilterTexture
#define D3DXFilterVolumeTexture D3DXFilterTexture
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 9 中的材質函數](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
