---
description: 傳回字元資料格中圖像位置和方向的相關資訊。
ms.assetid: 80a78e68-6f88-4cd2-bb7b-0c608ae700aa
title: 'ID3DXFont：： GetGlyphData 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetGlyphData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31f8d2e9d61cd7a8d6bd96fbdd3f6f6a7d895568
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974856"
---
# <a name="id3dxfontgetglyphdata-method"></a>ID3DXFont：： GetGlyphData 方法

傳回字元資料格中圖像位置和方向的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetGlyphData(
  [in]  UINT               Glyph,
  [out] LPDIRECT3DTEXTURE9 *ppTexture,
  [out] RECT               *pBlackBox,
  [out] POINT              *pCellInc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

圖像 \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

字元識別碼。

</dd> <dt>

*ppTexture* \[擴展\]
</dt> <dd>

類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

包含圖像之 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) 物件的指標位址。

</dd> <dt>

*pBlackBox* \[擴展\]
</dt> <dd>

類型： **[ **RECT**](/previous-versions//dd162897(v=vs.85))\***

完全括住圖像之最小矩形物件的指標。

</dd> <dt>

*pCellInc* \[擴展\]
</dt> <dd>

類型： **[ **POINT**](../winprog/windows-data-types.md)\***

二維向量的指標，可將目前字元資料格的原點連接至下一個字元資料格的來源。 請參閱 [**點**](../winprog/windows-data-types.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
