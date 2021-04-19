---
description: 定義 WIC 中使用的詞彙。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b066757a-8841-4976-b20b-989ebba5eb3b
title: Windows 影像處理元件詞彙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6812024571727c8f769df88f8233119eed13ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001393"
---
# <a name="windows-imaging-component-glossary"></a><span data-ttu-id="1b632-103">Windows 影像處理元件詞彙</span><span class="sxs-lookup"><span data-stu-id="1b632-103">Windows Imaging Component Glossary</span></span>

## <a name="b"></a><span data-ttu-id="1b632-104">B</span><span class="sxs-lookup"><span data-stu-id="1b632-104">B</span></span>

<dl> <dt>

<span data-ttu-id="1b632-105">**位深度**</span><span class="sxs-lookup"><span data-stu-id="1b632-105">**bit depth**</span></span>
</dt> <dd>

<span data-ttu-id="1b632-106">可指定至影像中之單一像素的色彩值數目。</span><span class="sxs-lookup"><span data-stu-id="1b632-106">The number of color values that can be assigned to a single pixel in an image.</span></span> <span data-ttu-id="1b632-107">色彩深度範圍可從 1 位元 (黑白) 到 32 位元 (超過 1670 萬色)。</span><span class="sxs-lookup"><span data-stu-id="1b632-107">Color depth can range from 1 bit (black and white) to 32 bits (over 16.7 million colors).</span></span> <span data-ttu-id="1b632-108">另請參閱：色彩深度</span><span class="sxs-lookup"><span data-stu-id="1b632-108">See also: Color Depth</span></span>

</dd> <dt>

<span data-ttu-id="1b632-109">**每圖元的位數 (bpp)**</span><span class="sxs-lookup"><span data-stu-id="1b632-109">**bits per pixel (bpp)**</span></span>
</dt> <dd>

<span data-ttu-id="1b632-110">表示數位化影像中每個圖元之色彩值的位數。</span><span class="sxs-lookup"><span data-stu-id="1b632-110">The number of bits that represent the color value of each pixel in a digitized image.</span></span> <span data-ttu-id="1b632-111">另請參閱： BPP</span><span class="sxs-lookup"><span data-stu-id="1b632-111">See also:BPP</span></span>

</dd> </dl>

## <a name="c"></a><span data-ttu-id="1b632-112">C</span><span class="sxs-lookup"><span data-stu-id="1b632-112">C</span></span>

<dl> <dt>

<span data-ttu-id="1b632-113">**剪**</span><span class="sxs-lookup"><span data-stu-id="1b632-113">**clipper**</span></span>
</dt> <dd>

<span data-ttu-id="1b632-114">IWICBitmapClipper 物件。</span><span class="sxs-lookup"><span data-stu-id="1b632-114">An IWICBitmapClipper object.</span></span>

</dd> <dt>

<span data-ttu-id="1b632-115">**編 解碼 器**</span><span class="sxs-lookup"><span data-stu-id="1b632-115">**codec**</span></span>
</dt> <dd>

<span data-ttu-id="1b632-116">此篩選會壓縮 (編碼) 或解壓縮 (資料流程) 資料串流。</span><span class="sxs-lookup"><span data-stu-id="1b632-116">A filter that compresses (encodes) or decompresses (decodes) a data stream.</span></span>

</dd> <dt>

<span data-ttu-id="1b632-117">**色彩內容**</span><span class="sxs-lookup"><span data-stu-id="1b632-117">**color context**</span></span>
</dt> <dd>

<span data-ttu-id="1b632-118">色彩設定檔的抽象概念。</span><span class="sxs-lookup"><span data-stu-id="1b632-118">An abstraction for a color profile.</span></span> <span data-ttu-id="1b632-119">您可以從 (ie 的檔案載入設定檔。「sRGB 色彩空間設定檔. icm」 ) 或從讀取所取得的記憶體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1b632-119">The profile can be loaded from a file (ie. "sRGB Color Space Profile.icm") or from a memory buffer obtained by reading.</span></span> <span data-ttu-id="1b632-120">色彩內容資訊是由 WIC 的 IWICColorCoNtext 介面所定義，並使用 GetColorCoNtext 方法來抓取。</span><span class="sxs-lookup"><span data-stu-id="1b632-120">Color context information is defined by the IWICColorContext interface for WIC, and is retrieved with the GetColorContext method.</span></span>

</dd> <dt>

<span data-ttu-id="1b632-121">**色彩轉換**</span><span class="sxs-lookup"><span data-stu-id="1b632-121">**color transform**</span></span>
</dt> <dd>

<span data-ttu-id="1b632-122">以指定的輸出像素格式，將來源色彩內容的色彩對應到目的色彩內容。</span><span class="sxs-lookup"><span data-stu-id="1b632-122">Mapping colors from the source color context to the destination color context in a given output pixel format.</span></span>

</dd> <dt>

<span data-ttu-id="1b632-123">**CYMK 色彩模型**</span><span class="sxs-lookup"><span data-stu-id="1b632-123">**CYMK color model**</span></span>
</dt> <dd>

<span data-ttu-id="1b632-124">多維度色彩空間，由組成指定色彩的青色、洋紅、黃色和黑色濃度所組成。</span><span class="sxs-lookup"><span data-stu-id="1b632-124">Multidimensional color space consisting of the cyan, magenta, yellow, and black intensities that make up a given color.</span></span>

</dd> </dl>

## <a name="d"></a><span data-ttu-id="1b632-125">D</span><span class="sxs-lookup"><span data-stu-id="1b632-125">D</span></span>

<dl> <dt>

<span data-ttu-id="1b632-126">**解碼 器**</span><span class="sxs-lookup"><span data-stu-id="1b632-126">**decoder**</span></span>
</dt> <dd>

<span data-ttu-id="1b632-127">請參閱其他詞彙：編解碼器</span><span class="sxs-lookup"><span data-stu-id="1b632-127">See Other Term: codec</span></span>

</dd> </dl>

## <a name="e"></a><span data-ttu-id="1b632-128">E</span><span class="sxs-lookup"><span data-stu-id="1b632-128">E</span></span>

<dl> <dt>

<span data-ttu-id="1b632-129">**編碼**</span><span class="sxs-lookup"><span data-stu-id="1b632-129">**encoder**</span></span>
</dt> <dd>

<span data-ttu-id="1b632-130">請參閱其他詞彙：編解碼器</span><span class="sxs-lookup"><span data-stu-id="1b632-130">See Other Term: codec</span></span>

</dd> </dl>

## <a name="l"></a><span data-ttu-id="1b632-131">L</span><span class="sxs-lookup"><span data-stu-id="1b632-131">L</span></span>

<dl> <dt>

<span data-ttu-id="1b632-132">**無損**</span><span class="sxs-lookup"><span data-stu-id="1b632-132">**lossless**</span></span>
</dt> <dd>

<span data-ttu-id="1b632-133">一種壓縮類型，可確保原始資料可以完全復原，而不會遺失影像品質。</span><span class="sxs-lookup"><span data-stu-id="1b632-133">A type of compression that ensures that the original data can be recovered exactly, with no loss in image quality.</span></span>

</dd> <dt>

<span data-ttu-id="1b632-134">**有損**</span><span class="sxs-lookup"><span data-stu-id="1b632-134">**lossy**</span></span>
</dt> <dd>

<span data-ttu-id="1b632-135">將被視為不必要資訊的資料壓縮的程式會被移除，而且無法在解壓縮時復原。</span><span class="sxs-lookup"><span data-stu-id="1b632-135">A process for compressing data in which information deemed unnecessary is removed and cannot be recovered upon decompression.</span></span> <span data-ttu-id="1b632-136">通常會搭配音訊和視覺資料使用，在此情況下，品質會稍微降低。</span><span class="sxs-lookup"><span data-stu-id="1b632-136">Typically used with audio and visual data in which a slight degradation of quality is acceptable.</span></span>

</dd> </dl>

## <a name="m"></a><span data-ttu-id="1b632-137">M</span><span class="sxs-lookup"><span data-stu-id="1b632-137">M</span></span>

<dl> <dt>

<span data-ttu-id="1b632-138">**多執行緒單元 (MTA)**</span><span class="sxs-lookup"><span data-stu-id="1b632-138">**multithreaded apartment (MTA)**</span></span>
</dt> <dd>

<span data-ttu-id="1b632-139">元件物件模型 (COM) 所支援的多執行緒形式。</span><span class="sxs-lookup"><span data-stu-id="1b632-139">A form of multithreading that is supported by Component Object Model (COM).</span></span> <span data-ttu-id="1b632-140">在多執行緒單元模型中，進程中已初始化為自由執行緒的所有線程都位於單一單元中。</span><span class="sxs-lookup"><span data-stu-id="1b632-140">In a multithreaded apartment model, all of the threads in the process that have been initialized as free-threaded reside in a single apartment.</span></span>

</dd> </dl>

## <a name="n"></a><span data-ttu-id="1b632-141">N</span><span class="sxs-lookup"><span data-stu-id="1b632-141">N</span></span>

<dl> <dt>

<span data-ttu-id="1b632-142">**原生像素格式**</span><span class="sxs-lookup"><span data-stu-id="1b632-142">**native pixel format**</span></span>
</dt> <dd>

<span data-ttu-id="1b632-143">WIC 提供的其中一個像素格式，其中描述點陣圖中每個圖元的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="1b632-143">One of the pixel formats provided by WIC, wherein the memory layout of each pixel in a bitmap is described.</span></span>

</dd> </dl>

## <a name="p"></a><span data-ttu-id="1b632-144">P</span><span class="sxs-lookup"><span data-stu-id="1b632-144">P</span></span>

<dl> <dt>

<span data-ttu-id="1b632-145">**調色板**</span><span class="sxs-lookup"><span data-stu-id="1b632-145">**palette**</span></span>
</dt> <dd>

<span data-ttu-id="1b632-146">物件或應用程式所使用的色彩集合。</span><span class="sxs-lookup"><span data-stu-id="1b632-146">Set of colors used by an object or application.</span></span>

</dd> <dt>

<span data-ttu-id="1b632-147">**相片中繼資料原則**</span><span class="sxs-lookup"><span data-stu-id="1b632-147">**photo metadata policy**</span></span>
</dt> <dd>

<span data-ttu-id="1b632-148">用於讀取、寫入和移除映射中繼資料的 windows 原則。</span><span class="sxs-lookup"><span data-stu-id="1b632-148">The windows policy for reading, writing, and removing image metadata.</span></span>

</dd> <dt>

<span data-ttu-id="1b632-149">**像素格式**</span><span class="sxs-lookup"><span data-stu-id="1b632-149">**pixel format**</span></span>
</dt> <dd>

<span data-ttu-id="1b632-150">記憶體中圖元色彩元件的大小和相片順序。</span><span class="sxs-lookup"><span data-stu-id="1b632-150">Size and arrangement of pixel color components in memory.</span></span> <span data-ttu-id="1b632-151">它是以每個圖元使用的總位數以及用來儲存色彩紅色、綠色、藍色和 Alpha 元件的位數來指定。</span><span class="sxs-lookup"><span data-stu-id="1b632-151">It is specified by the total number of bits used per pixel and the number of bits used to store the red, green, blue, and alpha components of the color.</span></span> <span data-ttu-id="1b632-152">例如，RGB24 像素格式使用24個位來儲存圖元色彩，每個紅色、綠色和藍色各有8位。</span><span class="sxs-lookup"><span data-stu-id="1b632-152">For example, the RGB24 pixel format uses 24 bits to store a pixel color, with eight bits each for red, green, and blue.</span></span> <span data-ttu-id="1b632-153">ARGB32 像素格式使用32位，具有24位的色彩資訊和8位的 Alpha 色板資訊。</span><span class="sxs-lookup"><span data-stu-id="1b632-153">The ARGB32 pixel format uses 32 bits, with 24 bits of color information and 8 bits of alpha channel information.</span></span>

</dd> <dt>

<span data-ttu-id="1b632-154">**漸進式解碼**</span><span class="sxs-lookup"><span data-stu-id="1b632-154">**progressive decoding**</span></span>
</dt> <dd>

<span data-ttu-id="1b632-155">解碼已使用不同解碼層級相關資訊進行編碼之影像的進程。</span><span class="sxs-lookup"><span data-stu-id="1b632-155">The process for decoding images that have been encoded with information about the different decoding levels.</span></span>

</dd> </dl>

## <a name="s"></a><span data-ttu-id="1b632-156">S</span><span class="sxs-lookup"><span data-stu-id="1b632-156">S</span></span>

<dl> <dt>

<span data-ttu-id="1b632-157">**流**</span><span class="sxs-lookup"><span data-stu-id="1b632-157">**stream**</span></span>
</dt> <dd>

<span data-ttu-id="1b632-158">是指可用於依序讀取或寫入檔案、記憶體或網路位置之資料的 IStream COM 介面。</span><span class="sxs-lookup"><span data-stu-id="1b632-158">Refers to an IStream COM interface which can be used to sequentially read or write data to files, memory, or network locations.</span></span>

</dd> </dl>

## <a name="t"></a><span data-ttu-id="1b632-159">T</span><span class="sxs-lookup"><span data-stu-id="1b632-159">T</span></span>

<dl> <dt>

<span data-ttu-id="1b632-160">**語氣曲線**</span><span class="sxs-lookup"><span data-stu-id="1b632-160">**tone curve**</span></span>
</dt> <dd>

<span data-ttu-id="1b632-161">數位攝影中用來顯示影像色調範圍的圖形。</span><span class="sxs-lookup"><span data-stu-id="1b632-161">A graph used in digital photography that displays the tonal range of the image.</span></span>

</dd> </dl>

## <a name="w"></a><span data-ttu-id="1b632-162">W</span><span class="sxs-lookup"><span data-stu-id="1b632-162">W</span></span>

<dl> <dt>

<span data-ttu-id="1b632-163">**Windows 影像處理元件 (WIC)**</span><span class="sxs-lookup"><span data-stu-id="1b632-163">**Windows Imaging Component (WIC)**</span></span>
</dt> <dd>

<span data-ttu-id="1b632-164">可延伸的平臺，可為數字影像提供低層級的 API。</span><span class="sxs-lookup"><span data-stu-id="1b632-164">An extensible platform that provides low-level API for digital images.</span></span>

</dd> </dl>

 

 



