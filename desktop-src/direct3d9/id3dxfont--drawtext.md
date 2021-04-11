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
ms.openlocfilehash: 96636c372ee48d516286935f03d80b8e9815ffc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196250"
---
# <a name="id3dxfontdrawtext-method"></a><span data-ttu-id="2314c-104">ID3DXFont：:D rawText 方法</span><span class="sxs-lookup"><span data-stu-id="2314c-104">ID3DXFont::DrawText method</span></span>

<span data-ttu-id="2314c-105">繪製格式化的文字。</span><span class="sxs-lookup"><span data-stu-id="2314c-105">Draws formatted text.</span></span> <span data-ttu-id="2314c-106">這個方法支援 ANSI 和 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="2314c-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="2314c-107">語法</span><span class="sxs-lookup"><span data-stu-id="2314c-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="2314c-108">參數</span><span class="sxs-lookup"><span data-stu-id="2314c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2314c-109">*pSprite* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2314c-109">*pSprite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2314c-110">類型： **[ **LPD3DXSPRITE**](id3dxsprite.md)**</span><span class="sxs-lookup"><span data-stu-id="2314c-110">Type: **[**LPD3DXSPRITE**](id3dxsprite.md)**</span></span>

<span data-ttu-id="2314c-111">包含字串之 [**ID3DXSprite**](id3dxsprite.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="2314c-111">Pointer to an [**ID3DXSprite**](id3dxsprite.md) object that contains the string.</span></span> <span data-ttu-id="2314c-112">可以是 **Null**，在此情況下，Direct3D 會以它自己的 sprite 物件轉譯字串。</span><span class="sxs-lookup"><span data-stu-id="2314c-112">Can be **NULL**, in which case Direct3D will render the string with its own sprite object.</span></span> <span data-ttu-id="2314c-113">為了提高效率，如果在資料列中呼叫 **DrawText** 一次以上，則應該指定 sprite 物件。</span><span class="sxs-lookup"><span data-stu-id="2314c-113">To improve efficiency, a sprite object should be specified if **DrawText** is to be called more than once in a row.</span></span>

</dd> <dt>

<span data-ttu-id="2314c-114">*pString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2314c-114">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2314c-115">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2314c-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2314c-116">要繪製之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="2314c-116">Pointer to a string to draw.</span></span> <span data-ttu-id="2314c-117">如果 Count 參數為-1，則字串必須以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="2314c-117">If the Count parameter is -1, the string must be null-terminated.</span></span>

</dd> <dt>

<span data-ttu-id="2314c-118">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2314c-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2314c-119">類型： **[ **INT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2314c-119">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2314c-120">指定字串中的字元數。</span><span class="sxs-lookup"><span data-stu-id="2314c-120">Specifies the number of characters in the string.</span></span> <span data-ttu-id="2314c-121">如果 Count 為-1，則會假設 pString 參數是以 null 終止之字串的指標，而 **DrawText** 會自動計算字元計數。</span><span class="sxs-lookup"><span data-stu-id="2314c-121">If Count is -1, then the pString parameter is assumed to be a pointer to a null-terminated string and **DrawText** computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="2314c-122">*pRect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2314c-122">*pRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2314c-123">類型： **[ **LPRECT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2314c-123">Type: **[**LPRECT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2314c-124">[**矩形結構的**](/previous-versions//dd162897(v=vs.85))指標，其中包含要格式化文字的矩形（以邏輯座標表示）。</span><span class="sxs-lookup"><span data-stu-id="2314c-124">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span> <span data-ttu-id="2314c-125">矩形右邊的座標值必須大於其左邊的座標值。</span><span class="sxs-lookup"><span data-stu-id="2314c-125">The coordinate value of the rectangle's right side must be greater than that of its left side.</span></span> <span data-ttu-id="2314c-126">同樣地，底部的座標值必須大於頂端的座標值。</span><span class="sxs-lookup"><span data-stu-id="2314c-126">Likewise, the coordinate value of the bottom must be greater than that of the top.</span></span>

</dd> <dt>

<span data-ttu-id="2314c-127">*格式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2314c-127">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2314c-128">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2314c-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2314c-129">指定格式化文字的方法。</span><span class="sxs-lookup"><span data-stu-id="2314c-129">Specifies the method of formatting the text.</span></span> <span data-ttu-id="2314c-130">它可以是下列值的任意組合：</span><span class="sxs-lookup"><span data-stu-id="2314c-130">It can be any combination of the following values:</span></span>



| <span data-ttu-id="2314c-131">值</span><span class="sxs-lookup"><span data-stu-id="2314c-131">Value</span></span>                                                                                                                                                         | <span data-ttu-id="2314c-132">意義</span><span class="sxs-lookup"><span data-stu-id="2314c-132">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span><dl> <span data-ttu-id="2314c-133"><dt>**DT \_ 底部**</dt></span><span class="sxs-lookup"><span data-stu-id="2314c-133"><dt>**DT\_BOTTOM**</dt></span></span> </dl>             | <span data-ttu-id="2314c-134">將文字對齊矩形的底部。</span><span class="sxs-lookup"><span data-stu-id="2314c-134">Justifies the text to the bottom of the rectangle.</span></span> <span data-ttu-id="2314c-135">此值必須與 DT 單行合併 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2314c-135">This value must be combined with DT\_SINGLELINE.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span><dl> <span data-ttu-id="2314c-136"><dt>**DT \_ CALCRECT**</dt></span><span class="sxs-lookup"><span data-stu-id="2314c-136"><dt>**DT\_CALCRECT**</dt></span></span> </dl>       | <span data-ttu-id="2314c-137">決定矩形的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="2314c-137">Determines the width and height of the rectangle.</span></span> <span data-ttu-id="2314c-138">如果有多行文字， **DrawText** 會使用 pRect 參數所指向之矩形的寬度，並將矩形的基底延伸至系結最後一行文字。</span><span class="sxs-lookup"><span data-stu-id="2314c-138">If there are multiple lines of text, **DrawText** uses the width of the rectangle pointed to by the pRect parameter and extends the base of the rectangle to bound the last line of text.</span></span> <span data-ttu-id="2314c-139">如果只有一行文字， **DrawText** 會修改矩形的右邊，使其系結該行中的最後一個字元。</span><span class="sxs-lookup"><span data-stu-id="2314c-139">If there is only one line of text, **DrawText** modifies the right side of the rectangle so that it bounds the last character in the line.</span></span> <span data-ttu-id="2314c-140">無論是哪一種情況， **DrawText** 都會傳回格式化文字的高度，但不會繪製文字。</span><span class="sxs-lookup"><span data-stu-id="2314c-140">In either case, **DrawText** returns the height of the formatted text but does not draw the text.</span></span><br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span><dl> <span data-ttu-id="2314c-141"><dt>**DT \_ CENTER**</dt></span><span class="sxs-lookup"><span data-stu-id="2314c-141"><dt>**DT\_CENTER**</dt></span></span> </dl>             | <span data-ttu-id="2314c-142">在矩形中將文字水準置中。</span><span class="sxs-lookup"><span data-stu-id="2314c-142">Centers text horizontally in the rectangle.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span><dl> <span data-ttu-id="2314c-143"><dt>**DT \_ EXPANDTABS**</dt></span><span class="sxs-lookup"><span data-stu-id="2314c-143"><dt>**DT\_EXPANDTABS**</dt></span></span> </dl> | <span data-ttu-id="2314c-144">展開定位字元。</span><span class="sxs-lookup"><span data-stu-id="2314c-144">Expands tab characters.</span></span> <span data-ttu-id="2314c-145">每個定位預設有八個字元。</span><span class="sxs-lookup"><span data-stu-id="2314c-145">The default number of characters per tab is eight.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span><dl> <span data-ttu-id="2314c-146"><dt>**\_向左 DT**</dt></span><span class="sxs-lookup"><span data-stu-id="2314c-146"><dt>**DT\_LEFT**</dt></span></span> </dl>                   | <span data-ttu-id="2314c-147">將文字靠左對齊。</span><span class="sxs-lookup"><span data-stu-id="2314c-147">Aligns text to the left.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span><dl> <span data-ttu-id="2314c-148"><dt>**DT \_ NOCLIP**</dt></span><span class="sxs-lookup"><span data-stu-id="2314c-148"><dt>**DT\_NOCLIP**</dt></span></span> </dl>             | <span data-ttu-id="2314c-149">繪製而不裁剪。</span><span class="sxs-lookup"><span data-stu-id="2314c-149">Draws without clipping.</span></span> <span data-ttu-id="2314c-150">使用 DT NOCLIP 時， **DrawText** 會稍微快一點 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2314c-150">**DrawText** is somewhat faster when DT\_NOCLIP is used.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="DT_RIGHT"></span><span id="dt_right"></span><dl> <span data-ttu-id="2314c-151"><dt>**DT \_ 右邊**</dt></span><span class="sxs-lookup"><span data-stu-id="2314c-151"><dt>**DT\_RIGHT**</dt></span></span> </dl>                | <span data-ttu-id="2314c-152">將文字對齊右邊。</span><span class="sxs-lookup"><span data-stu-id="2314c-152">Aligns text to the right.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span><dl> <span data-ttu-id="2314c-153"><dt>**DT \_ RTLREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="2314c-153"><dt>**DT\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="2314c-154">當選取希伯來文或阿拉伯文字型時，以由右至左的雙向文字讀取順序顯示文字。</span><span class="sxs-lookup"><span data-stu-id="2314c-154">Displays text in right-to-left reading order for bidirectional text when a Hebrew or Arabic font is selected.</span></span> <span data-ttu-id="2314c-155">所有文字的預設讀取順序都是由左至右。</span><span class="sxs-lookup"><span data-stu-id="2314c-155">The default reading order for all text is left-to-right.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span><dl> <span data-ttu-id="2314c-156"><dt>**DT \_ 單行**</dt></span><span class="sxs-lookup"><span data-stu-id="2314c-156"><dt>**DT\_SINGLELINE**</dt></span></span> </dl> | <span data-ttu-id="2314c-157">只在單一行上顯示文字。</span><span class="sxs-lookup"><span data-stu-id="2314c-157">Displays text on a single line only.</span></span> <span data-ttu-id="2314c-158">換行字元和換行字元不會中斷。</span><span class="sxs-lookup"><span data-stu-id="2314c-158">Carriage returns and line feeds do not break the line.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span><dl> <span data-ttu-id="2314c-159"><dt>**DT \_ TOP**</dt></span><span class="sxs-lookup"><span data-stu-id="2314c-159"><dt>**DT\_TOP**</dt></span></span> </dl>                      | <span data-ttu-id="2314c-160">靠上對齊文字。</span><span class="sxs-lookup"><span data-stu-id="2314c-160">Top-justifies text.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span><dl> <span data-ttu-id="2314c-161"><dt>**DT \_ VCENTER**</dt></span><span class="sxs-lookup"><span data-stu-id="2314c-161"><dt>**DT\_VCENTER**</dt></span></span> </dl>          | <span data-ttu-id="2314c-162">將文字水準置中 (單行) 。</span><span class="sxs-lookup"><span data-stu-id="2314c-162">Centers text vertically (single line only).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span><dl> <span data-ttu-id="2314c-163"><dt>**DT \_ WORDBREAK**</dt></span><span class="sxs-lookup"><span data-stu-id="2314c-163"><dt>**DT\_WORDBREAK**</dt></span></span> </dl>    | <span data-ttu-id="2314c-164">中斷單字。</span><span class="sxs-lookup"><span data-stu-id="2314c-164">Breaks words.</span></span> <span data-ttu-id="2314c-165">如果單字會延伸超出 pRect 參數所指定的矩形邊緣，單字之間的行會自動中斷。</span><span class="sxs-lookup"><span data-stu-id="2314c-165">Lines are automatically broken between words if a word would extend past the edge of the rectangle specified by the pRect parameter.</span></span> <span data-ttu-id="2314c-166">換行字元序列也會中斷這一行。</span><span class="sxs-lookup"><span data-stu-id="2314c-166">A carriage return/line feed sequence also breaks the line.</span></span><br/>                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="2314c-167">*色彩* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2314c-167">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2314c-168">類型： **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="2314c-168">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="2314c-169">文字的色彩。</span><span class="sxs-lookup"><span data-stu-id="2314c-169">Color of the text.</span></span> <span data-ttu-id="2314c-170">如需詳細資訊，請參閱 [**D3DCOLOR**](d3dcolor.md)。</span><span class="sxs-lookup"><span data-stu-id="2314c-170">For more information, see [**D3DCOLOR**](d3dcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2314c-171">傳回值</span><span class="sxs-lookup"><span data-stu-id="2314c-171">Return value</span></span>

<span data-ttu-id="2314c-172">類型： **[ **INT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2314c-172">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2314c-173">如果函式成功，則傳回值為邏輯單元中文字的高度。</span><span class="sxs-lookup"><span data-stu-id="2314c-173">If the function succeeds, the return value is the height of the text in logical units.</span></span> <span data-ttu-id="2314c-174">如果 \_ 指定了 DT VCENTER 或 dt \_ 底端，則傳回值是從 pRect (top 到所繪製文字底部) 的位移。</span><span class="sxs-lookup"><span data-stu-id="2314c-174">If DT\_VCENTER or DT\_BOTTOM is specified, the return value is the offset from pRect (top to the bottom) of the drawn text.</span></span> <span data-ttu-id="2314c-175">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="2314c-175">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2314c-176">備註</span><span class="sxs-lookup"><span data-stu-id="2314c-176">Remarks</span></span>

<span data-ttu-id="2314c-177">這個方法的參數非常類似于 GDI [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext) 函式的參數。</span><span class="sxs-lookup"><span data-stu-id="2314c-177">The parameters of this method are very similar to those of the GDI [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext) function.</span></span>

<span data-ttu-id="2314c-178">這個方法支援 ANSI 和 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="2314c-178">This method supports both ANSI and Unicode strings.</span></span>

<span data-ttu-id="2314c-179">必須在 [**BeginScene**](/windows/desktop/api) 內呼叫這個方法 .。。 [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) 組塊。</span><span class="sxs-lookup"><span data-stu-id="2314c-179">This method must be called inside a [**BeginScene**](/windows/desktop/api) ... [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) block.</span></span> <span data-ttu-id="2314c-180">唯一的例外狀況是當應用程式使用 DT \_ CALCRECT 來呼叫 DrawText，以計算指定文字區塊的大小時。</span><span class="sxs-lookup"><span data-stu-id="2314c-180">The only exception is when an application calls **DrawText** with DT\_CALCRECT to calculate the size of a given block of text.</span></span>

<span data-ttu-id="2314c-181">除非使用 DT \_ NOCLIP 格式，否則這個方法會將文字剪下，使其不會出現在指定的矩形之外。</span><span class="sxs-lookup"><span data-stu-id="2314c-181">Unless the DT\_NOCLIP format is used, this method clips the text so that it does not appear outside the specified rectangle.</span></span> <span data-ttu-id="2314c-182">除非指定了 DT 單行格式，否則所有格式都會假設有多行 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2314c-182">All formatting is assumed to have multiple lines unless the DT\_SINGLELINE format is specified.</span></span>

<span data-ttu-id="2314c-183">如果選取的字型對矩形而言太大，則這個方法不會嘗試以較小的字型取代。</span><span class="sxs-lookup"><span data-stu-id="2314c-183">If the selected font is too large for the rectangle, this method does not attempt to substitute a smaller font.</span></span>

<span data-ttu-id="2314c-184">這個方法只支援行距和方向都為零的字型。</span><span class="sxs-lookup"><span data-stu-id="2314c-184">This method supports only fonts whose escapement and orientation are both zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="2314c-185">規格需求</span><span class="sxs-lookup"><span data-stu-id="2314c-185">Requirements</span></span>



| <span data-ttu-id="2314c-186">需求</span><span class="sxs-lookup"><span data-stu-id="2314c-186">Requirement</span></span> | <span data-ttu-id="2314c-187">值</span><span class="sxs-lookup"><span data-stu-id="2314c-187">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2314c-188">標頭</span><span class="sxs-lookup"><span data-stu-id="2314c-188">Header</span></span><br/>  | <dl> <span data-ttu-id="2314c-189"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="2314c-189"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="2314c-190">程式庫</span><span class="sxs-lookup"><span data-stu-id="2314c-190">Library</span></span><br/> | <dl> <span data-ttu-id="2314c-191"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2314c-191"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2314c-192">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2314c-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2314c-193">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="2314c-193">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
