---
description: 針對裝置和字型間接建立字型物件。
ms.assetid: 480f3012-8495-47ca-a649-11ce53cee06c
title: 'D3DXCreateFontIndirect 函式 (D3dx9core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFontIndirect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 086f9cb4cff7666fc3977551e2c9fd4a61150d46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323160"
---
# <a name="d3dxcreatefontindirect-function"></a>D3DXCreateFontIndirect 函式

針對裝置和字型間接建立字型物件。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateFontIndirect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_  const D3DXFONT_DESC     *pDesc,
  _Out_       LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，與字型物件相關聯的裝置。

</dd> <dt>

*pDesc* \[在\]
</dt> <dd>

Type： **Const [**D3DXFONT \_ DESC**](d3dxfont-desc.md) \***

[**D3DXFONT \_ DESC**](d3dxfont-desc.md)結構的指標，描述要建立之字型物件的屬性。 如果編譯器設定需要 Unicode，則資料類型 D3DXFONT \_ DESC 會解析為 D3DXFONT \_ DESCW; 否則，資料類型會解析為 D3DXFONT \_ DESCA。 請參閱＜備註＞。

</dd> <dt>

*ppFont* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXFONT**](id3dxfont.md)\***

傳回 [**ID3DXFont**](id3dxfont.md) 介面的指標，表示所建立的字型物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

編譯器設定也會決定函式版本。 如果已定義 Unicode，函式呼叫會解析為 D3DXCreateFontIndirectW。 否則，函式呼叫會解析為 D3DXCreateFontIndirectA，因為正在使用 ANSI 字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般用途函數](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
