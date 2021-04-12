---
title: IDWriteFontFallback MapCharacters 方法
description: 決定用來呈現文字開頭範圍的適當字型。
ms.assetid: 9D3DBBF7-72D4-473D-A321-E64BC94493D5
keywords:
- MapCharacters 方法直接寫入
- MapCharacters 方法 Direct Write，IDWriteFontFallback 介面
- IDWriteFontFallback 介面 Direct Write，MapCharacters 方法
topic_type:
- apiref
api_name:
- IDWriteFontFallback.MapCharacters
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 428778afc12c668d284dffb5a8a6f734c03f0705
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317311"
---
# <a name="idwritefontfallbackmapcharacters-method"></a><span data-ttu-id="19437-106">IDWriteFontFallback：： MapCharacters 方法</span><span class="sxs-lookup"><span data-stu-id="19437-106">IDWriteFontFallback::MapCharacters method</span></span>

<span data-ttu-id="19437-107">決定用來呈現文字開頭範圍的適當字型。</span><span class="sxs-lookup"><span data-stu-id="19437-107">Determines an appropriate font to use to render the beginning range of text.</span></span>

## <a name="syntax"></a><span data-ttu-id="19437-108">語法</span><span class="sxs-lookup"><span data-stu-id="19437-108">Syntax</span></span>


```C++
HRESULT MapCharacters(
                       IDWriteTextAnalysisSource *source,
                       UINT32                    textPosition,
                       UINT32                    textLength,
  [in, optional]       IDWriteFontCollection     *baseFontCollection,
  [in, optional] const wchar_t                   *baseFamilyName,
                       DWRITE_FONT_WEIGHT        baseWeight,
                       DWRITE_FONT_STYLE         baseStyle,
                       DWRITE_FONT_STRETCH       baseStretch,
  [out]                UINT32                    *mappedLength,
  [out]                IDWriteFont               **mappedFont,
  [out]                FLOAT                     *scale
);
```



## <a name="parameters"></a><span data-ttu-id="19437-109">參數</span><span class="sxs-lookup"><span data-stu-id="19437-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19437-110">*source*</span><span class="sxs-lookup"><span data-stu-id="19437-110">*source*</span></span> 
</dt> <dd>

<span data-ttu-id="19437-111">類型： \**[**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) \** _</span><span class="sxs-lookup"><span data-stu-id="19437-111">Type: \**[**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource)\** _</span></span>

<span data-ttu-id="19437-112">文字來源執行會保存文字和地區設定。</span><span class="sxs-lookup"><span data-stu-id="19437-112">The text source implementation holds the text and locale.</span></span>

</dd> <dt>

<span data-ttu-id="19437-113">_textPosition \*</span><span class="sxs-lookup"><span data-stu-id="19437-113">_textPosition\*</span></span> 
</dt> <dd>

<span data-ttu-id="19437-114">類型： **UINT32**</span><span class="sxs-lookup"><span data-stu-id="19437-114">Type: **UINT32**</span></span>

<span data-ttu-id="19437-115">要分析的開始位置。</span><span class="sxs-lookup"><span data-stu-id="19437-115">Starting position to analyze.</span></span>

</dd> <dt>

<span data-ttu-id="19437-116">*textLength*</span><span class="sxs-lookup"><span data-stu-id="19437-116">*textLength*</span></span> 
</dt> <dd>

<span data-ttu-id="19437-117">類型： **UINT32**</span><span class="sxs-lookup"><span data-stu-id="19437-117">Type: **UINT32**</span></span>

<span data-ttu-id="19437-118">要分析的文字長度。</span><span class="sxs-lookup"><span data-stu-id="19437-118">Length of the text to analyze.</span></span>

</dd> <dt>

<span data-ttu-id="19437-119">*baseFontCollection* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="19437-119">*baseFontCollection* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="19437-120">類型： \**[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) \** _</span><span class="sxs-lookup"><span data-stu-id="19437-120">Type: \**[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)\** _</span></span>

<span data-ttu-id="19437-121">要使用的預設字型集合。</span><span class="sxs-lookup"><span data-stu-id="19437-121">Default font collection to use.</span></span>

</dd> <dt>

<span data-ttu-id="19437-122">_baseFamilyName \* \[ in，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="19437-122">_baseFamilyName\* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="19437-123">類型： \**const wchar \_ t \** _</span><span class="sxs-lookup"><span data-stu-id="19437-123">Type: \**const wchar\_t\** _</span></span>

<span data-ttu-id="19437-124">基底字型的系列名稱。</span><span class="sxs-lookup"><span data-stu-id="19437-124">Family name of the base font.</span></span> <span data-ttu-id="19437-125">如果您傳遞 null，則不會對該系列進行任何比對。</span><span class="sxs-lookup"><span data-stu-id="19437-125">If you pass null, no matching will be done against the family.</span></span>

</dd> <dt>

<span data-ttu-id="19437-126">_baseWeight \*</span><span class="sxs-lookup"><span data-stu-id="19437-126">_baseWeight\*</span></span> 
</dt> <dd>

<span data-ttu-id="19437-127">類型： **[ **DWRITE \_ 字型 \_ 粗細**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**</span><span class="sxs-lookup"><span data-stu-id="19437-127">Type: **[**DWRITE\_FONT\_WEIGHT**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**</span></span>

<span data-ttu-id="19437-128">所需的權數。</span><span class="sxs-lookup"><span data-stu-id="19437-128">The desired weight.</span></span>

</dd> <dt>

<span data-ttu-id="19437-129">*baseStyle*</span><span class="sxs-lookup"><span data-stu-id="19437-129">*baseStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="19437-130">類型： **[ **DWRITE \_ 字型 \_ 樣式**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**</span><span class="sxs-lookup"><span data-stu-id="19437-130">Type: **[**DWRITE\_FONT\_STYLE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**</span></span>

<span data-ttu-id="19437-131">所需的樣式。</span><span class="sxs-lookup"><span data-stu-id="19437-131">The desired style.</span></span>

</dd> <dt>

<span data-ttu-id="19437-132">*baseStretch*</span><span class="sxs-lookup"><span data-stu-id="19437-132">*baseStretch*</span></span> 
</dt> <dd>

<span data-ttu-id="19437-133">類型： **[ **DWRITE \_ 字型 \_ 延展**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**</span><span class="sxs-lookup"><span data-stu-id="19437-133">Type: **[**DWRITE\_FONT\_STRETCH**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**</span></span>

<span data-ttu-id="19437-134">所需的 stretch。</span><span class="sxs-lookup"><span data-stu-id="19437-134">The desired stretch.</span></span>

</dd> <dt>

<span data-ttu-id="19437-135">*mappedLength* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="19437-135">*mappedLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19437-136">類型： \**UINT32 \** _</span><span class="sxs-lookup"><span data-stu-id="19437-136">Type: \**UINT32\** _</span></span>

<span data-ttu-id="19437-137">對應至對應字型的文字長度。</span><span class="sxs-lookup"><span data-stu-id="19437-137">Length of text mapped to the mapped font.</span></span> <span data-ttu-id="19437-138">如果文字長度不是) 零，則這一律會小於或等於文字長度，並大於零 (，讓呼叫端前進至少一個字元。</span><span class="sxs-lookup"><span data-stu-id="19437-138">This will always be less than or equal to the text length and greater than zero (if the text length is non-zero) so the caller advances at least one character.</span></span>

</dd> <dt>

<span data-ttu-id="19437-139">_mappedFont \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="19437-139">_mappedFont\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19437-140">類型： **[ **IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***</span><span class="sxs-lookup"><span data-stu-id="19437-140">Type: **[**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***</span></span>

<span data-ttu-id="19437-141">應該用來呈現文字的第一個 *mappedLength* 字元的字型。</span><span class="sxs-lookup"><span data-stu-id="19437-141">The font that should be used to render the first *mappedLength* characters of the text.</span></span> <span data-ttu-id="19437-142">如果傳回 Null，這表示沒有字型可以轉譯文字，而 *mappedLength* 是要跳過的字元數 (以遺漏的圖像) 呈現。</span><span class="sxs-lookup"><span data-stu-id="19437-142">If it returns NULL, that means that no font can render the text, and *mappedLength* is the number of characters to skip (rendered with a missing glyph).</span></span>

</dd> <dt>

<span data-ttu-id="19437-143">*調整規模* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="19437-143">*scale* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19437-144">類型： \**FLOAT \** _</span><span class="sxs-lookup"><span data-stu-id="19437-144">Type: \**FLOAT\** _</span></span>

<span data-ttu-id="19437-145">縮放比例，以將所傳回字型的 em 大小乘以。</span><span class="sxs-lookup"><span data-stu-id="19437-145">Scale factor to multiply the em size of the returned font by.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19437-146">傳回值</span><span class="sxs-lookup"><span data-stu-id="19437-146">Return value</span></span>

<span data-ttu-id="19437-147">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="19437-147">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="19437-148">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="19437-148">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="19437-149">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="19437-149">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="19437-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="19437-150">Requirements</span></span>



| <span data-ttu-id="19437-151">需求</span><span class="sxs-lookup"><span data-stu-id="19437-151">Requirement</span></span> | <span data-ttu-id="19437-152">值</span><span class="sxs-lookup"><span data-stu-id="19437-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19437-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19437-153">Minimum supported client</span></span><br/> | <span data-ttu-id="19437-154">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19437-154">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="19437-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19437-155">Minimum supported server</span></span><br/> | <span data-ttu-id="19437-156">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19437-156">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="19437-157">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="19437-157">Minimum supported phone</span></span><br/>  | <span data-ttu-id="19437-158">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19437-158">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="19437-159">程式庫</span><span class="sxs-lookup"><span data-stu-id="19437-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="19437-160"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="19437-160"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="19437-161">DLL</span><span class="sxs-lookup"><span data-stu-id="19437-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19437-162"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19437-162"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="19437-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19437-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19437-164">**IDWriteFontFallback**</span><span class="sxs-lookup"><span data-stu-id="19437-164">**IDWriteFontFallback**</span></span>](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)
</dt> </dl>

 

