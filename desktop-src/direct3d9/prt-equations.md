---
description: 若要完全瞭解執行 PRT 的著色器，請先衍生出著色器用來計算 exit radiance 的公式。
ms.assetid: 66876e9e-cde1-4d04-9b31-30be1c115e6b
title: 'PRT 方 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65559fada82fda7f7eed1c7d05543883a06a19e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109380"
---
# <a name="prt-equations-direct3d-9"></a><span data-ttu-id="ca89e-103">PRT 方 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="ca89e-103">PRT Equations (Direct3D 9)</span></span>

<span data-ttu-id="ca89e-104">若要完全瞭解執行 PRT 的著色器，請先衍生出著色器用來計算 exit radiance 的公式。</span><span class="sxs-lookup"><span data-stu-id="ca89e-104">To fully understand a shader that implements PRT, it is useful to derive the formula the shader uses to calculate exit radiance.</span></span>

<span data-ttu-id="ca89e-105">若要開始，請使用下列方程式，計算在具有任意距離光源的擴散物件上，直接光源所產生的結束 radiance。</span><span class="sxs-lookup"><span data-stu-id="ca89e-105">To start off, the following equation is the general equation to calculate exit radiance resulting from direct lighting on a diffuse object with arbitrary distant lighting.</span></span>

![結束 radiance 的方程式，由具有任意距離光線的擴散物件上的直接光源所產生](images/prt-theory-eq1.png)

<span data-ttu-id="ca89e-107">其中：</span><span class="sxs-lookup"><span data-stu-id="ca89e-107">where:</span></span>



| <span data-ttu-id="ca89e-108">參數</span><span class="sxs-lookup"><span data-stu-id="ca89e-108">Parameter</span></span>     | <span data-ttu-id="ca89e-109">Description</span><span class="sxs-lookup"><span data-stu-id="ca89e-109">Description</span></span>                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca89e-110">Rp</span><span class="sxs-lookup"><span data-stu-id="ca89e-110">Rₚ</span></span>            | <span data-ttu-id="ca89e-111">位於頂點 p 的結束 radiance。</span><span class="sxs-lookup"><span data-stu-id="ca89e-111">The exit radiance at vertex p.</span></span> <span data-ttu-id="ca89e-112">在網格上的每個頂點上進行評估。</span><span class="sxs-lookup"><span data-stu-id="ca89e-112">Evaluated at every vertex on the mesh.</span></span>                                   |
| <span data-ttu-id="ca89e-113">p<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="ca89e-113">p<sub>d</sub></span></span> | <span data-ttu-id="ca89e-114">介面的 >albedo。</span><span class="sxs-lookup"><span data-stu-id="ca89e-114">The albedo of the surface.</span></span>                                                                              |
| <span data-ttu-id="ca89e-115">pi</span><span class="sxs-lookup"><span data-stu-id="ca89e-115">pi</span></span>            | <span data-ttu-id="ca89e-116">常數，用來做為能源節約正規化因素。</span><span class="sxs-lookup"><span data-stu-id="ca89e-116">A constant, used as an energy conservation normalization factor.</span></span>                                        |
| <span data-ttu-id="ca89e-117">L (s) </span><span class="sxs-lookup"><span data-stu-id="ca89e-117">L(s)</span></span>          | <span data-ttu-id="ca89e-118">燈光環境 (來源 radiance) 。</span><span class="sxs-lookup"><span data-stu-id="ca89e-118">The lighting environment (source radiance).</span></span>                                                             |
| <span data-ttu-id="ca89e-119">Vp ₍ s ₎</span><span class="sxs-lookup"><span data-stu-id="ca89e-119">Vₚ₍ₛ₎</span></span>         | <span data-ttu-id="ca89e-120">點 p 的二進位可見度函數。</span><span class="sxs-lookup"><span data-stu-id="ca89e-120">A binary visibility function for point p.</span></span> <span data-ttu-id="ca89e-121">如果點可以看到燈，則為1，否則為0。</span><span class="sxs-lookup"><span data-stu-id="ca89e-121">It is 1 if the point can see the light, 0 if not.</span></span>             |
| <span data-ttu-id="ca89e-122">Hnp ₍ s ₎</span><span class="sxs-lookup"><span data-stu-id="ca89e-122">Hₙₚ₍ₛ₎</span></span>        | <span data-ttu-id="ca89e-123">Lambert 法則的余弦詞彙。</span><span class="sxs-lookup"><span data-stu-id="ca89e-123">The cosine term from Lambert's law.</span></span> <span data-ttu-id="ca89e-124">等於 max ( (Np ·s) 、0) ，其中 Np 是位於點 p 的法線曲面。</span><span class="sxs-lookup"><span data-stu-id="ca89e-124">Equal to max((Nₚ· s), 0) where Nₚ is the surface normal at point p.</span></span> |
| <span data-ttu-id="ca89e-125">s</span><span class="sxs-lookup"><span data-stu-id="ca89e-125">s</span></span>             | <span data-ttu-id="ca89e-126">在球體上整合的變數。</span><span class="sxs-lookup"><span data-stu-id="ca89e-126">The variable that integrates over the sphere.</span></span>                                                           |



 

<span data-ttu-id="ca89e-127">使用球形的函式（例如球形諧波）時，下列方程式近似于光源環境。</span><span class="sxs-lookup"><span data-stu-id="ca89e-127">Using spherical basis functions, such as spherical harmonics, the following equation approximates the lighting environment.</span></span>

![光源環境的方程式](images/prt-theory-eq2.png)

<span data-ttu-id="ca89e-129">其中：</span><span class="sxs-lookup"><span data-stu-id="ca89e-129">where:</span></span>



| <span data-ttu-id="ca89e-130">參數</span><span class="sxs-lookup"><span data-stu-id="ca89e-130">Parameter</span></span>        | <span data-ttu-id="ca89e-131">Description</span><span class="sxs-lookup"><span data-stu-id="ca89e-131">Description</span></span>                                              |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="ca89e-132">L (s) </span><span class="sxs-lookup"><span data-stu-id="ca89e-132">L(s)</span></span>             | <span data-ttu-id="ca89e-133">燈光環境 (來源 radiance) 。</span><span class="sxs-lookup"><span data-stu-id="ca89e-133">The lighting environment (source radiance).</span></span>              |
| <span data-ttu-id="ca89e-134">i</span><span class="sxs-lookup"><span data-stu-id="ca89e-134">i</span></span>                | <span data-ttu-id="ca89e-135">以基礎函數的數目加總的整數。</span><span class="sxs-lookup"><span data-stu-id="ca89e-135">An integer that sums over the number of basis functions.</span></span> |
| <span data-ttu-id="ca89e-136">O</span><span class="sxs-lookup"><span data-stu-id="ca89e-136">O</span></span>                | <span data-ttu-id="ca89e-137">球形諧波的順序。</span><span class="sxs-lookup"><span data-stu-id="ca89e-137">The order of spherical harmonics.</span></span>                        |
| <span data-ttu-id="ca89e-138">l<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="ca89e-138">l<sub>i</sub></span></span>    | <span data-ttu-id="ca89e-139">係數。</span><span class="sxs-lookup"><span data-stu-id="ca89e-139">A coefficient.</span></span>                                           |
| <span data-ttu-id="ca89e-140">Y<sub>i (s) </sub></span><span class="sxs-lookup"><span data-stu-id="ca89e-140">Y<sub>i(s)</sub></span></span> | <span data-ttu-id="ca89e-141">對球體的一些基礎函數。</span><span class="sxs-lookup"><span data-stu-id="ca89e-141">Some basis function over the sphere.</span></span>                     |



 

<span data-ttu-id="ca89e-142">這些係數的集合（L '）提供函數 L (s) 的最佳近似值，其基礎函數為 Y (s) 。</span><span class="sxs-lookup"><span data-stu-id="ca89e-142">The collection of these coefficients, L', provides the optimal approximation for function L(s) with the basis functions Y(s).</span></span> <span data-ttu-id="ca89e-143">替代和散發會產生下列方程式。</span><span class="sxs-lookup"><span data-stu-id="ca89e-143">Substituting and distributing yields the following equation.</span></span>

![替代 l (s) 並散發之後的結束 radiance 方程式](images/prt-theory-eq3.png)

<span data-ttu-id="ca89e-145">Y<sub>i (s </sub>的整數) Vp ₍ s ₎ Hnp ₍ s ₎是模擬器針對網格上每個頂點所 precomputes 的傳輸係數 t<sub>pi</sub> 。</span><span class="sxs-lookup"><span data-stu-id="ca89e-145">The integral of Y<sub>i(s)</sub>Vₚ₍ₛ₎Hₙₚ₍ₛ₎ is a transfer coefficient t<sub>pi</sub> that the simulator precomputes for every vertex on the mesh.</span></span> <span data-ttu-id="ca89e-146">替代此項會產生下列方程式。</span><span class="sxs-lookup"><span data-stu-id="ca89e-146">Substituting this yields the following equation.</span></span>

![替代傳輸係數之後的結束 radiance 方程式](images/prt-theory-eq4.png)

<span data-ttu-id="ca89e-148">將此變更為向量標記法會產生下列未壓縮的方程式，以計算每個通道的結束 radiance。</span><span class="sxs-lookup"><span data-stu-id="ca89e-148">Changing this to vector notation yields the following uncompressed equation to calculate exit radiance for each channel.</span></span>

![變更為向量標記法之後，結束 radiance 的方程式](images/prt-theory-eq5.png)

<span data-ttu-id="ca89e-150">其中：</span><span class="sxs-lookup"><span data-stu-id="ca89e-150">where:</span></span>



| <span data-ttu-id="ca89e-151">參數</span><span class="sxs-lookup"><span data-stu-id="ca89e-151">Parameter</span></span>     | <span data-ttu-id="ca89e-152">Description</span><span class="sxs-lookup"><span data-stu-id="ca89e-152">Description</span></span>                                                                                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca89e-153">Rp</span><span class="sxs-lookup"><span data-stu-id="ca89e-153">Rₚ</span></span>            | <span data-ttu-id="ca89e-154">位於頂點 p 的結束 radiance。</span><span class="sxs-lookup"><span data-stu-id="ca89e-154">The exit radiance at vertex p.</span></span>                                                                                                                                                      |
| <span data-ttu-id="ca89e-155">p<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="ca89e-155">p<sub>d</sub></span></span> | <span data-ttu-id="ca89e-156">介面的 >albedo。</span><span class="sxs-lookup"><span data-stu-id="ca89e-156">The albedo of the surface.</span></span>                                                                                                                                                          |
| <span data-ttu-id="ca89e-157">L</span><span class="sxs-lookup"><span data-stu-id="ca89e-157">L'</span></span>            | <span data-ttu-id="ca89e-158">L<sub>i</sub>的向量，以及將來源 radiance 投射到球形調和基礎函式的投射。</span><span class="sxs-lookup"><span data-stu-id="ca89e-158">The vector of l<sub>i</sub>, and is the projection of the source radiance into the spherical harmonic basis functions.</span></span> <span data-ttu-id="ca89e-159">這是球形調和係數的 order ²向量。</span><span class="sxs-lookup"><span data-stu-id="ca89e-159">This is an order² vector of spherical harmonic coefficients.</span></span> |
| <span data-ttu-id="ca89e-160">Tp</span><span class="sxs-lookup"><span data-stu-id="ca89e-160">Tₚ</span></span>            | <span data-ttu-id="ca89e-161">頂點 p 的 order ²傳送向量。</span><span class="sxs-lookup"><span data-stu-id="ca89e-161">An order² transfer vector for vertex p.</span></span> <span data-ttu-id="ca89e-162">模擬器會將傳輸係數除以 p。</span><span class="sxs-lookup"><span data-stu-id="ca89e-162">The simulator divides the transfer coefficients by p.</span></span>                                                                                       |



 

<span data-ttu-id="ca89e-163">這兩個向量都是球面調和係數的 order ²向量，所以請注意，這只是一個點乘積。</span><span class="sxs-lookup"><span data-stu-id="ca89e-163">Both of these vectors are an order² vector of spherical harmonic coefficients, so notice that this is simply a dot product.</span></span> <span data-ttu-id="ca89e-164">視順序而定，點可能很昂貴，因此可以使用壓縮。</span><span class="sxs-lookup"><span data-stu-id="ca89e-164">Depending on the order, the dot can be expensive so compression can be used.</span></span> <span data-ttu-id="ca89e-165">稱為「叢集主體元件分析」的演算法 (CPCA) 有效率地將資料壓縮。</span><span class="sxs-lookup"><span data-stu-id="ca89e-165">An algorithm called Clustered Principal Component Analysis (CPCA) efficiently compresses the data.</span></span> <span data-ttu-id="ca89e-166">這可讓您使用較高順序的球面調和近似值，以產生更清晰的陰影。</span><span class="sxs-lookup"><span data-stu-id="ca89e-166">This enables the use of a higher-order spherical harmonic approximation which results in sharper shadows.</span></span>

<span data-ttu-id="ca89e-167">CPCA 提供下列方程式，以接近傳輸向量。</span><span class="sxs-lookup"><span data-stu-id="ca89e-167">CPCA provides the following equation to approximate the transfer vector.</span></span>

![近似值傳送向量的方程式](images/prt-theory-eq6.png)

<span data-ttu-id="ca89e-169">其中：</span><span class="sxs-lookup"><span data-stu-id="ca89e-169">where:</span></span>



| <span data-ttu-id="ca89e-170">參數</span><span class="sxs-lookup"><span data-stu-id="ca89e-170">Parameter</span></span>      | <span data-ttu-id="ca89e-171">Description</span><span class="sxs-lookup"><span data-stu-id="ca89e-171">Description</span></span>                                          |
|----------------|------------------------------------------------------|
| <span data-ttu-id="ca89e-172">Tp</span><span class="sxs-lookup"><span data-stu-id="ca89e-172">Tₚ</span></span>             | <span data-ttu-id="ca89e-173">頂點 p 的傳送向量。</span><span class="sxs-lookup"><span data-stu-id="ca89e-173">The transfer vector for vertex p.</span></span>                    |
| <span data-ttu-id="ca89e-174">Mk</span><span class="sxs-lookup"><span data-stu-id="ca89e-174">Mₖ</span></span>             | <span data-ttu-id="ca89e-175">群集 k 的平均值。</span><span class="sxs-lookup"><span data-stu-id="ca89e-175">The mean for cluster k.</span></span>                              |
| <span data-ttu-id="ca89e-176">j</span><span class="sxs-lookup"><span data-stu-id="ca89e-176">j</span></span>              | <span data-ttu-id="ca89e-177">加總 PCA 向量數目的整數。</span><span class="sxs-lookup"><span data-stu-id="ca89e-177">An integer that sums over the number of PCA vectors.</span></span> |
| <span data-ttu-id="ca89e-178">N</span><span class="sxs-lookup"><span data-stu-id="ca89e-178">N</span></span>              | <span data-ttu-id="ca89e-179">PCA 向量的數目。</span><span class="sxs-lookup"><span data-stu-id="ca89e-179">The number of PCA vectors.</span></span>                           |
| <span data-ttu-id="ca89e-180">w<sub>pj</sub></span><span class="sxs-lookup"><span data-stu-id="ca89e-180">w<sub>pj</sub></span></span> | <span data-ttu-id="ca89e-181">點 p 的第 j 個 PCA 加權。</span><span class="sxs-lookup"><span data-stu-id="ca89e-181">The jth PCA weight for point p.</span></span>                      |
| <span data-ttu-id="ca89e-182">B<sub>kj</sub></span><span class="sxs-lookup"><span data-stu-id="ca89e-182">B<sub>kj</sub></span></span> | <span data-ttu-id="ca89e-183">適用于群集 k 的第 j 個 PCA 基礎向量。</span><span class="sxs-lookup"><span data-stu-id="ca89e-183">The jth PCA basis vector for cluster k.</span></span>              |



 

<span data-ttu-id="ca89e-184">群集只是共用相同 mean 向量的一些頂點。</span><span class="sxs-lookup"><span data-stu-id="ca89e-184">A cluster is simply some number of vertices that share the same mean vector.</span></span> <span data-ttu-id="ca89e-185">以下會討論如何取得叢集平均數、PCA 加權、PCA 基礎向量和頂點的叢集識別碼。</span><span class="sxs-lookup"><span data-stu-id="ca89e-185">How to get the cluster mean, the PCA weights, the PCA basis vectors, and the cluster ids for the vertices is discussed below.</span></span>

<span data-ttu-id="ca89e-186">以這兩個方會產生：</span><span class="sxs-lookup"><span data-stu-id="ca89e-186">Substituting these two equations yields:</span></span>

![替代傳送向量之後，exit radiance 的方程式](images/prt-theory-eq7.png)

<span data-ttu-id="ca89e-188">然後，發佈點乘積會產生下列方程式。</span><span class="sxs-lookup"><span data-stu-id="ca89e-188">Then distributing the dot product yields the following equation.</span></span>

![發佈點乘積之後的結束 radiance 方程式](images/prt-theory-eq8.png)

<span data-ttu-id="ca89e-190">因為這兩個 (Mk ·L ' ) 和 (B<sub>kj</sub>·L ' ) 是每個頂點的常數，此範例會以 CPU 計算這些值，並將它們以常數的形式傳遞至頂點著色器;因為 w<sub>pj</sub> 每個頂點的變更，此範例會將每個頂點的資料儲存在頂點緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="ca89e-190">Because both (Mₖ· L') and (B<sub>kj</sub>· L') are constant per vertex, the sample calculates these values with the CPU and passes them as constants into the vertex shader; because w<sub>pj</sub> changes for each vertex, the sample stores this per-vertex data in the vertex buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca89e-191">相關主題</span><span class="sxs-lookup"><span data-stu-id="ca89e-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca89e-192">預先計算 Radiance 傳輸</span><span class="sxs-lookup"><span data-stu-id="ca89e-192">Precomputed Radiance Transfer</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 



