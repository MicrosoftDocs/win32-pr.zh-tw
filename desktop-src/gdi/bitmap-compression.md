---
description: Windows 支援將點陣圖壓縮的格式，以每圖元8或4個位來定義色彩。 壓縮會減少點陣圖所需的磁片和記憶體儲存體。
ms.assetid: 14d14662-910a-4f3f-914e-6ccfc602c822
title: 點陣圖壓縮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38739f0e33f095b8eff567fc63b57db96b8cdc66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114737"
---
# <a name="bitmap-compression"></a><span data-ttu-id="d6125-104">點陣圖壓縮</span><span class="sxs-lookup"><span data-stu-id="d6125-104">Bitmap Compression</span></span>

<span data-ttu-id="d6125-105">Windows 支援將點陣圖壓縮的格式，以每圖元8或4個位來定義色彩。</span><span class="sxs-lookup"><span data-stu-id="d6125-105">Windows supports formats for compressing bitmaps that define their colors with 8 or 4 bits-per-pixel.</span></span> <span data-ttu-id="d6125-106">壓縮會減少點陣圖所需的磁片和記憶體儲存體。</span><span class="sxs-lookup"><span data-stu-id="d6125-106">Compression reduces the disk and memory storage required for the bitmap.</span></span>

<span data-ttu-id="d6125-107">當點陣圖資訊標頭結構的 **壓縮** 成員是 BI \_ RLE8 時，會使用 (RLE) 格式的執行長度編碼來壓縮8位點陣圖。</span><span class="sxs-lookup"><span data-stu-id="d6125-107">When the **Compression** member of the bitmap information header structure is BI\_RLE8, a run-length encoding (RLE) format is used to compress an 8-bit bitmap.</span></span> <span data-ttu-id="d6125-108">這種格式可以用編碼或絕對模式壓縮。</span><span class="sxs-lookup"><span data-stu-id="d6125-108">This format can be compressed in encoded or absolute modes.</span></span> <span data-ttu-id="d6125-109">這兩種模式都可以出現在相同點陣圖中的任何位置：</span><span class="sxs-lookup"><span data-stu-id="d6125-109">Both modes can occur anywhere in the same bitmap:</span></span>

-   <span data-ttu-id="d6125-110">*編碼模式* 包含兩個位元組：第一個位元組指定使用第二個位元組中包含的色彩索引來繪製的連續圖元數。</span><span class="sxs-lookup"><span data-stu-id="d6125-110">*Encoded mode* consists of two bytes: the first byte specifies the number of consecutive pixels to be drawn using the color index contained in the second byte.</span></span> <span data-ttu-id="d6125-111">此外，配對的第一個位元組可以設定為零，表示表示行尾、點陣圖結尾或 delta 的 escape 字元（視第二個位元組的值而定）。</span><span class="sxs-lookup"><span data-stu-id="d6125-111">In addition, the first byte of the pair can be set to zero to indicate an escape character that denotes the end of a line, the end of a bitmap, or a delta, depending on the value of the second byte.</span></span> <span data-ttu-id="d6125-112">Escape 的解讀取決於配對的第二個位元組值，它可以是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="d6125-112">The interpretation of the escape depends on the value of the second byte of the pair, which can be one of the following values.</span></span>



| <span data-ttu-id="d6125-113">值</span><span class="sxs-lookup"><span data-stu-id="d6125-113">Value</span></span> | <span data-ttu-id="d6125-114">意義</span><span class="sxs-lookup"><span data-stu-id="d6125-114">Meaning</span></span>                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6125-115">0</span><span class="sxs-lookup"><span data-stu-id="d6125-115">0</span></span>     | <span data-ttu-id="d6125-116">行結尾。</span><span class="sxs-lookup"><span data-stu-id="d6125-116">End of line.</span></span>                                                                                                                                                |
| <span data-ttu-id="d6125-117">1</span><span class="sxs-lookup"><span data-stu-id="d6125-117">1</span></span>     | <span data-ttu-id="d6125-118">點陣圖結尾。</span><span class="sxs-lookup"><span data-stu-id="d6125-118">End of bitmap.</span></span>                                                                                                                                              |
| <span data-ttu-id="d6125-119">2</span><span class="sxs-lookup"><span data-stu-id="d6125-119">2</span></span>     | <span data-ttu-id="d6125-120">三角洲。</span><span class="sxs-lookup"><span data-stu-id="d6125-120">Delta.</span></span> <span data-ttu-id="d6125-121">在 escape 之後的2個位元組包含不帶正負號的值，指出下一個圖元與目前位置的水準和垂直位移。</span><span class="sxs-lookup"><span data-stu-id="d6125-121">The 2 bytes following the escape contain unsigned values indicating the horizontal and vertical offsets of the next pixel from the current position.</span></span> |



 

-   <span data-ttu-id="d6125-122">在 *絕對模式* 中，第一個位元組為零，而第二個位元組是範圍03H 到 FFH 的值。</span><span class="sxs-lookup"><span data-stu-id="d6125-122">In *absolute mode*, the first byte is zero and the second byte is a value in the range 03H through FFH.</span></span> <span data-ttu-id="d6125-123">第二個位元組代表後面的位元組數目，每個位元組都包含單一圖元的色彩索引。</span><span class="sxs-lookup"><span data-stu-id="d6125-123">The second byte represents the number of bytes that follow, each of which contains the color index of a single pixel.</span></span> <span data-ttu-id="d6125-124">當第二個位元組為兩個或更少時，表示 escape 的意義與編碼模式相同。</span><span class="sxs-lookup"><span data-stu-id="d6125-124">When the second byte is two or less, the escape has the same meaning as encoded mode.</span></span> <span data-ttu-id="d6125-125">在絕對模式中，每次執行都必須對齊字邊界。</span><span class="sxs-lookup"><span data-stu-id="d6125-125">In absolute mode, each run must be aligned on a word boundary.</span></span>

<span data-ttu-id="d6125-126">下列範例會顯示8位壓縮點陣圖的十六進位值：</span><span class="sxs-lookup"><span data-stu-id="d6125-126">The following example shows the hexadecimal values of an 8-bit compressed bitmap:</span></span>


```C++
[03 04] [05 06] [00 03 45 56 67] [02 78] [00 02 05 01] 
[02 78] [00 00] [09 1E] [00 01] 
```



<span data-ttu-id="d6125-127">點陣圖會依下列方式展開 (兩位數值代表單一圖元) 的色彩索引：</span><span class="sxs-lookup"><span data-stu-id="d6125-127">The bitmap expands as follows (two-digit values represent a color index for a single pixel):</span></span>


```C++
04 04 04 
06 06 06 06 06 
45 56 67 
78 78 
move current position 5 right and 1 down 
78 78 
end of line 
1E 1E 1E 1E 1E 1E 1E 1E 1E 
end of RLE bitmap 
```



<span data-ttu-id="d6125-128">當 **壓縮** 成員是 BI \_ RLE4 時，會使用4位點陣圖的執行長度編碼格式來壓縮點陣圖，這也會使用編碼和絕對模式：</span><span class="sxs-lookup"><span data-stu-id="d6125-128">When the **Compression** member is BI\_RLE4, the bitmap is compressed by using a run-length encoding format for a 4-bit bitmap, which also uses encoded and absolute modes:</span></span>

-   <span data-ttu-id="d6125-129">在編碼模式中，配對的第一個位元組會包含要使用第二個位元組中的色彩索引繪製的圖元數。</span><span class="sxs-lookup"><span data-stu-id="d6125-129">In encoded mode, the first byte of the pair contains the number of pixels to be drawn using the color indexes in the second byte.</span></span> <span data-ttu-id="d6125-130">第二個位元組包含兩個色彩索引，一個在其高序位4位，另一個則為低序位4位。</span><span class="sxs-lookup"><span data-stu-id="d6125-130">The second byte contains two color indexes, one in its high-order 4 bits and one in its low-order 4 bits.</span></span> <span data-ttu-id="d6125-131">第一個圖元是使用由高序位4位所指定的色彩來繪製，第二個是使用低序位4位中的色彩繪製，第三個則是使用高序位4位中的色彩來繪製，依此類推，直到第一個位元組指定的所有圖元都已繪製為止。</span><span class="sxs-lookup"><span data-stu-id="d6125-131">The first of the pixels is drawn using the color specified by the high-order 4 bits, the second is drawn using the color in the low-order 4 bits, the third is drawn using the color in the high-order 4 bits, and so on, until all the pixels specified by the first byte have been drawn.</span></span>
-   <span data-ttu-id="d6125-132">在絕對模式中，第一個位元組是零。</span><span class="sxs-lookup"><span data-stu-id="d6125-132">In absolute mode, the first byte is zero.</span></span> <span data-ttu-id="d6125-133">第二個位元組包含後面的色彩索引數目。</span><span class="sxs-lookup"><span data-stu-id="d6125-133">The second byte contains the number of color indexes that follow.</span></span> <span data-ttu-id="d6125-134">後續的位元組包含其高和低序位4位的色彩索引，每個圖元一個色彩索引。</span><span class="sxs-lookup"><span data-stu-id="d6125-134">Subsequent bytes contain color indexes in their high- and low-order 4 bits, one color index for each pixel.</span></span> <span data-ttu-id="d6125-135">在絕對模式中，每次執行都必須對齊字邊界。</span><span class="sxs-lookup"><span data-stu-id="d6125-135">In absolute mode, each run must be aligned on a word boundary.</span></span> <span data-ttu-id="d6125-136">BI RLE8 說明的行結尾、點陣圖結尾和 delta esc \_ 也適用于 bi \_ RLE4 壓縮。</span><span class="sxs-lookup"><span data-stu-id="d6125-136">The end-of-line, end-of-bitmap, and delta escapes described for BI\_RLE8 also apply to BI\_RLE4 compression.</span></span>

<span data-ttu-id="d6125-137">下列範例顯示4位壓縮點陣圖的十六進位值：</span><span class="sxs-lookup"><span data-stu-id="d6125-137">The following example shows the hexadecimal values of a 4-bit compressed bitmap:</span></span>


```C++
03 04 05 06 00 06 45 56 67 00 04 78 00 02 05 01 
04 78 00 00 09 1E 00 01 
```



<span data-ttu-id="d6125-138">點陣圖會依下列方式展開 (單一位數值代表單一圖元) 的色彩索引：</span><span class="sxs-lookup"><span data-stu-id="d6125-138">The bitmap expands as follows (single-digit values represent a color index for a single pixel):</span></span>


```C++
0 4 0 
0 6 0 6 0 
4 5 5 6 6 7 
7 8 7 8 
move current position 5 right and 1 down 
7 8 7 8 
end of line 
1 E 1 E 1 E 1 E 1 
end of RLE bitmap 
```



 

 



