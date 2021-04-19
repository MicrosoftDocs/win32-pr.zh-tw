---
description: 使用16位 RGB
ms.assetid: 0a245187-4120-4003-9a8f-6b1e8fa40d38
title: 使用16位 RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6bf4b3217af4d0261d4ab26ca011881762a2a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985185"
---
# <a name="working-with-16-bit-rgb"></a><span data-ttu-id="e7cfe-103">使用16位 RGB</span><span class="sxs-lookup"><span data-stu-id="e7cfe-103">Working with 16-bit RGB</span></span>

<span data-ttu-id="e7cfe-104">針對16位未壓縮的 RGB 定義了兩種格式：</span><span class="sxs-lookup"><span data-stu-id="e7cfe-104">Two formats are defined for 16-bit uncompressed RGB:</span></span>

-   <span data-ttu-id="e7cfe-105">MEDIASUBTYPE \_ 555 會針對圖元中的紅色、綠色和藍色元件使用五個位。</span><span class="sxs-lookup"><span data-stu-id="e7cfe-105">MEDIASUBTYPE\_555 uses five bits each for the red, green, and blue components in a pixel.</span></span> <span data-ttu-id="e7cfe-106">**文字** 中最有效的位會被忽略。</span><span class="sxs-lookup"><span data-stu-id="e7cfe-106">The most significant bit in the **WORD** is ignored.</span></span>
-   <span data-ttu-id="e7cfe-107">MEDIASUBTYPE \_ 565 針對 red 和 blue 元件使用五個位，綠色元件則使用六位。</span><span class="sxs-lookup"><span data-stu-id="e7cfe-107">MEDIASUBTYPE\_565 uses five bits for the red and blue components, and six bits for the green component.</span></span> <span data-ttu-id="e7cfe-108">這種格式反映了人類願景對可見頻譜之綠色部分最敏感的事實。</span><span class="sxs-lookup"><span data-stu-id="e7cfe-108">This format reflects the fact that human vision is most sensitive to the green portions of the visible spectrum.</span></span>

<span data-ttu-id="e7cfe-109">**RGB 565**</span><span class="sxs-lookup"><span data-stu-id="e7cfe-109">**RGB 565**</span></span>

<span data-ttu-id="e7cfe-110">若要從 RGB 565 影像中將色彩元件解壓縮，請將每個圖元視為 **單字** 類型，並使用下列位元遮罩：</span><span class="sxs-lookup"><span data-stu-id="e7cfe-110">To extract the color components from an RGB 565 image, treat each pixel as a **WORD** type and use the following bit masks:</span></span>


```C++
WORD red_mask = 0xF800;
WORD green_mask = 0x7E0;
WORD blue_mask = 0x1F;
```



<span data-ttu-id="e7cfe-111">從圖元取得色彩元件，如下所示：</span><span class="sxs-lookup"><span data-stu-id="e7cfe-111">Get the color components from a pixel as follows:</span></span>


```C++
BYTE red_value = (pixel & red_mask) >> 11;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);
```



<span data-ttu-id="e7cfe-112">請記住，紅色和藍色通道是5位，而綠色通道為6位。</span><span class="sxs-lookup"><span data-stu-id="e7cfe-112">Remember that the red and blue channels are 5 bits and the green channel is 6 bits.</span></span> <span data-ttu-id="e7cfe-113">若要將這些值轉換為8位元件 (24 位或32位 RGB) ，您必須將適當的位數向左移位：</span><span class="sxs-lookup"><span data-stu-id="e7cfe-113">To convert these values to 8-bit components (for 24-bit or 32-bit RGB), you must left-shift the appropriate number of bits:</span></span>


```C++
// Expand to 8-bit values.
BYTE red   = red_value << 3;
BYTE green = green_value << 2;
BYTE blue  = blue_value << 3;
```



<span data-ttu-id="e7cfe-114">反轉此進程以建立 RGB 565 圖元。</span><span class="sxs-lookup"><span data-stu-id="e7cfe-114">Reverse this process to create an RGB 565 pixel.</span></span> <span data-ttu-id="e7cfe-115">假設色彩值已截斷為正確位數：</span><span class="sxs-lookup"><span data-stu-id="e7cfe-115">Assuming the color values have been truncated to the correct number of bits:</span></span>


```C++
WORD pixel565 = (red_value << 11) | (green_value << 5) | blue_value;
```



<span data-ttu-id="e7cfe-116">**RGB 555**</span><span class="sxs-lookup"><span data-stu-id="e7cfe-116">**RGB 555**</span></span>

<span data-ttu-id="e7cfe-117">使用 RGB 555 基本上與 RGB 565 相同，不同之處在于位元遮罩和位移位作業不同。</span><span class="sxs-lookup"><span data-stu-id="e7cfe-117">Working with RGB 555 is essentially the same as RGB 565, except the bit masks and bit shift operations are different.</span></span> <span data-ttu-id="e7cfe-118">若要從 RGB 555 圖元取得色彩元件，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="e7cfe-118">To get the color components from an RGB 555 pixel, do the following:</span></span>


```C++
WORD red_mask = 0x7C00;
WORD green_mask = 0x3E0;
WORD blue_mask = 0x1F;

BYTE red_value = (pixel & red_mask) >> 10;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);

// Expand to 8-bit values:
BYTE red   = red_value << 3;
BYTE green = green_value << 3;
BYTE blue  = blue_value << 3;
```



<span data-ttu-id="e7cfe-119">若要將紅色、綠色和藍色色彩值封裝成 RGB 555 圖元，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="e7cfe-119">To pack the red, green, and blue color values into an RGB 555 pixel, do the following:</span></span>


```C++
WORD pixel565 = (red << 10) | (green << 5) | blue;
```



## <a name="related-topics"></a><span data-ttu-id="e7cfe-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="e7cfe-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7cfe-121">未壓縮的 RGB 影片子類型</span><span class="sxs-lookup"><span data-stu-id="e7cfe-121">Uncompressed RGB Video Subtypes</span></span>](uncompressed-rgb-video-subtypes.md)
</dt> </dl>

 

 



