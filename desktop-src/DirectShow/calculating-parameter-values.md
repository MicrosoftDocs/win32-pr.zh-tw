---
description: 計算參數值
ms.assetid: cc3c26ed-a007-4350-99be-0ebd94953689
title: 計算參數值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89dac0767d7d19bc4331e1a9ee032ec5b3eaae2e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106979706"
---
# <a name="calculating-parameter-values"></a><span data-ttu-id="29f9c-103">計算參數值</span><span class="sxs-lookup"><span data-stu-id="29f9c-103">Calculating Parameter Values</span></span>

<span data-ttu-id="29f9c-104">輸入緩衝區可能非常大。</span><span class="sxs-lookup"><span data-stu-id="29f9c-104">Potentially, an input buffer could be very large.</span></span> <span data-ttu-id="29f9c-105">在理想的情況下，當 SQL-DMO 處理緩衝區時，參數將會在整個批次的資料中完全遵循其曲線。</span><span class="sxs-lookup"><span data-stu-id="29f9c-105">Ideally, when the DMO processes the buffer, the parameters will exactly follow their curves throughout the entire batch of data.</span></span> <span data-ttu-id="29f9c-106">不過，每個一一點時間在計算這些值的方式方面都有一些。</span><span class="sxs-lookup"><span data-stu-id="29f9c-106">However, a DMO has some leeway in how it calculates those values.</span></span>

-   <span data-ttu-id="29f9c-107">最準確的方法是為每個不可部分完成的資料單位計算確切的值;例如，每個音訊範例。</span><span class="sxs-lookup"><span data-stu-id="29f9c-107">The most accurate approach is to calculate the exact value for every atomic unit of data; for example, each audio sample.</span></span> <span data-ttu-id="29f9c-108">這種方法是計算成本最高的方法。</span><span class="sxs-lookup"><span data-stu-id="29f9c-108">This approach is the most computationally expensive.</span></span>
-   <span data-ttu-id="29f9c-109">另一種方法是將資料分割成一些固定大小的較小單位，例如100範例。</span><span class="sxs-lookup"><span data-stu-id="29f9c-109">Another approach is to slice the data into smaller units of some fixed size, such as 100 samples.</span></span> <span data-ttu-id="29f9c-110">這種方法會建立「階梯-逐步執行」效果。</span><span class="sxs-lookup"><span data-stu-id="29f9c-110">This approach creates a "stair-stepping" effect.</span></span> <span data-ttu-id="29f9c-111">某些參數可能是可接受的。</span><span class="sxs-lookup"><span data-stu-id="29f9c-111">For some parameters, that might be acceptable.</span></span> <span data-ttu-id="29f9c-112">在音訊效果中，它可能會建立可聽見的構件。</span><span class="sxs-lookup"><span data-stu-id="29f9c-112">In audio effects, it might create audible artifacts.</span></span>
-   <span data-ttu-id="29f9c-113">折衷的方法是使用先前的技巧，但在每個批次中，針對每個範例執行參數值的線性插補。</span><span class="sxs-lookup"><span data-stu-id="29f9c-113">A compromise is to use the previous technique, but within each batch, perform a linear interpolation of the parameter value for each sample.</span></span>

<span data-ttu-id="29f9c-114">這些問題對於音訊處理特別重要。</span><span class="sxs-lookup"><span data-stu-id="29f9c-114">These issues are especially important for audio processing.</span></span> <span data-ttu-id="29f9c-115">音訊的一秒可能包含每個頻道48000個音訊樣本，這是很多要執行的計算，但 ear 對像是別名之類的成品很敏感。</span><span class="sxs-lookup"><span data-stu-id="29f9c-115">One second of audio might contain 48,000 audio samples per channel, which is a lot of calculations to perform, yet the ear is sensitive to artifacts such as aliasing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29f9c-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="29f9c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29f9c-117">媒體參數</span><span class="sxs-lookup"><span data-stu-id="29f9c-117">Media Parameters</span></span>](media-parameters.md)
</dt> </dl>

 

 



