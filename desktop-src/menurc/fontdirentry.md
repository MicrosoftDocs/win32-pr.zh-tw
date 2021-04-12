---
title: FONTDIRENTRY 結構
description: 包含字型資源群組中個別字型的相關資訊。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: 0ada2afe-b299-4ef2-99b7-96da10ee218a
keywords:
- FONTDIRENTRY 結構功能表和其他資源
topic_type:
- apiref
api_name:
- FONTDIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1cee72a490fd2b94b1c810797f656d81418c0f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464677"
---
# <a name="fontdirentry-structure"></a><span data-ttu-id="90827-105">FONTDIRENTRY 結構</span><span class="sxs-lookup"><span data-stu-id="90827-105">FONTDIRENTRY structure</span></span>

<span data-ttu-id="90827-106">包含字型資源群組中個別字型的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="90827-106">Contains information about an individual font in a font resource group.</span></span> <span data-ttu-id="90827-107">此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="90827-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="90827-108">語法</span><span class="sxs-lookup"><span data-stu-id="90827-108">Syntax</span></span>


```C++
typedef struct {
  WORD  dfVersion;
  DWORD dfSize;
  CHAR  dfCopyright[60];
  WORD  dfType;
  WORD  dfPoints;
  WORD  dfVertRes;
  WORD  dfHorizRes;
  WORD  dfAscent;
  WORD  dfInternalLeading;
  WORD  dfExternalLeading;
  BYTE  dfItalic;
  BYTE  dfUnderline;
  BYTE  dfStrikeOut;
  WORD  dfWeight;
  BYTE  dfCharSet;
  WORD  dfPixWidth;
  WORD  dfPixHeight;
  BYTE  dfPitchAndFamily;
  WORD  dfAvgWidth;
  WORD  dfMaxWidth;
  BYTE  dfFirstChar;
  BYTE  dfLastChar;
  BYTE  dfDefaultChar;
  BYTE  dfBreakChar;
  WORD  dfWidthBytes;
  DWORD dfDevice;
  DWORD dfFace;
  DWORD dfReserved;
  CHAR  szDeviceName;
  CHAR  szFaceName;
} FONTDIRENTRY;
```



## <a name="members"></a><span data-ttu-id="90827-109">成員</span><span class="sxs-lookup"><span data-stu-id="90827-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="90827-110">**dfVersion**</span><span class="sxs-lookup"><span data-stu-id="90827-110">**dfVersion**</span></span>
</dt> <dd>

<span data-ttu-id="90827-111">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="90827-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90827-112">工具可用來讀取和寫入資源檔的資源資料的使用者定義版本號碼。</span><span class="sxs-lookup"><span data-stu-id="90827-112">A user-defined version number for the resource data that tools can use to read and write resource files.</span></span>

</dd> <dt>

<span data-ttu-id="90827-113">**dfSize**</span><span class="sxs-lookup"><span data-stu-id="90827-113">**dfSize**</span></span>
</dt> <dd>

<span data-ttu-id="90827-114">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="90827-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="90827-115">檔案的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="90827-115">The size of the file, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="90827-116">**dfCopyright \[ 60\]**</span><span class="sxs-lookup"><span data-stu-id="90827-116">**dfCopyright\[60\]**</span></span>
</dt> <dd>

<span data-ttu-id="90827-117">類型： **CHAR**</span><span class="sxs-lookup"><span data-stu-id="90827-117">Type: **CHAR**</span></span>

</dd> <dd>

<span data-ttu-id="90827-118">字型供應商的著作權資訊。</span><span class="sxs-lookup"><span data-stu-id="90827-118">The font supplier's copyright information.</span></span>

</dd> <dt>

<span data-ttu-id="90827-119">**dfType**</span><span class="sxs-lookup"><span data-stu-id="90827-119">**dfType**</span></span>
</dt> <dd>

<span data-ttu-id="90827-120">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="90827-120">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90827-121">字型檔案的類型。</span><span class="sxs-lookup"><span data-stu-id="90827-121">The type of font file.</span></span>

</dd> <dt>

<span data-ttu-id="90827-122">**dfPoints**</span><span class="sxs-lookup"><span data-stu-id="90827-122">**dfPoints**</span></span>
</dt> <dd>

<span data-ttu-id="90827-123">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="90827-123">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90827-124">這個字元集最適合的點大小。</span><span class="sxs-lookup"><span data-stu-id="90827-124">The point size at which this character set looks best.</span></span>

</dd> <dt>

<span data-ttu-id="90827-125">**dfVertRes**</span><span class="sxs-lookup"><span data-stu-id="90827-125">**dfVertRes**</span></span>
</dt> <dd>

<span data-ttu-id="90827-126">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="90827-126">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90827-127">此字元集已數位化的垂直解析度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="90827-127">The vertical resolution, in dots per inch, at which this character set was digitized.</span></span>

</dd> <dt>

<span data-ttu-id="90827-128">**dfHorizRes**</span><span class="sxs-lookup"><span data-stu-id="90827-128">**dfHorizRes**</span></span>
</dt> <dd>

<span data-ttu-id="90827-129">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="90827-129">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90827-130">此字元集已數位化的水準解析度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="90827-130">The horizontal resolution, in dots per inch, at which this character set was digitized.</span></span>

</dd> <dt>

<span data-ttu-id="90827-131">**dfAscent**</span><span class="sxs-lookup"><span data-stu-id="90827-131">**dfAscent**</span></span>
</dt> <dd>

<span data-ttu-id="90827-132">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="90827-132">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90827-133">從字元定義儲存格頂端到印刷字型基準的距離。</span><span class="sxs-lookup"><span data-stu-id="90827-133">The distance from the top of a character definition cell to the baseline of the typographical font.</span></span>

</dd> <dt>

<span data-ttu-id="90827-134">**dfInternalLeading**</span><span class="sxs-lookup"><span data-stu-id="90827-134">**dfInternalLeading**</span></span>
</dt> <dd>

<span data-ttu-id="90827-135">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="90827-135">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90827-136">**DfPixHeight** 成員所設定之界限內的開頭數量。</span><span class="sxs-lookup"><span data-stu-id="90827-136">The amount of leading inside the bounds set by the **dfPixHeight** member.</span></span> <span data-ttu-id="90827-137">此區域可能會出現重音符號和其他的變音符號字元。</span><span class="sxs-lookup"><span data-stu-id="90827-137">Accent marks and other diacritical characters can occur in this area.</span></span>

</dd> <dt>

<span data-ttu-id="90827-138">**dfExternalLeading**</span><span class="sxs-lookup"><span data-stu-id="90827-138">**dfExternalLeading**</span></span>
</dt> <dd>

<span data-ttu-id="90827-139">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="90827-139">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90827-140">應用程式在資料列之間新增的額外前置量。</span><span class="sxs-lookup"><span data-stu-id="90827-140">The amount of extra leading that the application adds between rows.</span></span>

</dd> <dt>

<span data-ttu-id="90827-141">**dfItalic**</span><span class="sxs-lookup"><span data-stu-id="90827-141">**dfItalic**</span></span>
</dt> <dd>

<span data-ttu-id="90827-142">類型： **位元組**</span><span class="sxs-lookup"><span data-stu-id="90827-142">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="90827-143">如果不等於零，則為斜體字型。</span><span class="sxs-lookup"><span data-stu-id="90827-143">An italic font if not equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="90827-144">**dfUnderline**</span><span class="sxs-lookup"><span data-stu-id="90827-144">**dfUnderline**</span></span>
</dt> <dd>

<span data-ttu-id="90827-145">類型： **位元組**</span><span class="sxs-lookup"><span data-stu-id="90827-145">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="90827-146">如果不等於零，則為加上底線的字型。</span><span class="sxs-lookup"><span data-stu-id="90827-146">An underlined font if not equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="90827-147">**dfStrikeOut**</span><span class="sxs-lookup"><span data-stu-id="90827-147">**dfStrikeOut**</span></span>
</dt> <dd>

<span data-ttu-id="90827-148">類型： **位元組**</span><span class="sxs-lookup"><span data-stu-id="90827-148">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="90827-149">如果不等於零，則為刪除線字型。</span><span class="sxs-lookup"><span data-stu-id="90827-149">A strikeout font if not equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="90827-150">**dfWeight**</span><span class="sxs-lookup"><span data-stu-id="90827-150">**dfWeight**</span></span>
</dt> <dd>

<span data-ttu-id="90827-151">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="90827-151">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90827-152">範圍0到1000的字型粗細。</span><span class="sxs-lookup"><span data-stu-id="90827-152">The weight of the font in the range 0 through 1000.</span></span> <span data-ttu-id="90827-153">例如，400為羅馬，700為粗體。</span><span class="sxs-lookup"><span data-stu-id="90827-153">For example, 400 is roman and 700 is bold.</span></span> <span data-ttu-id="90827-154">如果此值為零，則會使用預設權數。</span><span class="sxs-lookup"><span data-stu-id="90827-154">If this value is zero, a default weight is used.</span></span> <span data-ttu-id="90827-155">如需其他定義的值，請參閱 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構的描述。</span><span class="sxs-lookup"><span data-stu-id="90827-155">For additional defined values, see the description of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> <dt>

<span data-ttu-id="90827-156">**dfCharSet**</span><span class="sxs-lookup"><span data-stu-id="90827-156">**dfCharSet**</span></span>
</dt> <dd>

<span data-ttu-id="90827-157">類型： **位元組**</span><span class="sxs-lookup"><span data-stu-id="90827-157">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="90827-158">字型的字元集。</span><span class="sxs-lookup"><span data-stu-id="90827-158">The character set of the font.</span></span> <span data-ttu-id="90827-159">如需預先定義的值，請參閱 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構的描述。</span><span class="sxs-lookup"><span data-stu-id="90827-159">For predefined values, see the description of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> <dt>

<span data-ttu-id="90827-160">**dfPixWidth**</span><span class="sxs-lookup"><span data-stu-id="90827-160">**dfPixWidth**</span></span>
</dt> <dd>

<span data-ttu-id="90827-161">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="90827-161">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90827-162">為向量字型進行數位化的格線寬度。</span><span class="sxs-lookup"><span data-stu-id="90827-162">The width of the grid on which a vector font was digitized.</span></span> <span data-ttu-id="90827-163">針對點陣字型，如果成員不等於零，則代表點陣圖中所有字元的寬度。</span><span class="sxs-lookup"><span data-stu-id="90827-163">For raster fonts, if the member is not equal to zero, it represents the width for all the characters in the bitmap.</span></span> <span data-ttu-id="90827-164">如果成員等於零，字型就會有可變寬度的字元。</span><span class="sxs-lookup"><span data-stu-id="90827-164">If the member is equal to zero, the font has variable-width characters.</span></span>

</dd> <dt>

<span data-ttu-id="90827-165">**dfPixHeight**</span><span class="sxs-lookup"><span data-stu-id="90827-165">**dfPixHeight**</span></span>
</dt> <dd>

<span data-ttu-id="90827-166">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="90827-166">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90827-167">點陣字型的字元點陣圖高度，或向量字型已數位化之格線的高度。</span><span class="sxs-lookup"><span data-stu-id="90827-167">The height of the character bitmap for raster fonts or the height of the grid on which a vector font was digitized.</span></span>

</dd> <dt>

<span data-ttu-id="90827-168">**dfPitchAndFamily**</span><span class="sxs-lookup"><span data-stu-id="90827-168">**dfPitchAndFamily**</span></span>
</dt> <dd>

<span data-ttu-id="90827-169">類型： **位元組**</span><span class="sxs-lookup"><span data-stu-id="90827-169">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="90827-170">字型的音調和系列。</span><span class="sxs-lookup"><span data-stu-id="90827-170">The pitch and the family of the font.</span></span> <span data-ttu-id="90827-171">如需詳細資訊，請參閱 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構的描述。</span><span class="sxs-lookup"><span data-stu-id="90827-171">For additional information, see the description of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> <dt>

<span data-ttu-id="90827-172">**dfAvgWidth**</span><span class="sxs-lookup"><span data-stu-id="90827-172">**dfAvgWidth**</span></span>
</dt> <dd>

<span data-ttu-id="90827-173">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="90827-173">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90827-174">字型中字元的平均寬度 (通常定義為字母 x) 的寬度。</span><span class="sxs-lookup"><span data-stu-id="90827-174">The average width of characters in the font (generally defined as the width of the letter x).</span></span> <span data-ttu-id="90827-175">此值不包含粗體或斜體字元所需的懸垂。</span><span class="sxs-lookup"><span data-stu-id="90827-175">This value does not include the overhang required for bold or italic characters.</span></span>

</dd> <dt>

<span data-ttu-id="90827-176">**dfMaxWidth**</span><span class="sxs-lookup"><span data-stu-id="90827-176">**dfMaxWidth**</span></span>
</dt> <dd>

<span data-ttu-id="90827-177">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="90827-177">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90827-178">字型中最寬字元的寬度。</span><span class="sxs-lookup"><span data-stu-id="90827-178">The width of the widest character in the font.</span></span>

</dd> <dt>

<span data-ttu-id="90827-179">**dfFirstChar**</span><span class="sxs-lookup"><span data-stu-id="90827-179">**dfFirstChar**</span></span>
</dt> <dd>

<span data-ttu-id="90827-180">類型： **位元組**</span><span class="sxs-lookup"><span data-stu-id="90827-180">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="90827-181">字型中定義的第一個字元碼。</span><span class="sxs-lookup"><span data-stu-id="90827-181">The first character code defined in the font.</span></span>

</dd> <dt>

<span data-ttu-id="90827-182">**dfLastChar**</span><span class="sxs-lookup"><span data-stu-id="90827-182">**dfLastChar**</span></span>
</dt> <dd>

<span data-ttu-id="90827-183">類型： **位元組**</span><span class="sxs-lookup"><span data-stu-id="90827-183">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="90827-184">在字型中定義的最後一個字元碼。</span><span class="sxs-lookup"><span data-stu-id="90827-184">The last character code defined in the font.</span></span>

</dd> <dt>

<span data-ttu-id="90827-185">**dfDefaultChar**</span><span class="sxs-lookup"><span data-stu-id="90827-185">**dfDefaultChar**</span></span>
</dt> <dd>

<span data-ttu-id="90827-186">類型： **位元組**</span><span class="sxs-lookup"><span data-stu-id="90827-186">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="90827-187">要替代字型中不是字元的字元。</span><span class="sxs-lookup"><span data-stu-id="90827-187">The character to substitute for characters not in the font.</span></span>

</dd> <dt>

<span data-ttu-id="90827-188">**dfBreakChar**</span><span class="sxs-lookup"><span data-stu-id="90827-188">**dfBreakChar**</span></span>
</dt> <dd>

<span data-ttu-id="90827-189">類型： **位元組**</span><span class="sxs-lookup"><span data-stu-id="90827-189">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="90827-190">將用來定義文字對齊方式之斷詞的字元。</span><span class="sxs-lookup"><span data-stu-id="90827-190">The character that will be used to define word breaks for text justification.</span></span>

</dd> <dt>

<span data-ttu-id="90827-191">**dfWidthBytes**</span><span class="sxs-lookup"><span data-stu-id="90827-191">**dfWidthBytes**</span></span>
</dt> <dd>

<span data-ttu-id="90827-192">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="90827-192">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90827-193">點陣圖每個資料列中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="90827-193">The number of bytes in each row of the bitmap.</span></span> <span data-ttu-id="90827-194">此值一律為偶數，因此資料列會在字邊界上開始。</span><span class="sxs-lookup"><span data-stu-id="90827-194">This value is always even so that the rows start on word boundaries.</span></span> <span data-ttu-id="90827-195">若為向量字型，此成員沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="90827-195">For vector fonts, this member has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="90827-196">**dfDevice**</span><span class="sxs-lookup"><span data-stu-id="90827-196">**dfDevice**</span></span>
</dt> <dd>

<span data-ttu-id="90827-197">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="90827-197">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="90827-198">檔案中的位移，表示指定裝置名稱的以 null 終止的字串。</span><span class="sxs-lookup"><span data-stu-id="90827-198">The offset in the file to a null-terminated string that specifies a device name.</span></span> <span data-ttu-id="90827-199">若為泛型字型，此值為零。</span><span class="sxs-lookup"><span data-stu-id="90827-199">For a generic font, this value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="90827-200">**dfFace**</span><span class="sxs-lookup"><span data-stu-id="90827-200">**dfFace**</span></span>
</dt> <dd>

<span data-ttu-id="90827-201">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="90827-201">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="90827-202">檔案中的位移，表示命名為以 null 終止的字串，該字串會為字樣命名。</span><span class="sxs-lookup"><span data-stu-id="90827-202">The offset in the file to a null-terminated string that names the typeface.</span></span>

</dd> <dt>

<span data-ttu-id="90827-203">**dfReserved**</span><span class="sxs-lookup"><span data-stu-id="90827-203">**dfReserved**</span></span>
</dt> <dd>

<span data-ttu-id="90827-204">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="90827-204">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="90827-205">這個成員是保留的。</span><span class="sxs-lookup"><span data-stu-id="90827-205">This member is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="90827-206">**szDeviceName**</span><span class="sxs-lookup"><span data-stu-id="90827-206">**szDeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="90827-207">類型： **CHAR**</span><span class="sxs-lookup"><span data-stu-id="90827-207">Type: **CHAR**</span></span>

</dd> <dd>

<span data-ttu-id="90827-208">如果指定特定裝置的字型檔案，則為裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="90827-208">The name of the device if this font file is designated for a specific device.</span></span>

</dd> <dt>

<span data-ttu-id="90827-209">**szFaceName**</span><span class="sxs-lookup"><span data-stu-id="90827-209">**szFaceName**</span></span>
</dt> <dd>

<span data-ttu-id="90827-210">類型： **CHAR**</span><span class="sxs-lookup"><span data-stu-id="90827-210">Type: **CHAR**</span></span>

</dd> <dd>

<span data-ttu-id="90827-211">字型的字型名稱。</span><span class="sxs-lookup"><span data-stu-id="90827-211">The typeface name of the font.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90827-212">備註</span><span class="sxs-lookup"><span data-stu-id="90827-212">Remarks</span></span>

<span data-ttu-id="90827-213">.Res 檔中的每個字型都有一個 **FONTDIRENTRY** 結構。</span><span class="sxs-lookup"><span data-stu-id="90827-213">There is one **FONTDIRENTRY** structure for every font in the .res file.</span></span> <span data-ttu-id="90827-214">使用字型資源產生 .res 檔案的應用程式，也必須將每個字型的 **FONTDIRENTRY** 結構新增至檔案。</span><span class="sxs-lookup"><span data-stu-id="90827-214">Applications that generate .res files with font resources must also add to the file a **FONTDIRENTRY** structure for each font.</span></span>

<span data-ttu-id="90827-215">字型聲明可以與中的其他資源宣告混合使用。RC 檔案，因為字型在 .res 檔中不需要是連續的。</span><span class="sxs-lookup"><span data-stu-id="90827-215">Font declarations can be mixed with other resource declarations in the .RC file because fonts do not need to be contiguous in the .res file.</span></span>

## <a name="requirements"></a><span data-ttu-id="90827-216">規格需求</span><span class="sxs-lookup"><span data-stu-id="90827-216">Requirements</span></span>



| <span data-ttu-id="90827-217">需求</span><span class="sxs-lookup"><span data-stu-id="90827-217">Requirement</span></span> | <span data-ttu-id="90827-218">值</span><span class="sxs-lookup"><span data-stu-id="90827-218">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="90827-219">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90827-219">Minimum supported client</span></span><br/> | <span data-ttu-id="90827-220">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90827-220">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="90827-221">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90827-221">Minimum supported server</span></span><br/> | <span data-ttu-id="90827-222">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90827-222">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="90827-223">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90827-223">See also</span></span>

<dl> <dt>

<span data-ttu-id="90827-224">**參考**</span><span class="sxs-lookup"><span data-stu-id="90827-224">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="90827-225">**DIRENTRY**</span><span class="sxs-lookup"><span data-stu-id="90827-225">**DIRENTRY**</span></span>](direntry.md)
</dt> <dt>

[<span data-ttu-id="90827-226">**FONTGROUPHDR**</span><span class="sxs-lookup"><span data-stu-id="90827-226">**FONTGROUPHDR**</span></span>](fontgrouphdr.md)
</dt> <dt>

<span data-ttu-id="90827-227">**概念**</span><span class="sxs-lookup"><span data-stu-id="90827-227">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="90827-228">資源</span><span class="sxs-lookup"><span data-stu-id="90827-228">Resources</span></span>](resources.md)
</dt> <dt>

<span data-ttu-id="90827-229">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="90827-229">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="90827-230">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="90827-230">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

