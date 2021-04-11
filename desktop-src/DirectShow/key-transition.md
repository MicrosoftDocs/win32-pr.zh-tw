---
description: 金鑰轉換
ms.assetid: 5d1ed2e4-82c2-4364-b8f0-22bba974bc22
title: 金鑰轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3e4f83bbe26f49989d612efe718c2d838ce7f1d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845975"
---
# <a name="key-transition"></a><span data-ttu-id="1a4ae-103">金鑰轉換</span><span class="sxs-lookup"><span data-stu-id="1a4ae-103">Key Transition</span></span>

> [!Note]  
> <span data-ttu-id="1a4ae-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="1a4ae-104">\[Deprecated.</span></span> <span data-ttu-id="1a4ae-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="1a4ae-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1a4ae-106">金鑰轉換會根據 RGB 值、Alpha 值、色調或亮度來執行加密。</span><span class="sxs-lookup"><span data-stu-id="1a4ae-106">The Key transition performs keying based on RGB value, alpha value, hue or luminance.</span></span>

<span data-ttu-id="1a4ae-107">下圖顯示金鑰轉換：</span><span class="sxs-lookup"><span data-stu-id="1a4ae-107">The following image shows the key transition:</span></span>

![金鑰轉換](images/trans-key.png)

<span data-ttu-id="1a4ae-109">類別識別碼 (CLSID) ： {C5B19592-145E-11D3-9F04-006008039E37}</span><span class="sxs-lookup"><span data-stu-id="1a4ae-109">Class ID (CLSID): {C5B19592-145E-11D3-9F04-006008039E37}</span></span>

<span data-ttu-id="1a4ae-110">CLSID 變數名稱： CLSID \_ DxtKey</span><span class="sxs-lookup"><span data-stu-id="1a4ae-110">CLSID Variable Name: CLSID\_DxtKey</span></span>

<span data-ttu-id="1a4ae-111">易記名稱： "DxtKey"</span><span class="sxs-lookup"><span data-stu-id="1a4ae-111">Friendly Name: "DxtKey"</span></span>

<span data-ttu-id="1a4ae-112">屬性</span><span class="sxs-lookup"><span data-stu-id="1a4ae-112">Properties</span></span>



| <span data-ttu-id="1a4ae-113">屬性</span><span class="sxs-lookup"><span data-stu-id="1a4ae-113">Property</span></span>   | <span data-ttu-id="1a4ae-114">類型</span><span class="sxs-lookup"><span data-stu-id="1a4ae-114">Type</span></span>  | <span data-ttu-id="1a4ae-115">有效範圍</span><span class="sxs-lookup"><span data-stu-id="1a4ae-115">Valid range</span></span>           | <span data-ttu-id="1a4ae-116">Description</span><span class="sxs-lookup"><span data-stu-id="1a4ae-116">Description</span></span>                                                                                                                                                                                                                                                | <span data-ttu-id="1a4ae-117">套用至</span><span class="sxs-lookup"><span data-stu-id="1a4ae-117">Applies To</span></span>                     |
|------------|-------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="1a4ae-118">色調</span><span class="sxs-lookup"><span data-stu-id="1a4ae-118">Hue</span></span>        | <span data-ttu-id="1a4ae-119">int</span><span class="sxs-lookup"><span data-stu-id="1a4ae-119">int</span></span>   | <span data-ttu-id="1a4ae-120">0-360</span><span class="sxs-lookup"><span data-stu-id="1a4ae-120">0–360</span></span>                 | <span data-ttu-id="1a4ae-121">要做為索引鍵的色調值。</span><span class="sxs-lookup"><span data-stu-id="1a4ae-121">The hue value on which to key.</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="1a4ae-122">色調</span><span class="sxs-lookup"><span data-stu-id="1a4ae-122">Hue</span></span>                            |
| <span data-ttu-id="1a4ae-123">Invert</span><span class="sxs-lookup"><span data-stu-id="1a4ae-123">Invert</span></span>     | <span data-ttu-id="1a4ae-124">BOOL</span><span class="sxs-lookup"><span data-stu-id="1a4ae-124">BOOL</span></span>  | <span data-ttu-id="1a4ae-125">**FALSE** 或 **TRUE**</span><span class="sxs-lookup"><span data-stu-id="1a4ae-125">**FALSE** or **TRUE**</span></span> | <span data-ttu-id="1a4ae-126">布林值，指出是否要反轉索引鍵的預設運算。</span><span class="sxs-lookup"><span data-stu-id="1a4ae-126">Boolean value indicating whether to invert the default operation of the key.</span></span> <span data-ttu-id="1a4ae-127">如果 **為 FALSE**，則會以預設方式將上層影像中的圖元變成透明。</span><span class="sxs-lookup"><span data-stu-id="1a4ae-127">If **FALSE**, pixels in the overlying image are made transparent in the default manner.</span></span> <span data-ttu-id="1a4ae-128">若 **為 TRUE**，則作業反轉。</span><span class="sxs-lookup"><span data-stu-id="1a4ae-128">If **TRUE**, the operation inverts.</span></span>                                                   | <span data-ttu-id="1a4ae-129">色度、色調、亮度、Nonred</span><span class="sxs-lookup"><span data-stu-id="1a4ae-129">Chroma, Hue, Luminance, Nonred</span></span> |
| <span data-ttu-id="1a4ae-130">KeyType</span><span class="sxs-lookup"><span data-stu-id="1a4ae-130">KeyType</span></span>    | <span data-ttu-id="1a4ae-131">int</span><span class="sxs-lookup"><span data-stu-id="1a4ae-131">int</span></span>   | <span data-ttu-id="1a4ae-132">請參閱備註</span><span class="sxs-lookup"><span data-stu-id="1a4ae-132">See Remarks</span></span>           | <span data-ttu-id="1a4ae-133">指定索引鍵的類型。</span><span class="sxs-lookup"><span data-stu-id="1a4ae-133">Specifies the type of key.</span></span> <span data-ttu-id="1a4ae-134">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="1a4ae-134">For more information, see Remarks.</span></span>                                                                                                                                                                                              | <span data-ttu-id="1a4ae-135">全部</span><span class="sxs-lookup"><span data-stu-id="1a4ae-135">All</span></span>                            |
| <span data-ttu-id="1a4ae-136">Luminance</span><span class="sxs-lookup"><span data-stu-id="1a4ae-136">Luminance</span></span>  | <span data-ttu-id="1a4ae-137">int</span><span class="sxs-lookup"><span data-stu-id="1a4ae-137">int</span></span>   | <span data-ttu-id="1a4ae-138">0–100</span><span class="sxs-lookup"><span data-stu-id="1a4ae-138">0–100</span></span>                 | <span data-ttu-id="1a4ae-139">要做為索引鍵的亮度值。</span><span class="sxs-lookup"><span data-stu-id="1a4ae-139">The luminance value on which to key.</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="1a4ae-140">Luminance</span><span class="sxs-lookup"><span data-stu-id="1a4ae-140">Luminance</span></span>                      |
| <span data-ttu-id="1a4ae-141">RGB</span><span class="sxs-lookup"><span data-stu-id="1a4ae-141">RGB</span></span>        | <span data-ttu-id="1a4ae-142">DWORD</span><span class="sxs-lookup"><span data-stu-id="1a4ae-142">DWORD</span></span> | <span data-ttu-id="1a4ae-143">0x0 –0xFFFFFF</span><span class="sxs-lookup"><span data-stu-id="1a4ae-143">0x0 – 0xFFFFFF</span></span>        | <span data-ttu-id="1a4ae-144">按鍵的色彩。</span><span class="sxs-lookup"><span data-stu-id="1a4ae-144">The color on which to key.</span></span> <span data-ttu-id="1a4ae-145">此值為十六進位數位，格式為 0x *RRGGBB*，其中 *RR* 為紅色值， *GG* 為綠色值，而 *BB* 為藍色值。</span><span class="sxs-lookup"><span data-stu-id="1a4ae-145">The value is a hexadecimal number with the format 0x *RRGGBB*, where *RR* is the red value, *GG* is the green value, and *BB* is the blue value.</span></span> <span data-ttu-id="1a4ae-146"> (純紅色、綠色和藍色分別為0xFF0000、0x00FF00 和0x0000FF。 ) </span><span class="sxs-lookup"><span data-stu-id="1a4ae-146">(Pure red, green, and blue are 0xFF0000, 0x00FF00, and 0x0000FF, respectively.)</span></span> | <span data-ttu-id="1a4ae-147">色度</span><span class="sxs-lookup"><span data-stu-id="1a4ae-147">Chroma</span></span>                         |
| <span data-ttu-id="1a4ae-148">相似度</span><span class="sxs-lookup"><span data-stu-id="1a4ae-148">Similarity</span></span> | <span data-ttu-id="1a4ae-149">int</span><span class="sxs-lookup"><span data-stu-id="1a4ae-149">int</span></span>   | <span data-ttu-id="1a4ae-150">0–100</span><span class="sxs-lookup"><span data-stu-id="1a4ae-150">0–100</span></span>                 | <span data-ttu-id="1a4ae-151">變成透明的色彩資料範圍。</span><span class="sxs-lookup"><span data-stu-id="1a4ae-151">The range of color data that becomes transparent.</span></span> <span data-ttu-id="1a4ae-152">在較高的值中，較大範圍的相似色彩是透明的。</span><span class="sxs-lookup"><span data-stu-id="1a4ae-152">At higher values, a wider range of similar colors is transparent.</span></span>                                                                                                                                        | <span data-ttu-id="1a4ae-153">色度、Nonred</span><span class="sxs-lookup"><span data-stu-id="1a4ae-153">Chroma, Nonred</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="1a4ae-154">備註</span><span class="sxs-lookup"><span data-stu-id="1a4ae-154">Remarks</span></span>

<span data-ttu-id="1a4ae-155">執行的索引鍵類型取決於 **KeyType** 屬性的值，必須是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="1a4ae-155">The type of key that is performed depends on the value of the **KeyType** property, which must be one of the following:</span></span>



| <span data-ttu-id="1a4ae-156">值</span><span class="sxs-lookup"><span data-stu-id="1a4ae-156">Value</span></span> | <span data-ttu-id="1a4ae-157">列舉型別</span><span class="sxs-lookup"><span data-stu-id="1a4ae-157">Enumeration</span></span>       | <span data-ttu-id="1a4ae-158">描述</span><span class="sxs-lookup"><span data-stu-id="1a4ae-158">Description</span></span>                                           |
|-------|-------------------|-------------------------------------------------------|
| <span data-ttu-id="1a4ae-159">0</span><span class="sxs-lookup"><span data-stu-id="1a4ae-159">0</span></span>     | <span data-ttu-id="1a4ae-160">DXTKEY \_ RGB</span><span class="sxs-lookup"><span data-stu-id="1a4ae-160">DXTKEY\_RGB</span></span>       | <span data-ttu-id="1a4ae-161">以 RGB 值 (按鍵) 的色度按鍵。</span><span class="sxs-lookup"><span data-stu-id="1a4ae-161">Chroma key (key by RGB value).</span></span>                        |
| <span data-ttu-id="1a4ae-162">1</span><span class="sxs-lookup"><span data-stu-id="1a4ae-162">1</span></span>     | <span data-ttu-id="1a4ae-163">DXTKEY \_ NONRED</span><span class="sxs-lookup"><span data-stu-id="1a4ae-163">DXTKEY\_NONRED</span></span>    | <span data-ttu-id="1a4ae-164">Nonred 鍵。</span><span class="sxs-lookup"><span data-stu-id="1a4ae-164">Nonred key.</span></span> <span data-ttu-id="1a4ae-165"> (使藍和綠區域透明。 ) </span><span class="sxs-lookup"><span data-stu-id="1a4ae-165">(Makes blue and green areas transparent.)</span></span> |
| <span data-ttu-id="1a4ae-166">2</span><span class="sxs-lookup"><span data-stu-id="1a4ae-166">2</span></span>     | <span data-ttu-id="1a4ae-167">DXTKEY \_ 亮度</span><span class="sxs-lookup"><span data-stu-id="1a4ae-167">DXTKEY\_LUMINANCE</span></span> | <span data-ttu-id="1a4ae-168">亮度索引鍵。</span><span class="sxs-lookup"><span data-stu-id="1a4ae-168">Luminance key.</span></span>                                        |
| <span data-ttu-id="1a4ae-169">3</span><span class="sxs-lookup"><span data-stu-id="1a4ae-169">3</span></span>     | <span data-ttu-id="1a4ae-170">DXTKEY \_ ALPHA</span><span class="sxs-lookup"><span data-stu-id="1a4ae-170">DXTKEY\_ALPHA</span></span>     | <span data-ttu-id="1a4ae-171">依字母值的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="1a4ae-171">Key by alpha value.</span></span>                                   |
| <span data-ttu-id="1a4ae-172">4</span><span class="sxs-lookup"><span data-stu-id="1a4ae-172">4</span></span>     | <span data-ttu-id="1a4ae-173">DXTKEY \_ 色調</span><span class="sxs-lookup"><span data-stu-id="1a4ae-173">DXTKEY\_HUE</span></span>       | <span data-ttu-id="1a4ae-174">按鍵（依色調）。</span><span class="sxs-lookup"><span data-stu-id="1a4ae-174">Key by hue.</span></span>                                           |



 

<span data-ttu-id="1a4ae-175">索引鍵類型預設為 DXTKEY \_ ALPHA。</span><span class="sxs-lookup"><span data-stu-id="1a4ae-175">The key type defaults to DXTKEY\_ALPHA.</span></span>

 

 



