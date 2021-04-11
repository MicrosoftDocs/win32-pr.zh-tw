---
description: 環境光源感應器的主要感應器資料類型 illuminance 在 lux 中，每個正方形計量)  (的流明。 本主題所述的原則是以將 lux 值做為輸入，並在程式中回應該資料的基礎。
ms.assetid: 29855779-7c27-4cfe-b8af-b33bc86a1f62
title: 瞭解和解讀 Lux 值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8012f983eeac29cc07b18ac2d27918d2df6ed52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027086"
---
# <a name="understanding-and-interpreting-lux-values"></a><span data-ttu-id="4146d-104">瞭解和解讀 Lux 值</span><span class="sxs-lookup"><span data-stu-id="4146d-104">Understanding and Interpreting Lux Values</span></span>

<span data-ttu-id="4146d-105">環境光源感應器的主要感應器資料類型 illuminance 在 lux 中，每個正方形計量)  (的流明。</span><span class="sxs-lookup"><span data-stu-id="4146d-105">The primary sensor data type for ambient light sensors is illuminance in lux (lumens per square meter).</span></span> <span data-ttu-id="4146d-106">本主題所述的原則是以將 lux 值做為輸入，並在程式中回應該資料的基礎。</span><span class="sxs-lookup"><span data-stu-id="4146d-106">The principles outlined in this topic are based on taking lux values as input and reacting to that data in a program.</span></span>

<span data-ttu-id="4146d-107">Lux 讀數會與每秒吸收的每個平方計量表直接成正比。</span><span class="sxs-lookup"><span data-stu-id="4146d-107">Lux readings are directly proportional to the energy per square meter that is absorbed per second.</span></span> <span data-ttu-id="4146d-108">人們對光線等級的認知並不是那麼簡單。</span><span class="sxs-lookup"><span data-stu-id="4146d-108">Human perception of light levels is not so straightforward.</span></span> <span data-ttu-id="4146d-109">人們對光線的認知很複雜，因為我們的眼睛不斷調整，而其他生物處理常式會影響我們的認知。</span><span class="sxs-lookup"><span data-stu-id="4146d-109">Human perception of light is complicated because our eyes are constantly adjusting and other biological processes are affecting our perception.</span></span> <span data-ttu-id="4146d-110">不過，我們可以利用已知的上限和下限來建立數個感興趣的範圍，以簡化的觀點來思考這項認知。</span><span class="sxs-lookup"><span data-stu-id="4146d-110">However, we can think of this perception from a simplified perspective by creating several ranges of interest with known upper and lower thresholds.</span></span>

<span data-ttu-id="4146d-111">下列範例資料集代表一般光源條件的粗略臨界值，以及對應的光源步驟。</span><span class="sxs-lookup"><span data-stu-id="4146d-111">The following example data set represents rough thresholds for common lighting conditions, and the corresponding lighting step.</span></span> <span data-ttu-id="4146d-112">在這裡，每個光源步驟都代表光源環境中的變更。</span><span class="sxs-lookup"><span data-stu-id="4146d-112">Here, each lighting step represents a change in lighting environment.</span></span>

> [!Note]  
> <span data-ttu-id="4146d-113">此資料集適用于說明，對所有使用者或情況而言可能不完全正確。</span><span class="sxs-lookup"><span data-stu-id="4146d-113">This data set is for illustration and may not be completely accurate for all users or situations.</span></span>

 



| <span data-ttu-id="4146d-114">光源條件</span><span class="sxs-lookup"><span data-stu-id="4146d-114">Lighting condition</span></span> | <span data-ttu-id="4146d-115">從 (lux) </span><span class="sxs-lookup"><span data-stu-id="4146d-115">From (lux)</span></span> | <span data-ttu-id="4146d-116">若要 (lux) </span><span class="sxs-lookup"><span data-stu-id="4146d-116">To (lux)</span></span> | <span data-ttu-id="4146d-117">平均值 (lux) </span><span class="sxs-lookup"><span data-stu-id="4146d-117">Mean value (lux)</span></span> | <span data-ttu-id="4146d-118">光源步驟</span><span class="sxs-lookup"><span data-stu-id="4146d-118">Lighting step</span></span> |
|--------------------|------------|----------|------------------|---------------|
| <span data-ttu-id="4146d-119">音調黑色</span><span class="sxs-lookup"><span data-stu-id="4146d-119">Pitch Black</span></span>        | <span data-ttu-id="4146d-120">0</span><span class="sxs-lookup"><span data-stu-id="4146d-120">0</span></span>          | <span data-ttu-id="4146d-121">10</span><span class="sxs-lookup"><span data-stu-id="4146d-121">10</span></span>       | <span data-ttu-id="4146d-122">5</span><span class="sxs-lookup"><span data-stu-id="4146d-122">5</span></span>                | <span data-ttu-id="4146d-123">1</span><span class="sxs-lookup"><span data-stu-id="4146d-123">1</span></span>             |
| <span data-ttu-id="4146d-124">非常深</span><span class="sxs-lookup"><span data-stu-id="4146d-124">Very Dark</span></span>          | <span data-ttu-id="4146d-125">11</span><span class="sxs-lookup"><span data-stu-id="4146d-125">11</span></span>         | <span data-ttu-id="4146d-126">50</span><span class="sxs-lookup"><span data-stu-id="4146d-126">50</span></span>       | <span data-ttu-id="4146d-127">30</span><span class="sxs-lookup"><span data-stu-id="4146d-127">30</span></span>               | <span data-ttu-id="4146d-128">2</span><span class="sxs-lookup"><span data-stu-id="4146d-128">2</span></span>             |
| <span data-ttu-id="4146d-129">深室內</span><span class="sxs-lookup"><span data-stu-id="4146d-129">Dark Indoors</span></span>       | <span data-ttu-id="4146d-130">51</span><span class="sxs-lookup"><span data-stu-id="4146d-130">51</span></span>         | <span data-ttu-id="4146d-131">200</span><span class="sxs-lookup"><span data-stu-id="4146d-131">200</span></span>      | <span data-ttu-id="4146d-132">125</span><span class="sxs-lookup"><span data-stu-id="4146d-132">125</span></span>              | <span data-ttu-id="4146d-133">3</span><span class="sxs-lookup"><span data-stu-id="4146d-133">3</span></span>             |
| <span data-ttu-id="4146d-134">立體室內</span><span class="sxs-lookup"><span data-stu-id="4146d-134">Dim Indoors</span></span>        | <span data-ttu-id="4146d-135">201</span><span class="sxs-lookup"><span data-stu-id="4146d-135">201</span></span>        | <span data-ttu-id="4146d-136">400</span><span class="sxs-lookup"><span data-stu-id="4146d-136">400</span></span>      | <span data-ttu-id="4146d-137">300</span><span class="sxs-lookup"><span data-stu-id="4146d-137">300</span></span>              | <span data-ttu-id="4146d-138">4</span><span class="sxs-lookup"><span data-stu-id="4146d-138">4</span></span>             |
| <span data-ttu-id="4146d-139">一般室內</span><span class="sxs-lookup"><span data-stu-id="4146d-139">Normal Indoors</span></span>     | <span data-ttu-id="4146d-140">401</span><span class="sxs-lookup"><span data-stu-id="4146d-140">401</span></span>        | <span data-ttu-id="4146d-141">1000</span><span class="sxs-lookup"><span data-stu-id="4146d-141">1000</span></span>     | <span data-ttu-id="4146d-142">700</span><span class="sxs-lookup"><span data-stu-id="4146d-142">700</span></span>              | <span data-ttu-id="4146d-143">5</span><span class="sxs-lookup"><span data-stu-id="4146d-143">5</span></span>             |
| <span data-ttu-id="4146d-144">明亮的室內</span><span class="sxs-lookup"><span data-stu-id="4146d-144">Bright Indoors</span></span>     | <span data-ttu-id="4146d-145">1001</span><span class="sxs-lookup"><span data-stu-id="4146d-145">1001</span></span>       | <span data-ttu-id="4146d-146">5000</span><span class="sxs-lookup"><span data-stu-id="4146d-146">5000</span></span>     | <span data-ttu-id="4146d-147">3000</span><span class="sxs-lookup"><span data-stu-id="4146d-147">3000</span></span>             | <span data-ttu-id="4146d-148">6</span><span class="sxs-lookup"><span data-stu-id="4146d-148">6</span></span>             |
| <span data-ttu-id="4146d-149">暗室外</span><span class="sxs-lookup"><span data-stu-id="4146d-149">Dim Outdoors</span></span>       | <span data-ttu-id="4146d-150">5001</span><span class="sxs-lookup"><span data-stu-id="4146d-150">5001</span></span>       | <span data-ttu-id="4146d-151">10,000</span><span class="sxs-lookup"><span data-stu-id="4146d-151">10,000</span></span>   | <span data-ttu-id="4146d-152">7500</span><span class="sxs-lookup"><span data-stu-id="4146d-152">7500</span></span>             | <span data-ttu-id="4146d-153">7</span><span class="sxs-lookup"><span data-stu-id="4146d-153">7</span></span>             |
| <span data-ttu-id="4146d-154">一間的戶外雲</span><span class="sxs-lookup"><span data-stu-id="4146d-154">Cloudy Outdoors</span></span>    | <span data-ttu-id="4146d-155">10001</span><span class="sxs-lookup"><span data-stu-id="4146d-155">10,001</span></span>     | <span data-ttu-id="4146d-156">30,000</span><span class="sxs-lookup"><span data-stu-id="4146d-156">30,000</span></span>   | <span data-ttu-id="4146d-157">20,000</span><span class="sxs-lookup"><span data-stu-id="4146d-157">20,000</span></span>           | <span data-ttu-id="4146d-158">8</span><span class="sxs-lookup"><span data-stu-id="4146d-158">8</span></span>             |
| <span data-ttu-id="4146d-159">直射</span><span class="sxs-lookup"><span data-stu-id="4146d-159">Direct Sunlight</span></span>    | <span data-ttu-id="4146d-160">30001</span><span class="sxs-lookup"><span data-stu-id="4146d-160">30,001</span></span>     | <span data-ttu-id="4146d-161">100,000</span><span class="sxs-lookup"><span data-stu-id="4146d-161">100,000</span></span>  | <span data-ttu-id="4146d-162">65000</span><span class="sxs-lookup"><span data-stu-id="4146d-162">65,000</span></span>           | <span data-ttu-id="4146d-163">9</span><span class="sxs-lookup"><span data-stu-id="4146d-163">9</span></span>             |



 

<span data-ttu-id="4146d-164">如果我們使用此資料表中的 mean 值將此資料視覺化，我們會看到 lux 對照明步驟的關聯性不是線性的，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="4146d-164">If we visualize this data by using the mean values from this table, we see that the lux-to-lighting-step relationship is not linear, as show in the following graph.</span></span>

![線性 illuminance 圖形](images/luxtostep.png)

<span data-ttu-id="4146d-166">但是，如果我們使用 X 軸上的對數刻度來查看這項資料，我們可以看到大約呈線性的關聯性。</span><span class="sxs-lookup"><span data-stu-id="4146d-166">However, if we view this data by using a logarithmic scale on the x-axis, we can see that a roughly linear relationship emerges.</span></span>

![對數 illuminance 圖](images/luxlogtostep.png)

### <a name="an-example-transform"></a><span data-ttu-id="4146d-168">範例轉換</span><span class="sxs-lookup"><span data-stu-id="4146d-168">An Example Transform</span></span>

<span data-ttu-id="4146d-169">根據先前提供的環境光源感應器的範例資料集，您可以抵達下列方程式，將 lux 值對應到人類認知。</span><span class="sxs-lookup"><span data-stu-id="4146d-169">Based on the sample data set for ambient light sensors previously provided, you could arrive at the following equation to map lux values to human perception.</span></span> <span data-ttu-id="4146d-170">在此範例中，預期的值範圍從 0 lux 到 1000000 lux。</span><span class="sxs-lookup"><span data-stu-id="4146d-170">In this example, the expected values range from 0 lux to 1,000,000 lux.</span></span>

![lux 值方程式](images/sensor-lux-equation.jpg)

<span data-ttu-id="4146d-172">此方程式會產生在0.0 和1.0 之間以大致線性方式變化的值。</span><span class="sxs-lookup"><span data-stu-id="4146d-172">This equation results in values that vary in a roughly linear fashion between 0.0 and 1.0.</span></span> <span data-ttu-id="4146d-173">此結果指出人們看過的燈光如何根據先前所顯示的範例資料集而改變。</span><span class="sxs-lookup"><span data-stu-id="4146d-173">This result indicates how human-perceived lighting changed based on the example data set that was shown previously.</span></span>

 

 



