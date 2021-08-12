---
description: 繪製格式化的文字。 這個方法支援 ANSI 和 Unicode 字串。
ms.assetid: 205e9e23-4293-4195-9e41-d8c06dabd285
title: 'ID3DX10Font：:D rawText 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.DrawText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1eabe3a88fb3d38021eee8f186baed1d8403d18026d4d1704d520ad3c8b8f72c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303168"
---
# <a name="id3dx10fontdrawtext-method"></a>ID3DX10Font：:D rawText 方法

繪製格式化的文字。 這個方法支援 ANSI 和 Unicode 字串。

## <a name="syntax"></a>語法


```C++
INT DrawText(
  [in] LPD3DX10SPRITE pSprite,
  [in] LPCTSTR        pString,
  [in] INT            Count,
  [in] LPRECT         pRect,
  [in] UINT           Format,
  [in] D3DXCOLOR      Color
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSprite* \[在\]
</dt> <dd>

類型： **[ **LPD3DX10SPRITE**](id3dx10sprite.md)**

ID3DX10Sprite 物件的指標，其中包含您想要繪製的字串。 可以是 **Null**，在此情況下，Direct3D 會以它自己的 sprite 物件轉譯字串。 為了提高效率，如果在資料列中多次呼叫 ID3DX10Font：:D rawText，就應該指定 sprite 物件。

</dd> <dt>

*pString* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**

要繪製之字串的指標。 如果已定義 UNICODE，此參數型別會解析為 LPCWSTR，否則，此型別會解析為 LPCSTR。 如果 Count 參數為-1，則字串必須是以 **Null** 結束。

</dd> <dt>

*計數* \[在\]
</dt> <dd>

類型： **[ **INT**](../winprog/windows-data-types.md)**

字串中的字元數。 如果 Count 為-1，則會假設 pString 參數是包含以 Null 終止之字串和 ID3DX10Font 的 sprite 的指標：:D rawText 會自動計算字元計數。

</dd> <dt>

*pRect* \[在\]
</dt> <dd>

類型： **LPRECT**

[矩形結構的](/previous-versions//ms536136(v=vs.85))指標，其中包含要格式化文字的矩形（以邏輯座標表示）。 如同任何 RECT 物件，矩形右邊的座標值必須大於其左邊的座標值。 同樣地，底部的座標值必須大於頂端的座標值。

</dd> <dt>

*格式* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

指定格式化文字的方法。 它可以是下列值的任意組合：



| Item                                                                                      | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span>DT \_ 底部<br/>             | 將文字對齊矩形底部。 此值必須與 DT 單行合併 \_ 。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>DT \_ CALCRECT<br/>       | 告訴 DrawText 根據您告訴它繪製的字串長度，自動計算矩形的寬度和高度。 如果有多行文字，ID3DX10Font：:D rawText 會使用 pRect 參數所指向之矩形的寬度，並擴充矩形的基底以系結最後一行文字。 如果只有一行文字，ID3DX10Font：:D rawText 會修改矩形的右邊，使其限定該行中的最後一個字元。 在任一種情況下，ID3DX10Font：:D rawText 都會傳回格式化文字的高度，但不會繪製文字。<br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span>DT \_ CENTER<br/>             | 在矩形中水準置中文字。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>DT \_ EXPANDTABS<br/> | 展開 [tab 字元]。 每個定位預設有八個字元。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span>\_向左 DT<br/>                   | 將文字靠左對齊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span>DT \_ NOCLIP<br/>             | 繪製而不剪下。 ID3DX10Font：使用 DT NOCLIP 時，:D rawText 會稍微快一點 \_ 。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RIGHT"></span><span id="dt_right"></span>DT \_ 右邊<br/>                | 將文字靠右對齊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>DT \_ RTLREADING<br/> | 當選取希伯來文或阿拉伯文字型時，以由右至左的讀取順序來顯示雙向文字的文字。 所有文字的預設讀取順序都是由左至右。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>DT \_ 單行<br/> | 只在單一行上顯示文字。 換行字元和換行字元不會中斷。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span>DT \_ TOP<br/>                      | 頂端對齊文字。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span>DT \_ VCENTER<br/>          | 將文字置中垂直 (只) 一行。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>DT \_ WORDBREAK<br/>    | 中斷單字。 如果單字會延伸超出 pRect 參數所指定的矩形邊緣，單字之間的行會自動中斷。 換行字元序列也會中斷這一行。<br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*色彩* \[在\]
</dt> <dd>

類型： **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

文字的色彩。 請參閱 [**D3DXCOLOR**](d3d10-d3dxcolor.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **INT**](../winprog/windows-data-types.md)**

如果函式成功，則傳回值為邏輯單元中文字的高度。 如果 \_ 指定了 DT VCENTER 或 dt \_ 底端，則傳回值是從 pRect (top 到所繪製文字底部) 的位移。 如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

這個方法的參數非常類似于 [GDI DrawText](/previous-versions//ms533909(v=vs.85)) 函式的參數。

這個方法支援 ANSI 和 Unicode 字串。

除非使用 DT \_ NOCLIP 格式，否則這個方法會將文字剪下，使其不會出現在指定的矩形之外。 除非指定了 DT 單行格式，否則所有格式都會假設有多行 \_ 。

如果選取的字型對矩形而言太大，則這個方法不會嘗試以較小的字型取代。

這個方法只支援行距和方向都為零的字型。

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

 

 
