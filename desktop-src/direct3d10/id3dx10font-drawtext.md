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
ms.openlocfilehash: 5fa23684be1b63cfbd8e3d07d3578d87fdfbf46a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991467"
---
# <a name="id3dx10fontdrawtext-method"></a><span data-ttu-id="51b77-104">ID3DX10Font：:D rawText 方法</span><span class="sxs-lookup"><span data-stu-id="51b77-104">ID3DX10Font::DrawText method</span></span>

<span data-ttu-id="51b77-105">繪製格式化的文字。</span><span class="sxs-lookup"><span data-stu-id="51b77-105">Draw formatted text.</span></span> <span data-ttu-id="51b77-106">這個方法支援 ANSI 和 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="51b77-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="51b77-107">語法</span><span class="sxs-lookup"><span data-stu-id="51b77-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="51b77-108">參數</span><span class="sxs-lookup"><span data-stu-id="51b77-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51b77-109">*pSprite* \[在\]</span><span class="sxs-lookup"><span data-stu-id="51b77-109">*pSprite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51b77-110">類型： **[ **LPD3DX10SPRITE**](id3dx10sprite.md)**</span><span class="sxs-lookup"><span data-stu-id="51b77-110">Type: **[**LPD3DX10SPRITE**](id3dx10sprite.md)**</span></span>

<span data-ttu-id="51b77-111">ID3DX10Sprite 物件的指標，其中包含您想要繪製的字串。</span><span class="sxs-lookup"><span data-stu-id="51b77-111">Pointer to an ID3DX10Sprite object that contains the string you wish to draw.</span></span> <span data-ttu-id="51b77-112">可以是 **Null**，在此情況下，Direct3D 會以它自己的 sprite 物件轉譯字串。</span><span class="sxs-lookup"><span data-stu-id="51b77-112">Can be **NULL**, in which case Direct3D will render the string with its own sprite object.</span></span> <span data-ttu-id="51b77-113">為了提高效率，如果在資料列中多次呼叫 ID3DX10Font：:D rawText，就應該指定 sprite 物件。</span><span class="sxs-lookup"><span data-stu-id="51b77-113">To improve efficiency, a sprite object should be specified if ID3DX10Font::DrawText is to be called more than once in a row.</span></span>

</dd> <dt>

<span data-ttu-id="51b77-114">*pString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="51b77-114">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51b77-115">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51b77-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="51b77-116">要繪製之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="51b77-116">Pointer to a string to draw.</span></span> <span data-ttu-id="51b77-117">如果已定義 UNICODE，此參數型別會解析為 LPCWSTR，否則，此型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="51b77-117">If UNICODE is defined, this parameter type resolves to an LPCWSTR, otherwise, the type resolves to an LPCSTR.</span></span> <span data-ttu-id="51b77-118">如果 Count 參數為-1，則字串必須是以 **Null** 結束。</span><span class="sxs-lookup"><span data-stu-id="51b77-118">If the Count parameter is -1, the string must be **NULL** terminated.</span></span>

</dd> <dt>

<span data-ttu-id="51b77-119">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="51b77-119">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51b77-120">類型： **[ **INT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51b77-120">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="51b77-121">字串中的字元數。</span><span class="sxs-lookup"><span data-stu-id="51b77-121">The number of characters in the string.</span></span> <span data-ttu-id="51b77-122">如果 Count 為-1，則會假設 pString 參數是包含以 Null 終止之字串和 ID3DX10Font 的 sprite 的指標：:D rawText 會自動計算字元計數。</span><span class="sxs-lookup"><span data-stu-id="51b77-122">If Count is -1, then the pString parameter is assumed to be a pointer to a sprite containing a NULL-terminated string and ID3DX10Font::DrawText computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="51b77-123">*pRect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="51b77-123">*pRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51b77-124">類型： **LPRECT**</span><span class="sxs-lookup"><span data-stu-id="51b77-124">Type: **LPRECT**</span></span>

<span data-ttu-id="51b77-125">[矩形結構的](/previous-versions//ms536136(v=vs.85))指標，其中包含要格式化文字的矩形（以邏輯座標表示）。</span><span class="sxs-lookup"><span data-stu-id="51b77-125">Pointer to a [RECT](/previous-versions//ms536136(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span> <span data-ttu-id="51b77-126">如同任何 RECT 物件，矩形右邊的座標值必須大於其左邊的座標值。</span><span class="sxs-lookup"><span data-stu-id="51b77-126">As with any RECT object, the coordinate value of the rectangle's right side must be greater than that of its left side.</span></span> <span data-ttu-id="51b77-127">同樣地，底部的座標值必須大於頂端的座標值。</span><span class="sxs-lookup"><span data-stu-id="51b77-127">Likewise, the coordinate value of the bottom must be greater than that of the top.</span></span>

</dd> <dt>

<span data-ttu-id="51b77-128">*格式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="51b77-128">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51b77-129">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51b77-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="51b77-130">指定格式化文字的方法。</span><span class="sxs-lookup"><span data-stu-id="51b77-130">Specify the method of formatting the text.</span></span> <span data-ttu-id="51b77-131">它可以是下列值的任意組合：</span><span class="sxs-lookup"><span data-stu-id="51b77-131">It can be any combination of the following values:</span></span>



| <span data-ttu-id="51b77-132">項目</span><span class="sxs-lookup"><span data-stu-id="51b77-132">Item</span></span>                                                                                      | <span data-ttu-id="51b77-133">描述</span><span class="sxs-lookup"><span data-stu-id="51b77-133">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51b77-134"><span id="DT_BOTTOM"></span><span id="dt_bottom"></span>DT \_ 底部</span><span class="sxs-lookup"><span data-stu-id="51b77-134"><span id="DT_BOTTOM"></span><span id="dt_bottom"></span>DT\_BOTTOM</span></span><br/>             | <span data-ttu-id="51b77-135">將文字對齊矩形底部。</span><span class="sxs-lookup"><span data-stu-id="51b77-135">Justify the text to the bottom of the rectangle.</span></span> <span data-ttu-id="51b77-136">此值必須與 DT 單行合併 \_ 。</span><span class="sxs-lookup"><span data-stu-id="51b77-136">This value must be combined with DT\_SINGLELINE.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="51b77-137"><span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>DT \_ CALCRECT</span><span class="sxs-lookup"><span data-stu-id="51b77-137"><span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>DT\_CALCRECT</span></span><br/>       | <span data-ttu-id="51b77-138">告訴 DrawText 根據您告訴它繪製的字串長度，自動計算矩形的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="51b77-138">Tell DrawText to automatically calculate the width and height of the rectangle based on the length of the string you tell it to draw.</span></span> <span data-ttu-id="51b77-139">如果有多行文字，ID3DX10Font：:D rawText 會使用 pRect 參數所指向之矩形的寬度，並擴充矩形的基底以系結最後一行文字。</span><span class="sxs-lookup"><span data-stu-id="51b77-139">If there are multiple lines of text, ID3DX10Font::DrawText uses the width of the rectangle pointed to by the pRect parameter and extends the base of the rectangle to bound the last line of text.</span></span> <span data-ttu-id="51b77-140">如果只有一行文字，ID3DX10Font：:D rawText 會修改矩形的右邊，使其限定該行中的最後一個字元。</span><span class="sxs-lookup"><span data-stu-id="51b77-140">If there is only one line of text, ID3DX10Font::DrawText modifies the right side of the rectangle so that it bounds the last character in the line.</span></span> <span data-ttu-id="51b77-141">在任一種情況下，ID3DX10Font：:D rawText 都會傳回格式化文字的高度，但不會繪製文字。</span><span class="sxs-lookup"><span data-stu-id="51b77-141">In either case, ID3DX10Font::DrawText returns the height of the formatted text but does not draw the text.</span></span><br/> |
| <span data-ttu-id="51b77-142"><span id="DT_CENTER"></span><span id="dt_center"></span>DT \_ CENTER</span><span class="sxs-lookup"><span data-stu-id="51b77-142"><span id="DT_CENTER"></span><span id="dt_center"></span>DT\_CENTER</span></span><br/>             | <span data-ttu-id="51b77-143">在矩形中水準置中文字。</span><span class="sxs-lookup"><span data-stu-id="51b77-143">Center text horizontally in the rectangle.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="51b77-144"><span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>DT \_ EXPANDTABS</span><span class="sxs-lookup"><span data-stu-id="51b77-144"><span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>DT\_EXPANDTABS</span></span><br/> | <span data-ttu-id="51b77-145">展開 [tab 字元]。</span><span class="sxs-lookup"><span data-stu-id="51b77-145">Expand tab characters.</span></span> <span data-ttu-id="51b77-146">每個定位預設有八個字元。</span><span class="sxs-lookup"><span data-stu-id="51b77-146">The default number of characters per tab is eight.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="51b77-147"><span id="DT_LEFT"></span><span id="dt_left"></span>\_向左 DT</span><span class="sxs-lookup"><span data-stu-id="51b77-147"><span id="DT_LEFT"></span><span id="dt_left"></span>DT\_LEFT</span></span><br/>                   | <span data-ttu-id="51b77-148">將文字靠左對齊。</span><span class="sxs-lookup"><span data-stu-id="51b77-148">Align text to the left.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="51b77-149"><span id="DT_NOCLIP"></span><span id="dt_noclip"></span>DT \_ NOCLIP</span><span class="sxs-lookup"><span data-stu-id="51b77-149"><span id="DT_NOCLIP"></span><span id="dt_noclip"></span>DT\_NOCLIP</span></span><br/>             | <span data-ttu-id="51b77-150">繪製而不剪下。</span><span class="sxs-lookup"><span data-stu-id="51b77-150">Draw without clipping.</span></span> <span data-ttu-id="51b77-151">ID3DX10Font：使用 DT NOCLIP 時，:D rawText 會稍微快一點 \_ 。</span><span class="sxs-lookup"><span data-stu-id="51b77-151">ID3DX10Font::DrawText is somewhat faster when DT\_NOCLIP is used.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="51b77-152"><span id="DT_RIGHT"></span><span id="dt_right"></span>DT \_ 右邊</span><span class="sxs-lookup"><span data-stu-id="51b77-152"><span id="DT_RIGHT"></span><span id="dt_right"></span>DT\_RIGHT</span></span><br/>                | <span data-ttu-id="51b77-153">將文字靠右對齊。</span><span class="sxs-lookup"><span data-stu-id="51b77-153">Align text to the right.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="51b77-154"><span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>DT \_ RTLREADING</span><span class="sxs-lookup"><span data-stu-id="51b77-154"><span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>DT\_RTLREADING</span></span><br/> | <span data-ttu-id="51b77-155">當選取希伯來文或阿拉伯文字型時，以由右至左的讀取順序來顯示雙向文字的文字。</span><span class="sxs-lookup"><span data-stu-id="51b77-155">Display text in right-to-left reading order for bidirectional text when a Hebrew or Arabic font is selected.</span></span> <span data-ttu-id="51b77-156">所有文字的預設讀取順序都是由左至右。</span><span class="sxs-lookup"><span data-stu-id="51b77-156">The default reading order for all text is left-to-right.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="51b77-157"><span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>DT \_ 單行</span><span class="sxs-lookup"><span data-stu-id="51b77-157"><span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>DT\_SINGLELINE</span></span><br/> | <span data-ttu-id="51b77-158">只在單一行上顯示文字。</span><span class="sxs-lookup"><span data-stu-id="51b77-158">Display text on a single line only.</span></span> <span data-ttu-id="51b77-159">換行字元和換行字元不會中斷。</span><span class="sxs-lookup"><span data-stu-id="51b77-159">Carriage returns and line feeds do not break the line.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="51b77-160"><span id="DT_TOP"></span><span id="dt_top"></span>DT \_ TOP</span><span class="sxs-lookup"><span data-stu-id="51b77-160"><span id="DT_TOP"></span><span id="dt_top"></span>DT\_TOP</span></span><br/>                      | <span data-ttu-id="51b77-161">頂端對齊文字。</span><span class="sxs-lookup"><span data-stu-id="51b77-161">Top-justify text.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="51b77-162"><span id="DT_VCENTER"></span><span id="dt_vcenter"></span>DT \_ VCENTER</span><span class="sxs-lookup"><span data-stu-id="51b77-162"><span id="DT_VCENTER"></span><span id="dt_vcenter"></span>DT\_VCENTER</span></span><br/>          | <span data-ttu-id="51b77-163">將文字置中垂直 (只) 一行。</span><span class="sxs-lookup"><span data-stu-id="51b77-163">Center text vertically (single line only).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="51b77-164"><span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>DT \_ WORDBREAK</span><span class="sxs-lookup"><span data-stu-id="51b77-164"><span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>DT\_WORDBREAK</span></span><br/>    | <span data-ttu-id="51b77-165">中斷單字。</span><span class="sxs-lookup"><span data-stu-id="51b77-165">Break words.</span></span> <span data-ttu-id="51b77-166">如果單字會延伸超出 pRect 參數所指定的矩形邊緣，單字之間的行會自動中斷。</span><span class="sxs-lookup"><span data-stu-id="51b77-166">Lines are automatically broken between words if a word would extend past the edge of the rectangle specified by the pRect parameter.</span></span> <span data-ttu-id="51b77-167">換行字元序列也會中斷這一行。</span><span class="sxs-lookup"><span data-stu-id="51b77-167">A carriage return/line feed sequence also breaks the line.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="51b77-168">*色彩* \[在\]</span><span class="sxs-lookup"><span data-stu-id="51b77-168">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51b77-169">類型： **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="51b77-169">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

<span data-ttu-id="51b77-170">文字的色彩。</span><span class="sxs-lookup"><span data-stu-id="51b77-170">Color of the text.</span></span> <span data-ttu-id="51b77-171">請參閱 [**D3DXCOLOR**](d3d10-d3dxcolor.md)。</span><span class="sxs-lookup"><span data-stu-id="51b77-171">See [**D3DXCOLOR**](d3d10-d3dxcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51b77-172">傳回值</span><span class="sxs-lookup"><span data-stu-id="51b77-172">Return value</span></span>

<span data-ttu-id="51b77-173">類型： **[ **INT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51b77-173">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="51b77-174">如果函式成功，則傳回值為邏輯單元中文字的高度。</span><span class="sxs-lookup"><span data-stu-id="51b77-174">If the function succeeds, the return value is the height of the text in logical units.</span></span> <span data-ttu-id="51b77-175">如果 \_ 指定了 DT VCENTER 或 dt \_ 底端，則傳回值是從 pRect (top 到所繪製文字底部) 的位移。</span><span class="sxs-lookup"><span data-stu-id="51b77-175">If DT\_VCENTER or DT\_BOTTOM is specified, the return value is the offset from pRect (top to the bottom) of the drawn text.</span></span> <span data-ttu-id="51b77-176">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="51b77-176">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="51b77-177">備註</span><span class="sxs-lookup"><span data-stu-id="51b77-177">Remarks</span></span>

<span data-ttu-id="51b77-178">這個方法的參數非常類似于 [GDI DrawText](/previous-versions//ms533909(v=vs.85)) 函式的參數。</span><span class="sxs-lookup"><span data-stu-id="51b77-178">The parameters of this method are very similar to those of the [GDI DrawText](/previous-versions//ms533909(v=vs.85)) function.</span></span>

<span data-ttu-id="51b77-179">這個方法支援 ANSI 和 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="51b77-179">This method supports both ANSI and Unicode strings.</span></span>

<span data-ttu-id="51b77-180">除非使用 DT \_ NOCLIP 格式，否則這個方法會將文字剪下，使其不會出現在指定的矩形之外。</span><span class="sxs-lookup"><span data-stu-id="51b77-180">Unless the DT\_NOCLIP format is used, this method clips the text so that it does not appear outside the specified rectangle.</span></span> <span data-ttu-id="51b77-181">除非指定了 DT 單行格式，否則所有格式都會假設有多行 \_ 。</span><span class="sxs-lookup"><span data-stu-id="51b77-181">All formatting is assumed to have multiple lines unless the DT\_SINGLELINE format is specified.</span></span>

<span data-ttu-id="51b77-182">如果選取的字型對矩形而言太大，則這個方法不會嘗試以較小的字型取代。</span><span class="sxs-lookup"><span data-stu-id="51b77-182">If the selected font is too large for the rectangle, this method does not attempt to substitute a smaller font.</span></span>

<span data-ttu-id="51b77-183">這個方法只支援行距和方向都為零的字型。</span><span class="sxs-lookup"><span data-stu-id="51b77-183">This method supports only fonts whose escapement and orientation are both zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="51b77-184">規格需求</span><span class="sxs-lookup"><span data-stu-id="51b77-184">Requirements</span></span>



| <span data-ttu-id="51b77-185">需求</span><span class="sxs-lookup"><span data-stu-id="51b77-185">Requirement</span></span> | <span data-ttu-id="51b77-186">值</span><span class="sxs-lookup"><span data-stu-id="51b77-186">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51b77-187">標頭</span><span class="sxs-lookup"><span data-stu-id="51b77-187">Header</span></span><br/>  | <dl> <span data-ttu-id="51b77-188"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="51b77-188"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="51b77-189">程式庫</span><span class="sxs-lookup"><span data-stu-id="51b77-189">Library</span></span><br/> | <dl> <span data-ttu-id="51b77-190"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="51b77-190"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51b77-191">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51b77-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51b77-192">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="51b77-192">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="51b77-193">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="51b77-193">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
