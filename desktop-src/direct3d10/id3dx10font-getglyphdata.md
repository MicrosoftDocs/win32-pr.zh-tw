---
description: 傳回字元資料格中圖像位置和方向的相關資訊。
ms.assetid: 1114b06a-c0f0-4c2a-86ad-2ed72bee4049
title: 'ID3DX10Font：： GetGlyphData 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetGlyphData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eaabcd6de2acf5ec86ab8c9a47d4224ed230104fe189816abd9d02fd3ac09596
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302888"
---
# <a name="id3dx10fontgetglyphdata-method"></a>ID3DX10Font：： GetGlyphData 方法

傳回字元資料格中圖像位置和方向的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetGlyphData(
  [in]  UINT                     Glyph,
  [out] ID3D10ShaderResourceView **ppTexture,
  [in]  RECT                     *pBlackBox,
  [in]  POINT                    *pCellInc
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

類型： **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***

包含圖像之 ID3D10Texture 物件的指標位址。

</dd> <dt>

*pBlackBox* \[在\]
</dt> <dd>

類型： **[ **RECT**](/previous-versions//dd162897(v=vs.85))\***

完全括住圖像之最小矩形物件的指標。 請參閱 [RECT](/previous-versions//ms536136(v=vs.85))。

</dd> <dt>

*pCellInc* \[在\]
</dt> <dd>

類型： **POINT \***

二維向量的指標，可將目前字元資料格的原點連接至下一個字元資料格的來源。 請參閱 [點](/previous-versions//ms536119(v=vs.85))。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
