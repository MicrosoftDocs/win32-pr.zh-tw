---
title: 附錄矩陣轉換
description: 本主題提供2D 圖形的矩陣轉換數學總覽。
ms.assetid: 8cc01f45-dd84-4f3e-a5f2-26edc5cbdfa1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5a9b09f75b17e4baf8afe5e7fde8643c06982f
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/28/2021
ms.locfileid: "104561986"
---
# <a name="appendix-matrix-transforms"></a><span data-ttu-id="7f176-103">附錄：矩陣轉換</span><span class="sxs-lookup"><span data-stu-id="7f176-103">Appendix: Matrix Transforms</span></span>

<span data-ttu-id="7f176-104">本主題提供2D 圖形的矩陣轉換數學總覽。</span><span class="sxs-lookup"><span data-stu-id="7f176-104">This topic provides a mathematical overview of matrix transforms for 2-D graphics.</span></span> <span data-ttu-id="7f176-105">不過，您不需要知道矩陣數學，也可以在 Direct2D 中使用轉換。</span><span class="sxs-lookup"><span data-stu-id="7f176-105">However, you don't need to know matrix math in order to use transforms in Direct2D.</span></span> <span data-ttu-id="7f176-106">如果您對數學有興趣，請閱讀本主題。否則，請隨意略過本主題。</span><span class="sxs-lookup"><span data-stu-id="7f176-106">Read this topic if you are interested in the math; otherwise, feel free to skip this topic.</span></span>

-   [<span data-ttu-id="7f176-107">矩陣簡介</span><span class="sxs-lookup"><span data-stu-id="7f176-107">Introduction to Matrices</span></span>](#introduction-to-matrices)
    -   [<span data-ttu-id="7f176-108">矩陣作業</span><span class="sxs-lookup"><span data-stu-id="7f176-108">Matrix Operations</span></span>](#matrix-operations)
-   [<span data-ttu-id="7f176-109">仿射轉換</span><span class="sxs-lookup"><span data-stu-id="7f176-109">Affine Transforms</span></span>](#affine-transforms)
    -   [<span data-ttu-id="7f176-110">轉譯轉換</span><span class="sxs-lookup"><span data-stu-id="7f176-110">Translation Transform</span></span>](#translation-transform)
    -   [<span data-ttu-id="7f176-111">調整轉換</span><span class="sxs-lookup"><span data-stu-id="7f176-111">Scaling Transform</span></span>](#scaling-transform)
    -   [<span data-ttu-id="7f176-112">繞著原點旋轉</span><span class="sxs-lookup"><span data-stu-id="7f176-112">Rotation Around the Origin</span></span>](#rotation-around-the-origin)
    -   [<span data-ttu-id="7f176-113">圍繞任意點旋轉</span><span class="sxs-lookup"><span data-stu-id="7f176-113">Rotation Around an Arbitrary Point</span></span>](#rotation-around-an-arbitrary-point)
    -   [<span data-ttu-id="7f176-114">扭曲轉換</span><span class="sxs-lookup"><span data-stu-id="7f176-114">Skew Transform</span></span>](#skew-transform)
-   [<span data-ttu-id="7f176-115">代表 Direct2D 中的轉換</span><span class="sxs-lookup"><span data-stu-id="7f176-115">Representing Transforms in Direct2D</span></span>](#representing-transforms-in-direct2d)
-   [<span data-ttu-id="7f176-116">下一步</span><span class="sxs-lookup"><span data-stu-id="7f176-116">Next</span></span>](#next)

## <a name="introduction-to-matrices"></a><span data-ttu-id="7f176-117">矩陣簡介</span><span class="sxs-lookup"><span data-stu-id="7f176-117">Introduction to Matrices</span></span>

<span data-ttu-id="7f176-118">矩陣是實數的矩形陣列。</span><span class="sxs-lookup"><span data-stu-id="7f176-118">A matrix is a rectangular array of real numbers.</span></span> <span data-ttu-id="7f176-119">矩陣的 *順序* 是資料列和資料行的數目。</span><span class="sxs-lookup"><span data-stu-id="7f176-119">The *order* of the matrix is the number of rows and columns.</span></span> <span data-ttu-id="7f176-120">例如，如果矩陣有3個數據列和2個數據行，則順序為3×2。</span><span class="sxs-lookup"><span data-stu-id="7f176-120">For example, if the matrix has 3 rows and 2 columns, the order is 3 × 2.</span></span> <span data-ttu-id="7f176-121">矩陣通常會顯示以方括弧括住的矩陣元素：</span><span class="sxs-lookup"><span data-stu-id="7f176-121">Matrices are usually shown with the matrix elements enclosed in square brackets:</span></span>

![3 x 2 矩陣。](images/matrix01.png)

<span data-ttu-id="7f176-123">標記法：矩陣是以大寫字母來指定。</span><span class="sxs-lookup"><span data-stu-id="7f176-123">Notation: A matrix is designated by a capital letter.</span></span> <span data-ttu-id="7f176-124">元素是由小寫字母所指定。</span><span class="sxs-lookup"><span data-stu-id="7f176-124">Elements are designated by lowercase letters.</span></span> <span data-ttu-id="7f176-125">注標表示元素的資料列和資料行編號。</span><span class="sxs-lookup"><span data-stu-id="7f176-125">Subscripts indicate the row and column number of an element.</span></span> <span data-ttu-id="7f176-126">例如，第一個 *ij* 是矩陣 a 之 i'th 資料列和 j'th 資料行的元素。</span><span class="sxs-lookup"><span data-stu-id="7f176-126">For example, a *ij* is the element at the i'th row and j'th column of the matrix A.</span></span>

<span data-ttu-id="7f176-127">下圖顯示的是 i × j 矩陣，並在矩陣的每個資料格中有個別元素。</span><span class="sxs-lookup"><span data-stu-id="7f176-127">The following diagram shows an i × j matrix, with the individual elements in each cell of the matrix.</span></span>

![具有 i 個數據列和 j 資料行的矩陣。](images/matrix15.png)

### <a name="matrix-operations"></a><span data-ttu-id="7f176-129">矩陣作業</span><span class="sxs-lookup"><span data-stu-id="7f176-129">Matrix Operations</span></span>

<span data-ttu-id="7f176-130">本節說明在矩陣上定義的基本作業。</span><span class="sxs-lookup"><span data-stu-id="7f176-130">This section describes the basic operations defined on matrices.</span></span>

<span data-ttu-id="7f176-131">*加法*。</span><span class="sxs-lookup"><span data-stu-id="7f176-131">*Addition*.</span></span> <span data-ttu-id="7f176-132">藉由加入 A 和 B 的對應元素，即可取得兩個矩陣的加總 + B：</span><span class="sxs-lookup"><span data-stu-id="7f176-132">The sum A + B of two matrices is obtained by adding the corresponding elements of A and B:</span></span>

<dl> <span data-ttu-id="7f176-133">A + b = \[ a *ij* \]  +  \[ b *ij* \]  =  \[ a *ij* + B *ij*\]</span><span class="sxs-lookup"><span data-stu-id="7f176-133">A + B = \[ a *ij* \] + \[ b *ij* \] = \[ a *ij* + b *ij* \]</span></span>
</dl>

<span data-ttu-id="7f176-134">純量 *乘法*。</span><span class="sxs-lookup"><span data-stu-id="7f176-134">*Scalar multiplication*.</span></span> <span data-ttu-id="7f176-135">這項作業會將矩陣乘以實數。</span><span class="sxs-lookup"><span data-stu-id="7f176-135">This operation multiplies a matrix by a real number.</span></span> <span data-ttu-id="7f176-136">假設有一個實數 *，則* 會將 a 的每個元素乘以 *k* 來取得純量產品 kA。</span><span class="sxs-lookup"><span data-stu-id="7f176-136">Given a real number *k*, the scalar product kA is obtained by multiplying every element of A by *k*.</span></span>

<dl> <span data-ttu-id="7f176-137">kA = k \[ a *ij* \]  =  \[ k × a *ij*\]</span><span class="sxs-lookup"><span data-stu-id="7f176-137">kA = k\[ a *ij* \] = \[ k × a *ij* \]</span></span>
</dl>

<span data-ttu-id="7f176-138">*矩陣乘法*。</span><span class="sxs-lookup"><span data-stu-id="7f176-138">*Matrix multiplication*.</span></span> <span data-ttu-id="7f176-139">假設有兩個矩陣 A 和 B 的 order (m x n) 和 (n × p) ，則產品 C = A × B 是訂單 (m × p) 的矩陣，定義如下：</span><span class="sxs-lookup"><span data-stu-id="7f176-139">Given two matrices A and B with order (m × n) and (n × p), the product C = A × B is a matrix with order (m × p), defined as follows:</span></span>

![顯示矩陣乘法的公式。](images/matrix02.png)

<span data-ttu-id="7f176-141">或者，等同：</span><span class="sxs-lookup"><span data-stu-id="7f176-141">or, equivalently:</span></span>

<dl> <span data-ttu-id="7f176-142">c *ij* = a *i* 1 x b1 *j* + a *i* 2 x b2 *j* + ... + a *in* + b *nj*  
</span><span class="sxs-lookup"><span data-stu-id="7f176-142">c *ij* = a *i* 1 x b1 *j* + a *i* 2 x b2 *j* + ... + a *in* + b *nj*  
</span></span></dl>

<span data-ttu-id="7f176-143">也就是說，若要計算每個專案 c *ij*，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="7f176-143">That is, to compute each element c *ij*, do the following:</span></span>

1.  <span data-ttu-id="7f176-144">取得 A 的 i'th 資料列和 B 的 j'th 資料行。</span><span class="sxs-lookup"><span data-stu-id="7f176-144">Take the i'th row of A and the j'th column of B.</span></span>
2.  <span data-ttu-id="7f176-145">將資料列和資料行中的每個元素配對：第一個資料行專案的第一個資料列專案、第二個數據行專案的第二個數據列專案，依此類推。</span><span class="sxs-lookup"><span data-stu-id="7f176-145">Multiply each pair of elements in the row and column: the first row entry by the first column entry, the second row entry by the second column entry, and so forth.</span></span>
3.  <span data-ttu-id="7f176-146">加總結果。</span><span class="sxs-lookup"><span data-stu-id="7f176-146">Sum the result.</span></span>

<span data-ttu-id="7f176-147">以下範例會將 (2 × 2) 矩陣乘以 (2 × 3) 矩陣。</span><span class="sxs-lookup"><span data-stu-id="7f176-147">Here is an example of multiplying a (2 × 2) matrix by a (2 × 3) matrix.</span></span>

![矩陣乘法。](images/matrix03.png)

<span data-ttu-id="7f176-149">矩陣乘法不是可交換的。</span><span class="sxs-lookup"><span data-stu-id="7f176-149">Matrix multiplication is not commutative.</span></span> <span data-ttu-id="7f176-150">也就是說，A × B ≠ B × A。此外，從定義中，它會遵循並非每個矩陣配對都可以相乘。</span><span class="sxs-lookup"><span data-stu-id="7f176-150">That is, A × B ≠ B × A. Also, from the definition it follows that not every pair of matrices can be multiplied.</span></span> <span data-ttu-id="7f176-151">左側矩陣中的資料行數目必須等於右邊矩陣中的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="7f176-151">The number of columns in the left-hand matrix must equal the number of rows in the right-hand matrix.</span></span> <span data-ttu-id="7f176-152">否則，×運算子未定義。</span><span class="sxs-lookup"><span data-stu-id="7f176-152">Otherwise, the × operator is not defined.</span></span>

<span data-ttu-id="7f176-153">*識別矩陣*。</span><span class="sxs-lookup"><span data-stu-id="7f176-153">*Identify matrix*.</span></span> <span data-ttu-id="7f176-154">識別矩陣（指定 I）是定義如下的正方形矩陣：</span><span class="sxs-lookup"><span data-stu-id="7f176-154">An identity matrix, designated I, is a square matrix defined as follows:</span></span>

<dl> <span data-ttu-id="7f176-155">如果 *i* j，我的 *ij* = 1  =  \*\*，否則為0。</span><span class="sxs-lookup"><span data-stu-id="7f176-155">I *ij* = 1 if *i* = *j*, or 0 otherwise.</span></span>  
</dl>

<span data-ttu-id="7f176-156">換句話說，識別矩陣包含每個元素1，其中的資料列編號等於資料行編號，而所有其他元素則為零。</span><span class="sxs-lookup"><span data-stu-id="7f176-156">In other words, an identity matrix contains 1 for each element where the row number equals the column number, and zero for all other elements.</span></span> <span data-ttu-id="7f176-157">例如，以下是3×3身分識別矩陣。</span><span class="sxs-lookup"><span data-stu-id="7f176-157">For example, here is the 3 × 3 identity matrix.</span></span>

![識別矩陣。](images/matrix04.png)

<span data-ttu-id="7f176-159">下列 equalities 會保留任何矩陣 M。</span><span class="sxs-lookup"><span data-stu-id="7f176-159">The following equalities hold for any matrix M.</span></span>

<dl> <span data-ttu-id="7f176-160">M x I = M</span><span class="sxs-lookup"><span data-stu-id="7f176-160">M x I = M</span></span>  
<span data-ttu-id="7f176-161">I x M = M</span><span class="sxs-lookup"><span data-stu-id="7f176-161">I x M = M</span></span>  
</dl>

## <a name="affine-transforms"></a><span data-ttu-id="7f176-162">仿射轉換</span><span class="sxs-lookup"><span data-stu-id="7f176-162">Affine Transforms</span></span>

<span data-ttu-id="7f176-163">*仿射轉換* 是將一個座標空間對應到另一個座標空間的數學運算。</span><span class="sxs-lookup"><span data-stu-id="7f176-163">An *affine transform* is a mathematical operation that maps one coordinate space to another.</span></span> <span data-ttu-id="7f176-164">換句話說，它會將一組點對應到另一組點。</span><span class="sxs-lookup"><span data-stu-id="7f176-164">In other words, it maps one set of points to another set of points.</span></span> <span data-ttu-id="7f176-165">仿射轉換有一些功能可讓它們在電腦圖形中很實用。</span><span class="sxs-lookup"><span data-stu-id="7f176-165">Affine transforms have some features that make them useful in computer graphics.</span></span>

-   <span data-ttu-id="7f176-166">仿射轉換會保留 *共* 的。</span><span class="sxs-lookup"><span data-stu-id="7f176-166">Affine transforms preserve *collinearity*.</span></span> <span data-ttu-id="7f176-167">如果有三個以上的點落在一行，它們仍會形成轉換之後的一行。</span><span class="sxs-lookup"><span data-stu-id="7f176-167">If three or more points fall on a line, they still form a line after the transformation.</span></span> <span data-ttu-id="7f176-168">直條保持直接。</span><span class="sxs-lookup"><span data-stu-id="7f176-168">Straight lines remain straight.</span></span>
-   <span data-ttu-id="7f176-169">兩個仿射轉換的組合是仿射轉換。</span><span class="sxs-lookup"><span data-stu-id="7f176-169">The composition of two affine transforms is an affine transform.</span></span>

<span data-ttu-id="7f176-170">2D 空間的仿射轉換具有下列格式。</span><span class="sxs-lookup"><span data-stu-id="7f176-170">Affine transforms for 2-D space have the following form.</span></span>

![顯示2D 空間的仿射轉換。](images/matrix05.png)

<span data-ttu-id="7f176-172">如果您套用先前指定的矩陣乘法定義，您可以顯示兩個仿射轉換的乘積為另一個仿射轉換。</span><span class="sxs-lookup"><span data-stu-id="7f176-172">If you apply the definition of matrix multiplication given earlier, you can show that the product of two affine transforms is another affine transform.</span></span> <span data-ttu-id="7f176-173">若要使用仿射轉換來轉換2D 點，點會以1×3矩陣表示。</span><span class="sxs-lookup"><span data-stu-id="7f176-173">To transform a 2D point using an affine transform, the point is represented as a 1 × 3 matrix.</span></span>

<dl> <span data-ttu-id="7f176-174">P = \| x y 1 \|</span><span class="sxs-lookup"><span data-stu-id="7f176-174">P = \| x y 1 \|</span></span>  
</dl>

<span data-ttu-id="7f176-175">前兩個元素包含點的 x 和 y 座標。</span><span class="sxs-lookup"><span data-stu-id="7f176-175">The first two elements contain the x and y coordinates of the point.</span></span> <span data-ttu-id="7f176-176">第三個元素會放置1，讓數學運算正常運作。</span><span class="sxs-lookup"><span data-stu-id="7f176-176">The 1 is placed in the third element to make the math work out correctly.</span></span> <span data-ttu-id="7f176-177">若要套用轉換，請將這兩個矩陣相乘，如下所示。</span><span class="sxs-lookup"><span data-stu-id="7f176-177">To apply the transform, multiply the two matrices as follows.</span></span>

<dl> <span data-ttu-id="7f176-178">P ' = P × M</span><span class="sxs-lookup"><span data-stu-id="7f176-178">P' = P × M</span></span>  
</dl>

<span data-ttu-id="7f176-179">這會擴充至下列各項。</span><span class="sxs-lookup"><span data-stu-id="7f176-179">This expands to the following.</span></span>

![仿射轉換。](images/matrix06.png)

<span data-ttu-id="7f176-181">其中</span><span class="sxs-lookup"><span data-stu-id="7f176-181">where</span></span>

<dl> <span data-ttu-id="7f176-182">x ' = ax + cy + e</span><span class="sxs-lookup"><span data-stu-id="7f176-182">x' = ax + cy + e</span></span>  
<span data-ttu-id="7f176-183">y ' = bx + dy + f</span><span class="sxs-lookup"><span data-stu-id="7f176-183">y' = bx + dy + f</span></span>  
</dl>

<span data-ttu-id="7f176-184">若要取得已轉換的點，請採用矩陣 P 的前兩個元素。</span><span class="sxs-lookup"><span data-stu-id="7f176-184">To get the transformed point, take the first two elements of matrix P'.</span></span>

<dl> <span data-ttu-id="7f176-185">p = (x '，y ' ) = (ax + cy + e，bx + dy + f) </span><span class="sxs-lookup"><span data-stu-id="7f176-185">p = (x', y') = (ax + cy + e, bx + dy + f)</span></span>  
</dl>

> [!Note]  
> <span data-ttu-id="7f176-186">1× *n* 矩陣稱為「資料 *列向量*」。</span><span class="sxs-lookup"><span data-stu-id="7f176-186">A 1 × *n* matrix is called a *row vector*.</span></span> <span data-ttu-id="7f176-187">Direct2D 和 Direct3D 都使用資料列向量來代表2D 或3D 空間中的點。</span><span class="sxs-lookup"><span data-stu-id="7f176-187">Direct2D and Direct3D both use row vectors to represent points in 2D or 3D space.</span></span> <span data-ttu-id="7f176-188">您可以使用資料行向量 (*n* × 1) 和轉換轉換矩陣來取得相等的結果。</span><span class="sxs-lookup"><span data-stu-id="7f176-188">You can get an equivalent result by using a column vector (*n* × 1) and transposing the transform matrix.</span></span> <span data-ttu-id="7f176-189">大部分的圖形文字都會使用直條圖向量形式。</span><span class="sxs-lookup"><span data-stu-id="7f176-189">Most graphics texts use the column vector form.</span></span> <span data-ttu-id="7f176-190">本主題提供與 Direct2D 和 Direct3D 一致的資料列向量形式。</span><span class="sxs-lookup"><span data-stu-id="7f176-190">This topic presents the row vector form for consistency with Direct2D and Direct3D.</span></span>

 

<span data-ttu-id="7f176-191">接下來的幾個部分會衍生基本轉換。</span><span class="sxs-lookup"><span data-stu-id="7f176-191">The next several sections derive the basic transforms.</span></span>

### <a name="translation-transform"></a><span data-ttu-id="7f176-192">轉譯轉換</span><span class="sxs-lookup"><span data-stu-id="7f176-192">Translation Transform</span></span>

<span data-ttu-id="7f176-193">轉譯轉換矩陣的格式如下。</span><span class="sxs-lookup"><span data-stu-id="7f176-193">The translation transform matrix has the following form.</span></span>

![轉譯轉換。](images/matrix07.png)

<span data-ttu-id="7f176-195">在此方程式中插入點 *P* 會產生：</span><span class="sxs-lookup"><span data-stu-id="7f176-195">Plugging a point *P* into this equation yields:</span></span>

<dl> <span data-ttu-id="7f176-196">P ' = (*x*  +  *dx*， *y*  +  *dy*) </span><span class="sxs-lookup"><span data-stu-id="7f176-196">P' = (*x* + *dx*, *y* + *dy*)</span></span>
</dl>

<span data-ttu-id="7f176-197">這會對應至 X 軸 (x，y) 在 Y 軸的 X 軸和 *dy* 中由 *dx* 轉譯。</span><span class="sxs-lookup"><span data-stu-id="7f176-197">which corresponds to the point (x, y) translated by *dx* in the X-axis and *dy* in the Y-axis.</span></span>

![顯示兩個點轉譯的圖表。](images/graphics22.png)

### <a name="scaling-transform"></a><span data-ttu-id="7f176-199">調整轉換</span><span class="sxs-lookup"><span data-stu-id="7f176-199">Scaling Transform</span></span>

<span data-ttu-id="7f176-200">縮放變換矩陣的格式如下。</span><span class="sxs-lookup"><span data-stu-id="7f176-200">The scaling transform matrix has the following form.</span></span>

![調整轉換。](images/matrix09.png)

<span data-ttu-id="7f176-202">在此方程式中插入點 *P* 會產生：</span><span class="sxs-lookup"><span data-stu-id="7f176-202">Plugging a point *P* into this equation yields:</span></span>

<dl> <span data-ttu-id="7f176-203">P ' = (*x* ∙ *dx*， *y* ∙ *dy*) </span><span class="sxs-lookup"><span data-stu-id="7f176-203">P' = (*x* ∙ *dx*, *y* ∙ *dy*)</span></span>
</dl>

<span data-ttu-id="7f176-204">這會對應到點 (x，y) 以 *dx* 和 *dy* 來調整。</span><span class="sxs-lookup"><span data-stu-id="7f176-204">which corresponds to the point (x,y) scaled by *dx* and *dy*.</span></span>

![顯示雙點比例的圖表。](images/graphics23.png)

### <a name="rotation-around-the-origin"></a><span data-ttu-id="7f176-206">繞著原點旋轉</span><span class="sxs-lookup"><span data-stu-id="7f176-206">Rotation Around the Origin</span></span>

<span data-ttu-id="7f176-207">沿著原點旋轉點的矩陣具有下列格式。</span><span class="sxs-lookup"><span data-stu-id="7f176-207">The matrix to rotate a point around the origin has the following form.</span></span>

![顯示旋轉轉換的公式。](images/matrix11.png)

<span data-ttu-id="7f176-209">轉換的點為：</span><span class="sxs-lookup"><span data-stu-id="7f176-209">The transformed point is:</span></span>

<dl> <span data-ttu-id="7f176-210">P ' = (*x* CosΘ– ysinΘ， *x* sinΘ + *y* cosΘ) </span><span class="sxs-lookup"><span data-stu-id="7f176-210">P' = (*x* cosΘ – ysinΘ, *x* sinΘ + *y* cosΘ)</span></span>
</dl>

<span data-ttu-id="7f176-211">證明。</span><span class="sxs-lookup"><span data-stu-id="7f176-211">Proof.</span></span> <span data-ttu-id="7f176-212">若要顯示 P ' 代表旋轉，請考慮下圖。</span><span class="sxs-lookup"><span data-stu-id="7f176-212">To show that P' represents a rotation, consider the following diagram.</span></span>

![顯示原點周圍旋轉的圖表。](images/graphics24.png)

<span data-ttu-id="7f176-214">假設︰</span><span class="sxs-lookup"><span data-stu-id="7f176-214">Given:</span></span>

<dl> <dt>

<span data-ttu-id="7f176-215"><span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x，y) </span><span class="sxs-lookup"><span data-stu-id="7f176-215"><span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x,y)</span></span>
</dt> <dd>

<span data-ttu-id="7f176-216">要轉換的原始點。</span><span class="sxs-lookup"><span data-stu-id="7f176-216">The original point to transform.</span></span>

</dd> <dt>

<span data-ttu-id="7f176-217">Φ</span><span class="sxs-lookup"><span data-stu-id="7f176-217">Φ</span></span>
</dt> <dd>

<span data-ttu-id="7f176-218">由線條 (0，0) 到 P 所形成的角度。</span><span class="sxs-lookup"><span data-stu-id="7f176-218">The angle formed by the line (0,0) to P.</span></span>

</dd> <dt>

<span data-ttu-id="7f176-219">Θ</span><span class="sxs-lookup"><span data-stu-id="7f176-219">Θ</span></span>
</dt> <dd>

<span data-ttu-id="7f176-220">用來旋轉與原點 (x，y) 的角度。</span><span class="sxs-lookup"><span data-stu-id="7f176-220">The angle by which to rotate (x,y) about the origin.</span></span>

</dd> <dt>

<span data-ttu-id="7f176-221"><span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P ' = (x '，y ' ) </span><span class="sxs-lookup"><span data-stu-id="7f176-221"><span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P' = (x',y')</span></span>
</dt> <dd>

<span data-ttu-id="7f176-222">已轉換的點。</span><span class="sxs-lookup"><span data-stu-id="7f176-222">The transformed point.</span></span>

</dd> <dt>

<span data-ttu-id="7f176-223"><span id="R"></span><span id="r"></span>R</span><span class="sxs-lookup"><span data-stu-id="7f176-223"><span id="R"></span><span id="r"></span>R</span></span>
</dt> <dd>

<span data-ttu-id="7f176-224">行的長度 (0、0) 至 P。也是旋轉圓形的半徑。</span><span class="sxs-lookup"><span data-stu-id="7f176-224">The length of the line (0,0) to P. Also the radius of the circle of rotation.</span></span>

</dd> </dl>

> [!Note]  
> <span data-ttu-id="7f176-225">此圖表會使用幾何中使用的標準座標系統，其中正面 y 軸會指向。</span><span class="sxs-lookup"><span data-stu-id="7f176-225">This diagram uses the standard coordinate system used in geometry, where the positive y-axis points up.</span></span> <span data-ttu-id="7f176-226">Direct2D 會使用 Windows 座標系統，其中正 y 軸會向下點。</span><span class="sxs-lookup"><span data-stu-id="7f176-226">Direct2D uses the Windows coordinate system, where the positive y-axis points down.</span></span>

 

<span data-ttu-id="7f176-227">X 軸和線條 (0，0) 至 P ' 之間的角度為Φ + Θ。</span><span class="sxs-lookup"><span data-stu-id="7f176-227">The angle between the x-axis and the line (0,0) to P' is Φ + Θ.</span></span> <span data-ttu-id="7f176-228">下列身分識別會保存：</span><span class="sxs-lookup"><span data-stu-id="7f176-228">The following identities hold:</span></span>

<dl> <span data-ttu-id="7f176-229">x = R cosΦ</span><span class="sxs-lookup"><span data-stu-id="7f176-229">x = R cosΦ</span></span>  
<span data-ttu-id="7f176-230">y = R sinΦ</span><span class="sxs-lookup"><span data-stu-id="7f176-230">y = R sinΦ</span></span>  
<span data-ttu-id="7f176-231">x ' = R cos (Φ + Θ) </span><span class="sxs-lookup"><span data-stu-id="7f176-231">x' = R cos(Φ + Θ)</span></span>  
<span data-ttu-id="7f176-232">y ' = R sin (Φ + Θ) </span><span class="sxs-lookup"><span data-stu-id="7f176-232">y' = R sin(Φ+ Θ)</span></span>  
</dl>

<span data-ttu-id="7f176-233">現在以Θ的角度來解決 x ' 和 y '。</span><span class="sxs-lookup"><span data-stu-id="7f176-233">Now solve for x' and y' in terms of Θ.</span></span> <span data-ttu-id="7f176-234">依三角加法公式：</span><span class="sxs-lookup"><span data-stu-id="7f176-234">By the trigonometric addition formulas:</span></span>

<dl> <span data-ttu-id="7f176-235">x ' = R (cosΦcosΘ– sinΦsinΘ) = RcosΦcosΘ– RsinΦsinΘ</span><span class="sxs-lookup"><span data-stu-id="7f176-235">x' = R(cosΦcosΘ – sinΦsinΘ) = RcosΦcosΘ – RsinΦsinΘ</span></span>  
<span data-ttu-id="7f176-236">y ' = R (sinΦcosΘ + cosΦsinΘ) = RsinΦcosΘ + RcosΦsinΘ</span><span class="sxs-lookup"><span data-stu-id="7f176-236">y' = R(sinΦcosΘ + cosΦsinΘ) = RsinΦcosΘ + RcosΦsinΘ</span></span>  
</dl>

<span data-ttu-id="7f176-237">取代，我們取得：</span><span class="sxs-lookup"><span data-stu-id="7f176-237">Substituting, we get:</span></span>

<dl> <span data-ttu-id="7f176-238">x ' = xcosΘ– ysinΘ</span><span class="sxs-lookup"><span data-stu-id="7f176-238">x' = xcosΘ – ysinΘ</span></span>  
<span data-ttu-id="7f176-239">y ' = xsinΘ + ycosΘ</span><span class="sxs-lookup"><span data-stu-id="7f176-239">y' = xsinΘ + ycosΘ</span></span>  
</dl>

<span data-ttu-id="7f176-240">對應至稍早所示的已轉換點 P '。</span><span class="sxs-lookup"><span data-stu-id="7f176-240">which corresponds to the transformed point P' shown earlier.</span></span>

### <a name="rotation-around-an-arbitrary-point"></a><span data-ttu-id="7f176-241">圍繞任意點旋轉</span><span class="sxs-lookup"><span data-stu-id="7f176-241">Rotation Around an Arbitrary Point</span></span>

<span data-ttu-id="7f176-242">若要旋轉 (x，y) 以外的某個點，則會使用下列矩陣。</span><span class="sxs-lookup"><span data-stu-id="7f176-242">To rotate around a point (x,y) other than the origin, the following matrix is used.</span></span>

![旋轉轉換。](images/matrix13.png)

<span data-ttu-id="7f176-244">您可以使用 (x，y) 的點作為來源，來衍生此矩陣。</span><span class="sxs-lookup"><span data-stu-id="7f176-244">You can derive this matrix by taking the point (x,y) to be the origin.</span></span>

![顯示圍繞點旋轉的圖表。](images/graphics25.png)

<span data-ttu-id="7f176-246">讓 (x1，y1) 是旋轉點 (x0 的結果點，y0) 圍繞 (x，y) 的位置。</span><span class="sxs-lookup"><span data-stu-id="7f176-246">Let (x1, y1) be the point that results from rotating the point (x0, y0) around the point (x,y).</span></span> <span data-ttu-id="7f176-247">我們可以依照下列方式衍生 x1。</span><span class="sxs-lookup"><span data-stu-id="7f176-247">We can derive x1 as follows.</span></span>

<dl> <span data-ttu-id="7f176-248">x1 = (x0 – x) cosΘ– (y0 – y) sinΘ + x</span><span class="sxs-lookup"><span data-stu-id="7f176-248">x1 = (x0 – x)cosΘ– (y0 – y)sinΘ + x</span></span>  
<span data-ttu-id="7f176-249">x1 = x0cosΘ– y0sinΘ + \[ (1 – cosΘ) + ysinΘ \]</span><span class="sxs-lookup"><span data-stu-id="7f176-249">x1 = x0cosΘ – y0sinΘ + \[ (1 – cosΘ) + ysinΘ \]</span></span>  
</dl>

<span data-ttu-id="7f176-250">現在使用先前的公式 x1 = ax0 + cy0 + e，將此方程式插回到轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="7f176-250">Now plug this equation back into the transform matrix, using the formula x1 = ax0 + cy0 + e from earlier.</span></span> <span data-ttu-id="7f176-251">使用相同的程式來衍生 y1。</span><span class="sxs-lookup"><span data-stu-id="7f176-251">Use the same procedure to derive y1.</span></span>

### <a name="skew-transform"></a><span data-ttu-id="7f176-252">扭曲轉換</span><span class="sxs-lookup"><span data-stu-id="7f176-252">Skew Transform</span></span>

<span data-ttu-id="7f176-253">扭曲轉換是由四個參數所定義：</span><span class="sxs-lookup"><span data-stu-id="7f176-253">The skew transform is defined by four parameters:</span></span>

-   <span data-ttu-id="7f176-254">Θ：沿著 X 軸扭曲的數量，以 y 軸的角度來測量。</span><span class="sxs-lookup"><span data-stu-id="7f176-254">Θ: The amount to skew along the x-axis, measured as an angle from the y-axis.</span></span>
-   <span data-ttu-id="7f176-255">Φ：沿著 y 軸扭曲的數量，以 X 軸的角度來測量。</span><span class="sxs-lookup"><span data-stu-id="7f176-255">Φ: The amount to skew along the y-axis, measured as an angle from the x-axis.</span></span>
-   <span data-ttu-id="7f176-256"> (*px*、 *.py*) ：執行扭曲的點的 x 和 y 座標。</span><span class="sxs-lookup"><span data-stu-id="7f176-256">(*px*, *py*): The x- and y-coordinates of the point about which the skew is performed.</span></span>

<span data-ttu-id="7f176-257">扭曲轉換會使用下列矩陣。</span><span class="sxs-lookup"><span data-stu-id="7f176-257">The skew transform uses the following matrix.</span></span>

![扭曲轉換。](images/matrix14.png)

<span data-ttu-id="7f176-259">轉換的點為：</span><span class="sxs-lookup"><span data-stu-id="7f176-259">The transformed point is:</span></span>

<dl> <span data-ttu-id="7f176-260">P ' = (*x*  +  *y* tanΘ– *.py* tanΘ、 *y*  +  *x* tanΦ) – *.py* tanΦ</span><span class="sxs-lookup"><span data-stu-id="7f176-260">P' = (*x* + *y* tanΘ – *py* tanΘ, *y* + *x* tanΦ) – *py* tanΦ</span></span>
</dl>

<span data-ttu-id="7f176-261">或等同：</span><span class="sxs-lookup"><span data-stu-id="7f176-261">or equivalently:</span></span>

<dl> <span data-ttu-id="7f176-262">P ' = (*x* + (*y* – *.py*) tanΘ、 *y* + (*x* – *px*) tanΦ) </span><span class="sxs-lookup"><span data-stu-id="7f176-262">P' = (*x* + (*y* – *py*)tanΘ, *y* + (*x* – *px*)tanΦ)</span></span>
</dl>

<span data-ttu-id="7f176-263">若要查看這項轉換的運作方式，請個別考慮每個元件。</span><span class="sxs-lookup"><span data-stu-id="7f176-263">To see how this transform works, consider each component individually.</span></span> <span data-ttu-id="7f176-264">Θ參數會將 x 方向的每個點依等於 tanΘ的數量移動。</span><span class="sxs-lookup"><span data-stu-id="7f176-264">The Θ parameter moves every point in the x direction by an amount equal to tanΘ.</span></span> <span data-ttu-id="7f176-265">下圖顯示Θ和 X 軸扭曲之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="7f176-265">The following diagram shows the relation between Θ and the x-axis skew.</span></span>

![顯示沿著 X 軸扭曲的圖表。](images/graphics26.png)

<span data-ttu-id="7f176-267">以下是套用至矩形的相同扭曲：</span><span class="sxs-lookup"><span data-stu-id="7f176-267">Here is the same skew applied to a rectangle:</span></span>

![套用至矩形時，沿著 X 軸顯示扭曲的圖表。](images/graphics27.png)

<span data-ttu-id="7f176-269">Φ參數的效果相同，但沿著 y 軸：</span><span class="sxs-lookup"><span data-stu-id="7f176-269">The Φ parameter has the same effect, but along the y-axis:</span></span>

![顯示沿著 y 軸扭曲的圖表。](images/graphics28.png)

<span data-ttu-id="7f176-271">下圖顯示套用至矩形的 y 軸扭曲。</span><span class="sxs-lookup"><span data-stu-id="7f176-271">The next diagram shows y-axis skew applied to a rectangle.</span></span>

![圖表會顯示套用至矩形時沿著 y 軸的扭曲。](images/graphics29.png)

<span data-ttu-id="7f176-273">最後，參數 *px* 和 *.py* 會將沿著 X 軸和 y 軸扭曲的中心點移位。</span><span class="sxs-lookup"><span data-stu-id="7f176-273">Finally, the parameters *px* and *py* shift the center point for the skew along the x- and y-axes.</span></span>

## <a name="representing-transforms-in-direct2d"></a><span data-ttu-id="7f176-274">代表 Direct2D 中的轉換</span><span class="sxs-lookup"><span data-stu-id="7f176-274">Representing Transforms in Direct2D</span></span>

<span data-ttu-id="7f176-275">所有 Direct2D 轉換都是仿射轉換。</span><span class="sxs-lookup"><span data-stu-id="7f176-275">All Direct2D transforms are affine transforms.</span></span> <span data-ttu-id="7f176-276">Direct2D 不支援非仿射轉換。</span><span class="sxs-lookup"><span data-stu-id="7f176-276">Direct2D does not support non-affine transforms.</span></span> <span data-ttu-id="7f176-277">轉換會以 [**D2D1 \_ 矩陣 \_ 3X2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) 結構表示。</span><span class="sxs-lookup"><span data-stu-id="7f176-277">Transforms are represented by the [**D2D1\_MATRIX\_3X2\_F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) structure.</span></span> <span data-ttu-id="7f176-278">此結構定義了3×2矩陣。</span><span class="sxs-lookup"><span data-stu-id="7f176-278">This structure defines a 3 × 2 matrix.</span></span> <span data-ttu-id="7f176-279">因為仿射轉換的第三個數據行一律是相同的 (\[ 0、0、1 \]) ，而且因為 Direct2D 不支援非仿射轉換，所以不需要指定整個3×3矩陣。</span><span class="sxs-lookup"><span data-stu-id="7f176-279">Because the third column of an affine transform is always the same (\[0, 0, 1\]), and because Direct2D does not support non-affine transforms, there is no need to specify the entire 3 × 3 matrix.</span></span> <span data-ttu-id="7f176-280">就內部而言，Direct2D 會使用3×3矩陣來計算轉換。</span><span class="sxs-lookup"><span data-stu-id="7f176-280">Internally, Direct2D uses 3 × 3 matrices to compute the transforms.</span></span>

<span data-ttu-id="7f176-281">[**D2D1 \_ 矩陣 \_ 3X2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f)的成員是根據其索引位置進行命名： **\_ 11** 成員是元素 (1、1) 、 **\_ 12** 個成員是元素 (1、2) 等等。</span><span class="sxs-lookup"><span data-stu-id="7f176-281">The members of the [**D2D1\_MATRIX\_3X2\_F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) are named according to their index position: the **\_11** member is element (1,1), the **\_12** member is element (1,2), and so forth.</span></span> <span data-ttu-id="7f176-282">雖然您可以直接將結構成員初始化，但建議您使用 [**D2D1：： Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) 類別。</span><span class="sxs-lookup"><span data-stu-id="7f176-282">Although you can initialize the structure members directly, it is recommended to use the [**D2D1::Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class.</span></span> <span data-ttu-id="7f176-283">這個類別會繼承 **D2D1 \_ 矩陣 \_ 3X2 \_ F** ，並提供 helper 方法來建立任何基本的仿射轉換。</span><span class="sxs-lookup"><span data-stu-id="7f176-283">This class inherits **D2D1\_MATRIX\_3X2\_F** and provides helper methods for creating any of the basic affine transforms.</span></span> <span data-ttu-id="7f176-284">此類別也會定義用來撰寫兩個或多個轉換的 [**運算子 \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) ，如在 Direct2D 中套用 [轉換](applying-transforms-in-direct2d.md)所述。</span><span class="sxs-lookup"><span data-stu-id="7f176-284">The class also defines [**operator\*()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) for composing two or more transforms, as described in [Applying Transforms in Direct2D](applying-transforms-in-direct2d.md).</span></span>

## <a name="next"></a><span data-ttu-id="7f176-285">下一個</span><span class="sxs-lookup"><span data-stu-id="7f176-285">Next</span></span>

[<span data-ttu-id="7f176-286">模組4：使用者輸入</span><span class="sxs-lookup"><span data-stu-id="7f176-286">Module 4. User Input</span></span>](module-4--user-input.md)

 

 