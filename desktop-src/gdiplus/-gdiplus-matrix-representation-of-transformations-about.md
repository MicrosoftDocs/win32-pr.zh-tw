---
description: M&\# 215; n 矩陣是以 m 資料列和 n 資料行排列的一組數位。 下圖顯示數個矩陣。
ms.assetid: 62215ae0-b095-42b2-911c-aa7607a8b61a
title: 以矩陣來表示轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0577cae38c401e842cff2ff14179594f9118dfd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690344"
---
# <a name="matrix-representation-of-transformations"></a><span data-ttu-id="23b8d-104">以矩陣來表示轉換</span><span class="sxs-lookup"><span data-stu-id="23b8d-104">Matrix Representation of Transformations</span></span>

<span data-ttu-id="23b8d-105">*M × n* 矩陣是以 *m* 列和 *n* 資料行排列的一組數位。</span><span class="sxs-lookup"><span data-stu-id="23b8d-105">An *m×n* matrix is a set of numbers arranged in *m* rows and *n* columns.</span></span> <span data-ttu-id="23b8d-106">下圖顯示數個矩陣。</span><span class="sxs-lookup"><span data-stu-id="23b8d-106">The following illustration shows several matrices.</span></span>

![顯示不同維度的六個矩陣的圖例](images/aboutgdip05-art04.png)

<span data-ttu-id="23b8d-108">您可以藉由新增個別元素，加入兩個相同大小的矩陣。</span><span class="sxs-lookup"><span data-stu-id="23b8d-108">You can add two matrices of the same size by adding individual elements.</span></span> <span data-ttu-id="23b8d-109">下圖顯示兩個矩陣加法範例。</span><span class="sxs-lookup"><span data-stu-id="23b8d-109">The following illustration shows two examples of matrix addition.</span></span>

![說明如何執行矩陣加法的圖例](images/aboutgdip05-art05.png)

<span data-ttu-id="23b8d-111">*M × n* 矩陣可乘以 *n × p* 矩陣，而結果為 *m × p* 矩陣。</span><span class="sxs-lookup"><span data-stu-id="23b8d-111">An *m×n* matrix can be multiplied by an *n×p* matrix, and the result is an *m×p* matrix.</span></span> <span data-ttu-id="23b8d-112">第一個矩陣中的資料行數目必須與第二個矩陣中的資料列數目相同。</span><span class="sxs-lookup"><span data-stu-id="23b8d-112">The number of columns in the first matrix must be the same as the number of rows in the second matrix.</span></span> <span data-ttu-id="23b8d-113">例如，4×2矩陣可乘以2×3矩陣，以產生4×3矩陣。</span><span class="sxs-lookup"><span data-stu-id="23b8d-113">For example, a 4 ×2 matrix can be multiplied by a 2 ×3 matrix to produce a 4 ×3 matrix.</span></span>

<span data-ttu-id="23b8d-114">您可以將矩陣的平面和資料列和資料行中的點視為向量。</span><span class="sxs-lookup"><span data-stu-id="23b8d-114">Points in the plane and rows and columns of a matrix can be thought of as vectors.</span></span> <span data-ttu-id="23b8d-115">例如， (2，5) 是具有兩個元件的向量，而 (3，7，1) 是具有三個元件的向量。</span><span class="sxs-lookup"><span data-stu-id="23b8d-115">For example, (2, 5) is a vector with two components, and (3, 7, 1) is a vector with three components.</span></span> <span data-ttu-id="23b8d-116">兩個向量的點乘積定義如下：</span><span class="sxs-lookup"><span data-stu-id="23b8d-116">The dot product of two vectors is defined as follows:</span></span>

<span data-ttu-id="23b8d-117"> (a，b) • (c，d) = ac + bd</span><span class="sxs-lookup"><span data-stu-id="23b8d-117">(a, b) • (c, d) = ac + bd</span></span>

<span data-ttu-id="23b8d-118"> (a，b，c) • (d，e，f) = ad + 為 + cf</span><span class="sxs-lookup"><span data-stu-id="23b8d-118">(a, b, c) • (d, e, f) = ad + be + cf</span></span>

<span data-ttu-id="23b8d-119">例如， (2，3) 和 (5 的點乘積，4) 是 (2)  (5) + (3)  (4) = 22。</span><span class="sxs-lookup"><span data-stu-id="23b8d-119">For example, the dot product of (2, 3) and (5, 4) is (2)(5) + (3)(4) = 22.</span></span> <span data-ttu-id="23b8d-120"> (2，5，1) 和 (4，3，1) 的點乘積為 (2)  (4) + (5)  (3) + (1)  (1) = 24。</span><span class="sxs-lookup"><span data-stu-id="23b8d-120">The dot product of (2, 5, 1) and (4, 3, 1) is (2)(4) + (5)(3) + (1)(1) = 24.</span></span> <span data-ttu-id="23b8d-121">請注意，兩個向量的點乘積是數位，而不是另一個向量。</span><span class="sxs-lookup"><span data-stu-id="23b8d-121">Note that the dot product of two vectors is a number, not another vector.</span></span> <span data-ttu-id="23b8d-122">另請注意，只有在兩個向量具有相同數目的元件時，您才可以計算點乘積。</span><span class="sxs-lookup"><span data-stu-id="23b8d-122">Also note that you can calculate the dot product only if the two vectors have the same number of components.</span></span>

<span data-ttu-id="23b8d-123">讓 (i，j) 成為 **第** i 個數據列和 j #**第** 一個資料行中的矩陣 A 專案。</span><span class="sxs-lookup"><span data-stu-id="23b8d-123">Let A(i, j) be the entry in matrix A in the i **th** row and the j **th** column.</span></span> <span data-ttu-id="23b8d-124">例如， (3，2) 是 3 **rd** 資料列和 2 **nd** 資料行中矩陣 A 的專案。</span><span class="sxs-lookup"><span data-stu-id="23b8d-124">For example A(3, 2) is the entry in matrix A in the 3 **rd** row and the 2 **nd** column.</span></span> <span data-ttu-id="23b8d-125">假設 A、B 和 C 是矩陣，而 AB = C。C 的專案計算方式如下：</span><span class="sxs-lookup"><span data-stu-id="23b8d-125">Suppose A, B, and C are matrices, and AB = C. The entries of C are calculated as follows:</span></span>

<span data-ttu-id="23b8d-126">C (i，j) = (的資料列 i) • (a B B 的資料行 j) </span><span class="sxs-lookup"><span data-stu-id="23b8d-126">C(i, j) = (row i of A) • (column j of B)</span></span>

<span data-ttu-id="23b8d-127">下圖顯示數個矩陣乘法範例。</span><span class="sxs-lookup"><span data-stu-id="23b8d-127">The following illustration shows several examples of matrix multiplication.</span></span>

![顯示如何執行矩陣乘法的圖例](images/aboutgdip05-art06.png)

<span data-ttu-id="23b8d-129">如果您將平面中的某個點視為1×2矩陣，您可以藉由將該點乘以2×2矩陣來進行轉換。</span><span class="sxs-lookup"><span data-stu-id="23b8d-129">If you think of a point in the plane as a 1 × 2 matrix, you can transform that point by multiplying it by a 2 × 2 matrix.</span></span> <span data-ttu-id="23b8d-130">下圖顯示套用到點 (2，1) 的數個轉換。</span><span class="sxs-lookup"><span data-stu-id="23b8d-130">The following illustration shows several transformations applied to the point (2, 1).</span></span>

![顯示如何使用矩陣乘法來調整、旋轉或反映平面中某個點的圖例](images/aboutgdip05-art07.png)

<span data-ttu-id="23b8d-132">上圖中顯示的所有轉換都是線性轉換。</span><span class="sxs-lookup"><span data-stu-id="23b8d-132">All the transformations shown in the previous figure are linear transformations.</span></span> <span data-ttu-id="23b8d-133">某些其他轉換（例如平移）並不是線性的，且無法表示為與2×2矩陣相乘。</span><span class="sxs-lookup"><span data-stu-id="23b8d-133">Certain other transformations, such as translation, are not linear, and cannot be expressed as multiplication by a 2 × 2 matrix.</span></span> <span data-ttu-id="23b8d-134">假設您想要開始使用 (2，1) 的點，請將它旋轉90度，將其轉譯為 x 方向的3個單位，並以 y 方向轉譯為4個單位。</span><span class="sxs-lookup"><span data-stu-id="23b8d-134">Suppose you want to start with the point (2, 1), rotate it 90 degrees, translate it 3 units in the x direction, and translate it 4 units in the y direction.</span></span> <span data-ttu-id="23b8d-135">您可以執行矩陣乘法，然後再加上矩陣加法來完成這項操作。</span><span class="sxs-lookup"><span data-stu-id="23b8d-135">You can accomplish this by performing a matrix multiplication followed by a matrix addition.</span></span>

![顯示矩陣乘法和加法如何旋轉點並將其轉譯兩次的圖例](images/aboutgdip05-art08.png)

<span data-ttu-id="23b8d-137">線性轉換 (乘以2×2矩陣) 接著平移 (加上1×2矩陣) 稱為「仿射」轉換。</span><span class="sxs-lookup"><span data-stu-id="23b8d-137">A linear transformation (multiplication by a 2 × 2 matrix) followed by a translation (addition of a 1 × 2 matrix) is called an affine transformation.</span></span> <span data-ttu-id="23b8d-138">另一種方式是將仿射轉換儲存在一組矩陣中 (一個用於線性部分，而另一個用於轉譯) 是在3×3矩陣中儲存整個轉換。</span><span class="sxs-lookup"><span data-stu-id="23b8d-138">An alternative to storing an affine transformation in a pair of matrices (one for the linear part and one for the translation) is to store the entire transformation in a 3 × 3 matrix.</span></span> <span data-ttu-id="23b8d-139">若要進行這項工作，平面中的點必須以虛擬的第三座標儲存在1×3矩陣中。</span><span class="sxs-lookup"><span data-stu-id="23b8d-139">To make this work, a point in the plane must be stored in a 1 × 3 matrix with a dummy 3rd coordinate.</span></span> <span data-ttu-id="23b8d-140">一般的技巧是讓所有的第三個座標等於1。</span><span class="sxs-lookup"><span data-stu-id="23b8d-140">The usual technique is to make all 3rd coordinates equal to 1.</span></span> <span data-ttu-id="23b8d-141">例如，點 (2，1) 是以矩陣 \[ 2 1 1 表示 \] 。</span><span class="sxs-lookup"><span data-stu-id="23b8d-141">For example, the point (2, 1) is represented by the matrix \[2 1 1\].</span></span> <span data-ttu-id="23b8d-142">下圖顯示仿射轉換 (旋轉90度;以 x 方向轉譯3個單位，y 方向的4個單位) 以單一3×3矩陣的乘法表示。</span><span class="sxs-lookup"><span data-stu-id="23b8d-142">The following illustration shows an affine transformation (rotate 90 degrees; translate 3 units in the x direction, 4 units in the y direction) expressed as multiplication by a single 3 × 3 matrix.</span></span>

![顯示矩陣乘法如何執行仿射轉換的圖例](images/aboutgdip05-art09.png)

<span data-ttu-id="23b8d-144">在上述範例中， (2，1) 的點對應到 (2，6) 的點。</span><span class="sxs-lookup"><span data-stu-id="23b8d-144">In the previous example, the point (2, 1) is mapped to the point (2, 6).</span></span> <span data-ttu-id="23b8d-145">請注意，3×3矩陣的第三個數據行包含數位0、0、1。</span><span class="sxs-lookup"><span data-stu-id="23b8d-145">Note that the third column of the 3 × 3 matrix contains the numbers 0, 0, 1.</span></span> <span data-ttu-id="23b8d-146">這一律會是仿射轉換的3×3矩陣的情況。</span><span class="sxs-lookup"><span data-stu-id="23b8d-146">This will always be the case for the 3 × 3 matrix of an affine transformation.</span></span> <span data-ttu-id="23b8d-147">重要的數位是資料行1和2中的六個數字。</span><span class="sxs-lookup"><span data-stu-id="23b8d-147">The important numbers are the six numbers in columns 1 and 2.</span></span> <span data-ttu-id="23b8d-148">矩陣左上2×2部分代表轉換的線性部分，而第三列中的前兩個專案表示轉譯。</span><span class="sxs-lookup"><span data-stu-id="23b8d-148">The upper-left 2 × 2 portion of the matrix represents the linear part of the transformation, and the first two entries in the 3rd row represent the translation.</span></span>

![圖例顯示對仿射轉換的3x3 矩陣而言，前兩個數據行是最重要的](images/aboutgdip05-art10.png)

<span data-ttu-id="23b8d-150">在 Windows GDI + 中，您可以在 [**矩陣**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) 物件中儲存仿射轉換。</span><span class="sxs-lookup"><span data-stu-id="23b8d-150">In Windows GDI+ you can store an affine transformation in a [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object.</span></span> <span data-ttu-id="23b8d-151">由於矩陣的第三個數據行（代表仿射轉換）一律 (0、0、1) ，因此當您建立 **矩陣** 物件時，您只需要在前兩個數據行中指定六個數字。</span><span class="sxs-lookup"><span data-stu-id="23b8d-151">Because the third column of a matrix that represents an affine transformation is always (0, 0, 1), you specify only the six numbers in the first two columns when you construct a **Matrix** object.</span></span> <span data-ttu-id="23b8d-152">語句會建立 `Matrix myMatrix(0.0f, 1.0f, -1.0f, 0.0f, 3.0f, 4.0f);` 上圖所示的矩陣。</span><span class="sxs-lookup"><span data-stu-id="23b8d-152">The statement `Matrix myMatrix(0.0f, 1.0f, -1.0f, 0.0f, 3.0f, 4.0f);` constructs the matrix shown in the previous figure.</span></span>

## <a name="composite-transformations"></a><span data-ttu-id="23b8d-153">複合轉換</span><span class="sxs-lookup"><span data-stu-id="23b8d-153">Composite Transformations</span></span>

<span data-ttu-id="23b8d-154">複合轉換是一種轉換序列，後面接著另一個。</span><span class="sxs-lookup"><span data-stu-id="23b8d-154">A composite transformation is a sequence of transformations, one followed by the other.</span></span> <span data-ttu-id="23b8d-155">請考慮下列清單中的矩陣和轉換：</span><span class="sxs-lookup"><span data-stu-id="23b8d-155">Consider the matrices and transformations in the following list:</span></span>

-   <span data-ttu-id="23b8d-156">矩陣 A 旋轉90度度</span><span class="sxs-lookup"><span data-stu-id="23b8d-156">Matrix A    Rotate 90 degrees</span></span>
-   <span data-ttu-id="23b8d-157">矩陣 B 以 x 方向的2因數來調整</span><span class="sxs-lookup"><span data-stu-id="23b8d-157">Matrix B    Scale by a factor of 2 in the x direction</span></span>
-   <span data-ttu-id="23b8d-158">矩陣 C 以 y 方向轉譯3個單位</span><span class="sxs-lookup"><span data-stu-id="23b8d-158">Matrix C    Translate 3 units in the y direction</span></span>

<span data-ttu-id="23b8d-159">如果您是以矩陣 2 1 1 表示的點 (2，1) （由矩陣表示），然後 \[ \] 再乘 A、B、C，則點 (2，1) 將會依照列出的順序來進行三個轉換。</span><span class="sxs-lookup"><span data-stu-id="23b8d-159">If you start with the point (2, 1) — represented by the matrix \[2 1 1\] — and multiply by A, then B, then C, the point (2,1) will undergo the three transformations in the order listed.</span></span>

<span data-ttu-id="23b8d-160">\[2 1 1 \] ABC = \[ – 2 5 1\]</span><span class="sxs-lookup"><span data-stu-id="23b8d-160">\[2 1 1\]ABC = \[ –2 5 1\]</span></span>

<span data-ttu-id="23b8d-161">與其將複合轉換的三個部分儲存在三個不同的矩陣中，您可以將 A、B 和 C 兩者相乘，以取得儲存整個複合轉換的單一3×3矩陣。</span><span class="sxs-lookup"><span data-stu-id="23b8d-161">Rather than store the three parts of the composite transformation in three separate matrices, you can multiply A, B, and C together to get a single 3 × 3 matrix that stores the entire composite transformation.</span></span> <span data-ttu-id="23b8d-162">假設 ABC = D。然後，點乘以 D 會將相同的結果與點乘 A，然後 B，再加上 C。</span><span class="sxs-lookup"><span data-stu-id="23b8d-162">Suppose ABC = D. Then a point multiplied by D gives the same result as a point multiplied by A, then B, then C.</span></span>

<span data-ttu-id="23b8d-163">\[2 1 1 \] D = \[ – 2 5 1\]</span><span class="sxs-lookup"><span data-stu-id="23b8d-163">\[2 1 1\]D = \[ –2 5 1\]</span></span>

<span data-ttu-id="23b8d-164">下圖顯示矩陣 A、B、C 和 D。</span><span class="sxs-lookup"><span data-stu-id="23b8d-164">The following illustration shows the matrices A, B, C, and D.</span></span>

![圖例顯示如何藉由將組成矩陣相乘來執行多個轉換](images/aboutgdip05-art12.png)

<span data-ttu-id="23b8d-166">您可以藉由將個別的轉換矩陣相乘來形成複合轉換的矩陣，表示任何一系列的仿射轉換都可以儲存在單一 [**矩陣**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) 物件中。</span><span class="sxs-lookup"><span data-stu-id="23b8d-166">The fact that the matrix of a composite transformation can be formed by multiplying the individual transformation matrices means that any sequence of affine transformations can be stored in a single [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object.</span></span>

> [!Note]  
> <span data-ttu-id="23b8d-167">複合轉換的順序很重要。</span><span class="sxs-lookup"><span data-stu-id="23b8d-167">The order of a composite transformation is important.</span></span> <span data-ttu-id="23b8d-168">一般而言，旋轉、接著調整規模，然後轉譯與縮放比例不同，然後旋轉然後轉譯。</span><span class="sxs-lookup"><span data-stu-id="23b8d-168">In general, rotate, then scale, then translate is not the same as scale, then rotate, then translate.</span></span> <span data-ttu-id="23b8d-169">同樣地，矩陣乘法的順序也很重要。</span><span class="sxs-lookup"><span data-stu-id="23b8d-169">Similarly, the order of matrix multiplication is important.</span></span> <span data-ttu-id="23b8d-170">一般來說，ABC 與 k 不同。</span><span class="sxs-lookup"><span data-stu-id="23b8d-170">In general, ABC is not the same as BAC.</span></span>

 

<span data-ttu-id="23b8d-171">[**矩陣**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix)類別提供數種方法來建立複合轉換：[**矩陣：：乘法**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-multiply)、 [**matrix：：旋轉**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotate)、 [**Matrix：： RotateAt**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotateat)、 [**matrix：： Scale**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-scale)、 [**matrix：：切變**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear)和 [**matrix：：轉譯**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-translate)。</span><span class="sxs-lookup"><span data-stu-id="23b8d-171">The [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class provides several methods for building a composite transformation: [**Matrix::Multiply**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-multiply), [**Matrix::Rotate**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotate), [**Matrix::RotateAt**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotateat), [**Matrix::Scale**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-scale), [**Matrix::Shear**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear), and [**Matrix::Translate**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-translate).</span></span> <span data-ttu-id="23b8d-172">下列範例會建立複合轉換的矩陣，其會先旋轉30度，然後在 y 方向以2的因數進行縮放，然後以 x 方向轉譯5個單位。</span><span class="sxs-lookup"><span data-stu-id="23b8d-172">The following example creates the matrix of a composite transformation that first rotates 30 degrees, then scales by a factor of 2 in the y direction, and then translates 5 units in the x direction.</span></span>


```
Matrix myMatrix;
myMatrix.Rotate(30.0f);
myMatrix.Scale(1.0f, 2.0f, MatrixOrderAppend);
myMatrix.Translate(5.0f, 0.0f, MatrixOrderAppend);
```



<span data-ttu-id="23b8d-173">下圖顯示矩陣。</span><span class="sxs-lookup"><span data-stu-id="23b8d-173">The following illustration shows the matrix.</span></span>

![顯示矩陣，其中包含以三角函數表示的值，以及包含這些函式之近似值的矩陣](images/aboutgdip05-art13.png)

 

 



