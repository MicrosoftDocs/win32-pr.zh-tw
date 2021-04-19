---
description: 定義字型屬性。
ms.assetid: 66e8a320-2b83-4766-a9a7-5571ee6c9f2a
title: 'D3DX10_FONT_DESC 結構 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_FONT_DESC
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 0b358c57e6410827177e76e3da30b2f5f9896ee2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999002"
---
# <a name="d3dx10_font_desc-structure"></a><span data-ttu-id="b2b8f-103">D3DX10 \_ 字型 \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="b2b8f-103">D3DX10\_FONT\_DESC structure</span></span>

<span data-ttu-id="b2b8f-104">定義字型屬性。</span><span class="sxs-lookup"><span data-stu-id="b2b8f-104">Defines font attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2b8f-105">語法</span><span class="sxs-lookup"><span data-stu-id="b2b8f-105">Syntax</span></span>


```C++
typedef struct D3DX10_FONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName[LF_FACESIZE];
} D3DX10_FONT_DESC, *LPD3DX10_FONT_DESC;
```



## <a name="members"></a><span data-ttu-id="b2b8f-106">成員</span><span class="sxs-lookup"><span data-stu-id="b2b8f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b2b8f-107">**高度**</span><span class="sxs-lookup"><span data-stu-id="b2b8f-107">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="b2b8f-108">類型： **[ **INT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2b8f-108">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b2b8f-109">字型字元資料格或字元的高度（以邏輯單位表示）。</span><span class="sxs-lookup"><span data-stu-id="b2b8f-109">Height, in logical units, of the font's character cell or character.</span></span>

</dd> <dt>

<span data-ttu-id="b2b8f-110">**寬度**</span><span class="sxs-lookup"><span data-stu-id="b2b8f-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="b2b8f-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2b8f-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b2b8f-112">字型中字元的寬度（以邏輯單位表示）。</span><span class="sxs-lookup"><span data-stu-id="b2b8f-112">Width, in logical units, of characters in the font.</span></span>

</dd> <dt>

<span data-ttu-id="b2b8f-113">**Weight**</span><span class="sxs-lookup"><span data-stu-id="b2b8f-113">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="b2b8f-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2b8f-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b2b8f-115">字型的權數，範圍介於0到1000之間。</span><span class="sxs-lookup"><span data-stu-id="b2b8f-115">Weight of the font in the range from 0 through 1000.</span></span>

</dd> <dt>

<span data-ttu-id="b2b8f-116">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="b2b8f-116">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="b2b8f-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2b8f-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b2b8f-118">要求的 mipmap 層級數目。</span><span class="sxs-lookup"><span data-stu-id="b2b8f-118">Number of mipmap levels requested.</span></span> <span data-ttu-id="b2b8f-119">如果此值為零或 D3DX \_ 預設值，則會建立完整的 mipmap 鏈。</span><span class="sxs-lookup"><span data-stu-id="b2b8f-119">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span> <span data-ttu-id="b2b8f-120">如果值為1，則紋理空間的對應方式會與螢幕空間相同。</span><span class="sxs-lookup"><span data-stu-id="b2b8f-120">If the value is 1, the texture space is mapped identically to the screen space.</span></span>

</dd> <dt>

<span data-ttu-id="b2b8f-121">**斜體**</span><span class="sxs-lookup"><span data-stu-id="b2b8f-121">**Italic**</span></span>
</dt> <dd>

<span data-ttu-id="b2b8f-122">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2b8f-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b2b8f-123">針對斜體字型，設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="b2b8f-123">Set to **TRUE** for an Italic font.</span></span>

</dd> <dt>

<span data-ttu-id="b2b8f-124">**字元集**</span><span class="sxs-lookup"><span data-stu-id="b2b8f-124">**CharSet**</span></span>
</dt> <dd>

<span data-ttu-id="b2b8f-125">類型： **[**位元組**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2b8f-125">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b2b8f-126">字元集。</span><span class="sxs-lookup"><span data-stu-id="b2b8f-126">Character set.</span></span>

</dd> <dt>

<span data-ttu-id="b2b8f-127">**OutputPrecision**</span><span class="sxs-lookup"><span data-stu-id="b2b8f-127">**OutputPrecision**</span></span>
</dt> <dd>

<span data-ttu-id="b2b8f-128">類型： **[**位元組**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2b8f-128">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b2b8f-129">輸出精確度。</span><span class="sxs-lookup"><span data-stu-id="b2b8f-129">Output precision.</span></span> <span data-ttu-id="b2b8f-130">輸出精確度定義輸出必須符合要求的字型高度、寬度、字元方向、行距、音調和字型類型的程度。</span><span class="sxs-lookup"><span data-stu-id="b2b8f-130">The output precision defines how closely the output must match the requested font height, width, character orientation, escapement, pitch, and font type.</span></span>

</dd> <dt>

<span data-ttu-id="b2b8f-131">**品質**</span><span class="sxs-lookup"><span data-stu-id="b2b8f-131">**Quality**</span></span>
</dt> <dd>

<span data-ttu-id="b2b8f-132">類型： **[**位元組**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2b8f-132">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b2b8f-133">輸出品質。</span><span class="sxs-lookup"><span data-stu-id="b2b8f-133">Output quality.</span></span>

</dd> <dt>

<span data-ttu-id="b2b8f-134">**PitchAndFamily**</span><span class="sxs-lookup"><span data-stu-id="b2b8f-134">**PitchAndFamily**</span></span>
</dt> <dd>

<span data-ttu-id="b2b8f-135">類型： **[**位元組**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2b8f-135">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b2b8f-136">字型的音調和系列。</span><span class="sxs-lookup"><span data-stu-id="b2b8f-136">Pitch and family of the font.</span></span>

</dd> <dt>

<span data-ttu-id="b2b8f-137">**FaceName \[ LF \_ FACESIZE\]**</span><span class="sxs-lookup"><span data-stu-id="b2b8f-137">**FaceName\[LF\_FACESIZE\]**</span></span>
</dt> <dd>

<span data-ttu-id="b2b8f-138">類型： **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="b2b8f-138">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="b2b8f-139">以 Null 終止的字串，指定字型的字型名稱。</span><span class="sxs-lookup"><span data-stu-id="b2b8f-139">A NULL-terminated string that specifies the typeface name of the font.</span></span> <span data-ttu-id="b2b8f-140">字串的長度不能超過32個字元，包括結束的 **Null** 字元。</span><span class="sxs-lookup"><span data-stu-id="b2b8f-140">The length of the string must not exceed 32 characters, including the terminating **NULL** character.</span></span> <span data-ttu-id="b2b8f-141">如果 FaceName 是空字串，則會使用符合其他指定屬性的第一個字型。</span><span class="sxs-lookup"><span data-stu-id="b2b8f-141">If FaceName is an empty string, the first font that matches the other specified attributes will be used.</span></span> <span data-ttu-id="b2b8f-142">如果編譯器設定需要 Unicode，則資料類型 TCHAR 會解析為 WCHAR;否則，資料型別會解析為 CHAR。</span><span class="sxs-lookup"><span data-stu-id="b2b8f-142">If the compiler settings require Unicode, the data type TCHAR resolves to WCHAR; otherwise, the data type resolves to CHAR.</span></span> <span data-ttu-id="b2b8f-143">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="b2b8f-143">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2b8f-144">備註</span><span class="sxs-lookup"><span data-stu-id="b2b8f-144">Remarks</span></span>

<span data-ttu-id="b2b8f-145">編譯器設定也會決定結構類型。</span><span class="sxs-lookup"><span data-stu-id="b2b8f-145">The compiler setting also determines the structure type.</span></span> <span data-ttu-id="b2b8f-146">如果已定義 Unicode，D3DX10 \_ 字型 \_ DESC 結構類型會解析為 D3DX10 \_ 字型 \_ DESCW; 否則，結構類型會解析成 D3DX10 \_ 字型 \_ DESCA。</span><span class="sxs-lookup"><span data-stu-id="b2b8f-146">If Unicode is defined, the D3DX10\_FONT\_DESC structure type resolves to a D3DX10\_FONT\_DESCW; otherwise the structure type resolves to a D3DX10\_FONT\_DESCA.</span></span>

<span data-ttu-id="b2b8f-147">GDI [LOGFONT](/previous-versions//ms533931(v=vs.85)) 結構中提供上述成員的可能值。</span><span class="sxs-lookup"><span data-stu-id="b2b8f-147">Possible values of the above members are given in the GDI [LOGFONT](/previous-versions//ms533931(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2b8f-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2b8f-148">Requirements</span></span>



| <span data-ttu-id="b2b8f-149">需求</span><span class="sxs-lookup"><span data-stu-id="b2b8f-149">Requirement</span></span> | <span data-ttu-id="b2b8f-150">值</span><span class="sxs-lookup"><span data-stu-id="b2b8f-150">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b8f-151">標頭</span><span class="sxs-lookup"><span data-stu-id="b2b8f-151">Header</span></span><br/> | <dl> <span data-ttu-id="b2b8f-152"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="b2b8f-152"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2b8f-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2b8f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2b8f-154">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="b2b8f-154">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
