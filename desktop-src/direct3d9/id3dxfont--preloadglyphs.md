---
description: 將一連串的字元載入視訊記憶體，以改善轉譯至裝置的效率。
ms.assetid: df023359-bcb3-4c05-950b-19cdeba97c85
title: 'ID3DXFont：:P reloadGlyphs 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadGlyphs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 954d9e8abb310f962f7188720cb32035baf50d3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035428"
---
# <a name="id3dxfontpreloadglyphs-method"></a>ID3DXFont：:P reloadGlyphs 方法

將一連串的字元載入視訊記憶體，以改善轉譯至裝置的效率。

## <a name="syntax"></a>語法


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*First* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要載入視訊記憶體的第一個圖像的識別碼。

</dd> <dt>

*Last* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要載入視訊記憶體之最後一個圖像的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="remarks"></a>備註

這個方法會產生包含輸入字型的材質。 圖像會繪製成一系列的三角形。

字元不會轉譯至裝置;您仍然必須呼叫 [**DrawText**](id3dxfont--drawtext.md) 來呈現字元。 不過，藉由將字元預先載入視訊記憶體， **DrawText** 將使用明顯較少的 CPU 資源。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
