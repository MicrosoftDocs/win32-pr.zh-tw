---
description: 阿拉伯文和許多其他語言都具有傳統的數位圖形，與最常用於電腦的傳統西方數位不同。
ms.assetid: 6b5267d8-b102-410c-bdc9-831555ca2f84
title: 數位形狀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e6581b8b0eb87ae09b387c038c1ceba43125ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980002"
---
# <a name="digit-shapes"></a><span data-ttu-id="acd46-103">數位形狀</span><span class="sxs-lookup"><span data-stu-id="acd46-103">Digit Shapes</span></span>

<span data-ttu-id="acd46-104">阿拉伯文和許多其他語言都具有傳統的數位圖形，與最常用於電腦的傳統西方數位不同。</span><span class="sxs-lookup"><span data-stu-id="acd46-104">Arabic and many other languages have classical shapes for numbers that are different from the conventional western digits most often used on computers.</span></span> <span data-ttu-id="acd46-105">為了避免對這些圖形命名有不明確的情況，本檔會使用 Unicode 標準的下列名稱。</span><span class="sxs-lookup"><span data-stu-id="acd46-105">To avoid ambiguity in naming these shapes, this document uses the following names from the Unicode standard.</span></span>



| <span data-ttu-id="acd46-106">數位的 Unicode 名稱</span><span class="sxs-lookup"><span data-stu-id="acd46-106">Unicode name of the digits</span></span>                                     | <span data-ttu-id="acd46-107">使用的國家/地區</span><span class="sxs-lookup"><span data-stu-id="acd46-107">Country/region where used</span></span>                                    |
|----------------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="acd46-108">歐洲數位</span><span class="sxs-lookup"><span data-stu-id="acd46-108">European digits</span></span>                                                | <span data-ttu-id="acd46-109">歐洲、美洲及許多其他國家/地區</span><span class="sxs-lookup"><span data-stu-id="acd46-109">Europe, the Americas, and many other countries/regions</span></span>       |
| <span data-ttu-id="acd46-110">Arabic-Indic 數位</span><span class="sxs-lookup"><span data-stu-id="acd46-110">Arabic-Indic digits</span></span>                                            | <span data-ttu-id="acd46-111">阿拉伯文國家/地區 (雖然有許多使用歐洲位數) </span><span class="sxs-lookup"><span data-stu-id="acd46-111">Arabic countries/regions (although many use European digits)</span></span> |
| <span data-ttu-id="acd46-112">其他國家/地區數位：印度文數位、泰文數位和 like</span><span class="sxs-lookup"><span data-stu-id="acd46-112">Other national digits: Indic digits, Thai digits, and the like</span></span> | <span data-ttu-id="acd46-113">不同國家/地區</span><span class="sxs-lookup"><span data-stu-id="acd46-113">Various countries/regions</span></span>                                    |



 

<span data-ttu-id="acd46-114">Unicode 為每個數位圖形提供個別的程式碼點。</span><span class="sxs-lookup"><span data-stu-id="acd46-114">Unicode provides separate code points for each digit shape.</span></span> <span data-ttu-id="acd46-115">因此，若要存取特殊語言數位圖形，您的應用程式可以針對上述數位使用相關的 Unicode 字元碼，U + 0030 到 U + 0039。</span><span class="sxs-lookup"><span data-stu-id="acd46-115">Thus, to access special language digit shapes, your application can use the relevant Unicode character codes for the digits above, U+0030 through U+0039.</span></span> <span data-ttu-id="acd46-116">這些代碼一律會以適當的圖形顯示，且受限於字型的可用性。</span><span class="sxs-lookup"><span data-stu-id="acd46-116">These codes are always displayed with the appropriate shape, subject to font availability.</span></span>

<span data-ttu-id="acd46-117">Unicode 字元碼 U + 0030 到 U + 0039 名義上表示歐洲數位0到9，但可以改變其數位圖形。</span><span class="sxs-lookup"><span data-stu-id="acd46-117">The Unicode character codes U+0030 through U+0039 nominally represent the European digits 0 through 9, but their digit shape can be altered.</span></span> <span data-ttu-id="acd46-118">GDI 和 DirectWrite 文字 Api 提供應用程式控制此行為的機制。</span><span class="sxs-lookup"><span data-stu-id="acd46-118">GDI and DirectWrite text APIs provide mechanisms for applications to control this behavior.</span></span> <span data-ttu-id="acd46-119"> (請參閱，例如 [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) 或 [**IDWriteTextAnalysisSink：： SetNumberSubstitution**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution)。 ) 某些 shell 控制項和使用者介面架構中的行為，可能會回應使用者地區設定的數位替代; [地區設定 \_ IDIGITSUBSTITUTION](locale-idigitsubstitution.md) LCTYPE 可以用來取得不同地區設定的預設數位替代設定，或用於數位替換的目前使用者桌面設定。</span><span class="sxs-lookup"><span data-stu-id="acd46-119">(See, for instance, [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) or [**IDWriteTextAnalysisSink::SetNumberSubstitution**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution).) The behavior in some shell controls and user interface frameworks may respond to user locale settings for digit substitution; the [LOCALE\_IDIGITSUBSTITUTION](locale-idigitsubstitution.md) LCTYPE can be used to obtain default digit substitution settings for different locales or the current user's desktop settings for digit substitution.</span></span>

## <a name="native-digits"></a><span data-ttu-id="acd46-120">原生位數</span><span class="sxs-lookup"><span data-stu-id="acd46-120">Native Digits</span></span>

<span data-ttu-id="acd46-121">原生位數是使用者在主控台的 [地區及語言選項] 部分的 [ **數位** ] 屬性工作表中選擇的數位形狀。</span><span class="sxs-lookup"><span data-stu-id="acd46-121">Native digits are the digit shapes chosen by the user in the **Number** property sheet in the regional and language options portion of the Control Panel.</span></span> <span data-ttu-id="acd46-122">若要尋找使用者慣用的數位標記法，您的應用程式會使用 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 或 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) 函式搭配 [地區設定 \_ SNATIVEDIGITS](locale-snative-constants.md) 常數來表示地區設定資訊。</span><span class="sxs-lookup"><span data-stu-id="acd46-122">To find the digit presentation preferred by the user, your application uses the [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) or [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) function with the [LOCALE\_SNATIVEDIGITS](locale-snative-constants.md) constant representing the locale information.</span></span>

> [!Note]  
> <span data-ttu-id="acd46-123">通常，Unicode 數位代碼會在執行時間作業系統常式中產生。</span><span class="sxs-lookup"><span data-stu-id="acd46-123">Typically, Unicode digit codes are generated in runtime operating system routines.</span></span> <span data-ttu-id="acd46-124">因此，必須升級一般執行時間作業系統，應用程式才能適當地檢查 [地區設定 \_ SNATIVEDIGITS](locale-snative-constants.md) 。</span><span class="sxs-lookup"><span data-stu-id="acd46-124">Therefore, common runtime operating systems must be upgraded for the application to inspect [LOCALE\_SNATIVEDIGITS](locale-snative-constants.md) appropriately.</span></span>

 

## <a name="digit-substitution"></a><span data-ttu-id="acd46-125">數位替換</span><span class="sxs-lookup"><span data-stu-id="acd46-125">Digit Substitution</span></span>

<span data-ttu-id="acd46-126">應用程式可以使用數位替代來告訴作業系統如何透過 U + 0039 列印數位 U + 0030。</span><span class="sxs-lookup"><span data-stu-id="acd46-126">The application can use digit substitution to tell the operating system how to print digits U+0030 through U+0039.</span></span> <span data-ttu-id="acd46-127">[地區設定 \_ IDIGITSUBSTITUTION](locale-idigitsubstitution.md)常數控制這種作業。</span><span class="sxs-lookup"><span data-stu-id="acd46-127">The [LOCALE\_IDIGITSUBSTITUTION](locale-idigitsubstitution.md) constant controls this operation.</span></span>

## <a name="digit-shaping-for-a-single-function"></a><span data-ttu-id="acd46-128">單一函式的數位成形</span><span class="sxs-lookup"><span data-stu-id="acd46-128">Digit Shaping for a Single Function</span></span>

<span data-ttu-id="acd46-129">[ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta)、 [GetCharacterPlacement](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa)和[GCP \_ 結果](/windows/win32/api/wingdi/ns-wingdi-gcp_resultsa)函式具有旗標，可在函式呼叫期間管理 Unicode 程式碼 U + 0030 至 u + 0039 的替代。</span><span class="sxs-lookup"><span data-stu-id="acd46-129">The [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [GetCharacterPlacement](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa), and [GCP\_RESULTS](/windows/win32/api/wingdi/ns-wingdi-gcp_resultsa) functions have flags that govern the substitution of Unicode codes U+0030 through U+0039 for the duration of the function call.</span></span> <span data-ttu-id="acd46-130">這些旗標會覆寫主控台中的地區設定，但不會重設設定。</span><span class="sxs-lookup"><span data-stu-id="acd46-130">These flags override regional settings in the Control Panel, but do not reset the settings.</span></span> <span data-ttu-id="acd46-131">此外，它們不會覆寫 Unicode 代碼 NADS 和節點。</span><span class="sxs-lookup"><span data-stu-id="acd46-131">Also, they do not override the Unicode codes NADS and NODS.</span></span> <span data-ttu-id="acd46-132">以下是可用的旗標。</span><span class="sxs-lookup"><span data-stu-id="acd46-132">The following flags are available.</span></span>



| <span data-ttu-id="acd46-133">Flags</span><span class="sxs-lookup"><span data-stu-id="acd46-133">Flags</span></span>                 | <span data-ttu-id="acd46-134">使用的數位</span><span class="sxs-lookup"><span data-stu-id="acd46-134">Digits used</span></span>                      | <span data-ttu-id="acd46-135">使用於</span><span class="sxs-lookup"><span data-stu-id="acd46-135">Used in</span></span>                   |
|-----------------------|----------------------------------|---------------------------|
| <span data-ttu-id="acd46-136">ETO \_ NUMERICSLATIN</span><span class="sxs-lookup"><span data-stu-id="acd46-136">ETO\_NUMERICSLATIN</span></span>    | <span data-ttu-id="acd46-137">歐洲數位</span><span class="sxs-lookup"><span data-stu-id="acd46-137">European digits</span></span>                  | <span data-ttu-id="acd46-138">**ExtTextOut**</span><span class="sxs-lookup"><span data-stu-id="acd46-138">**ExtTextOut**</span></span>            |
| <span data-ttu-id="acd46-139">ETO \_ NUMERICSLOCAL</span><span class="sxs-lookup"><span data-stu-id="acd46-139">ETO\_NUMERICSLOCAL</span></span>    | <span data-ttu-id="acd46-140">適用于地區設定的數位</span><span class="sxs-lookup"><span data-stu-id="acd46-140">Digits appropriate to the locale</span></span> | <span data-ttu-id="acd46-141">**ExtTextOut**</span><span class="sxs-lookup"><span data-stu-id="acd46-141">**ExtTextOut**</span></span>            |
| <span data-ttu-id="acd46-142">GCP \_ NUMERICSLATIN</span><span class="sxs-lookup"><span data-stu-id="acd46-142">GCP\_NUMERICSLATIN</span></span>    | <span data-ttu-id="acd46-143">歐洲數位</span><span class="sxs-lookup"><span data-stu-id="acd46-143">European digits</span></span>                  | <span data-ttu-id="acd46-144">**GetCharacterPlacement**</span><span class="sxs-lookup"><span data-stu-id="acd46-144">**GetCharacterPlacement**</span></span> |
| <span data-ttu-id="acd46-145">GCP \_ NUMERICSLOCAL</span><span class="sxs-lookup"><span data-stu-id="acd46-145">GCP\_NUMERICSLOCAL</span></span>    | <span data-ttu-id="acd46-146">適用于地區設定的數位</span><span class="sxs-lookup"><span data-stu-id="acd46-146">Digits appropriate to the locale</span></span> | <span data-ttu-id="acd46-147">**GetCharacterPlacement**</span><span class="sxs-lookup"><span data-stu-id="acd46-147">**GetCharacterPlacement**</span></span> |
| <span data-ttu-id="acd46-148">GCPCLASS \_ LATINNUMBER</span><span class="sxs-lookup"><span data-stu-id="acd46-148">GCPCLASS\_LATINNUMBER</span></span> | <span data-ttu-id="acd46-149">歐洲數位</span><span class="sxs-lookup"><span data-stu-id="acd46-149">European digits</span></span>                  | <span data-ttu-id="acd46-150">**GCP \_ 結果**</span><span class="sxs-lookup"><span data-stu-id="acd46-150">**GCP\_RESULTS**</span></span>          |
| <span data-ttu-id="acd46-151">GCPCLASS \_ LOCALNUMBER</span><span class="sxs-lookup"><span data-stu-id="acd46-151">GCPCLASS\_LOCALNUMBER</span></span> | <span data-ttu-id="acd46-152">適用于地區設定的數位</span><span class="sxs-lookup"><span data-stu-id="acd46-152">Digits appropriate to the locale</span></span> | <span data-ttu-id="acd46-153">**GCP \_ 結果**</span><span class="sxs-lookup"><span data-stu-id="acd46-153">**GCP\_RESULTS**</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="acd46-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="acd46-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acd46-155">關於國家語言支援</span><span class="sxs-lookup"><span data-stu-id="acd46-155">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="acd46-156">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="acd46-156">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> <dt>

[<span data-ttu-id="acd46-157">**GetLocaleInfoEx**</span><span class="sxs-lookup"><span data-stu-id="acd46-157">**GetLocaleInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
</dt> </dl>

 

 
