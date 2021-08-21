---
description: ID3DXFont 介面會封裝在特定裝置上呈現特定字型所需的材質和資源。
ms.assetid: ac40b600-3b9f-4e6e-8563-18597b3dd602
title: 'ID3DXFont 介面 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f05322ef2d7898f0025154989e9ac09ab8355025d8ad1ed94034fb25da66592f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493649"
---
# <a name="id3dxfont-interface"></a>ID3DXFont 介面

ID3DXFont 介面會封裝在特定裝置上呈現特定字型所需的材質和資源。

## <a name="members"></a>成員

**ID3DXFont** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXFont** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXFont** 介面具有這些方法。



| 方法                                                    | 描述                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrawText**](id3dxfont--drawtext.md)                   | 繪製格式化的文字。 這個方法支援 ANSI 和 Unicode 字串。<br/>                                                                                                                                                               |
| [**GetDC**](id3dxfont--getdc.md)                         | 傳回已設定字型 (DC) 的顯示裝置內容控制碼。<br/>                                                                                                                                                           |
| [**GetDesc**](id3dxfont--getdesc.md)                     | 取得目前字型物件的描述。 GetDescW 和 GetDescA 與這個方法相同，不同之處在于指標會分別傳回至 [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) 或 **D3DXFONT \_ DESCA** 結構。<br/> |
| [**GetDevice**](id3dxfont--getdevice.md)                 | 抓取與字型物件相關聯的 Direct3D 裝置。<br/>                                                                                                                                                                     |
| [**GetGlyphData**](id3dxfont--getglyphdata.md)           | 傳回字元資料格中圖像位置和方向的相關資訊。<br/>                                                                                                                                            |
| [**GetTextMetrics**](id3dxfont--gettextmetrics.md)       | 捕獲 [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) 結構中所識別的字型特性。 這個方法支援 ANSI 和 Unicode 編譯器設定。<br/>                                                                       |
| [**OnLostDevice**](id3dxfont--onlostdevice.md)           | 您可以使用此方法來釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。 只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。<br/>                                              |
| [**OnResetDevice**](id3dxfont--onresetdevice.md)         | 您可以使用這個方法來重新取得資源，並儲存初始狀態。<br/>                                                                                                                                                                    |
| [**PreloadCharacters**](id3dxfont--preloadcharacters.md) | 將一連串字元載入視訊記憶體，以改善轉譯至裝置的效率。<br/>                                                                                                                               |
| [**PreloadGlyphs**](id3dxfont--preloadglyphs.md)         | 將一連串的字元載入視訊記憶體，以改善轉譯至裝置的效率。<br/>                                                                                                                                   |
| [**PreloadText**](id3dxfont--preloadtext.md)             | 將格式化的文字載入視訊記憶體，以改善轉譯至裝置的效率。 這個方法支援 ANSI 和 Unicode 字串。<br/>                                                                                        |



 

## <a name="remarks"></a>備註

**ID3DXFont** 介面的取得方式是呼叫 [**D3DXCreateFont**](d3dxcreatefont.md)或 [**D3DXCreateFontIndirect**](d3dxcreatefontindirect.md)。

LPD3DXFONT 型別定義為 **ID3DXFont** 介面的指標。


```
typedef interface ID3DXFont ID3DXFont;
typedef interface ID3DXFont *LPD3DXFONT;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
