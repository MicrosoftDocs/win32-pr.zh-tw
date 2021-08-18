---
description: 繪製格式化的文字。 這個方法支援 ANSI 和 Unicode 字串。
ms.assetid: c1c3657e-632e-46a5-91da-e102ac8ef9bb
title: 'ID3DXFont：:D rawText 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.DrawText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d2a0b2dc61e2dd2a41f5a2fe864973fca91a5e471c75d6afc353c147f7a00fcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987418"
---
# <a name="id3dxfontdrawtext-method"></a>ID3DXFont：:D rawText 方法

繪製格式化的文字。 這個方法支援 ANSI 和 Unicode 字串。

## <a name="syntax"></a>語法


```C++
INT DrawText(
  [in] LPD3DXSPRITE pSprite,
  [in] LPCTSTR      pString,
  [in] INT          Count,
  [in] LPRECT       pRect,
  [in] DWORD        Format,
  [in] D3DCOLOR     Color
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSprite* \[在\]
</dt> <dd>

類型： **[ **LPD3DXSPRITE**](id3dxsprite.md)**

包含字串之 [**ID3DXSprite**](id3dxsprite.md) 物件的指標。 可以是 **Null**，在此情況下，Direct3D 會以它自己的 sprite 物件轉譯字串。 為了提高效率，如果在資料列中呼叫 **DrawText** 一次以上，則應該指定 sprite 物件。

</dd> <dt>

*pString* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**

要繪製之字串的指標。 如果 Count 參數為-1，則字串必須以 null 結束。

</dd> <dt>

*計數* \[在\]
</dt> <dd>

類型： **[ **INT**](../winprog/windows-data-types.md)**

指定字串中的字元數。 如果 Count 為-1，則會假設 pString 參數是以 null 終止之字串的指標，而 **DrawText** 會自動計算字元計數。

</dd> <dt>

*pRect* \[在\]
</dt> <dd>

類型： **[ **LPRECT**](../winprog/windows-data-types.md)**

[**矩形結構的**](/previous-versions//dd162897(v=vs.85))指標，其中包含要格式化文字的矩形（以邏輯座標表示）。 矩形右邊的座標值必須大於其左邊的座標值。 同樣地，底部的座標值必須大於頂端的座標值。

</dd> <dt>

*格式* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

指定格式化文字的方法。 它可以是下列值的任意組合：



| 值                                                                                                                                                         | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span><dl> <dt>**DT \_ 底部**</dt> </dl>             | 將文字對齊矩形的底部。 此值必須與 DT 單行合併 \_ 。<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span><dl> <dt>**DT \_ CALCRECT**</dt> </dl>       | 決定矩形的寬度和高度。 如果有多行文字， **DrawText** 會使用 pRect 參數所指向之矩形的寬度，並將矩形的基底延伸至系結最後一行文字。 如果只有一行文字， **DrawText** 會修改矩形的右邊，使其系結該行中的最後一個字元。 無論是哪一種情況， **DrawText** 都會傳回格式化文字的高度，但不會繪製文字。<br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span><dl> <dt>**DT \_ CENTER**</dt> </dl>             | 在矩形中將文字水準置中。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span><dl> <dt>**DT \_ EXPANDTABS**</dt> </dl> | 展開定位字元。 每個定位預設有八個字元。<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span><dl> <dt>**\_向左 DT**</dt> </dl>                   | 將文字靠左對齊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span><dl> <dt>**DT \_ NOCLIP**</dt> </dl>             | 繪製而不裁剪。 使用 DT NOCLIP 時， **DrawText** 會稍微快一點 \_ 。<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="DT_RIGHT"></span><span id="dt_right"></span><dl> <dt>**DT \_ 右邊**</dt> </dl>                | 將文字對齊右邊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span><dl> <dt>**DT \_ RTLREADING**</dt> </dl> | 當選取希伯來文或阿拉伯文字型時，以由右至左的雙向文字讀取順序顯示文字。 所有文字的預設讀取順序都是由左至右。<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span><dl> <dt>**DT \_ 單行**</dt> </dl> | 只在單一行上顯示文字。 換行字元和換行字元不會中斷。<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span><dl> <dt>**DT \_ TOP**</dt> </dl>                      | 靠上對齊文字。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span><dl> <dt>**DT \_ VCENTER**</dt> </dl>          | 將文字水準置中 (單行) 。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span><dl> <dt>**DT \_ WORDBREAK**</dt> </dl>    | 中斷單字。 如果單字會延伸超出 pRect 參數所指定的矩形邊緣，單字之間的行會自動中斷。 換行字元序列也會中斷這一行。<br/>                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*色彩* \[在\]
</dt> <dd>

類型： **[ **D3DCOLOR**](d3dcolor.md)**

文字的色彩。 如需詳細資訊，請參閱 [**D3DCOLOR**](d3dcolor.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **INT**](../winprog/windows-data-types.md)**

如果函式成功，則傳回值為邏輯單元中文字的高度。 如果 \_ 指定了 DT VCENTER 或 dt \_ 底端，則傳回值是從 pRect (top 到所繪製文字底部) 的位移。 如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

這個方法的參數非常類似于 GDI [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext) 函式的參數。

這個方法支援 ANSI 和 Unicode 字串。

必須在 [**BeginScene**](/windows/desktop/api) 內呼叫這個方法 .。。 [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) 組塊。 唯一的例外狀況是當應用程式使用 DT \_ CALCRECT 來呼叫 DrawText，以計算指定文字區塊的大小時。

除非使用 DT \_ NOCLIP 格式，否則這個方法會將文字剪下，使其不會出現在指定的矩形之外。 除非指定了 DT 單行格式，否則所有格式都會假設有多行 \_ 。

如果選取的字型對矩形而言太大，則這個方法不會嘗試以較小的字型取代。

這個方法只支援行距和方向都為零的字型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
