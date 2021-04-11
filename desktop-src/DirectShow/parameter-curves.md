---
description: 參數曲線
ms.assetid: c073e7d0-c119-4c36-a5b2-b31dd6326ac8
title: 參數曲線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3c482112c8bd76217f5cbdabdf3cda13b09c3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109512"
---
# <a name="parameter-curves"></a><span data-ttu-id="d5a1d-103">參數曲線</span><span class="sxs-lookup"><span data-stu-id="d5a1d-103">Parameter Curves</span></span>

<span data-ttu-id="d5a1d-104">媒體參數可在一段時間後沿著曲線。</span><span class="sxs-lookup"><span data-stu-id="d5a1d-104">Media parameters are able to follow a curve over time.</span></span> <span data-ttu-id="d5a1d-105">每個曲線都是由數學公式和兩個端點所描述。</span><span class="sxs-lookup"><span data-stu-id="d5a1d-105">Each curve is described by a mathematical formula and two end-points.</span></span> <span data-ttu-id="d5a1d-106">每個端點都是由參考時間和曲線在該時間的值來定義。</span><span class="sxs-lookup"><span data-stu-id="d5a1d-106">Each end-point is defined by a reference time and the value of the curve at that time.</span></span> <span data-ttu-id="d5a1d-107">此公式用來計算點之間的中繼值，並決定曲線的形狀。</span><span class="sxs-lookup"><span data-stu-id="d5a1d-107">The formula is used to calculate intermediate values between the points, and determines the shape of the curve.</span></span> <span data-ttu-id="d5a1d-108">可能的曲線如下：</span><span class="sxs-lookup"><span data-stu-id="d5a1d-108">The possible curves are:</span></span>

-   <span data-ttu-id="d5a1d-109">跳</span><span class="sxs-lookup"><span data-stu-id="d5a1d-109">Jump</span></span>
-   <span data-ttu-id="d5a1d-110">線性</span><span class="sxs-lookup"><span data-stu-id="d5a1d-110">Linear</span></span>
-   <span data-ttu-id="d5a1d-111">Square</span><span class="sxs-lookup"><span data-stu-id="d5a1d-111">Square</span></span>
-   <span data-ttu-id="d5a1d-112">反向正方形</span><span class="sxs-lookup"><span data-stu-id="d5a1d-112">Inverse square</span></span>
-   <span data-ttu-id="d5a1d-113">正弦函數</span><span class="sxs-lookup"><span data-stu-id="d5a1d-113">Sine</span></span>

<span data-ttu-id="d5a1d-114">「跳躍」表示直接跳到結束值。</span><span class="sxs-lookup"><span data-stu-id="d5a1d-114">"Jump" means jump directly to the end value.</span></span> <span data-ttu-id="d5a1d-115">下圖顯示其他曲線。</span><span class="sxs-lookup"><span data-stu-id="d5a1d-115">The other curves are shown in the following diagram.</span></span>

![參數曲線](images/param-curves01.png)

<span data-ttu-id="d5a1d-117">數學曲線的運作方式如下。</span><span class="sxs-lookup"><span data-stu-id="d5a1d-117">Mathematically, the curves work as follows.</span></span> <span data-ttu-id="d5a1d-118">假設某個曲線開始于時間 *t*₀，值為 *v*₀，並在時間 *t*₁的值為 *v*₁時結束。</span><span class="sxs-lookup"><span data-stu-id="d5a1d-118">Suppose that a curve begins at time *t*₀ with a value of *v*₀, and ends at time *t*₁ with a value of *v*₁.</span></span> <span data-ttu-id="d5a1d-119">定義曲線的兩個點是 (*t*₀、 *v*₀) 和 (*t*₁， *v*₁) 。</span><span class="sxs-lookup"><span data-stu-id="d5a1d-119">The two points that define the curve are (*t*₀, *v*₀) and (*t*₁, *v*₁).</span></span>

-   <span data-ttu-id="d5a1d-120">讓Δ *t* 成為曲線的總持續時間， *t*₁–*t*₀。</span><span class="sxs-lookup"><span data-stu-id="d5a1d-120">Let Δ *t* be the total duration of the curve, *t*₁–*t*₀.</span></span>
-   <span data-ttu-id="d5a1d-121">讓Δ *v* 成為開始與結束值（ *v*₁–*v*₀）之間的間隔。</span><span class="sxs-lookup"><span data-stu-id="d5a1d-121">Let Δ *v* be the interval between the starting and ending values, *v*₁–*v*₀.</span></span>
-   <span data-ttu-id="d5a1d-122">在 *任何時候，t* ₀ \**<= *t*  <=  *t*₁，let Δ *t*' = *t*–*t\*₀。</span><span class="sxs-lookup"><span data-stu-id="d5a1d-122">At any time *t* such that *t*₀ <= *t* <= *t*₁, let Δ *t*' = *t*–*t*₀.</span></span>

![參數計算](images/param-curves02.png)

<span data-ttu-id="d5a1d-124">在時間 *t* 的參數值為：</span><span class="sxs-lookup"><span data-stu-id="d5a1d-124">The value of the parameter at time *t* is:</span></span>

<span data-ttu-id="d5a1d-125">*v* = f ( Δ *t*'/Δ *t* ) \* Δ *v*  +  *v*₀</span><span class="sxs-lookup"><span data-stu-id="d5a1d-125">*v* = f( Δ *t*' / Δ *t* ) \* Δ *v* + *v*₀</span></span>

<span data-ttu-id="d5a1d-126">其中 f (x) 是由曲線型別決定的函式：</span><span class="sxs-lookup"><span data-stu-id="d5a1d-126">where f(x) is a function determined by the curve type:</span></span>

-   <span data-ttu-id="d5a1d-127">線性： y = x</span><span class="sxs-lookup"><span data-stu-id="d5a1d-127">Linear: y = x</span></span>
-   <span data-ttu-id="d5a1d-128">正方形： y = x ^ 2</span><span class="sxs-lookup"><span data-stu-id="d5a1d-128">Square: y = x^2</span></span>
-   <span data-ttu-id="d5a1d-129">反向方形： y = sqrt (x) </span><span class="sxs-lookup"><span data-stu-id="d5a1d-129">Inverse square: y = sqrt(x)</span></span>
-   <span data-ttu-id="d5a1d-130">正弦： y = \[ sin (πx –π/2) + 1 \] /2</span><span class="sxs-lookup"><span data-stu-id="d5a1d-130">Sine: y = \[ sin(πx – π/2) + 1 \] / 2</span></span>

<span data-ttu-id="d5a1d-131">觀察Δ *t*' < Δ *t*，所以Δ *t*'/Δ *t* 這個詞彙的範圍是從0到1。</span><span class="sxs-lookup"><span data-stu-id="d5a1d-131">Observe that Δ *t*' < Δ *t*, so the term Δ *t*'/Δ *t* ranges from 0 to 1.</span></span> <span data-ttu-id="d5a1d-132">因此，f (x) 的範圍也是從0到1，而 *v* 一律落在 *v*₀和 *v*₁之間。</span><span class="sxs-lookup"><span data-stu-id="d5a1d-132">Therefore, f(x) also ranges from 0 to 1, and *v* always falls between *v*₀ and *v*₁.</span></span> <span data-ttu-id="d5a1d-133">無論 *v*₀ < *v*₁或反之亦然，都是如此。</span><span class="sxs-lookup"><span data-stu-id="d5a1d-133">This is true whether *v*₀ < *v*₁ or vice versa.</span></span> <span data-ttu-id="d5a1d-134">換句話說，曲線 (*t*₀、 *v*₀、 *t*₁、 *v*₁) 的矩形進行系結。</span><span class="sxs-lookup"><span data-stu-id="d5a1d-134">In other words, the curve is bounded by the rectangle (*t*₀, *v*₀, *t*₁, *v*₁).</span></span>

<span data-ttu-id="d5a1d-135">針對正弦曲線， (πx –π/2 的值) 範圍從–π/2 到π/2，這表示 sin (πx –π/2) 範圍從–1到1。</span><span class="sxs-lookup"><span data-stu-id="d5a1d-135">For the sine curve, the value of (πx – π/2) ranges from –π/2 to π/2, which means that sin(πx – π/2) ranges from –1 to 1.</span></span> <span data-ttu-id="d5a1d-136">然後，結果會正規化，讓 f (x) 落在 (0 – 1) 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="d5a1d-136">The result is then normalized so that f(x) falls into the range (0–1).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5a1d-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="d5a1d-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5a1d-138">媒體參數</span><span class="sxs-lookup"><span data-stu-id="d5a1d-138">Media Parameters</span></span>](media-parameters.md)
</dt> </dl>

 

 



