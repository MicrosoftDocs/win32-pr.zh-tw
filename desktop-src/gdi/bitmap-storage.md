---
description: 點陣圖應儲存在使用已建立點陣圖檔案格式的檔案中，並指派具有三個字元 .bmp 副檔名的名稱。
ms.assetid: 44f19d14-4e0e-4512-8c86-6bd34ca4e87b
title: 點陣圖儲存體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28046f6d78f5137d0dfc5b1396bbf76be318daa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114729"
---
# <a name="bitmap-storage"></a><span data-ttu-id="5bd02-103">點陣圖儲存體</span><span class="sxs-lookup"><span data-stu-id="5bd02-103">Bitmap Storage</span></span>

<span data-ttu-id="5bd02-104">點陣圖應儲存在使用已建立點陣圖檔案格式的檔案中，並指派具有三個字元 .bmp 副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="5bd02-104">Bitmaps should be saved in a file that uses the established bitmap file format and assigned a name with the three-character .bmp extension.</span></span> <span data-ttu-id="5bd02-105">所建立的點陣圖檔案格式包含 [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) 結構，後面接著 [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))、 [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)或 [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) 結構。</span><span class="sxs-lookup"><span data-stu-id="5bd02-105">The established bitmap file format consists of a [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) structure followed by a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header), or [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) structure.</span></span> <span data-ttu-id="5bd02-106">[**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)結構的陣列 (也稱為色彩資料表) 遵循點陣圖資訊標頭結構。</span><span class="sxs-lookup"><span data-stu-id="5bd02-106">An array of [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structures (also called a color table) follows the bitmap information header structure.</span></span> <span data-ttu-id="5bd02-107">色彩表後面接著第二個索引陣列， (實際的點陣圖資料) 。</span><span class="sxs-lookup"><span data-stu-id="5bd02-107">The color table is followed by a second array of indexes into the color table (the actual bitmap data).</span></span>

<span data-ttu-id="5bd02-108">點陣圖檔案格式如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="5bd02-108">The bitmap file format is shown in the following illustration.</span></span>

![點陣圖檔案格式的圖表，其中顯示 bitmapfileheader、bitmapinfoheader、rgbquad 陣列和色彩索引陣列](images/csbmp-02.png)

<span data-ttu-id="5bd02-110">[**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader)結構的成員會識別檔案;指定檔案的大小（以位元組為單位）。並指定從標頭中第一個位元組到點陣圖資料之第一個位元組的位移。</span><span class="sxs-lookup"><span data-stu-id="5bd02-110">The members of the [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) structure identify the file; specify the size of the file, in bytes; and specify the offset from the first byte in the header to the first byte of bitmap data.</span></span> <span data-ttu-id="5bd02-111">[**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))、 [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)或 [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header)結構的成員會指定點陣圖的寬度和高度（以圖元為單位）。色彩格式 (色彩平面的計數和點陣圖建立所在之顯示裝置的每圖元色彩位) ;點陣圖資料是否在儲存體之前壓縮，以及使用的壓縮類型;點陣圖資料的位元組數目;點陣圖建立所在之顯示裝置的解析度;以及資料中表示的色彩數目。</span><span class="sxs-lookup"><span data-stu-id="5bd02-111">The members of the [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header), or [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) structure specify the width and height of the bitmap, in pixels; the color format (count of color planes and color bits-per-pixel) of the display device on which the bitmap was created; whether the bitmap data was compressed before storage and the type of compression used; the number of bytes of bitmap data; the resolution of the display device on which the bitmap was created; and the number of colors represented in the data.</span></span> <span data-ttu-id="5bd02-112">[**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)結構會針對裝置的調色板中的每個色彩指定 RGB 濃度值。</span><span class="sxs-lookup"><span data-stu-id="5bd02-112">The [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structures specify the RGB intensity values for each of the colors in the device's palette.</span></span>

<span data-ttu-id="5bd02-113">色彩索引陣列會將一種色彩（以索引的形式）與 [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) 結構建立關聯，並將每個圖元以點陣圖表示。</span><span class="sxs-lookup"><span data-stu-id="5bd02-113">The color-index array associates a color, in the form of an index to an [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure, with each pixel in a bitmap.</span></span> <span data-ttu-id="5bd02-114">因此，色彩索引陣列中的位數會等於為 **RGBQUAD** 結構編制索引所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="5bd02-114">Thus, the number of bits in the color-index array equals the number of pixels times the number of bits needed to index the **RGBQUAD** structures.</span></span> <span data-ttu-id="5bd02-115">例如，8x8 的黑色和白色點陣圖具有 8 \* 8 \* 1 = 64 位的色彩索引陣列，因為有一位需要用來為兩個色彩編制索引。</span><span class="sxs-lookup"><span data-stu-id="5bd02-115">For example, an 8x8 black-and-white bitmap has a color-index array of 8 \* 8 \* 1 = 64 bits, because one bit is needed to index two colors.</span></span> <span data-ttu-id="5bd02-116">「 [關於點陣圖](about-bitmaps.md)」中提及的 Redbrick.bmp 是具有16色的32x32 點陣圖;其色彩索引陣列為 32 \* 32 \* 4 = 4096 位，因為四個位索引16色。</span><span class="sxs-lookup"><span data-stu-id="5bd02-116">The Redbrick.bmp, mentioned in [About Bitmaps](about-bitmaps.md), is a 32x32 bitmap with 16 colors; its color-index array is 32 \* 32 \* 4 = 4096 bits because four bits index 16 colors.</span></span>

<span data-ttu-id="5bd02-117">若要建立由上而下點陣圖的色彩索引陣列，請從點陣圖的頂端行開始。</span><span class="sxs-lookup"><span data-stu-id="5bd02-117">To create a color-index array for a top-down bitmap, start at the top line in the bitmap.</span></span> <span data-ttu-id="5bd02-118">最左邊圖元之色彩的 [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) 索引是以色彩索引陣列 (的第一個 *n* 位，其中 *n* 是指出所有 **RGBQUAD** 結構) 所需的位數。</span><span class="sxs-lookup"><span data-stu-id="5bd02-118">The index of the [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) for the color of the left-most pixel is the first *n* bits in the color-index array (where *n* is the number of bits needed to indicate all of the **RGBQUAD** structures).</span></span> <span data-ttu-id="5bd02-119">右邊的下一個圖元色彩是陣列中的下一個 *n* 位，依此類推。</span><span class="sxs-lookup"><span data-stu-id="5bd02-119">The color of the next pixel to the right is the next *n* bits in the array, and so forth.</span></span> <span data-ttu-id="5bd02-120">當您到達行中最右邊的圖元之後，請繼續下一行中最左邊的圖元。</span><span class="sxs-lookup"><span data-stu-id="5bd02-120">After you reach the right-most pixel in the line, continue with the left-most pixel in the line below.</span></span> <span data-ttu-id="5bd02-121">繼續進行，直到完成整個點陣圖為止。</span><span class="sxs-lookup"><span data-stu-id="5bd02-121">Continue until you finish with the entire bitmap.</span></span> <span data-ttu-id="5bd02-122">如果是自下而上的點陣圖，請從點陣圖底部的位置開始，而不是從上一行開始，從左至右，然後繼續前往點陣圖的頂端行。</span><span class="sxs-lookup"><span data-stu-id="5bd02-122">If it is a bottom-up bitmap, start at the bottom line of the bitmap instead of the top line, still going from left to right, and continue to the top line of the bitmap.</span></span>

<span data-ttu-id="5bd02-123">下列十六進位輸出顯示 Redbrick.bmp 檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="5bd02-123">The following hexadecimal output shows the contents of the file Redbrick.bmp.</span></span>


```C++
0000    42 4d 76 02 00 00 00 00  00 00 76 00 00 00 28 00 
0010    00 00 20 00 00 00 20 00  00 00 01 00 04 00 00 00 
0020    00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00 
0030    00 00 00 00 00 00 00 00  00 00 00 00 80 00 00 80 
0040    00 00 00 80 80 00 80 00  00 00 80 00 80 00 80 80 
0050    00 00 80 80 80 00 c0 c0  c0 00 00 00 ff 00 00 ff 
0060    00 00 00 ff ff 00 ff 00  00 00 ff 00 ff 00 ff ff 
0070    00 00 ff ff ff 00 00 00  00 00 00 00 00 00 00 00 
0080    00 00 00 00 00 00 00 00  00 00 00 00 00 00 09 00 
0090    00 00 00 00 00 00 11 11  01 19 11 01 10 10 09 09 
00a0    01 09 11 11 01 90 11 01  19 09 09 91 11 10 09 11 
00b0    09 11 19 10 90 11 19 01  19 19 10 10 11 10 09 01 
00c0    91 10 91 09 10 10 90 99  11 11 11 11 19 00 09 01 
00d0    91 01 01 19 00 99 11 10  11 91 99 11 09 90 09 91 
00e0    01 11 11 11 91 10 09 19  01 00 11 90 91 10 09 01 
00f0    11 99 10 01 11 11 91 11  11 19 10 11 99 10 09 10 
0100    01 11 11 11 19 10 11 09  09 10 19 10 10 10 09 01 
0110    11 19 00 01 10 19 10 11  11 01 99 01 11 90 09 19 
0120    11 91 11 91 01 11 19 10  99 00 01 19 09 10 09 19 
0130    10 91 11 01 11 11 91 01  91 19 11 00 99 90 09 01 
0140    01 99 19 01 91 10 19 91  91 09 11 99 11 10 09 91 
0150    11 10 11 91 99 10 90 11  01 11 11 19 11 90 09 11 
0160    00 19 10 11 01 11 99 99  99 99 99 99 99 99 09 99 
0170    99 99 99 99 99 99 00 00  00 00 00 00 00 00 00 00 
0180    00 00 00 00 00 00 90 00  00 00 00 00 00 00 00 00 
0190    00 00 00 00 00 00 99 11  11 11 19 10 19 19 11 09 
01a0    10 90 91 90 91 00 91 19  19 09 01 10 09 01 11 11 
01b0    91 11 11 11 10 00 91 11  01 19 10 11 10 01 01 11 
01c0    90 11 11 11 91 00 99 09  19 10 11 90 09 90 91 01 
01d0    19 09 91 11 01 00 90 10  19 11 00 11 11 00 10 11 
01e0    01 10 11 19 11 00 90 19  10 91 01 90 19 99 00 11 
01f0    91 01 11 01 91 00 99 09  09 01 10 11 91 01 10 91 
0200    99 11 10 90 91 00 91 11  00 10 11 01 10 19 19 09 
0210    10 00 99 01 01 00 91 01  19 91 19 91 11 09 10 11 
0220    00 91 00 10 90 00 99 01  11 10 09 10 10 19 09 01 
0230    91 90 11 09 11 00 90 99  11 11 11 90 19 01 19 01 
0240    91 01 01 19 09 00 91 10  11 91 99 09 09 90 11 91 
0250    01 19 11 11 91 00 91 19  01 00 11 00 91 10 11 01 
0260    11 11 10 01 11 00 99 99  99 99 99 99 99 99 99 99 
0270    99 99 99 99 99 90 
```



<span data-ttu-id="5bd02-124">下表顯示與點陣圖檔案中的結構相關聯的資料位元組。</span><span class="sxs-lookup"><span data-stu-id="5bd02-124">The following table shows the data bytes associated with the structures in a bitmap file.</span></span>



| <span data-ttu-id="5bd02-125">結構</span><span class="sxs-lookup"><span data-stu-id="5bd02-125">Structure</span></span>                                    | <span data-ttu-id="5bd02-126">對應的位元組</span><span class="sxs-lookup"><span data-stu-id="5bd02-126">Corresponding bytes</span></span> |
|----------------------------------------------|---------------------|
| [<span data-ttu-id="5bd02-127">**BITMAPFILEHEADER**</span><span class="sxs-lookup"><span data-stu-id="5bd02-127">**BITMAPFILEHEADER**</span></span>](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) | <span data-ttu-id="5bd02-128">0x00 0x0D</span><span class="sxs-lookup"><span data-stu-id="5bd02-128">0x00 0x0D</span></span>           |
| <span data-ttu-id="5bd02-129">[**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5bd02-129">[**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))</span></span> | <span data-ttu-id="5bd02-130">0x0E 0x35</span><span class="sxs-lookup"><span data-stu-id="5bd02-130">0x0E 0x35</span></span>           |
| <span data-ttu-id="5bd02-131">[**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) 陣列</span><span class="sxs-lookup"><span data-stu-id="5bd02-131">[**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) array</span></span>             | <span data-ttu-id="5bd02-132">0x36 0x75</span><span class="sxs-lookup"><span data-stu-id="5bd02-132">0x36 0x75</span></span>           |
| <span data-ttu-id="5bd02-133">色彩索引陣列</span><span class="sxs-lookup"><span data-stu-id="5bd02-133">Color-index array</span></span>                            | <span data-ttu-id="5bd02-134">0x76 0x275</span><span class="sxs-lookup"><span data-stu-id="5bd02-134">0x76 0x275</span></span>          |



 

 

 
