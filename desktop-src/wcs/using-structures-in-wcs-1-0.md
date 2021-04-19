---
title: 在 WCS 1.0 中使用結構
description: WCS 1.0 所使用的大部分結構非常簡單，只需要一點說明。 這些檔記載于有權參考結構的 WCS 1.0 參考區段中。
ms.assetid: 8d3682e2-38fd-4a33-b386-ab0716bb6972
keywords:
- Windows Color System (WCS) ，結構
- WCS (Windows 色彩系統) ，結構
- 影像色彩管理，結構
- 色彩管理，結構
- 色彩，結構
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d6e434ccfa6d96aa815f0c1997dc7f34178a32
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106982158"
---
# <a name="using-structures-in-wcs-10"></a><span data-ttu-id="f5769-109">在 WCS 1.0 中使用結構</span><span class="sxs-lookup"><span data-stu-id="f5769-109">Using Structures in WCS 1.0</span></span>

<span data-ttu-id="f5769-110">WCS 1.0 所使用的大部分結構非常簡單，只需要一點說明。</span><span class="sxs-lookup"><span data-stu-id="f5769-110">Most of the structures used by WCS 1.0 are very straightforward and require little explanation.</span></span> <span data-ttu-id="f5769-111">這些檔記載于有權參考 [結構](structures.md)的 WCS 1.0 參考區段中。</span><span class="sxs-lookup"><span data-stu-id="f5769-111">They are documented in the WCS 1.0 Reference section entitled [Structures](structures.md).</span></span>

<span data-ttu-id="f5769-112">例外狀況是 [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw)函數所使用的 [**COLORMATCHSETUPW**](/windows/win32/api/icm/ns-icm-colormatchsetupw)結構，以及 Wingdi 中定義的下列 Windows 結構：</span><span class="sxs-lookup"><span data-stu-id="f5769-112">Exceptions are the [**COLORMATCHSETUPW**](/windows/win32/api/icm/ns-icm-colormatchsetupw) structure used by the [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) function, and the following Windows structures defined in Wingdi.h:</span></span>

-   [<span data-ttu-id="f5769-113">BITMAPV5HEADER</span><span class="sxs-lookup"><span data-stu-id="f5769-113">BITMAPV5HEADER</span></span>](#windows-bitmap-header-structures)
-   [<span data-ttu-id="f5769-114">**LOGCOLORSPACE**</span><span class="sxs-lookup"><span data-stu-id="f5769-114">**LOGCOLORSPACE**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea)
-   [<span data-ttu-id="f5769-115">**CIEXYZ**</span><span class="sxs-lookup"><span data-stu-id="f5769-115">**CIEXYZ**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-tagciexyz)
-   [<span data-ttu-id="f5769-116">**CIEXYZTRIPLE**</span><span class="sxs-lookup"><span data-stu-id="f5769-116">**CIEXYZTRIPLE**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-tagicexyztriple)

<span data-ttu-id="f5769-117">下列主題會以更高的長度討論：</span><span class="sxs-lookup"><span data-stu-id="f5769-117">The following topics are discussed at greater length:</span></span>

-   [<span data-ttu-id="f5769-118">Windows 點陣圖標頭結構</span><span class="sxs-lookup"><span data-stu-id="f5769-118">Windows Bitmap Header Structures</span></span>](#windows-bitmap-header-structures)
-   [<span data-ttu-id="f5769-119">V4 和 V5 標頭之間的差異</span><span class="sxs-lookup"><span data-stu-id="f5769-119">Differences Between V4 and V5 Headers</span></span>](#differences-between-v4-and-v5-headers)
-   [<span data-ttu-id="f5769-120">Bitmap.exe：用於轉換點陣圖標頭的 Command-Line 公用程式</span><span class="sxs-lookup"><span data-stu-id="f5769-120">Bitmap.exe: a Command-Line Utility for Converting Bitmap Headers</span></span>](#bitmapexe-a-command-line-utility-for-converting-bitmap-headers)

## <a name="windows-bitmap-header-structures"></a><span data-ttu-id="f5769-121">Windows 點陣圖標頭結構</span><span class="sxs-lookup"><span data-stu-id="f5769-121">Windows Bitmap Header Structures</span></span>

<span data-ttu-id="f5769-122">WCS 1.0 允許將 ICC 色彩設定檔連結或內嵌于與裝置無關的點陣圖 (Dib) 。</span><span class="sxs-lookup"><span data-stu-id="f5769-122">WCS 1.0 allows ICC color profiles to be linked or embedded in device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="f5769-123">這可讓 DIB 色彩的特性比在 Windows 95 中使用 WCS 更準確。</span><span class="sxs-lookup"><span data-stu-id="f5769-123">This allows DIB colors to be characterized more accurately than was possible using WCS in Windows 95.</span></span> <span data-ttu-id="f5769-124">[BITMAPV5HEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) 是新的點陣圖標頭結構，在 Windows 98 版本的 Wingdi 中定義。</span><span class="sxs-lookup"><span data-stu-id="f5769-124">[BITMAPV5HEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) , the new bitmap header structure, is defined in Wingdi.h in the release of Windows 98.</span></span> <span data-ttu-id="f5769-125">基於開發目的，這個程式設計人員的參考也包含在 file Icm 中。</span><span class="sxs-lookup"><span data-stu-id="f5769-125">For development purposes, it is also included in the file Icm.h with this Programmer's Reference.</span></span> <span data-ttu-id="f5769-126">**BITMAPV5HEADER** 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="f5769-126">The **BITMAPV5HEADER** structure is as follows:</span></span>


```C++
typedef struct {
    DWORD        bV5Size;
    LONG         bV5Width;
    LONG         bV5Height;
    WORD         bV5Planes;
    WORD         bV5BitCount;
    DWORD        bV5Compression;
    DWORD        bV5SizeImage;
    LONG         bV5XPelsPerMeter;
    LONG         bV5YPelsPerMeter;
    DWORD        bV5ClrUsed;
    DWORD        bV5ClrImportant;
    DWORD        bV5RedMask;
    DWORD        bV5GreenMask;
    DWORD        bV5BlueMask;
    DWORD        bV5AlphaMask;
    DWORD        bV5CSType;
    CIEXYZTRIPLE bV5Endpoints;
    DWORD        bV5GammaRed;
    DWORD        bV5GammaGreen;
    DWORD        bV5GammaBlue;
    DWORD        bV5Intent;         // Rendering intent for bitmap 
    DWORD        bV5ProfileData;    // Offset to profile data 
    DWORD        bV5ProfileSize;    // Size of embedded profile data 
    DWORD        bV5Reserved;       // Should be zero 
} BITMAPV5HEADER, FAR *LPBITMAPV5HEADER, *PBITMAPV5HEADER;
```



<span data-ttu-id="f5769-127">成員 **bV5CSType** 可以將值設定檔 \_ 內嵌或設定檔 \_ 連結，以指定設定檔是否內嵌或連結到 DIB。</span><span class="sxs-lookup"><span data-stu-id="f5769-127">The member **bV5CSType** can have the values PROFILE\_EMBEDDED or PROFILE\_LINKED to specify whether a profile is embedded or linked with the DIB.</span></span> <span data-ttu-id="f5769-128">成員 **bV5ProfileData** 是從 **BITMAPV5HEADER** 結構的開頭到設定檔資料開頭的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f5769-128">The member **bV5ProfileData** is the offset in bytes from the beginning of the **BITMAPV5HEADER** structure to the start of the profile data.</span></span> <span data-ttu-id="f5769-129">如果設定檔是內嵌的，則設定檔資料是實際的設定檔，如果已連結，則設定檔資料是設定檔以 null 終止的檔案名。</span><span class="sxs-lookup"><span data-stu-id="f5769-129">If the profile is embedded, profile data is the actual profile, and if it is linked, the profile data is the null-terminated file name of the profile.</span></span> <span data-ttu-id="f5769-130">這不可以是 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="f5769-130">This cannot be a Unicode string.</span></span> <span data-ttu-id="f5769-131">它必須以專用於 Windows 字元集的字元來撰寫 (字碼頁 1252) 。</span><span class="sxs-lookup"><span data-stu-id="f5769-131">It must be composed exclusively of characters from the Windows character set (code page 1252).</span></span>

<span data-ttu-id="f5769-132">當 DIB 載入記憶體時，設定檔資料 (（如果有的話）) 應該接在 color 資料表之後， **bV5ProfileData** 就應該從 **BITMAPV5HEADER** 結構的開頭提供設定檔資料的位移。</span><span class="sxs-lookup"><span data-stu-id="f5769-132">When a DIB is loaded into memory, the profile data (if present) should follow the color table, and **bV5ProfileData** should give the offset of the profile data from the beginning of the **BITMAPV5HEADER** structure.</span></span> <span data-ttu-id="f5769-133">此成員的值現在將會不同，因為點陣圖位不會在記憶體中的色彩表之後。</span><span class="sxs-lookup"><span data-stu-id="f5769-133">The value of this member will be different now, as the bitmap bits do not follow the color table in memory.</span></span> <span data-ttu-id="f5769-134">應用程式應該在將 DIB 載入記憶體之後，修改 **bV5ProfileData** 成員。</span><span class="sxs-lookup"><span data-stu-id="f5769-134">Applications should modify the **bV5ProfileData** member after loading the DIB into memory.</span></span>

<span data-ttu-id="f5769-135">針對壓縮的 Dib，設定檔資料應遵循點陣圖位，類似于檔案格式。</span><span class="sxs-lookup"><span data-stu-id="f5769-135">For packed DIBs, the profile data should follow the bitmap bits similar to the file format.</span></span> <span data-ttu-id="f5769-136">**BV5ProfileData** 成員仍應從 **BITMAPV5HEADER** 結構的開頭提供設定檔資料的位移。</span><span class="sxs-lookup"><span data-stu-id="f5769-136">The **bV5ProfileData** member should still give the offset of the profile data from the beginning of the **BITMAPV5HEADER** structure.</span></span>

<span data-ttu-id="f5769-137">只有當 **bV5Size**  ==  **sizeof** ( **BITMAPV5HEADER** ) **ANDbV5CSType** 是設定檔 \_ 內嵌或設定檔連結時，應用程式才應該存取設定檔資料 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f5769-137">Applications should access the profile data only when **bV5Size** == **sizeof** ( **BITMAPV5HEADER** ) **ANDbV5CSType** is PROFILE\_EMBEDDED or PROFILE\_LINKED.</span></span>

<span data-ttu-id="f5769-138">如果設定檔連結，設定檔的路徑可以是任何完整名稱 (包括可以使用 Win32 **CreateFile** 函數開啟的網路路徑) 。</span><span class="sxs-lookup"><span data-stu-id="f5769-138">If a profile is linked, the path of the profile can be any fully qualified name (including a network path) that can be opened using the Win32 **CreateFile** function.</span></span>

## <a name="differences-between-v4-and-v5-headers"></a><span data-ttu-id="f5769-139">V4 和 V5 標頭之間的差異</span><span class="sxs-lookup"><span data-stu-id="f5769-139">Differences Between V4 and V5 Headers</span></span>

<span data-ttu-id="f5769-140">使用新的點陣圖結構時，辨識 **BITMAPV4HEADER** 和 **BITMAPV5HEADER** 結構設定方式的差異會很有用：</span><span class="sxs-lookup"><span data-stu-id="f5769-140">In working with the new bitmap structure, it is useful to recognize differences in how **BITMAPV4HEADER** and **BITMAPV5HEADER** structures are set up:</span></span>



| <span data-ttu-id="f5769-141">V4 標頭</span><span class="sxs-lookup"><span data-stu-id="f5769-141">V4 Header</span></span>     | <span data-ttu-id="f5769-142">意義</span><span class="sxs-lookup"><span data-stu-id="f5769-142">Meaning</span></span>                                                                                                                              |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5769-143">**bV4CSType**</span><span class="sxs-lookup"><span data-stu-id="f5769-143">**bV4CSType**</span></span> | <span data-ttu-id="f5769-144">LCS \_ 校正 \_ 的 RGB。</span><span class="sxs-lookup"><span data-stu-id="f5769-144">LCS\_CALIBRATED\_RGB.</span></span> <span data-ttu-id="f5769-145">這個值表示會在適當的欄位中提供端點和 gammas。</span><span class="sxs-lookup"><span data-stu-id="f5769-145">This value implies that end points and gammas are given in the appropriate fields.</span></span> <span data-ttu-id="f5769-146">假值會造成問題。</span><span class="sxs-lookup"><span data-stu-id="f5769-146">Bogus values cause trouble.</span></span> |
| <span data-ttu-id="f5769-147">**bV4CSType**</span><span class="sxs-lookup"><span data-stu-id="f5769-147">**bV4CSType**</span></span> | <span data-ttu-id="f5769-148">LCS \_ sRGB。</span><span class="sxs-lookup"><span data-stu-id="f5769-148">LCS\_sRGB.</span></span> <span data-ttu-id="f5769-149">此值表示點陣圖位於 sRGB 色彩空間 (gammas，且已忽略) 的端點。</span><span class="sxs-lookup"><span data-stu-id="f5769-149">This value implies that the bitmap is in sRGB color space (gammas and endpoints ignored).</span></span>                                 |
| <span data-ttu-id="f5769-150">**bV4CSType**</span><span class="sxs-lookup"><span data-stu-id="f5769-150">**bV4CSType**</span></span> | <span data-ttu-id="f5769-151">LCS \_ WINDOWS \_ 色彩 \_ 空間。</span><span class="sxs-lookup"><span data-stu-id="f5769-151">LCS\_WINDOWS\_COLOR\_SPACE.</span></span> <span data-ttu-id="f5769-152">此值表示點陣圖在 Windows 預設色彩空間中。</span><span class="sxs-lookup"><span data-stu-id="f5769-152">This value implies that the bitmap is in Windows default color space.</span></span>                                    |



 



| <span data-ttu-id="f5769-153">V5 標頭</span><span class="sxs-lookup"><span data-stu-id="f5769-153">V5 Header</span></span>     | <span data-ttu-id="f5769-154">意義</span><span class="sxs-lookup"><span data-stu-id="f5769-154">Meaning</span></span>                                                                                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5769-155">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="f5769-155">**bV5CSType**</span></span> | <span data-ttu-id="f5769-156">LCS \_ 校正 \_ 的 RGB。</span><span class="sxs-lookup"><span data-stu-id="f5769-156">LCS\_CALIBRATED\_RGB.</span></span> <span data-ttu-id="f5769-157">這個值表示會在適當的欄位中提供端點和 gammas。</span><span class="sxs-lookup"><span data-stu-id="f5769-157">This value implies that end points and gammas are given in the appropriate fields.</span></span> <span data-ttu-id="f5769-158">假值會造成問題。</span><span class="sxs-lookup"><span data-stu-id="f5769-158">Bogus values cause trouble.</span></span>                         |
| <span data-ttu-id="f5769-159">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="f5769-159">**bV5CSType**</span></span> | <span data-ttu-id="f5769-160">LCS \_ sRGB。</span><span class="sxs-lookup"><span data-stu-id="f5769-160">LCS\_sRGB.</span></span> <span data-ttu-id="f5769-161">此值表示點陣圖位於 sRGB 色彩空間 (gammas，且已忽略) 的端點。</span><span class="sxs-lookup"><span data-stu-id="f5769-161">This value implies that the bitmap is in sRGB color space (gammas and endpoints ignored).</span></span>                                                         |
| <span data-ttu-id="f5769-162">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="f5769-162">**bV5CSType**</span></span> | <span data-ttu-id="f5769-163">\_內嵌的設定檔。</span><span class="sxs-lookup"><span data-stu-id="f5769-163">PROFILE\_EMBEDDED.</span></span> <span data-ttu-id="f5769-164">此值表示 **bV5ProfileData** 指向記憶體緩衝區，其中包含要使用的設定檔 (gammas 和端點會被忽略) 。</span><span class="sxs-lookup"><span data-stu-id="f5769-164">This value implies that **bV5ProfileData** points to a memory buffer that contains the profile to use (gammas and endpoints are ignored).</span></span> |
| <span data-ttu-id="f5769-165">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="f5769-165">**bV5CSType**</span></span> | <span data-ttu-id="f5769-166">設定檔已 \_ 連結。</span><span class="sxs-lookup"><span data-stu-id="f5769-166">PROFILE\_LINKED.</span></span> <span data-ttu-id="f5769-167">此值表示 **bV5ProfileData** 會指向要使用之設定檔的檔案名 (gammas 和端點會被忽略) 。</span><span class="sxs-lookup"><span data-stu-id="f5769-167">This value implies that **bV5ProfileData** points to the file name of the profile to use (gammas and endpoints are ignored).</span></span>                |
| <span data-ttu-id="f5769-168">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="f5769-168">**bV5CSType**</span></span> | <span data-ttu-id="f5769-169">LCS \_ WINDOWS \_ 色彩 \_ 空間。</span><span class="sxs-lookup"><span data-stu-id="f5769-169">LCS\_WINDOWS\_COLOR\_SPACE.</span></span> <span data-ttu-id="f5769-170">此值表示點陣圖在 Windows 預設色彩空間中。</span><span class="sxs-lookup"><span data-stu-id="f5769-170">This value implies that the bitmap is in Windows default color space.</span></span>                                                            |



 

<span data-ttu-id="f5769-171">為了將舊版點陣圖轉換成新的 BITMAPV5HEADER 結構或從新的結構進行轉換，WCS 1.0 程式設計人員參考中包含名為 Bitmap.exe 的命令列轉換公用程式檔。</span><span class="sxs-lookup"><span data-stu-id="f5769-171">In order to convert older bitmaps to and from the new **BITMAPV5HEADER** structure, a command-line conversion utility file named Bitmap.exe is included in the WCS 1.0 Programmer's Reference.</span></span>

## <a name="bitmapexe-a-command-line-utility-for-converting-bitmap-headers"></a><span data-ttu-id="f5769-172">BitMap.exe：用於轉換點陣圖標頭的 Command-Line 公用程式</span><span class="sxs-lookup"><span data-stu-id="f5769-172">BitMap.exe: a Command-Line Utility for Converting Bitmap Headers</span></span>

<span data-ttu-id="f5769-173">Bitmap.exe 是一個命令列公用程式，位於 \\ 您指定之安裝資料夾下的 Bin 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="f5769-173">Bitmap.exe is a command-line utility located in the \\Bin folder under the installation folder that you specified.</span></span> <span data-ttu-id="f5769-174">它會修改 Windows 點陣圖的標頭，讓您可以將現有的點陣圖從 **BITMAPINFOHEADER** 和 **BITMAPV4HEADER** 標頭結構轉換為較新的 **BITMAPV5HEADER** 結構，再轉換回來。</span><span class="sxs-lookup"><span data-stu-id="f5769-174">It modifies the headers of Windows bitmaps, allowing you to convert existing bitmaps from **BITMAPINFOHEADER** and **BITMAPV4HEADER** header structures to the newer **BITMAPV5HEADER** structure and back again.</span></span> <span data-ttu-id="f5769-175">命令列語法如下所示：</span><span class="sxs-lookup"><span data-stu-id="f5769-175">The command-line syntax is as follows:</span></span>


```C++
BITMAP [/d] [/1|4|5] [/s] [/f] 
filename
```



<span data-ttu-id="f5769-176">命令列參數有下列效果。</span><span class="sxs-lookup"><span data-stu-id="f5769-176">The command-line switches have the following effects.</span></span>



| <span data-ttu-id="f5769-177">參數</span><span class="sxs-lookup"><span data-stu-id="f5769-177">Switch</span></span> | <span data-ttu-id="f5769-178">意義</span><span class="sxs-lookup"><span data-stu-id="f5769-178">Meaning</span></span>                                                                  |
|--------|--------------------------------------------------------------------------|
| <span data-ttu-id="f5769-179">/d</span><span class="sxs-lookup"><span data-stu-id="f5769-179">/d</span></span>     | <span data-ttu-id="f5769-180">預設值會自動輸入在轉換的標頭中。</span><span class="sxs-lookup"><span data-stu-id="f5769-180">Default values are automatically entered in the converted headers.</span></span>       |
| <span data-ttu-id="f5769-181">/1</span><span class="sxs-lookup"><span data-stu-id="f5769-181">/1</span></span>     | <span data-ttu-id="f5769-182">將指定的點陣圖轉換成 **BITMAPINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="f5769-182">Convert the specified bitmaps to **BITMAPINFOHEADER**</span></span>                    |
| <span data-ttu-id="f5769-183">/4</span><span class="sxs-lookup"><span data-stu-id="f5769-183">/4</span></span>     | <span data-ttu-id="f5769-184">將指定的點陣圖轉換成 **BITMAPV4HEADER**</span><span class="sxs-lookup"><span data-stu-id="f5769-184">Convert the specified bitmaps to **BITMAPV4HEADER**</span></span>                      |
| <span data-ttu-id="f5769-185">/5</span><span class="sxs-lookup"><span data-stu-id="f5769-185">/5</span></span>     | <span data-ttu-id="f5769-186">將指定的點陣圖轉換成 **BITMAPV5HEADER**</span><span class="sxs-lookup"><span data-stu-id="f5769-186">Convert the specified bitmaps to **BITMAPV5HEADER**</span></span>                      |
| <span data-ttu-id="f5769-187">/f</span><span class="sxs-lookup"><span data-stu-id="f5769-187">/f</span></span>     | <span data-ttu-id="f5769-188">強制轉換，即使點陣圖已經有右邊的標頭</span><span class="sxs-lookup"><span data-stu-id="f5769-188">Forces conversion, even if the bitmap already has the right header</span></span>       |
| <span data-ttu-id="f5769-189">/s</span><span class="sxs-lookup"><span data-stu-id="f5769-189">/s</span></span>     | <span data-ttu-id="f5769-190">轉換指定資料夾和其下所有子目錄中的點陣圖</span><span class="sxs-lookup"><span data-stu-id="f5769-190">Converts bitmaps in the specified folder and all subdirectories under it</span></span> |



 

 

 