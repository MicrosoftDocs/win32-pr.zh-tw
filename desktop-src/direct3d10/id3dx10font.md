---
description: ID3DX10Font 介面會封裝在特定裝置上呈現特定字型所需的材質和資源。
ms.assetid: 81f4ffe3-f50d-47ce-ae85-15a2a19cacbd
title: 'ID3DX10Font 介面 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1b40230aa983154f9bfc85b3ffb0f08f713b00213259d18bb9b160374b670795
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540344"
---
# <a name="id3dx10font-interface"></a>ID3DX10Font 介面

ID3DX10Font 介面會封裝在特定裝置上呈現特定字型所需的材質和資源。

## <a name="members"></a>成員

**ID3DX10Font** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DX10Font** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX10Font** 介面具有這些方法。



| 方法                                                     | 描述                                                                                                                                           |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrawText**](id3dx10font-drawtext.md)                   | 繪製格式化的文字。 這個方法支援 ANSI 和 Unicode 字串。<br/>                                                                        |
| [**GetDC**](id3dx10font-getdc.md)                         | 傳回已將字型設定在其上的顯示裝置內容 (DC) 的控制碼。<br/>                                                            |
| [**GetDesc**](id3dx10font-getdesc.md)                     | 取得目前字型物件的描述。<br/>                                                                                              |
| [**GetDevice**](id3dx10font-getdevice.md)                 | 取出與字型物件相關聯的 Direct3D 裝置。<br/>                                                                              |
| [**GetGlyphData**](id3dx10font-getglyphdata.md)           | 傳回字元資料格中圖像位置和方向的相關資訊。<br/>                                                     |
| [**GetTextMetrics**](id3dx10font-gettextmetrics.md)       | 取得字型特性。<br/>                                                                                                             |
| [**PreloadCharacters**](id3dx10font-preloadcharacters.md) | 將一連串字元載入視訊記憶體，以改善轉譯至裝置的效率。<br/>                                        |
| [**PreloadGlyphs**](id3dx10font-preloadglyphs.md)         | 將一連串的字元載入視訊記憶體，以改善轉譯至裝置的效率。<br/>                                            |
| [**PreloadText**](id3dx10font-preloadtext.md)             | 將格式化的文字載入視訊記憶體，以改善轉譯至裝置的效率。 這個方法支援 ANSI 和 Unicode 字串。<br/> |



 

## <a name="remarks"></a>備註

ID3DX10Font 介面的取得方式是呼叫 [**D3DX10CreateFont**](d3dx10createfont.md) 或 [**D3DX10CreateFontIndirect**](d3dx10createfontindirect.md)。

LPD3DX10FONT 型別定義為 ID3DX10Font 介面的指標。


```
typedef interface ID3DX10Font ID3DX10Font;
typedef interface ID3DX10Font *LPD3DX10FONT;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
