---
title: _BITMAPINFOHEADER 結構
description: '\_BITMAPINFOHEADER 結構會定義影片框架的格式。'
ms.assetid: 394b8ded-81db-4ad3-8cf7-086f1e832771
keywords:
- _BITMAPINFOHEADER 結構 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- _BITMAPINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481c80b6d209e0da8d00ef06d88392504bcae8e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995449"
---
# <a name="_bitmapinfoheader-structure"></a><span data-ttu-id="392c1-104">\_BITMAPINFOHEADER 結構</span><span class="sxs-lookup"><span data-stu-id="392c1-104">\_BITMAPINFOHEADER structure</span></span>

<span data-ttu-id="392c1-105">**\_ BITMAPINFOHEADER** 結構會定義影片框架的格式。</span><span class="sxs-lookup"><span data-stu-id="392c1-105">The **\_BITMAPINFOHEADER** structure defines the format of a video frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="392c1-106">語法</span><span class="sxs-lookup"><span data-stu-id="392c1-106">Syntax</span></span>


```C++
typedef struct _tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} _BITMAPINFOHEADER;
```



## <a name="members"></a><span data-ttu-id="392c1-107">成員</span><span class="sxs-lookup"><span data-stu-id="392c1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="392c1-108">**biSize**</span><span class="sxs-lookup"><span data-stu-id="392c1-108">**biSize**</span></span>
</dt> <dd>

<span data-ttu-id="392c1-109">指定結構所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="392c1-109">Specifies the number of bytes required by the structure.</span></span>

</dd> <dt>

<span data-ttu-id="392c1-110">**biWidth**</span><span class="sxs-lookup"><span data-stu-id="392c1-110">**biWidth**</span></span>
</dt> <dd>

<span data-ttu-id="392c1-111">指定點陣圖的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="392c1-111">Specifies the width of the bitmap, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="392c1-112">**biHeight**</span><span class="sxs-lookup"><span data-stu-id="392c1-112">**biHeight**</span></span>
</dt> <dd>

<span data-ttu-id="392c1-113">指定點陣圖的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="392c1-113">Specifies the height of the bitmap, in pixels.</span></span> <span data-ttu-id="392c1-114">如果 **biHeight** 是正數，則點陣圖是最下層的 DIB，而其原點是左下角。</span><span class="sxs-lookup"><span data-stu-id="392c1-114">If **biHeight** is positive, the bitmap is a bottom-up DIB and its origin is the lower-left corner.</span></span> <span data-ttu-id="392c1-115">如果 **biHeight** 是負數，則點陣圖是由上而下的 DIB，而其原點是左上角。</span><span class="sxs-lookup"><span data-stu-id="392c1-115">If **biHeight** is negative, the bitmap is a top-down DIB and its origin is the upper-left corner.</span></span> <span data-ttu-id="392c1-116">如果 **biHeight** 是負的，表示由上而下的 DIB， **BICOMPRESSION** 必須是 bi \_ RGB 或 bi \_ 位欄位。</span><span class="sxs-lookup"><span data-stu-id="392c1-116">If **biHeight** is negative, indicating a top-down DIB, **biCompression** must be either BI\_RGB or BI\_BITFIELDS.</span></span> <span data-ttu-id="392c1-117">無法壓縮由上而下的 Dib。</span><span class="sxs-lookup"><span data-stu-id="392c1-117">Top-down DIBs cannot be compressed.</span></span>

</dd> <dt>

<span data-ttu-id="392c1-118">**biPlanes**</span><span class="sxs-lookup"><span data-stu-id="392c1-118">**biPlanes**</span></span>
</dt> <dd>

<span data-ttu-id="392c1-119">指定目標裝置的平面數目。</span><span class="sxs-lookup"><span data-stu-id="392c1-119">Specifies the number of planes for the target device.</span></span> <span data-ttu-id="392c1-120">此值必須設定為1。</span><span class="sxs-lookup"><span data-stu-id="392c1-120">This value must be set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="392c1-121">**biBitCount**</span><span class="sxs-lookup"><span data-stu-id="392c1-121">**biBitCount**</span></span>
</dt> <dd>

<span data-ttu-id="392c1-122">指定每圖元的位數。</span><span class="sxs-lookup"><span data-stu-id="392c1-122">Specifies the number of bits per pixel.</span></span> <span data-ttu-id="392c1-123">**BITMAPINFOHEADER** 結構的 **biBitCount** 成員會決定用來定義每個圖元的位數，以及點陣圖中的最大色彩數目。</span><span class="sxs-lookup"><span data-stu-id="392c1-123">The **biBitCount** member of the **BITMAPINFOHEADER** structure determines the number of bits that define each pixel and the maximum number of colors in the bitmap.</span></span> <span data-ttu-id="392c1-124">此成員必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="392c1-124">This member must be one of the following values.</span></span>



| <span data-ttu-id="392c1-125">值</span><span class="sxs-lookup"><span data-stu-id="392c1-125">Value</span></span> | <span data-ttu-id="392c1-126">描述</span><span class="sxs-lookup"><span data-stu-id="392c1-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="392c1-127">1</span><span class="sxs-lookup"><span data-stu-id="392c1-127">1</span></span>     | <span data-ttu-id="392c1-128">點陣圖為單色，bmiColors 成員包含兩個專案。</span><span class="sxs-lookup"><span data-stu-id="392c1-128">The bitmap is monochrome, and the bmiColors member contains two entries.</span></span> <span data-ttu-id="392c1-129">點陣圖陣列中的每個位都代表一個圖元。</span><span class="sxs-lookup"><span data-stu-id="392c1-129">Each bit in the bitmap array represents a pixel.</span></span> <span data-ttu-id="392c1-130">如果位為 clear，圖元就會顯示為 bmiColors 資料表中第一個專案的色彩;如果設定位，圖元就會有資料表中第二個專案的色彩。</span><span class="sxs-lookup"><span data-stu-id="392c1-130">If the bit is clear, the pixel is displayed with the color of the first entry in the bmiColors table; if the bit is set, the pixel has the color of the second entry in the table.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="392c1-131">2</span><span class="sxs-lookup"><span data-stu-id="392c1-131">2</span></span>     | <span data-ttu-id="392c1-132">點陣圖有四個可能的色彩值。</span><span class="sxs-lookup"><span data-stu-id="392c1-132">The bitmap has four possible color values.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="392c1-133">4</span><span class="sxs-lookup"><span data-stu-id="392c1-133">4</span></span>     | <span data-ttu-id="392c1-134">點陣圖最多可有16個色彩，而 bmiColors 成員最多包含16個專案。</span><span class="sxs-lookup"><span data-stu-id="392c1-134">The bitmap has a maximum of 16 colors, and the bmiColors member contains up to 16 entries.</span></span> <span data-ttu-id="392c1-135">點陣圖中的每個圖元都會以4位索引表示在色彩資料表中。</span><span class="sxs-lookup"><span data-stu-id="392c1-135">Each pixel in the bitmap is represented by a 4-bit index into the color table.</span></span> <span data-ttu-id="392c1-136">例如，如果點陣圖中的第一個位元組是0x1F，則位元組代表兩個圖元。</span><span class="sxs-lookup"><span data-stu-id="392c1-136">For example, if the first byte in the bitmap is 0x1F, the byte represents two pixels.</span></span> <span data-ttu-id="392c1-137">第一個圖元包含第二個數據表專案中的色彩，而第二個圖元包含第十六個數據表專案中的色彩。</span><span class="sxs-lookup"><span data-stu-id="392c1-137">The first pixel contains the color in the second table entry, and the second pixel contains the color in the sixteenth table entry.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="392c1-138">8</span><span class="sxs-lookup"><span data-stu-id="392c1-138">8</span></span>     | <span data-ttu-id="392c1-139">點陣圖的最大值為256，而 bmiColors 成員最多包含256個專案。</span><span class="sxs-lookup"><span data-stu-id="392c1-139">The bitmap has a maximum of 256 colors, and the bmiColors member contains up to 256 entries.</span></span> <span data-ttu-id="392c1-140">在此情況下，陣列中的每個位元組都代表一個圖元。</span><span class="sxs-lookup"><span data-stu-id="392c1-140">In this case, each byte in the array represents a single pixel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="392c1-141">16</span><span class="sxs-lookup"><span data-stu-id="392c1-141">16</span></span>    | <span data-ttu-id="392c1-142">點陣圖的最大值為 2 ^ 16 色。</span><span class="sxs-lookup"><span data-stu-id="392c1-142">The bitmap has a maximum of 2^16 colors.</span></span> <span data-ttu-id="392c1-143">如果 BITMAPINFOHEADER 的 biCompression 成員是 BI \_ RGB，則 bmiColors 成員為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="392c1-143">If the biCompression member of the BITMAPINFOHEADER is BI\_RGB, the bmiColors member is **NULL**.</span></span> <span data-ttu-id="392c1-144">點陣圖陣列中的每個單字都代表一個圖元。</span><span class="sxs-lookup"><span data-stu-id="392c1-144">Each WORD in the bitmap array represents a single pixel.</span></span> <span data-ttu-id="392c1-145">紅色、綠色和藍色的相對濃度會以每個色彩元件的5位表示。</span><span class="sxs-lookup"><span data-stu-id="392c1-145">The relative intensities of red, green, and blue are represented with 5 bits for each color component.</span></span> <span data-ttu-id="392c1-146">藍色的值是最不重要的5位，後面接著每個綠色和紅色的5位。</span><span class="sxs-lookup"><span data-stu-id="392c1-146">The value for blue is in the least significant 5 bits, followed by 5 bits each for green and red.</span></span> <span data-ttu-id="392c1-147">不會使用最重要的位。</span><span class="sxs-lookup"><span data-stu-id="392c1-147">The most significant bit is not used.</span></span> <span data-ttu-id="392c1-148">BmiColors 色彩表可用來優化以調色板為基礎的裝置上使用的色彩，而且必須包含 biClrUsed 成員所指定的專案數。</span><span class="sxs-lookup"><span data-stu-id="392c1-148">The bmiColors color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the biClrUsed member.</span></span> |
| <span data-ttu-id="392c1-149">24</span><span class="sxs-lookup"><span data-stu-id="392c1-149">24</span></span>    | <span data-ttu-id="392c1-150">點陣圖最多可有 2 ^ 24 個色彩，而 bmiColors 成員為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="392c1-150">The bitmap has a maximum of 2^24 colors, and the bmiColors member is **NULL**.</span></span> <span data-ttu-id="392c1-151">點陣圖陣列中的每個三位元組三位元組分別代表一個圖元的藍色、綠色和紅色的相對濃度。</span><span class="sxs-lookup"><span data-stu-id="392c1-151">Each 3-byte triplet in the bitmap array represents the relative intensities of blue, green, and red, respectively, for a pixel.</span></span> <span data-ttu-id="392c1-152">BmiColors 色彩表可用來優化以調色板為基礎的裝置上使用的色彩，而且必須包含 biClrUsed 成員所指定的專案數。</span><span class="sxs-lookup"><span data-stu-id="392c1-152">The bmiColors color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the biClrUsed member.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="392c1-153">32</span><span class="sxs-lookup"><span data-stu-id="392c1-153">32</span></span>    | <span data-ttu-id="392c1-154">點陣圖最多有 2 ^ 32 個色彩。</span><span class="sxs-lookup"><span data-stu-id="392c1-154">The bitmap has a maximum of 2^32 colors.</span></span> <span data-ttu-id="392c1-155">如果 biCompression 成員是 BI \_ RGB，bmiColors 成員就會是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="392c1-155">If the biCompression member is BI\_RGB, the bmiColors member is **NULL**.</span></span> <span data-ttu-id="392c1-156">點陣圖陣列中的每個 DWORD 分別代表藍色、綠色和紅色的相對濃度（圖元）。</span><span class="sxs-lookup"><span data-stu-id="392c1-156">Each DWORD in the bitmap array represents the relative intensities of blue, green, and red, respectively, for a pixel.</span></span> <span data-ttu-id="392c1-157">不會使用每個 DWORD 的最高位元組。</span><span class="sxs-lookup"><span data-stu-id="392c1-157">The high byte in each DWORD is not used.</span></span> <span data-ttu-id="392c1-158">BmiColors 色彩表可用來優化以調色板為基礎的裝置上使用的色彩，而且必須包含 biClrUsed 成員所指定的專案數。</span><span class="sxs-lookup"><span data-stu-id="392c1-158">The bmiColors color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the biClrUsed member.</span></span>                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="392c1-159">**biCompression**</span><span class="sxs-lookup"><span data-stu-id="392c1-159">**biCompression**</span></span>
</dt> <dd>

<span data-ttu-id="392c1-160">指定壓縮的下點陣圖壓縮類型 (由上而下的 Dib 無法壓縮) 。</span><span class="sxs-lookup"><span data-stu-id="392c1-160">Specifies the type of compression for a compressed bottom-up bitmap (top-down DIBs cannot be compressed).</span></span> <span data-ttu-id="392c1-161">這個成員可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="392c1-161">This member can be the one of the following values.</span></span>



| <span data-ttu-id="392c1-162">值</span><span class="sxs-lookup"><span data-stu-id="392c1-162">Value</span></span>         | <span data-ttu-id="392c1-163">描述</span><span class="sxs-lookup"><span data-stu-id="392c1-163">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="392c1-164">BI \_ RGB</span><span class="sxs-lookup"><span data-stu-id="392c1-164">BI\_RGB</span></span>       | <span data-ttu-id="392c1-165">未壓縮的格式。</span><span class="sxs-lookup"><span data-stu-id="392c1-165">An uncompressed format.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="392c1-166">BI \_ 位欄位</span><span class="sxs-lookup"><span data-stu-id="392c1-166">BI\_BITFIELDS</span></span> | <span data-ttu-id="392c1-167">指定不壓縮點陣圖，而色彩表包含三個 DWORD 色遮罩，分別指定每個圖元的紅色、綠色和藍色元件。</span><span class="sxs-lookup"><span data-stu-id="392c1-167">Specifies that the bitmap is not compressed and that the color table consists of three DWORD color masks that specify the red, green, and blue components, respectively, of each pixel.</span></span> <span data-ttu-id="392c1-168">這在搭配使用 16 bpp 和 32-bpp 點陣圖時有效。</span><span class="sxs-lookup"><span data-stu-id="392c1-168">This is valid when used with 16-bpp and 32-bpp bitmaps.</span></span> <span data-ttu-id="392c1-169">在 Microsoft Windows CE 2.0 版和更新版本中，此值是有效的。</span><span class="sxs-lookup"><span data-stu-id="392c1-169">This value is valid in Microsoft Windows CE version 2.0 and later.</span></span> |



 

</dd> <dt>

<span data-ttu-id="392c1-170">**biSizeImage**</span><span class="sxs-lookup"><span data-stu-id="392c1-170">**biSizeImage**</span></span>
</dt> <dd>

<span data-ttu-id="392c1-171">指定影像的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="392c1-171">Specifies the size of the image, in bytes.</span></span> <span data-ttu-id="392c1-172">對於 BI RGB 點陣圖，這可以設為零 \_ 。</span><span class="sxs-lookup"><span data-stu-id="392c1-172">This may be set to zero for BI\_RGB bitmaps.</span></span>

</dd> <dt>

<span data-ttu-id="392c1-173">**biXPelsPerMeter**</span><span class="sxs-lookup"><span data-stu-id="392c1-173">**biXPelsPerMeter**</span></span>
</dt> <dd>

<span data-ttu-id="392c1-174">指定點陣圖目標裝置的水準解析度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="392c1-174">Specifies the horizontal resolution, in pixels per meter, of the target device for the bitmap.</span></span> <span data-ttu-id="392c1-175">應用程式可以使用此值從最符合目前裝置特性的資源群組中選取點陣圖。</span><span class="sxs-lookup"><span data-stu-id="392c1-175">An application can use this value to select a bitmap from a resource group that best matches the characteristics of the current device.</span></span>

</dd> <dt>

<span data-ttu-id="392c1-176">**biYPelsPerMeter**</span><span class="sxs-lookup"><span data-stu-id="392c1-176">**biYPelsPerMeter**</span></span>
</dt> <dd>

<span data-ttu-id="392c1-177">為點陣圖的目標裝置指定垂直解析度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="392c1-177">Specifies the vertical resolution, in pixels per meter, of the target device for the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="392c1-178">**biClrUsed**</span><span class="sxs-lookup"><span data-stu-id="392c1-178">**biClrUsed**</span></span>
</dt> <dd>

<span data-ttu-id="392c1-179">指定點陣圖實際使用之色彩表中的色彩索引數目。</span><span class="sxs-lookup"><span data-stu-id="392c1-179">Specifies the number of color indexes in the color table that are actually used by the bitmap.</span></span> <span data-ttu-id="392c1-180">如果這個值為零，則點陣圖會使用與 **biCompression** 所指定之壓縮模式的 **biBitCount** 成員值相對應的最大色彩數目。</span><span class="sxs-lookup"><span data-stu-id="392c1-180">If this value is zero, the bitmap uses the maximum number of colors corresponding to the value of the **biBitCount** member for the compression mode specified by **biCompression**.</span></span>

</dd> <dt>

<span data-ttu-id="392c1-181">**biClrImportant**</span><span class="sxs-lookup"><span data-stu-id="392c1-181">**biClrImportant**</span></span>
</dt> <dd>

<span data-ttu-id="392c1-182">指定顯示點陣圖所需的色彩索引數目。</span><span class="sxs-lookup"><span data-stu-id="392c1-182">Specifies the number of color indexes required for displaying the bitmap.</span></span> <span data-ttu-id="392c1-183">如果此值為零，則需要所有色彩。</span><span class="sxs-lookup"><span data-stu-id="392c1-183">If this value is zero, all colors are required.</span></span>

<span data-ttu-id="392c1-184">如果 biClrUsed 為非零值，且 biBitCount 成員小於16，則 biClrUsed 成員會指定圖形引擎或設備磁碟機所存取的實際色彩數目。</span><span class="sxs-lookup"><span data-stu-id="392c1-184">If biClrUsed is nonzero and the biBitCount member is less than 16, the biClrUsed member specifies the actual number of colors the graphics engine or device driver accesses.</span></span> <span data-ttu-id="392c1-185">如果 biBitCount 為16或更大，biClrUsed 成員會指定色彩表的大小，用來將系統調色板的效能優化。</span><span class="sxs-lookup"><span data-stu-id="392c1-185">If biBitCount is 16 or greater, the biClrUsed member specifies the size of the color table used to optimize performance of the system color palettes.</span></span> <span data-ttu-id="392c1-186">如果 biBitCount 等於16或32，最佳色彩選擇區會緊接在三個 DWORD 遮罩之後開始。</span><span class="sxs-lookup"><span data-stu-id="392c1-186">If biBitCount equals 16 or 32, the optimal color palette starts immediately following the three DWORD masks.</span></span>

<span data-ttu-id="392c1-187">如果點陣圖是封裝點陣圖 (點陣圖陣列會緊接在 \_ BITMAPINFOHEADER 結構之後，且由單一指標) 參考，則 biClrUsed 成員必須是零或色彩表的實際大小。</span><span class="sxs-lookup"><span data-stu-id="392c1-187">If the bitmap is a packed bitmap (a bitmap in which the bitmap array immediately follows the \_BITMAPINFOHEADER structure and is referenced by a single pointer), the biClrUsed member must be either zero or the actual size of the color table.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="392c1-188">備註</span><span class="sxs-lookup"><span data-stu-id="392c1-188">Remarks</span></span>

<span data-ttu-id="392c1-189">此結構包含在 **\_ VIDEOINFOHEADER** 結構中。</span><span class="sxs-lookup"><span data-stu-id="392c1-189">This structure is contained within a **\_VIDEOINFOHEADER** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="392c1-190">規格需求</span><span class="sxs-lookup"><span data-stu-id="392c1-190">Requirements</span></span>



| <span data-ttu-id="392c1-191">需求</span><span class="sxs-lookup"><span data-stu-id="392c1-191">Requirement</span></span> | <span data-ttu-id="392c1-192">值</span><span class="sxs-lookup"><span data-stu-id="392c1-192">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="392c1-193">標頭</span><span class="sxs-lookup"><span data-stu-id="392c1-193">Header</span></span><br/> | <dl> <span data-ttu-id="392c1-194"><dt>Wmdm .idl</dt></span><span class="sxs-lookup"><span data-stu-id="392c1-194"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="392c1-195">另請參閱</span><span class="sxs-lookup"><span data-stu-id="392c1-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="392c1-196">**結構**</span><span class="sxs-lookup"><span data-stu-id="392c1-196">**Structures**</span></span>](structures.md)
</dt> <dt>

[<span data-ttu-id="392c1-197">**\_VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="392c1-197">**\_VIDEOINFOHEADER**</span></span>](-videoinfoheader.md)
</dt> </dl>

 

 





