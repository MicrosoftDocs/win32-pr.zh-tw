---
title: CMM 轉換建立旗標
description: Cmm 使用轉換建立旗標作為如何建立色彩轉換的提示。 它是由 CMM 決定最適合使用這些旗標的方式。
ms.assetid: f3942929-272c-4f08-98ac-a4d14d2f6ac4
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852ef5c080c361bfffb6915d808787d46e63ba5c
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/02/2021
ms.locfileid: "106981910"
---
# <a name="cmm-transform-creation-flags"></a><span data-ttu-id="a1892-104">CMM 轉換建立旗標</span><span class="sxs-lookup"><span data-stu-id="a1892-104">CMM Transform Creation Flags</span></span>

<span data-ttu-id="a1892-105">Cmm 使用轉換建立旗標作為如何建立色彩轉換的提示。</span><span class="sxs-lookup"><span data-stu-id="a1892-105">CMMs use transform creation flags as hints for how to create a color transform.</span></span> <span data-ttu-id="a1892-106">它是由 CMM 決定最適合使用這些旗標的方式。</span><span class="sxs-lookup"><span data-stu-id="a1892-106">It is up to the CMM to determine how best to use these flags.</span></span>

<span data-ttu-id="a1892-107">所有使用這些旗標的函式會透過名為 *dwFlags* 的參數來傳遞或接收旗標值。</span><span class="sxs-lookup"><span data-stu-id="a1892-107">All of the functions that use these flags pass or receive flag values through a parameter called *dwFlags*.</span></span> <span data-ttu-id="a1892-108">*DwFlags* 的高序位 **字** 應該設定為下表中的值。</span><span class="sxs-lookup"><span data-stu-id="a1892-108">The high-order **WORD** of *dwFlags* should be set to a value from the following table.</span></span>



| <span data-ttu-id="a1892-109">常數</span><span class="sxs-lookup"><span data-stu-id="a1892-109">Constant</span></span>                    | <span data-ttu-id="a1892-110">描述</span><span class="sxs-lookup"><span data-stu-id="a1892-110">Description</span></span>                                                                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1892-111">啟用 \_ GAMUT \_ 檢查</span><span class="sxs-lookup"><span data-stu-id="a1892-111">ENABLE\_GAMUT\_CHECKING</span></span>     | <span data-ttu-id="a1892-112">使用此轉換進行範圍檢查。</span><span class="sxs-lookup"><span data-stu-id="a1892-112">Use this transform for gamut checking.</span></span>                                                                                                       |
| <span data-ttu-id="a1892-113">使用 \_ 相對 \_ 色度</span><span class="sxs-lookup"><span data-stu-id="a1892-113">USE\_RELATIVE\_COLORIMETRIC</span></span> | <span data-ttu-id="a1892-114">請勿保留白色點。</span><span class="sxs-lookup"><span data-stu-id="a1892-114">Do not preserve the white point.</span></span> <span data-ttu-id="a1892-115">如果輸出 gamut 不支援指定的色彩，請使用最接近的支援色彩。</span><span class="sxs-lookup"><span data-stu-id="a1892-115">If the output gamut does not support a given color, use the nearest supported color.</span></span> <span data-ttu-id="a1892-116">請參閱轉譯意圖。</span><span class="sxs-lookup"><span data-stu-id="a1892-116">See Rendering Intents.</span></span> |
| <span data-ttu-id="a1892-117">快速 \_ 翻譯</span><span class="sxs-lookup"><span data-stu-id="a1892-117">FAST\_TRANSLATE</span></span>             | <span data-ttu-id="a1892-118">只查詢色彩。</span><span class="sxs-lookup"><span data-stu-id="a1892-118">Look up color only.</span></span> <span data-ttu-id="a1892-119">請勿插入色彩。</span><span class="sxs-lookup"><span data-stu-id="a1892-119">Do not interpolate the color.</span></span>                                                                                            |
| <span data-ttu-id="a1892-120">PRESERVEBLACK</span><span class="sxs-lookup"><span data-stu-id="a1892-120">PRESERVEBLACK</span></span>               | <span data-ttu-id="a1892-121">將適當的黑色產生 GMMP 插入轉換序列中的最後一個 GMMP</span><span class="sxs-lookup"><span data-stu-id="a1892-121">Inserts the appropriate black generation GMMP as the last GMMP in the transform sequence</span></span>                                                     |
| <span data-ttu-id="a1892-122">WCS \_ 永遠</span><span class="sxs-lookup"><span data-stu-id="a1892-122">WCS\_ALWAYS</span></span>                 | <span data-ttu-id="a1892-123">即使是針對 ICC 轉換，也請使用 WCS 程式碼路徑。</span><span class="sxs-lookup"><span data-stu-id="a1892-123">Use the WCS code path even for ICC transforms.</span></span>                                                                                               |
| <span data-ttu-id="a1892-124">順序 \_ 轉換</span><span class="sxs-lookup"><span data-stu-id="a1892-124">SEQUENTIAL\_TRANSFORM</span></span>       | <span data-ttu-id="a1892-125">用來建立順序 (非優化) 色彩轉換的轉換建立旗標。</span><span class="sxs-lookup"><span data-stu-id="a1892-125">Transform creation flag for creating a sequential (non-optimized) color transform.</span></span>                                                           |



 

<span data-ttu-id="a1892-126">低序位 **單字** 可以具有下列其中一個常數值。</span><span class="sxs-lookup"><span data-stu-id="a1892-126">The low-order **WORD** can have one of the following constant values.</span></span>



| <span data-ttu-id="a1892-127">常數</span><span class="sxs-lookup"><span data-stu-id="a1892-127">Constant</span></span>     | <span data-ttu-id="a1892-128">描述</span><span class="sxs-lookup"><span data-stu-id="a1892-128">Description</span></span>                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1892-129">證明 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="a1892-129">PROOF\_MODE</span></span>  | <span data-ttu-id="a1892-130">轉換將用來預覽映射。</span><span class="sxs-lookup"><span data-stu-id="a1892-130">Transform will be used to preview the image.</span></span> <span data-ttu-id="a1892-131">影像品質低。</span><span class="sxs-lookup"><span data-stu-id="a1892-131">Low image quality.</span></span>                                    |
| <span data-ttu-id="a1892-132">標準 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="a1892-132">NORMAL\_MODE</span></span> | <span data-ttu-id="a1892-133">轉換將用於一般影像顯示。</span><span class="sxs-lookup"><span data-stu-id="a1892-133">Transform will be used for normal image display.</span></span> <span data-ttu-id="a1892-134">平均影像品質。</span><span class="sxs-lookup"><span data-stu-id="a1892-134">Average image quality.</span></span>                            |
| <span data-ttu-id="a1892-135">最佳 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="a1892-135">BEST\_MODE</span></span>   | <span data-ttu-id="a1892-136">轉換將會用來顯示目標裝置上可能的最高品質影像。</span><span class="sxs-lookup"><span data-stu-id="a1892-136">Transform will be used for the display of the highest-quality image possible on the target device.</span></span> |



 

<span data-ttu-id="a1892-137">從證明 \_ 模式移至最佳 \_ 模式，輸出品質通常會改善，並轉換速度下降。</span><span class="sxs-lookup"><span data-stu-id="a1892-137">Moving from PROOF\_MODE to BEST\_MODE, output quality generally improves and transform speed declines.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1892-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="a1892-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1892-139">基本色彩管理概念</span><span class="sxs-lookup"><span data-stu-id="a1892-139">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="a1892-140">ICM 常數</span><span class="sxs-lookup"><span data-stu-id="a1892-140">ICM Constants</span></span>](wcs-constants.md)
</dt> </dl>

 

 




