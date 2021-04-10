---
title: 色彩空間轉換
description: 色彩空間轉換
ms.assetid: f5f1ec99-b3b9-4420-bf64-3872d9bbe650
keywords:
- Windows Media Format SDK，色彩空間轉換
- Advanced Systems Format (ASF) 、色彩空間轉換
- ASF (Advanced Systems Format) ，色彩空間轉換
- 色彩空間轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cbc284995cbc72aee148e12977dad9f4476b29c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183495"
---
# <a name="color-space-conversion"></a><span data-ttu-id="28dd5-107">色彩空間轉換</span><span class="sxs-lookup"><span data-stu-id="28dd5-107">Color Space Conversion</span></span>

<span data-ttu-id="28dd5-108">在設定檔和輸入格式中，壓縮影片格式的色彩深度通常會有差異。</span><span class="sxs-lookup"><span data-stu-id="28dd5-108">There is often a difference between the color depth of the compressed video format in the profile and the input format.</span></span> <span data-ttu-id="28dd5-109">發生這種情況時，來源影片必須轉換成符合目的地的色彩空間。</span><span class="sxs-lookup"><span data-stu-id="28dd5-109">When this happens, the source video must be converted to conform to the color space of the destination.</span></span> <span data-ttu-id="28dd5-110">寫入器會處理這個進程，並與內部的色彩空間轉換器進行通訊。</span><span class="sxs-lookup"><span data-stu-id="28dd5-110">The writer handles this process, communicating with an internal color-space converter.</span></span>

<span data-ttu-id="28dd5-111">讀取器也會與色彩空間轉換器通訊，以協調壓縮格式和輸出格式之間的任何差異。</span><span class="sxs-lookup"><span data-stu-id="28dd5-111">The reader also communicates with the color-space converter to reconcile any difference between the compressed format and the output format.</span></span>

<span data-ttu-id="28dd5-112">如同在資料上執行的所有轉換，在色彩深度之間轉換可以減少輸出品質。</span><span class="sxs-lookup"><span data-stu-id="28dd5-112">As with all transforms performed on data, converting between color depths can reduce the quality of the output.</span></span> <span data-ttu-id="28dd5-113">可能的話，您應該使用具有與壓縮格式相同色彩深度的輸入和輸出格式。</span><span class="sxs-lookup"><span data-stu-id="28dd5-113">When possible, you should use input and output formats with the same color depth as the compressed format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28dd5-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="28dd5-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28dd5-115">**檔案寫入功能**</span><span class="sxs-lookup"><span data-stu-id="28dd5-115">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="28dd5-116">**使用輸入**</span><span class="sxs-lookup"><span data-stu-id="28dd5-116">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> <dt>

[<span data-ttu-id="28dd5-117">**使用輸出**</span><span class="sxs-lookup"><span data-stu-id="28dd5-117">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




