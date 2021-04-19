---
description: 定義字型的屬性。
ms.assetid: 6f456f26-3410-4205-a013-e3c12bf0feb1
title: 'D3DXFONT_DESC 結構 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFONT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: d7c142787e4e4fac5be53763a3c19fd86a27efd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992715"
---
# <a name="d3dxfont_desc-structure"></a><span data-ttu-id="bb5a9-103">D3DXFONT \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="bb5a9-103">D3DXFONT\_DESC structure</span></span>

<span data-ttu-id="bb5a9-104">定義字型的屬性。</span><span class="sxs-lookup"><span data-stu-id="bb5a9-104">Defines the attributes of a font.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb5a9-105">語法</span><span class="sxs-lookup"><span data-stu-id="bb5a9-105">Syntax</span></span>


```C++
typedef struct D3DXFONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName;
} D3DXFONT_DESC, *LPD3DXFONT_DESC;
```



## <a name="members"></a><span data-ttu-id="bb5a9-106">成員</span><span class="sxs-lookup"><span data-stu-id="bb5a9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bb5a9-107">**高度**</span><span class="sxs-lookup"><span data-stu-id="bb5a9-107">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="bb5a9-108">類型： **[ **INT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb5a9-108">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bb5a9-109">字型字元資料格或字元的高度（以邏輯單位表示）。</span><span class="sxs-lookup"><span data-stu-id="bb5a9-109">Height, in logical units, of the font's character cell or character.</span></span>

</dd> <dt>

<span data-ttu-id="bb5a9-110">**寬度**</span><span class="sxs-lookup"><span data-stu-id="bb5a9-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="bb5a9-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb5a9-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bb5a9-112">字型中字元的寬度（以邏輯單位表示）。</span><span class="sxs-lookup"><span data-stu-id="bb5a9-112">Width, in logical units, of characters in the font.</span></span>

</dd> <dt>

<span data-ttu-id="bb5a9-113">**Weight**</span><span class="sxs-lookup"><span data-stu-id="bb5a9-113">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="bb5a9-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb5a9-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bb5a9-115">字型的權數，範圍介於0到1000之間。</span><span class="sxs-lookup"><span data-stu-id="bb5a9-115">Weight of the font in the range from 0 through 1000.</span></span>

</dd> <dt>

<span data-ttu-id="bb5a9-116">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="bb5a9-116">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="bb5a9-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb5a9-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bb5a9-118">要求的 mip 層級數目。</span><span class="sxs-lookup"><span data-stu-id="bb5a9-118">Number of mip levels requested.</span></span> <span data-ttu-id="bb5a9-119">如果此值為零或 D3DX \_ 預設值，則會建立完整的 mipmap 鏈。</span><span class="sxs-lookup"><span data-stu-id="bb5a9-119">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span> <span data-ttu-id="bb5a9-120">如果值為1，則紋理空間的對應方式會與螢幕空間相同。</span><span class="sxs-lookup"><span data-stu-id="bb5a9-120">If the value is 1, the texture space is mapped identically to the screen space.</span></span>

</dd> <dt>

<span data-ttu-id="bb5a9-121">**斜體**</span><span class="sxs-lookup"><span data-stu-id="bb5a9-121">**Italic**</span></span>
</dt> <dd>

<span data-ttu-id="bb5a9-122">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb5a9-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bb5a9-123">針對斜體字型，設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="bb5a9-123">Set to **TRUE** for an Italic font.</span></span>

</dd> <dt>

<span data-ttu-id="bb5a9-124">**字元集**</span><span class="sxs-lookup"><span data-stu-id="bb5a9-124">**CharSet**</span></span>
</dt> <dd>

<span data-ttu-id="bb5a9-125">類型： **[**位元組**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb5a9-125">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bb5a9-126">字元集。</span><span class="sxs-lookup"><span data-stu-id="bb5a9-126">Character set.</span></span>

</dd> <dt>

<span data-ttu-id="bb5a9-127">**OutputPrecision**</span><span class="sxs-lookup"><span data-stu-id="bb5a9-127">**OutputPrecision**</span></span>
</dt> <dd>

<span data-ttu-id="bb5a9-128">類型： **[**位元組**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb5a9-128">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bb5a9-129">輸出精確度。</span><span class="sxs-lookup"><span data-stu-id="bb5a9-129">Output precision.</span></span> <span data-ttu-id="bb5a9-130">輸出精確度定義輸出必須符合要求的字型高度、寬度、字元方向、行距、音調和字型類型的程度。</span><span class="sxs-lookup"><span data-stu-id="bb5a9-130">The output precision defines how closely the output must match the requested font height, width, character orientation, escapement, pitch, and font type.</span></span>

</dd> <dt>

<span data-ttu-id="bb5a9-131">**品質**</span><span class="sxs-lookup"><span data-stu-id="bb5a9-131">**Quality**</span></span>
</dt> <dd>

<span data-ttu-id="bb5a9-132">類型： **[**位元組**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb5a9-132">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bb5a9-133">輸出品質。</span><span class="sxs-lookup"><span data-stu-id="bb5a9-133">Output quality.</span></span>

</dd> <dt>

<span data-ttu-id="bb5a9-134">**PitchAndFamily**</span><span class="sxs-lookup"><span data-stu-id="bb5a9-134">**PitchAndFamily**</span></span>
</dt> <dd>

<span data-ttu-id="bb5a9-135">類型： **[**位元組**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb5a9-135">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bb5a9-136">字型的音調和系列。</span><span class="sxs-lookup"><span data-stu-id="bb5a9-136">Pitch and family of the font.</span></span>

</dd> <dt>

<span data-ttu-id="bb5a9-137">**FaceName**</span><span class="sxs-lookup"><span data-stu-id="bb5a9-137">**FaceName**</span></span>
</dt> <dd>

<span data-ttu-id="bb5a9-138">類型： **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="bb5a9-138">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="bb5a9-139">以 null 終止的字串，或指定字型字型名稱的字元。</span><span class="sxs-lookup"><span data-stu-id="bb5a9-139">A null-terminated string or characters that specifies the typeface name of the font.</span></span> <span data-ttu-id="bb5a9-140">字串的長度不能超過32個字元，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="bb5a9-140">The length of the string must not exceed 32 characters, including the terminating null character.</span></span> <span data-ttu-id="bb5a9-141">如果 FaceName 是空字串，則會使用符合其他指定屬性的第一個字型。</span><span class="sxs-lookup"><span data-stu-id="bb5a9-141">If FaceName is an empty string, the first font that matches the other specified attributes will be used.</span></span> <span data-ttu-id="bb5a9-142">如果編譯器設定需要 Unicode，則資料類型 TCHAR 會解析為 WCHAR;否則，資料型別會解析為 CHAR。</span><span class="sxs-lookup"><span data-stu-id="bb5a9-142">If the compiler settings require Unicode, the data type TCHAR resolves to WCHAR; otherwise, the data type resolves to CHAR.</span></span> <span data-ttu-id="bb5a9-143">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="bb5a9-143">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb5a9-144">備註</span><span class="sxs-lookup"><span data-stu-id="bb5a9-144">Remarks</span></span>

<span data-ttu-id="bb5a9-145">編譯器設定也會決定結構類型。</span><span class="sxs-lookup"><span data-stu-id="bb5a9-145">The compiler setting also determines the structure type.</span></span> <span data-ttu-id="bb5a9-146">如果已定義 Unicode，D3DXFONT \_ DESC 結構類型會解析為 D3DXFONT \_ DESCW; 否則，結構類型會解析為 D3DXFONT \_ DESCA。</span><span class="sxs-lookup"><span data-stu-id="bb5a9-146">If Unicode is defined, the D3DXFONT\_DESC structure type resolves to a D3DXFONT\_DESCW; otherwise the structure type resolves to a D3DXFONT\_DESCA.</span></span>

<span data-ttu-id="bb5a9-147">GDI [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構中提供上述成員的可能值。</span><span class="sxs-lookup"><span data-stu-id="bb5a9-147">Possible values of the above members are given in the GDI [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb5a9-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb5a9-148">Requirements</span></span>



| <span data-ttu-id="bb5a9-149">需求</span><span class="sxs-lookup"><span data-stu-id="bb5a9-149">Requirement</span></span> | <span data-ttu-id="bb5a9-150">值</span><span class="sxs-lookup"><span data-stu-id="bb5a9-150">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb5a9-151">標頭</span><span class="sxs-lookup"><span data-stu-id="bb5a9-151">Header</span></span><br/> | <dl> <span data-ttu-id="bb5a9-152"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="bb5a9-152"><dt>D3dx9core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb5a9-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb5a9-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb5a9-154">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="bb5a9-154">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="bb5a9-155">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="bb5a9-155">**GetDesc**</span></span>](id3dxfont--getdesc.md)
</dt> </dl>

 

 
