---
description: 建立字型物件。請注意，我們建議您不要使用這個函式，而是使用 DirectWrite 和 DirectXTK library SpriteFont 類別。
ms.assetid: 057ee033-37d8-4fc1-9f35-776393fff008
title: 'D3DX10CreateFontIndirect 函式 (D3DX10Core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFontIndirect
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ae69b02483a94a80a06ef52ee4857eb081cfcfb2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322771"
---
# <a name="d3dx10createfontindirect-function"></a>D3DX10CreateFontIndirect 函式

建立字型物件。

> [!Note]  
> 我們建議您不要使用這個函式，而是使用 [DirectWrite](../directwrite/direct-write-portal.md) 和 [DirectXTK](https://github.com/Microsoft/DirectXTK) 程式庫 **SpriteFont** 類別。

 

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10CreateFontIndirect(
  _In_        ID3D10Device     *pDevice,
  _In_  const D3DX10_FONT_DESC *pDesc,
  _Out_       LPD3DX10FONT     *ppFont
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

[**ID3D10Device 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)介面的指標。

</dd> <dt>

*pDesc* \[在\]
</dt> <dd>

類型： **Const [**D3DX10 \_ 字型 \_ DESC**](d3dx10-font-desc.md) \***

[**D3DX10 \_ 字型 \_ DESC**](d3dx10-font-desc.md)結構的指標，描述要建立之字型物件的屬性。 如果已定義 Unicode，函式呼叫會解析為 D3DXCreateFontIndirectW。 否則，函式呼叫會解析為 D3DXCreateFontIndirectA，因為正在使用 ANSI 字串。

</dd> <dt>

*ppFont* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DX10FONT**](id3dx10font.md)\***

傳回 [**ID3DX10Font 介面**](id3dx10font.md)的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般用途函數](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
