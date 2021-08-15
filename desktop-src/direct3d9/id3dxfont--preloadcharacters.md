---
description: 將一連串字元載入視訊記憶體，以改善轉譯至裝置的效率。
ms.assetid: bb49842e-99de-406b-bf4b-139d6499f96e
title: 'ID3DXFont：:P reloadCharacters 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadCharacters
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2cad2a324a6a5d56ff88dd343cf091b8c4ff2b99cd829344ae91f364458ec51a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295314"
---
# <a name="id3dxfontpreloadcharacters-method"></a>ID3DXFont：:P reloadCharacters 方法

將一連串字元載入視訊記憶體，以改善轉譯至裝置的效率。

## <a name="syntax"></a>語法


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*First* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要載入視訊記憶體之第一個字元的識別碼。

</dd> <dt>

*Last* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要載入視訊記憶體之最後一個字元的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="remarks"></a>備註

這個方法會產生包含代表輸入字元之字元的材質。 圖像會繪製成一系列的三角形。

字元將不會轉譯至裝置;您仍然必須呼叫 [**DrawText**](id3dxfont--drawtext.md) 來呈現字元。 不過，藉由將字元預先載入視訊記憶體， **DrawText** 將使用明顯較少的 CPU 資源。

這個方法會在內部使用 GDI 函數 [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa)將字元轉換成字元。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
